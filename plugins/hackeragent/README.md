# HackerAgent Installation

## Quick Install

```bash
git clone https://github.com/edumame/hackeragent.git
cd hackeragent/skill && ./setup
```

The setup script auto-detects your agent (Claude Code, Codex, Cursor, Gemini CLI, Windsurf) and installs the skill.

## What Gets Installed

1. A `/mentormates` skill command in your agent's skill directory
2. A SessionStart hook that auto-injects hackathon context into every conversation
3. A `~/.hackeragent/` config directory

## Setup Your Project

After installing, connect to your hackathon project using one of these methods:

### Option A: Copy from MentorMates (recommended)
When you create a project on MentorMates, it generates a ready-to-paste config. Copy it into your terminal:

```bash
echo '{"token":"YOUR_TOKEN","mm_project_id":"YOUR_PROJECT_ID","mm_event_id":"YOUR_EVENT_ID","api_url":"https://hackeragent.vercel.app"}' > ~/.hackeragent/config.json
```

### Option B: Use your MentorMates API key
```bash
echo '{"api_key":"mm_key_...","api_url":"https://hackeragent.vercel.app"}' > ~/.hackeragent/config.json
```

Then type `/mentormates` to create projects automatically.

### Option C: Interactive
Type `/mentormates` in your agent and follow the prompts.

## Verify

After setup, your agent will automatically:
- Load hackathon context (judging criteria, sponsor challenges, deadlines)
- Sync your project progress as you build
- Auto-populate your submission when you're ready

Type `/mentormates status` to check your connection.
