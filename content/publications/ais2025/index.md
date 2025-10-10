---
title: 'A Quantitative Method for Running Deviation Based on State Space Reconstruction'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Hanjun Li

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'

date: '2025-10-09T00:00:00Z'

# Schedule page publish date (NOT publication's date).
publishDate: '2025-10-09T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *3rd conference on Artificial Intelligence in Sports*
publication_short: In *AIS*

abstract: This study developed a novel quantitative method using nonlinear dynamic analysis and state space reconstruction to analyze running movement patterns. Laminarity and correlation dimension effectively distinguished Patellofemoral Pain Syndrome patients from healthy controls, validating nonlinear indices for injury risk identification.

# Summary. An optional shortened abstract.
summary: This study developed a novel quantitative method using nonlinear dynamic analysis to analyze running movement patterns.

tags:
  - Running Injury

# Display this page in the Featured widget?
featured: true

# Standard identifiers for auto-linking
# hugoblox:
#   ids:
#     doi: 10.5555/123456

# Custom links
links:
  # - type: pdf
  #   url: ""
  # - type: code
  #   url: https://github.com/HugoBlox/hugo-blox-builder
  # - type: dataset
  #   url: https://github.com/HugoBlox/hugo-blox-builder
  # - type: slides
  #   url: https://www.slideshare.net/
  # - type: source
  #   url: https://github.com/HugoBlox/hugo-blox-builder
  # - type: video
  #   url: https://youtube.com

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
## Introduction

 As a popular form of exercise, lower limb injuries associated with running have received increasing attention. Traditional paradigms of lower limb running injuries, such as the "impact force paradigm" and "excessive pronation paradigm," have been questioned due to their unclear relationship with injury risk and lack of epidemiological support. In recent years, the "Habitual Motion Path" (HMP) paradigm has been proposed, emphasizing that runners follow a specific, habitual movement trajectory when performing certain tasks, which is considered the path of least resistance for joint motion. However, existing research still faces challenges in quantifying HMP, and while the Run Signature series of methods provides a quantification approach, it has not yet gained widespread recognition in the academic community. This study aims to apply nonlinear dynamic analysis and clustering algorithms to quantify lower limb movement trajectory deviation, providing new evidence for the HMP hypothesis.

## Methods

This study included 53 participants (25 controls, 28 with Patellofemoral Pain Syndrome, PFP), with each participant completing tests under two footwear conditions using markerless motion capture with Qualisys video system and Theia3D software. Data collection included running kinematics at a fixed speed of 14 km/h under two footwear conditions, as well as squat movements performed by participants at comfortable posture and speed (HMP baseline data). After raw data preprocessing, nonlinear dynamic analysis was performed based on the nonlinearTseries package. Time delay parameters were determined using autocorrelation function (ACF) and average mutual information (AMI) methods, optimal embedding dimension was selected using the Cao algorithm, and state space reconstruction was performed on knee joint angle time series. Habitual motion path deviation indices (HMP_X_DIV, HMP_Y_DIV, HMP_Z_DIV), correlation dimension (corrDim function), sample entropy (sampleEntropy function), and 11 indices from recurrence quantification analysis (rqa function: REC, DET, LAM, ENTR, etc.) were calculated. Ward.D2 hierarchical clustering method was applied to group nonlinear indices, and independent sample t-tests were used to analyze between-group differences.

## Results

The main findings of this study are as follows (*p<0.05, **p<0.01): (1) A novel method based on nonlinear dynamic analysis and clustering algorithms was successfully developed, enabling quantitative analysis of lower limb movement trajectory deviation. (2) Habitual motion path deviation indices showed: X-axis deviation (PFP: 0.007±0.195 vs. CON: -0.022±0.214), Y-axis deviation (PFP: -1.446±3.073 vs. CON: -1.891±2.632), Z-axis deviation (PFP: -4.552±3.807 vs. CON: -4.624±3.961), with no statistically significant differences in all three dimensions (p>0.05), indicating no obvious systematic differences in three-dimensional knee joint trajectory deviation between the two groups. (3) System complexity indices indicated: correlation dimension (PFP: 1.311±0.078 vs. CON: 1.334±0.081, p=0.047*), sample entropy (PFP: 0.260±0.051 vs. CON: 0.273±0.057, p=0.077), with the control group showing significantly higher correlation dimension than the PFP group, while sample entropy showed marginally significant difference. (4) Recurrence quantification analysis revealed: recurrence rate REC (PFP: 0.0014±0.0007 vs. CON: 0.0015±0.0003, p=0.686), determinism DET (PFP: 0.993±0.005 vs. CON: 0.994±0.004, p=0.292), laminarity LAM (PFP: 0.694±0.236 vs. CON: 0.773±0.165, p=0.005**), where LAM showed the control group significantly higher than the PFP group, reflecting significant differences in movement trajectory laminarity characteristics between the two groups. (5) Other recurrence quantification analysis indices showed: RATIO (PFP: 788.74±278.10 vs. CON: 712.22±189.53, p=0.022) and Lmean (PFP: 21.68±13.58 vs. CON: 18.89±4.01, p=0.045) both showed the PFP group significantly higher than the control group, indicating that the PFP group exhibits different characteristics in the complexity of recurrence structure. (6) Clustering analysis based on nonlinear indices classified the 53 participants into three categories, with the distribution of PFP and control groups showing significant hierarchical patterns: Cluster 1 (CON: 60% vs. PFP: 40%), Cluster 2 (CON: 48.3% vs. PFP: 51.7%), Cluster 3 (CON: 10% vs. PFP: 90%), validating the effectiveness of nonlinear indices in distinguishing movement injury risk.

## Conclusion
This study provides an innovative method for quantitative analysis of lower limb movement trajectory deviation, which has important value for validating the HMP hypothesis and understanding lower limb injury mechanisms. The research conclusions indicate: (1) Nonlinear dynamic analysis indices based on the nonlinearTseries package can effectively distinguish PFP patients from healthy controls, with laminarity LAM being the most significant distinguishing index, with the control group significantly higher than the PFP group; correlation dimension also showed the control group higher than the PFP group, indicating that healthy individuals' movement patterns have higher determinism and structural characteristics; (2) RATIO and Lmean indices in recurrence quantification analysis showed the PFP group significantly higher than the control group, reflecting that PFP patients exhibit different dynamic characteristics in recurrence structure complexity; (3) Clustering analysis results showed significant hierarchical distribution characteristics, validating the effectiveness of nonlinear indices in identifying movement injury risk; (4) Habitual motion path deviation indices (HMP_DIV) did not reach statistical significance in all three dimensions, suggesting limited sensitivity of this index in detecting PFP movement pattern differences.