---
layout: page
title: Bioinformatic analyses
permalink: /bioinformatic-analyses/
nav: true
nav_order: 2
display_categories: []
horizontal: false
---
<div class="container">
<div class="row">
<div class="col-4">
{% include figure.html loading="eager" path="assets/img/97da0295-a339-4e00-aa3f-1fd9cc130ce3_182418261.png" title="Portfolio illustration" class="img-fluid rounded z-depth-1" %} 
</div>
<div class="col-8">
<p>
This portfolio presents a selection of bioinformatic methods I routinely use. While this list reflects my current expertise, I can also implement new analyses upon request, provided that relevant R packages or Python libraries are available.
</p>
<p>
For questions or collaboration inquiries, you can reach me using the links in the navigation bar of the <a href="mailto:jviot@chu-besancon.fr">Contact</a> section.
</p>
<p>
Currently under construction, the various analyses will be progressively completed.
</p>
</div>
</div>
</div>

To support computationally intensive projects, I have access to the <a href="https://meso.univ-fcomte.fr/" target="_blank" rel="noopener noreferrer">Mésocentre de Franche-Comté</a> supercomputing facilities. This includes high-memory nodes (up to 1TB RAM) for large-scale data processing (e.g., expression matrices with millions of cells) and Nvidia A100 40GB GPUs for machine learning and AI model training and inference (e.g. bioinformatic algorithms implemented in Python taking advantage of GPU-accelerated computing).

With a strong background in cancer research and bioinformatics, I specialize in analyzing complex biological datasets to uncover insights into breast, lung, and colorectal cancers. Below are my key areas of expertise, ranging from well-established skills to exploratory techniques in genomics, transcriptomics, and computational biology.

<div class="expertise-section">
    <h2>Areas of Expertise</h2>

<div class="expertise-title">Significant Experience</div>
<ul>
<li><strong>Transcriptomics (Bulk RNA-seq):</strong> RNA-seq alignment (genome-based or pseudo-alignment), transcript or gene counting, and analysis.  ref(<a href="https://jviot.github.io/publications/#retrovirus">1</a>, <a href="https://jviot.github.io/publications/#esr1">2</a>, <a href="https://jviot.github.io/publications/#transipedia">3</a>, <a href="https://jviot.github.io/publications/#pan-cancer">4</a>, <a href="https://jviot.github.io/publications/#cd226">5</a>, <a href="https://jviot.github.io/publications/#fibroblast">6</a>)</li>
<li><strong>Differential Gene Expression Analysis</strong>  ref(<a href="https://jviot.github.io/publications/#retrovirus">1</a>, <a href="https://jviot.github.io/publications/#esr1">2</a>, <a href="https://jviot.github.io/publications/#transipedia">3</a>, <a href="https://jviot.github.io/publications/#pan-cancer">4</a>, <a href="https://jviot.github.io/publications/#cd226">5</a>, <a href="https://jviot.github.io/publications/#fibroblast">6</a>)</li>
<li><strong>Pathway Enrichment Analysis</strong>  ref(<a href="https://jviot.github.io/publications/#retrovirus">1</a>, <a href="https://jviot.github.io/publications/#esr1">2</a>, <a href="https://jviot.github.io/publications/#transipedia">3</a>, <a href="https://jviot.github.io/publications/#pan-cancer">4</a>, <a href="https://jviot.github.io/publications/#cd226">5</a>, <a href="https://jviot.github.io/publications/#fibroblast">6</a>)</li>
<li><strong>Immune Deconvolution</strong>  ref(<a href="https://jviot.github.io/publications/#retrovirus">1</a>, <a href="https://jviot.github.io/publications/#cd226">5</a>)</li>
<li><strong>Transposable Elements (with a focus on Endogenous Retroviruses)</strong>  ref(<a href="https://jviot.github.io/publications/#retrovirus">1</a>)</li>
<li><strong>Biostatistics and Modeling (Machine Learning)</strong>  ref(<a href="https://jviot.github.io/publications/#retrovirus">1</a>)</li>
</ul>

<div class="expertise-title">Limited/Exploratory Experience</div>
<ul>
<li><strong>Transcriptomics (Single-cell RNA-seq):</strong> Alignment and analysis (Seurat)</li>
<li><strong>Metabam and IGV Visualization</strong></li>
<li><strong>Genome Browser</strong></li>
<li><strong>ATAQ-seq</strong></li>
<li><strong>Bisulfite-seq</strong></li>
<li><strong>Proteomics (PepQuery)</strong></li>
<li><strong>DNA-seq:</strong> Variant calling, copy number variation, genomic signatures</li>
<li><strong>Fusion Transcripts</strong></li>
<li><strong>Digital Pathology (QuPath)</strong></li>
</ul>
</div>


<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
