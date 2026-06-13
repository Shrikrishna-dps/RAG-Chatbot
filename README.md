# RAG Chatbot

SCM Intelligence Assistant

# Public Chatbot URL

https://cloud.flowiseai.com/chatbot/0be36a98-7d56-4a96-b636-a23d77f97ccc

---

# Overview

SCM Intelligence Assistant is a RAG-based chatbot built using Flowise AI for supply chain analytics and supplier governance queries.

The chatbot answers questions related to:

* supplier performance
* disruption risks
* compliance scores
* regional PO concentration
* rebate eligibility
* defect rates
* governance policies

---

# Technologies Used

# Framework

* Flowise AI

# LLM

* Groq API
* Model: llama-3.1-8b-instant

# Embeddings

* sentence-transformers/all-MiniLM-L6-v2

# Vector Database

* Pinecone

# Memory

* Buffer Memory

---

# Chunk Configurations Tried

# Configuration 1 (used this for output)

* Chunk Size: 1000
* Chunk Overlap: 100

Result:
Better policy retrieval and broader context understanding.

# Configuration 2

* Chunk Size: 500
* Chunk Overlap: 100

Result:
Faster retrieval and better supplier-specific accuracy.

---

# Retrieval Configuration

* Pinecone Top K: 15
* Similarity Search enabled
* Conversational Retrieval QA Chain used
* Source document retrieval enabled

---

AI:
Hi there! How can I help?

Question 1

Me:
Which Tier-3 suppliers have an active disruption flag, and what response level applies per policy?

AI:
Based on the provided context, the Tier-3 suppliers with an active disruption flag are:

Dravex Components India
Plataforma Metales SA
Maghreb Castworks
Helios Pack Greece
Cerromax Mineria
Orinoco Pack SAPI
Quetzal Textiles
Sibertek Molding
Archipelago PCB Corp
Varna Electronics EAD
Deltaforge Vietnam
According to the policy, these suppliers are classified as High Risk with active disruption flags. Per Policy Section 9:

Response Level = Level 3 Activate

Actions required:

CPO escalation
Alternate supplier activation
Minimum 40% alternate sourcing volume

Question 2

Me:
Which suppliers qualify for the annual Volume Rebate Program and how many are there?

AI:
Based on the provided context, the suppliers that qualify for the annual Volume Rebate Program are:

SUP-028 | Hokkaido Alloy Tech
SUP-044 | Broken Hill Alloys
SUP-049 | Munich Alloy Technik
SUP-060 | Nordloom Finland Oy
SUP-102 | Crestline Chemical Supply
There are 5 suppliers that qualify for the annual Volume Rebate Program.

Question 3

Me:
Which region has the highest total PO value, and does it breach the concentration limit?

AI:
Based on the provided context, the region with the highest total PO value is APAC with a value of USD 131,620,400, which is 36.97% of the total PO value.

This does not breach the concentration limit of 45%.

Question 4

Me:
Which suppliers are on Supplier Watch List (SWL) status and what does it restrict?

AI:
Based on the provided context, the suppliers on Supplier Watch List (SWL) status are:

SUP-014 | Deccan Polymer Mfg
SUP-017 | Sahyadri Alloy Tech
SUP-020 | MeKong Pack Co
SUP-022 | DaNang Metal Works
SUP-078 | Varna Electronics EAD
SUP-089 | Yucatan Polymer Mfg
SUP-092 | Buenos Aires Pack
SUP-095 | Cerromax Mineria
SUP-096 | Lima Polymer SA
SWL status restricts:

New Purchase Order issuance is capped at 20% of the prior quarter's order volume
The supplier remains on SWL until the next scheduled audit clears the Compliance Score above 60
Scores below 70 at a scheduled audit additionally trigger a mandatory follow-up audit within 60 days at the supplier's cost (Section 7.2)

Question 5

Me:
Which product category has the highest average defect rate and does it exceed the Tier-2 limit?

AI:
Based on the provided context, the product category with the highest average defect rate is Mechanical Components at 1.882%.

According to the context, the Tier-2 limit is 2.50%. The category average of 1.882% is below this threshold. However, it exceeds the Tier-1 limit of 0.99%.

---

## Notes

* Public chatbot sharing enabled through Flowise Cloud.
* Chatbot tested using all provided validation questions.
* API keys and environment variables excluded from repository.
