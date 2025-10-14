# 🧠 RAG PDF Assistant

Et Retrieval-Augmented Generation (RAG) projekt, der gør det muligt at søge intelligent i PDF-dokumenter ved hjælp af lokal embeddings og sprogmodeller.  
Projektet kombinerer **LangChain**, **ChromaDB** og **Ollama** (f.eks. med *Mistral*) for at besvare spørgsmål baseret på indhold fra dine egne filer.

---

## 🚀 Funktionalitet

- Læser og indlæser PDF-dokumenter fra en valgt mappe (`DATA_PATH`)
- Deler tekst op i mindre bidder (chunks)
- Laver embeddings med en lokal model (via HuggingFace eller Ollama)
- Gemmer embeddings i en vedvarende Chroma-database (`CHROMA_PATH`)
- Muliggør retrieval af relevante dokumentafsnit baseret på brugerens spørgsmål
- Kombinerer dokumentkontekst med et Large Language Model (LLM) prompt for at generere et informeret svar

---

## 🗂️ Projektstruktur

