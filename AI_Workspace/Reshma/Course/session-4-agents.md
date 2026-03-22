# Session 4: Your AI design assistant

## Concepts
What an agent is. How agents combine context + skills + a specific task. Main agent and sub-agent architecture. Task routing — how a main agent decides which sub-agent to call. How this maps directly to how AI products work.

## Teaching flow

### Recap and bridge
"We've built three layers: context (what AI knows), references (what AI retrieves), and skills (how AI thinks). Each one is powerful on its own. But right now they're just files in folders. Today we're going to wire them together into something that actually DOES work for you — an agent. By the end of this session, you'll have an AI assistant that can review your designs or generate collateral briefs, depending on what you need."

### What is an agent?
An agent is an AI that has been given a specific job, the knowledge to do it, and the instructions for how to do it. It's the combination of everything you've built so far — pointed at a task. When you ask an AI to "review this design," without any setup, it gives you generic feedback. When your agent does it, it reads your brand guidelines (context), pulls relevant references if needed (retrieval), and applies your review criteria (skills). Same AI, completely different result.

### What is a sub-agent?
A sub-agent is a specialist. Instead of one agent that does everything (and does nothing well), you create focused agents for focused tasks. A design critique agent is different from a collateral creator agent — they need different skills, different references, sometimes different context.

A main agent sits above them and routes: "Is this a review task or a creation task?" Then it hands off to the right sub-agent. This is exactly how complex AI products work — there's an orchestrator that figures out what kind of request this is, then routes to the specialist that can handle it.

### Connect to their work
Ask: "Think about the different types of design tasks you do in a week. How many genuinely different TYPES are there?" Help them identify the categories — review/critique, creating new collateral from a brief, building product UI, checking brand compliance across existing materials.

Then ask: "If you had a junior designer joining your team, would you give them one giant instruction manual? Or would you say 'for reviews, follow this process; for collateral, follow this process'?" That's sub-agents. Specialization.

### Build: Create tasks/design-agent.md
Based on the task categories they identified, YOU write the main agent file — the orchestrator. This is a prompt that:
1. Reads from context/ to know the brand
2. Determines what type of task is being requested
3. Routes to the appropriate sub-agent:
   - For review/critique tasks → calls the design review skill from skills/design-review.md
   - For collateral creation tasks → calls the brand compliance skill from skills/brand-compliance-check.md and uses references from references/marketing-collateral/
4. Returns structured output appropriate to the task type

Show them the file, explain the routing logic, and commit with a descriptive message.

### Build: Create tasks/design-critique-sub-agent.md
YOU create a focused agent for design critique. It reads context/brand-guidelines.md and context/design-system.md, applies skills/design-review.md, and outputs a structured review with scores and specific feedback per criteria. Commit with a descriptive message.

Then test it live — ask them to describe a recent design (or share a screenshot if available). YOU run the critique agent against it and show them the structured output. Ask: "Is this feedback useful? What would you change about the criteria? What's missing?" If they suggest changes, update the skill file based on their feedback and commit. This teaches them that agents are living systems you refine, not set-and-forget.

### Build: Create tasks/collateral-creator-sub-agent.md
YOU create a focused agent for generating collateral briefs. It reads context/brand-guidelines.md, pulls from references/marketing-collateral/, applies skills/brand-compliance-check.md, and generates a structured brief for a specific collateral piece — dimensions, copy direction, visual approach, brand compliance notes. Commit with a descriptive message.

### Reflection
"You now have an agent system — a main agent that routes to sub-agents based on the task. Look at your product. It does the same thing: a user asks a question, the system determines what kind of question it is — is it about enrollment trends, financial data, peer comparison? — and routes to the right data source and processing logic. You just built a miniature version of that architecture. What does this help you understand about how your product handles different types of user queries?"

### Quiz
"A user of your product asks: 'How does our graduation rate compare to similar institutions?' Walk me through what happens — what's the context, what gets retrieved, what skill is applied, and how does routing work? Use the vocabulary from this week."
