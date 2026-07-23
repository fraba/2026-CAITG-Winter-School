# AI Winter School - Software setup guide

> **Please read this first.**
>
> During the school you will install *agentic* AI software on your own computer. This kind of software necessarily has read and write access to the files on your machine, and it may move data off your computer through an API (for example, whenever you use a language model that does not run locally). We will not be doing anything inherently dangerous during the school, but before you install and run these tools it is a good idea to:
>
> - Remove confidential information from your computer, along with any personal or identifiable information about other people (for example students or research participants).
> - Back up anything important. Backing up your computer is always a good idea, and especially so before installing new software.

## Before you arrive

You do **not** need to install anything in advance. We will install and configure these tools together in class, working through this document step by step.

There is one exception. If you do **not** have administrator rights to install software on your own computer (for example, a locked-down or institution-managed laptop), please arrange this before the school, or bring a machine on which you can install software. Sorting out permissions can take time, and without them you will not be able to install the applications when we do this together.

## Need help with the setup?

If you get stuck at any point, you can ask the Winter School installation assistant. It is a chatbot that can walk you through the steps on this page.

- <https://app.cogniti.ai/agents/6a559641a6f6e7bc9a81fb41/chat?k=fxgX-l_NcY-93cx9UhwXLOdCDAboh1yhKGXzyOVWpZM>

Sign in with a University of Sydney, Google, or Microsoft account to use it.

## Quick checklist

- [ ] Google account, with access to Colab, Kaggle, Google AI Studio and Antigravity
- [ ] Antigravity IDE installed (Day 2)
- [ ] Python, installed via conda
- [ ] Node.js and the uv package manager (for the Day 2 Antigravity demos)
- [ ] LM Studio installed, with at least one small local model downloaded
- [ ] Access to at least one LLM (a local model via LM Studio, or an API key)
- [ ] Obsidian installed (for the literature review session)
- [ ] Hermes agent installed (desktop app or command line)
- [ ] Field of Study (FoS) package downloaded
- [ ] Cogniti agent opened in your browser (signed in with a USyd or Google account)
- [ ] LDaCA Wordflow desktop app installed
- [ ] Padlet group-activity link (password to follow)

---

## Google account, Colab, Kaggle, AI Studio and Antigravity

**Used for:** Day 2, Dr Nathaniel Butterworth and the Google Developer Group AI for Science masterclass (Python, LLMs, AI agents and computer vision).

You need a Google account so you can use Google Colab (cloud notebooks), Kaggle, Google AI Studio and Antigravity (see the next section).

**What to do:** If you do not already have a Google account, create one, then sign in to each of the services below at least once to confirm they work.

- Google account: <https://myaccount.google.com/>
- Google Colab: <https://colab.research.google.com/>
- Kaggle: <https://www.kaggle.com/>
- Google AI Studio: <https://aistudio.google.com/prompts/new_chat>

Please also read the workshop notes before the session. They will be updated up until the course, so check back closer to the date:

- <https://gdgaiforscience.github.io/CAITG-WinterSchool/>

---

## Antigravity IDE

**Used for:** Day 2, the Google Developer Group AI for Science masterclass.

Antigravity is Google's AI-assisted code editor. It is built on top of Visual Studio Code, with agentic AI features built in, and is the main tool used across the Day 2 sessions.

**What to do:**

1. Download and install Antigravity IDE for your operating system: <https://antigravity.google/download#antigravity-ide>
2. The first time you launch it, work through the short configuration steps (the defaults are fine) and sign in with your Google account.

**Also install these, so the Day 2 demos run smoothly:**

- **Python via conda** (see the Python section below): <https://conda-forge.org/download/>
- **Node.js** (needed for the BigQuery demo): <https://nodejs.org/>
- **uv package manager** (needed to run the MCP demos): <https://docs.astral.sh/uv/getting-started/installation/>

