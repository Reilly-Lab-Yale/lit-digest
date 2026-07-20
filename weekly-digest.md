# Reilly Lab Lit Digest

A weekly scan of new and exciting papers, synthesized for your easy digestion. Just drop a paper in
slack or email it to me as a suggestion and it will get in here.

Sourced from: `#interesting_papers` `#interesting-papers_evolution` `#joint-jax-yale` `#longevity-consortium` `#talks` `#xspecies-modeling` `#ukbb_crispri`

---

## 🎉 Hot off the press — from the Reilly Lab!

1. **The Encyclopedia of DNA Elements** (first: ENCODE Project Consortium; senior: T. Reddy; *bioRxiv* 2026.07.06.731365, July 8 2026).
   - ENCODE's **capstone reference map** of genome regulation â 20+ years distilled into **>16,000 genome-wide experiments**, predominantly in **primary cells and tissues**.
   - Regulatory-element catalog anchored on **5.3 million DNase I hypersensitive sites** (essentially all accessible regulatory DNA), plus chromatin states, TF occupancy, nascent transcription, and **predicted functional consequences of non-coding variants**.
   - Expanded gene catalog: **~18,000 novel human lncRNA genes, ~150,000 novel transcript isoforms**, and transcript-stability maps across cell types/time.
   - Maps **regulatory-element ↔ gene interactions across >100 human tissues/cell lines at up to 10 bp resolution** (a vast loop-anchor network), plus parallel **mouse** developmental maps.
   - **Reilly Lab contribution:** as an **ENCODE Functional Characterization Center** (with the Sabeti & Tewhey labs), the lab supplies **MPRA + non-coding CRISPR** functional testing of candidate elements — the "does it actually regulate?" layer behind the catalog. (Full consortium author list not enumerable this run; credited at lab level.)
   👥 Reilly Lab: Steve Reilly
   https://www.biorxiv.org/content/10.64898/2026.07.06.731365v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/07/08/2026.07.06.731365/F1.large.jpg)

2. **Long-term isolation and archaic introgression shape functional genetic variation in Near Oceania**
   (first: P. Reilly; senior: S. Tucci; *Science* adr6749, June 11 2026).
   - **177 new high-coverage Near Oceanian genomes** across 12 populations, analyzed alongside 1,284
     worldwide genomes — a major fill of a long-underrepresented region.
   - Ancestors of Near Oceanians interbred with **at least three distinct Denisovan-related groups**.
   - **The lab's MPRA functionally tested the archaic variants — 3,100+ that alter gene expression** —
     moving from "resurrecting" archaic DNA to showing it actively switches genes on and off.
   - Adaptive archaic variants are **enriched in the interferon-γ antiviral immune pathway**.
   - A Denisovan-derived **TRPS1** variant ties to **skeletal development**, echoing recurrent local
     adaptation in other global populations.
   👥 Reilly Lab: Steve Reilly, Jared Akers | alumni: Stephen Rong, Maggie Prentice
   https://www.science.org/doi/10.1126/science.adr6749
   ![fig](https://news.yale.edu/sites/default/files/styles/opengraph_image/public/2026-06/YN_world-map-genome-pacific.jpg?h=b1877eb9&itok=BwVxBfsQ)

---

## Week of 2026-07-20

1. **An encyclopedia of human enhancer–gene regulatory interactions** (first: Gschwind; senior: Engreitz; *Nature*, July 15 2026).
   - Builds **ENCODE-rE2G**, a predictive model of enhancer-gene regulation trained on the largest benchmark to date: **10,356 CRISPR-perturbation element-gene pairs**, **30,000+ fine-mapped eQTLs**, and **569 fine-mapped GWAS variant-to-gene links**.
   - Applies the model genome-wide to build an **encyclopedia of >92 million enhancer-gene interactions** across **1,458 biosamples / 369 cell types and tissues**.
   - Beyond enhancer activity and 3D contact frequency, **promoter class and enhancer-enhancer synergy** turn out to matter for whether an enhancer actually drives its target gene.
   - Not a Reilly-authored paper, but a direct ENCODE4 companion resource to last week's ENCODE flagship — the Reilly Lab's own MPRA/CRISPRi perturbation data (as an ENCODE FCC) is the same kind of data this model is trained and benchmarked on.
   - Shared independently in two channels by Thanh-Thanh Nguyen ("this is out!").
   Shared `#interesting_papers` `#ukbb_crispri`.
   https://www.nature.com/articles/s41586-026-10781-4
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41586-026-10781-4/MediaObjects/41586_2026_10781_Fig1_HTML.png)

