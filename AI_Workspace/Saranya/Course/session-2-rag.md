# Session 2: Not everything belongs in memory

## Concepts
RAG (Retrieval Augmented Generation). The difference between persistent context and retrieved references. Token limits as a design constraint. Why organizing what AI pulls from — and when — matters as much as what AI always knows.

## Teaching flow

### Recap and bridge
"Yesterday you built your first context file — your brand guidelines. That's information AI should always have. But here's the question: should AI always have EVERYTHING? What about competitor screenshots, copy documents for specific pages, user research for a particular feature? If you loaded all of that all the time, you'd bury the important stuff under noise."

### What is RAG?
RAG means the AI goes and finds specific information only when it needs it, rather than carrying everything at all times. Think of it this way: your persistent context is what's pinned to the wall above your desk — always visible. RAG is the filing cabinet next to you. You don't spread every file across your desk. You pull the right folder when you're working on a specific task, then put it back.

In AI products, this is how large knowledge bases work. You can't fit an entire university's data into one context window. Instead, the system figures out which data is relevant to the question and pulls just that. This is exactly what your product does when a user asks a question — it doesn't load every data source at once. It identifies which source answers that question and retrieves from it.

### Why not just load everything?
Teach token limits simply: "AI's desk has a size limit — called a token limit. Tokens are roughly chunks of words. Every file you load, every message in the conversation, takes up space. If you fill the desk with everything, AI has less room to actually think and respond. Worse, when there's too much on the desk, AI starts paying less attention to each individual piece. Choosing what to load is a design decision."

### Connect to their work
Ask: "Think about when you design a landing page versus when you design a product UI screen versus when you create a pitch deck. Your brand guidelines stay the same across all three. But what CHANGES? What references or inputs are specific to each task?"

Help them categorize their design inputs:
- **Always needed (persistent context):** Brand guidelines, design system, component library, typography rules
- **Needed for specific tasks (retrieval):** Copy documents for a specific page, user research for a specific feature, competitor references for a specific redesign, content briefs for specific collateral

Ask them: "Who decides what gets pulled for which task?" In their work, THEY decide — they open the right Figma file or reference doc. In an AI product, the retrieval system decides. That's what makes RAG hard to build well and why it matters that they understand it.

### Build: Create the references folder structure
Guide them to organize their references/ folder by task type:
```
references/
├── product-ui/
├── marketing-collateral/
├── landing-pages/
└── pitch-decks/
```

Have them put one real reference document into the most relevant subfolder — a copy doc, a competitor screenshot description, a brief they recently used. Commit with a descriptive message.

Then ask: "Look at your context/ folder and your references/ folder side by side. Explain to me the difference between these two in your own words — and tell me when AI should use each one."

### Build: Create context/design-system.md
If they have a design system or component library documentation, guide them to create a second persistent context file. If they don't have formal documentation, help them articulate the key rules: grid system, spacing scale, component naming conventions, breakpoints. This reinforces Session 1's concept while expanding their context foundation.

### Reflection
"You now have two types of AI knowledge in your workspace: things AI always knows (context/) and things AI pulls when relevant (references/). This is the same architecture behind your product. The product has persistent knowledge — like what IPEDS fields mean — and retrieved knowledge — like specific institutional data for a specific query. You just built a personal version of the same system. How does this change how you'd think about designing the interface for a product that uses RAG?"

### Quiz
"Categorize each of these — persistent context or retrieval reference?
- Your icon library naming conventions
- A mood board for a specific campaign
- Your approved brand color palette
- User interview notes for a feature redesign
- Your grid system and spacing scale
- A competitor's pricing page screenshot
- Your component library documentation"
