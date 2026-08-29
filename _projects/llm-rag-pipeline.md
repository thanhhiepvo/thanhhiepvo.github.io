---
layout: project
title: "LLM &amp; RAG Pipeline"
subtitle: "Ontology-guided retrieval with LangChain, ChromaDB, and FAISS"
selected: "y"
published: false
order: 1
github: ""
---

An end-to-end retrieval-augmented generation system for the legal domain, built during my
research at Queen's University Belfast. Rather than relying on embedding similarity alone,
retrieval is guided by an ontology so that the model's answers stay anchored to the
concepts and relations the domain actually defines.

**Dual retrieval.** Two parallel pipelines built on LangChain, ChromaDB, and FAISS retrieve
ontology entities and sentence-level legal obligations jointly, so a query surfaces both
the governing concept and the specific obligation text.

**Fine-tuning.** Decoder-only LLMs adapted with LoRA and other PEFT methods, evaluated
across both open- and closed-source models, targeting knowledge representation,
disambiguation, and reasoning.

**Related work.** This line of work also produced my undergraduate thesis,
*Building Ontology-based Constraints for Large Language Models*.
