# DIA Flow

**An AI-assisted workspace for turning clinical knowledge into testable digital treatment pathways.**

![DIA Flow — 32-second product walkthrough](assets/dia-flow-demo.gif)

*32-second silent walkthrough. The animation restarts automatically.*

**[Open the full-resolution MP4 →](assets/dia-flow-demo.mp4)**

> DIA Flow is an exploratory product prototype. It is not clinically validated and is not intended for treatment delivery or clinical decision-making.

## Why I built it

Designing a digital treatment programme is not simply a matter of moving clinical text onto a screen. Clinical knowledge has to be translated into a coherent patient journey with the right sequence, level of detail, interactions, exercises, decision points and tone.

That work is often fragmented across documents, workshops, whiteboards and handovers between clinicians, researchers, designers and developers. Generative AI can speed up early drafts, but it also introduces important questions: What information did the model use? Which claims are supported by evidence? How does a clinician stay in control? And how can a proposed programme be tested before it becomes expensive to build?

I created DIA Flow to explore a more transparent and product-oriented workflow for answering those questions.

## Who it is for

DIA Flow is designed for healthcare professionals and multidisciplinary digital-health teams who develop or improve digital interventions — particularly psychologists, therapists, researchers, product professionals and designers.

The prototype supports the early product-development stages: framing a programme, creating a first structure, reviewing content, testing the patient journey and iterating with domain experts.

## What DIA Flow does

DIA Flow turns a clinical brief and local source material into a structured, editable programme rather than a flat AI-generated document.

1. **Add the programme brief and context.** The user describes the target group, purpose and constraints, and can add notes, documents or images as local context.
2. **Generate a first treatment flow.** The system proposes a graph of connected modules containing content, exercises, surveys and flow logic.
3. **Review the clinical rationale.** When web evidence is enabled, source-backed clinical rationale and limitations are kept separate from user-provided context.
4. **Edit at page and block level.** The clinician can rewrite content directly or request focused AI suggestions, then replace, append or insert the result.
5. **Preview the patient experience.** The programme can be tested as a mobile, tablet or desktop journey, including required questions, survey scoring and branching.
6. **Challenge the design with synthetic personas.** A persona can move through a selected programme and respond to exercises and surveys, helping the team identify unclear wording, friction and assumptions before testing with real users.

Persona simulation is a design aid. It does not predict real patient behaviour and cannot replace research with patients or healthcare professionals.

## Product principles

- **AI proposes; the healthcare professional decides.** Generated structures and content remain editable and require human review.
- **Context is not the same as evidence.** Local notes and documents can shape tone, audience and programme design, while clinical claims require a separate evidence trail.
- **Traceability should be visible.** The interface shows which local context informed a generation and can connect clinical rationale to its sources, assumptions and limitations.
- **A programme should be experienced, not only described.** Preview and simulation make it possible to inspect the actual sequence and interactions early.
- **The prototype supports design decisions, not clinical decisions.** It is a product exploration rather than a validated clinical system.

## Features shown — and beyond the video

- Visual flow builder with connected programme modules
- Content, exercise, survey, introduction and completion nodes
- Conditional logic, scoring and parallel branches
- Multi-page modules with block-based editing
- AI-assisted programme and content generation using structured outputs
- Local retrieval/RAG from text, PDF, DOCX and image context
- Separate evidence bundles with sources, assumptions and limitations
- Patient preview across mobile, tablet and desktop layouts
- Synthetic patient personas with simulated answers, mood and engagement
- Local workspace persistence for iterative prototyping

## Formative usability work

I have used workshops and think-aloud sessions with healthcare professionals to examine whether the workflow makes sense to its intended users: from creating the first programme structure to reviewing AI-generated output and retaining professional control.

A small formative usability evaluation with eight healthcare professionals informed subsequent iterations of the prototype. This work evaluated the product concept and interaction flow; it was not a study of clinical effectiveness.

## Technical architecture

| Layer | Implementation |
| --- | --- |
| Frontend | React 19, TypeScript, Vite and Tailwind CSS |
| Backend | Express server acting as the application and AI proxy layer |
| AI generation | OpenAI Responses API with schema-constrained structured output |
| Programme model | Typed graph of nodes, pages, blocks and connections with a dedicated preview runtime |
| Context | Local file-based retrieval/RAG with optional reranking for user-provided material |
| Evidence | Separate source-verified evidence bundles linked to programmes and content |
| Storage | Local workspace and asset persistence for prototype use |

The distinction between local context and verified evidence is deliberate: internal material can inform product design without being presented as proof of a clinical claim.

## Development approach

DIA Flow is my own product prototype. I defined the problem, product concept, information architecture, user flows, AI workflows, prompt logic, technical approach and evaluation activities, and I built the working application through iterative prototyping.

I used an AI-assisted development workflow to translate product decisions into a functional prototype quickly. Responsibility for the product direction, clinical framing, architecture choices, testing and final review remained mine.

## What I learned

- The difficult part of applying generative AI in a specialist domain is not producing more text; it is creating a reviewable workflow around that output.
- Structured AI output becomes much more useful when it maps directly to a product domain model — in this case nodes, pages, blocks, connections and evidence links.
- Clinicians need to see and edit the result at the same level at which patients will experience it. A graph alone is not enough; content editing and patient preview have to stay connected.
- Synthetic personas are useful for surfacing design questions, but they become misleading if treated as evidence about real users.
- Building, demonstrating and testing an end-to-end prototype creates better conversations with domain experts than discussing an abstract AI opportunity.

## Current status

The prototype demonstrates a product direction and a set of working interaction patterns. It uses demo content, is not connected to a clinical production environment and should not be used with patient data.

The next product questions would concern deeper validation with intended users, governance for clinical content and evidence, integration with existing treatment platforms, and the boundary between useful AI assistance and the professional judgement that must remain with clinicians.

## About the creator

I am Oliver Rønn Christensen, a product-oriented digital-health professional with experience across digital treatment, AI, user research and cross-functional product development. My work focuses on bridging clinical practice, user needs, technology and product strategy.
