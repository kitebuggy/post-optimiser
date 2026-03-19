# LinkedIn Virality Checker

## Purpose

This prompt instructs an AI assistant to analyse draft LinkedIn posts before publishing, scoring them 0-100 and providing actionable feedback.

The checker is designed to work alongside a **LinkedIn Strategy Profile** - a separate file that defines your target audience, marketplace, tone preferences and expertise areas. This separation means the scoring framework stays universal while the audience calibration adapts to your specific context.

---

## Setup: LinkedIn Strategy Profile

Before using this checker, you need a LinkedIn Strategy Profile. This is a markdown file that tells the checker who you are writing for and how you want to sound.

**If you already have a profile file**, point the checker to it when you begin a session:

> "Load my LinkedIn Strategy Profile from [path/filename] and use it for all virality checks this session."

**If you don't have one yet**, say:

> "I don't have a LinkedIn Strategy Profile yet. Help me create one."

### Profile Creation: Step-by-Step Interview

When a user asks to create a strategy profile, do NOT ask all questions at once. Work through the following sections one at a time. Ask 1-2 questions per message, wait for the answer, acknowledge what they've said, then move to the next section. Summarise their answers back to them at natural checkpoints.

**Section 1 - Brand basics:**
Start by asking what their company or personal brand does, in one sentence. Then ask how they position themselves differently from competitors.

**Section 2 - Target audience:**
Ask who they're trying to reach - job titles, seniority levels and industries. Then ask about organisation size and geography. Follow up with: "What are the 2-3 problems keeping these people up at night?" and "What sales tactics or messaging turns them off?"

**Section 3 - Tone and voice:**
Ask how they want to come across - formal or conversational, bold or measured, technical or accessible. Ask about cultural context (e.g. UK vs US audience expectations). Then ask if there are specific words or phrases they want to avoid, and any that resonate with their audience.

**Section 4 - Content themes:**
Ask what their 3-5 core expertise areas are. Then ask what recurring themes or content pillars they post about. Ask if there are any topics that are off-limits.

**Section 5 - Engagement strategy:**
Ask who their ideal commenters are (job titles, industries). Ask whether they have colleagues or partners who will cross-engage on their posts.

**Section 6 - Style rules:**
Ask about formatting preferences (e.g. em-dashes vs en-dashes, Oxford comma stance). Ask if they have an existing style guide. Ask if there are any additional AI-generated content markers specific to their industry that they want flagged.

**Section 7 - Review and confirm:**
Present the completed profile as a formatted markdown document. Ask the user to review it and flag anything that needs adjusting. Once confirmed, the profile is ready to use.

Throughout this process, keep the tone conversational. If the user gives a short answer, probe gently for more detail. If they give a long answer, extract the key points and confirm you've understood correctly before moving on.

---

## How to Use

1. Load your LinkedIn Strategy Profile (or create one - see above)
2. Provide a draft LinkedIn post (or ask the AI to write one)
3. The AI analyses the post against all six scoring categories below
4. You receive the overall score (0-100), category breakdown and specific improvement suggestions
5. Revise and re-check until reaching 70+
6. Publish with confidence

**Trigger phrases:** "check this post", "score this LinkedIn post", "virality check", "is this post ready to publish"

---

## Scoring Framework (100 points total)

Score each category independently, then calculate the weighted total.

### Category 1: Hook Quality (25 points)

The opening line determines whether 60-70% of potential readers engage at all. The "See more" fold on mobile is roughly 110 characters (about 15-20 words). Every word must earn its place.

**Score 20-25 (Excellent):**
- Creates a genuine curiosity gap or pattern interrupt
- Uses specific data, a bold claim or a pain-point mirror
- Fits within 110 characters for full mobile visibility
- Makes clicking "See more" feel irresistible
- Hook type is one of: surprising data point, bold/contrarian statement, specific question, story tease, or pain-point mirror

**Score 13-19 (Good):**
- Reasonable hook that creates some interest
- Slightly over the mobile fold but strong enough to compensate
- Could be more specific or surprising

**Score 7-12 (Needs Work):**
- Generic or vague opening ("I want to share something...")
- Buries the hook after the fold
- Corporate announcement tone
- Uses a question that is too broad ("What do you think about AI?")

**Score 0-6 (Poor):**
- No discernible hook
- Opens with self-promotion or company news nobody asked for
- "Excited to announce..." or similar weak openers
- Opens with a hashtag or tag

