# Reader-centred technical writing

A reusable Markdown skill for writing and revising technical prose with ChatGPT, Claude, or another language model. It focuses on how readers follow an argument: what arrives first, where the action sits, and which information receives emphasis.

The skill is intended for research papers, dissertations, literature reviews, reports, abstracts, and technical explanations. It includes eight worked examples and asks the model to preserve your evidence, technical meaning, and voice.

**[Read the skill](SKILL.md)** · **[Download the Markdown file](https://raw.githubusercontent.com/zty05070242/reader-centred-technical-writing/main/SKILL.md)**

## Quick start

1. Download [SKILL.md](https://raw.githubusercontent.com/zty05070242/reader-centred-technical-writing/main/SKILL.md). If it opens as text, save it as `SKILL.md`.
2. Attach it to your ChatGPT or Claude conversation alongside your draft. You can also paste its contents into the conversation.
3. Give the model a specific writing task. For example:

```text
Apply the attached reader-centred technical-writing skill to my draft.
Improve structure, clarity, and precision while preserving my technical
meaning, evidence, citations, and voice. Return the revised text first,
then explain the most important changes. Flag missing evidence rather
than inventing it.
```

Include the audience, word limit, and any assignment or journal requirements when they matter. For a short passage, the attachment and a clear request are enough. The lecture PDF is not needed to use the skill.

## What the skill teaches

The central sentence-level approach is **whose story → action → intended emphasis**:

- Establish the topic early, so the reader knows whose story the sentence tells.
- Keep the grammatical subject and its verb close together.
- Express the action through the verb instead of burying it in abstract nouns.
- Put the intended takeaway where readers are likely to give it emphasis, often near the sentence's end.

At larger scales, the skill develops paragraphs around a clear point, connects evidence to conclusions, and organises sources into an argument. It also covers informative abstracts, quantitative precision, attribution, equations, and a final reading from an unfamiliar reader's perspective.

These are tools for making decisions, rather than a fixed template for every sentence. For example, passive voice can help when it keeps the same topic in view; shortening a passage should not remove an important condition.

### A small example

**Before**

> An evaluation of the effect of window length on the estimate was carried out.

**After**

> We evaluated how window length affected the estimate.

The revision puts the action in the verb and makes the sentence easier to follow. If the document requires an impersonal style, “The study evaluated…” may fit better. Neither version supplies a finding about the size or direction of the effect.

## Use it for recurring writing

### ChatGPT projects

Add `SKILL.md` to the project's files and add this instruction to the project:

```text
For technical and academic writing tasks, read and apply the uploaded
SKILL.md. Follow the requirements of the current task and preserve my
meaning, evidence, and voice.
```

Start your writing conversation inside that project. ChatGPT projects share uploaded files and project instructions across their chats. See the [official project documentation](https://learn.chatgpt.com/docs/projects).

### Claude projects

Add `SKILL.md` to the project's files or knowledge and use the same project instruction above. Then provide the draft and the outcome you want in a conversation within the project. See [Claude's project documentation](https://support.claude.com/en/articles/9517075-what-are-projects).

These project workflows use the file as writing guidance. A file in this GitHub repository does not automatically become available to an unrelated conversation.

### Claude Code: install as a personal skill

If you use Claude Code locally, place the repository in its personal skills directory:

```sh
mkdir -p ~/.claude/skills
git clone https://github.com/zty05070242/reader-centred-technical-writing.git \
  ~/.claude/skills/reader-centred-technical-writing
```

Then invoke it in Claude Code:

```text
/reader-centred-technical-writing Revise the introduction in draft.md for clarity and flow. Preserve its claims and citations.
```

If you prefer to install manually, create `~/.claude/skills/reader-centred-technical-writing/` and put `SKILL.md` inside it. These instructions apply to local Claude Code; other Claude surfaces have their own skill settings. See the [official skills documentation](https://code.claude.com/docs/en/skills).

## More ways to use it

| Task | Example request |
| --- | --- |
| Review before rewriting | “Apply the skill to this section. Identify the three changes that would most improve the reader's understanding, and show a revision for each.” |
| Write an abstract | “Using the skill and the supplied methods and results, write a 200-word abstract that reports the main findings.” |
| Shorten a passage | “Reduce this discussion to 600 words. Preserve the quantitative results, necessary qualifications, and attribution.” |
| Learn from edits | “Revise this paragraph and explain how topic position, verbs, and sentence endings affect its meaning.” |

## Source and credit

This project grew from a close reading of Enzo De Sena's *Audio Research Seminars: Technical writing*, dated 15 October 2024, at the University of Surrey. The lecture presents Gopen's approach to reader expectations alongside examples of paragraph development, abstracts, referencing, and technical style.

The skill paraphrases those teaching principles and turns them into instructions a language model can apply. It adds practical checks for preserving technical meaning and avoiding invented evidence. The [source and adaptation section](SKILL.md#source-and-adaptation) identifies the relevant slides and distinguishes those additions from the lecture's content.

The original lecture PDF and the separate handouts it mentions are not distributed here. The skill does not claim to review those separate handouts or to replace a discipline's methodological guidance. Numerical examples illustrate writing choices; they are not evidence for a manuscript.

## Repository contents

```text
reader-centred-technical-writing/
├── SKILL.md     The self-contained writing skill and worked examples
├── README.md    Usage, installation, and source credit
└── LICENSE      MIT license for this repository's original material
```

No scripts, packages, or API keys are required to use the writing instructions.

## License

The original material in this repository is available under the [MIT License](LICENSE). Credit for the lecture and the ideas it presents remains with their respective authors; the repository's license does not license the original lecture, cited papers, or other third-party works.