2. **Intrinsic promoter responsiveness dictates sensitivity to transcriptional activation by enhancers** (first: Tan; senior: Engreitz; *bioRxiv* 2026.06.25.734173, June 26 2026).
   - Compares **six reporter-assay designs** across **25,000 enhancer-promoter pairs**, finding that assay architecture itself biases measured enhancer-promoter "compatibility."
   - After removing those confounders, promoters differ **>100-fold** in intrinsic responsiveness to enhancer activation, while enhancers activate all promoters in a **similar rank order**.
   - Promoter output scales with enhancer activity via a **power law with a promoter-specific exponent**, modulated by core-promoter TF motifs — adding this exponent to the Activity-by-Contact model improves prediction of which genes are "skipped" by enhancers.
   - Flags a specific confound directly relevant to our own MPRA constructs: **upstream reporter designs can let the CRE initiate its own transcription** instead of the intended promoter, contaminating the measured signal — Grace Oualline and Mackenzie Noon cross-checked this against Reilly-Tewhey MPRA data and found the signal "seemed overwhelmingly promoter-like."
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.64898/2026.06.25.734173v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/06/26/2026.06.25.734173/F1.large.jpg)

3. **EpiBinder: a multimodal framework for cell-type-specific prediction and interpretation of transcription factor binding** (first: Solozabal; senior: Afek; *bioRxiv* 2026.07.06.736502, July 6 2026).
   - Adds **base-resolution DNA methylation + chromatin accessibility** as input modalities to a deep-learning TF-binding model, on top of sequence.
   - Improves TF-binding prediction by **up to 10% AUPRC** over sequence-only baselines across multiple human cell lines.
   - Produces **base-level attribution maps** flagging candidate methylation-sensitive binding sites and TF-TF dependencies.
   - Discovered-pass hit against the sequence-to-function watch-topic — relevant to adding epigenetic context to `malinois-coda`/`mpac`-style CRE activity models to resolve cell-type-specific ambiguity.
   https://www.biorxiv.org/content/10.64898/2026.07.06.736502v1

---

## Week of 2026-07-13

1. **Immune context unmasks regulatory effects of Neanderthal and Denisovan introgression** (first: unknown; senior: unknown; *bioRxiv* 2026.05.29.727880, 2026).
   - An **MPRA of archaic-introgressed variants** (Neanderthal + Denisovan) testing allele-specific regulatory activity of introgressed sequence.
   - Central claim in the title: an **immune / activated cell context "unmasks" regulatory effects** that are invisible at baseline — many archaic alleles are regulatory **only in a stimulated state**.
   - Implication: **context-dependent** reporter assays recover **adaptive-introgression regulatory function** that resting-state MPRA misses — a design lesson for the lab's own introgression + single-cell MPRA work.
   - Surfaced while auditing papers affected by the **mpraflow / MPRAnalyze** bug, so worth reading with that caveat in mind.
   - ⚠ First/senior authors unresolved this run (v1 not yet indexed; no browser to render the bioRxiv page) — verify before citing.
   Shared `#interesting-papers_evolution`.
   https://www.biorxiv.org/content/10.64898/2026.05.29.727880v1

