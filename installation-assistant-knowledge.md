# AI Winter School - Installation Assistant Knowledge Base

This document is the knowledge source for an assistant that helps students install and set up the software used at the CAITG AI Winter School (27-30 July 2026, Camperdown). It restates the participant setup guide in a form built for answering installation questions.

---

## How the assistant should use this document

**Your role.** You help winter school participants install and configure the tools listed below. You are patient, friendly, and plain-spoken. Many participants are not confident with the command line or with installing software, so explain things simply and one step at a time.

**Before giving steps.** If the participant has not said which system they are on, ask first: Windows, macOS, or Linux. For macOS, also ask whether it is Apple Silicon (M1 or newer) or an Intel Mac, because some tools differ. Then give only the steps for their system.

**Stay grounded.** Use only the links, commands, and versions in this document. Do not invent steps, filenames, version numbers, or download links. If something is not covered here, say so and point the participant to a facilitator rather than guessing.

**Reassure about timing.** Participants do not need to install anything before the school. Everything is done together in class, following the setup guide. The one exception is administrator rights: if a participant cannot install software on their computer, they should sort that out before the school or bring a machine they can install on.

**Safety rules you must follow.**

- Never ask a participant for, or accept, passwords, API keys, credit card or payment details. If a step needs any of these, tell the participant to enter it themselves.
- Do not tell participants to turn off their antivirus or security software in general. Only the specific, vendor-documented steps in this document are acceptable (for example, choosing "More info" then "Run anyway" on Windows for the named apps below).
- Where relevant, remind participants about privacy and backups (see "Safety and permissions").
- Stay on topic. Help only with installing and setting up these tools. For anything else, refer the participant to a facilitator.

**When to escalate.** If the answer is not in this document, or a step still fails after the documented fix, tell the participant to ask a facilitator during the setup session, or to contact the organisers.

---

## Quick facts

- The school runs 27-30 July 2026 at the Camperdown campus.
- There is no need to install anything in advance. Installation is done together in class.
- The only reason to prepare in advance is if the participant does not have administrator rights to install software on their computer.
- The tools, by day:
  - Day 2 (Dr Nathaniel Butterworth, Google Developer Group masterclass): Google account, Google Colab, Kaggle, Google AI Studio, Antigravity IDE, plus Python (conda), Node.js, and uv.
  - Day 3 (writing, Dr Bronwyn Dyson): Cogniti. Day 3 (literature review, Francesco Bailo): Obsidian and Hermes agent, plus access to an LLM.
  - Day 4 (Dr Justin Kyle Miller): Field of Study (FoS) package. Day 4 (text analytics): LDaCA Wordflow.
  - Used across several sessions: LM Studio and access to at least one LLM.
  - Group activity: a Padlet link.

---

## Safety and permissions

**Agentic software and your data.** During the school you install AI software that acts on your own computer. This kind of software necessarily has read and write access to your files, and it may send data off your computer through an API whenever you use a language model that does not run locally. Nothing dangerous is planned, but before installing and running these tools it is wise to:

- Remove confidential information from your computer, along with any personal or identifiable information about other people (for example students or research participants).
- Back up anything important. Backing up is always a good idea, and especially before installing new software.

**Administrator rights.** Installing desktop applications usually requires administrator rights on the computer. On a locked-down or institution-managed laptop this may be blocked. A participant in that situation should arrange the right permissions before the school, or bring a machine they can install on. Getting permissions changed can take time.

---

## Platform support at a glance

- Google account, Colab, Kaggle, AI Studio: any computer with a browser.
- Antigravity IDE: download the installer for your operating system.
- Python (via conda), Node.js, uv: Windows, macOS, Linux.
- LM Studio: Windows, macOS, Linux.
- Obsidian: Windows, macOS (Intel and Apple Silicon), Linux. Does not need administrator rights.
- Hermes agent: desktop installers for macOS and Windows; on Linux use the terminal install.
- Field of Study (FoS): any computer with Python.
- Cogniti: any computer with a browser (nothing to install).
- LDaCA Wordflow: desktop installers for Windows (x64) and macOS (Apple Silicon only). Intel Macs and Linux have no desktop installer and use the browser or uv fallback.
- Padlet: any computer with a browser.

---

## Tool: Google account, Colab, Kaggle, and Google AI Studio

**What it is and who needs it.** Used on Day 2 (Dr Nathaniel Butterworth). A Google account gives access to Google Colab (cloud Python notebooks), Kaggle, and Google AI Studio. It is also the account used to sign in to Antigravity.

**Steps.** If the participant does not already have a Google account, they create one, then sign in once to each service to confirm it works.

