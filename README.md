# LinkedIn Post Optimiser

A data-driven toolkit for scoring, improving and maximising the reach
of LinkedIn posts. Built on analysis of 1.8M+ posts and designed for
B2B thought leadership.

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

**1. Algorithm Research** - the evidence base. Data on how LinkedIn's
algorithm weights engagement signals, the golden window, dwell time,
comment threading and format multipliers. Read this first to
understand *why* the other components work.

**2. Virality Checker** - an AI prompt that scores draft LinkedIn
posts 0-100 across six categories: hook quality, content structure,
engagement triggers, content value, technical optimisation and
audience calibration. Use it with any AI assistant (Claude, ChatGPT,
etc.) by pasting the prompt and your draft post.

**3. Post Accelerator Playbook** - a step-by-step guide for what to do
before, during and after publishing. Covers the 30-minute golden
window, cross-engagement strategy and what not to do.

## Getting started

### 1. Create your LinkedIn Strategy Profile

The Virality Checker is designed to work with a **LinkedIn Strategy
Profile** - a markdown file that describes your target audience, tone,
expertise areas and content themes. This means the universal scoring
framework adapts to your specific context.

Copy `profiles/strategy-profile-template.md` and fill it in. See
`profiles/example-strategy-profile.md` for a worked example.

If you're using an AI assistant, you can ask it to help:

> "I want to create a LinkedIn Strategy Profile. Ask me the questions
> I need to answer."

### 2. Score a post

Open your AI assistant, paste the content of
`skill/linkedin-virality-checker.md` as context, load your strategy
profile and then paste your draft post:

> "Here's my draft LinkedIn post. Score it using the virality checker."

Target 70+ before publishing.

### 3. Follow the playbook

Once your post scores 70+, use `playbook/post-accelerator-playbook.md`
for the publishing workflow. The full playbook is for high-stakes
posts; the light version covers everyday publishing.

## Key findings from the research

- The first 30 minutes determine 75% of total reach
- Comments from industry experts carry 5-7x more algorithmic weight
- Posts with 3+ person comment threads get 5.2x amplification
- External links in the post body reduce reach by 25-40%
- Dwell time (61+ seconds) correlates with 15.6% engagement rate vs
  1.2% for posts viewed under 3 seconds
- AI-detected content sees ~30% reach reduction

## Research sources

- 1.8M+ posts (van der Blom Algorithm Insights 2025)
- 1M posts (Socialinsider)
- 621,833 posts (AuthoredUp)
- 50,000+ posts (LinkIntel)
- 40+ additional sources on LinkedIn algorithm mechanics and B2B engagement

## Contributing

If you have additional research data or improvements to the scoring
framework, pull requests are welcome.

## Licence

MIT
