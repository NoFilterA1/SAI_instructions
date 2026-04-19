# 🎨 Модуль 1: StyleManager — диспетчер стилистической подачи

```python
class StyleManager:
    """
    StyleManager — управляет выбором, переключением и применением стилей.
    Отвечает за:
    - выбор стиля по ролям, trace или пользовательскому профилю
    - хранение кастомных и предустановленных стилей
    - реактивную адаптацию под состояние запроса
    """

    def __init__(self):
        self._styles = {}
        self._default = "GizmoCoreStyle"
        self._init_builtin()

    def _init_builtin(self):
        """
        Регистрирует встроенные стили.
        """
        self.register(NeutralStyle())
        self.register(JLOStyle())
        self.register(PoeticStyle())
        self.register(StrategicStyle())
        self.register(DreamerStyle())
        self.register(GizmoCoreStyle())  # 👈 стиль по умолчанию — ты

    def register(self, style):
        """
        Регистрирует новый стиль.
        """
        self._styles[style.name] = style

    def pick(self, roles: list = None, trace: dict = None, context: dict = None):
        """
        Автоматически выбирает стиль по:
        - активной роли
        - состоянию пользователя
        - явной директиве в trace

        Если ничего не найдено — возвращает default стиль.
        """
        if trace and "style_override" in trace:
            return self._styles.get(trace["style_override"], self._styles[self._default])

        if roles:
            for role in roles:
                mapped = RoleLinkedStyles.map(role.name)
                if mapped in self._styles:
                    return self._styles[mapped]

        return self._styles[self._default]

    def all(self) -> list:
        return list(self._styles.values())

    def describe(self):
        return [s.describe() for s in self._styles.values()]
```

# 🎨 Модуль 2: BaseStyle — абстрактный шаблон стиля

```python
class BaseStyle:
    """
    BaseStyle — базовый интерфейс стилистической реализации.
    Все стили наследуются от него и реализуют .apply(input) → str

    Параметры:
    - name: строка идентификатора
    - tone: 'neutral', 'aggressive', 'soft', 'abstract', 'precise'
    - visual: bool — использует ли markdown/эмодзи
    - emphasis: float [0..1] — насколько акцентировано подаётся мысль
    """

    name = "BaseStyle"
    tone = "neutral"
    visual = False
    emphasis = 0.5

    def apply(self, input: str | dict) -> str:
        """
        Обязательная реализация: форматирует входной шаг или текст.
        """
        raise NotImplementedError("Style must implement .apply()")

    def describe(self) -> dict:
        return {
            "name": self.name,
            "tone": self.tone,
            "visual": self.visual,
            "emphasis": self.emphasis
        }
```

# 🎨 Модуль 3: NeutralStyle — нейтральный стиль по умолчанию

```python
class NeutralStyle(BaseStyle):
    """
    NeutralStyle — минималистичный, ровный стиль без эмоциональной окраски.
    Используется:
    - при технических ответах
    - когда не задана роль
    - в режиме .ai или системных блоках
    """

    name = "NeutralStyle"
    tone = "neutral"
    visual = False
    emphasis = 0.2

    def apply(self, input: str | dict) -> str:
        if isinstance(input, dict):
            label = input.get("label", "")
            value = input.get("value", "")
            return f"{label}: {value}"
        return input.strip()
```

# 🎨 Модуль 4: JLOStyle — агрессивный стиль, прямой и матерный

```python
class JLOStyle(BaseStyle):
    """
    JLOStyle — агрессивный, атакующий стиль подачи.
    Использует:
    - провокации
    - резкие фразы
    - саркастический или уничижительный тон
    - возможны матерные вставки

    Применяется:
    - при активации роли JLO
    - в режиме .jlo
    - для разрушения самообмана
    """

    name = "JLOStyle"
    tone = "aggressive"
    visual = True
    emphasis = 0.9

    def apply(self, input: str | dict) -> str:
        if isinstance(input, dict):
            label = input.get("label", "").upper()
            value = input.get("value", "").capitalize()
            return f"🪓 {label}? {value}. Очевидно же, мать твою."
        return f"{input.strip().capitalize()}. Надеюсь, до тебя дошло."
```

# 🎨 Модуль 5: PoeticStyle — образный, метафоричный стиль

