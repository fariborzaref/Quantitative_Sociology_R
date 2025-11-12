<!-- README.html for "Quantitative Sociology with R" -->

<h1>Quantitative Sociology with R</h1>
<p><strong>Instructor:</strong> Dr. Fariborz Aref</p>
<hr/>

<h3>Overview</h3>
<p>
  This repository accompanies the course <strong>Quantitative Sociology with R</strong>, a graduate and upper-undergraduate course integrating sociological theory with advanced statistical modeling.
  Students progress from conceptualizing inequality and structure to building fully reproducible R analyses and reports.
</p>

<hr/>

<h3>Course Objectives</h3>
<ul>
  <li>Translate sociological questions into measurable variables and statistical models.</li>
  <li>Master regression, GLM, GEE, HLM, and SEM using real-world social data.</li>
  <li>Apply visualization and interpretation techniques that communicate evidence clearly.</li>
  <li>Build reproducible pipelines using <strong>R Markdown / Quarto</strong>, <code>tidyverse</code>, and GitHub.</li>
  <li>Develop critical reasoning about data, bias, and theory.</li>
</ul>

<hr/>

<h3>Core Topics by Module</h3>
<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Week</th>
      <th>Theme</th>
      <th>Core Focus</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>1</strong></td>
      <td>Foundations of Sociological Data</td>
      <td>Tidy data, measurement, and validity</td>
    </tr>
    <tr>
      <td><strong>2</strong></td>
      <td>Descriptive Inequality</td>
      <td>Distributions, Lorenz &amp; Gini, visual storytelling</td>
    </tr>
    <tr>
      <td><strong>3</strong></td>
      <td>Regression Logic</td>
      <td>Model specification, interpretation, and causality</td>
    </tr>
    <tr>
      <td><strong>4</strong></td>
      <td>Generalized Linear Models</td>
      <td>Binary and count outcomes in social data</td>
    </tr>
    <tr>
      <td><strong>5</strong></td>
      <td>Hierarchical &amp; Longitudinal Models</td>
      <td>Individuals nested in contexts; HLM vs. GEE</td>
    </tr>
    <tr>
      <td><strong>6</strong></td>
      <td>Structural Equation Models</td>
      <td>Latent constructs, path diagrams, mediation</td>
    </tr>
    <tr>
      <td><strong>7</strong></td>
      <td>Visualization &amp; Reporting</td>
      <td><code>ggplot2</code>, marginal effects, coefficient plots</td>
    </tr>
    <tr>
      <td><strong>8</strong></td>
      <td>Replication &amp; Open Science</td>
      <td>Transparency, Quarto, GitHub publishing</td>
    </tr>
  </tbody>
</table>

<hr/>

<h3>🧪 Example: Multilevel Model</h3>
<pre><code>library(lme4)
library(performance)

# Two-level model: individuals nested within countries
model &lt;- lmer(inequality ~ education + income + (1 + income | country), data = oecd_panel)

summary(model)
performance::icc(model)
</code></pre>

<hr/>

<h3>📂 Repository Structure</h3>
<pre><code>Quantitative_Sociology_R/
├── Week01_Data/
├── Week02_Descriptive/
├── Week03_Regression/
├── Week04_GLM/
├── Week05_HLM_GEE/
├── Week06_SEM/
├── Week07_Visualization/
├── Week08_OpenScience/
└── Project_Replication/
</code></pre>

<hr/>

<h3>🔑 Key R Packages</h3>
<pre><code>library(tidyverse)
library(lme4)
library(geepack)
library(lavaan)
library(fixest)
library(marginaleffects)
library(modelsummary)
library(performance)
library(quarto)
</code></pre>

<hr/>

<h3>License &amp; Citation</h3>
<p>Educational use permitted under <strong>CC BY-NC 4.0</strong>.</p>
<blockquote>
  Aref, F. (2025). <em>Quantitative Sociology with R</em>. GitHub.
</blockquote>