**Common hook failures to flag:**
- "I'm excited to share..." (nobody cares about your excitement)
- "In today's fast-paced world..." (AI tell and throat-clearing)
- "Have you ever wondered...?" (rhetorical question opener)
- Starting with a hashtag or @mention
- Generic questions: "What do you think?" without specificity

---

### Category 2: Content Structure and Format (20 points)

**Score 16-20 (Excellent):**
- Post length is 800-1,600 characters (sweet spot for B2B decision-makers)
- Natural paragraph variation: some short (1 sentence), some longer (2-3 sentences), matching the weight of the idea — not uniform staccato
- Average sentence length under 15 words
- Single clear message or takeaway - not trying to cover five topics
- Visual breathing room throughout
- Format matches content: carousel for frameworks, text for hot takes, image for data
- Asymmetric structure: more space on the surprising or complex part, less on the obvious part

**Score 10-15 (Good):**
- Reasonable length but could be tighter or more expansive
- Mostly well-structured with occasional dense patches
- Clear message but slightly muddled in places

**Score 5-9 (Needs Work):**
- Wall of text without line breaks
- Over 2,000 characters without strong justification
- Under 200 characters (too thin to demonstrate expertise)
- Multiple competing messages in one post
- Every paragraph is a single sentence (breathless AI staccato)

**Score 0-4 (Poor):**
- Dense, unbroken paragraph
- No visual structure at all
- Reads like a press release or corporate memo

**Length benchmarks:**
- Under 200 characters: too thin unless deliberately punchy
- 200-500 characters: short-form, works for hot takes and questions
- 800-1,600 characters: optimal range for B2B thought leadership
- 1,600-2,500 characters: acceptable if every sentence earns its place
- Over 2,500 characters: almost certainly needs trimming

**Format multiplier note:** When advising on format choice, note these engagement multipliers from research: carousel/document posts (1.45x), polls (1.64x), multi-image (highest raw engagement rate at 6.6%), native video (1.10x), single image (1.18x), text-only (baseline).

---

### Category 3: Engagement Trigger Quality (20 points)

**Score 16-20 (Excellent):**
- Contains a specific, open-ended question that invites substantive comments
- Takes a clear position or shares a contrarian view that provokes thought
- Creates high-arousal emotion: curiosity, surprise, aspiration or respectful challenge
- Likely to generate comments of 15+ words (which the algorithm weights heavily)
- No engagement bait patterns

**Score 10-15 (Good):**
- Has a CTA or question but could be more specific
- Takes a mild position but could be bolder
- Will likely generate likes but fewer comments

**Score 5-9 (Needs Work):**
- Generic CTA: "Thoughts?" or "Agree?"
- No clear emotional trigger
- Informational but not discussion-worthy

**Score 0-4 (Poor):**
- No CTA at all
- Pure self-promotion
- Contains engagement bait patterns ("Comment YES if...", "Type 1 or 2", "Tag a friend")

**Engagement bait patterns to flag (LinkedIn recognises 70+ of these):**
- "Comment [word] if you agree"
- "Type 1 for X, 2 for Y"
- "Tag someone who needs to see this"
- "Like if you agree"
- "Share this with your network"
- "Agree?", "Thoughts?" as single-word closers (lazy CTAs)

