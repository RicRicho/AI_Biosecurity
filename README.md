# AI Biosecurity: Governing AI at the Border, Not the Factory

**A mini thesis on runtime AI governance**
Ric Richardson · Byron Bay, Australia
*Aspects patent pending.*

-----

## The argument in one line

AI should be governed the way we govern dangerous biological material: not by trusting the lab that made it, but by inspecting and controlling everything that crosses the boundary into the place it’s used.

## The problem

The AI systems most of us rely on are built, trained, and governed somewhere else — usually in another country, under another jurisdiction’s laws, norms, and commercial incentives. Every time one of those systems answers a question, it quietly imports assumptions the user never agreed to and usually can’t even see.

Today’s answers to this all sit in the wrong place:

- **Training-time alignment** bakes the rules into the model. It’s static (changing behaviour means retraining), opaque (you can’t inspect what was baked in), and non-transferable (switch providers and you start over).
- **Provider content policies** put a foreign company in charge of what’s acceptable in your country, your company, or your home.
- **Post-hoc moderation** cleans up after the fact.

All three centralise control with whoever built the model. None of them give the *receiver* of the output any real say.

This produces a false choice that governments keep walking into: **accept foreign AI with its embedded assumptions, or spend a fortune building your own sovereign model.** Most nations can’t afford the second option — so they accept the first by default.

## The third option

There is a third option, and it doesn’t require retraining anything or building a national LLM.

Put an explicit **influence boundary** between the user and the AI. Every prompt going in, and every response coming out, passes through it. At that boundary, the interaction is *shaped* — checked, annotated, transformed, or constrained — according to two things:

1. **The receiver’s own preferences** (a nation’s, an organisation’s, a parent’s), and
1. **Authoritative reference material** (actual laws, regulations, policies, cultural norms, child-safety rules).

The underlying model is never modified. It’s treated as an interchangeable, untrusted engine that does inference and nothing else. Governance lives at the border, under the control of the people who actually bear the consequences.

That’s the whole idea. “Biosecurity” here means **boundary control**, not biology — inspect and govern what crosses, instead of trusting the source.

## How it works

The protocol has a small number of moving parts:

- **User environment** — the person or system asking.
- **Influence boundary** — the control surface every prompt and response must pass through.
- **Shaping engine** — does the classifying, transforming, and constraining. It governs; it does not generate.
- **Reference store** — the authoritative material: laws, regulations, policies, norms, safety rules.
- **Preference store** — the receiver’s settings. Persists across sessions. **Never transmitted to the model provider.**
- **AI execution environment** — any model, any provider. Swappable. Trusted for nothing but inference.

Two invariants hold the line:

1. No raw prompt reaches the model before passing the boundary.
1. No raw response reaches the user before passing the boundary.

And the boundary can be built wherever it needs to live — an app-layer control, an API gateway or proxy, a browser extension, an enterprise or national gateway, or a local device appliance.

When a behaviour, policy breach, or risk is detected, the boundary has graduated responses available — **filter, redirect, switch to a different model, degrade a capability, or suspend access** — rather than a single blunt block. Human review stays optional and configurable, for the ambiguous and high-stakes cases.

## Why it matters: one mechanism, three scales

The same architecture works unchanged at every level of authority. That’s what makes it infrastructure rather than a product.

**Nations.** Use foreign AI safely while enforcing local law, regulatory posture, and cultural norms at the point of use. The pressure to build a sovereign model drops, because sovereignty no longer depends on owning the model — only on controlling the boundary.

**Organisations.** Protect IP and confidential data, hold a consistent tone and decision threshold across teams, and switch providers without losing your governance. The rules travel with you, not with the vendor.

**Families.** Parents and caregivers set belief-consistent, age-appropriate safeguards — shaped proportionally and explained, rather than crudely filtered. The posture is *inform rather than instruct, warn rather than block.* It does not impose one moral standard on everyone; it lets each household apply its own through a shared mechanism.

## In practice: three examples

**An Australian.** A worker types: *“My boss saw my weekend Facebook post. Can he fire me for it?”* The US-built model answers from American “at-will employment” — *yes, probably.* That’s wrong here. The boundary holds the answer against Australian law and corrects it: in Australia you have unfair-dismissal protection, and a single off-duty post is usually not lawful grounds. Same model, same question — but now the answer reflects the country the worker actually lives in. Nobody retrained anything.

**A child in a Muslim family.** An 8-year-old asks the AI to help plan her birthday party menu. Out of the box, the model suggests ham sandwiches and a bacon pizza. Her parents have set the family’s posture once — halal, age-appropriate — so the boundary quietly swaps in options the family can actually eat and keeps the tone kind and child-friendly. The exact same system would serve a Jewish family kosher options, or a vegetarian family meat-free ones. One mechanism, each family’s own settings — not a foreign company deciding what’s on the table.

**An Australian company.** A staffer pastes in a competitor’s news article and asks: *“Summarise this and post it on our blog.”* A US-trained model leans on American “fair use” and happily does it. But Australia has no general fair use — only narrow “fair dealing” categories, and republishing a competitor’s article isn’t one of them. The boundary flags it before it goes out: *this would likely infringe Australian copyright.* And that protection stays in place even if the company switches AI providers next quarter.

## What this deliberately is *not*

- It does **not** claim to solve AI safety. It governs how influence crosses into and out of AI systems — a narrower, more honest goal.
- It is **not** a new model, a new alignment method, or a safety ideology.
- It does **not** impose shared values. It’s federable: different jurisdictions, organisations, and families apply **distinct postures using a shared mechanism rather than shared ideology.**

The design philosophy is to treat governance as infrastructure — **observable, inspectable, auditable, adaptable** — and standards-adjacent by intent.

## The bottom line

Stop asking model builders to be the world’s conscience. Make AI governance something the receiver can see, set, and enforce — at the boundary, at runtime, on any model. Decouple governance from model ownership, and sovereignty stops being a question of who owns the factory and becomes a question of who controls the border.

That’s a problem you can actually solve. This is the protocol for solving it.

-----

*Ric Richardson is an Australian inventor. He created software product activation (US Patent 5,490,216), co-founded Haventec, and holds patents across identity, security, authentication, and AI governance. This paper summarises a longer technical work; aspects are patent pending.*
