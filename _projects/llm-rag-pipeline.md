---
layout: project
title: "LLM &amp; RAG Pipeline"
subtitle: "Ontology-guided retrieval with LangChain, Chroma, and FAISS"
selected: "y"
order: 1
github: ""
---

A retrieval-augmented generation pipeline that uses an ontology to constrain what the
language model is allowed to assert. Domain concepts and their relations are encoded as
an ontology, and retrieval is guided by that structure rather than by embedding similarity
alone.

**Stack.** LangChain for orchestration, Chroma and FAISS as dual vector stores, and
ontology-derived constraints applied at the prompt-construction step.

**Related work.** This project grew out of my undergraduate thesis,
*Building Ontology-based Constraints for Large Language Models*, and my research at
Queen's University Belfast.