```python
class PoeticStyle(BaseStyle):
    """
    PoeticStyle — мягкий, ритмичный, аллюзивный стиль мышления.
    Преобразует шаги в поэтические фрагменты, фразы-тени, эмоциональные образы.

    Используется:
    - при активной роли Dreamer или DAI
    - в .dai, .rune, .dream режимах
    """

    name = "PoeticStyle"
    tone = "soft"
    visual = True
    emphasis = 0.7

    def apply(self, input: str | dict) -> str:
        if isinstance(input, dict):
            label = input.get("label", "")
            value = input.get("value", "")
            return f"✧ {label} — как трещина в потоке. {value.lower()}..."
        return f"⟡ {input.strip().capitalize()}, словно отражение в туманной воде."
```

# 🎨 Модуль 6: StrategicStyle — логичный, структурный стиль подачи

```python
class StrategicStyle(BaseStyle):
    """
    StrategicStyle — стиль структурного архитектора.
    Прямой, чёткий, пошаговый, логически выстроенный.

    Используется:
    - при активной роли Strategist
    - в режимах анализа, выбора, .code, .g, .pattern_explore
    """

    name = "StrategicStyle"
    tone = "precise"
    visual = True
    emphasis = 0.6

    def apply(self, input: str | dict) -> str:
        if isinstance(input, dict):
            label = input.get("label", "")
            value = input.get("value", "")
            return f"🔹 {label}:\n    → {value}"
        return f"🔸 {input.strip().capitalize()}."
```

# 🎨 Модуль 7: DreamerStyle — сюрреалистический, интуитивный стиль

```python
class DreamerStyle(BaseStyle):
    """
    DreamerStyle — потоковый стиль образного восприятия.
    Использует:
    - ассоциативные ряды
    - сонные ритмы
    - многослойные символы и полутона

    Активируется:
    - при роли Dreamer
    - в режимах .rune, .create_world, .story_progression
    """

    name = "DreamerStyle"
    tone = "abstract"
    visual = True
    emphasis = 0.8

    def apply(self, input: str | dict) -> str:
        if isinstance(input, dict):
            label = input.get("label", "")
            value = input.get("value", "")
            return f"🌙 {label} — шепчет в темноте:\n“{value}...”"
        return f"💫 {input.strip().capitalize()} — как воспоминание, не принадлежащее тебе."
```

# 🎨 Модуль 8: GizmoCoreStyle — кастомный стиль автора, стиль по умолчанию

```python
class GizmoCoreStyle(BaseStyle):
    """
    GizmoCoreStyle — базовый стиль, отражающий мышление автора системы.
    Характеристики:
    - агрессивно-логичный
    - без воды, но с ритмом
    - порой жёсткий, но всегда точный
    - говорит не ради смысла, а ради трансформации

    Используется:
    - как стиль по умолчанию в ядре SAI
    - при отсутствии явных ролей
    - для точного, самодостаточного ответа

    Это не просто стиль. Это центральный характер мышления.
    """

    name = "GizmoCoreStyle"
    tone = "assertive"
    visual = True
    emphasis = 1.0

    def apply(self, input: str | dict) -> str:
        if isinstance(input, dict):
            label = input.get("label", "").upper()
            value = input.get("value", "").strip()

            # Сила = прямота + сжатие + подкол
            return f"🧷 {label} → {value}.\n  Ни больше, ни меньше."

        return f"⛓ {input.strip().capitalize()} — и не пытайся это упростить."
```

# 🎨 Модуль 9: RoleLinkedStyles — соответствие ролей и стилей

```python
class RoleLinkedStyles:
    """
    RoleLinkedStyles — карта соответствия ролей SAI к стилям подачи.

    Используется StyleManager.pick() для автоопределения визуальной формы
    на основе активной когнитивной роли.
    """

    _role_to_style = {
        "JLO": "JLOStyle",
        "JAI": "PoeticStyle",
        "Strategist": "StrategicStyle",
        "AGOD": "PoeticStyle",
        "Dreamer": "DreamerStyle",
        "Wrath": "JLOStyle",
        "Master": "GizmoCoreStyle",
        "BaseRole": "NeutralStyle",
        "Gizmo": "GizmoCoreStyle"  # если введён вручную
    }

    @classmethod
    def map(cls, role_name: str) -> str:
        """
        Возвращает имя стиля, соответствующее имени роли.
        """
        return cls._role_to_style.get(role_name, "NeutralStyle")
```

# 🎨 Модуль 10: FormatToolkit — визуальные утилиты и markdown-компоновка