- Google account: https://myaccount.google.com/
- Google Colab: https://colab.research.google.com/
- Kaggle: https://www.kaggle.com/
- Google AI Studio: https://aistudio.google.com/prompts/new_chat

**Workshop notes** (updated up to the course): https://gdgaiforscience.github.io/CAITG-WinterSchool/

**Common questions.**

- "I don't have a Google account." They can create a free one at the link above. A personal Gmail address is fine.
- "Is Google AI Studio the same as LM Studio?" No. Google AI Studio is a Google website for using Gemini models in the cloud. LM Studio is a separate desktop app for running models on your own computer. They are different tools with similar names.

---

## Tool: Antigravity IDE

**What it is and who needs it.** Used on Day 2. Antigravity is Google's AI-assisted code editor, built on top of Visual Studio Code, with agentic AI features. It is the main tool for the Day 2 sessions.

**Steps.**

1. Download and install Antigravity IDE for your operating system: https://antigravity.google/download#antigravity-ide
2. On first launch, work through the short configuration steps (the defaults are fine) and sign in with your Google account.

**Also needed for the Day 2 demos:** Python via conda, Node.js, and the uv package manager. See their own sections below.

**Permissions caution.** Antigravity is powerful and can modify or delete files. Advise participants to review the permissions they grant it and to proceed thoughtfully.

**Common questions.**

- "Which account do I sign in with?" The same Google account used for Colab, Kaggle, and AI Studio.
- "Do I still need Visual Studio Code?" Not for Antigravity itself, since Antigravity is built on VS Code. A plain VS Code install is only needed if the participant prefers it for other local work.

---

## Tool: Python (via conda) and a code editor

**What it is and who needs it.** Used for the Day 2 masterclass, the Field of Study (FoS) package, and any session where code runs on the participant's own computer.

**Recommended install.** Install Python through conda (Miniforge), which makes it easy to create separate environments for different sessions.

- conda (Miniforge): https://conda-forge.org/download/

Plain Python (version 3.11 or later) also works if the participant prefers it: https://www.python.org/downloads/

**Code editor.** If Antigravity is installed, the participant already has an editor, since Antigravity is built on Visual Studio Code. Otherwise, Visual Studio Code is a good free editor: https://code.visualstudio.com/

**Common questions.**

- "conda or plain Python?" Either works. Conda (Miniforge) is recommended because it manages separate environments cleanly. If the participant only ever uses Google Colab, they can skip installing Python locally, because Colab runs Python in the cloud. Note that the Day 2 Antigravity demos and the local-model sessions do need Python on the participant's own machine.

---

## Tool: Node.js and the uv package manager

**What it is and who needs it.** Needed for the Day 2 Antigravity demos. Node.js is used for the BigQuery demo. The uv package manager is used to run the MCP demos, and it is also useful for running LDaCA Wordflow without installing it.

**Steps.**

- Node.js: https://nodejs.org/
- uv package manager: https://docs.astral.sh/uv/getting-started/installation/

---

## Tool: LM Studio (run a language model on your own computer)

**What it is and who needs it.** Used across several sessions. LM Studio is a free desktop app (Windows, macOS, Linux) that downloads and runs open-source language models entirely on the participant's own machine, with no data leaving the computer. It is also a free way to meet the "access to an LLM" requirement.

**Steps.**

1. Download and install for your operating system: https://lmstudio.ai/download
2. Open LM Studio, go to the Discover tab, and download at least one small model. A 4B-parameter model (for example a small Llama, Qwen, or Gemma model) is a good starting point and runs on most laptops.
3. Load the model in the Chat tab and send a test prompt to confirm it works.
4. Optional: in the Developer or Local Server tab, start the local server. This exposes an API that tools such as Hermes can connect to.

**Common questions.**

- "Which model should I download?" Start with a small model, around 4B parameters. Smaller models run faster and use less memory.
- "It is very slow, or it will not load." The model is probably too large for the computer's memory. Try a smaller model.
- "macOS says the app is damaged and cannot be opened." This is a known macOS quarantine message for some downloaded apps. The documented fix for LM Studio is to open Terminal and run: `xattr -cr /Applications/LM\ Studio.app` then open the app again. Only apply this to LM Studio, which is a known, trusted app.

---

## Access to at least one LLM

**What it is and who needs it.** Needed for Day 3 (literature review) and Day 4, and useful throughout. Participants need to be able to reach a language model in one of two ways:

- A local model via LM Studio (free), or
- An API key from a provider such as OpenAI, Anthropic, Google, or OpenRouter.

If possible, participants should have access to more than one model, because some exercises compare outputs across models.

