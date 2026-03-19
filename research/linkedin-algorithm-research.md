# LinkedIn Algorithm Research

## Overview

This document captures research findings on LinkedIn's content
distribution algorithm, drawn from multiple large-scale analyses. It
is structured in two parts:

**Part 1 — Early Engagement Mechanics** covers the engagement signals,
golden window and format multipliers that determine how posts are
distributed once they pass the initial quality filter. This research
was conducted in late 2025 and the underlying mechanics remain valid.

**Part 2 — The 360Brew Shift (March 2026 update)** covers LinkedIn's
fundamental algorithm overhaul: the replacement of task-specific
ranking models with a single 150-billion-parameter AI model called
360Brew. This changes *what gets through the quality filter in the
first place*, particularly for AI-generated content, and introduces
semantic analysis, topic authority scoring and AI content detection.

The engagement mechanics in Part 1 still apply — once a post clears
the 360Brew quality gate, the golden window, comment threading and
dwell time dynamics are unchanged. But 360Brew means that
template-following, AI-patterned posts may never reach the engagement
test at all.

---

# Part 1: Early Engagement Mechanics

*Research basis: 1.8M+ posts (van der Blom Algorithm Insights 2025),
50,000+ posts (LinkIntel), 1M posts (Socialinsider), 621,833 posts
(AuthoredUp), and 40+ additional sources.*

---

## The Golden Window: First 30 Minutes

LinkIntel's analysis of 50,000+ posts found that the first 30 minutes
now influence **75% of total reach**, up from 60% in 2024. Posts where
the author responds to comments within 30 minutes receive:

- 64% more total comments
- 2.3x more views

This is the single highest-leverage intervention point after the
content itself. The algorithm uses early engagement velocity to decide
whether to push the post to a wider audience beyond the initial 2–5%
sample.

Under 360Brew, LinkedIn now calls this "Sustained Relevance Scoring"
rather than the golden hour. The concept is similar, but the window
for high-quality posts has extended: posts that maintain genuine
engagement over 48–72 hours can achieve 340% longer active
distribution time.

---

## Engagement Signal Hierarchy

LinkedIn's algorithm does not treat all engagement equally. The
weighting from highest to lowest value:

1. **Share with caption** — highest value. Someone endorsing your
   content to their own network with added context.
2. **Save** — strong signal of reference value. Under 360Brew, saves
   have become one of the most critical ranking signals. A post with
   200 saves now dramatically outperforms one with 1,000 likes.
3. **Repost** — similar to share but without added commentary.
4. **Long comment (15+ words)** — worth roughly 2.5x a like.
5. **Standard comment (5+ words)** — worth roughly 2x a like.
6. **Reaction** (emoji reactions beyond thumbs up).
7. **Like** — lowest value. Likes carry significantly less weight
   under 360Brew than they did previously.

A single substantive 15+ word comment is worth approximately 2.5
passive likes in algorithmic terms.

---

## Comment Threading Multiplier

Posts that spark 3+ comment exchanges between different participants
(not just the author replying to individuals, but people replying to
each other) receive **5.2x amplification** versus comparable posts
without that discussion depth.

This is why contrarian takes and genuine questions outperform
informational posts — they create debate between readers rather than a
series of isolated reactions.

Under 360Brew, the algorithm also evaluates **comment quality and
lexical diversity**. Comment sections filled with "Great post!" or
"Agree!" are identified as low-entropy noise. If comments share
similar phrasing or originate from a tight cluster of users who always
engage with each other, the model downgrades reach.

---

## Expert Commenter Weighting

Comments from relevant industry experts carry **5–7x more algorithmic
weight** than interactions from random connections.

One comment from a senior decision-maker in your target audience is
worth five or six from people outside the industry. The algorithm
assesses professional background alignment between the commenter and
the post topic.

Under 360Brew, engagement from relevant industry experts carries even
greater weight. An MIT Sloan study of 1,200 B2B profiles found that
the top 30% with highest network relevance (not network size) achieved
210% higher content performance.

---

## Dwell Time: The Primary Ranking Signal

Dwell time (how long someone spends reading a post) is the
algorithm's most important ranking signal because it is nearly
impossible to fake.

- Posts with 61+ seconds of dwell time average a 15.6% engagement rate
- Posts viewed under 3 seconds average just 1.2%

This is why well-structured content with visual breathing room
outperforms short hot takes in the long run. Carousels are
particularly strong, averaging 2–3 minutes of dwell time versus 15–30
seconds for text posts.

