---
layout: page
title: Breast Cancer Epigenomics
description: Are benign tissues truly normal epigenetically?
img: assets/img/sample_location_diagram.jpg
importance: 1
category: work
---

#### The Big Picture 

How does DNA methylation—a critical epigenetic process—shape breast cancer development? Tumor-adjacent "normal" (AN) tissue often acts as a reference point for studying cancer-related changes, but is it truly normal? Could these epigenetic profiles hint at cancer predisposition, or are they altered in response to the tumor itself?

#### What We Did

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sample_location_diagram.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

To find answers, I studied DNA methylation across a "tumor proximity axis" (TPxA):

1. Healthy Donated Breast (HDB) – Samples from cancer-free donors.
2. Contralateral Unaffected Breast (CUB) – Tissue farthest from the tumor.
3. Ipsilateral Opposite Quadrant (OQ) – Tissue closer to the tumor, but not adjacent.
4. Tumor-Adjacent Normal (AN) – Tissue right next to the tumor.
5. Tumor (TU) – Cancer tissue itself.

Using Illumina’s Methylation EPICv1.0 BeadChip, methylation profiles were assayed for over 850,000 CpGs across the genome for 446 breast tissue samples from 251 women.

#### What We Found

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/dml_sankey.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

DNA methylation revealed striking relationships between the normal tissue categories:

1. Tumor vs. Normal Tissues: Expectedly, tumors had unique methylation profiles that stood apart from all normal tissues.
2. Case-Benign Tissues : Case-benign tissues (normal tissues from cancer patients) were quite similar to each other, regardless of their location.
3. Case-Benign vs. Healthy Donated Breast: Methylation profiles of case-benign tissues were highly distinct from healthy donor tissue, with their differences pointing towards hormone-receptor pathways.

#### What This Means

* Tumor-adjacent "normal" tissue isn’t normal—it shares epigenetic features with cancer.
* Benign tissues may carry early, systemic epigenetic changes linked to cancer predisposition.

#### Why It Matters

* If the clear patterns we see in case-benign tissue truly represents cancer predisposition, this means that epigenetic markers have a strong potential for being used as risk markers.
* This study informs future research in their selection of the reference tissue, depending on their research question. 

#### Challenges & What I Learned

One of the biggest challenges of this project was the analysis design. Having 5 categories of tissues, there are technically 10 different binary comparisons that you could make. We tried many different comparisons and eventually landed on the TPxA, but even then, we had to look at "differences of differences" sometimes to really get to what was happening in our data.


