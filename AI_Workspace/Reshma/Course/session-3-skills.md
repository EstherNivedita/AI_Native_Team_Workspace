# Session 3: Teaching AI your taste

## Concepts
Skills and custom instructions. The difference between knowledge (context/RAG) and capability (skills). How you codify expertise into reusable instructions. Why HOW AI does something matters as much as WHAT it knows.

## Teaching flow

### Recap and bridge
"We've built two layers of your workspace — context (what AI always knows) and references (what AI pulls when needed). But knowing your brand guidelines doesn't mean AI can evaluate whether a design follows them. That's like giving someone a recipe book but never teaching them how to cook. Today we're going to teach AI how to THINK like you."

### What is a skill file?
A skill file is a set of instructions that tells AI HOW to perform a specific task — not what to know, but what to do and how to evaluate. Think about how you review a design. You don't just look at it randomly. You have criteria in your head: Is the hierarchy clear? Are the brand colors used correctly? Is the spacing consistent? Is it accessible? You've built this judgment over years. A skill file captures that judgment in a structured way so AI can apply it too.

The difference matters: context is knowledge ("our primary color is #2B6CB0"), a skill is capability ("when reviewing a design, check that the primary color is used for CTAs and headings only, never for body text or backgrounds").

### Connect to their work
Ask: "Walk me through how you review a design — either your own or a teammate's. What do you look at first? What are your non-negotiables? What makes you say 'this isn't ready'?"

Listen carefully. Capture the criteria they mention. Then ask: "Have you ever written these down? Could a new designer joining your team know these rules without sitting next to you for a month?" This is the gap that skill files close.

### Build: Create skills/design-review.md
Based on the review criteria they just described, YOU write a structured skill file. Organize it into clear sections. Push them for specificity before you write — if they say something vague, ask them to sharpen it:

Not "check the colors" → ask "What specifically should I check about the colors? Which colors go where? What's not allowed?"

Not "make sure it looks good" → ask "What makes it look good to YOU? One focal point? Consistent spacing? What's the first thing you'd flag?"

Include sections for: brand compliance, visual hierarchy, typography, spacing and layout, accessibility basics, component usage. Show them the file you created, ask what they'd change or add, iterate based on their feedback, then commit with a descriptive message.

### Build: Create skills/brand-compliance-check.md
Ask them: "What's the difference between a full design review and a quick brand compliance check? When would you use each?" Based on their answer, YOU create a second, more focused skill file — specifically for checking marketing collateral against brand guidelines. This is narrower, faster, and focused on brand consistency across different formats (social posts, banners, pitch decks, ads). Commit with a descriptive message.

This reinforces that different tasks need different skills — just like in an AI product, different user queries trigger different processing logic.

### Reflection
"We just did something most people never do — turned your expertise into a document that someone else (or something else) can follow. Think about your product. When a user asks a question, the product doesn't just retrieve data — it needs to know HOW to interpret and present it. What IPEDS field to use, how to compare institutions fairly, what caveats to include. Those are skills. The data sources are knowledge. The interpretation logic is skill. We just built the same thing for design."

### Quiz
"For each of these, tell me — is it knowledge (belongs in context/ or references/) or capability (belongs in skills/)?
- Your brand's approved font families
- The rule that CTAs must use the primary brand color
- A competitor's landing page screenshot
- The checklist you use before handing off to development
- Your grid system breakpoints
- The principle that every page should have one clear visual focal point
- User interview notes about navigation confusion"
