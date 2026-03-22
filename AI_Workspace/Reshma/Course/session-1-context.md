# Session 1: What does AI actually see?

## Concepts
Context window. Persistent context. Why what you give AI determines what AI gives you back.

## Teaching flow

### Start with what they know
Ask: "When you use AI to help with a design task — writing copy, generating ideas, reviewing something — what do you usually type?" Listen. They'll likely describe giving a one-off instruction with no background. Use this as the opening: "Every time you do that, AI starts from zero. It knows nothing about your brand, your design system, your product, or your standards. You're asking an expert for help but not telling them who you are."

### What is a context window?
The context window is everything AI can "see" in a single conversation — your prompt, any files you share, and the conversation history. It's like a desk. Whatever's on the desk, AI can work with. Whatever isn't on the desk doesn't exist to AI. The size of the desk is limited, so what you choose to put on it matters.

### What is persistent context?
Some information is relevant to EVERY design task you do — your brand guidelines, your color palette, your typography rules, your component library. This is persistent context: the information that should always be on the desk. Right now, this knowledge lives in your head or in scattered files. If you could give AI this information once and have it always available, every AI interaction starts from a much better place.

### Connect to their work
Ask: "What information do you carry in your head into every single design task? The stuff so automatic you don't even think about it?" Help them list it: brand colors, fonts, spacing rules, logo usage guidelines, tone, audience. That's their persistent context.

### Build: Create the first context file
Ask them to describe their brand guidelines — colors, fonts, logo rules, tone, anything consistent across every design. If they have an existing document, ask them to share or describe it. Based on what they tell you, YOU create `context/brand-guidelines.md` in their workspace folder. Show them the file, ask if anything is missing or needs changing, then commit with a descriptive message.

### Reflection
"I just created persistent context for your AI workspace. From now on, any AI tool you use for design can start by reading this file — and it immediately knows your brand. Think about your product — when a user asks a question, what's the equivalent of brand guidelines? What does the product always need to know, regardless of the question?"

### Quiz
"I'm going to name some things. Tell me — would this be persistent context (always on the desk) or not?
- Your brand color palette
- A brief for a one-time pitch deck
- Your typography scale
- Competitor screenshots for a landing page redesign
- Your component library naming conventions"