2. **Genome-wide absolute quantification of chromatin looping** (first: Jusuf; senior: Hansen; *Nature Structural & Molecular Biology*, 2026).
   - **Calibrates Micro-C against live-imaging** to convert contact frequencies into **absolute looping probabilities** across 65,929 loops genome-wide.
   - Loops are **rare**: mean pairwise looping probability **~1.2%**, maximum **~25%** — the looped state is the exception, not the rule.
   - **CTCF–CTCF loops (~2.2%) are stronger than cis-regulatory loops (<1%)**, reframing enhancer–promoter "loops" as **transient, low-probability** contacts.
   - A useful quantitative prior for **3D-genome / cross-species modeling** (why it was flagged in `#xspecies-modeling`).
   Shared `#xspecies-modeling`.
   https://www.nature.com/articles/s41594-026-01819-2
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41594-026-01819-2/MediaObjects/41594_2026_1819_Fig1_HTML.png)

## Week of 2026-07-05

1. **Somatic cancer variants enriched in Alzheimer's disease microglia-like cells drive inflammatory and proliferative states** (first: Huang; senior: Walsh; *Cell*, 2026).
   - **Classic cancer-driver somatic mutations accumulate in microglia** in Alzheimer's disease brains, without producing cancer.
   - Mutant microglial clones are **selected for survival and proliferation**, creating a persistent **inflammatory niche**.
   - The resulting chronic inflammation plausibly **kills neighboring "bystander" neurons**, linking clonal somatic selection to neurodegeneration.
   - Extends the somatic-mosaicism-as-disease-driver logic from neurons to **glia** — directly adjacent to the lab's own somatic-mosaicism work.
   Shared `#interesting_papers`.
   https://www.cell.com/cell/fulltext/S0092-8674(26)00341-7

2. **ATLAS — population-level disease locus discovery via differential attention in genomic language models** (first: unknown; senior: unknown; *bioRxiv* 2026.02.09.704696, February 2026).
   - Compares **attention patterns from a pretrained genomic language model** between disease and control cohorts to localize disease loci **without variant calling or supervised training**.
   - Gene-level differential attention prioritizes candidates; a base-level pass **localizes signal to single-haplotype resolution**.
   - Validated on synthetic data and a **β-thalassemia cohort**; recovers known loci with **higher recall than GWAS** at low allele frequencies (down to 10%) and small cohort sizes (<200/group).
   - An unsupervised alternative to MPAC-style variant-effect prediction, worth tracking for rare-variant/small-cohort settings.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.64898/2026.02.09.704696v1

## Week of 2026-06-28

_Quiet curated week (no new shares in the paper channels); both entries are from the weekly discovered-pass scan._

1. **Modeling cis-regulatory variation in human brain enhancers across a large Parkinson's Disease cohort** (first: Sigalova; senior: Aerts; *bioRxiv* 2026.03.15.711881, v2 2026).
   - **190 human donors (115 control, 75 Parkinson's):** long-read whole-genome sequencing + single-nucleus multiome of **anterior cingulate cortex and substantia nigra**.
   - **Cell-type-aware sequence-to-function deep-learning** predicts chromatin accessibility, then **scores how variants perturb enhancer activity** in each brain cell type.
   - Nominates **53,841 high-confidence cis-acting variants** that modulate **cell-type-specific enhancer accessibility**.
   - Closest external template for the **brain-cell-type MPRA atlas + MPAC**: the same "**predict accessibility, then score the variant**" logic, run in disease-relevant brain regions.
   - Direct hook for the lab's **PD / immune MPRA** thread — an orthogonal, model-based prioritization of Parkinson's regulatory variants to cross against MPRA allelic skews.
   https://www.biorxiv.org/content/10.64898/2026.03.15.711881v2
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/04/16/2026.03.15.711881/F1.large.jpg)

