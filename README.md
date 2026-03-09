# Competitive Pokémon TCG Data Mining
**Author:** Axel Alvarez  
**Course:** CS 4412: Data Mining  
**Status:** Milestone 2: Initial Implementation

## Project Overview
This project utilizes the **Knowledge Discovery in Databases (KDD)** process to analyze the competitive Pokémon TCG metagame. The goal is to mathematically define the **"Immutable Core"** (essential cards) of top-tier decks versus the **"Flex Slots"** (adaptable tech choices) used to respond to the environment.

---

## Milestone 2: Initial Implementation

### **1. Data Selection & Collection**
* **Source:** Automated retrieval via the Limitless TCG API.
* **Volume:** Aggregated **2,664 raw records** from the 50 most recent Standard format tournaments.
* **Cleaning:** Filtered out 47 incomplete or private decklists, resulting in a high-integrity dataset of **2,617 usable decks**.

### **2. Preprocessing & Transformation**
* **Normalization:** Implemented custom logic to group regional card variants (e.g., *Boss's Orders*, *Professor's Research*) into canonical IDs to reduce noise for future mining.
* **Feature Engineering:** Utilized a `DictVectorizer` to convert categorical decklists into a numerical format.
* **Matrix Generation:** Successfully generated a **Binary Sparse Matrix** consisting of **2,617 rows and 811 unique card features**.

### **3. Key EDA Insights**
* **Core Size Discovery:** Analysis of unique card counts per deck reveals that the average competitive "Core Engine" consists of **27–30 unique cards**.
* **Synergy Mapping:** Correlation heatmaps identified strong functional synergies between top staples like *Iono* and *Nest Ball*, providing the baseline for cluster validation.

---

## Repository Structure
* `/notebooks/`: Primary development notebook (`Alvarez_M2.ipynb`).
* `/reports/`: Detailed PDF summaries and milestone documentation.
* `/src/`: (Upcoming) Standalone Python scripts for final Mining models.

---
