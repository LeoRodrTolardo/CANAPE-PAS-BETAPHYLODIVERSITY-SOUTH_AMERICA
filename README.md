# South American Freshwater Fish Phylogenetic Diversity Analyses

This repository contains the scripts used to investigate patterns of evolutionary diversity in South American freshwater fish assemblages. The workflow integrates phylogenetic endemism analyses, conservation effectiveness assessments, and phylogenetic beta diversity approaches to identify river basins of evolutionary significance and evaluate their representation within protected area networks.

## Overview

Freshwater ecosystems harbor a substantial portion of global biodiversity and evolutionary history. Understanding the spatial distribution of unique evolutionary lineages is essential for developing conservation strategies that preserve both species richness and phylogenetic diversity.

This repository provides scripts for three complementary analyses:
1. **CANAPE** (Categorical Analysis of Neo- and Paleo-Endemism)
2. **Protected Area Effectiveness Assessment**
3. **Phylogenetic Beta Diversity Analysis**

Together, these approaches allow the identification of evolutionary hotspots, the evaluation of their conservation status, and the investigation of phylogenetic differentiation among river basins across South America.

---

## Analytical Framework

### 1. CANAPE Analysis
The CANAPE framework was used to identify river basins containing significant concentrations of geographically restricted evolutionary lineages.

This method classifies areas into distinct categories of evolutionary endemism:
* **Neo-endemism:** areas dominated by recently diversified lineages with restricted distributions.
* **Paleo-endemism:** areas containing ancient lineages with restricted distributions.
* **Mixed endemism:** areas exhibiting both neo- and paleo-endemism signals.
* **Super-endemism:** areas with exceptionally strong evolutionary endemism.

The results highlight river basins that represent important centers of evolutionary history and diversification.

---

### 2. Protected Area Effectiveness
To evaluate the conservation status of evolutionarily important basins, a protected area effectiveness analysis was performed.

The objective was to determine whether CANAPE-prioritized basins receive protection levels that differ from random expectations. The assessment considered two categories of protected areas:
* Strictly Protected Areas
* Sustainable Use Protected Areas

Observed protection levels were compared against null model simulations to quantify whether these basins are overrepresented or underrepresented within the South American protected area network.

---

### 3. Phylogenetic Beta Diversity
Phylogenetic beta diversity analyses were conducted to investigate evolutionary differentiation among river basins. The analyses partition phylogenetic dissimilarity into two major components:

#### Phylogenetic Turnover
Represents the replacement of evolutionary lineages among basins and indicates unique evolutionary composition.

#### Phylogenetic Nestedness
Represents situations in which assemblages constitute phylogenetic subsets of richer communities.

These components provide insights into the processes shaping the distribution of evolutionary diversity across South America.

---

## Repository Structure

```text
.
├── scripts
│   ├── CANAPE
│   ├── Protected_Area_Effectiveness
│   ├── Phylogenetic_Beta_Diversity
│   └── Auxiliary_Functions
│
├── data
│   ├── occurrence_data
│   ├── phylogenetic_tree
│   └── protected_areas
│
├── outputs
│   ├── maps
│   ├── figures
│   └── tables
│
└── README.md
```

---

## Data Requirements

To reproduce the analyses, the following datasets are required:
* Species occurrence matrix
* Phylogenetic tree (dated or ultrametric)
* River basin spatial boundaries
* Protected area spatial layers
* Environmental or geographic predictors (optional)

---

## Software Requirements

The analyses were developed in **R**. Main packages used throughout the workflow include:

```r
canaper
ape
picante
phyloregion
vegan
terra
sf
tidyverse
raster
```

*Additional package dependencies may be specified within individual scripts.*

---

## Workflow

* **Step 1 – Data Preparation**
  * Import species occurrence data.
  * Prepare phylogenetic trees.
  * Standardize taxonomic nomenclature.
  * Build basin-by-species matrices.

* **Step 2 – CANAPE Analysis**
  * Calculate phylogenetic endemism metrics.
  * Generate null models.
  * Classify river basins according to CANAPE categories.

* **Step 3 – Protected Area Assessment**
  * Overlay CANAPE results with protected area layers.
  * Calculate protection coverage.
  * Compare observed protection against null expectations.

* **Step 4 – Phylogenetic Beta Diversity**
  * Calculate pairwise phylogenetic dissimilarity.
  * Partition beta diversity into turnover and nestedness components.
  * Identify unique and redundant evolutionary assemblages.

* **Step 5 – Visualization**
  * Generate maps.
  * Produce summary tables.
  * Export publication-ready figures.

---

## Applications

Although developed for South American freshwater fishes, this workflow can be adapted to other taxonomic groups and geographic regions, including:
* Freshwater organisms
* Terrestrial vertebrates
* Plants
* Invertebrates
* Marine taxa

---

## Expected Outputs

The workflow generates:
* CANAPE classification maps
* Phylogenetic endemism metrics
* Protected area effectiveness statistics
* Phylogenetic turnover maps
* Nestedness maps
* Pairwise phylogenetic dissimilarity matrices
* Publication-ready figures and tables

---

## Contact

For questions, suggestions, bug reports, or collaborations, please open an **Issue** or a **Pull Request** in this repository.