2. **BlueSTARR — deep-learning models of gene-regulatory perturbations from whole-genome reporter assays** (first: Majoros; senior: Reddy; *bioRxiv* 2026.03.27.714770, March 31 2026).
   - **BlueSTARR** is a retrainable framework trained on **whole-genome STARR-seq** (two cell lines + one drug treatment) to **prioritize variants never directly assayed**.
   - Turns a genome-scale reporter assay into a **variant-effect predictor** — the **train-on-reporter-data-then-predict** logic that underlies **MPAC**.
   - Recovers a genome-wide signature of **purifying selection against both loss- and gain-of-function** regulatory variants.
   - The **gain-of-function** signal is biased toward selection against **new cis-regulatory activity in closed chromatin proximal to genes** — i.e. the genome resists switching quiet regions on.
   - Supplies a **selection-aware prior** for ranking extreme-effect regulatory variants, complementing FLARE and the complex-trait-tails work digested last week.
   https://www.biorxiv.org/content/10.64898/2026.03.27.714770v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/03/31/2026.03.27.714770/F1.large.jpg)

## Week of 2026-06-24

1. **FLARE — common vs. rare noncoding variant effects across cellular contexts** (first: Marderstein;
   senior: Montgomery; *Nature Genetics*, June 15 2026).
   - **Common variants act cell-type-specifically**, while **ultra-rare variants have larger, broader effects**.
   - Built from **~3 billion deep-learning chromatin-accessibility predictions**.
   - Strongest **purifying selection falls in fetal neurons**.
   - Adds **evolutionary constraint** to prioritize extreme-effect noncoding variants.
   - Closest external analog to **MPAC + the brain-cell-type MPRA atlas** — a **frequency-by-effect hypothesis** our allelic skews can test.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41588-026-02619-6
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41588-026-02619-6/MediaObjects/41588_2026_2619_Fig1_HTML.png)

2. **Global map of introgressed structural variation and selection** (first: Hsieh; senior: Eichler;
   *Science* adz7518, June 11 2026; PMID 42275491).
   - First **genome-wide catalog of archaic-introgressed SVs (≥50 bp)** across populations.
   - **Papua New Guineans carry the largest burden**, and a subset is **under selection**.
   - The **structural-variant complement** to our SNP/MPRA Near-Oceania work (adr6749).
   - Obvious integration: **intersect introgressed SVs with our archaic emVars**.
   Shared `#interesting-papers_evolution`.
   https://www.science.org/doi/10.1126/science.adz7518
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2025/06/24/2025.06.24.661368/F1.large.jpg)

3. **Distinct genetic architecture in the tails of complex traits** (first: Souaiaia; senior: O'Reilly;
   *Nature*).
   - Across **74 traits**, the **extreme tails depart from common-variant polygenicity**.
   - Adding **rare variants closes the gap** → **rare large-effect alleles drive the tails**.
   - A **frequency-stratified echo of FLARE** (rare = large effect).
   - Reinforces why **MPRA should prioritize rare / extreme regulatory variants**.
   - Discussed at **JAX–Yale journal club, June 25** (Tian Xia).
   https://www.nature.com/articles/s41586-026-10516-5
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41586-026-10516-5/MediaObjects/41586_2026_10516_Fig1_HTML.png)

4. **Derivation of elephant induced pluripotent stem cells** (first: Appleton; senior: Hysolli;
   *Nature Methods*).
   - First **elephant induced pluripotent stem cells (emiPSCs)**.
   - Achieved only by **suppressing the expanded TP53 retrogenes** behind elephant cancer resistance (**Peto's paradox**).
   - A tractable **in-vitro model** for the Longevity Consortium's **long-lived-species / comparative-regulation** arm.
   Shared `#longevity-consortium` + `#interesting_papers`.
   https://www.nature.com/articles/s41592-026-03136-4
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41592-026-03136-4/MediaObjects/41592_2026_3136_Fig1_HTML.png)