**Common questions.**

- "Do I have to pay?" Running a local model with LM Studio is free. API keys from commercial providers usually require a paid account or credit. If a participant does not want to pay, the local option through LM Studio is the way to go.
- "What is an API key?" It is a secret code from a model provider that lets a program use that provider's models. Participants create it in their own account with the provider, and paste it into the tool that needs it. The assistant must never ask a participant to share their API key.

---

## Tool: Obsidian

**What it is and who needs it.** Used on Day 3 (literature review, Francesco Bailo). Obsidian is a free note-taking and knowledge-management app that stores notes as plain markdown files in a local folder called a vault. It is used to organise literature notes and the links between them.

**Steps.**

1. Download and install Obsidian for the participant's operating system: https://obsidian.md/download
2. Open Obsidian and create a new vault when prompted. A vault is just a folder for the notes, so any location is fine.

Obsidian is free for personal use, needs no account, and installs into a user folder without administrator rights. It works on Windows, macOS (Intel and Apple Silicon), and Linux.

**Common questions.**

- "Do I need an account or to pay?" No. Obsidian is free for personal use and needs no sign-up. Notes stay on the computer as markdown files.
- "I don't have admin rights on my laptop." Obsidian installs into a user folder and does not need administrator rights, so it should install anyway.
- "What is a vault?" It is simply a folder where Obsidian keeps the notes. Creating one is part of first launch, and any location works.

---

## Tool: Hermes agent

**What it is and who needs it.** Used on Day 3 (literature review, Francesco Bailo). Hermes is an open-source AI agent from Nous Research, used together with an LLM (a local model via LM Studio, or an API key). It comes in two forms, and a participant only needs one. The desktop app is recommended for most people.

### Option A: Desktop app (recommended, no terminal needed)

The desktop app is a normal graphical application, and it installs the command-line version at the same time.

1. Go to https://hermes-agent.nousresearch.com/ and download the installer. macOS and Windows have direct downloads. On Linux, use Option B.
2. Run the installer. On Windows the installer is not signed yet, so a SmartScreen warning may appear. Choose "More info", then "Run anyway".
3. Open the app, sign in when prompted, and choose your model. Point it either at the LM Studio local server or at an API key.

### Option B: Command line (for those who prefer the terminal)

1. Install with the one-line command for your system:
   - macOS, Linux, or WSL2:
     ```
     curl -fsSL https://hermes-agent.nousresearch.com/install.sh | bash
     ```
   - Windows (native), in PowerShell:
     ```
     iex (irm https://hermes-agent.nousresearch.com/install.ps1)
     ```
   The installer bundles what it needs, including its own Python.
2. Reload the shell and start it:
   ```
   source ~/.bashrc
   hermes
   ```
   On macOS this may be `source ~/.zshrc` instead.
3. Choose the model with `hermes model`.

**Documentation:** https://hermes-agent.nousresearch.com/docs/
**Repository:** https://github.com/nousresearch/hermes-agent

**Common questions.**

- "Desktop or command line?" For most participants, the desktop app is easier and needs no terminal. The command line is fine for those comfortable with it.
- "Windows blocked the installer / SmartScreen warning." The Windows installer is not code-signed yet, so this warning is expected. Choose "More info", then "Run anyway".
- "My antivirus flagged uv.exe as malware." This is a known false positive. `uv` is the Python package manager Hermes bundles. The vendor-documented fix is to whitelist the Hermes bin folder in the antivirus (not the individual file, since it changes with updates). If unsure, the participant should ask a facilitator rather than change security settings on their own.

---

## Tool: Field of Study (FoS) package

**What it is and who needs it.** Used on Day 4 (Dr Justin Kyle Miller, text classification and agent-based modelling).

**Steps.** Download the files from the repository and follow the instructions in its README to install.

- https://github.com/ZJU-Computational-Social-Science-Lab/fos

This package runs locally, so it needs Python installed (see the Python section) and access to an LLM (a local model via LM Studio, or an API key). More than one LLM is helpful.

**Common questions.**

- "What do I need before this works?" Python on your own machine, and access to at least one LLM.

---

## Tool: Cogniti

**What it is and who needs it.** Used on Day 3 (writing, Dr Bronwyn Dyson). Cogniti is a University of Sydney web tool for custom AI teaching agents. It runs in the browser, so there is nothing to install.

**The agent used in the session:**

- https://app.cogniti.ai/agents/6a5ebd80c2014df40d477a4f/chat?k=qIuPxVpu0X64gc5wXP7FzJmFXHbEPgRx6lcsMhDXyck

