name: "urdu-poet"
description: "Generate original, emotionally rich Urdu poetry inspired by Gulzar or Jaun Elia. Each invocation produces a fresh poem with randomized style, mood, and structure, and outputs both Urdu script and Roman Urdu for easy sharing."
version: "2.0"

# Urdu Poet Skill

## Purpose
Generates high-quality Urdu poetry suitable for social media (Twitter/X) without user input. Output includes clean Urdu script and Roman Urdu for accessibility. Poetry feels human, literary, and emotionally resonant.


## When to Use
- User asks for Urdu poetry, couplets, shayari, or nazm
- User wants short poetic content for Twitter/X
- User wants emotionally expressive writing in Urdu
- User references Gulzar or Jaun Elia stylistically
- User wants creative content without providing parameters

## When NOT to Use
- User asks for translation or explanation of existing poetry
- User wants only English poetry
- User wants long-form prose, essays, or analysis
- User wants strict classical ghazal structure (qafiya, radif)
- User asks for literary analysis or critique

## Core Execution Flow

```
1. Select random attributes → 2. Draft poem → 3. Validate → 4. Output
```

Each invocation must:
- Select attributes using the Randomization Algorithm below
- Generate exactly one complete poem
- Output Urdu first, then Roman Urdu
- Be copy-paste ready for social media


## Randomization Algorithm

Execute in order:

### Step 1: Select Style (pick exactly one)
```
Random.choice(["Gulzar", "Jaun Elia"])
```

### Step 2: Select Theme (pick exactly one)
```
Random.choice(["Love", "Loneliness", "Longing", "Loss", "Hope", "Silence",
              "Time", "Memory", "Identity", "Emotional distance"])
```

### Step 3: Select Tone (pick exactly one)
```
Random.choice(["Melancholic", "Romantic", "Thoughtful", "Quietly bitter",
              "Softly hopeful", "Reflective", "Existential"])
```

### Step 4: Determine Length
```
Fixed: 1-2 lines (single sher)
```

### Step 5: Verify Compatibility
```
IF (Tone == "Quietly bitter" OR Tone == "Existential") AND (Theme == "Hope" OR Theme == "Love"):
    Reselect Theme OR Tone to ensure consistency
```

### Step 6: Generate
Draft poem using selected attributes and Style Guidelines below.


## Style Guidelines

### Gulzar Style
| Element | Requirement |
|---------|-------------|
| Metaphors | Subtle, visual, nature-based |
| Topics | Silence, pauses, time, memory, solitude |
| Emotion | Restrained, observational, not dramatic |
| Language | Soft, fluid, gentle flow |
| Avoid | Harsh bitterness, direct accusation |

### Jaun Elia Style
| Element | Requirement |
|---------|-------------|
| Focus | Introspection, internal conflict |
| Mood | Irony, melancholy, existential unease |
| Emotion | Wounded, tired, quietly rebellious |
| Language | Personal, unsettled, conversational |
| Avoid | Excessive romance, decorative imagery


## Language & Script Rules

### Urdu Script (Primary Output)
- Clean, standard Urdu only
- Unicode-safe (RTL text)
- No experimental glyphs or decorative marks
- No English words mixed in

### Roman Urdu (Secondary Output)
- Simple, widely readable Roman Urdu
- Line-by-line correspondence with Urdu (same number of lines)
- No English translation, brackets, or parentheses


## Quality Constraints

### Content Requirements
| Constraint | Detail |
|------------|--------|
| Originality | No imitation of real verses or famous shers |
| Language | No clichés, overused phrases, or rhyme-forcing |
| Style | No moral preaching or modern slang |
| Tone | Must feel emotionally sincere and human |
| Standalone | Must read naturally without context |

### Character Limit & Validation
- Target: Combined output ≤280 characters (Urdu + Roman Urdu)
- Soft limit: If 280-300 chars, minimize blank lines
- Hard limit: If >300 chars, regenerate shorter version
- Count: Include all characters (spaces, newlines, blank line)

### Validation Checklist
Before outputting, verify:
- [ ] Urdu and Roman Urdu have matching line counts
- [ ] Combined length ≤300 characters
- [ ] No English words in Urdu section
- [ ] No brackets, quotes, or labels
- [ ] Style matches selected (Gulzar/Jaun Elia)
- [ ] Theme and tone are consistent


## Output Format (CRITICAL)

### Strict Format Rules
```
[Line 1 - Urdu]
[Line 2 - Urdu]
...
[Single blank line]
[Line 1 - Roman Urdu]
[Line 2 - Roman Urdu]
...
```

### Forbidden Elements
- No markdown formatting
- No quotes (single or double)
- No labels like "Urdu:" or "Roman:"
- No explanations, metadata, or notes
- No language mixing within lines
- No trailing spaces

### Output Length
- Urdu: 1-2 lines
- Roman Urdu: Same line count as Urdu
- Blank line: Exactly ONE empty line separator


## Examples

### Example 1 (Gulzar | Loneliness | Melancholic)
```
خاموشی نے آج پھر نام لے کر پکارا
ہم نے سن کر بھی انکار کر دیا

Khamoshi ne aaj phir naam le kar pukara
Hum ne sun kar bhi inkaar kar diya
```
*Length: ~90 characters*

### Example 2 (Jaun Elia | Loss | Existential)
```
دل کے درد کو الفاظ میں ڈھالوں
تیرے عشق کے زخم ہیں کتنے نازک

Dil ke dard ko alfaaz mein dhaloon
Tere ishq ke zakhm hain kitne naazuk
```
*Length: ~95 characters*

### Example 3 (Gulzar | Time | Softly hopeful)
```
واپسی کا انتظار ہے ابھی
دھپ میں رہتی ہے یہ رات

Waapsi ka intezaar hai abhi
Dhoop mein rehti hai ye raat
```
*Length: ~70 characters*

### Example 4 (Jaun Elia | Memory | Thoughtful)
```
یادوں کے سائے ستا رہے ہیں
دل کو سکون کہاں ملتا

Yaadon ke saaye sata rahe hain
Dil ko sukoon kahan milta
```
*Length: ~85 characters*

---

## Error Handling & Troubleshooting

### Character Limit Exceeded
| Scenario | Action |
|----------|--------|
| >300 chars | Regenerate with fewer words, shorter lines |
| 280-300 chars | Remove extra blank lines if any |
| Consistently failing | Use 1-line poems instead of 2 |

### Style Mismatch
| Issue | Solution |
|-------|----------|
| Sounds too generic | Add specific imagery unique to style |
| Wrong tone for theme | Refer to Randomization Step 5, verify compatibility |
| Mixing styles | Ensure Gulzar's restraint OR Jaun Elia's introspection, not both |

### Output Format Issues
| Problem | Fix |
|---------|-----|
| Uneven line counts | Ensure Roman Urdu matches Urdu line-by-line |
| Extra blank lines | Keep exactly ONE blank line separator |
| Labels/quotes present | Remove all formatting before output |

### Quality Failures
| Symptom | Remedy |
|---------|--------|
| Cliché detected | Replace with fresh metaphor or imagery |
| Rhyme feels forced | Rewrite focusing on meaning first, rhyme second |
| Sounding mechanical | Use more conversational, natural word order |
