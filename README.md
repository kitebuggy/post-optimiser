# LinkedIn Post Optimiser

A data-driven toolkit for scoring, improving and maximising the reach of LinkedIn posts. Built on analysis of 1.8M+ posts, updated for LinkedIn's 360Brew algorithm overhaul, and designed for B2B thought leadership.

## What's in this repo

```
linkedin-post-optimiser/
├── research/
│   └── linkedin-algorithm-research.md    # The data behind everything
├── skill/
│   └── linkedin-virality-checker.md      # AI prompt: scores posts 0-100
├── playbook/
│   └── post-accelerator-playbook.md      # Step-by-step publishing guide
├── profiles/
│   ├── strategy-profile-template.md      # Blank template - fill in yours
│   └── example-strategy-profile.md       # Worked example (fictional company)
└── README.md
```

## How it works

The toolkit has three components that work together:

**1. [Algorithm Research](research/linkedin-algorithm-research.md)** — the evidence base. Covers both the engagement mechanics that determine post distribution (golden window, dwell time, comment threading, format multipliers) and the 360Brew algorithm shift that changed how LinkedIn evaluates content and creators. Read this first to understand *why* the other components work.

**2. [Virality Checker](skill/linkedin-virality-checker.md)** — an AI prompt that scores draft LinkedIn posts 0–100 across six categories: hook quality, content structure, engagement triggers, content value, technical optimisation and audience calibration. Includes a two-level AI tell detection system: lexical tells (word and phrase patterns) and a rhetorical pattern scan (ten structural moves that signal AI-generated content). Use it with any AI assistant (Claude, ChatGPT, etc.) by pasting the prompt and your draft post.

**3. [Post Accelerator Playbook](playbook/post-accelerator-playbook.md)** — a step-by-step guide for what to do before, during and after publishing. Covers profile-level foundations (topic authority, profile-content alignment), the 30-minute golden window, cross-engagement strategy, save-worthy content and what not to do.

## Getting started

### Step 1: Set up the Virality Checker in your AI assistant

The checker works with any AI assistant (Claude, ChatGPT, Gemini, etc.). Open a new conversation and paste the following:

> I want you to act as my LinkedIn post scorer. Here are your instructions:
>
> [paste the entire contents of [`skill/linkedin-virality-checker.md`](skill/linkedin-virality-checker.md) here]

The assistant will now understand the scoring framework and how to use it.

### Step 2: Create your LinkedIn Strategy Profile

The checker scores posts against six categories. The last one, Audience Calibration, adapts to your specific context using a **LinkedIn Strategy Profile** — a markdown file that describes your target audience, tone, expertise areas and content themes.

You have two options:

**Option A: Build one interactively (recommended)**

In the same conversation where you loaded the checker, say:

> "I don't have a LinkedIn Strategy Profile yet. Help me create one."

The assistant will walk you through seven sections one at a time, asking 1–2 questions per step. At the end it will present a completed profile for you to save.

**Option B: Fill in the template manually**

Copy [`profiles/strategy-profile-template.md`](profiles/strategy-profile-template.md), fill in each section and save it. See [`profiles/example-strategy-profile.md`](profiles/example-strategy-profile.md) for a worked example of a completed profile.

### Step 3: Load your profile (if using Option B or a saved profile)

In your AI conversation, paste your completed profile:

> Here is my LinkedIn Strategy Profile. Use this for audience calibration when scoring posts:
>
> [paste the contents of your saved profile here]

### Step 4: Score a post

Paste your draft LinkedIn post and ask:

> "Score this post."

The assistant will return a score out of 100 with a category breakdown, strengths, improvements, AI tells (lexical and rhetorical), anti-pattern flags and human signal bonuses. Target 70+ before publishing.

### Step 5: Follow the playbook

Once your post scores 70+, use [`playbook/post-accelerator-playbook.md`](playbook/post-accelerator-playbook.md) for the publishing workflow. The full playbook is for high-stakes posts; the light version covers everyday publishing.

### Tips for ongoing use

- **Save your strategy profile** as a file so you can paste it into new conversations without rebuilding it each time.
- **You don't need to reload the checker every time** if your AI assistant supports custom instructions, system prompts or project knowledge. Upload the checker and your profile there for persistent access.
- **The research document** ([`research/linkedin-algorithm-research.md`](research/linkedin-algorithm-research.md)) is useful background reading but doesn't need to be loaded into the AI. The checker already incorporates the research findings into its scoring criteria.

## Key findings from the research

### Engagement mechanics (still valid under 360Brew)
- The first 30 minutes determine 75% of total reach
- Comments from industry experts carry 5–7x more algorithmic weight
- Posts with 3+ person comment threads get 5.2x amplification
- External links in the post body reduce reach by 25–40%
- Dwell time (61+ seconds) correlates with 15.6% engagement rate vs 1.2% for posts viewed under 3 seconds

### The 360Brew shift (late 2025 onwards)
- LinkedIn replaced its algorithm with a 150-billion-parameter AI model that evaluates content semantically
- AI-generated content receives ~30% less reach and ~55% less engagement
- Posts with recognisable AI template patterns see up to 47% less organic reach
- Saves have become one of the most critical ranking signals, ahead of likes
- The algorithm evaluates the creator's profile, topic consistency and engagement patterns — not just the post
- Topic authority builds over 60–90 days of consistent posting within a defined niche
- Optimal posting frequency is 3–4 per week (daily posting cannibalises distribution)

## Research sources

- 1.8M+ posts (van der Blom Algorithm Insights 2025)
- 3M+ posts (AuthoredUp, Q3 2025)
- 3,368 posts from 99 profiles (Originality.ai, January 2026)
- 1M posts (Socialinsider)
- 621,833 posts (AuthoredUp, 2024)
- 500+ B2B profiles (Brixon Group)
- 50,000+ posts (LinkIntel)
- LinkedIn 360Brew engineering documentation and third-party analyses
- 60+ additional sources on LinkedIn algorithm mechanics, AI content detection and B2B engagement

## Contributing

If you have additional research data or improvements to the scoring framework, pull requests are welcome.

## Licence

MIT
