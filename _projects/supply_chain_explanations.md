---
layout: page
title: "MAESTRO: Agentic RAG for supply-chain optimization"
description: A multi-expert chatbot combining document retrieval, spreadsheet analysis, and clear explanations of supply-chain optimization.
permalink: /project/supply_chain_explanations/
img: assets/img/projects/maestro/problem-types.png
importance: 5
category: research
start_date: 2025-08
end_date: 2025-12
tags:
  - RAG
  - LangGraph
  - Multi-Agent Systems
  - Supply Chain
---

**Corteva · Industry-sponsored research · August–December 2025**

[Source code](https://github.com/Manavvora/MAESTRO) · [Project documentation](https://github.com/Manavvora/MAESTRO#readme)

## Project overview

**MAESTRO** stands for **Multi-Agent Expert System for Transparent Response Orchestration**. It helps non-technical stakeholders understand supply-chain optimization models and their outputs by combining retrieved context, computed spreadsheet facts, and explanations from specialized agents.

The project covers two settings: **facility location**, where questions concern the placement of warehouses or other facilities, and **multi-commodity flow**, where users need to understand how products move through a logistics network. The goal is to turn model documentation and solver output into explanations with clear site names, relevant numbers, and supporting sources.

{% include figure.liquid
   path="assets/img/projects/maestro/pipeline.png"
   alt="MAESTRO pipeline: text and spreadsheet inputs, ChromaDB retrieval, optional Pandas analysis, expert routing, and aggregation into a business answer with sources."
   caption="MAESTRO combines retrieved document context and computed spreadsheet facts before expert routing and response aggregation."
%}

## How it works

1. **Retrieve relevant context.** Text documents and spreadsheet content are indexed in ChromaDB using sentence-transformer embeddings. Semantic search supplies the relevant passages, together with their source filenames and chunk identifiers.
2. **Compute facts from solver output.** When matching spreadsheets are present, a Pandas analysis node computes product movements over time, throughput by location, and capacity utilization. Those facts are added to the context used by the agents.
3. **Route to specialized experts.** Keyword-based routing selects mathematical, optimization, supply-chain, or implementation expertise. If no routing keywords match, all four roles are consulted.
4. **Synthesize a stakeholder-facing answer.** An aggregator reconciles the expert responses into a direct answer, supporting findings, an explanation, and relevant recommendations. The command-line interface also reports the retrieved sources, chunk relevance, and expert domains used.

The implementation uses **Python, LangGraph, ChromaDB, sentence-transformers, Pandas, and Gemini**. LangGraph carries the retrieved context, computed facts, selected experts, and responses through the workflow.

## Two supply-chain workflows

{% include figure.liquid
   path="assets/img/projects/maestro/problem-types.png"
   alt="Comparison of facility-location questions answered from text context and multi-commodity-flow questions answered using text, solver output, and computed spreadsheet facts."
   caption="Facility-location questions primarily use document context; multi-commodity-flow questions additionally use spreadsheet calculations."
%}

For **facility location**, the knowledge base contains the problem description, assumptions, formulation, solution approach, and implementation details. Retrieved context helps explain what the model does and why its assumptions matter.

For **multi-commodity flow**, the system also reads solver-output and capacity spreadsheets. This supports questions such as:

- Which locations processed the most product, and which processing steps contributed?
- Where is utilization highest relative to available capacity?
- How does a particular product move through the network over time?

The repository includes three implementations: a multi-expert baseline without retrieval, traditional RAG with vector retrieval, and the LangGraph workflow with spreadsheet analysis. These provide progressively richer ways to ground the experts’ answers.

## My contribution

I built a multi-agent chatbot to explain supply-chain optimization outputs to non-technical stakeholders. My work focused on:

- **Agentic RAG orchestration:** Implemented the LangGraph workflow connecting retrieval, tool use, and response generation for source-grounded explanations.
- **Expert routing and aggregation:** Routed questions to role-based expert agents and synthesized their responses into an answer that stakeholders could understand.

**Collaborators:** Manav Vora, Mo Phoompho, and Melkior Ornik.

The diagrams are from the [MAESTRO repository](https://github.com/Manavvora/MAESTRO), released under the [MIT License]({{ "/assets/img/projects/maestro/LICENSE.txt" | relative_url }}).
