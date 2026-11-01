# Remco de Graaf

Managing Director and co-owner of [Reshift Digital](https://www.reshift.nl/), the largest tech-focused media company in the Netherlands. Founder of [Zoom.nl](https://zoom.nl) and [SkyStatus](https://skystatus.pro).

I am not a programmer. I trained as a journalist and spent 25 years building media businesses. Since 2025 I have been building production software with AI agents as the engineering team: SkyStatus first, then the 2026 rebuild of Zoom.nl. At Reshift we are now bringing the same way of building to every brand. I do this as a managing director, not just because I enjoy it. The rules of search, content and media are being rewritten, and I want my view of them to come from experience.

**The agent thinks, the system enforces.** An agent is a strong engineer that forgets, guesses and agrees too easily. So the rules are code in the path of the work, not documents beside it. The full method: [remcodegraaf.com/method](https://remcodegraaf.com/method).

## How I build

- **Guards in the path.** Hooks refuse a commit that holds a secret, a push to production that carries someone else's commit, a destructive database statement. Every guard fails closed and says why. The agent never routes around a guard. When one stops it, the agent stops and explains why. Where an override exists, it is explicit and it is a person's call, never the agent's. A wrong guard gets changed in the open, with a test.
- **Two labs.** Claude Code and OpenAI Codex come from different labs. In most of my projects Claude Code builds and Codex reviews, as an independent second lab. In SkyStatus they are peers: both build, with equal authority. Every finding is a hypothesis until it is checked against file and line. In one round Codex cited the right line eight times out of eight, and two of its three proposed fixes would have added a bug. So the fix gets checked on its own.
- **Red first.** A guard only counts once you have seen it block the thing it is meant to block. Every fix starts with a failing test.
- **Count with tools.** Three model passes planned the same change and missed the same five display components. A grep found them in ten seconds.
- **Measure before you reason.** A finding on two cases is a hypothesis. Observation first, cause second, and the cause stays labelled as a guess until it is proven.
- **Simplify on evidence.** SkyStatus grew to 96 scheduled jobs, with layers that healed failures and audited the fleet. In October 2026 a complexity audit switched 35 of them off, the self-healing lanes included. The alert channel went from about 45 unread messages a day to pages that need a person.
- **Live means proven live.** A merge starts a deploy. It is live when production serves that exact commit.

## What runs on it

| Project | What it is | Stack |
|---|---|---|
| [SkyStatus](https://skystatus.pro) | Flying Blue analytics: XP and status tracking, statement import, a mileage run simulator, guides in English, Dutch, French and German. The lab where the method was developed. 81 registered gates and 20,000+ tests. | React, TypeScript, Supabase, Vercel |
| [Zoom.nl](https://zoom.nl) | The largest photo community in the Netherlands, 2.5M+ photos and 145,000+ members. Rebuilt in 2026 from a legacy monorepo into an ad-free platform built to be found by search engines and LLMs. Live since 22 September 2026. Builders on the team ship through pull requests, under the same guards as I do. | Next.js 16, React 19, Tailwind v4, Supabase, DatoCMS |
| [ID.nl](https://id.nl) | Reshift's tech and lifestyle brand. I wrote the plan and led the launch in 2022. Now on the same SEO and structured data foundation as Zoom.nl. | Next.js, DatoCMS |
| [Reshift Digital](https://www.reshift.nl/) | The publisher: Kieskeurig.nl, ID.nl, Review.nl, Zoom.nl, Zoom Academy, Computer Idee and Computer!Totaal. Every brand and every workflow is moving to this way of building. | |

Almost all of it lives in private repositories. The contribution graph is the public trace: 14,000+ commits and 800+ pull requests in the past year.

## What it does not solve

Agents still produce shallow visual design without a tight feedback loop, so design stays close to a person with eyes on the result. Long sessions drift, so work is cut into pieces with clear hand-overs. And a second lab adds noise as well as insight, which is why every finding stays a hypothesis.

## Writing

- [The agent thinks, the system enforces](https://remcodegraaf.com/method) (October 2026). The method in seven parts.
- [Bouwen met AI zonder programmeren: code was het kleinste deel](https://www.frankwatching.com/archive/2026/04/12/bouwen-met-ai-zonder-programmeren-code/) (Frankwatching, April 2026, in Dutch). How a domain expert ships production software with AI, and why the code turned out to be the smallest part.

## Background

- **2026 to now.** [Managing Director and co-owner](https://www.reshift.nl/en/about-reshift/management/), Reshift Digital, with Kevin van Oosteren. Innovation, AI, content and community.
- **2025 to now.** Founder, SkyStatus.
- **2015 to 2026.** Director of Content, Reshift Digital. Launched ID.nl, Zoom Academy and Tech Academy.
- **2010 to 2014.** Shareholder in Focus Media Groep, publisher and editor-in-chief of Focus magazine. Editor-in-chief of Discovery Magazine NL from 2012.
- **1999 to 2010.** Editorial management, IDG Netherlands (Computer!Totaal, Tips & Trucs, iPhone Magazine), editor-in-chief in the last years. Wrote the plan for Zoom Magazine in 2003. Zoom.nl went online at the end of 2004.
- **Founder** of Zoom Academy (77,000+ students) and Tech Academy (40,000+ students).

## Elsewhere

[remcodegraaf.com](https://remcodegraaf.com) · [LinkedIn](https://www.linkedin.com/in/remcodegraaf/) · [Frankwatching](https://www.frankwatching.com/archive/author/remco-de-graaf/)

Always happy to compare notes on guards, review loops and agentic engineering inside a company that was never a software company.
