# Competitive Pokémon TCG Data Mining: Structural Analysis
**Author:** Axel Alvarez  
**Course:** CS 4412: Data Mining  
**Status:** Milestone 3: Advanced Implementation & Discovery

---

## Project Overview
This project utilizes the **Knowledge Discovery in Databases (KDD)** process to deconstruct the competitive Pokémon TCG metagame. By leveraging live tournament data via the **Limitless TCG API**, the analysis moves beyond descriptive frequency counts to mathematically define the **"Immutable Core"** of top-tier archetypes and quantify the performance costs of strategic innovation.



---

## Milestone 3: Advanced Implementation

### **1. Pattern Discovery (FP-Growth)**
* **Technique:** Implemented the **FP-Growth algorithm** for association rule mining.
* **Optimization:** Utilized a custom **Disjoint Itemset** filter and a confidence threshold of $Confidence \ge 0.85$. 
* **Discovery:** Successfully isolated six distinct strategic engines by filtering data noise, allowing for a mathematical definition of a deck's **Immutable Core** versus its **Flex Slots**.

### **2. Dimensionality Reduction & Mapping (PCA)**
* **Technique:** Applied **Principal Component Analysis (PCA)** to condense the 811-feature card matrix into a two-dimensional "Metagame Geography."
* **Visualization:** Identified distinct archetype islands representing optimized competitive strategies, revealing how decks cluster based on shared core utilities.



### **3. Anomaly Detection (Local Outlier Factor)**
* **Technique:** Integrated **Local Outlier Factor (LOF)** to identify **"Rogue"** archetypes as density-based outliers.
* **Metric:** By analyzing local density rather than simple distance, the model flagged decks sitting in the "white space" of the metagame map—innovative lists that defy standard cluster conventions.



### **4. Classification & Performance Correlation**
* **Interpreter:** Trained a **Decision Tree Classifier** to translate abstract PCA coordinates into human-readable rules, identifying the **"Buddy-Buddy Poffin"** engine as the primary axis of metagame divergence.

---

## Repository Structure
* `/notebooks/`: Primary development notebook (`Alvarez_M3.ipynb`) including the full end-to-end pipeline.
* `/reports/`: Detailed PDF analysis and milestone documentation.
* `/src/`: Production-ready scripts for the FP-Growth and PCA engines.

---

## Getting Started
### **Requirements**
* `pandas`, `numpy`, `matplotlib`, `seaborn`
* `scikit-learn`
* `mlxtend` (for FP-Growth)

### **Execution**
1. Clone the repository.
2. Ensure an active internet connection for the live API ingestion.
3. Run `Alvarez_M3.ipynb`. The notebook is designed for **full reproducibility**, automatically handling data normalization, feature selection, and iterative mining.