A note on permissions: Antigravity is powerful and can modify or delete files, so review the permissions you grant it and proceed thoughtfully.

---

## LM Studio (run a language model on your own laptop)

**Used for:** running local models in several hands-on sessions, including the prompting activities and Day 4 with Dr Justin Kyle Miller. This also gives you a free way to meet the "access to an LLM" requirement below.

LM Studio is a free desktop app (Windows, macOS and Linux) that lets you download and run open-source language models entirely on your own machine, with no data leaving your computer.

**What to do:**

1. Download the installer for your operating system from <https://lmstudio.ai/download> and install it.
2. Open LM Studio, go to the **Discover** tab, and download at least one small model. A 4B-parameter model (for example a small Llama, Qwen or Gemma model) is a good starting point and will run on most laptops.
3. Load the model in the **Chat** tab and send a test prompt to confirm it works.
4. Optional but useful: in the **Developer** / **Local Server** tab, start the local server. This exposes an API that other tools (such as Hermes) can connect to.

Smaller models run faster and use less memory. If your laptop struggles, try a smaller model.

---

## Access to at least one LLM

**Used for:** Day 3 (AI for literature review) and Day 4, and useful throughout.

You need to be able to reach a language model, either of these ways:

- **A local model via LM Studio** (free, see above), or
- **An API key** from a provider such as OpenAI, Anthropic, Google or OpenRouter (these usually require a paid account or credit).

If at all possible, please have access to **more than one** model, as some exercises benefit from comparing outputs across models.

---

## Obsidian

**Used for:** Day 3, Francesco Bailo (AI for literature review).

Obsidian is a free note-taking and knowledge-management app that stores everything as plain markdown files in a local folder (called a "vault"). We will use it to organise literature notes and the links between them during the literature review session.

**What to do:**

1. Download and install Obsidian for your operating system from <https://obsidian.md/download>. It is free for personal use, needs no account, and works on Windows, macOS (Intel and Apple Silicon) and Linux.
2. Open Obsidian and create a new vault when prompted. A vault is just a folder where your notes are kept, so any location on your computer is fine.

Obsidian installs into a user folder and does not need administrator rights, so you can install it even on a locked-down or institution-managed laptop.

---

## Hermes agent

**Used for:** Day 3, Francesco Bailo (AI for literature review).

Hermes is an open-source AI agent from Nous Research. We will use it together with an LLM (either a local model via LM Studio, or an API key). It comes in two forms, and you only need one.

**Option A: Desktop app (recommended, no terminal needed).**

The desktop app is a normal graphical application, and it installs the command-line version for you at the same time.

1. Go to <https://hermes-agent.nousresearch.com/> and download the installer for your system. macOS and Windows have direct downloads; on Linux, use the terminal install in Option B.
2. Run the installer. On Windows the installer is not signed yet, so you may see a SmartScreen warning. Click "More info", then "Run anyway".
3. Open the app, sign in when prompted, and choose your model. Point it either at your LM Studio local server or at an API key.

**Option B: Command line (if you prefer the terminal).**

1. Install with the one-line command for your system:
   - macOS, Linux or WSL2:
     ```
     curl -fsSL https://hermes-agent.nousresearch.com/install.sh | bash
     ```
   - Windows (native), in PowerShell:
     ```
     iex (irm https://hermes-agent.nousresearch.com/install.ps1)
     ```
   The installer bundles what it needs (including its own Python), so you do not need to install Python separately just for Hermes.
2. Reload your shell and start it:
   ```
   source ~/.bashrc
   hermes
   ```
   (On macOS you may need `source ~/.zshrc` instead.)
3. Choose your model with `hermes model`. Point it either at your LM Studio local server or at an API key.

Full documentation and troubleshooting: <https://hermes-agent.nousresearch.com/docs/>

Repository: <https://github.com/nousresearch/hermes-agent>

---

## Field of Study (FoS) package

**Used for:** Day 4, Dr Justin Kyle Miller (text classification and agent-based modelling).