Under 360Brew, dwell time has been formally elevated to the #1
ranking factor, ahead of all other engagement signals.

---

## Additional Distribution Factors

- Posts continue distribution for **48–72 hours** under 360Brew (up
  from 2–3 weeks via Suggested Posts in 2024–25). High-performing
  content can circulate for longer, but consecutive posts now
  cannibalise each other more aggressively.
- Posting multiple times within 24 hours causes the newer post to
  receive less reach.
- More than 3 consecutive same-format posts decrease reach by 20%+.
- Minimum gap between posts should be 12 hours.
- The optimal posting frequency is now **3–4 posts per week**, not
  daily. Each new post cuts the distribution lifecycle of the
  previous one.
- Optimal posting times for B2B: Tuesday to Thursday, 9–11 AM in
  your target audience's timezone.
- Content from individual profiles receives 3x higher engagement than
  company page posts. Under 360Brew, this gap has widened further.
- Recycled or duplicate content achieves 84% less reach than original
  content.

---

## Format Engagement Multipliers

Research shows different post formats have measurably different
engagement levels:

| Format | Engagement Multiplier |
|--------|----------------------|
| Polls | 1.64x |
| Carousel/Document | 1.45x (6.6% engagement rate) |
| Multi-image | Highest raw engagement (6.6%) |
| Single image | 1.18x |
| Native video | 1.10x |
| Text-only | Baseline |

Under 360Brew, single-image posts underperform text-only content by
30%, reversing 2024–25 patterns. Videos under 30 seconds achieve 200%
higher completion rates than longer formats. LinkedIn Live videos
receive 7x more reactions than standard video uploads.

---

# Part 2: The 360Brew Shift

*Research basis: LinkedIn 360Brew engineering documentation, Richard
van der Blom Algorithm Insights 2025 (1.8M posts), AuthoredUp (3M+
posts, Q3 2025), Originality.ai (3,368 posts, January 2026),
Brixon Group (500+ B2B profiles), and 20+ additional sources on
360Brew mechanics and AI content detection.*

---

## What Changed

In late 2024, LinkedIn began replacing its entire content ranking
infrastructure — previously a collection of thousands of task-specific
models — with a single unified AI system called 360Brew. This is a
decoder-only transformer with 150 billion parameters, trained
specifically on LinkedIn's networking data.

The old algorithm tracked metadata: clicks, hashtags, connection
graphs, post timestamps. 360Brew reads meaning. It understands that
"AI governance framework" and "EU AI Act compliance strategy" are
related concepts even if those exact terms never appear together. It
interprets whether someone's profile, expertise claims and content
actually align.

The practical consequence: LinkedIn now evaluates **you**, not just
your posts. Your profile, posting history, topic consistency and
engagement patterns are assessed holistically.

---

## AI Content Detection

360Brew does not use a simple binary "AI detector." It evaluates a
combination of signals that, together, make low-effort AI content
easy to identify:

**Lexical diversity.** Human writers naturally vary vocabulary,
sentence structure and rhythm. AI falls into patterns — repeating
similar phrases, using predictable transitions, maintaining an
unnaturally consistent tone.

**Template pattern recognition.** Posts that follow the standard AI
template (Hook → Body → CTA, with single-sentence paragraphs, bullet
points and a rhetorical question close) are structurally identical to
millions of other AI-generated posts. 360Brew's semantic engine
recognises this conformity.

**Profile-content alignment.** The algorithm checks whether posts
match the creator's stated expertise. AI-written content often lacks
the specific, contextual language that comes from real professional
experience in a particular domain.

**Engagement authenticity.** Comment velocity, account relationship
patterns and engagement timing are analysed to identify coordinated
or automated engagement.

### The Penalty

The data on AI content suppression is consistent across sources:

- AI-generated content receives approximately **30% less reach** and
  **55% less engagement** compared to human-written posts (van der
  Blom, 2025).
- Posts with recognisable AI patterns achieve up to **47% less
  organic reach** (Brixon Group, 500+ B2B profiles).
- Overall, median post reach dropped 47% year-over-year after the
  360Brew rollout (AuthoredUp, 3M+ posts, Q3 2025). This partly
  reflects the relevance-first design: fewer impressions, but
  higher-quality impressions.

Posts that could have been written by anyone — or any AI — are
distributed to no one in particular.

---

## Topic Authority

360Brew assigns topic authority based on sustained content within a
defined area. The mechanics:

