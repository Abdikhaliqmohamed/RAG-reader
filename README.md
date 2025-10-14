#  RAG PDF Assistant

Et Retrieval-Augmented Generation (RAG) projekt, der gør det muligt at søge intelligent i PDF-dokumenter ved hjælp af lokal embeddings og sprogmodeller.  
Projektet kombinerer **LangChain**, **ChromaDB** og **Ollama** (f.eks. med *Mistral*) for at besvare spørgsmål baseret på indhold fra dine egne filer.

---

##  Funktionalitet

- Læser og indlæser PDF-dokumenter fra en valgt mappe (`DATA_PATH`)
- Deler tekst op i mindre bidder (chunks)
- Laver embeddings med en lokal model (via HuggingFace eller Ollama)
- Gemmer embeddings i en vedvarende Chroma-database (`CHROMA_PATH`)
- Muliggør retrieval af relevante dokumentafsnit baseret på brugerens spørgsmål
- Kombinerer dokumentkontekst med et Large Language Model (LLM) prompt for at generere et informeret svar

---

## Projektstruktur

| **rag_project** |
|------|-------|---------------------------|---------|
| 1 | query_data.py # Indeholder funktioner til at søge i databasen og køre RAG-query |
| 2 | create_data.py # Indeholder funktioner til at loade, splitte og gemme PDF-data i Chroma | 
| 3 | main.py # Hovedfil, der kalder query_rag() | 
| 4 | requirements.txt # Python dependencies| 
| 5 | data/ # PDF-dokumenter der skal indlæses | 
| 6 | chroma/ # Vedvarende database med embeddings (genereres automatisk) | 


📁 rag_project/
│
├── query_data.py # Indeholder funktioner til at søge i databasen og køre RAG-query
├── create_data.py # Indeholder funktioner til at loade, splitte og gemme PDF-data i Chroma
├── main.py # Hovedfil, der kalder query_rag()
│
├── requirements.txt # Python dependencies
│
├── 📂 data/ # PDF-dokumenter der skal indlæses
└── 📂 chroma/ # Vedvarende database med embeddings (genereres automatisk)
