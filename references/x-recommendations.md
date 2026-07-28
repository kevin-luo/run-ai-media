# X recommendation notes

Last verified: 2026-07-28.

Use current X documentation and `xai-org/x-algorithm` as the source of truth. Re-check both when the account strategy changes or the repository receives a material update.

## Confirmed in current public sources

- For You mixes content from accounts a person follows with recommended content from outside that network.
- Thunder retrieves recent in-network posts. Phoenix Retrieval finds out-of-network posts with a two-tower model and similarity search.
- Phoenix ranks candidates with a Grok-derived transformer trained on engagement sequences.
- The ranker predicts multiple actions, including favorite, reply, repost, quote, click, profile click, video view, photo expand, share, dwell, follow, not interested, block, mute, and report.
- A weighted scorer combines action probabilities. Positive and negative actions can move the score in opposite directions.
- The pipeline removes old, duplicate, previously seen, blocked, muted, and ineligible posts. It attenuates repeated posts from the same author and adjusts out-of-network scores.
- X says the neural network is continuously trained on interactions. Its public policy also says no single signal has a permanently fixed importance.
- Trends favor conversations gaining popularity now.

Official sources:

- [X: For You Home Timeline Recommendations](https://help.x.com/en/resources/recommender-systems/for-you-home-timeline-recommendations)
- [X: Our approach to recommendations](https://help.x.com/en/rules-and-policies/recommendations)
- [xAI: X For You Feed Algorithm](https://github.com/xai-org/x-algorithm)
- [xAI: Phoenix recommendation system](https://github.com/xai-org/x-algorithm/blob/main/phoenix/README.md)

## Do not present these as facts

The current official documentation and repository do not establish:

- a fixed 1,500-candidate pool or a permanent 50/50 in-network split;
- a universal 30- or 60-minute cutoff for distribution;
- an 80-hour recommendation window;
- fixed multipliers such as “one reply equals 27 likes” or “an author reply equals 150 likes”;
- guaranteed Premium or verification boosts;
- a universal penalty for every outbound link;
- special ranking treatment for videos under 2 minutes 20 seconds;
- an ideal posting frequency that applies to every account.

Treat such claims as hypotheses for account-level experiments. Do not repeat the numbers in public copy unless a current primary source supports them.

## Operational implications

These are editorial choices informed by public signals, not guaranteed ranking formulas:

- Give readers something worth pausing on: native video, a screenshot, a concrete result, a useful disagreement, or a practical question.
- Write for a likely human response. Avoid empty questions, manufactured controversy, and “comment 1 if you want it” bait.
- Join rising conversations where the account has first-hand experience. A sharp reply can introduce the account without forcing a separate post.
- Use the first self-reply for a source, repository, or genuinely useful detail. Do not manufacture a reply chain to simulate activity.
- Check a new post during its first hour when practical and answer real comments naturally. Treat this as community work, not a ranking hack.
- Avoid duplicate copy, repeated calls to action, reply bursts, and several near-identical posts.
- Let an original post breathe. Do not bury it immediately under another original.
- Diagnose performance across a batch of comparable posts. One low-view post cannot isolate the cause.

## Account rules for @luosilent

- Publish no more than one normal original post per 24 hours.
- Allow a second original only for an unusually strong time-sensitive topic, at least six hours after the previous original.
- Space ordinary replies by at least 90 minutes.
- Keep the main post self-contained. Put outbound links in the first self-reply when the link is useful.
- Use at most one hashtag, only when it is a natural topic label people are actively using.
- Review original-post results by topic, format, hook, posting time, watch time or dwell proxy, replies, profile visits, and follows.
- Never trade accuracy or voice for a supposed algorithm trick.