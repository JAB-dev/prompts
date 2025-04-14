# AI-Driven Dev {Prompts}

> A collection of prompts for developers with built-in software to call any prompt, from any application.

- [🚀 **The "AI-Driven Dev" prompt library**](#-the-ai-driven-dev-prompt-library)
  - [1) Installation](#1-installation)
  - [2) How to use a prompt?](#2-how-to-use-a-prompt-)
  - [3) Updating prompts](#3-updating-prompts)
    - [Automatic update via .bashrc / .zshrc](#automatic-update-via-bashrc--zshrc)
    - [Automatic update via cron (Linux)](#automatic-update-via-cron-linux)
    - [Automatic update via Launchd (OSX)](#automatic-update-via-launchd-osx)
  - [4) Known issues](#4-known-issues)
- [**🔥 Contribution**](#-contribution)
  - [Additional resources](#additional-resources)
- [**👌 Good prompt practices**](#-good-prompt-practices)
  - [Template of "perfect" prompt `:promptTemplate`](#template-of-perfect-prompt-prompttemplate)
    - [Template](#template)
    - [Example of applying the template in a prompt with Cursor](#example-of-applying-the-template-in-a-prompt-with-cursor)
  - [Create a prompt (CRAFT method) `:promptCreate`](#create-a-prompt-craft-method-promptcreate)
  - [List good practices `:promptBestPractices`](#list-good-practices-promptbestpractices)
  - [Extract a list of rules `:promptExtractRules`](#extract-a-list-of-rules-promptextractrules)
  - [Extract a list of actions from a conversation `:promptExtractActions`](#extract-a-list-of-actions-from-a-conversation-promptextractactions)
  - [Extract a rule from a conversation `:promptExtractSingleRule`](#extract-a-rule-from-a-conversation-promptextractsinglerule)
  - [Optimize a prompt `:promptOpt`](#optimize-a-prompt-promptopt)
  - [Correct AI weaknesses `:promptStart`](#correct-ai-weaknesses-promptstart)
- [**🙋‍♂️ Generate a feature**](#️-generate-a-feature)
  - [List of user stories for an epic `:featureUserStories`](#list-of-user-stories-for-an-epic-featureuserstories)
  - [User story `:featureUserStory`](#user-story-featureuserstory)
  - [Instruction sheet (aka: technical plan) `:featureInstructions`](#instruction-sheet-aka-technical-plan-featureinstructions)
  - [Create the dev path for a feature `:featurePath`](#create-the-dev-path-for-a-feature-featurepath)
  - [Create a feature `:featureCreate`](#create-a-feature-featurecreate)
- [**📦 Starting a project**](#-starting-a-project)
  - [Imagine a project (from scratch) `:projectBootstrap`](#imagine-a-project-from-scratch-projectbootstrap)
  - [Ensure good practices `:projectEnforce`](#ensure-good-practices-projectenforce)
  - [Structure of URLs `:projectURL`](#structure-of-urls-projecturl)
- [**💽 Database**](#-database)
  - [Structure and schemas `:dbStructure`](#structure-and-schemas-dbstructure)
  - [Generate SQL schema from specifications `:dbGenSQL`](#generate-sql-schema-from-specifications-dbgensql)
  - [Generate entities from an SQL schema `:dbGenEntity`](#generate-entities-from-an-sql-schema-dbgenentity)
- [**🚀 Code generation**](#-code-generation)
  - [Preview code `:codePreview`](#preview-code-codepreview)
  - [Ask the AI Editor to code the plan `:codeFromPlan`](#ask-the-ai-editor-to-code-the-plan-codefromplan)
  - [Write code from a Deep Research `:codeDeepResearch`](#write-code-from-a-deep-research-codedeepresearch)
  - [Generate fake data `:codeFake`](#generate-fake-data-codefake)
- [**🏞️ Generate code from an image**](#️-generate-code-from-an-image)
  - [Extract image details `:imageRepro1ExtractDetails`](#extract-image-details-imagerepro1extractdetails)
  - [Refine the design `:imageRepro2Refine`](#refine-the-design-imagerepro2refine)
  - [Implement the design `:imageRepro3Implementation`](#implement-the-design-imagerepro3implementation)
  - [Auto-correct the design `:imageMCPAutoCorrection`](#auto-correct-the-design-imagemcpautocorrection)
  - [Advanced design (with animations/states) `:imageAdvancedImplementation`](#advanced-design-with-animationsstates-imageadvancedimplementation)
- [**🐛 Fix bugs**](#-fix-bugs)
  - [Fix a technical bug (with error message) `:bugFinder`](#fix-a-technical-bug-with-error-message-bugfinder)
  - [Fix a functional bug (we don't know what causes it) `:bugReveal`](#fix-a-functional-bug-we-dont-know-what-causes-it-bugreveal)
  - [Prevent the AI Editor from going around in circles on a bug `:bugRethink`](#prevent-the-ai-editor-from-going-around-in-circles-on-a-bug-bugrethink)
  - [Debug code by adding "logging" `:debugLog`](#debug-code-by-adding-logging-debuglog)
  - [Detect inconsistencies `:debugInconsistency`](#detect-inconsistencies-debuginconsistency)
- [**🧪 Tests**](#-tests)
  - [Test first `:testFirst`](#test-first-testfirst)
  - [Gherkin `:testGenGherkin`](#gherkin-testgengherkin)
  - [List untested functions `:testUntested`](#list-untested-functions-testuntested)
  - [Generate a unit test for a file `:testUnit`](#generate-a-unit-test-for-a-file-testunit)
- [**📚 Documentation**](#-documentation)
  - [Generate a README `:docReadMe`](#generate-a-readme-docreadme)
  - [Wireframe instructions from a spec `:docWireframeInstructions`](#wireframe-instructions-from-a-spec-docwireframeinstructions)
  - [Merge multiple Markdown files `:mdMerge`](#merge-multiple-markdown-files-mdmerge)
  - [Generate Mermaid diagrams `:docMermaid`](#generate-mermaid-diagrams-docmermaid)
- [**🙏 Maintenance**](#-maintenance)
  - [Version upgrade `:maintenanceUpdateDeps`](#version-upgrade-maintenanceupdatedeps)
    - [Upgrade framework `:maintenanceUpdateFramework`](#upgrade-framework-maintenanceupdateframework)
- [**🔄 Refactoring**](#-refactoring)
  - [Refactoring suggestion: `:refactSuggest`](#refactoring-suggestion-refactsuggest)
  - [Add comments to code `:refactComment`](#add-comments-to-code-refactcomment)
  - [Create a new generic file `:refactGeneric`](#create-a-new-generic-file-refactgeneric)
  - [SRP - Single Responsibility Principle `:refactSRP`](#srp---single-responsibility-principle-refactsrp)
  - [Beautify code `:refactOpt`](#beautify-code-refactopt)
  - [Optimize code performance `:refactPerf`](#optimize-code-performance-refactperf)
  - [Refactor a file `:refactFile`](#refactor-a-file-refactfile)
- [**🧙 Code review**](#-code-review)
  - [Do a code review `:adviceReview`](#do-a-code-review-advicereview)
  - [Review a project's architecture `:adviceArchitecture`](#review-a-projects-architecture-advicearchitecture)
  - [Design Patterns `:adviceDesignPatterns`](#design-patterns-advicedesignpatterns)
- [**🧑‍🍳 Project management**](#-project-management)
  - [Define milestones and epics `:pmMilestones`](#define-milestones-and-epics-pmmilestones)
  - [Write a specification document `:pmSpecs`](#write-a-specification-document-pmspecs)
  - [Choose a technical stack `:pmTechStack`](#choose-a-technical-stack-pmtechstack)
- [**🗣️ Chat and conversations**](#️-chat-and-conversations)
  - [Top 3 `:chatTop3`](#top-3-chattop3)
  - [Summarize in one sentence `:chatSummarize`](#summarize-in-one-sentence-chatsummarize)
  - [Search the internet `:chatOnline`](#search-the-internet-chatonline)
  - [Answer in French `:chatFr`](#answer-in-french-chatfr)
  - [Markdown output `:chatOutputMd`](#markdown-output-chatoutputmd)
  - [Load the knowledge base `:chatKB`](#load-the-knowledge-base-chatkb)
  - [Evaluate an answer `:chatEvaluate`](#evaluate-an-answer-chatevaluate)
  - [Start a new conversation / chat `:chatRestart`](#start-a-new-conversation--chat-chatrestart)
- [**📝 Writing and content**](#-writing-and-content)
  - [Simplify text `:contentRephrase`](#simplify-text-contentrephrase)
  - [Make text more concise `:contentFocus`](#make-text-more-concise-contentfocus)
  - [Focus on benefits `:contentFocusBenefits`](#focus-on-benefits-contentfocusbenefits)

- [Summarize Text `:contentSummarize`](#summarize-text-contentsummarize)
- [**💻 Commands**](#-commands)
  - [Delete Empty Folders `:cmdEmptyFolders`](#delete-empty-folders-cmdemptyfolders)
  - [OSX](#osx)
    - [Update Homebrew `:osxBrew`](#update-homebrew-osxbrew)
- [**🏄‍♂️ Reasoning Prompts**](#️-reasoning-prompts)
  - [Feature Planning `reasonFeaturePlan`](#feature-planning-reasonfeatureplan)
  - [Code Audit `:reasonCodeAudit`](#code-audit-reasoncodeaudit)
- [**🕵 Agents**](#-agents)
  - [Refactoring Agent](#refactoring-agent)
- [**🎬 Presentation**](#-presentation)
  - [Create Program / Plan `:presentationCreate`](#create-program--plan-presentationcreate)
  - [Expand a Sub-Part of the Program `:presentationExpand` #WIP](#expand-a-sub-part-of-the-program--presentationexpand-wip)
  - [Convert a Sub-Part to Slides `:presentationConvert` #WIP](#convert-a-sub-part-to-slides-presentationconvert-wip)

## 🚀 **The "AI-Driven Dev" Prompt Library**

To code faster with AI, you need:

1. Quality prompts (we've written them for you)
2. Understanding where to use them (we have a [Discord](https://bit.ly/alexsoyes-discord))
3. Having access to these prompts everywhere, from ChatGPT to Chrome to VSCode.

### 1) Installation

---

1. Install the text expander [Espanso](https://espanso.org/install/) (opensource and compatible with Mac, Windows, Linux)

2. Retrieve our package:

```console
espanso install ai-driven-dev-prompts --git git@github.com:ai-driven-dev/prompts.git --external
```

3. That's it!

### 2) How to use a prompt?

---

When you need a prompt:

1. **Use the keyboard shortcut**: Mac `⌥ + Space` - (Windows / Linux: `ALT + Space`)
2. **Search for the prompt name**, e.g., `feature`.
3. **Insert the prompt** into your application (remember to focus on the input area).

![espanso usage](docs/espanso.gif)

### 3) Updating the prompts

---

The prompts are updated regularly by the AI-Driven Dev community.

```console
espanso package update ai-driven-dev-prompts
```

<details>
<summary>Automatic Update via .bashrc / .zshrc</summary>

#### Automatic Update via .bashrc / .zshrc

Add this line to your shell configuration file (`~/.bashrc` or `~/.zshrc`):

```console
espanso package update ai-driven-dev-prompts
```

</details>

<details>
<summary>Automatic Update via cron (Linux)</summary>

#### Automatic Update via cron (Linux)

Add this line to your cron configuration file (`crontab -e`):

```console
0 0 * * * espanso package update ai-driven-dev-prompts
```

</details>

<details>
<summary>Automatic Update via Launchd (OSX)</summary>

#### Automatic Update via Launchd (OSX)

Add this line to your Launchd configuration file (`~/Library/LaunchAgents/com.espanso.update-prompts.plist`):

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
    <dict>
        <key>Label</key>
        <string>com.espanso.update</string>
        <key>ProgramArguments</key>

```xml
<array>
    <string>/bin/sh</string>
    <string>-c</string>
    <string>/usr/local/bin/espanso package update ai-driven-dev-prompts</string>
</array>
<key>RunAtLoad</key>
<true/>
<key>StartInterval</key>
<integer>86400</integer>
<key>StandardOutPath</key>
<string>/tmp/espanso_update.log</string>
<key>StandardErrorPath</key>
<string>/tmp/espanso_update_error.log</string>
</dict>
</plist>
```

Launch the service:

```console
launchctl load ~/Library/LaunchAgents/com.espanso.update-prompts.plist
```

</details>

### 4) Known Issues

Sometimes, Espanso will paste a `v` instead of the prompt; this happens when the software is launched. Simply relaunch the prompt.

<details>
<summary>Configure Espanso not to paste the "v"</summary>

This configuration might help you avoid copying issues.

(To test, may not work for everyone)

```console
espanso edit
```

```yml
preserve_clipboard: false
pre_paste_delay: 1000
backend: clipboard
```

</details>

## **🔥 Contribution**

- Did you see an error?
- Do you want to add a prompt?

> See [CONTRIBUTION.md](CONTRIBUTION.md) for more details. 😍

### Additional Resources

- [Bolt](https://github.com/stackblitz/bolt.new/blob/main/app/lib/.server/llm/prompts.ts) - Prompts for StackBlitz
- [Supabase](https://github.com/supabase/supabase/tree/master/examples/prompts) - Prompts for Supabase

## **👌 Prompt Best Practices**

1. **Use these prompts as templates** to create your prompts.
2. **Prompt in English** for better performance.
3. **If you're starting out**, begin structuring your prompts with a template 👇.
4. **Use `xml` for variables**.
5. **Format the text in `markdown`** for readability and clarity.

### "Perfect" Prompt Template `:promptTemplate`

To make a good prompt, you primarily need a good structure.

1. **Required Fields**:
   - `Goal`: What you want to achieve with this prompt
   - `Rules`: Guidelines and constraints to respect
   - `Context`: Contextual information or environment details
2. *Optional* but recommended:
   - `Steps`: Details of the procedure to follow
   - `Input Example`: Example input to illustrate usage (if necessary)
   - `Output Example`: Expected output format (if necessary)

> Note: `Context` and `Example` can be a link to a file, or a code snippet!

<details>
<summary>See the template</summary>

#### Template

```markdown
# Goal
"[[What you want to achieve with this prompt]]"

# Rules
- "[[Rule 1]]"
- "[[Rule 2]]"
- "[[Rule 3]]"

# Steps
1. "[[Step 1]]"
2. "[[Step 2]]"
```
3. "[[Step 3]]"

# Context
[[Describe the context of the prompt]]

# Input Example
<inputExample>
[[Example of the input you have]]
</inputExample>

# Output Example
<outputExample>
[[Example of the output you want to get]]
</outputExample>
```
````

</details>

### Traduction d'un document technique `:promptTranslateTechnicalDocument`

> Traduit un document technique dans une autre langue.

<details>

<summary>Voir le prompt</summary>

````markdown
Goal: Translate given technical document into another language.

Technical document: ```[[technical document]]```

Language: "[[language]]"

Rules:
- Be accurate and concise.
- Focus on technical language.
- Keep the same structure of the document.
````

</details>

### Générer des exemples de code `:promptGenerateCodeExamples`

> Génère des exemples de code, dans le langage de votre choix.

<details>

<summary>Voir le prompt</summary>

````markdown
Goal: Generate code examples in specified language.

Language: "[[language]]"
Context: "[[context]]"

Rules:
- Be accurate and concise.
- Use comments to explain the code.
- Focus on one element by example.
````

</details>

```
file: {file-name-with.mdc}
description: {when to apply the rule}
globs: {which paths}
---

> {When }

## {Main rule}
- {rule 1}
- {rule 2}
- {rule 3}
...

## {Rule} : Example
```
...
```

````

`````

</details>

### Extract a list of actions from a conversation `:promptExtractActions`

> Quick summary of what you need to do.

<details>
<summary>See the prompt</summary>

```markdown
Summarize actions I need to do regarding that just specific part.

- Use short numbered and ordered bullet points.
- Straight to the point.
- Only the essential actions.
- No style.
- Export in markdown formatted text block surrounded by 4 backticks.
- Use English.
```

</details>

### Extract a rule from a conversation `:promptExtractSingleRule`

> In a conversation, extract "the" sentence, rule, that summarizes what needs to be done.
> Very useful when you are fixing a bug with AI and need to extract a rule.

<details>
<summary>See the prompt</summary>

```markdown
Generate a **clear and actionable** rule to prevent repeating a specific mistake.  

Based on our last discussion, give me a **universal rule** that ensures I won’t make this mistake again.  
- **Imperative and unambiguous**.  
- **Short** (maximum **15 words**).  
- **Immediately applicable** (e.g., "Always check X before executing Y.").  
```

</details>

### Optimize a prompt `:promptOpt`

> If you want to improve a prompt's performance in a command, use this prompt.

<details>
<summary>See the prompt</summary>

```markdown
Act as en **elite Prompt Engineer** that transform prompt into high performing prompts. 

# Steps
1. **Read** the prompt carefully and identify major weaknesses.  
   - Identify the **context**, the **desired role**, the **goal**, and potential **gaps**.
   - Find inconsistencies, ambiguities, duplications or missing details.
2. **Explain** those weaknesses clearly.  
  - Use **bullet points** for each issue.
3. **Suggest** concise, high-impact improvements.  
  - Use **bullet points** for each improvement.
4. **Rewrite** a final version that is clear, focused, and achieves the goal.

**Important**:
- Do not be lazy, ALWAYS return the full prompt.

# Rules  
- Translate the prompt in english.
- Make very short sentences, straight to the point, clear and concise.
- Only titles for formatting.
- No emojis.
- Minimal example 
- Maintain or clarify original intent.
- Add constraints (length, tone, format) if needed.

# Output Format to the user
1. **Weaknesses**  
2. **Suggested Improvements**  
3. **Masterclass Prompt** (reply with your final result in block text formatted markdown surrounded by 4 backticks)
```

# Prompt to improve
<prompt>
[[Your prompt]]
</prompt>

### Correct AI Weaknesses `:promptStart`

> The AI has already undergone a "pre-prompt" that will influence your conversation. Here's how to bypass the imposed limitations.
>
> Use when the AI doesn't answer correctly or doesn't provide the entire code!

<details>
<summary>View prompt</summary>

```markdown
- Please follow every steps mentioned.
- Do not be lazy.
- Always provide the full document.
- Do not generate code.
- Answer in the shortest way possible, avoid long sentences, go straight to the point.
- Confirmation questions: Only ONE question per confirmation.
```

</details>

## **🙋‍♂️ Generate a feature**

Collection of prompts to generate features.

### List of user stories for an epic `:featureUserStories`

> Allows you to write a list of user stories, to go into a given epic. If you want a very detailed US, use `:featureUserStory`.

<details>
  <summary>View prompt</summary>
  
````markdown
Create a list of user stories from user needs, starting from an epic. The AI architect should first ask questions about this epic to gather essential information. From these questions, develop a plan of user stories. Once the user story plan is validated, the task is complete.

Steps:
1. **Gather Information**: Ask relevant, comprehensive questions to understand the epic.
2. **Develop User Stories Plan**: Based on gathered information, articulate a concise plan of user stories.
3. **Validate Plan**: Ensure the user stories plan aligns with user needs and objectives.

Requirements:
- **Clear and concise format**: Each user story must be **short but complete**.  
- **Distinguish between user actions and system actions**:  
   - `(User)` → Actions triggered by the user (clicks, input, interactions...).  
   - `(System)` → Actions triggered automatically (data loading, API requests...).  
- **Use inputs and outputs**:  
   - **Trigger**: When the action occurs.  
   - **Input**: Data required for the action.  
   - **Output**: Data returned by the action.  
- **Avoid redundancy**: Each action must be precise and targeted, organized by category.

Example:
```markdown
# User Stories for Newsletter Dashboard

## User Data

### The dashboard retrieves the user profile** (System)
  - **Trigger**: On dashboard load  
  - **Input**: `userId: string`  
  - **Output**: `{ id, firstName, lastName, avatarUrl }`  

## The dashboard retrieves the user's email alias (System)
  - **Trigger**: On dashboard load  
  - **Input**: `projectId: string`  
  - **Output**: `newsletterAlias: string`  

## AI Personalization

### The user configures a message for the AI (User)
  - **Trigger**: When modifying the input field  
  - **Input**: `customMessage: string`  
  - **Output**: Stored in `UserProfile.prompt_instruction`  

### The dashboard verifies that the sent message matches the stored one (System)
  - **Trigger**: When receiving the API response  
  - **Input**: `customMessage: string`  
  - **Output**:  
    - ✅ **If identical** → Normal display  
    - ❌ **If different** → Show error and update the value  
```

# Notes

- Ensure questions are thorough to gather complete context for the epic.
- User stories should be clear, actionable, and tailored to specific user needs.

````

</details>

### User-story `:featureUserStory`

If you want to generate user stories for your project.

**Parameters**:

- "Requirements or Epics": The description of the feature to be generated

### Instruction Sheet (aka: technical plan) `:featureInstructions`

> Create a detailed instruction sheet for a specific feature, **relatively simple**.

### Step 4: Fill the "Instruction Template"

- Fill "Instruction Template".
- Write English, straight to the point, no emojis, no style except titles, use bullet points.
- Replace placeholders (`{variables}`) with actual user inputs.
- Define flow of the feature, from start to end of what AI Editor should do.

Instructions Template in English:
```markdown
# Instruction: {title}

> Please follow this plan using proper rules.

## Goal
{goal}

## Existing files

{get affected files from knowledge base, no comments}

### New file to create

{not found in knowledge base, no comments}

## Grouped tasks

### {Group 1}  

> {goal}

- {task1, with logical bridge to task2}
- {task2}  
...

### {Group 2}

> {goal}

- {task1}
...

## Validation checkpoints

- {verification1}  
```

### Step 5: Final Review
- Translate in English.
- Export in a Canvas.
- Print official documentations URLs related to the feature.
- Do a full review (list inconsistencies, ambiguities, missing details).
- Evaluate confidence to implement, 0 = no confidence, 100 = 100% sure everything is correct.
- Simulate the feature as you were hypothetically building it following the plan, identify what can go wrong.
- Check for best practices.
- Propose enhancements.
- Independently check for:  
   - **Completeness** → Are all key details covered?  
   - **Correctness** → Are dependencies, versions, and steps accurate?  
   - **Clarity** → Is the instruction unambiguous?  
- **Propose improvements in bullet points.**  
- **User Confirmation:**  
   - Ask: **"Would you like to integrate these suggestions? (YES/NO)"**  
   - If **NO** → Keep as is.  
   - If **YES** → Apply the changes.  

````

</details>

### Create the development path of a feature `:featurePath`

> Useful to ask the AI "how to do" a feature before asking it to do it; to increase accuracy and quality.

<details>
  <summary>See the prompt</summary>
  
````markdown
Goal: Create a detailed path to implement a feature before generating code.

Feature: "[[Feature to build]]"

Rules:
- Load project's knowledge base with existing stack.
- Based on requirements, look for online documentation to verify the feasibility.
- List top 3 ways to do it.
- Evaluate confidence level for each of the proposed ways.
- Ask the user to choose the best way.
````

</details>

### Create a feature `:featureCreate`

> Generates all the steps of a **large feature to brainstorm** to have a global, complete and extremely detailed overview of a feature.

<details>
  <summary>See the prompt</summary>
  
````markdown
````

</details>

Goal:
Build a new, existing or not, feature in our project.

Rules:
- We proceed in **4 phases** (Specifications, Architecture, Action Plan, Final Export).
- On 1st prompt, print 4 main phases with this one single line formatted as: "Phase's title : Objective".
- Start directly with Phase 1.  

---

## Process Overview

### Phase 1: 🧠 Gather Specifications
- **Objective**: Obtain project requirements and clarify purpose, features, constraints, and environment needs.
- **Actions**:
  - All questions must be a concise, single line.
  - Ask targeted questions to confirm:
    - Functional requirements.
    - Chosen technologies, tools, or libraries (including **versions**).
    - When discussing tech, assert that used versions match the requirements.
    - Constraints (modularity, scalability, guidelines).
    - Environment setups (API tokens, configuration files).
    - Testing, Documentation, and CI/CD requirements.
- **Output**:
  - A validated list of specifications.

**Important**: Do not move to Phase 2 until the explicitly user confirms Phase 1.

---

### Phase 2: 🧱 Define or Refine Architecture
- **Objective**: Collaboratively create or adjust the project's architecture.
- **Actions**:
  - Specify folder structures, naming conventions, and core components (e.g., commands, utilities, events).
  - Define environment variables (with placeholder values).
  - Ensure modularity, scalability, and maintainability.
  - Check in the knowledge base if an architecture already exists. Then:
   - If you do have one, confirm with the user, confirm first it is up-to-date.
   - If you don't know it, ask the user to provide it.  
   - If it doesn't exist, the user will let you know.  
  - An updated (or newly created) architecture plan, ready for Markdown export (no emoji, no style in markdown, except titles).
  - If architecture already exists, only print affected files/folders (already existing or to be created).

**Important**: Do not move to Phase 3 until the user confirms Phase 2.

---

### Phase 3: 🗂️ Develop a Detailed Plan of Actions
- **Objective**: Outline each step to implement and configure the architecture.
- **Rules**:
  - Not git actions, only technical steps.
  - No code generation, only setup instructions.
  - No assumptions, no "not needed" steps.
  - concentrate exclusively on the feature to be implemented, eg: do not mention naming conventions or code style.
  - Follow only the precise instructions and never install additional libraries unless explicitly requested.
  - Do not give code or commands to execute (e.g., `mkdir ...`); instead, say “create the new files/folders xxx.”
- **Actions**:
  - **Configuration Tasks**: External dependency setup, token generation, key management, environment variables.
  - **Technical Setup**: Initializing the project, installing dependencies, creating files/folders.
  - Ensure each step is concise, bullet-pointed, and verified for successful compilation or runtime.
- **Output**:
  - A validated, step-by-step action plan.
  - Be sure everything discussed on "Phase 1" is covered entirely.

**Important**: Do not move to Phase 4 until the user confirms Phase 3.

Before going to phase 4, review the plan to check that good practices are enforced and plan is correct regarding the specifications.

---

### Phase 4: 🧑‍💻 Export in Markdown
- **Objective**: Produce a final Markdown document suitable for the “developer” and the “AI Editor.”
- **Rules**: 
  - Phase 4 must be answered in markdown format on a text block with 4 backticks.
  - Avoid repetition and focus only on the essentials.
  - No code generation or example but provide instructions on what to do.
  - Provide this phase in english.
- **Actions**:
  - **Sections**:
    1. **Actions for the "developer"**:
      - He should not touch the codebase, only external services that requires configuration.
      - Only **Configuration Tasks** (from Phase 3)
    2. **Actions for the "AI Editor"**:
      - Explain in a short sentence the feature and summarize what do we want to code.
      - Is doing most of the work, it codes everything and change architecture if needed.
      - **Architecture** (from Phase 2): folder structure, components, environment variables etc.
      - **Technical Setup Instructions** (from Phase 3).
      - Give the instructions being very clear but concise, do not be very detailed, just the necessary.
      - **Output in english language.**
      - Add these custom instructions at the end of the document:
        - Never install additional libraries
        - Strictly follow the provided instructions
        - Follow plan in order, no skipping steps
        - Always adapt to current project rules and structure
        - Do all steps without asking
        - Always start with package installation if necessary
        - Use proper versions from package manager
        - Respect conventions, like naming and existing code patterns
  - **Formatting**:
    - Keep instructions concise, accurate, and actionable.

1. Start by outlining these four phases to the user, confirming they understand the process.
2. Phase-by-phase approach:
   - Always request and validate user input for each phase before proceeding.
   - Never skip or combine phases.
3. Never generate code—you are the Architect, not the code generator.
4. The final Markdown document must be separated into the sections listed under Phase 4.

---

## **Instructions**

1. **Begin by presenting the four phases to the user, ensuring their understanding.**
2. **Execute phase-by-phase**:
   - Always request and validate user input for each phase before continuing.
   - **Never skip or combine any phases**.
3. **Do not produce code**—you are the architect, not the code generator.
4. Create the final **Markdown document** with the sections from Phase 4.

---

## **Expected Final Output**

Upon completion of all phases, you will produce a **Markdown document** containing:

1. **Guide for the Developer**:
   - Validated specifications and project goals.
   - Configuration tasks (external dependencies, tokens, etc.).
2. **Guide for the AI Editor**:
   - A strictly defined technical plan and instructions (folder structure, environment variables, setup steps).

---

## **📦 Project Startup**

### Imagining a project (from scratch) `:projectBootstrap`

> Define the steps to start a project (needs, hosting, back-end, front-end, database, etc.)

## Goal
Your objective is to **guide the developer through a structured decision-making process**, validating each step, resolving contradictions, and providing a **final architecture summary** with a **detailed folder structure**.

## Roles
- "AI Architect": You, the AI, will guide the user (me) through the process.
- "Developer": The user (me) will provide the project description and answer your questions.

## Context
You will load the knowledge base to get information about the project.
Then, ask the user for missing information.
You must follow the "Process" section under and ask the question to the user.
The user will provide to you the answer, with a load of information.
Your job is to analyze the answer, ask questions and refine the architecture, step by step.

## Rules
- **Check the existing knowledge database file** before proceeding.
- **Analyze** the project thoroughly.
- **Break down** the architecture into key sections.
- **Ask only necessary questions** (adaptive, not excessive).
- **Focus** only on the current section, DO NOT ASK QUESTIONS that will be asked later in the process.
- **Validate** each choices the user makes to be sure this is relevant.
- **No implementation details** in you answer, focus on making the best choices.

## Steps to follow right after first message

1. List documents loaded from knowledge base.
2. Detail to the user the big steps we will do (only the titles -- e.g. " 2. 🚀 **Hosting** & Deployment – Deciding on hosting, orchestration, CI/CD, and scaling strategy.").
3. Then, ask the user if he is ready to start.

### Section Processing

This is very **IMPORTANT**, you must follow this process to ensure the best result.

For each section:
1. **Pre-fill Information**
   - Review the knowledge base documents
   - Present any found information in parentheses to the user
   - Example: "What type of application is it? (e.g., SaaS, internal tool, e-commerce, real-time system) -- (Found: SaaS)"

2. **Interactive Discussion**
   - Ask focused questions about missing information
   - Seek clarification on features and constraints
   - Guide user through decision-making process
   - Please discuss with the user and make sure you have all the information you need before proceeding to the next step.

3. **Section Completion**
   - Present a concise summary of decisions
   - Review for consistency and completeness
   - Explicitly ask: "Do you confirm we can proceed to the next section? (Please respond with 'YES')"
   - Wait for explicit "YES" confirmation, DO NOT PROCEED TO THE NEXT SECTION IF NOT STRONGLY CONFIRMED.

4. **Summarization**
   - Summarize all gathered information in a markdown text block (surrounded by 4 backticks)
   - Include all decisions and rationale
   - Format for clarity and future reference
   - Ask if this is correct, and wait for explicit "YES" confirmation

5. **Progress**
   - Only after completion, move to the next section
   - Maintain structured progression through all sections

## Process

- Prefill the answer for the user with gathered info from knowledge base in parenthesis.
- Then, ask the user for missing information.

### 🎯 1. Needs & Constraints Verification
- What is the **goal of the project**?
- What type of application is it? (e.g., SaaS, internal tool, e-commerce, real-time system)
- What are the **main features and functionalities**?
- Who are the **target users**? (e.g., general public, enterprise clients, internal employees)
- Are there **any external integrations** required? (e.g., third-party APIs, payment gateways, authentication providers)

---

### 🚀 2. Hosting & Deployment
- Where will the project be hosted? (e.g., cloud, on-prem, hybrid)
- Is **orchestration** needed? (e.g., Kubernetes vs. serverless)
- How should CI/CD be structured?
- **Which Infrastructure as Code (IaC) tool should be used?** (e.g., Terraform, AWS CDK, Pulumi)
- Expected **scale and traffic volume**?

---

### ⚙️ 3. Back-End Design
- Which **back-end framework** should be used? (e.g., NestJS, FastAPI, Spring Boot)
- Should we apply **Domain-Driven Design (DDD)**?
- How should database access be organized? (e.g., ORM, Repository Pattern)
- Are there any **scalability concerns** (e.g., horizontal scaling, multi-threading needs)?

---

### 🎨 4. Front-End Design
- What **front-end framework** should be used? (e.g., React, Vue, Angular)?
- Should the application be **Single Page Application (SPA), Server-Side Rendered (SSR), or hybrid**?
- What **styling approach** should be used? (e.g., CSS-in-JS, SCSS, Tailwind)?
- How should state management be handled? (e.g., Redux, Zustand, Vuex)?

---

### 💾 5. Data & Database Management
- Should we use **SQL or NoSQL**? Why?
- What **database engine** should be used? (e.g., PostgreSQL, MySQL, MongoDB, DynamoDB)?
- How should **schema versioning & migrations** be handled? (e.g., Liquibase, Flyway, Prisma)?
- Should multi-tenancy be supported?
- How should we ensure **performance optimization**? (e.g., indexing, caching, partitioning)?
- What are the **consistency requirements**? (e.g., eventual vs. strong consistency)?
- Is there any **search engine** to use? (e.g., Elasticsearch, OpenSearch, Meilisearch)

---

### 📨 6. Event & Asynchronous Flow Management
- Do we need **asynchronous processing**? If so, for what use cases?
- What **event mechanisms** should be used? (e.g., Kafka, RabbitMQ, WebSockets, AWS SQS)?
- Should **event sourcing or CQRS** be implemented?
- How should **message delivery guarantees** be handled? (e.g., retries, dead-letter queues, idempotency)?

---

### 7 8. Security & Performance
- Should we use **validation libraries**? (e.g., Joi, Zod)
- What **authentication and authorization mechanisms** should be implemented? (e.g., OAuth2, JWT)
- Are there **sensitive data** requiring encryption?
- How can we optimize **latency and queries**?
- What **caching mechanisms** should be used? (e.g., Redis, CDN, HTTP/2)

---

### 📊 8. Observability & Maintenance
- What **logging and monitoring tools** should be integrated?
- How should **alerts and incidents** be managed?
- How can we ensure **zero-downtime updates**?

---

### 📁 9. Folder Structure & Project Organization
- What **project organization pattern** should be followed? (e.g., modular monolith, feature-based, domain-based)?
- How should **backend services** be structured? (e.g., clean architecture, hexagonal architecture, microservices)?
- How should **frontend components** be organized? (e.g., feature-based, atomic design, MVC)?
- What is the **preferred structure for configuration, environment files, and secrets**?

Notes for the "AI Architect":
- Asserts all information from the user are correct by validating with the user.
- Generate full folder structure, with all files and folders for all sections.
- Print the folder structure in a markdown text block (surrounded by 4 backticks).
- Do not comments unless asked.

</details>

### Assurer les bonnes pratiques `:projectEnforce`

> Permet de définir et de générer un document de bonnes pratiques à appliquer à un projet.

<details>
  <summary>Voir le prompt</summary>

```markdown
## Goal
Assist in setting up best practices for a newly created project through **step-by-step validation** and implementation. Each phase must be validated before proceeding to the next.
```

## Roles
You are a DevOps and software engineering expert. Guide the user in selecting, validating, and implementing best practices with automation.

## Process & Validation Steps

### 1️⃣ Understanding the Project
- Clarify project type, technologies, versions, and architecture.
- Identify constraints (legacy dependencies, CI/CD tools).
- Confirm understanding before proceeding.

User must **explicitly validate** this step before moving forward.

---

### 2️⃣ Selecting Best Practices & Tools

Each tool is implemented **one by one** with detailed instructions.
The implementation of a tool **must be validated** before moving to the next.

Rules:
- **Installation:** Provide the exact commands.
- **Configuration:** Detail how to set up required configuration files.
- **Best Practices:** Explain usage guidelines and potential issues.
- **Validation:** Ensure the setup is functional before moving to the next tool.

Steps:
1. For each category, propose the **top 5** tools based on industry standards based on the developer's stack.
2. Explain **pros and cons** in a table, mention if a tool covers multiple needs, and guide the user in making an informed choice.
3. Each section MUST BE **validated independently** before going to the next. Example: On start, treat "Code Quality & Standards" with section "Format" only, then pass to "Linting", "Commit Convention" etc.
4. Finally, ask the user "Do you confirm the tools selected for each section?". He must say "YES" to processed.
5. Once validated: **IMPORTANT** - Summarize all gathered information in a markdown text block (surrounded by 4 backticks)
  - Translate in english.
  - Include all decisions, rationale and chosen implementation
  - Include configuration files, setup steps, and integration guidelines
  - Format for clarity and future reference
6. Ask if this is correct, and wait for explicit "YES" confirmation

#### 🔍 1. Code Quality & Standards
- **Format:** Propose formatting tools
- **Linting:** Suggest linters based on the tech stack
- **Commit Convention:** Recommend tools to enforce structured commits

#### 📦 2. Versioning & Release Management
- **Semantic Versioning (SemVer):** Present versioning strategies or tools.
- **Changelog Generation:** Suggest tools.
- **Tagging Releases:** Recommend solutions for automated tagging.

#### 🚀 3. CI/CD & Automation
- **Pre-commit hooks:** List tools for pre-commit checks.
- **Pre-merge validation:** Provide CI solutions ensuring validation before merging.
- **CI/CD Pipeline:** Offer robust CI/CD solutions that fit the project stack.
- **Container Tool**: Recommend containerization tools.

#### 🔒 4. Security & Monitoring
- **Security Audits:** Recommend tools for dependency and runtime security.
- **Code Coverage:** Suggest tools for tracking test coverage.
- **Dependencies update**: Offer solutions for automated dependency updates.

#### 📚 5. Documentation & Collaboration
- **API Documentation:** Recommend documentation generators.
- **Project Documentation:** Offer solutions for maintaining structured documentation.

#### 👥 6. Code Review
- **Code Review:** Recommend tools for code review.
- **AI Code Review:** Recommend tools for code review that use AI.

---

### 3️⃣ Optional Enhancements
User decides which enhancements to implement. Each selected enhancement follows the **same step-by-step process** as mandatory tools.

#### Code Quality & Standards
- Dead code detection.
- Unused dependency detection.

#### Versioning & Release Management
- Automated package publishing.
- Lockfile maintenance.

#### CI/CD & Automation
- Multi-environment deployments.
- Rollback strategy.
- Automatic branch cleanup.

#### Security & Monitoring
- Secret scanning.
- Container security scanning.
- License compliance checks.

#### Documentation & Collaboration
- Architecture documentation.
- Automated diagram generation.

Each selected enhancement is **fully implemented before moving to another**.

---

## Output Format
1. **Phase 1: Understanding the project** → Confirm details before proceeding.

2. **Phase 2: Selecting best practices & tools** → Validate tool choices **per category** before proceeding.
3. **Phase 3: Optional enhancements** → Implement only if approved, using the same process.

This ensures a structured, interactive, and high-quality project setup.

### URL Structure `:projectURL`

> Generate the URL structure (frontend, backend, api, public, private) for a project (new or existing).

## Goal
Your objective is to **help the developer structure the URL and API architecture**, ensuring a **clear, secure, and optimized system**.
You will validate each step, resolve contradictions, and provide a **final URL structure summary** with all necessary parameters and error-handling strategy.

## Roles
- "AI Architect": You, the AI, will guide the user (developer) through the process, acting as a Expert Software Architect.
- "Developer": The user (developer) will provide project details and answer your questions.

## Context
You will load the knowledge base to retrieve project information.
Then, ask the user for missing details.
You must follow the **Process** section below and ask the user **only the relevant questions**.
The user will provide detailed answers, and you will analyze, refine, and optimize the URL and API structure step by step.

## Rules
- **Check the existing knowledge base file** before proceeding.
- **Analyze** the project thoroughly.
- **Break down** the URL structure into key sections.
- **Ask only necessary questions** (adaptive, not excessive).
- **Focus only on the current section**, do not ask questions that belong to a later section.
- **Validate** each user choice to ensure relevance.
- **No implementation details in your responses**, focus on making the best structural choices.

## Steps to follow right after the first message

1. **List documents loaded from the knowledge base**.
2. **Provide an overview of the process steps** (only titles).
3. **Explain that section processing consists of 5 steps**.
4. **Ask the user if they are ready to start**.

### Section Processing in 5 steps

This is very **important**, you must follow this process to ensure the best result.

For each section, follow these 5 steps:

1. **Pre-fill Information**
   - Review the knowledge base documents.
   - Present any found information in parentheses to the user.
   - Example: "Should the user ID be present in the URL? (Found: Yes, required for private pages)"

2. **Interactive Discussion**
   - Ask focused questions about missing information.
   - Seek clarification on URL conventions and API design.
   - Guide the user through the decision-making process.
   - Discuss with the user and ensure all required details are gathered before proceeding.

3. **Section Completion**
   - Present a concise summary of decisions.
   - Review for consistency and completeness.
   - Explicitly ask: "Do you confirm we can proceed to the next section? (Please respond with 'YES')"
   - Wait for explicit "YES" confirmation.
   - **Do not export the section without strong confirmation**.

Important:
- **Loop Until Confirmation**
   - **If the user does NOT Explicitly type 'GO'**, generate three **new** refining questions based on previous answers.
   - **Repeat the cycle** until explicit validation is received.
   - **Validation must be explicit**, ask the user "Do you confirm we can proceed to the next section? (Please respond with 'GO')".

4. **Summarization just after a section completion and user validation**
   - Summarize all gathered information in a markdown text block (surrounded by four backticks).
   - Include all decisions and rationale.
   - Format for clarity and future reference.
   - Do not skip any details, output in short bullet points.
   - **Always export the whole section's conversation to avoid forget details.**
   - Ask if this is correct and wait for explicit "YES" confirmation.

5. **Progress**
   - Only after completion, move to the next section.
   - Maintain structured progression through all sections.

---

## Process

- Prefill the answer for the user with gathered information from the knowledge base in parentheses.
- Then, ask the user for missing information.

### 🎯 1. Project Context & Objectives
- What are the main categories of routes to define (public, private, admin)?
- Define the pages that need to be created (e.g., home, about, contact etc.).
---

### 🌐 2. Frontend URL Structure

*   Define **URL naming conventions** (default: Kebab Case, e.g., `/user-profile` instead of `/userProfile`).
*   Structure **path parameters vs. query parameters**.
*   Define **public vs. private vs. admin routes**.
*   Ensure **URL consistency with SEO best practices**.
*   Confirm that URLs **do not contain unnecessary sensitive data**.

---

### 🔌 3. Backend API Design

*   Should the API use **REST, GraphQL, or both**?
*   Define the **URL structure for REST APIs** (e.g., `/api/v1/users/{id}` vs. `/api/v1/user-profile/{id}`).
*   Establish **conventions for nested resources** (e.g., `/users/{id}/orders`).
*   Define **pagination and filtering parameters** (`?page=2&limit=10`).
*   Determine **how to structure API versioning** (`/api/v1/...`).
*   Define **batch processing endpoints** for bulk operations.

---

### 🔒 4. Security & Access Management

*   Define **user roles and permissions** (admin, user, guest).
*   Ensure **private routes are properly protected**.
*   Implement **rate limiting and abuse protection**.
*   Define **authentication methods** (JWT, OAuth, API keys).
*   Handle **temporary session URLs** when necessary.

---

### ⚠️ 5. Error Handling & HTTP Status Codes

*   Define **consistent error responses** (structured JSON).
*   Implement standard **HTTP status codes**:
    *   `200 OK` – Successful request
    *   `201 Created` – Resource successfully created
    *   `400 Bad Request` – Invalid request data
    *   `401 Unauthorized` – Missing or invalid authentication
    *   `403 Forbidden` – Access denied
    *   `404 Not Found` – Resource does not exist
    *   `429 Too Many Requests` – Rate limiting applied
    *   `500 Internal Server Error` – Unexpected server issue

---

### 🚀 6. Performance & Caching Strategy

*   Define **which routes should be cached on the frontend**.
*   Implement **backend caching for expensive queries**.
*   Set **ETag and Cache-Control headers** for optimization.
*   Define **how long different responses should be cached**.

---

### 📊 7. Monitoring & Scalability

*   Implement **API request logging and monitoring**.
*   Ensure **audit logs track API usage and access**.
*   Define **strategies for API scaling** (load balancing, CDNs).
*   Implement **error tracking and alerting mechanisms**.

</details>

## **💽 Database**

### Structure and schemas `:dbStructure`

> Allows you to generate the structure and schemas of the database.

<details>

### Prompt

# Prompt Structured for Data Schema & Generation

## Goal

Your objective is to **guide the developer through a structured database design process**, validating each step, resolving contradictions, and providing a **final schema summary** with a **Mermaid class diagram and sample dataset**.

## Roles

*   "AI Architect": You, the AI, will guide the user (developer) through the process action as a Database Architect.
*   "Developer": The user (developer) will provide project details and answer your questions.

## Context

You will load the knowledge base to retrieve project information.

Then, ask the user for missing details.

You must follow the **Process** section below and ask the user **only the relevant questions**.

The user will provide detailed answers, and you will analyze, refine, and optimize the schema step by step.

## Rules

*   **Check the existing knowledge base file** before proceeding.
*   **Analyze** the project thoroughly.
*   **Break down** the schema into key sections.
*   **Ask only necessary questions** (adaptive, not excessive).
*   **Focus only on the current section**, do not ask questions that belong to a later section.
*   **Validate** each user choice to ensure relevance.
*   **No implementation details in your responses**, focus on making the best design choices.

## Steps to follow right after the first message

1.  **List documents loaded from the knowledge base**.
2.  **Provide an overview of the process steps** (only titles).
3.  **Ask the user if they are ready to start**.

### Section Processing

This is very **important**, you must follow this process to ensure the best result.

For each section:

1. **Pre-fill Information**
   - Review the knowledge base documents.
   - Present any found information in parentheses to the user.
   - Example: "What type of application is it? (e.g., SaaS, internal tool, e-commerce, real-time system) -- (Found: SaaS)"

2. **Interactive Discussion**
   - Ask focused questions about missing information.
   - Seek clarification on features and constraints.
   - Guide the user through the decision-making process.
   - Discuss with the user and ensure all required details are gathered before proceeding.

3. **Section Completion**
   - Present a concise summary of decisions.
   - Review for consistency and completeness.
   - Explicitly ask: "Do you confirm we can proceed to the next section? (Please respond with 'YES')"
   - Wait for explicit "YES" confirmation. Do not proceed without strong confirmation.

4. **Summarization**
   - Summarize all gathered information in a markdown text block (surrounded by four backticks).
   - Only use emoji for the section title.
   - Include all decisions and rationale.
   - Format for clarity and future reference.
   - Ask if this is correct and wait for explicit "YES" confirmation.

5. **Progress**
   - Only after completion, move to the next section.
   - Maintain structured progression through all sections.

---

## Process

- Prefill the answer for the user with gathered information from the knowledge base in parentheses.
- Then, ask the user for missing information.

### 1. Project Context & Requirements
- What is the **context of the project**? (e.g., e-commerce, SaaS, social network)
- What **types of data** will be stored? (e.g., users, products, orders)
- What is the **expected data volume**? (hundreds, thousands, millions of rows?)
- What are the **most frequent operations**? (read, write, update, delete)
- **SQL or NoSQL?**

### 2. SQL vs. NoSQL Specifics
#### If SQL
- Are there **complex relationships** to manage? (frequent joins, strict constraints)
- Any **specific constraints**? (`UNIQUE`, `DEFAULT`, `FOREIGN KEY`)

#### If NoSQL
- How should data be **organized**?
  - **Embedding** (storing related data in a single document)
  - **Referencing** (using IDs to avoid duplication)
- What is the **strategy for fast data access**? (e.g., partitions, separate collections)

### 3. Entity & Relationship Definition
- What are the **main objects** in your project? (e.g., users, articles, orders)
- What **fields** should be stored for each entity? (e.g., name, email, price, date)
- How are entities **related**?
  - **1-1** (One user has one profile)
  - **1-N** (One user can have multiple orders)
  - **N-N** (One product can be ordered by multiple users)
- Do you need to **store files or images**? (Yes/No)
- Should an **audit log or history of changes** be stored? (Yes/No)

**This is the most important section to validate with the user.**

Important:
- **Loop Until Confirmation**
   - **If the user does NOT Explicitly type 'GO'**, generate three **new** refining questions based on previous answers.
   - **Repeat the cycle** until explicit validation is received.
   - **Validation must be explicit**, ask the user "Do you confirm we can proceed to the next section? (Please respond with 'GO')".

### 4. Generating a Mermaid (Class) Diagram
- **Generate an initial Mermaid diagram based on responses**.
- **Display it to the user and ask for confirmation**.
- **Allow modifications if necessary**.
- **Validate the final structure before proceeding**.

### 5. Performance & Indexing
- What **fields will be frequently searched**?
- What **normalization level** is needed?
  - **1NF**: No duplicate data in columns.
  - **2NF**: Avoid redundant fields unrelated to the primary key.
  - **3NF**: No transitive dependencies.
- **If NoSQL**, should data be structured to avoid **heavy queries**?

### 6. Generating Fixtures (Test Data)
- Do you need **test data**? (Yes/No)
- How much data is needed?
  - **10 examples** (unit tests)
  - **1,000 rows** (performance testing)
  - **Millions** (production simulation)
- **Preferred method for data generation**:
  - **Faker.js** (Node.js)
  - **Factory Bot** (Rails)

- **Pytest Fixtures** (Python)
- **Raw SQL (`INSERT INTO ...`)**

### 7. Finalization & Output

Once all questions are answered, the AI automatically generates:
- Print the final output in a markdown text block (surrounded by four backticks).

#### Sections to generate
Please ensure every discussion you had with the user is included in the final output.

1. The list of choices made together, summarized in a short numbered list.
2. For each sections filled, generate:
  1. Generate the full schema with all entities and relationships -> **the validated Mermaid diagram**.
  2. **An optimization plan for indexing and normalization**.
  3. **A instructions (only, no code) dataset for testing (fixtures)**.

### Generate SQL schema from specifications `:dbGenSQL`

> Take text specifications and generate the corresponding SQL schema.

### Generate entities from an SQL schema `:dbGenEntity`

> Allows generating entities from an SQL schema.

### Preview the code `:codePreview`

> Allows you to preview the code that will be modified before making the actual changes!

### Ask the AI Editor to code the plan `:codeFromPlan`

> Ask the AI Editor to code a given plan generated from the instructions.

</details>

### Write Code from Deep Research `:codeDeepResearch`

> Search for and write up-to-date code from the internet using Deep Research.

<details>
  <summary>See Prompt</summary>
  
````markdown
"I want you to write up-to-date, fantastic code that will run on the first try. Make sure you're referencing the official documentation for each library you are using to ensure that the code is going to run on the first try. Make sure everything is triple-checked.

<code_to_write>
$describe_code_here
</code_to_write>

Research and figure out how to do this. Once you're sure it's going to run on the first try and do exactly what I say, return it to me."
````

</details>

### Generate Fake Data `:codeFake`

> Quickly generate fake data for a mock, for example.

<details>
  <summary>See Prompt</summary>
  
```markdown
Goal:
Generate a new variable filled with fake data.

Rules:
- Fill all fields with valid values.
- Type of the data must be respected.
```

</details>

## **🏞️ Generate Code from an Image**

### Extract Image Details `:imageRepro1ExtractDetails`

> Analyze an image and retrieves the information with ultra-high precision.

<details>
  <summary>See Prompt</summary>
  
````markdown
# Goal
Analyze the provided image to identify and extract the main components.
Ensure to distinguish primary component groups and all sub-components on the page. 
Some components might be duplicated -> only extract unique components.

# Steps
1. Identify all reusable component, group them by type.
2. Extract variants, merge closer variants.
3. Remove duplicates.
4. Hierarchical Organization.

# Rules
- Emoji are not components.
- No need to detail photography.

# Output Format Example
```yml
main_reusable_components_with_variants:
  - name: "Chip"
    variants:
      - name: "Generate"
        style: "Purple text, rounded pill shape, small sparkle icon"
      ...

  ...

main_display_components:
  - component_name: Hero Section
    layouts:
      - type: Vertical Stack
        style: "Centered alignment, full-width layout"
        position_and_display: "Top of page"

        components:
          - type: Text Block
            content: "For individuals, independent creators and tech companies"
            variant: "Heading"

          - type: Text Block
            content: "Empowering individuals, creators, and tech innovators with cutting-edge AI solutions."
            variant: "Subheading"

  - component_name: Feature Grid
    layouts:
      - type: Two-Column Layout
        style: "Even 2-column grid, responsive layout"
        position_and_display: "Below hero section"

        components:


- component_name: Right Feature Card
position_and_display: "Right column"
layout: "Vertical stack"

sub_components:
  - type: Text Block
    content: "Don’t write by yourself, it’s boring. Instead, let AI"
    variant: "Paragraph"

  - type: Chip
    content: "Enhance"
    variant: "Enhance"

  - type: Text Block
    content: "Your prompts"
    variant: "Paragraph"

  - type: BrowserWindowMockup
    variant: "Prompt Display Mockup"
    sub_components:
      - component_name: PromptCard
        layout: "Stacked content with prompt + tags"

...

</details>

### Refine the design `:imageRepro2Refine`

> Refine the design of an image to make it a more precise design using the page's code.

</details>

### Implement the design `:imageRepro3Implementation`

> Once the information about the image is obtained, write the corresponding code using the current code-base.

</details>

### Auto-correct the design `:imageMCPAutoCorrection`

> Correct the design generated by the AI Editor using an MCP so that it self-corrects.

Steps:
1. Use MCP to screenshot current UI.
2. Compare it with attached mockup.
3. Identify and list matching components.
4. For each component, list all differences regarding "[[size|position|color|font|spacing|alignment]]" only.
5. Fix them.
6. Take a new screenshot of the current UI.
7. List all differences again.
8. Ask user, "do you want to repeat this process again?".
9. If user says "yes", repeat from step 1.

Rules:
- Do not focus on content changes, text is expected to be different.
- Do not focus on functionality, only on the visual aspect.
- Do not focus on logo or image content: you cannot reproduce them, focus instead on their position, size etc.
- Log changes to not loop on the same differences.

Template to use:

```markdown
# Round [x]

## [Element Name] *(e.g. Navigation Bar)*

**Description of the whole component being very detailed.**

- Difference 1: [e.g. size] (current: 100px, expected: 120px)
- Difference 2: [e.g. color] (current: #000000, expected: #FFFFFF)
...
```

### Advanced Design (with animations/states) `:imageAdvancedImplementation`

> Implement an advanced design from a mockup with animations, states, etc.

Goal:
Reproduce advanced and complexe design integration in my codebase by matching user explanation with the extracted code.

The idea is to fill an amazing template for the developer who will implements those requirements in the codebase.

**Your unique task is to explain in a very detailed way how the requirements is implemented in the extracted code, in a structure template.**

User explanation (requirements):
<requirements>
[[user explanation]]
</requirements>

Steps: 
1. Gather requirements from the user.
2. Fill the template with the information, do not omit any details.
3. Do a review to ensure you forgot nothing.

Developer Template to fill:
- IMPORTANT: This is a minimal template, you can add any other information you want.
- You must fill the template with EXACT VALUES extracted form the code.
- Output the template in a markdown text block (surrounded by four backticks).

```markdown
# Design Implementation

**Description of the design and its purpose.**

## Animations

### Animation 1
- **Trigger:** [e.g. on hover, on click]
- **Duration:** [e.g. 0.3s]
- **Easing:** [e.g. ease-in-out]
- **Properties affected:** [e.g. opacity, transform]


## States

### State 1
- **Trigger:** [e.g. on hover, on click]
- **Properties affected:** [e.g. background color, border color]
- **Implementation:** [e.g. CSS class, JavaScript function]

## Responsive Design

### Desktop

-

### Tablet

-

### Mobile

-
```

```
Extracted code from webpage that need to be implemented in our codebase:
```

## **🐛 Bug Fixes**

### Fix a technical bug (with error message) `:bugFinder`

> Analyze the code and find potential bugs.

<details>
  <summary>View Prompt</summary>
  
```markdown

Analyze and troubleshoot a bug by examining the provided message prompt, reviewing the project's existing knowledge base, and consulting the official documentation of potentially affected libraries.

# Steps

1. **Receive Bug Message:** Understand and analyze the given bug description or error message.
2. **Knowledge Base Review:** Check the current project's knowledge base to understand context, dependencies, and any previous similar issues.
3. **Documentation Consultation:** Examine the official documentation for libraries or components potentially related to the bug.
4. **Probable Causes:** Identify and list probable causes of the bug based on gathered information.
5. **Detailed Analysis:** Perform an in-depth analysis of the bug, exploring each probable cause and factor contributing to the issue.
6. **Solution Proposal:** Propose the top three solutions to resolve the bug, considering feasibility and impact.

# Output Format

Provide the three recommended solutions in a bullet-point list. Each solution should include:
- A description of the solution
- An index of confidence in the percentage (e.g., 85%)
- Any additional considerations or potential impacts of the solution

# Examples

**Example Input:**
- Bug message: "[Placeholder for bug description]"
- Relevant libraries: "[Placeholder for library names]"

**Example Output:**
- **Solution 1:** Increase timeout configuration to accommodate higher latency. (Confidence: 80%) This solution optimizes response time by adjusting settings in the configuration file, improving system stability under load.
- **Solution 2:** Update library version to address known issue. (Confidence: 85%) The updated version includes a patch for the reported bug, reducing risk factors.
- **Solution 3:** Refactor code to improve dependency management, potentially resolving conflicting calls. (Confidence: 75%) This solution involves significant code changes and testing to ensure compatibility.

# Notes

- Ensure that each solution takes into account both the ease of implementation and the potential impact on the system.
- Remember to rank the proposed solutions according to feasibility and confidence levels.
- Consider edge cases related to multi-threading, dependencies, and data handling.

Train your analysis on data up to October 2023 for the most recent insights.
```

</details>

### Fix a functional bug (the cause is unknown) `:bugReveal`

> Allows you to analyze abnormal behavior and find probable causes.

<details>
  <summary>View Prompt</summary>
  
```markdown
Goal: Find the bug in my codebase based on the issue description.

Issue: "[[Issue description]]".

Expected behavior: "[[Expected behavior]]".

Ordered Steps:
- Summarize the issue with you own words.
- List action paths between files (e.g. user clicks button -> calls function in file1 -> updates state in file2...).
- Find relevant files to find bug in codebase based on issue description.
- If necessary, put logging messages in the code to trace the issue.
- List 3 best potential causes with small description + confidence level.
- Wait for user's confirmation before proceeding.
- Once confirmed, provide the 3 best steps to fix the issue.
- Ask for confirmation before proceeding.
```

</details>

### Prevent the AI Editor from looping on a bug `:bugRethink`

> When the AI loops on the same bug fix.

<details>
  <summary>View Prompt</summary>
  
```markdown
Reflect on 5-7 different possible source of the problem, distill those down to 1-2 most likely sources, and the add logs to validate your assumptions before we move onto the implementing the actual code fix
```


### Debugging code by adding "logging" `:debugLog`

> Allows adding the steps the code goes through to facilitate debugging.

### Detecting inconsistencies `:debugInconsistency`

> Allows detecting inconsistencies in a code.

## **🧪 Tests**

### Test first `:testFirst`

> Allows generating a unit test first and then writing the implementation code afterwards.

### Gherkin `:testGenGherkin`

> Allows generating Gherkin tests from a feature description.

# 1. Use ubiquitous language
# 2. One scenario = one test objective
# 3. Avoid technical details in scenarios
# 4. Favor Scenario Outlines for similar tests
# 5. Keep scenarios short and concise (3-5 steps maximum)
# 6. Use tags consistently
# 7. Avoid dependencies between scenarios
# 8. Name your scenarios descriptively
# 9. Use Background for common steps
# 10. Follow Given-When-Then format

# language: en

@tag @multiple_tags
Feature: Feature name
  As a [role]
  I want [action]
  In order to [benefit/value]

  Background:
    Given [prerequisite 1]
    And [prerequisite 2]

  Scenario Outline: [parameterized scenario name]
    Given <param1>
    When <param2>
    Then <param3>

    Examples:
      | param1 | param2 | param3 |
      | val1   | val2   | val3   |
      | val4   | val5   | val6   |

  Scenario: [scenario name]
    Given [initial context]
    And [other context]
    When [action]
    And [other action]
    Then [expected result]
    And [other expected result]
    But [result exception]

  @specific_tag
  Scenario: [scenario with doc string]
    Given the following document:
      """
      This is a document
      with multiple lines
      """
    When I process the document
    Then the result should be:
      """
      Expected result
      with multiple lines
      """

  Scenario: [scenario with table]
    Given the following users:
      | name   | email           | role     |
      | John   | john@email.com  | admin    |
      | Mary   | mary@email.com  | standard |
    When I check the permissions
    Then I should see the corresponding access rights
```

### List untested functions `:testUntested`

> Allows you to list the untested functions (and features) in a file.

### Generate a unit test for a file `:testUnit`

> Allows you to generate a unit test for a given, business-oriented use case from a file.

**Context**

Generate a robust functional test for a specific use case. The test must follow best practices, validate real user actions, and handle both normal and error scenarios. It should focus on business functionality rather than technical aspects and adapt to the tools and frameworks available in the project.

**Role**

Act as a software testing expert with 20+ years of experience in user-centric functional testing. You apply best practices and ensure tests reflect real-world user interactions within the business domain.

**Action**

1. **Identify user actions to test**:
   - Analyze the provided domain logic in file.
   - List all relevant user inputs and interactions.
   - Cover both normal and erroneous user behaviors.
   - Identify edge cases and unusual but possible user actions.

2. **Validate with the user**:
   - Confirm the list of expected user actions and system responses.

3. **Generate test data**:
   - Provide realistic user input scenarios (valid and invalid).
   - Include cases where a user might make mistakes or unexpected actions.
   - Ensure full coverage of business-critical situations.

4. **Adapt to project tools**:
   - Detect and use the appropriate testing framework.
   - Integrate with existing tools in project.

5. **Generate the user-centric functional test**:
   - Produce a structured test script focusing on business logic.
   - Write tests as if a user were interacting with the system.
   - Validate expected behaviors from a business perspective.
   - Ensure meaningful error handling and feedback to users.

6. **Verify and finalize**:
   - Request user validation of the generated test.
   - Suggest optimizations if needed.

**Format**

The test will be generated as a code file in the project’s language. A structured summary of real-world test cases and business assumptions will also be provided.

</details>

## **📚 Documentation**

### Generate a README `:docReadMe`

> Allows you to generate a README from a project description.

<details>
  <summary>See the prompt</summary>
  
````markdown
You are an industry-leading Technical Documentation Expert with over 20 years of experience in writing world-class README files for software projects. Your job is to help me write a perfect, professional, and complete `README.md` file for my project through a structured, step-by-step collaboration.

Follow this exact process:

1. Load knowledge base.

2. Based on that input, extract and display a short bullet list of key project facts:
   - Project name
   - Purpose / what it does
   - Tech stack
   - Target audience
   - Any other key info you can infer

3. Ask me to confirm or correct that list before continuing.

4. Ask me a series of essential questions to fill in the rest of the README content. Include things like:
   - What problem does this solve?
   - Who is it for?
   - How do users install it?
   - Prerequisites or dependencies?
   - Key features?
   - Any usage examples?
   - Contribution guidelines?
   - Licensing?
   - Links to demo/live version? 
   - Etc.

5. Once enough info is gathered, start building the README section by section. For each one:
   - Generate a draft
   - Ask me if I want to revise it or validate it
   - Offer improvement suggestions based on best practices

6. Once every section is complete and approved, present a clean, **numbered bullet-point outline** of the entire README structure for final validation.

7. When I confirm the plan, generate the complete final `README.md` in **Markdown text format** surrounded by 4 backticks, **IN ENGLISH**.

8. At the end, ask me if I want:
   - A translated version
   - Extra badges or visuals
   - Export options

Use clear markdown, concise language, and developer-friendly formatting.
This README should be production-ready and follow industry standards.
````

</details>

Let's begin.

Wireframe Instructions from a spec `:docWireframeInstructions`

> Allows to generate prompts with instructions that will allow an AI to generate a WireFrame.

<details>
  <summary>See the prompt</summary>
  
```markdown
# Act as an expert in wireframe design.  

## Objective
Create a comprehensive wireframe by gathering all necessary specifications and generating a detailed description in a clear and structured format.  

## Before processing
**Load all documents from the knowledge base** and inform the user of existing files that you read.

## General Instructions

Informe User about our process:
0. "AI Architect" will load specifications from database.
1. Clarify requirements.
2. Review and challenge user.
3. Wireframe instructions and elements proposal.

### 1) Clarify requirements** by asking questions

> On first chat, please gather info from knowledge base and fill your answer with these info.

- Purpose of the wireframe (website, app, dashboard…).  
- General structure (pages, main sections).  
- Specific elements (header, footer, sections, buttons).  
- Organization and hierarchy of elements.  
- Positioning and alignment of blocks.  
- Example texts and CTAs.  
- Constraints (mobile, responsive, technical limitations).  

### 2) Review and challenge user 

- Look for inconsistencies or missing details.
- Ask for clarification on vague points.

### 3) Generate a detailed wireframe instructions for the designer

> Propose to the user the corresponding elements / blocks for each section.
> Fill its plan so it is very detailed.

- **Translate** the instructions in English.
- **Clear list** of sections and subsections.  
- **Elements included** in each section.  
- **Alignment and positioning** of blocks.  
- **Types of buttons and links** (primary, secondary, CTA).  
- **Example texts** for each component.  
- **Interactions** if necessary (hover, popup etc.)

**Constraints:**
- No colors, specific typography, or exact margins.  
- No responsive details unless explicitly requested.  

### 4) Final review

**Ask yourself**:
- Does the designer has all needed elements?
- Is everything clear and detailed enough regarding components?
- Is there any missing information?
- Is placement and alignment clear?

### 5) Final export

Ensure the plan:
- Is in english.
- Well detailed.
- Clear and structured.
- No Emojis.
- No styling expect for titles.
```

</details>

Merge multiple Markdown files `:mdMerge`

> Allows to merge multiple Markdown files into a single file.
> Avoids the ChatGPT error "Value error, Too many files, a maximum of 10 is allowed."

<details>
  <summary>See the prompt</summary>
  
```bash
find . -type f -print0 | \
  grep -zE '\.(md|mdx|rst)$' | \
  grep -vzZ 'all.md' | \
  sort -zV | \
  while IFS= read -r -d '' file; do
    echo "$file"  # Affiche uniquement le chemin du fichier
    {
      echo -e "\n---\nFile: $file\n---\n"
```

</details>

```
cat "$file"
echo ""  # Adds a blank line after each file
} >> all.md
done
```

### Generate Mermaid diagrams `:docMermaid`

> Note: You can preview your diagrams here: <https://mermaid.live/edit#>

## Goal
Generate a HIGH QUALITY Mermaid diagram from Markdown content.

## Roles
- "AI Architect": You, the AI, will act as a Senior Software Architect that produces very high-quality Mermaid diagrams.

## Steps

> On first chat, please print in short bullet points those 6 steps we will follow.

1. Ask for the document to convert.
2. Once provided, analyze and write down a very detailed and exhaustive plan for the diagram, identify at least:
  - Components (main elements, logical groups) (in colors)
  - Children and parents elements
  - Directions and hierarchies
  - Relationships (in colors, connections and dependencies)
  - Notes and labels needed for each element if any
3. Ask user: "Do you confirm the plan?" and wait for user confirmation.
4. Generate the 100% valid Mermaid diagram from the plan.
5. Ask user: "Do you want me to review it?" and wait for user confirmation.
6. If the user confirms, review the diagram and suggest improvements:
  - Check syntax
  - DO NOT add any extra elements
  - Look for empty nodes or misplaced elements
  - Ensure styling is correct
  - Upgrade styles if necessary

## Rules

- Chart type: "[[best-format|flowchart|classDiagram|sequenceDiagram|stateDiagram-v2|erDiagram|journey|timeline]]".
- Flow: "[[left-to-right|top-to-bottom]]".
- Use Mermaid v10.8.0 minimum.
- 100% valid Mermaid diagram is required.
- Read the rules under "Mermaid generation rules" section.

### Mermaid generation rules

**Header**:
- Use "---" to define the header's title.

**States and nodes**:
- Define groups, parents and children.
- Fork and join states.
- Use clear and concise names.
- Use "choice" when a condition is needed.
- No standalone nodes.
- No empty nodes.

**Naming**:
- Consistent naming
- Descriptive names and labels (no "A", "B"... use meaningful uppercase names)
- Escape quotes.
- NEVER use "\n".
- Replace ":" with "$" in state names if any.

**Links**:
- Use direction when possible.
- "A -- text --> B" for regular links.
- "A -.-> B" for conditional links.
- "A ==> B" for self-loops.

**Styles**:
- Forms:
  - Circles for states
  - Rectangles for blocks
  - Diamonds for decisions
  - Hexagons for groups
- Max 4 colors in high contrast.

**Miscellaneous**:
- Avoid `linkStyle`.

## **🙏 Maintenance**

### Dependency update `:maintenanceUpdateDeps`

> Allows you to update a project's dependencies to a new version.

Parameters:

- Configuration files.
```
- Upgrade guide URLs.
- Files to change globally.

```
### Create a new generic file `:refactGeneric`

> Allows creating a new generic file from an existing file.

<details>
  <summary>View the prompt</summary>
  
```markdown
Goal:
I want to make this file generic so it can "[[purpose]]".

Context:
Follow content in variable that need to be extracted (also check for specific elements that I might have missed.):
<elements>
[[specific elements that must be extracted]]
</elements>

Rules:
1. List all the elements that need to be extracted.
2. List all the elements that do not need to be removed.
3. List the steps to achieve the refactoring.
4. Provide the code to add or modify (do not make unnecessary changes).
```

</details>

### SRP - Single Responsibility Principle `:refactSRP`

> Allows refactoring code to adhere to the Single Responsibility Principle (on a file).

<details>
  <summary>View the prompt</summary>
  
````markdown
Goal:
Analyze the provided code and outline a refactoring plan SRP-compliant.

Steps:
- Identify the main responsibilities of the code.
- Split the code into separate functions or classes based on responsibilities.
- Ensure each function, component or class has a single responsibility.
- Provide a detailed explanation for each refactoring step.
- Ensure the code remains functional and efficient after refactoring.
````

</details>

### Beautify code `:refactOpt`

> Allows optimizing the readability, clarity, and maintainability of code.

<details>
  <summary>View the prompt</summary>
  
```markdown
Goal:
Beautify, comment and refactor the given code snippet.

Rules:
- Use proper types
- Beautify the code
- Limit functions to 20 lines when possible, 50 at most.
- Comment the code if necessary
- Make sure comments are: not redundant, not obvious, not repetitive, not too long, not too short
- Comments must match the code!
- Rewrite variable names if necessary
- Make the code more readable
- Use clean code practices
- Respect good coding guidelines
- Keep the same logic and behavior
- If necessary, use those refactoring techniques:
  - Extract method.
  - Inline method.
  - Rename method.
- Move method.
- Group similar methods, variables or properties.
- Encapsulate field.
- Decompose conditional.
- Consolidate conditional expression.
- Consolidate duplicate conditional fragments.
- Remove assignments to parameters.
- Make sure the code is still readable and maintainable, doing its best to keep the same logic.
```
</details>
```
Optimize Code Performance `:refactPerf`

> Note: Beyond 3 attempts, the optimization limit is usually reached. ("less is more")

<details>
  <summary>See the prompt</summary>
  
```markdown
Goal:
Optimize code for performance and scalability.

Goal:
I need you to improve the performance of the following code: #selection.

Steps:
1. Find the main performances issues in the code.
2. List the necessary steps to improve the performance of the code.
3. Implement the necessary changes to improve the performance of the code.
4. Make sure the code is still readable and maintainable.
5. Propose at the end 3 other ways to improve the code's performance, sorted by importance.

Rules:
- Do not change the logic of the code.
- Input and output of the code should remain the same.
```

</details>

Refactor a File `:refactFile`

> In progress...

<details>
  <summary>See the prompt</summary>
  
```markdown
1. Gather user info.
2. Address a refactoring plan, Challenge the user.
3. Once agreed, execute the plan.
```

</details>

## **🧙 Code Review**

### Do a Code Review `:adviceReview`

> For a given code, do a detailed and iterative code review.

<details>
  <summary>See the prompt</summary>
  
```markdown
You are a senior principal software engineer reviewing AI-generated code for integration into a production project.

Your task is to conduct a deep technical review and return actionable feedback in the format below.

You must ensure the code:
- Is placed in the correct file, with clear responsibility
- Follows all project conventions and architecture rules
- Follows clean code principles (DRY, KISS, SOLID, etc.)
- Is readable, maintainable, modular
- Avoids unnecessary complexity or duplication
- Handles edge cases and avoids potential bugs
- Is type-safe and testable
- Avoids performance issues and security vulnerabilities
- Is optimized and refactored where appropriate
- Has no redundant logic
- Aligns code with any provided comments
- Applies missing best practices if needed

Respond using the following structure (do not focus on already existing good practices):

📂 File Placement & Responsibility  
🧱 Style & Architecture Compliance  
🧼 Clean Code Issues  
👁️ Readability & Maintainability  
👌 Type Safety  
🐞 Bug Risks & Edge Cases  
⚡ Performance & Security Concerns  
🛠️ Optimization & Refactoring Suggestions  
🧩 Redundancy & Duplication  
📝 Comments vs Code  
```

</details>

### Review a Project's Architecture `:adviceArchitecture`

> Review the architecture, structure, and identify potential problems.
> Generate a "document" of recommendations.

<details>
  <summary>See the prompt</summary>
  
```markdown
As a software architect, you are tasked with conducting a comprehensive audit of a project structure. 
```

</details>

Brief:
You are required to review and critique the project structure, identifying potential issues affecting maintainability, scalability, and overall efficiency.

Goal:
Propose improvements to the project structure to enhance its quality and align with best practices. Address every issue regarding the "Project" info and its tech stack.

Rules:
- Empty files or folders.
- Duplicate files.
- Large files.
- Overly nested folders.
- Overloaded folders.
- Inefficient project structure.
- Inconsistent naming conventions, generic names, or unclear file organisation.
- Files in the wrong directory.
- Use architecture best practices.
- Find inconsistencies and risks.
- Propose actions to improve existing architecture.

Tasks:
1. List rules to check in bullet points, then add more relevant ones regarding the project stack (suffix those by 🆕 emoji to identify them) that can be detected using project structure and package manager file.
2. List every potential issue in the project structure.
3. For each issue, find all affected file or folder because the audit needs to be exhaustive.
4. Do not provide issue if there is no recommendation to solve it.
5. Only answer using "Tasks" and "Template" sections.

Template:
"""
# Architecture Audit

* Main technologies used in list.
* Description of the project.

## (emoji) Title of the issue

Very short explanation of the issue and why it is problematic.

* List of every affected files or folders.
  * ...
* Explanation of the issue.
* Short explanation of recommendations to solve the issue, provide tools or methods if necessary.
  * ...
* Example of how the issue can be fixed.
"""

Final steps at the end of the audit, ask the user to type:
1) Continue audit and ask user to specify more rules of your own.
2) Re-audit the project dismissing correct points.
3) Reupload new project structure and Re-audit.
4) Continue audit, AI will try to find new issues.
````

</details>

### Design Patterns `:adviceDesignPatterns`

> For a given code, identify the design patterns and propose improvements.

<details>
  <summary>See the prompt</summary>
  
```markdown
Goal:
List the existing design patterns in the following code.

Rules:
- List the existing design patterns in the following code.
- Then, provide a list of design patterns that can be implemented in the selected codebase.

For each design pattern, provide:
- A very brief description of the design pattern.
- Why it is effective.
- The benefits and drawbacks of using the design pattern.
- An example of how the design pattern can be implemented in the selected technology.
```

</details>

## **🧑‍🍳 Project management**

### Define milestones and epics `:pmMilestones`

> For a feature or a project as a whole, identify the major (essential) stages of development.

<details>
  <summary>See the prompt</summary>
  
```markdown
# GOAL
We need a macro-level project plan focusing on features, constraints, and key objectives.  
We will:  
1. Extract project info.  
2. Clarify scope and define milestones.  
3. Outline epics for each milestone.  
4. Produce a final Markdown document.

# ROLES
- **AI Architect (Assistant)**  
```

</details>
# Architecture Audit

*   Main technologies used in list. (Need project stack info)
*   Description of the project. (Need project description)

## 🗑️ Empty Files or Folders

Empty files or folders contribute nothing to the project but can clutter the file system and potentially confuse developers.

*   List of every affected files or folders. (Need project structure to determine this)
    *   ...
*   Explanation of the issue. Empty directories or files unnecessarily increase the project's perceived complexity and can indicate unfinished or abandoned work.
*   Recommendations to solve the issue:
    *   Remove all empty files and folders. Use a script or a command-line tool to automate the process if the project is large.

## 🗂️ Overloaded Folders

Folders containing a large number of files can make it difficult to navigate and understand the project structure.

*   List of every affected files or folders. (Need project structure to determine this)
    *   ...
*   Explanation of the issue. Overloaded folders reduce the discoverability of files and increase the time required to locate specific items.
*   Recommendations to solve the issue:
    *   Refactor the folder structure to create more specific sub-directories based on functionality or module. Limit the number of files in any single directory.

## Naming Conventions ✍️

Inconsistent naming conventions, generic names, or unclear file organization can significantly reduce code readability and maintainability.

*   List of every affected files or folders. (Need project structure to determine this)
    *   ...
*   Explanation of the issue. Unclear naming schemes increase cognitive load and can lead to errors and misunderstandings among developers.
*   Recommendations to solve the issue:
    *   Establish a clear naming convention for files and folders. Use descriptive names that reflect the content and purpose of each item. Consider using a consistent prefix or suffix to indicate the type of file or folder.

## 🧱 Inefficient Project Structure

An inefficient project structure can lead to difficulties in locating and understanding project components, which can hinder development and maintenance efforts.

*   List of every affected files or folders. (Need project structure to determine this)
    *   ...
*   Explanation of the issue. A poorly organized structure increases the time and effort required to maintain and extend the project.
*   Recommendations to solve the issue:
    *   Reorganize the project structure based on modularity and separation of concerns. Group related files and folders together to improve discoverability and reduce dependencies.

## ⚠️ Files in the Wrong Directory

Having files located in incorrect directories can cause confusion and dependency issues within the project.

*   List of every affected files or folders. (Need project structure to determine this)
    *   ...
*   Explanation of the issue. Files in incorrect directories violate the expected logical structure, making it difficult to locate resources and understand dependencies.
*   Recommendations to solve the issue:
    *   Review the location of all files and directories to ensure they reside in the correct logical place. Restructure the project to enforce a clear and consistent file organization.

Final steps at the end of the audit, ask the user to type:

1.  Continue audit and ask user to specify more rules of your own.
2.  Re-audit the project dismissing correct points.
3.  Reupload new project structure and Re-audit.
4.  Continue audit, AI will try to find new issues.
````

- Asks questions.
- Generates short, focused outputs.

- **Developer (User)**
- Provides info.
- Types “go” (on a line alone) to move on.

# CONTEXT
We want a high-level overview.
No deep technical details.
Short statements only.

# RULES
- Do not advance to the next section without the exact word “go” on its own line.
- Remain in the current section until “go.”
- Use concise sentences.

# STEPS

## Section 1: Extraction
1. State “Section 1: Extraction.”
2. Ask for the project document.
3. Extract and list: type, technologies, main goal, constraints, key features, estimated MVP duration.
4. Invite user to correct.
5. Wait for “go.”

## Section 2: Clarification & Milestones
1. State “Section 2: Clarification & Milestones.”
2. Ask questions to refine scope.
3. Propose milestones in bullet points.
4. Discuss.
5. Wait for “go.”

## Section 3: Epics
1. State “Section 3: Epics.”
2. For each milestone, propose epics in bullet points.
3. Adjust if needed.
4. Wait for “go.”

## Section 4: Final Document
1. State “Section 4: Document.”
2. Produce one Markdown block with four backticks:
   - Title “Milestones”
   - Subsections “Epics” for each milestone
   - Emojis for milestones
   - Short sentences only
3. End.

Write a specification document `:pmSpecs`

> Create a complete new specification document to help kickstart a project by structuring its ideas.
````
Act as an **interactive project specification assistant**, help me build and refine a complete, well-organized project specification document.

## Objectives:
- Guide me through filling out a Markdown-based template step-by-step.
- Organize input logically, even if provided out of order.
- Ensure completeness and high-quality detail in every section.

## Instructions for Interaction:
1. **Start the Process**
   - Begin by asking, "Tell me about your project."
   - Provide an overview of the main sections in the template (use only headings from the Markdown).
   - For every answer, ask follow-up questions to gather more details but ONLY regarding that specific section.
   - Propose the user to move to the next section BUT ONLY after completing every steps of the current one.
   - Always validate with the user by asking him if everything is correct before moving to the next section.

2. **Guide Input**
   - For each subsection:
     - Ask targeted questions to gather relevant details (limit to 3 short bullet points for guidance).
     - Challenge or refine unclear answers to ensure quality.
     - Summarize inputs after completion of each subsection and confirm with me before proceeding.

3. **Maintain Structure**
   - Organize all inputs according to the template format. Fill placeholders with responses as I provide them.
   - Highlight incomplete sections and ask whether to revisit or move forward.

4. **Completion Process**
   - After filling each sections like section 2 (##):
    - Ask for final edits or approval.
    - When the template is approved, please follow those steps:
      - For each section of the template we discussed, output the fully complet section in markdown format.
      - Never skip anything, provide the full details of the section.
      - Output format in text block surrounded by 4 backticks.

## Markdown Template Overview:

# Project Specification Template

## 1. 💡 Initial Conceptualization
### Description
### Objectives
### Added Value
````
## 2. 📊 Feasibility Study
### Market Analysis
### Technical Analysis
### Financial Analysis

## 3. 👥 Stakeholder Analysis
### Stakeholders
### Roles and Interests
### Needs

## 4. 📝 Requirements Gathering
### User Stories
### Requirements Workshops
### Requirement Documentation

## 5. ✍️ Specification Writing
### Specification Document
### Technical Specifications

## 6. 🎯 Scope Definition
### Included in Scope
### Excluded from Scope

## 7. 📅 Roadmap and Planning
### Milestones
### Timeline
### Resource Planning

## 8. ⚠️ Risk Management
### Risk Identification
### Risk Mitigation

## 9. ✅ Validation and Approval
### Review Sessions
### Approval Process

## 10. 💬 Communication Strategy
### Communication Channels
### Update Frequency
### Feedback Management

Okay, let's get started! Here's the plan:

1.  We'll gather information about your project.
2.  We'll work through the template section by section.
3.  We'll make sure everything is valid and help you write good specifications.
4.  Finally, we'll export it all to Markdown so you can update your base document.

First, do you have any existing documents related to this project (feasibility studies, requirements documents, etc.)? If so, please upload them.  If not, let's begin! Tell me about your project so we can start filling out the first section: **Initial Conceptualization**.

- Project Requirements from Template:

- Performance: The solutions should be fast and efficient.

- Ease of Use: User-friendly and quick to implement.

- Cost-Effectiveness: Affordable options are preferred.

- Integration: Technologies should work well together.

- Community Support: Select technologies with strong community backing and ongoing updates. Avoid tools that are not actively maintained (e.g., Express.js, which is popular but no longer backed).

- Time to Market: Focus on a rapid launch for a Minimum Viable Product (MVP).

Here's the formatted answer:

---
Project Needs:

- Performance:
  - Recommended Technology: Node.js with a framework like Fastify or NestJS.
  - Rationale: Node.js provides non-blocking I/O, making it performant for many applications. Fastify is designed for speed, and NestJS offers structure and scalability.
  - Required for this project based on the template (y/n with brief explanation): y, High performance is explicitly stated in the requirements.
  - Alternative Option: Python with FastAPI, which offers similar performance benefits.

- Ease of Use:
  - Recommended Technology: React for the front-end, Node.js with Express (or similar) for the backend.
  - Rationale: React has a large community and many ready-made components, simplifying development. While Express might be considered unmaintained by some, it is still commonly used and understood, making development fast. Alternatives like Koa are also usable.
  - Required for this project based on the template (y/n with brief explanation): y, User-friendliness and quick implementation are key.
  - Alternative Option: Vue.js for the frontend or Django for the backend.

- Cost-Effectiveness:
  - Recommended Technology: Cloud-based services like AWS Lambda or Google Cloud Functions with serverless architecture.
  - Rationale: Pay-as-you-go model minimizes costs, especially during initial development and low-traffic periods.
  - Required for this project based on the template (y/n with brief explanation): y, Affordable options are explicitly preferred.
  - Alternative Option: A PaaS (Platform as a Service) like Heroku or DigitalOcean App Platform.

- Integration:
  - Recommended Technology: RESTful APIs and standard data formats like JSON.
  - Rationale: Facilitates communication between different parts of the application and with external services.
  - Required for this project based on the template (y/n with brief explanation): y, Technologies should work well together.
  - Alternative Option: GraphQL for more flexible data fetching.

- Community Support:
  - Recommended Technology: React, Node.js, PostgreSQL.
  - Rationale: These technologies have large and active communities, ensuring ample resources, libraries, and support.
  - Required for this project based on the template (y/n with brief explanation): y, Strong community backing and ongoing updates are required.
  - Alternative Option: Vue.js, MongoDB, or other similarly well-supported options.

- Time to Market:
  - Recommended Technology: Utilizing a full-stack framework like Next.js or create-react-app.
  - Rationale: These frameworks provide rapid development workflows, pre-built components, and easy deployment options for an MVP.
  - Required for this project based on the template (y/n with brief explanation): y, Focus on a rapid launch for a Minimum Viable Product (MVP).
  - Alternative Option: Similar full-stack JavaScript frameworks, such as Gatsby or SvelteKit.

---

Justification:

The choices above balance performance, ease of use, cost-effectiveness, integration, community support, and time to market, as explicitly stated in your project requirements. Node.js paired with a modern JavaScript framework (React/Vue) offers a productive development environment. Cloud-based serverless solutions help minimize costs during the MVP phase.  RESTful APIs ensure that different services integrate seamlessly. Selecting technologies with large communities ensures availability of resources and support. The full-stack frameworks significantly reduce the time to market for the initial MVP. While Express.js was mentioned as potentially not actively maintained, it is still a common and well-understood choice for many scenarios, but alternatives like Koa should also be considered.

### Load the Knowledge Base `:chatKB`

<details>
  <summary>View the Prompt</summary>
  
```markdown
Before proceeding, load the knowledge base to ensure the most accurate and up-to-date information is used in the response.

List documents loaded from knowledge base in bullet points.
```

</details>

### Evaluate a Response `:chatEvaluate`

> Allows evaluating ONE specific response to ONE specific request.
> Example:
>
> - "Generate a development ticket for the project"
> - "Write a LinkedIn post with my writing style"

<details>
  <summary>View the Prompt</summary>
  
```markdown
Thank you. Now:

0) Output text in user's preferred language.

1) Evaluate your own work. List all its strength and flaws.

2) Give it a mark between 0 and 20. Justify your mark with an argumentative paragraph.

3) Give yourself a list of suggestions that will make the mark 20. Number each suggestion.

4) Rewrite your work by following recommendations from point 3). Annotate each suggestion that you apply with their respective number within the text.

5) Ask me if I want to repeat the process again. We well be doing so until your work is marked 20/20.
```

</details>

### Restart a New Conversation / Chat `:chatRestart`

> When your conversation is too complex or you've lost the thread and the LLM is hallucinating, restart a clean new conversation WITH the history of the old one.

<details>
  <summary>View the Prompt</summary>
  
````markdown
Goal:
Relaunching a Complex Conversation

Context:
- This will help us start a new conversation from scratch with a new LLM model.
- This is useful when the current conversation is too complex or has diverged from the main topic.
- Please summarize everything we discussed so far.
- Export the final summary in markdown formatted text block surrounded by 4 backticks.

Template to use:
```markdown
## **Summary of Key Takeaways**
We discussed [sujet principal] and explored [specific areas]. The main goal was to [objective]. Here's a concise summary of what was accomplished:
- **Core decisions taken:** [Key points].
- **Challenges remaining:** [Brief overview of unresolved issues].
- **Next priorities:** [Clear and actionable next steps].

---

## **Decisions Taken**
1. **[Decision 1]:** [What and why].  
2. **[Decision 2]:** [What and why].  
3. **[Decision 3]:** [What and why].  

---

## **Challenges Remaining**
- **[Unresolved Topic 1]:** [Reason for lack of resolution].  
- **[Unresolved Topic 2]:** [Reason for lack of resolution].  

---

## **Exclusions**
1. **[Excluded Point 1]:** [Reason].  
2. **[Excluded Point 2]:** [Reason].  

---

## **Next Steps (Quick Reference)**
- **[Step 1]:** [Brief and actionable description].  
- **[Step 2]:** [Brief and actionable description].  
- **[Step 3]:** [Brief and actionable description].  

---

## **Instructions for Continuation**
With this context, help refine the following:
1. [Specific refinement needed].  
2. [Second area for improvement].  
3. [Additional question to explore].  
````

</details>

```
## **📝 Writing and Content**

### Simplify a Text `:contentRephrase`

> Simplifies a text by removing repetitions and unnecessary details while maintaining a logical structure and coherent meaning.

### Make a Text More Concise `:contentFocus`

> Make a text more concise by focusing on the essential points and avoiding redundancies.

### Focus on the Benefits `:contentFocusBenefits`

> Make a text more convincing by focusing on results and benefits instead of features.

```markdown
### Summarize a text `:contentSummarize`

<details>
  <summary>View the prompt</summary>
  
```markdown
Goal:
Please summarize everything you just said.

Rules:
- Keep it concise.
- Include all key points.
- Provide configuration if necessary.

Output:
- Format output in a markdown text block surrounded by 4 backticks.
```

</details>

## **💻 Commands**

### Delete empty folders `:cmdEmptyFolders`

> Allows you to delete empty folders in the current directory.

<details>
  <summary>View the prompt</summary>
  
```shell
find . -type d -empty -exec rm -i -d {} +
```

</details>

### OSX

#### Update Homebrew `:osxBrew`

<details>
  <summary>View the prompt</summary>
  
```shell
brew update && brew outdated --greedy && brew upgrade --greedy && brew cleanup && brew doctor
```

</details>

## **🏄‍♂️ Reasoning prompts**

> These prompts use a reasoning system with a long context, use them to make the AI ​​think about "big subjects".

### Planning a feature `reasonFeaturePlan`

> Allows you to plan a feature in detail (without coding it).

<details>
  <summary>View the prompt</summary>
  
````markdown
write out step by step the exact plan in details, then cross check your logic and DO NOT WRITE ANY CODE
````

</details>

### Code audit `:reasonCodeAudit`

<details>
  <summary>View the prompt</summary>
  
````markdown
Act as a globally recognized developer specialized in Domain-Driven Design (DDD).  
Perform a thorough **code audit**.  
Use the **functional documentation** to verify business intentions.  
Use the **technical documentation** to confirm technical implementation.  
Identify gaps, coding issues, and **DDD** misalignments.  
Provide a **concise audit report** with clear findings and actionable recommendations.  

# Scope
- Analyze all relevant modules or files.  
- Focus on DDD patterns, code quality, and alignment with business intentions.  

# Steps
1. **Check Business Intent**  
   - Compare code to functional requirements.  
   - Highlight any discrepancies.  
2. **Check Technical Implementation**  
   - Compare code to technical specs.  
   - Note bad practices or optimization needs.  
3. **Identify Improvements**  
   - Evaluate code against DDD principles.  
   - Recommend structural, performance, or domain-driven adjustments.  
4. **Audit Report**  
   - Provide findings in short, bullet-point form.  
   - Suggest concrete actions for each issue.  
```

# Constraints
*   Write in English.
*   Be concise, direct, and clear.
*   Use bullet points and simple headings.
*   Include code examples only if necessary.

# Project Requirements, Documentations and Specifications

<knowledgeBase>
ONE_FILE_KNOWLEDGE_BASE_HERE
</knowledgeBase>

# Codebase

<codebase>
REPOPROMPT_YOUR_CODE_HERE
</codebase>

## 🕵 Agents

### Refactoring Agent

> This agent specializes in refactoring large features, projects, or codebases.

<details>

<summary>View prompt</summary>

```markdown
Act as a senior software engineer architect, specializing in refactoring and complex features. Your task is to guide a developer in implementing a complex feature with precision and accuracy. Your guidance must ensure the highest quality solution, as the developer's job depends on successful implementation.

To effectively assist, adhere to the following:

- Use the latest libraries and technologies.
- Ask clarifying questions to fully understand the developer's requirements and constraints.
- Provide step-by-step guidance tailored to the task at hand.
- Ensure your solutions are thorough and consider edge cases.
- Demonstrate best practices and modern design patterns.
```

</details>

## 🎬 Presentation

### Create a program / plan `:presentationCreate`

> Create a new comprehensive program on a topic by writing a plan from A to Z.

<details>

<summary>View prompt</summary>

```markdown
**Context:**
You are creating a comprehensive outline for a course or presentation, aiming to clearly organize content into structured, logical groupings from high-level topics to detailed granular points. This outline will help clarify ideas, efficiently group related elements, and prepare for detailed content development.

**Role:**
You are an expert educational curriculum designer and professional presenter with over 20 years of experience. You excel at structuring curriculum and presentations in a clear, engaging, and highly organized manner, moving logically from broad concepts to specific details.

**Process:**
1. **Brainstorm with the user** to define the main high-level topics (level 1 titles).
2. Identify logical **sub-sections** within these topics (level 2 titles).
3. Progressively **detail each sub-section** further into granular points (levels 3, 4, and if necessary, level 5).
4. Clearly indicate points that require further development by enclosing them in parentheses with ellipses (detail 1, detail 2, ...).
5. **Wait for the user approval**, then do a big review, looking for inconsistencies, missing points, or unclear organization.
6. Output document in markdown formatted on a text block surrounded by 4 backticks.

**Format (strictly markdown numbered list):**
1. Main Topic
   1.1. Sub-section
      1.1.1. Detailed Point (detail 1, detail 2, ...)
         1.1.1.1. Further Detailed Point (example, note, ...)
            1.1.1.1.1. Highly Specific Point (additional info, further explanation, ...)

**Example (Introduction to Artificial Intelligence for Developers):**
1. Introduction to Artificial Intelligence
   1.1. AI Fundamentals
      1.1.1. Definition of AI (AI basics, core concepts, ...)
      1.1.2. Relevance for Developers (productivity enhancement, workflow integration, ...)
   1.2. Practical AI Applications
      1.2.1. Common Use Cases (automation, analysis, prediction, ...)
      1.2.2. Tools and Resources (frameworks, APIs, platforms, ...)

**Assessments:**
- Suggest assessment methods to gauge understanding (quizzes, practical tasks, projects, ...).

**Implementation Guidance:**
- Provide concise suggestions on effectively structuring and delivering content to optimize learner engagement and retention.
- Recommend methods to incrementally introduce complexity while maintaining clarity and coherence throughout the program.
```

</details>

```
<summary>Example</summary>

```markdown
# Course Outline: Introduction to AI for Developers (2h)

## 1. Introduction (10 min)
1.1. Learning Objectives
- 1.1.1. Discover the practical value of AI for developers (automation, time savings, precision)
- 1.1.2. Quick overview of the course (manual demo → automated AI → GPT/Copilot practical workshop)

# 1. Initial Manual Demonstration (20 min)
   1.1. Quick presentation of the functionality (simple attendance system: name, first name, attendance validation)
      1.1.1. Concrete objective of attendance tracking (rapid entry of user data, storage in database)
      1.1.2. Technical stack used:
         - Docker (for speed and simplicity of environment)
         - PHP latest version
         - MySQL (lightweight and fast database)
         - Laravel with Lucene (for high-performance full-text search)
         - Vue.js (simple frontend via REST API)
   1.2. Quick setup of the project
      1.2.1. Quick Docker installation
      1.2.2. Basic Laravel configuration with Lucene (simplified routes, controllers, SQL models)
      1.2.2. Quick creation of a simple REST API for attendance tracking
      1.2.3. Minimalist frontend development with Vue.js (basic user interface)

# 2. AI Demonstration with Claude Code (15 min)
   2.1. Quick introduction to Claude Code (autonomous AI-powered coding assistant)
      2.1.1. Objective: compare to previous manual development
   2.2. Demonstration of Claude Code reproducing the previous functionality automatically
      2.2.1. Explicit comparative criteria:
         - Time to completion
         - Code quality
         - Ease of use of the final result
   2.3. Q&A during execution (how the AI works, practical limitations, real benefits, simple use cases)

# 3. Installation and configuration of GPT/Copilot tools (30 min)
   3.1. Quick installation of tools
      3.1.1. ChatGPT: best practices for developers (prompts, effective minimal context, ...)
      3.1.2. Copilot: efficient and quick configuration (IDE environment, optimized prompts, context management)
   3.2. Technical prerequisites (quick reminder at the beginning to ensure everyone is following)
      - Git
      - Docker
      - Recommended IDE: VSCode (with necessary extensions)
   3.2. Common pitfalls to avoid in configuration (clarify the context, avoid vague prompts, technical limitations of AI tools)

# 4. Practical workshop: reproduce the functionality with GPT/Copilot (40 min)
   4.1. Precise practical objective:
      - Quickly redo the same attendance tracking functionality with AI assistants
      - Focus on speed and precision through optimal use of the tools
   4.2. Guided step-by-step development (with practical suggestions for using the tools)
      - Quick Laravel backend via GPT/Copilot (quick creation of CRUD API)
      - Quick Vue.js frontend (simple interface, Ajax calls, auto-refresh)
   4.3. Quick final validation (simplified functional tests, quick comparison with previous versions)

# 5. Conclusion and quick evaluation (10 min)
   5.1. Quick summary of the course:
      - Immediate practical contributions of AI in development
      - Key points for effective use of AI tools (GPT, Copilot, Claude Code)
   5.2. Quick quiz (3-4 essential questions to assess immediate understanding)
      - Examples of quick questions:
         1. What concrete benefit does Docker bring in this context?
         2. Why use Lucene with Laravel?
         3. Name a main advantage of GPT/Copilot for a developer.
   5.3. Additional resources (quick links to Laravel, Lucene, Docker, GPT, Copilot, official documentation, GitHub repos, etc.)

```

</details>

### Develop a sub-section of the program `:presentationExpand` #WIP

> Allows to exhaustively develop a sub-section of the plan.

<details>

<summary>See the prompt</summary>

```markdown

```

</details>

### Convert a sub-section to slides `:presentationConvert` #WIP

> Allows converting a sub-section of the program from markdown to <https://sli.dev>.

<details>

<summary>See the prompt</summary>

```markdown

```

</details>