- Post consistently about 2–3 related topics for **60–90 days** and
  360Brew starts to recognise you as a credible voice in that space.
- Scatter posts across random topics and the algorithm cannot
  determine who should see your content.
- If your profile says "Marketing Director" but you post about
  cryptocurrency, the algorithm sees a mismatch and suppresses
  distribution.
- Content that aligns with the creator's stated expertise receives
  higher confidence scoring and broader distribution.

This is why broad, generic "motivational" content is increasingly
crowded out — it provides no topical signal for the algorithm to
match against relevant audiences.

---

## Profile-Content Alignment

360Brew evaluates your profile before distributing your content. This
is what practitioners call the "profile-content audition":

- **Headline and About section** define your content niche in the
  algorithm's interpretation.
- **Professional experience** is matched against post topics. Domain-
  specific language that could only come from a practitioner carries
  more weight than generic advice.
- **Engagement history** — who you comment on, what you react to —
  tells the algorithm which "table you sit at." Engaging broadly with
  random content prevents the algorithm from placing you in a
  relevant content community.

---

## What 360Brew Penalises

Tactics that were common under the old system now actively harm
visibility:

- **Engagement bait.** "Comment YES if you agree" and similar
  patterns are detected and downgraded. LinkedIn recognises 70+
  engagement bait patterns.
- **Engagement pods.** LinkedIn's AI identifies reciprocal engagement
  patterns with 97% accuracy. Pods now suppress rather than boost
  reach.
- **External links in post body.** Posts with external links
  experience approximately 60% reach reduction. LinkedIn prioritises
  keeping users on platform.
- **Excessive hashtags.** More than 5 hashtags triggers a 68% reach
  reduction. Hashtags have had no measurable positive impact on reach
  since late 2024.
- **Topic scatter.** Posting across unrelated topics prevents 360Brew
  from classifying expertise.
- **Post-and-ghost behaviour.** Publishing AI content and not
  engaging with comments. 360Brew interprets this as low commitment
  and reduces distribution.
- **Post editing after publishing.** Significant edits reset the
  distribution clock.
- **Deletion and reposting.** LinkedIn's algorithm remembers deleted
  content and may penalise the repost.

---

## What 360Brew Rewards

The algorithm is explicitly designed to surface:

- **Genuine expertise.** Content that demonstrates real domain
  knowledge through specific examples, practitioner language and
  concrete results.
- **Topic consistency.** Sustained posting within a defined
  professional niche over 60–90+ days.
- **Save-worthy content.** Frameworks, checklists, original data and
  actionable specifics that people bookmark for later reference.
- **Substantive engagement.** Comments that add context, disagree
  thoughtfully or extend the conversation.
- **Dwell time.** Content dense enough to reward careful reading.
- **Authentic human voice.** Posts that vary in rhythm, include
  genuine uncertainty, and contain the rough edges that AI tends to
  smooth away.

---

## The Standard AI Post Template (What to Avoid)

Every AI post generator uses the same structural formula:

**Hook → Body → CTA**

The hook is constrained to 7–12 words or 210 characters. The body
uses single-sentence paragraphs, bullet points and white space. The
CTA is a rhetorical question or engagement prompt.

This template is now so ubiquitous that it functions as an AI
fingerprint. Over 53% of long-form LinkedIn posts are classified as
"Likely AI" by detection tools (Originality.ai, January 2026), and
the structural conformity is a primary detection signal.

The expanded version adds more layers (re-hook, end-of-body teaser,
second CTA for reposts) but the underlying architecture is identical.
A post that follows this template — regardless of how good the
individual sentences are — signals to both human readers and the
algorithm that it was assembled from a standard AI framework.

---

## AI Slop: The Audience Backlash

The backlash against AI-generated LinkedIn content is now widespread.
Audiences have developed sensitivity to AI-sounding posts, and
content that follows recognisable AI patterns gets scrolled past or
called out in comments.

Common audience complaints:

- Identical structures across unrelated posts
- Hollow enthusiasm: "I'm thrilled to announce..."
- Dramatic openings that deliver mundane conclusions
- Generic "lessons learned" that could apply to any industry
- Rhetorical questions that serve the algorithm, not the reader
- Emoji overload as personality substitutes

The professionals gaining ground under 360Brew are those with clear
expertise, consistent themes and content that reads as if a specific
human being wrote it about a specific subject they know well.

---

*Last updated: March 2026*