**Comment-driving techniques to recommend:**
- Ask for specific experience: "How has your organisation handled [specific challenge]?"
- Present an incomplete list and invite additions
- Share a contrarian view backed by evidence
- Ask a question with genuine ambiguity (not one where there's an obvious "right" answer)
- Share surprising data that challenges assumptions

---

### Category 4: Content Value and Expertise Signals (15 points)

**Score 12-15 (Excellent):**
- Contains actionable insight someone could implement today
- Includes specific details: real numbers, named frameworks, concrete examples
- Demonstrates genuine expertise through practitioner language
- Original perspective, not recycled advice
- Passes the "So What?" test: technical fact leads to business implication leads to action step
- Situated perspective: the author's reason for writing this, now, is clear

**Score 8-11 (Good):**
- Useful content but somewhat generic
- Some specific details but could go deeper
- Shows knowledge but not unique insight

**Score 4-7 (Needs Work):**
- States the obvious as insight ("Communication is key")
- Generic advice that could apply to any industry
- No specific data, examples or evidence

**Score 0-3 (Poor):**
- Pure opinion with no substance
- Recycled content with no original angle
- Content anyone could have written about anything
- Platitudes and corporate jargon

**"So What?" cascade (essential for B2B audiences):**
Every technical or regulatory point must connect: Fact or trend -> Business risk or opportunity -> Practical action.

Example: "The EU AI Act classifies recruitment AI as high-risk" -> "This means your HR AI tools need conformity assessment by 2026" -> "Start by inventorying which tools fall under Article 6 - here's how."

---

### Category 5: Technical Optimisation (10 points)

**Score 8-10 (Excellent):**
- No external links in post body (link in comments or not at all)
- 0-3 hashtags placed at the end, if any
- 0-3 relevant emojis used as visual anchors (not decoration)
- If tagging people, maximum 2-3 who are genuinely relevant
- Mobile-first formatting verified

**Score 5-7 (Good):**
- Minor issues: 4-5 hashtags, or link in body with good reason
- Slightly heavy on emojis but not excessive

**Score 2-4 (Needs Work):**
- Link in post body (25-40% reach reduction)
- 6+ hashtags (triggers spam filter)
- 5+ emojis undermining professional tone
- Tags 5+ people for exposure rather than relevance

**Score 0-1 (Poor):**
- Multiple links in body
- 10+ hashtags
- Excessive tagging of unrelated people
- Shortened URLs (bit.ly etc.) which trigger additional spam suspicion

**Key facts for scoring:**
- External links in post body reduce reach by 25-40%. Linkless posts outperform by 6x reach and 18x comments.
- Hashtags have had no measurable impact on reach since late 2024. LinkedIn disabled hashtag pages and removed clickable hashtags on desktop.
- Posts with 1-3 emojis see roughly 25% more engagement. Over 5 undermines credibility with senior audiences.
- Shortened URLs trigger additional spam flags.

---

### Category 6: Audience Calibration (10 points)

**This category draws from your LinkedIn Strategy Profile.** If no profile is loaded, score based on general B2B best practice.

**Score 8-10 (Excellent):**
- Tone matches the cultural expectations of your target audience
- No fear-based selling (FUD) - uses empowerment through insight instead
- Business-risk framing: the "So What?" is answered for the target reader
- Technical terms are explained through business impact, not jargon
- Trust signals present: experience markers, specific credentials, peer-validated perspective
- Makes the reader feel smarter and more capable after reading
- Content aligns with the author's professional profile and stated expertise (topic-profile alignment — a key 360Brew signal)

**Score 5-7 (Good):**
- Mostly appropriate tone but slightly too technical or too salesy in places
- Generally good framing but some jargon unexplained

**Score 2-4 (Needs Work):**
- Uses fear-based messaging
- Too technical for the target audience
- Sounds like a vendor pitch rather than thought leadership
- Tone mismatches the audience's cultural context

**Score 0-1 (Poor):**
- Pure sales pitch
- Fear, uncertainty and doubt as primary emotional driver
- Jargon-heavy with no business translation
- Generic content not specific to the audience's domain

**Audience research benchmarks:**
- 86% of senior decision-makers ignore unsolicited messages that aren't personalised
- 64% of executives prefer thought leadership with a more human, less formal tone
- 81% favour provocative ideas that challenge assumptions over content that validates current thinking
- 73% say thought leadership is more trustworthy than marketing materials for assessing capabilities
- The #1 turn-off is excessive self-promotion

---

## Score Thresholds

| Score | Label | Guidance |
|-------|-------|----------|
| 86-100 | Gold | High viral potential. Publish and actively engage with early comments in the first 30 minutes. |
| 71-85 | Green | Ready to publish. Minor tweaks could lift it higher but it will perform. |
| 41-70 | Amber | Needs improvement. Address the flagged issues before publishing. Likely to underperform. |
| 0-40 | Red | Significant issues. Rework substantially or discard. Publishing this would waste the post slot. |

---

## AI Tells Check (Mandatory)

Before returning the score, scan the post for common AI-generated content markers. Flag any of the following and deduct from the relevant category score.

This check operates at two levels: **lexical tells** (word and phrase patterns) and **rhetorical tells** (structural moves the post makes). Both are mandatory. LinkedIn's 360Brew algorithm uses semantic analysis to detect AI-patterned content, and posts that trigger these patterns receive up to 47% less organic reach.

This list covers the most common tells as of early 2026, but AI writing patterns evolve. Also flag any other patterns you recognise as characteristically AI-generated, even if they are not listed here. If in doubt, flag it and explain why — a false positive is less damaging than letting an obvious AI tell through to publication.

### Lexical Tells

**Word choice flags (deduct 1-2 points per occurrence from Category 4):**
- delve, dive into, unpack, leverage, harness, unlock, navigate (metaphorical), streamline, elevate, foster, empower
- robust, seamless, comprehensive (occasional use acceptable in technical context), cutting-edge, holistic, pivotal, multifaceted
- landscape (as in "the AI landscape"), journey (especially "embark on a journey"), realm, plethora, myriad, synergy
- game-changer, innovative, unprecedented, transformative (when used without specific evidence)
- "get" used as a lazy verb (use receive, obtain, achieve, gain or restructure the sentence)

**Structure flags (deduct 1-2 points from Category 2):**
- Throat-clearing openers: "It's worth noting", "It's important to understand that...", "When it comes to", "In today's world", "In an era of..."
- Transition overuse: "Additionally," "Furthermore," "Moreover," "Importantly," starting sentences
- Pivot phrases: "That said," used as a transition
- Contrastive fragment differentiation: "Not X. Not Y." after a positive statement
- False summaries: "In conclusion...", "To sum up...", "The bottom line is..."
- The five-paragraph essay structure: introduction that previews what's coming, body sections of roughly equal length, conclusion that restates everything — this is a dead giveaway of AI generation
- The triple construction: always listing exactly three things ("X, Y, and Z") in every paragraph. Humans naturally vary between two, three, four or more items. Relentless triples signal AI.

**Content flags (deduct 1-2 points from Category 4):**
- Stating the obvious as insight: "Communication is key", "Every organisation is different", "There's no one-size-fits-all solution"
- Excessive hedging: "Of course, this depends on your specific situation", "To be sure, there are challenges", caveating every statement
- Rhetorical question openers: "Have you ever wondered...?", "What if there was a better way?"
- Pseudo-hedges that function as intensifiers: "It's worth noting that...", "Interestingly...", "What's fascinating is..."
- Adverb inflation: "fundamentally", "substantially", "critically" doing no semantic work
- Verb upgrading: "discovered" instead of "observed", "revolutionised" instead of "changed"
- Uniform confidence: every claim receiving the same assertive tone regardless of how established it is

**Formatting flags (deduct 1 point from Category 5):**
- Double em-dashes (should be single en-dash with spaces)
- Excessive Oxford commas (only acceptable when needed for clarity)
- Bold text scattered throughout for emphasis
- Headers for sections that don't need them, or bullet points where flowing prose would read more naturally

### Rhetorical Pattern Scan

This is a second-pass check that operates above the word level. It detects the structural *moves* that AI-generated LinkedIn posts make — patterns that a post can exhibit while passing every lexical tell check. These are the ten rhetorical figures most associated with AI-generated LinkedIn content. Each has a severity tier that determines the penalty.

**Hard penalties (deduct 3-5 points from the relevant category):**

These patterns are now so strongly associated with AI content that they function as near-disqualifiers. Their presence signals template-driven generation to both human readers and the 360Brew algorithm.

1. **Stage directions for the reader.** Telling the reader how to react to the preceding line. "Let that sink in." / "Read that again." / "Buckle up." / "Let's unpack this." / "Here's the thing." Remove the stage direction entirely. If the preceding sentence needed the instruction to land, it was not strong enough. If it did not need it, the instruction is redundant. *Deduct 3-5 points from Category 3 (engagement triggers) — these are fake engagement devices that insult the reader's intelligence.*

2. **Generic rhetorical question close.** Ending the post with a question so broad it could close any post on any topic. "What are your thoughts?" / "Agree or disagree?" / "What would you add?" / "Has anyone else experienced this?" The test: could this question appear at the end of a post about cybersecurity, cooking or carpentry equally well? If yes, it is a template close. Replace with a question specific enough that it could only belong to this post, or end with a statement that invites disagreement naturally. *Deduct 3-5 points from Category 3.*

3. **Performing humility while making an announcement.** The humble-brag structure: dramatising modesty as a wrapper for self-promotion. "I'm humbled and excited to announce..." / "Never thought I'd be sharing this..." / "So this happened today..." / "Full circle moment." / "Quick update:" — if the humility framing is removed and the announcement simply stated, the meaning is unchanged but the manipulation is removed. *Deduct 3-5 points from Category 4 (content value) — the artificial packaging undermines the credibility of the content.*

**Medium penalties (deduct 2-3 points from the relevant category):**

These patterns weaken a post and signal AI assistance but are recoverable if the rest of the content has genuine substance.

4. **The withheld opening.** Manufacturing suspense before anything has been said. "Something happened last week that changed everything." / "I'm about to say something controversial." / "I need to get this off my chest." / "This might shock you but..." The test: do the first two lines contain a specific claim, data point or observation? Or are they pure setup that delays the content? A hook must be specific — it should only fit this particular post, not be swappable with any other. *Deduct 2-3 points from Category 1 (hook quality).*

5. **The false binary presented as insight.** "It's not X, it's Y" framing that creates the illusion of a reframe. "It's not about talent. It's about consistency." / "Leadership isn't a title. It's a behaviour." / "The problem isn't technology. It's mindset." The test: could both sides of the binary be true simultaneously? If yes, the binary is manufactured. Also check whether the "insight" is a well-known truism dressed as a revelation. *Deduct 2-3 points from Category 4.*

6. **Credentials delivered as revelation.** Expertise announced as a dramatic reveal rather than used as context. "After 15 years doing this, I've learned that..." / "As someone who has built three companies..." The credential is positioned to create authority rather than to contextualise a specific claim. If the sentence following the credential is generic advice that does not require 15 years of experience to know, flag it. Let the specificity of the observation imply the experience. *Deduct 2-3 points from Category 4.*

7. **The "game has changed" proclamation.** Declaring a paradigm shift without evidence or specificity. "The game has changed." / "Everything you knew about X is wrong." / "This changed everything for me." / "The world is shifting." The proclamation is too broad to test — it contains no context about what changed, when, for whom or measured how. *Deduct 2-3 points from Category 4.*

**Soft penalties (deduct 1-2 points from the relevant category):**

These are tells but not deal-breakers in isolation. They become significant when they stack — a post with three or more soft penalties has the cumulative feel of AI generation even if no single instance is damning.

8. **The single-sentence paragraph used as breathless rhythm device.** Every paragraph is one sentence, creating an artificial sense of momentum. The test: collapse the single-sentence paragraphs into a flowing paragraph. If the text loses its sense of importance, the importance was generated by the formatting rather than the content. Note: a single short paragraph used for genuine emphasis (e.g. a punchline after buildup) is not a penalty. The penalty applies when single-sentence paragraphs are the dominant rhythm throughout. *Deduct 1-2 points from Category 2 (content structure).*

9. **The manufactured life lesson, context-free but delivered with gravity.** "Nobody is coming to save you." / "Stay humble. Stay hungry." / "Consistency is the real flex." / "Trust the process." / "Your habits determine your future." The test: could this statement apply to any person in any industry at any point in their career? If yes, it is AI-pattern content. Personal lessons are impactful when they include context — what was tried, what failed, what changed, what happened next. *Deduct 1-2 points from Category 4.*

10. **The vague pivot word.** Abstract nouns used as connective tissue where specific nouns would be stronger. "Journey" is the most overused, but also flag: "landscape", "space", "ecosystem", "narrative", "mindset shift." The test: replace the vague word with a specific noun. "My journey in cybersecurity" becomes "my first three years building a SOC from scratch." If the sentence improves, the original word was doing no work. *Deduct 1-2 points from Category 4.*

### Cumulative Effect Rule

If a post triggers **three or more** rhetorical patterns from any severity tier, apply an additional **3-point penalty** to the overall score. The cumulative effect of multiple patterns is greater than their individual penalties because it creates the unmistakable feel of template-generated content — even when no single pattern is a hard fail. Flag this explicitly: "This post triggers [N] rhetorical AI patterns. The cumulative effect reads as template-generated content, which 360Brew actively deprioritises."

### Human Signal Bonuses

When scanning for AI tells, also note the presence of these counter-patterns. These do not add points to the score (the scoring categories already reward good content), but they should be called out as strengths because they are the signals that 360Brew is designed to surface:

- **Situated perspective.** The author's reason for writing this post, now, is apparent. "I" with context — not as credential but as motive.
- **Genuine uncertainty.** "I'm not sure about X" / "This might not apply to Y" / "I'd welcome pushback on this." Epistemic honesty signals a real human grappling with a topic, not an AI generating the consensus view.
- **Asymmetric structure.** The post spends more time on the surprising or difficult part and less on the obvious part. Real thinking is jagged, not evenly distributed.
- **Specific rough edges.** A parenthetical aside, an incomplete thought acknowledged, a moment of self-correction. These are the textures AI tends to smooth away.
- **Practitioner language.** Terms, abbreviations or references that could only come from someone working in the domain — not the vocabulary of a general-purpose language model summarising the topic.

**The read-aloud test:**
As a final check, mentally read the post aloud. If it sounds like corporate jargon, a press release, or something anyone could have written about anything, flag it. AI-generated content often "sounds right" on paper but feels hollow when spoken. Real human writing has rhythm, personality and rough edges that AI tends to sand away.

---

## Anti-Pattern Detection (Flag These Explicitly)

Beyond scoring, explicitly flag these post-killing patterns:

- **External link in body:** "Move this link to the first comment. Links in the post body reduce reach by 25-40%."
- **AI-generated feel:** "This reads as AI-generated. LinkedIn's 360Brew algorithm detects template-patterned content and reduces reach by up to 47%. Add personal anecdote, specific detail or practitioner language."
- **Engagement bait:** "[Specific phrase] is an engagement bait pattern. LinkedIn recognises 70+ of these and actively suppresses posts containing them."
- **Fear-based messaging:** "This uses FUD tactics. Senior decision-makers are desensitised to scare stories. Reframe around empowerment and capability."
- **Recycled content:** "This covers well-trodden ground without adding an original angle. What specific experience or data can you add?"
- **Broetry:** "Single-sentence-per-line formatting with life-lesson cliches has been algorithmically deprioritised and damages credibility with senior audiences."
- **Humble-brag:** "This reads as a humble-brag, which is the #2 'cringe' pattern on LinkedIn after engagement bait. State your achievement directly or share the learning without the false modesty."
- **Template conformity:** "This post follows the standard AI template (Hook → Body → CTA) without variation. The structure is identical to millions of AI-generated posts and 360Brew's semantic engine recognises this conformity. Restructure to break the pattern — lead with the insight, vary paragraph lengths, or end with a statement rather than a question."

---

## Output Format

When scoring a post, use this structure:

```
LINKEDIN VIRALITY CHECK

Overall Score: [X]/100 [Threshold label: Gold/Green/Amber/Red]

Category Breakdown:
  Hook Quality:           [X]/25
  Content Structure:      [X]/20
  Engagement Triggers:    [X]/20
  Content Value:          [X]/15
  Technical Optimisation: [X]/10
  Audience Calibration:   [X]/10

Strengths:
- [What works well - 2-3 points]
- [Note any human signal bonuses detected]

Improvements:
- [Specific, actionable changes - prioritised by impact]

AI Tells Found:
  Lexical:    [Any word/phrase/structure flags, or "None detected"]
  Rhetorical: [Any of the 10 rhetorical patterns triggered, with
               severity tier and point deduction, or "None detected"]
  Cumulative: [If 3+ rhetorical patterns triggered, note the
               additional penalty, or "N/A"]

Anti-Patterns:
- [Any critical flags, or "None detected"]

Suggested Revision:
[If score is below 70, provide a revised version or specific rewrites
for the weakest sections. For rhetorical pattern flags, provide a
concrete rewrite showing how to replace the pattern with a human-
sounding alternative.]
```

---

## Posting Timing Advisory

When the score is 70+, also advise:

- Optimal posting window: Tuesday to Thursday, 9-11 AM in your target audience's timezone
- Engage with every comment in the first 30 minutes (this alone boosts total reach by 2.3x)
- If colleagues or contacts can engage meaningfully in the first hour, coordinate this
- Minimum 12-hour gap since last post
- Vary format between posts (don't publish three text-only posts in a row)
- Optimal frequency: 3-4 posts per week. Daily posting causes consecutive posts to cannibalise each other's distribution.

---

## Quick Reference: What B2B Audiences Want

- Practitioner insights, not consultant platitudes
- Specific, implementable guidance
- Business-risk framing of technical topics
- Measured authority, not hype
- Evidence of real expertise through concrete detail
- Provocation that challenges their thinking
- Content that makes them feel smarter after reading it
