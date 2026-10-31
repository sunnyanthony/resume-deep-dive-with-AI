# Resume Deep-Dive

**An AI-powered, role-adaptive resume interviewer.** Uncover overlooked achievements, assess career seniority, and build an accurate, targeted resume through a thoughtful conversation — **one question at a time**.

> **Discover before you rewrite.** The goal is not to make existing bullet points sound bigger. It is to understand what the candidate actually accomplished, identify work their resume misses, and express it accurately for their target role and seniority.

## Why use it?

- **Works across careers.** The AI takes on an appropriate domain-interviewer perspective, rather than assuming every candidate is a Software Engineer or using a fixed technical checklist.
- **Level-aware.** It first makes a provisional, **general seniority assessment**, then considers the target job and any company-specific leveling evidence. A title or years of experience alone do not determine seniority.
- **One question at a time.** It listens, asks one focused follow-up, and adapts to the reply instead of presenting a long questionnaire.
- **Finds hidden contributions.** It explores responsibilities, judgment, collaboration, and results that the candidate may have omitted or underestimated.
- **Checks the evidence.** It distinguishes personal vs. team contributions, measured vs. theoretical numbers, and released vs. incomplete work; it respects confidentiality.
- **Writes concisely.** It uses STAR/CAR to understand the story, not to force every bullet into the same formula.
- **Multilingual interview; English resume by default.** Choose any interview language. The resume is drafted in English unless you request another language.

## Quick start — Prompt (ChatGPT, Claude, Gemini, etc.)

1. Open **[PROMPT.md](PROMPT.md)** and copy the entire prompt into a new AI conversation, or use it as project instructions where supported.
2. The interviewer asks which **language** you prefer for the conversation.
3. Share your existing resume, portfolio, or a description of your experience.
4. Receive a **provisional general seniority assessment** based on existing evidence; then specify the role you want next.
5. Answer **one question per turn** while the interviewer investigates your most relevant work, including achievements missing from the resume.
6. Review the resulting concise, target-specific bullets and request the full revised resume when ready.

No technical setup is required for this option.

## Quick start — Agent Skill

The standalone **[SKILL.md](skills/resume-deep-dive/SKILL.md)** is intended for AI environments that support Agent Skills.

1. Copy the entire `skills/resume-deep-dive/` directory into your agent's supported skills location, using that product's installation instructions.
2. Ask the agent to use **resume-deep-dive** to review your resume and interview you.
3. It will follow the same role-adaptive, evidence-first process, without requiring you to paste the full master prompt each time.

**Compatibility note:** Not every ChatGPT or other AI interface can directly install Agent Skills. When in doubt, use `PROMPT.md`. Installing a Skill does not make an AI more knowledgeable about a particular profession; it makes the workflow easier to reuse.

## Example conversation

**AI:** What language would you like to use for our interview? I'll draft your resume in English by default, unless you prefer another language.

**Candidate:** 繁體中文。

**AI:** 請分享你目前的履歷或 portfolio，我會先評估目前履歷呈現的 General Seniority，再了解你想應徵的職位。

*After reviewing the resume, the AI gives a short, provisional assessment and asks about the candidate's target role. It then interviews one achievement at a time.*

## Project structure

```text
resume-deep-dive/
├── README.md
├── PROMPT.md
├── LICENSE
└── skills/
    └── resume-deep-dive/
        └── SKILL.md
```

| File | Purpose |
| --- | --- |
| [`PROMPT.md`](PROMPT.md) | Full English master prompt for copy/paste use |
| [`skills/resume-deep-dive/SKILL.md`](skills/resume-deep-dive/SKILL.md) | Standalone Agent Skill for environments that support Skills |
| [`LICENSE`](LICENSE) | MIT License |

## Design principles

**One question at a time · Adapt to the person's field · Calibrate level with evidence · Find omitted achievements · Attribute work accurately · Protect confidential information · Keep bullets concise**

This project intentionally **does not enumerate specialty-specific technical questions**. The AI should derive its follow-ups from the candidate's actual experience, target profession, and level, rather than asking everyone the same predefined questions.

## Limitations

The AI's career-level assessment is an informed, provisional evaluation — not a promise of a specific company's title, an offer, or an interview. Company leveling should be grounded in a relevant job description or trustworthy framework when possible. Never share NDA-protected material or nonpublic employer information to improve a bullet point.

## License

Licensed under the [MIT License](LICENSE).
