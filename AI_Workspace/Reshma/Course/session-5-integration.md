# Session 5: Putting it all together

## Concepts
How context + RAG + skills + agents form a complete AI workflow. Version control of AI artifacts. The design handoff as a skill file. Evaluation — how do you know if your AI setup works well? The full architecture connection between their workspace and the product.

## Teaching flow

### Recap and bridge
"This is our final session. Over four days we've built context files, organized references, written skill files, and created an agent system with sub-agents. Today we're going to tie everything together — make sure your workspace is complete, create one more critical skill, and step back to see the full architecture of what we've built and how it maps to the product you're designing."

### Build: Create skills/design-handoff.md
Ask them: "When you hand off designs to the dev team today, what questions do they always come back with? What information is always missing?" Based on their answers, YOU create a design handoff template as a skill file. This is a structured spec that covers everything a developer needs:

Help them think through the sections by asking questions: What about interaction states? Accessibility? Responsive behavior? Edge cases? Then YOU write the file with sections for: screen/component name, design intent and user goal, layout specifications (grid, breakpoints, responsive behavior), interaction states (default, hover, active, disabled, error, loading), typography specs per element, color usage per element, spacing and padding values, accessibility requirements (contrast ratios, ARIA labels, focus states, keyboard navigation), assets to export, edge cases and content overflow behavior, and any animations or transitions.

Show them the file. Ask what's missing based on their real handoff experience. Iterate, then commit with a descriptive message.

This is also a teaching moment about AI and structured outputs: "This template is a skill because it tells AI how to GENERATE a structured handoff document from a design description. It's not just a blank form — it's instructions for producing consistent, complete output every time."

### Build: Create README.md
YOU create a README for their workspace that documents what everything is and how to use it. Structure:

- Purpose: What this workspace is and what it does
- Folder guide: One line per folder explaining what goes there
- How to use: How to invoke the main agent, when to update context files, how to add new references
- Maintenance: When to review and update skill files, how to version changes

Show them the README, ask if it makes sense, then commit.

### Build: Create changelog.md
YOU start a changelog that tracks changes to their workspace over time. First entry covers everything built during the course. Explain: "Your skill files and context docs will evolve. When you update your brand guidelines, when you refine your review criteria after using them — log it here. This is version control for your AI workflow, just like you version your design files." Commit.

### The full architecture — connect everything
Ask them to look at their complete workspace and map it to the product:

"Let's put it all together. In your workspace:
- context/ = what AI always knows → In your product: core domain knowledge like what IPEDS fields mean, institutional categories, standard metrics
- references/ = what AI retrieves for specific tasks → In your product: specific data sources queried for specific questions
- skills/ = how AI processes and evaluates → In your product: query interpretation logic, comparison frameworks, data presentation rules
- tasks/ = agents that orchestrate everything → In your product: the agent that receives a user question, determines the type, routes to the right source, applies the right logic, and returns an answer

You've been designing the interface for this system. Now you understand what's behind it."

### Evaluation concept
"How do you know your design review agent is giving good feedback? You test it. You run designs through it and check whether the output matches what YOU would say. When it doesn't, you refine the skill file. This is evaluation — and it's exactly how your product gets tested. Someone checks whether the answers are accurate, and when they're not, the team refines the routing, the data sources, or the processing logic."

### Final reflection
"You started this week watching me clone a repository. Now you have a complete AI-powered design workspace with persistent context, organized references, articulated skills, and an agent system with sub-agents. You understand context windows, RAG, skills, agents, routing, and evaluation. More importantly, you understand the architecture of the product you design every day. How will this change the way you approach your work — both using AI tools and designing for an AI product?"