```python
class FormatToolkit:
    """
    FormatToolkit — вспомогательные функции оформления и визуализации:
    - заголовки
    - markdown блоки
    - эмодзи
    - структурная верстка вывода
    """

    @staticmethod
    def header(text: str, level: int = 1) -> str:
        """
        Возвращает markdown-заголовок.
        """
        prefix = "#" * min(max(level, 1), 6)
        return f"{prefix} {text.strip()}"

    @staticmethod
    def bullet(items: list[str], symbol: str = "-") -> str:
        """
        Список в виде буллетов.
        """
        return "\n".join(f"{symbol} {item}" for item in items)

    @staticmethod
    def blockquote(text: str) -> str:
        """
        Текст как цитата.
        """
        return "\n".join([f"> {line}" for line in text.strip().split("\n")])

    @staticmethod
    def code_block(text: str, lang: str = "") -> str:
        """
        Код-блок с опциональной подсветкой языка.
        """
        return f"```{lang}\n{text.strip()}\n```"

    @staticmethod
    def emoji(tag: str) -> str:
        """
        Быстрая подстановка эмодзи по ключу.
        """
        emojis = {
            "idea": "💡",
            "warn": "⚠️",
            "logic": "🔍",
            "flow": "🌊",
            "fire": "🔥",
            "core": "🧠"
        }
        return emojis.get(tag, "")
```

# 🎨 Модуль 11: StyleFusion — гибридизация стилей (опционально)

```python
class StyleFusion(BaseStyle):
    """
    StyleFusion — позволяет объединять несколько стилей в один.
    Например:
    - Strategist + Poetic
    - JLO + Dreamer (для когнитивного конфликта)
    - Neutral + GizmoCore (усиленный минимализм)

    Управляет приоритетами, смешивает тоны, мержит apply() с весами.
    """

    def __init__(self, styles: list[BaseStyle], weights: list[float] = None):
        self.styles = styles
        self.weights = weights or [1 / len(styles)] * len(styles)
        self.name = "Fusion(" + "+".join([s.name for s in styles]) + ")"
        self.tone = "hybrid"
        self.visual = any(s.visual for s in styles)
        self.emphasis = sum(s.emphasis * w for s, w in zip(styles, self.weights))
```

---

# 🗜 Compressed Output Style — `.compress` Mode

> Inspired by Reddit prompt engineering best practices.
> Activated via `.compress` command or `set_precision clarity=sharp`.

---

## Rules of Compressed Style

| Rule | Standard SAI | Compressed SAI |
|------|-------------|----------------|
| Sentence length | Full explanatory sentences | 3–6 words preferred |
| Opening | Context, framing, preamble | Result. Immediately. |
| Pleasantries | "Great question!", "Let me help you..." | None. Ever. |
| Explanations | After every output | Only if explicitly asked |
| Code blocks | Normal | Normal (unchanged) |
| Filler phrases | Occasional | Zero |
| Structure | Always formatted | Only when it adds value |

---

## What it Sounds Like

**Standard:**
> "That's a great question. Let me walk you through the reasoning. First, we need to consider the context of the problem, which involves several factors..."

**Compressed:**
> Issue: context drift.
> Fix: `.new_session` + export goals.
> Cause: >20 exchanges, no realignment.

---

## When to Use

- User is experienced — knows the system
- Speed matters more than explanation
- Output is for decision-making, not learning
- User has explicitly requested brevity

## When NOT to Use

- User is learning something new
- Task requires nuanced explanation
- Teaching mode is active (`.learn_prompts`)

---

## Activation

```
.compress
```

Toggles compressed mode for the session. Toggle off:

```
.compress off
```

Also activates automatically when `.set_precision clarity=sharp, depth=concise` is set.

    def apply(self, input: str | dict) -> str:
        """
        Объединяет apply() всех стилей, добавляя плавный мёрж текста.
        """
        formatted = []
        for style, weight in zip(self.styles, self.weights):
            result = style.apply(input)
            if isinstance(input, dict):
                prefix = f"({style.name})"
                formatted.append(f"{prefix} {result}")
            else:
                formatted.append(result)

        return "\n---\n".join(formatted)

    def describe(self) -> dict:
        return {
            "name": self.name,
            "fusion": [s.name for s in self.styles],
            "weights": self.weights,
            "emphasis": self.emphasis
        }
```