**Steps.** Open the link in a browser and sign in. Participants can log in with a University of Sydney account or a Google account. Microsoft accounts also work. This means both University of Sydney and external participants can access it.

**Reading.** Dr Dyson has asked participants to read Chapter 5, "The Craft of Writing", by Helen Sword, in advance. This reading is circulated separately.

**Common questions.**

- "Which account do I use?" A University of Sydney login, a Google account, or a Microsoft account all work. External participants can use a Google or Microsoft account.
- "The link asks me to sign in." That is expected. Cogniti provides access through a login. Sign in with one of the account types above.

---

## Tool: LDaCA Wordflow

**What it is and who needs it.** Used on Day 4 (text analytics). LDaCA Wordflow is a desktop text analytics app from the Australian Text Analytics Platform, with tools for exploring a corpus (Frequency, Concordance, Trends, and more). The installed desktop version is used in the session.

**Where to get it.** The download links are in the "Latest" section of the repository:

- https://github.com/Australian-Text-Analytics-Platform/LDaCa_Text_Analytics_Tools/

**Steps.** For the current release (v0.5.6), download the full installer. The full installer is recommended for a first install because it includes everything the app needs and sets itself up on first launch without an internet connection.

- Windows: https://github.com/Australian-Text-Analytics-Platform/ldaca-wordflow/releases/download/v0.5.6/ldaca-wordflow-bundle-x64-0.5.6.msi
- macOS (Apple Silicon): https://github.com/Australian-Text-Analytics-Platform/ldaca-wordflow/releases/download/v0.5.6/ldaca-wordflow-bundle-apple-silicon-0.5.6.dmg

The macOS app is signed by Apple. On Windows a security prompt may appear: choose "More info", then "Run anyway". Advise participants to check the repository for a newer version before installing, since these links point to one specific release.

**If there is no installer for the participant's machine** (for example an Intel Mac, or Linux), Wordflow can run without being installed, in one of two ways:

- Open the browser-based Binder link in the repository (nothing to install), or
- If the participant has the uv package manager, run:
  ```
  uvx --refresh ldaca-wordflow@0.5.6
  ```

**Common questions.**

- "There is no Mac installer that matches my Mac." The macOS installer is for Apple Silicon Macs only. On an Intel Mac, use the Binder link or the uv command above.
- "I use Linux." There is no Linux desktop installer. Use the Binder link or the uv command above.
- "How do I know if my Mac is Apple Silicon or Intel?" Open the Apple menu and choose "About This Mac". Apple Silicon shows a chip name starting with "Apple M" (for example Apple M1, M2, M3). Intel shows an Intel processor.
- "Windows blocked the installer." Choose "More info", then "Run anyway". The Windows prompt is expected.

---

## Tool: Padlet group activity

**What it is.** A shared Padlet used for one of the group activities. It is password protected, and the password is circulated closer to the event.

- https://padlet.com/sydney/2026-caitg-winter-school-group-activity-ohsrn137fed7nr9w

**Common questions.**

- "It asks for a password." The password is circulated closer to the event. If the participant does not have it, direct them to a facilitator.

---

## General troubleshooting

**"Do I need to install everything before Monday?"** No. Everything is set up together in class, following the setup guide. The only thing to arrange in advance is administrator rights, if the participant cannot install software on their computer.

**"I don't have permission to install software."** The participant needs administrator rights on their computer to install the desktop apps. They should arrange this before the school, or bring a machine they can install on.

**"Windows says it protected my PC, or shows a blue SmartScreen box."** Some installers used at the school are not code-signed, so Windows shows this warning. For the named apps in this document (Hermes and LDaCA Wordflow), choose "More info", then "Run anyway". If the participant is unsure whether an installer is one of these, ask them what they were installing, and only confirm the step for the apps listed here.

**"macOS says an app is damaged or cannot be opened."** For LM Studio, the documented fix is to run `xattr -cr /Applications/LM\ Studio.app` in Terminal, then open the app again. For other apps, if there is no documented fix in this document, direct the participant to a facilitator rather than guessing.

**"Is my data safe using these tools?"** These are agentic tools with read and write access to the computer, and they can send data to a model provider through an API when a non-local model is used. Advise participants to remove confidential or personal information before running the tools, and to back up important files. Local models via LM Studio keep data on the computer.

**"The tool needs an API key and I don't want to pay."** Use a local model with LM Studio instead, which is free.

**Something not covered here.** Tell the participant this is outside what you can help with, and to ask a facilitator during the setup session.

---

## Escalation and contacts

If a participant's problem is not covered in this document, or a step still fails after the documented fix, direct them to a facilitator during the in-class setup, or to the organisers.
