---
title: "What We Learned Building AI Agents for Geospatial Analysis"
url: "https://carto.com/blog/lessons-building-ai-agents-geospatial-analysis/"
date: "Tue, 14 Apr 2026 00:00:00 +0000"
author: ""
feed_url: "https://carto.com/blog/index.xml"
---
<p>Late last year, we launched <a href="https://carto.com/blog/agentic-gis-bringing-ai-driven-spatial-analysis-to-everyone/">AI Agents</a> on the <a href="https://carto.com">CARTO platform</a>, a key piece of our <a href="https://carto.com/blog/what-is-agentic-gis/">Agentic GIS</a> vision to put geospatial analysis within reach of every team. These agents provide a conversational interface embedded in your maps, letting users perform spatial analysis through natural language, running queries directly on your data warehouse, powered by your vetted AI providers and LLMs of choice.</p>
<p>Since then, we've built and refined agents internally and with customers across dozens of use cases, from insurance risk assessment and network planning to retail site selection and urban mobility analysis. That hands-on experience taught us what makes a geospatial agent actually work, and what makes it fall short.</p>
<p>Those lessons pointed to a clear conclusion: building a reliable agent requires more than connecting a model to your data. It takes understanding how context, instructions, and tools need to work together for each use case. That's what led us to create the <strong><a href="https://docs.carto.com/carto-user-manual/ai-agents/agent-config-assistant">Agent Configuration Assistant</a></strong>, a tool that reduces the effort of setting up agents while raising their quality. You focus on your goal and requirements. The Assistant already has our best practices baked in.</p>
<div><video loop="loop" style="width: 100%; border-radius: 8px;">
<source src="https://carto.com/cdn.prod.website-files.com/63483ad423421bd16e7a7ae7/assistant-video-short.mp4" />
</video></div>
<p>This post walks through six of those lessons and how they shaped the way we build agents today.</p>
<div><h2 style="font-family: montserrat;">1. Start with a well-scoped use case</h2></div>
<p>It's tempting to create an all-purpose agent, one that handles site selection, revenue forecasting, logistics optimization, and customer segmentation all at once. But the broader the scope, the harder it is for the agent to know which datasets matter, which analysis to run, or what a good answer even looks like. It defaults to generic queries, picks the wrong datasets, and produces results that look plausible but are operationally useless.</p>
<p>The most effective agents we've seen are built around a <strong>specific, well-scoped use case</strong>, designed around <strong>the business questions the end user will actually ask</strong>. A territory manager agent built around one question, "Which stores are underperforming?" or "How does this region compare?", knows exactly where to look. It reaches for the stores dataset, prioritizes revenue and footfall metrics, and returns results as a map with regional context already in place.</p>
<div style="display: flex;">
<div style="border-radius: 6px;">
<p style="font-size: 0.8rem; font-weight: 700; color: #C47D10; letter-spacing: 0.5px;">Too broad</p>
<p style="margin: 0; font-size: 0.95rem; color: #333; line-height: 1.5;"><em>"An agent that helps with geospatial analysis. It can handle location data, run queries, and create visualizations for any use case."</em></p>
</div>
<div style="border-radius: 6px;">
<p style="font-size: 0.8rem; font-weight: 700; color: #036FE2; letter-spacing: 0.5px;">Focused</p>
<p style="margin: 0; font-size: 0.95rem; color: #333; line-height: 1.5;"><em>"An agent for retail territory managers that analyzes store performance by region, comparing revenue, footfall, and competitor proximity, and highlights underperforming locations."</em></p>
</div>
</div>
<p>If you've ever scoped a map dashboard, you already know this instinct. The same focus and intentionality that makes a good dashboard makes a good agent.</p>
<blockquote id="">Start narrow. Think about who will use this agent and what they need to accomplish. An agent built for a specific audience earns trust. An agent built for "everyone" earns none.</blockquote>
<div><h2 style="font-family: montserrat;">2. Context is what separates a useful agent from a frustrating one</h2></div>
<p>One of our earliest agents had access to a complex data model but we hadn't explained what the fields meant or how the tables related. The queries it generated were syntactically correct but operationally meaningless.</p>
<blockquote id="">Most agent failures are not model failures. They are context failures.</blockquote>
<p>For geospatial agents, context means giving the agent real knowledge about your data (what columns mean, how tables relate, what a good query looks like) and about the use case it serves. CARTO provides part of this context automatically, like the map configuration and the definitions of the tools enabled by the creator. The rest comes from you. The <a href="https://docs.carto.com/carto-user-manual/ai-agents/agent-config-assistant">Agent Configuration Assistant</a> makes this easier by generating the full agent configuration through conversation, including enabling <a href="https://carto.com/blog/carto-mcp-server-turn-your-ai-agents-into-geospatial-experts/">MCP tools</a> that turn complex geospatial operations into capabilities the agent can call.</p>
<div style="width: 100%;">
<svg viewBox="0 0 720 320" xmlns="http://www.w3.org/2000/svg">
<rect fill="#EEF1F6" height="320" rx="14" width="720">
<defs></defs>
<!-- Section labels -->
<text fill="#8895A5" font-size="9" font-weight="600" x="40" y="30">CONTEXT</text>
<text fill="#8895A5" font-size="9" font-weight="600" x="40" y="222">CAPABILITIES</text>
<!-- Elbow connectors: top row to agent -->
<!-- Use Case → Agent -->
<path d="M 140 96 L 140 120 L 280 120 L 280 139" fill="none" opacity="0.15" stroke="#162945" stroke-width="1.2">
<circle cx="280" cy="139" fill="#036FE2" opacity="0.5" r="3">
<!-- Instructions → Agent -->
<path d="M 360 96 L 360 139" fill="none" opacity="0.15" stroke="#162945" stroke-width="1.2">
<circle cx="360" cy="139" fill="#036FE2" opacity="0.5" r="3">
<!-- Semantic Model → Agent (dashed) -->
<path d="M 580 96 L 580 120 L 440 120 L 440 139" fill="none" opacity="0.15" stroke="#036FE2" stroke-dasharray="5 4" stroke-width="1.2">
<circle cx="440" cy="139" fill="#036FE2" opacity="0.3" r="3">
<!-- Elbow connectors: bottom row to agent -->
<!-- Map Context → Agent -->
<path d="M 140 238 L 140 214 L 280 214 L 280 189" fill="none" opacity="0.15" stroke="#162945" stroke-width="1.2">
<circle cx="280" cy="189" fill="#036FE2" opacity="0.5" r="3">
<!-- Core Tools → Agent -->
<path d="M 360 238 L 360 189" fill="none" opacity="0.15" stroke="#162945" stroke-width="1.2">
<circle cx="360" cy="189" fill="#036FE2" opacity="0.5" r="3">
<!-- MCP Tools → Agent -->
<path d="M 580 238 L 580 214 L 440 214 L 440 189" fill="none" opacity="0.15" stroke="#162945" stroke-width="1.2">
<circle cx="440" cy="189" fill="#036FE2" opacity="0.5" r="3">
<!-- AI Agent (center) -->
<rect fill="#162945" height="50" rx="10" width="160" x="280" y="139">
<text fill="#fff" font-size="14" font-weight="700" text-anchor="middle" x="360" y="169">AI Agent</text>
<!-- Top row cards -->
<!-- Use Case -->
<rect fill="#fff" height="56" rx="8" stroke="#D8DDE4" stroke-width="0.8" width="200" x="40" y="40">
<rect fill="#162945" height="56" rx="1.5" width="3" x="40" y="40">
<text fill="#162945" font-size="12" font-weight="600" x="60" y="63">Use Case</text>
<text fill="#6B7A8D" font-size="9" x="60" y="80">Audience, scope, purpose</text>
<!-- Instructions -->
<rect fill="#fff" height="56" rx="8" stroke="#D8DDE4" stroke-width="0.8" width="200" x="260" y="40">
<rect fill="#162945" height="56" rx="1.5" width="3" x="260" y="40">
<text fill="#162945" font-size="12" font-weight="600" x="280" y="63">Instructions</text>
<text fill="#6B7A8D" font-size="9" x="280" y="80">Behavior, workflows, examples</text>
<!-- Semantic Model (upcoming) -->
<rect fill="#fff" height="56" rx="8" stroke="#036FE2" stroke-dasharray="5 4" stroke-width="0.8" width="200" x="480" y="40">
<rect fill="#036FE2" height="56" opacity="0.4" rx="1.5" width="3" x="480" y="40">
<text fill="#036FE2" font-size="12" font-weight="600" opacity="0.6" x="500" y="63">Semantic Model</text>
<text fill="#6B7A8D" font-size="9" opacity="0.6" x="500" y="80">Definitions, relationships, metrics</text>
<rect fill="#EBF3FE" height="16" rx="8" width="54" x="617" y="48">
<text fill="#036FE2" font-size="7.5" font-weight="600" text-anchor="middle" x="644" y="59.5">upcoming</text>
<!-- Bottom row cards -->
<!-- Map Context -->
<rect fill="#fff" height="56" rx="8" stroke="#D8DDE4" stroke-width="0.8" width="200" x="40" y="238">
<rect fill="#162945" height="56" rx="1.5" width="3" x="40" y="238">
<text fill="#162945" font-size="12" font-weight="600" x="60" y="261">Map Context</text>
<text fill="#6B7A8D" font-size="9" x="60" y="278">Sources, layers, widgets, filters</text>
<!-- Core Tools -->
<rect fill="#fff" height="56" rx="8" stroke="#D8DDE4" stroke-width="0.8" width="200" x="260" y="238">
<rect fill="#162945" height="56" rx="1.5" width="3" x="260" y="238">
<text fill="#162945" font-size="12" font-weight="600" x="280" y="261">Core Tools</text>
<text fill="#6B7A8D" font-size="9" x="280" y="278">Query, add layer, charts</text>
<!-- MCP Tools -->
<rect fill="#fff" height="56" rx="8" stroke="#D8DDE4" stroke-width="0.8" width="200" x="480" y="238">
<rect fill="#162945" height="56" rx="1.5" width="3" x="480" y="238">
<text fill="#162945" font-size="12" font-weight="600" x="500" y="261">MCP Tools</text>
<text fill="#6B7A8D" font-size="9" x="500" y="278">CARTO MCP Server, Workflows</text>
<!-- Caption -->
<text fill="#8895A5" font-size="9.5" text-anchor="middle" x="360" y="310">Each layer adds context. Together, they make the agent effective.</text>
</svg>
</div>
<div><h2 style="font-family: montserrat;">3. Give your instructions structure, not just content</h2></div>
<p>The most common pattern we see with new agent creators is a long paragraph mixing datasets, behavior rules, edge cases, and example queries all together. Poorly structured instructions force the model to guess what matters most. Structured instructions guide it toward the right behavior.</p>
<p>The <a href="https://docs.carto.com/carto-user-manual/ai-agents/agent-config-assistant">Agent Configuration Assistant</a> handles this for you. It structures instructions following best practices, organizing them into clear sections like data definitions, behavior, workflows, edge cases, and example questions. You focus on what you know best. Your data, your use case, and the business questions your end users will ask. The Assistant structures that into instructions the agent can reliably follow.</p>
<figure class="w-richtext-figure-type-image w-richtext-align-center"><div><img alt="Agent Configuration Assistant showing structured instructions output" height="auto" src="https://carto.com/cdn.prod.website-files.com/63483ad423421bd16e7a7ae7/prompt-engineering-structured-instructions.png" style="border-radius: 8px;" width="auto" /></div></figure>
<blockquote id="">Structure isn't just formatting. It's how you tell the model what matters most.</blockquote>
<div><h2 style="font-family: montserrat;">4. You're designing an experience, not just configuring a tool</h2></div>
<p>We built an agent that scored and ranked locations based on demographics, competition, and accessibility. The analysis was solid, but the user didn't trust the results because they couldn't understand how the agent got there. Once we configured it to surface each step (the area considered, the enrichment applied, the score calculation), the same analysis went from "I don't trust this" to "this is exactly what I needed."</p>
<p>That lesson shaped how <a href="https://carto.com/ai-agents/">AI Agents</a> work today. As the agent works, it shows what it's doing, the steps it takes and the results it produces, so users can follow along rather than wait for a final answer. This transparency turns a black-box experience into one users can trust. From there, you design the rest of the experience. Should the agent open with a summary or ask what the user needs? Should it show a chart first, or a map? A sales executive wants to start broad and narrow down. A supply chain manager wants exceptions first. You shape these patterns through conversation starters, default behaviors, and instructions that handle ambiguity gracefully.</p>
<div><video loop="loop" style="width: 100%; border-radius: 8px;">
<source src="https://carto.com/cdn.prod.website-files.com/63483ad423421bd16e7a7ae7/agent-video-fires.mp4" />
</video></div>
<blockquote id="">The best agents feel like they were built for you, because someone took the time to design the conversation, not just the capabilities.</blockquote>
<div><h2 style="font-family: montserrat;">5. Test like your end users, then iterate</h2></div>
<p>You built the agent knowing exactly what it can do. Your end users don't know what the agent is capable of. They'll ask questions you didn't anticipate with phrasing you didn't expect. Test the agent the way they would, with imprecise questions, incomplete context, and real-world messiness. When someone types "how are my stores doing?" instead of a precise query, does the agent know what to do?</p>
<p>The iteration doesn't stop at launch. Real usage reveals assumptions you didn't know you'd made, and each round makes the agent sharper. Bring what you learn back to the <a href="https://docs.carto.com/carto-user-manual/ai-agents/agent-config-assistant">Agent Configuration Assistant</a> to refine and improve the configuration through conversation.</p>
<blockquote id="">Test with the questions your end users will actually ask, not the ones you used while building it. The iteration cycle is where good agents become great ones.</blockquote>
<div><h2 style="font-family: montserrat;">6. Good answers come from someone who understands the problem</h2></div>
<p>Building a good agent requires understanding how context, instructions, and tools work together. But the most critical ingredient isn't technical. <strong>It's knowing your data, your users, and what a good answer looks like.</strong></p>
<p>A data analyst who regularly answers "which locations are underperforming?" knows which dataset to query, which metrics matter, and what a misleading result looks like. That knowledge, your unique business context, is exactly what makes a well-configured agent. When you write instructions that say "always compare against the regional average," or build a Workflow for location allocation analysis and expose it as an <a href="https://carto.com/blog/carto-mcp-server-turn-your-ai-agents-into-geospatial-experts/">MCP tool</a>, you're encoding domain expertise that turns a generic AI into something your team actually trusts.</p>
<blockquote id="">The hardest part of building an agent isn't the technology. It's knowing which insights will drive your organization forward.</blockquote>
<div><h2 style="font-family: montserrat;">From lessons to product</h2></div>
<p>We built the <a href="https://docs.carto.com/carto-user-manual/ai-agents/agent-config-assistant">Agent Configuration Assistant</a> to put all of this context within reach. It captures how CARTO agents are structured, how to turn your requirements into structured instructions, and the available tool context to guide which tools to use for each use case.</p>
<p>You bring your goal and your domain knowledge. The Assistant generates an agent ready to deploy.</p>
<div><video loop="loop" style="width: 100%; border-radius: 8px;">
<source src="https://carto.com/cdn.prod.website-files.com/63483ad423421bd16e7a7ae7/assistant-video-config.mp4" />
</video></div>
<div><h2 style="font-family: montserrat;">Try it yourself</h2></div>
<p>Ready to build your own AI Agent? Start with a focused use case and let the <a href="https://docs.carto.com/carto-user-manual/ai-agents/agent-config-assistant">Agent Configuration Assistant</a> guide you. Sign up for a free <a href="https://app.carto.com/signup">14-day trial</a>, or <a href="https://go.carto.com/carto-demo-request">request a demo</a> to see AI Agents in action on your own data.</p>
