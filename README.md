# Reader-centred technical writing

A reusable Markdown skill for writing and revising technical prose with ChatGPT, Claude, or another language model. It focuses on how readers follow an argument: what arrives first, where the action sits, and which information receives emphasis.

The skill is intended for research papers, dissertations, literature reviews, reports, abstracts, and technical explanations. It includes eight worked examples and asks the model to preserve your evidence, technical meaning, and voice.

**[Read the skill](SKILL.md)** · **[Download the Markdown file](https://raw.githubusercontent.com/zty05070242/reader-centred-technical-writing/main/SKILL.md)**

## See what changes

The examples below are quoted from Enzo De Sena's *Audio Research Seminars: Technical writing* (15 October 2024). The references identify the slide numbers printed in the lecture, rather than the PDF page numbers. Punctuation has been lightly normalised; the explanations following the quotations are commentary added for this README.

### 1. Word order changes how much work the reader does

*Slide 35: Gopen's approach.*

> In the second study, people performed the task twice.

> Study participants, in the second study, twice performed the task.

The first version establishes the setting, then lets the subject and action follow naturally. The second interrupts that progression. This is the kind of change the skill looks for before reaching for more sophisticated vocabulary.

### 2. Put the action in the verb

*Slide 38: Verb.*

The lecture presents these three versions:

> What would be the student reaction accorded by the imposition of such a requirement?

> How would the students react to such a requirement?

> How would the students react if the Dean imposed the new requirement?

The later versions let *react* and *imposed* carry the actions that were buried in *reaction* and *imposition*. The third also identifies who imposes the requirement. The skill uses the author's intended meaning to choose how much of that relationship to make explicit.

### 3. The ending changes the impression

*Slide 39: Stress position.*

> Although Fred is a nice guy, he beats his dog.

> Although Fred beats his dog, he's a nice guy.

Both sentences contain the same two assertions, but they leave the reader with different impressions. The main clause and sentence ending receive emphasis. The skill checks whether that emphasis matches the point the author intends to make.

### 4. Is the point the accident, or where it happened?

*Slide 41: Stress position.*

> When I went downtown yesterday, I had a car accident.

> When I had the car accident yesterday, I was downtown.

The first sentence makes the accident the news. The second uses the accident as the starting point and makes the location the news. A revision needs to know what the reader already knows and what the sentence is meant to add.

### 5. Whose story is the sentence telling?

*Slide 42: Topic position.*

> Jack loves Jill.

> Jill is loved by Jack.

The relationship is the same, but the starting point changes from Jack to Jill. This explains why the skill does not automatically replace every passive sentence: the passive can keep the right person or thing in the topic position.

### 6. Give a paragraph a point before developing it

*Slide 45: Coffee paragraph, original and lecture revision.*

**Original**

> When brewing coffee at home, several things should be considered in order to ensure that the highest-possible quality is achieved. One such consideration is the roast and grind of the beans, and another is the container in which they are stored. Freshly roasted beans should be stored in an airtight container and then ground just before brewing.

**Revision shown in the lecture**

> The two most significant influences on the quality of home-brewed coffee are the coffee beans and how they are stored. Coffee beans should be freshly roasted and ground, and stored in an airtight container.

The revision replaces a general announcement about “several things” with a specific opening point. Slide 46 then expands the paragraph with comparisons, references, and a figure before ending with the practical conclusion:

> Therefore, coffee beans should be freshly roasted and ground, and stored in an airtight container.

The progression is **point → evidence → conclusion**. The skill applies that progression while checking that an edit preserves the intended technical details. The studies, percentages, and figure mentioned in slide 46 belong to the lecture's teaching example; they are not presented here as verified research evidence.

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
