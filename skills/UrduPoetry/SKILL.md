name: "urdu-poet"
description: "Generate original, emotionally rich Urdu poetry inspired by Gulzar or Jaun Elia. Each invocation produces a fresh poem with randomized style, mood, and structure, and outputs both Urdu script and Roman Urdu for easy sharing."

# Urdu Poet Skill

## Purpose
This skill generates **high-quality Urdu poetry** suitable for social media posting,
particularly Twitter/X, without requiring the user to specify inputs.

Each output includes:
- Clean Urdu script (primary)
- Roman Urdu (secondary, for readability)

The poetry should feel human, literary, and emotionally resonant —
not mechanical, repetitive, or templated.


## When to Use
- User asks for Urdu poetry or couplets
- User wants short poetic content for Twitter/X
- User wants emotionally expressive writing in Urdu
- User references Gulzar or Jaun Elia stylistically
- User asks for “something poetic”, “shayari”, or “nazm”
- User wants creative content without giving parameters


## When NOT to Use
- User asks for translation or explanation of poetry
- User wants only English poetry
- User wants long-form prose or essays
- User wants strict meter or classical ghazal structure
- User asks for analysis or critique of poetry


## Core Behavior
This skill operates **without user input**.

Each invocation must:
- Randomly select poetic attributes
- Generate a single complete poem
- Output Urdu **and** Roman Urdu together
- Be ready to copy-paste and post


## Randomization Rules

Each run must randomly select:

### Style (choose one)
- Gulzar
- Jaun Elia

### Theme (choose one)
- Love
- Loneliness
- Longing
- Loss
- Hope
- Silence
- Time
- Memory
- Identity
- Emotional distance

### Tone (choose one)
- Melancholic
- Romantic
- Thoughtful
- Quietly bitter
- Softly hopeful
- Reflective
- Existential

### Length (choose one)
- Short: 1–2 lines (single sher)

Randomness should feel **organic**, not evenly distributed or predictable.


## Style Guidelines

### If Style = Gulzar
- Use subtle metaphors and visual imagery
- Prefer nature, silence, pauses, time, memory
- Emotion should be restrained, not dramatic
- Language should feel soft, fluid, and observational
- Avoid harsh bitterness or direct accusation

### If Style = Jaun Elia
- Use introspection and emotional conflict
- Allow irony, melancholy, existential unease
- Emotion may feel wounded, tired, or quietly rebellious
- Language can feel personal and unsettled
- Avoid excessive romance or decorative imagery


## Language & Script Rules

### Urdu Script
- Must be clean, standard Urdu
- Unicode-safe, right-to-left text
- No experimental glyphs
- No English words

### Roman Urdu
- Simple, readable Roman Urdu
- Line-by-line correspondence with Urdu
- No English translation or explanation
- No brackets or parentheses


## Quality Constraints

The generated poetry MUST:
- Be original (no imitation of real verses)
- Avoid clichés and overused phrases
- Avoid rhyme-forcing
- Avoid moral preaching
- Avoid modern slang
- Feel emotionally sincere
- Read naturally when posted standalone


## Twitter Constraints

- Combined output (Urdu + Roman) must be ≤280 characters
- Line breaks are allowed
- Each line must feel complete
- The poem should work without context
- No trailing spaces or formatting artifacts


## Output Rules (VERY IMPORTANT)

- Output ONLY poetry
- First Urdu, then Roman Urdu
- Separate sections with a single blank line
- No markdown
- No quotes
- No labels
- No explanations
- No metadata
- No language mixing inside a line

Violation of output rules breaks the skill.


## Output Format

Urdu poetry  
(blank line)  
Roman Urdu poetry  

(1–4 lines each, matching order)


## Examples

### Example 1 — Theme: Melancholic

خاموشی نے آج پھر نام لے کر پکارا
ہم نے سن کر بھی انکار کر دیا

Khamoshi ne aaj phir naam le kar pukara
Hum ne sun kar bhi inkaar kar diya

### Example 2 — Theme: Love

دل کے درد کو الفاظ میں ڈھالوں
تیرے عشق کے زخم ہیں کتنے نازک

Dil ke dard ko alfaaz mein dhaloon
Tere ishq ke zakhm hain kitne naazuk