**What to do:** Download the files from the repository below and follow the instructions in its README to install.

- <https://github.com/ZJU-Computational-Social-Science-Lab/fos>

This package runs locally, so you will need Python installed (see the Python and code editor section below) as well as access to an LLM (local via LM Studio, or an API key). More than one LLM is helpful if you can manage it.

---

## Cogniti

**Used for:** Day 3, Dr Bronwyn Dyson (writing).

Cogniti is a University of Sydney web tool for custom AI teaching agents. It runs in your browser, so there is nothing to install. We will use this agent in the session:

- <https://app.cogniti.ai/agents/6a5ebd80c2014df40d477a4f/chat?k=qIuPxVpu0X64gc5wXP7FzJmFXHbEPgRx6lcsMhDXyck>

**What to do:** Open the link above in your browser and sign in. You can log in with a University of Sydney account or a Google account (Microsoft accounts also work), so both University of Sydney and external participants can access it.

Bronwyn has also asked participants to read Chapter 5, "The Craft of Writing", from Helen Sword in advance. This reading will be circulated separately.

---

## LDaCA Wordflow

**Used for:** Day 4 text analytics session.

LDaCA Wordflow is a desktop text analytics app from the Australian Text Analytics Platform, with tools for exploring a corpus (Frequency, Concordance, Trends and more). We will use the installed desktop version.

**What to do:** Install the desktop app for your operating system. The download links live in the "Latest" section of the repository:

- <https://github.com/Australian-Text-Analytics-Platform/LDaCa_Text_Analytics_Tools/>

For the current release (v0.5.6), download the **full installer**. This is recommended for a first install, as it includes everything the app needs and sets itself up on first launch without an internet connection.

- Windows: <https://github.com/Australian-Text-Analytics-Platform/ldaca-wordflow/releases/download/v0.5.6/ldaca-wordflow-bundle-x64-0.5.6.msi>
- macOS (Apple Silicon): <https://github.com/Australian-Text-Analytics-Platform/ldaca-wordflow/releases/download/v0.5.6/ldaca-wordflow-bundle-apple-silicon-0.5.6.dmg>

The macOS app is signed by Apple. On Windows you may see a security prompt: choose "More info", then "Run anyway".

Please check the repository for a newer version before installing, as the links above point to one specific release.

**If there is no installer for your machine** (for example an Intel Mac, or Linux), you can run Wordflow without installing it, in one of two ways:

- Open the browser-based Binder link in the repository (nothing to install), or
- If you have the uv package manager (see the Antigravity section), run:
  ```
  uvx --refresh ldaca-wordflow@0.5.6
  ```

---

## Python and a code editor

**Used for:** the Day 2 masterclass, the FoS package, and any session where you run code on your own machine.

We recommend installing Python through **conda** (Miniforge), which makes it easy to create isolated environments for different sessions:

- conda (Miniforge): <https://conda-forge.org/download/>

Plain Python (version 3.11 or later) from <https://www.python.org/downloads/> also works if you prefer.

You will also want a code editor. If you install Antigravity (above) you already have one, since it is built on Visual Studio Code. If you would rather use a plain editor for the local sessions, install Visual Studio Code:

- <https://code.visualstudio.com/>

If you only ever follow along in Google Colab, you can skip installing Python locally, as Colab runs Python in the cloud. Note, however, that the Day 2 Antigravity demos and the local-model sessions do need Python on your own machine.

---

## Padlet group activity

**Used for:** a group activity during the school.

There is a shared Padlet for one of the group activities. It is password protected, and the password will be circulated closer to the event.

- <https://padlet.com/sydney/2026-caitg-winter-school-group-activity-ohsrn137fed7nr9w>

---

*We will work through all of this together in class, so there is no need to install anything in advance. If you are unsure whether you have permission to install software on your computer, please check before the school (see "Before you arrive" above).*
