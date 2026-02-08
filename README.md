# Competitive Pokémon TCG Data Mining
**CS 4412: Data Mining (Spring 2026)**

## Author
**Axel Alvarez**
* **Course:** CS 4412 - Data Mining
* **University:** Kennesaw State University

## Project Overview
This semester-long project applies data mining techniques to competitive Trading Card Game (TCG) tournament results. By analyzing thousands of deck lists from the Standard format, this project aims to:
1.  **Cluster** decks into mathematical archetypes (K-Means/DBSCAN).
2.  **Discover** core card engines vs. tech choices using Association Rules (FP-Growth).
3.  **Identify** rogue decks and statistical outliers in the metagame.

## Dataset Source
The data is sourced from the **Limitless TCG Public API**.
* **Source URL:** [https://play.limitlesstcg.com/api](https://play.limitlesstcg.com/api)
* **Description:** JSON data containing tournament standings and detailed card lists for players in major events.
