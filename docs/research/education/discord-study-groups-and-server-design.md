# Discord Study Groups: Server Design and Community Resources

English consolidation and evidence review of two overlapping Spanish source notes:
- [`docs/El estudio grupal en Discord.txt`](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/e1a0b5d0bea8f3b258ecae687bc06696cb2e5f7e/docs/El%20estudio%20grupal%20en%20Discord.txt)
- [`docs/Los canales y servidores.txt`](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/e1a0b5d0bea8f3b258ecae687bc06696cb2e5f7e/docs/Los%20canales%20y%20servidores.txt)

**Status:** practical design guide, not a claim that a server, bot integration or learning outcome has been implemented or evaluated. The source drafts overlap substantially; this note consolidates their full channel, community, bot and moderation themes.

## What the source proposes

The drafts describe co-study and peer accountability; text, voice, video and screen sharing; quiet study, Pomodoro, discussion, project, resource, Q&A, goals and social spaces; subject-based roles; and optional participation modes. They also name Study Together, StudyStream, Spanish-language and subject communities, and propose study timers, time tracking, Forest integration, reaction roles, quizzes and AI assistants.

The source calls Discord study groups a standard or the most popular collaborative-learning tool and presents some communities and bots as large, established or feature-complete. Those superlatives, prevalence claims, catalogues and performance claims are not supported by comparative data in the supplied notes. Treat named products as examples to investigate, not endorsements or a current availability list.

## A small, low-friction server layout

| Category | Suggested channels | Purpose |
| --- | --- | --- |
| Start here | `#welcome`, `#rules`, `#announcements` | Explain purpose, participation norms, moderation/reporting route and how to find channels. |
| Resources | `#notes-and-resources`, `#questions` | Share links and notes; keep help requests searchable and asynchronous. |
| Quiet study | `Silent study` (voice), optional `Focus timer` (text) | Provide a quiet room; use a shared timer only if members want it. |
| Active work | `#subject-discussion`, small-group voice rooms | Support focused Q&A and project sessions without forcing one discipline into every room. |
| Breaks | `#general` or a social voice room | Keep casual conversation separate from focused study. |

Start with a few channels and add more only when members need them. Discord supports category/channel organization and permissions configured at server, category and channel levels. [Discord: Setting Up Permissions](https://support.discord.com/hc/en-us/articles/206029707-Setting-Up-Permissions-FAQ)

Use onboarding questions or roles for optional subject preferences where that helps members find relevant channels. Avoid collecting school, age, location, schedule or other personal details unless the server has a clear need and a defined retention/moderation plan. Onboarding can let members select roles and channels; private channels can be restricted by role. [Discord: Community Onboarding](https://support.discord.com/hc/en-us/articles/11074987197975-Community-Onboarding-FAQ) · [Discord: Role-exclusive channels](https://support.discord.com/hc/en-us/articles/206143877-How-do-I-set-up-a-Role-Exclusive-channel)

## Participation and moderation

- Make camera and screen sharing optional. Offer a camera-off, microphone-muted quiet room; explain what other members can see before anyone joins.
- Do not frame visible attendance, camera use, study-hour rankings or uninterrupted presence as proof of effort or learning. They are optional coordination signals, not validated learning outcomes.
- Keep moderation rules visible. Set expectations for respectful discussion, unsolicited direct messages, links, recording/screenshots, harassment, academic integrity and reporting. Use Discord's built-in Rules Screening and AutoMod where appropriate, then review reports with a human moderator. [Discord: Rules Screening](https://support.discord.com/hc/en-us/articles/1500000466882-Rules-Screening-FAQ) · [Discord: AutoMod FAQ](https://support.discord.com/hc/en-us/articles/4421269296535-AutoMod-FAQ)
- If minors may participate, set age-appropriate rules and moderation, avoid adult-only or private one-to-one study spaces, and follow Discord's current age, safety and privacy requirements. A server layout does not itself make a community safe. [Discord Safety Center](https://discord.com/safety) · [Discord: Teen safety](https://discord.com/safety/safer-place-for-teens)
- Apply least privilege to third-party apps. Review the app owner, requested permissions, data access, privacy policy, retention, moderation controls and removal path before installation. A bot is not required for timers, role selection or quizzes; consider built-in channels or external tools first.

## Timers, bots and other communities

A 25/5 Pomodoro cycle is one possible convention; the drafts also suggest 50/10. Let members choose or use their own timer. Timer and leaderboard data should not be treated as an objective measure of productivity.

The source names StudyLymics, Study Bot, Forest Bot, Carl-bot, Reaction Roles, QuizBot, Flatiron, ChatGPT and Claude bots. Their current Discord availability, ownership, permissions, integrations and specific features were not established by these source notes. In particular, the Forest integration and per-member study-time tracking claims require direct verification before consideration. Do not install an app or grant permissions based on this note.

Study Together's own page describes public and private rooms, camera/screen-share choices, silent study, 25/5 and 50/10 rooms, and time tracking; its Discord server is also listed in Discord's server directory. These are provider descriptions, not independent evidence of learning effects or suitability for every participant. [Study Together: Discord study rooms](https://www.studytogether.com/discord) · [Discord Server Directory: Study Together](https://discord.com/servers/study-together--595999872222756885)

The source also names StudyStream, FreeCodeCamp, Learn AI Together, Biocord and generic Spanish-language study servers. Their precise current server links, activity, moderation and age suitability were not verified here, so they are not presented as vetted recommendations. Check current official pages and community rules before joining or sharing personal information.

## Proposed follow-up: MAD-DISC-001

If the project later pilots a study community, first define its intended age range, learning purpose, moderator coverage, privacy notice, reporting/escalation process and acceptable third-party apps. Then test a minimal layout with voluntary participation and a short feedback form that does not collect sensitive personal data. Evaluate usability and perceived usefulness separately from grades, hours online or camera presence. No bot, attendance collection or public server is part of this documentation proposal.

Related proposal: [Aeronautical academy outreach and community funnel](../../strategy/aeronautical-academy-outreach-and-community-funnel.md) describes a separate, unverified route for inviting interested people into study and volunteer communities.

## Source coverage and provenance

Coverage combines both drafts: motivation/accountability and flexibility claims; quiet, Pomodoro, discussion, project, resource, Q&A, goals and social channels; subject roles and notification access; the named communities and claimed service features; the proposed bot categories, Forest integration, time statistics, quizzes and AI helpers; and camera/mute/privacy recommendations. Repeated content is consolidated. Unsupported popularity, size, always-on availability, effectiveness and bot-feature assertions are explicitly qualified.

Both originals are linked above at source commit `e1a0b5d0bea8f3b258ecae687bc06696cb2e5f7e`; Git blob IDs are `c2d43822a4e2fcf7780bcd7703aed4a4699d54d9` and `7749a658df8c66f79587237bc4848d819a111f3b`. The working TXT copies are removed by this migration; Git history preserves the originals. Official product pages were reviewed on 14 October 2026 for the bounded Discord and Study Together feature checks. No server, bot, account, data collection or learning evaluation was created or performed.
