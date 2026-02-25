---
layout: page
title: HERV
img: assets/img/ERV.png
importance: 1
category: Projects
related_publications: false
---
# Analyse des rétrovirus endogènes (ERV) / Endogenous Retroviruses (ERV) Analysis

---

## <a id="fr"></a>🇫🇷 Version française

### **Contexte sur les ERV**
Les **rétrovirus endogènes (ERV)** sont des séquences virales intégrées dans le génome humain, issues d’infections rétrovirales anciennes (datant de millions d’années). Bien que généralement silencieux en raison de mutations ou de mécanismes épigénétiques (comme la méthylation de l’ADN), certains ERV conservent des capacités de transcription et peuvent s’exprimer dans des contextes pathologiques, notamment **dans le cancer**. Leur réactivation, souvent associée à une hypométhylation globale ou à des altérations épigénétiques, peut influencer la tumorigenèse via plusieurs mécanismes :
- Production de protéines virales **immunogènes**,
- Modulation de l’expression de gènes voisins,
- Promotion de l’**instabilité génomique**.

Dans mon **travail de thèse de sciences** sur les métastases hépatiques de cancers colorectaux, l’expression différentielle de certains ERV a été corrélée à des **signatures pronostiques**, suggérant leur rôle potentiel comme **biomarqueurs** ou **cibles thérapeutiques**. Leur étude ouvre des perspectives pour comprendre la plasticité tumorale et identifier de nouvelles stratégies immunothérapeutiques.
**Publication** : [PubMed (40381378)](https://pubmed.ncbi.nlm.nih.gov/40381378/).

---

### **Outils et méthodologies**
Pour caractériser l’expression et le rôle des ERV, nous avons combiné plusieurs approches :

1. **Analyse transcriptomique** :
   - **Bulk RNA-seq** et **single-cell RNA-seq** pour quantifier l’expression des ERV dans les échantillons tumoraux.
   - Correction des **alignements multiples** (fréquents avec les éléments transposables) via **[Telescope](https://github.com/mlbendall/telescope)**, un outil spécialisé pour désambiguïser les lectures issues de séquences répétitives.

2. **Validation protéomique** :
   - Évaluation de la **traduction des transcrits HERV** en protéines dans des échantillons de cancers colorectaux primitifs du **TCGA**, à l’aide de **[PepQuery](http://www.pepquery.org/)**, un outil basé sur la spectrométrie de masse.

---

[🇬🇧 English Version](#en) | [Retour en haut](#)

---

## <a id="en"></a>🇬🇧 English Version

### **Background on ERVs**
**Endogenous retroviruses (ERVs)** are viral sequences integrated into the human genome, originating from ancient retroviral infections (millions of years old). While typically silenced due to mutations or epigenetic mechanisms (such as DNA methylation), some ERVs retain transcriptional activity and can be expressed in pathological contexts, particularly **in cancer**. Their reactivation, often linked to global hypomethylation or epigenetic alterations, may influence tumorigenesis through multiple mechanisms:
- Production of **immunogenic** viral proteins,
- Modulation of neighboring gene expression,
- Promotion of **genomic instability**.

In my **PhD research** on colorectal liver metastases, the differential expression of specific ERVs was correlated with **prognostic signatures**, suggesting their potential role as **biomarkers** or **therapeutic targets**. Studying ERVs offers insights into tumor plasticity and may reveal new immunotherapeutic strategies.
**Publication**: [PubMed (40381378)](https://pubmed.ncbi.nlm.nih.gov/40381378/).

---

### **Tools and Methodologies**
To characterize ERV expression and function, we combined multiple approaches:

1. **Transcriptomic Analysis**:
   - **Bulk RNA-seq** and **single-cell RNA-seq** to quantify ERV expression in tumor samples.
   - Correction of **multi-mapping reads** (common with transposable elements) using **[Telescope](https://github.com/mlbendall/telescope)**, a tool designed to disambiguate repetitive sequences.

2. **Proteomic Validation**:
   - Assessment of **HERV transcript translation** into proteins in primary colorectal cancer samples from **TCGA**, using **[PepQuery](http://www.pepquery.org/)**, a mass spectrometry-based tool.

---
[🇫🇷 Version française](#fr) | [Back to top](#)