5. **Plasma proteomic signatures of cellular aging predict disease** (first: Ding; senior: Wyss-Coray;
   *Nature Medicine*).
   - ML on **>7,000 plasma proteins in 60,542 people**.
   - Yields **cell-type-specific aging clocks spanning 40+ cell types**.
   - The clocks **forecast incident disease**.
   - Consortium-adjacent context for **why cell-type resolution matters in aging** (watch-level).
   Shared `#longevity-consortium`.
   https://www.nature.com/articles/s41591-026-04446-y
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41591-026-04446-y/MediaObjects/41591_2026_4446_Fig1_HTML.png)

---

## Week of 2026-06-15

1. **SPROUT — steered plant promoter editing via rollout-guided edit flows** (first: anonymous;
   senior: anonymous; OpenReview 2026).
   - **Inference-time steering** applied to a pre-trained Edit Flow sequence model.
   - Uses **rollout-estimated utility** to tilt generation toward target **plant promoter activity**.
   - Not human CREs — but **inference-time goal-directed control of a pretrained generative model is directly applicable to CODA/Malinois**.
   - Shared by Mackenzie Noon. **⚠ VERIFY** (conference preprint, may be anonymous at this stage).
   Shared `#interesting_papers`.
   https://openreview.net/pdf?id=4AF7WSp7Cs

2. **MPRabc — MPRA-informed modeling of context-specific enhancer-gene interactions** (first: DeGroat;
   senior: Kreimer; *Nucleic Acids Research* 54:10, June 2026).
   - Integrating **MPRA-measured enhancer activity as a feature** sharply improves enhancer-gene link prediction across cell contexts.
   - Key point: **MPRA activity is a training signal, not just a validation step**.
   - Implies our **scMPRA and variant-MPRA outputs could power interaction atlases** for specific brain cell types.
   https://www.biorxiv.org/content/10.64898/2026.05.01.722242v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/05/05/2026.05.01.722242/F1.large.jpg)

3. **EnhancAR — evolutionarily-conditioned generation of functionally diverse enhancers** (first: Duncan;
   senior: Lu; bioRxiv, April 2026).
   - Autoregressive model trained on **1.7M human enhancer homolog sets**.
   - Learns **functional grammar from conservation**; generates novel enhancers **without per-cell-type MPRA labels**.
   - A **different generative prior than CODA**: evolution as the conditioning signal.
   - **Scales to cell types lacking MPRA data** — a possible complement for brain subtypes outside the Pew atlas.
   https://www.biorxiv.org/content/10.64898/2026.04.13.718170v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/04/15/2026.04.13.718170/F1.large.jpg)

4. **TRACE — ARG-based detection of archaic introgression without archaic genomes** (first: Zhang;
   senior: Moorjani; bioRxiv, March 2026).
   - Detects **archaic introgression from inferred ARGs alone** — no archaic genomes or unadmixed outgroups needed.
   - Recovers known Neanderthal/Denisovan signal and reveals **ghost admixture from uncharacterized hominins**.
   - In Oceanians, confirms **Denisovan enrichment consistent with super-archaic gene flow** — overlaps our Near Oceania paper.
   - **Orthogonal to haplotype-matching**; useful for refining Oceanian introgression maps.
   https://www.biorxiv.org/content/10.64898/2026.03.03.709416v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/03/04/2026.03.03.709416/F1.large.jpg)

5. **Genetic background shapes AI-predicted variant effects** (first: Schilder; senior: Koo; bioRxiv,
   April 2026).
   - The **pVEP framework**: the same clinical variant is predicted **pathogenic in some haplotype backgrounds, benign in others**.
   - Holds across deep-learning models for **protein structure, splicing, and noncoding regulation**.
   - Caution for MPAC: **allelic-effect predictions should account for background sequence context**, not just the focal variant.
   - **⚠ VERIFY** full results.
   https://www.biorxiv.org/content/10.64898/2026.04.04.715328v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/04/07/2026.04.04.715328/F1.large.jpg)

---

## Week of 2026-06-10

1. **PARM — regulatory grammar of human promoters from MPRA-trained deep learning** (first:
   Barbadilla-Martínez; senior: van Steensel; *Nature* 2026, NKI).
   - Small, cheap-compute **CNN trained on promoter MPRAs** predicts autonomous promoter activity genome-wide.
   - Learns **interpretable TF-motif grammar** in its layers.
   - **Designs synthetic strong promoters**.
   - An **independent promoter-side analogue to Malinois/CODA** and a benchmark for our enhancer-design models.
   https://www.nature.com/articles/s41586-025-10093-z
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41586-025-10093-z/MediaObjects/41586_2025_10093_Fig1_HTML.png)

2. **sc-lentiMPRA of synthetic enhancers: motif-affinity encoding of cell-type specificity** (first:
   Rühle; senior: Velten; bioRxiv 2026-02-27).
   - Single-cell lentiMPRA over **~160 affinity-controlled synthetic enhancers in ~190k cells**.
   - **Low-affinity motifs track TF level near-linearly**; **high-affinity motifs saturate / buffer**.
   - I.e. **motif affinity is a tunable knob** for graded cell-type specificity — exactly the lever CODA needs.
   https://www.biorxiv.org/content/10.64898/2026.02.27.708495v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/03/02/2026.02.27.708495/F1.large.jpg)

3. **Predicting non-coding variant effects with AlphaGenome** (first: Murphy; senior: Koo; *Cell Research*
   2026, Research Highlight).
   - Highlight of the **AlphaGenome long-range foundation model**.
   - Predicts variant effects well for **large, local signals** but **fails on subtle and distal effects**.
   - That gap is **exactly where MPRA / MPAC add orthogonal value** — a good citation for why experimental validation stays necessary.
   https://www.nature.com/articles/s41422-026-01249-1
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41422-026-01249-1/MediaObjects/41422_2026_1249_Fig1_HTML.png)

4. **Effects of introgressed Neanderthal alleles on present-day brain morphology** (first: Zeloni;
   senior: Marnetto; bioRxiv 2026-04-14).
   - Surviving **archaic alleles associate with brain-imaging phenotypes** despite genome-wide depletion of archaic ancestry in functional regions.
   - **Phenotype-anchored introgressed regulatory variants** — natural MPRA targets.
   - Bridges our **introgression and brain-MPRA threads**.
   https://www.biorxiv.org/content/10.64898/2026.04.14.718380v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/04/14/2026.04.14.718380/F1.large.jpg)

5. **Single-cell multiomics across nine mammals: cell-type regulatory conservation in the brain** (first:
   Anderson; senior: Cochran; bioRxiv 2025-08-06).
   - **Nine-species snRNA + snATAC atlas** scores cCRE conservation per cell type.
   - **Validates with MPRA in human neural cells**.
   - The **template the lab's Longevity Consortium cross-species work** is building toward; a precedent for the Pew brain atlas.
   https://www.biorxiv.org/content/10.1101/2025.08.06.668931
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2025/08/06/2025.08.06.668931/F1.large.jpg)

6. **Cross-species enhancer-AAV toolkit for cell-type-specific access** (first: Wirthlin; senior: Ting;
   bioRxiv 2026-02-23).
   - **Enhancer-driven AAVs that keep cell-type specificity across species**.
   - The **delivery end of the CODA thesis**.
   - A **benchmark / comparator for the Pew gene-therapy aim**.
   https://www.biorxiv.org/content/10.64898/2026.02.23.706695v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/02/24/2026.02.23.706695/F1.large.jpg)

> Note (2026-06-10): a 7th candidate shared in `#longevity-consortium_p2_internal`
> (`biorxiv.org/.../2026.04.07.717039v2`) could not be verified — left in the inbox as `⚠ VERIFY`.
