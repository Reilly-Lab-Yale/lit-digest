# Reilly Lab Lit Digest

A weekly scan of new and exciting papers, synthesized for your easy digestion. Just drop a paper in
slack or email it to me as a suggestion and it will get in here.

Sourced from: `#interesting_papers` `#interesting-papers_evolution` `#joint-jax-yale` `#longevity-consortium` `#talks` `#xspecies-modeling` `#ukbb_crispri` `lab DM` `discovered`

---

## Week of 2026-09-27

1. **The gene-regulatory evolution of the human skeleton** (first: Yan; senior: Gokhman; *Nature*, 23 September 2026).
   - An MPRA screen of **561,410 human-derived substitutions** in regulatory elements, identifying **15,077 with human-specific activity** — a scale that makes this the reference dataset for human-derived regulatory change, not a candidate-locus study.
   - Paired with **human–ape hybrid cells**, which control for trans background and isolate cis effects; these showed **widespread downregulation of glycosaminoglycan (GAG) biosynthesis genes**.
   - The molecular signal is corroborated at the tissue level: human cartilage shows a **three- to fourfold reduction in joint GAG content** versus non-human apes, consistent **across eight joint types** — a rare case of MPRA output matching a measured physiological phenotype.
   - The GAG pathway carries **signatures of selection**, concentrated in chondroitin sulfate biosynthesis, and the ***ACAN* GAG anchor repeats expanded uniquely in humans in two pulses** — two independent lines of evidence that this was selected, not drift.
   - The framing is a trade-off: reduced GAG aligns with human-specific skeletal morphology **and** with elevated susceptibility to degenerative joint disease such as osteoarthritis.
   - **Why it matters here:** this is the closest external analogue to the lab's own archaic/modern 3′UTR work — same logic (assay human-derived regulatory variants at scale, then find the pathway), but on coding-adjacent skeletal biology, and it demonstrates the hybrid-cell cis/trans control as a complement to MPRA. Directly relevant to `archaic-3utr-mpra` and a useful precedent for how to land a human-specific-regulation story in a general journal.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41586-026-11053-x
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41586-026-11053-x/MediaObjects/41586_2026_11053_Fig1_HTML.png)

2. **Massively parallel assessment of gene regulatory activity at human cortical-structure-associated variants** (first: Matoba; senior: Stein; *Nature Neuroscience*, 23 September 2026).
   - MPRA over **9,092 cortical-structure-associated variants in human neural progenitor cells** — the relevant cell state for cortical surface area, rather than a convenient immortalized line.
   - **918 variants across 150 loci showed regulatory activity (76% of loci tested)**, and **more than half showed allelic effects** — a high hit rate that argues the GWAS signal for brain structure is substantially regulatory.
   - The mechanistic surprise: **Alu elements drove most of the activity**, specifically **younger Alus retaining intact RNA Pol III A/B box promoter elements** — a transposable-element origin for cortical regulatory variation.
   - **Wnt stimulation changed regulatory activity at a subset of loci**, i.e. condition-dependent enhancers that a single-condition MPRA would score as inert — a direct argument for assaying perturbed states.
   - Regional specificity was explained by **transcription-factor expression**: variants disrupting a TF's binding site had stronger effects in brain regions expressing that TF more highly.
   - **CRISPRi validation at the *FOXO3* locus** tied the regulatory effect to cortical surface area, closing the loop from reporter to phenotype.
   - **Why it matters here:** this is `brain-celltype-mpra`'s nearest neighbour and a template for the MIND Prize logic — measure a cell state, find the state-dependent elements. The Wnt-dependence result in particular supports assaying **resting vs activated** states rather than one condition, which is exactly the homeostatic-vs-DAM design.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41593-026-02454-2
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41593-026-02454-2/MediaObjects/41593_2026_2454_Fig1_HTML.png)

3. **Mapping and rewiring the MYBPC3 promoter for rescue of haploinsufficiency driven hypertrophic cardiomyopathy** (first: Renberg; senior: Helms; *bioRxiv*, 22 September 2026).
   - **Saturation mutagenesis MPRA in human iPSC-derived cardiomyocytes** across the *MYBPC3* promoter, mapping the essential regulatory elements and the noncoding loss-of-function variants within them.
   - The therapeutic inversion is the interesting part: rather than correcting the mutant allele, they **engineer the promoter to raise expression of the remaining wild-type allele** — treating haploinsufficiency as a dosage problem solvable in *cis*.
   - Screening **thousands of sequence and TF-binding-site combinations** identified **synergistic edits** that robustly increase expression, i.e. the gains were combinatorial rather than additive single-site effects.
   - Presented as a **generalizable strategy for haploinsufficient disease**, not a one-locus result.
   - **Why it matters here:** this is promoter *engineering as therapy* with a Kundaje/Engreitz/Kitzman methods stack — the same design space as `locium-synthetic-promoters` and the MIND Prize Aim 1, but tuning a natural promoter instead of writing one de novo. The synergy finding is a caution for any additive model of designed elements.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.20.752987v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/09/22/2026.09.20.752987/F1.large.jpg)

4. **A single-nucleus multi-omic atlas of gene regulation across 21 adult human tissues** (first: Fan; senior: Ardlie; *bioRxiv*, 27 September 2026).
   - Joint transcriptome + chromatin accessibility on **459,856 single-nucleus profiles, 21 tissues, 4 donors**, resolved into **9 lineages, 61 broad cell types and 313 subclusters**.
   - Catalogues **>1 million candidate cis-regulatory elements, of which 161,270 were previously unidentified** — the incremental discovery is concentrated in cell types that bulk and single-modality atlases under-sample.
   - Links elements to genes with **871,177 cCRE–gene associations**, and uses these to **train predictive models of variant effect** — the atlas is built as model training data, not just a browser resource.
   - From the GTEx group, so tissue sampling and donor metadata are aligned with existing GTEx eQTL resources.
   - **Why it matters here:** a ready-made, cell-type-resolved training and evaluation substrate for `mpac` and for cross-species ATAC modelling — and the cCRE–gene links are the kind of ground truth that MPAC-style predictions are scored against. Worth checking the microglia/brain subclusters against the MIND Prize plan.
   - ⚠ Figures were **not yet rendered on bioRxiv** at retrieval time (posted one day before this run) — no `![fig]`; re-check on a later run.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.25.754561v1

5. **Genetic background shapes AI-predicted variant effects** (first: Schilder; senior: Koo; *bioRxiv*, 7 April 2026).
   - Introduces **pVEP (personalized variant effect predictor)** and asks a question most benchmarks skip: does the *same* variant get the *same* prediction on a different haplotype background?
   - Scale: ~**85,000 missense, splice-altering and UTR variants** evaluated across **3,891 human genomes** and millions of haplotypes, using deep-learning effect predictors.
   - The headline result is a reproducibility problem for variant annotation: **many clinical variants are predicted pathogenic on some genetic backgrounds and benign on others** — the prediction is a property of the haplotype, not the variant.
   - Mechanisms are named rather than left as noise: **shifts in protein contacts** and **changes in splice-site recognition** account for much of the background dependence.
   - The equity consequence is explicit — background-dependent annotation matters most for **genetically diverse populations**, who are furthest from the reference haplotype the models were tuned on.
   - **Why it matters here:** the protein-coding mirror of last week's Kreevan/Org non-additivity result, and the same warning for `mpac` and for ClinVar VUS work — a model scored on reference + single alternate allele is answering a narrower question than the clinical one. Note this is an **April preprint** surfaced by the lab this week, not a new posting.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.64898/2026.04.04.715328v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/04/07/2026.04.04.715328/F1.large.jpg)

6. **Autism genes converge on three functional programs organized by neuronal subclass, developmental timing, and cortical patterning** (first: Smith; senior: Gandal; *bioRxiv*, 24 September 2026).
   - Takes **253 autism-associated genes** and asks where in neurodevelopment they actually act, rather than stopping at the gene list.
   - Genetic burden **concentrates in temporally-resolved neuronal subclasses** — newborn excitatory neurons, immature interneurons, and maturing intratelencephalic lineages — so the signal is a developmental *window*, not a cell type alone.
   - Convergence onto **three programs**: gene regulation, neuronal morphogenesis, and synaptic transmembrane signalling, with **MEF2C, SOX11 and FOXP2** as regulatory hubs.
   - Risk genes show an **anterior-to-posterior cortical expression gradient anchored in visual cortex**, and clinical severity tracks the pattern of excitatory-neuron involvement.
   - **Why it matters here:** the gene-regulation program is the entry point for MPRA/CODA work in neural cell types, and the named TF hubs are concrete motif targets. Also directly adjacent to the somatic-mosaicism/ASD strand of the K99.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.22.753508v2
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/09/23/2026.09.22.753508/F1.large.jpg)

7. **Targeted single-nucleus sequencing of 39,800 neurons reveals extensive low-frequency somatic variants** (first: Bidhan; senior: Rademakers; *bioRxiv*, 23 September 2026).
   - **Single-nucleus amplicon sequencing of 39,800 neurons** from superior temporal gyrus, FTLD-TDP type C versus controls — depth chosen to reach mutation frequencies bulk sequencing cannot see.
   - Finds an extensive landscape of **ultra-low-frequency (<1%) somatic mutations** across FTLD-TDP-associated genes, with ***TARDBP* carrying the highest proportion of mutation-bearing neurons**.
   - Two counterintuitive observations drive the interpretation: somatic burden **decreased with age at death**, and the **C-terminal domain showed *lower* mutational frequency than other regions** despite being the disease-relevant domain.
   - The authors' resolution is selective loss — **neurons carrying damaging mutations are progressively lost before autopsy**, so what survives to be sequenced is a depleted, biased sample. That reframes any cross-sectional somatic-burden estimate in post-mortem brain.
   - **Why it matters here:** methodologically the closest published analogue to the somatic-mosaicism arm of the K99, and the survivorship-bias argument is one the K99 will need to address directly in its own design.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.21.753260v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/09/23/2026.09.21.753260/F1.large.jpg)

8. **Reference genomes and fossils revise bat family phylogeny and biogeography** (first: Morales; senior: Teeling; *Nature*, 23 September 2026).
   - **Chromosome-level long-read assemblies for 103 bat species, 42 of them new, covering all 21 bat families** — the assembly-quality jump is what lets the phylogeny be revised rather than re-litigated.
   - Resolves contested relationships: **Myzopodidae as the earliest branch within Vespertilionoidea**, and **Emballonuroidea and Vespertilionoidea as sister groups**; reconstructs **26 ancestral bat chromosomes**.
   - Explains *why* earlier studies disagreed — a **mosaic evolutionary history** across the genome, meaning single-locus or low-coverage approaches were sampling conflicting histories.
   - Integrating **699 morphological characters across 65 species including 44 pre-Quaternary fossils** with neutrally evolving genomic sites, fossilized birth–death and dispersal–extinction analyses place **bat origins — and thus powered flight — in Europe in the late Palaeocene**, refuting African and North American origins.
   - **Why it matters here:** shared in the Longevity Consortium channel as a consortium output. Beyond the phylogeny, this is a substantially upgraded comparative substrate for cross-species regulatory modelling — the kind of alignment backbone `#atac_prediction` and the Zoonomia-style work depend on, in a clade central to the longevity portfolio. **Not a Reilly-lab paper** — Reilly is not an author.
   Shared `#longevity-consortium_p2_internal`.
   https://www.nature.com/articles/s41586-026-11007-3
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41586-026-11007-3/MediaObjects/41586_2026_11007_Fig1_HTML.png)

---

## Week of 2026-09-20

1. **Massively parallel characterization reveals context-dependent and non-additive regulatory effects of closely spaced variant pairs** (first: Kreevan; senior: Org; *bioRxiv*, 11 September 2026).
   - An MPRA over **7,285 pairs of close-proximity SNVs** drawn from blood-specific and broadly active enhancers, with **all four haplotypes** of each pair assayed in K562 — the design that actually isolates joint effects rather than inferring them.
   - Pairs were enriched for function by requiring **at least one member to be an eQTLGen eQTL**, so this is not a random-variant survey.
   - **57% of pairs had at least one derived haplotype differing significantly from the ancestral haplotype**, and individual variant effects frequently **flipped sign depending on the neighbouring allele** — allelic background, not the variant alone, sets the effect.
   - In a high-confidence subset, **59% (105/178) of pairs were non-additive**, and **non-additive pairs sat closer together than additive ones** — a distance dependence, which is the mechanistic tell.
   - The dominant deviation is **sub-additive**: when both single-derived haplotypes raised activity, the double-derived haplotype came in **below the additive expectation**, consistent with saturation/redundancy rather than cooperativity.
   - **Why it matters here:** this is the empirical counterpart to the exact reviewer question live on MPAC this week (R1C9 — haplotypes with empirical activity but near-zero prediction). It supplies external evidence that non-additivity is common, distance-dependent and largely sub-additive, which is precisely the regime a model trained on reference + single-variant alternates cannot represent. Also a ready-made benchmark for haplotype-level variant-effect prediction.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.10.750584v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/09/11/2026.09.10.750584/F1.large.jpg)

2. **Estimating cis and trans contributions to differences in gene regulation** (first: Hallgrímsdóttir; senior: Pachter; *GENETICS*, 11 September 2026).
   - A statistical framework for splitting an expression difference between two strains or species into a **cis component (local, allele-linked)** and a **trans component (diffusible, acting on both alleles)**.
   - The identifying logic is the classic F1-hybrid contrast: **allele-specific expression in the hybrid isolates cis**, and the difference between the parental ratio and the hybrid ratio gives trans — this work is about estimating that decomposition properly rather than by ad-hoc ratios.
   - Demonstrated across **yeast, human–chimpanzee hybrid cells, and mouse datasets**, with the claim that it **outperforms the prior analyses of those same datasets** — i.e. the re-analysis changes conclusions, not just error bars.
   - **Why it matters here:** the cis/trans split is the hinge of cross-species regulatory work — an MPRA measures cis by construction, so knowing how much of a between-species expression difference is cis at all bounds what a reporter assay can ever explain. Directly relevant to the xspecies-modeling thread and to interpreting human–chimp regulatory divergence.
   - ⚠ VERIFY: advance-access article; metadata taken from Crossref (the OUP page is bot-gated), and no figure could be retrieved.
   Shared `#interesting_papers`.
   https://academic.oup.com/genetics/advance-article/doi/10.1093/genetics/iyag228/8790449

3. **Using sequence-to-function models to interpret archaic hominin introgression** (first: Comerford; senior: Gallego Romero; *bioRxiv*, 01 September 2026).
   - Applies **AlphaGenome to 144,139 introgressed SNPs** segregating in present-day Papuan-ancestry individuals — a population whose introgressed variation is badly under-represented in reference resources, which is the gap the paper is built around.
   - The headline result is a **split verdict**: **chromatin-accessibility predictions recapitulate experimentally observed effects, while gene-expression predictions perform no better than chance**.
   - Sharper still, predictions **correlate better with a reporter assay of single-variant activity than with the same variants' effects in live cells** — the model is capturing *regulatory potential* of a sequence, not its realized effect in native chromatin.
   - Tissue-specific predictions let them nominate affected tissues for introgressed haplotypes, and they flag **JAK1 and TAB2** as genes under haplotypes carrying an excess of high-impact accessibility variants.
   - The authors are explicit about the limits: **variant→target-gene assignment and expression prediction remain unsolved** for introgressed variation.
   - **Why it matters here:** a direct, sober benchmark of a frontier sequence-to-function model on the lab's own archaic-introgression problem — and the finding that predictions track MPRA-style episomal activity better than in-cell effects is an argument *for* the reporter-assay-grounded approach, not against it.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.08.31.748430v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/09/01/2026.08.31.748430/F1.large.jpg)

4. **Identifying human-specific transcription factor binding site gains and losses that contribute to human-specific phenotypes** (first: Ferrando-Bernal; senior: Capra; *bioRxiv*, 12 September 2026).
   - Predicts **TFBS gains and losses for 16,883 modern-human-specific high-frequency variants** — the variants fixed or near-fixed in humans but ancestral in Neanderthal, Denisovan and great apes.
   - Intersecting with experimentally annotated **cCREs yields 3,357 human-specific variants that alter a motif**, the tractable subset of an otherwise uninterpretable catalogue.
   - The prioritization move is the interesting one: keep variants where **the target gene and the disrupted transcription factor are independently associated with the same phenotype** — a convergence filter rather than a score threshold.
   - That yields **128 candidate regulatory variants across 155 genes and 58 skeletal traits** known to differ between modern humans and archaic hominins, where the fossil record supplies an independent check.
   - Enrichment analyses extend the signal to **tissues with no fossil record — brain, vocal cords, testes and other reproductive organs**.
   - Independent support: the candidates are **enriched in modern-human-derived differentially methylated regions and among variants shown to alter expression in MPRAs**.
   - **Why it matters here:** a curated, motif-mechanistic shortlist of human-specific regulatory variants with MPRA-based validation already partly in hand — an obvious library input, and a complement to the hCONDEL line of work that asks the same question from deletions rather than substitutions.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.06.747930v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/09/12/2026.09.06.747930/F1.large.jpg)

5. **A massively parallel synthetic gene atlas for learning compact cis-regulatory grammar across cellular contexts** (first: Hagen; senior: Goodarzi; *bioRxiv*, 14 September 2026).
   - A company (Therna) platform release — **"Chronos"** — measuring **~60,000 compact cis-regulatory elements across ~50 cell lines in one pooled experiment**, split into a 5'UTR/internal-promoter module and a 3'UTR stability module.
   - The framing is deliberate: virtual-cell models learn cis regulation only from **endogenous genes inside broad native contexts**; synthetic genes with a **short, defined variable region** give a cleaner read of the code.
   - Two delivery arms separate two layers of control — **episomal DNA delivery gives DNA-normalized mRNA output (transcriptional)**, while **direct delivery of N1-methylpseudouridine-modified mRNA with longitudinal sampling gives decay rates (post-transcriptional)**.
   - Resolving 30,000-element libraries required **pushing single-cell RNA-seq to single-molecule quantification** — the scaling constraint worth noting for any sc-MPRA design.
   - **Why it matters here:** the same measurement problem scMPRAforge models, at a scale and with a cross-cell-line design worth benchmarking against; and the "compact element" emphasis lines up with the current push in `#generomics` toward shorter, cargo-friendly synthetic CREs. ⚠ VERIFY: an industry preprint and platform announcement — read the claims with that in mind.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.13.751267v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/09/14/2026.09.13.751267/F1.large.jpg)

6. **An atlas of transcription factor cooperation reveals how motif readers shape regulatory output** (first: Xiong; senior: Wang; *bioRxiv*, 18 September 2026).
   - Analyzes **1,552 TF binding datasets across 10 cell types**, testing competing mechanistic explanations for each TF–motif dependency against multi-omic data rather than assuming the canonical assignment.
   - The dependencies resolve into **three routes: direct sequence recognition, protein-mediated recruitment or exclusion, and regulatory context**.
   - The load-bearing result: a motif's predictive power was attributable to its **"canonical" TF in only about one third of resolved cases**, and those canonical TFs were often **barely expressed** in the cell type where the motif mattered.
   - **Motif similarity tracked regulatory-region type but not transcriptional outcome**; **reader identity tracked both** — so the protein interpreting the motif, not the motif label, predicts what happens.
   - Perturbation checks back this up: knocking down an inferred reader **dropped target-TF occupancy in proportion to the reader's prior binding**, and a natural variant disrupting the predictive motif propagated through every step of the inferred mechanism.
   - **Why it matters here:** motif-based interpretation of MPRA and model attributions routinely names the canonical TF; this says that attribution is wrong roughly two thirds of the time. A caution for how we read Malinois/MPAC motif explanations, and a reason to condition motif calls on cell-type TF expression. ⚠ Figures were not yet rendered on bioRxiv at retrieval time, so no image.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.14.751590v1

7. **Identifying putative pathogenic non-coding variants in unresolved rare disease patients using topologically associated domains** (first: Gacita; senior: Grant; *bioRxiv*, 20 September 2026).
   - Targets the diagnostic gap directly: **at least 50% of rare-disease patients remain unresolved after exome/genome sequencing**, and a share of the missing diagnoses are non-coding variants that WGS detects but nobody interprets.
   - **GAVURD** takes **trio WGS alignments**, calls de novo and rare inherited variants, then **links each variant to disease genes via TAD membership** rather than nearest-gene, and ranks by phenotypic overlap with the proband.
   - Proof of concept on **ten unresolved probands implicated six potentially causal non-coding variants**, each on a confluence of evidence rather than a single score.
   - The honest limit is that TAD-based gene assignment is coarse — it bounds the search space but does not establish the element–gene link, which is where functional follow-up has to come in.
   - **Why it matters here:** this is the upstream half of the GREGoRi U01 logic — a systematic shortlist generator whose output is exactly what an MPRA or CRISPRi follow-up should be pointed at. Worth reading alongside the AlphaGenome-Atlas rare-disease use case from two weeks ago, which solves the same problem with a model rather than with topology. ⚠ Figures were not yet rendered on bioRxiv at retrieval time, so no image.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.09.17.752339v1

---

## Week of 2026-09-13

1. **Predicting genome-wide functional constraints with GPN-Star** (first: Ye; senior: Song; *Nature*, 09 September 2026).
   - **A genomic language model with phylogeny built into the architecture** — GPN-Star conditions on whole-genome **alignments plus the species tree**, instead of asking a large transformer to rediscover evolutionary relatedness from raw sequence.
   - Trained separately at **vertebrate, mammal and primate timescales**, and the comparison is the interesting part: **which timescale wins is task-dependent**, with deeper evolution favouring some constraint tasks and recent divergence favouring others.
   - **State of the art across coding and non-coding variant effect prediction**, beating both standard gLMs and classical evolutionary models — the failure mode the authors call out for NLP-derived gLMs is that they are big and expensive yet still lose to phyloP-class methods.
   - Downstream genetics gains are concrete: **better prioritization of pathogenic and fine-mapped GWAS variants, stronger complex-trait heritability enrichments, and more power in rare-variant association testing**.
   - Generalizes beyond humans — trained for **mouse, chicken, *Drosophila*, *C. elegans* and *Arabidopsis***, arguing the framework rides the growth of comparative genomics rather than model scale.
   - **Why it matters here:** a conservation-native prior that is directly comparable to MPAC and Malinois-class sequence-to-function models, and Erin is already using it. The timescale decomposition is the piece worth stealing — it is the same question the archaic-introgression work asks about **when** constraint was imposed.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41586-026-11005-5
   ![fig](https://media.springernature.com/lw685/springer-static/image/art%3A10.1038%2Fs41586-026-11005-5/MediaObjects/41586_2026_11005_Fig1_HTML.png)

2. **3D epigenome of glial cell types in developing human cortex** (first: Jones; senior: Shen; *Nature*, 02 September 2026).
   - Profiles **four glial populations from mid-gestation human neocortex** — ventricular radial glia, outer radial glia, OPCs and microglia — integrating **expression, accessibility, DNA methylation and 3D chromatin contacts**.
   - The logic is that **looping, not linear proximity, assigns a cCRE to its gene**: cell-type-specific contacts are what let them call cell-type-specific candidate cis-regulatory elements at all.
   - **cCREs were validated in transgenic mouse embryos**, so this is not a correlative atlas — the regulatory calls carry in-vivo evidence.
   - Machine learning prioritized **112 schizophrenia risk variants inside glial cCREs**, and the **rs4449074 risk allele was confirmed in vivo to disrupt a vRG enhancer** — a clean variant→element→cell-type→disease chain.
   - **oRG cCREs are enriched for human accelerated regions**, and a subset of those HARs show **activity differences from their chimpanzee orthologues**, contacting genes in neuronal development.
   - **Why it matters here:** this is the brain-cell-type regulatory map the brain-celltype-MPRA project is aimed at, and the HAR/chimp-ortholog comparison is exactly the human-specific-regulation axis the lab's evolution work runs on. Also a benchmark set of validated cell-type cCREs to test MPRA designs against.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41586-026-10987-6
   ![fig](https://media.springernature.com/lw685/springer-static/image/art%3A10.1038%2Fs41586-026-10987-6/MediaObjects/41586_2026_10987_Fig1_HTML.png)

3. **AlphaGenome Atlas: a predictive map of every possible DNA letter change in the human genome** (first: Cheng; senior: Avsec; *Google DeepMind — resource release + technical report*, 08 September 2026).
   - **Precomputed AlphaGenome predictions for all ~9 billion possible single-nucleotide variants** in the human genome — roughly **27,000 prediction values per variant**, ~1 petabyte, free for academic use via a portal and the API.
   - Ships a single summary number, the **AlphaGenome Variant Impact (AVI) score**, which fuses AlphaGenome's regulatory predictions with **AlphaMissense**'s protein-level score so coding and non-coding variants are **ranked on one scale**.
   - AVI is **decomposed into additive feature attributions** — accessibility, splicing, conservation — so a score comes with a mechanism rather than a bare number.
   - Also releases a compendium of **>2,500 de novo sequence motifs** with genomic locations, usable for TF-binding interpretation of non-coding variants.
   - Early external uses: **GREGoR** investigators prioritized an overlooked *DNM1* splice-creating variant in unsolved rare disease; a UK Biobank reanalysis of **54,000 whole genomes found 22% more non-coding associations** by grouping rare variants on predicted molecular effect.
   - **Why it matters here:** a free, genome-wide baseline that every variant-effect claim will now be compared against — relevant to MPAC benchmarking and to the GREGoRi U01, whose consortium is already named as a user. ⚠ VERIFY: authorship is taken from the contributor list on the release page (Jun Cheng listed first, Žiga Avsec last); there is no conventional journal byline yet.
   Shared `#interesting_papers`.
   https://deepmind.google/blog/alphagenome-atlas-a-predictive-map-of-every-possible-dna-letter-change-in-the-human-genome/
   ![fig](https://lh3.googleusercontent.com/vOjFcTcdX2GCEB9yk-tJ7GAfyhTAMo-zW7scq3TrT9qk1mYw5qE0BdUqI8XQclMuUchZr7pYUFdVt3ZzrXc1NGFFJOqi7kIUX_QuAXZR7lkVzxjk=w1200-h630-n-nu-rw)

4. **Insights into longevity and virus-driven adaptation from *Myotis* bat genomes** (first: Vazquez; senior: Sudmant; *Nature*, 26 August 2026).
   - **Near-complete genome assemblies plus cell lines for eight closely related *Myotis* species** — the tight phylogenetic spacing is what makes selection scans interpretable here.
   - The central claim is a **link between longevity and antiviral immunity through pleiotropy**, rather than two independent bat superpowers.
   - **Different virus classes leave different signatures**: genome-wide over-representation of **positive selection in DNA-virus-interacting proteins**, but elevated **copy-number variation for RNA-virus-interacting proteins**.
   - ***Myotis*-specific duplications of *EIF2AK2*/PKR** carry **ancient trans-species copy-number polymorphisms** — variation maintained across speciation events, a strong signal of long-term balancing pressure.
   - **Recurrent evolution of long lifespan tracks positive selection in cancer pathways**, backed by a distinct DNA-damage response in primary cells of the long-lived *M. lucifugus*.
   - **Why it matters here:** a template for pairing comparative selection scans with functional assays in primary cells — the structural-variation-plus-selection framing is directly useful to the Longevity Consortium U19 and to the sweeps/DeepSweep line of work.
   Shared `#interesting-papers_evolution`.
   https://www.nature.com/articles/s41586-026-10932-7
   ![fig](https://media.springernature.com/lw685/springer-static/image/art%3A10.1038%2Fs41586-026-10932-7/MediaObjects/41586_2026_10932_Fig1_HTML.png)

---

## Week of 2026-08-30

1. **Predictive design of tissue-specific mammalian enhancers that function in the mouse embryo** (first: Chen; senior: Stark; *Nature Genetics*, August 2026).
   - **Compact CNNs, not foundation models.** Pre-trained on E11.5 mouse **ATAC-seq** (heart, limb, midbrain), then **fine-tuned by transfer learning** on only **311–432 VISTA-validated enhancers per tissue**.
   - **15 of 15 designed enhancers were active in their intended tissue** in E11.5 mouse embryos (site-specific transgenic reporter, no background activity) — a **100% in vivo hit rate** from de novo sequences with no significant similarity to mouse or human genomes.
   - The two-step recipe is the whole result: models trained on **accessibility alone or enhancers alone** dropped PPV to **20.9–52.1%**, versus **≥70.6%** for the transfer-learned models.
   - Transfer learning **re-weights motifs toward tissue master regulators** (MEF2/heart, TWIST1/limb, SOX3/CNS) and **down-weights broadly-expressed factors** like CTCF — evidence the models learn regulatory grammar, not chromatin memorization.
   - Design used **Ledidi** gradient-based sequence optimization jointly against the accessibility and activity models; **≥69.7%** of high-scoring designs scored low in the two off-target tissues.
   - **Why it matters here:** this is the mammalian-in-vivo counterpart to the lab's MPRA-trained design work (CODA, synthetic CRE efforts) — and a direct existence proof that **modest, cheap training sets beat MPRA scale** for in-vivo enhancer design. Relevant to the synthetic-CRE and TRA design aims.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41588-026-02729-1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2025/12/22/2025.12.22.695948/F1.large.jpg)

2. **Human brain organoids record the passage of time over multiple years** (first: Antón-Bolaños; senior: Arlotta; *Nature*, August 19 2026).
   - Brain organoids maintained and profiled for **over five years** — by a wide margin the longest sustained human-neural-tissue culture — by **adapting culture medium to sustain spontaneous neuronal activity** rather than merely keeping cells alive.
   - The organoids **kept developing, not just surviving**: cell types emerged in the correct developmental order, connectivity increased, and genes switched on/off on schedule.
   - The hardest evidence is **epigenetic**: **DNA methylation accumulated along the characteristic human developmental trajectory**, and after ~1 year organoids showed **postnatal-stage features**.
   - **Cells retain a memory of developmental time** — dissociated old organoids regenerate late-stage cell types; mixing old with young cells **restores neurogenic capacity, but only for late-stage neuron types**.
   - **Why it matters here:** a tractable substrate for **maturation-dependent regulatory variation** — the cell-state axis the lab keeps arguing matters more than cell type. Directly relevant to neuro/neurodegeneration framing and to any MPRA or CRISPR readout that needs a genuinely mature human neural context.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41586-026-10877-x
   ![fig](https://mediasvc.eurekalert.org/Api/v1/Multimedia/ecf7545e-4c4d-4ae9-8593-c9cb99e710c4/Rendition/thumbnail/Content/Public)


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
   <!-- celebrated: 2026-07-13 -->

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
   <!-- celebrated: 2026-06-15 -->

---

## Week of 2026-08-23

1. **Responsiveness of epigenetic aging biomarkers to longevity interventions in humans** (first: Sehgal; senior: Higgins-Chen; *Nature Medicine*, August 21 2026).
   - Builds **TranslAGE**, a harmonized database of **51 longitudinal interventional studies**, then recomputes **16 prominent epigenetic clocks plus 94 other DNAm biomarkers** on every one — so clock behaviour is finally comparable across trials instead of trapped in each paper's own pipeline.
   - The central question is **surrogate-endpoint validity**: a clock is only useful as a trial readout if it actually *moves* when you intervene. Most clocks were built to predict age or mortality cross-sectionally, and that is not the same property.
   - **Clocks trained on mortality or pace-of-aging respond most strongly** and agree with each other; first-generation chronological-age clocks are comparatively inert. The training target, not the algorithm, is what determines responsiveness.
   - **Pharmacological and lifestyle interventions drive the largest DNAm biomarker shifts** — but the paper's own framing of "longevity intervention" is broad (rapamycin and metformin sit alongside kidney transplant, gastric bypass, plasmapheresis, HBOT), so much of the signal is plausibly **disease-state reversal in specific patients rather than aging per se** — a caveat Isabel flagged when sharing it.
   - **Why it matters here:** this is the measurement-layer counterpart to the Longevity Consortium's sequence-layer work. If mortality-trained clocks are the responsive ones, they are the readouts worth pairing with regulatory-variant and comparative-genomics evidence.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41591-026-04562-9
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41591-026-04562-9/MediaObjects/41591_2026_4562_Fig1_HTML.png)

2. **Functional impact of genetic background on variable expressivity in neurodevelopmental disorders** (first: Sun; senior: Girirajan; *Nature Communications*, August 2026).
   - Uses the **16p12.1 deletion** as a tractable paradigm for **variable expressivity**: same CNV, very different phenotypes, and the usual explanation ("genetic background") is rarely made mechanistic.
   - Design pairs **patient-family iPSC lines with CRISPR-engineered isogenic 16p12.1 deletions**, which separates the deletion's own effect from the background it lands in — the isogenic arm is what makes the comparison interpretable.
   - Finding: **the deletion and rare background variants jointly shape chromatin accessibility and expression of neurodevelopmental genes**. Background is not noise added on top; it is co-determining the regulatory state.
   - Cellular phenotypes are **family-specific** — altered inhibitory-neuron production and NPC proliferation — and **correlate with head-size variation** in the corresponding patients, tying the dish back to the clinic.
   - **CRISPR activation of individual 16p12.1 genes variably rescues** the defects through developmental signaling, and integrative analysis nominates regulatory hubs including **FOXG1 and JUN**. Variable rescue is itself the point: which gene matters depends on background.
   - **Why it matters here:** this is the clean statement of the problem the ClinVar/GREGoRi work has to survive — a variant's functional readout is background-dependent, which argues for testing in multiple genetic contexts rather than one reference line.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41467-026-72598-z
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41467-026-72598-z/MediaObjects/41467_2026_72598_Fig1_HTML.png)

3. **Systemic epigenetic dysregulation as a driver of ageing and a therapeutic target** (first: Yücel; senior: Gladyshev; *Nature Reviews Molecular Cell Biology*, 2026).
   - Review proposing **"epigenetic fidelity"** — the capacity of chromatin regulatory systems to hold precise expression states — as the organizing variable, with aging framed as its progressive failure.
   - Four interdependent failure modes: **nuclear-architecture deterioration (lamina-associated domain breakdown)**, **loss of epigenetic memory via chromatin-modifying complexes such as PRC2**, **nucleosome alteration through replication-independent H3.3 accumulation**, and **transcription-factor-driven reprogramming**.
   - The argument is explicitly **systems-level**: these processes cross-regulate, so a local defect cascades into broader loss of cell-state maintenance — which is why single-target interventions tend to disappoint.
   - **Why it matters here:** the **transcription-factor reprogramming** arm is the actionable one for this lab — it predicts that aging shifts *which* TFs occupy regulatory elements, a hypothesis MPRA and comparative CRE work can test directly. Flagged in the Longevity Consortium channel with a specific suggestion to **look at AP-1 binding sites**.
   Shared `#longevity-consortium`.
   https://www.nature.com/articles/s41580-026-00958-0
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41580-026-00958-0/MediaObjects/41580_2026_958_Fig1_HTML.png)

---

## Week of 2026-08-16

1. **Uniform processing and analysis of IGVF massively parallel reporter assay data with MPRAsnakeflow** (first: Rosen; senior: Schubach; *bioRxiv* 2025.09.25.678548, posted September 29 2025; now out in *Genome Research*).
   - The **IGVF Consortium's MPRA focus group** standard: harmonized file formats plus **MPRAlib + MPRAsnakeflow**, a Snakemake pipeline taking raw MPRA reads all the way to counts, QC, and visualization.
   - Characterizes the technical variability sources that actually move MPRA results — **barcode sequence bias, outlier barcodes, and delivery method (episomal vs. lentiviral)** — and turns them into concrete best-practice recommendations.
   - Built explicitly for **cross-study integration**: uniform processing is the precondition for pooling MPRA datasets across labs and library designs.
   - **Why it matters here:** this is fast becoming the field-standard pipeline for exactly the kind of MPRA data the lab generates (scMPRAforge, brain-celltype-mpra, Locium screens) — worth a direct comparison against the lab's in-house processing choices, especially the barcode-bias and delivery-method corrections.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.1101/2025.09.25.678548v2
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2025/09/29/2025.09.25.678548/F1.large.jpg)

2. **Plasticity of human microglia and brain perivascular macrophages in aging and Alzheimer's disease** (first: Lee; senior: Roussos; *Nature Genetics*, online August 11 2026).
   - Profiles **832,505 myeloid cells** (microglia + perivascular macrophages) from the prefrontal cortex of **1,607 donors** spanning the human lifespan and the full range of AD neuropathology — the largest reference of its kind.
   - Delineates **13 transcriptionally distinct subtypes across 6 subclasses**, and tracks how their proportions shift with aging and AD progression.
   - A **GPNMB-high, disease-associated microglial subtype** expands with AD pathology and shows **elevated phagocytic activity** rather than pure damage — a protective, not purely pathogenic, disease-state signature.
   - **MITF** is identified as the upstream regulator required to sustain this state, and the protective effect is shown to **depend on TREM2 signaling** in both human tissue and mouse models; cell-cell interaction analysis further flags APOE–SORL1 and APOE–TREM2 as the relevant signaling pairs.
   - **Why it matters here:** this lands directly on the lab's own (Drive-only, not yet in this repo) Microglia R01 draft, *"Accessing diseased microglia via synthetic regulatory elements and longitudinal imaging"* — its Aim 2 is built around measuring and synthetically targeting homeostatic vs. DAM microglial states. This paper supplies exactly the kind of molecularly defined DAM-state markers (GPNMB/MITF/TREM2) that Aim 2's synthetic-CRE design would need to build around, and is a strong citation for the R01's premise that DAM states are a druggable, trackable target.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41588-026-02716-6
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41588-026-02716-6/MediaObjects/41588_2026_2716_Fig1_HTML.png)

3. **Investigating Data Size, Sequence Diversity, and Model Complexity in MPRA-based Sequence-to-Function Prediction** (first: Sheng; senior: Mostafavi; *bioRxiv* 2025.03.11.642630, posted March 13 2025).
   - Builds the **MPRA Dataset Collection (MDC)**: 150M+ labeled DNA subsequences pooled from 12 studies, mixing **random synthetic libraries and natural genomic sequences** with varied functional readouts (expression, splicing).
   - Systematically studies how **training data size, sequence diversity, and model complexity** trade off against how well a sequence-to-function model generalizes.
   - Key empirical result: models trained on **native genomic sequence are initially more accurate**, but models trained on **randomized sequence libraries eventually overtake them given enough data** — randomized sequences pack more distinct information per base than the genome does.
   - **Why it matters here:** this is a direct, concrete test of the "hold out the genome" debate that ran through `#interesting_papers` this week (Steve, Mackenzie, Grace, Aug 12) — the sticking point the group landed on is that "large enough" data is never the regime the lab actually operates in, so a smarter middle path (a data-embedding-guided choice of which sequences an MPRA library should even contain) may matter more for CODA/Malinois retraining than brute-force library scale.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.1101/2025.03.11.642630v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2025/03/13/2025.03.11.642630/F1.large.jpg)

4. **Correcting signal biases and detecting regulatory elements in STARR-seq data** (first: Kim; senior: Reddy; *Genome Research* 31(5):877, 2021).
   - Identifies the **technical biases that explain most of the variance in raw STARR-seq signal** (fragment-level composition and mappability effects), rather than treating that variance as biological.
   - Builds a statistical correction model that **substantially improves precision and recall** for calling regulatory elements, including **repressive** elements that naive pipelines tend to miss entirely.
   - Controls false discovery despite the **strong local spatial correlation** inherent to reporter-assay signal tracks.
   - **Why it matters here:** an older paper, but Jared re-surfaced it this week as a reference point for signal-bias correction — directly relevant background for any STARR-seq-adjacent QC or construct-design discussion in the lab's own reporter-assay pipelines.
   Shared `#interesting_papers`.
   https://genome.cshlp.org/content/31/5/877

---

## Week of 2026-08-09

1. **Active learning of enhancers and silencers in the developing neural retina** (first: Friedman; senior: Cohen; *Cell Systems* 16(1), online January 7 2025).
   - Trains models to separate **enhancers from silencers built from the same CRX binding sites** — the case where a single TF activates in one context and represses in another, which sequence models routinely get wrong.
   - The core move is **active learning**: instead of training once on whatever the genome happens to contain, the model **nominates the sequences it is least certain about**, those get synthesized and measured, and the cycle repeats.
   - This attacks the real bottleneck directly — **the genome does not contain enough natural CREs** to teach a model the higher-order interactions among motifs, so genome-trained models mostly rediscover the same large-effect motifs a motif scanner would find.
   - Iterating the loop recovers **grammar rules that distinguish activation from repression**, not just which motifs are present.
   - **Why it matters here:** this is the formal version of the lab-meeting idea Mackenzie flagged — **design the next MPRA library where the model is struggling**, rather than tiling more genome. Directly applicable to CODA/Malinois retraining and to how the next brain-cell-type library gets specified.
   - Steve's read: active learning was a hot ML topic a few years back, but it is **a good reminder of its utility in data-limited spaces** — which is exactly the regime MPRA design sits in.
   Shared `#interesting_papers`.
   https://pubmed.ncbi.nlm.nih.gov/39778579/
   ![fig](https://www.cell.com/cms/10.1016/j.cels.2024.12.004/asset/5c9026dd-23fa-4cd7-a560-710de5539325/main.assets/gr1.jpg)

2. **Resolving systematic errors in widely used enhancer activity assays in human cells** (first: Muerdter; senior: Stark; *Nat Methods* 15, online December 11 2017).
   - Two plasmid artifacts corrupt reporter assays: the **bacterial origin of replication acts as a competing core promoter**, and **transfection itself triggers a type-I interferon response**.
   - The ORI effect produces **false negatives** — a real enhancer looks dead because the ORI is already driving the transcript that gets counted.
   - The IFN-I response produces **false positives and distorted rankings**, because interferon-stimulated genes light up as a consequence of the delivery method rather than the sequence being tested.
   - The fix is twofold: **use the ORI as the sole core promoter** so it is a known constant instead of a hidden competitor, and **pharmacologically block the IFN-I response** during the assay.
   - With both corrections, single-candidate luciferase, MPRA, and STARR-seq all clean up enough to support **genome-wide enhancer screens**.
   - **Why it matters here:** an older paper, but it landed in `#interesting_papers` this week and ran a 20-reply thread — these are exactly the confounders that show up when comparing MPRA constructs across cell lines, and they bear on current construct-design and orientation decisions.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/nmeth.4534
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fnmeth.4534/MediaObjects/41592_2018_Article_BFnmeth4534_Fig1_HTML.jpg)

3. **Deep learning-guided design of cell type-specific AAV promoters** (first: S.K. Wang; senior: S. Wang; *bioRxiv* 2026.01.13.699371, posted January 14 2026).
   - Head-to-head comparison of **three strategies for designing cell-type-specific AAV promoters** from single-cell chromatin accessibility data, including **de novo generation by a deep model**.
   - **Deep-learning-guided design consistently beat the rational approaches** in vivo, targeting retinal ganglion cells and horizontal cells in mouse retina with **stronger and more specific expression**.
   - The synthetic promoters were **payload-agnostic** — they drove diverse transgenes well enough to both **record from and ablate** the targeted cells.
   - Activity **carried over into human retinal organoids**, the key translation signal: a sequence designed on mouse accessibility data still behaved in human tissue.
   - **Why it matters here:** this is the CODA thesis validated in a different tissue and a different lab, and it is the closest external benchmark for the Locium synthetic-promoter line — worth reading alongside the AAV off-target-toxicity and clinical-promoter-benchmark memos now circulating on that project.
   Shared `discovered`.
   https://www.biorxiv.org/content/10.64898/2026.01.13.699371v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/01/14/2026.01.13.699371/F1.large.jpg)

4. **Chorus: a unified interface for genomic sequence oracles** (first: Penzar; senior: Pinello; *software release (GitHub)*, 2026).
   - Puts **eight sequence-to-function models behind one API** — AlphaGenome, Enformer, Borzoi, ChromBPNet/BPNet, Sei, LegNet, EPInformer-seq, Cherimoya/CATv1 — so a question can be asked of all of them instead of one at a time.
   - The genuinely useful bit is **normalization**: every prediction comes back as an **effect percentile and an activity percentile**, calibrated against per-track CDF backgrounds built from thousands of sampled SNPs and genome-wide positions. That makes raw scores from different oracles **actually comparable**, which is the thing that normally blocks ensembling.
   - Each oracle runs in **its own conda environment**, which is what makes an eight-model install tractable at all; weights are **mirrored to HuggingFace** so the install path survives upstream churn (TFHub deprecation, dead Zenodo links).
   - Ships a **22-tool MCP server** — you can point Claude at it and ask in plain English for variant effects, region swaps, gene-TSS lookups, or cell-type discovery, and it picks the tool.
   - Supports **region replacement**: swap a synthetic sequence in for an endogenous element and predict accessibility across cell types — directly the CODA/synthetic-CRE design loop.
   - **Why it matters here:** it is a Pinello-lab release, and it is the closest thing yet to an off-the-shelf harness for the ensemble-of-oracles comparisons the lab keeps doing by hand. Worth a look for MPRAgent and for benchmarking against Malinois.
   Shared `#interesting_papers`.
   https://github.com/pinellolab/chorus

5. **Pangenome Graph Node-Phenotype Association shows GWAS-like quality results with only few individuals** (first: Carrette; senior: Muller; *bioRxiv* 2026.07.31.741971, July 31 2026).
   - **GraNPA** runs a GWAS-like association directly on a **pangenome variation graph** instead of on variant calls against a single reference.
   - Because a graph node *is* the variation, the same analysis covers **everything from SNPs to large structural variants** in one pass — no separate SV pipeline, and **no reference bias introduced by variant calling**.
   - Phenotype information is folded into the nodes to give each one a **Phenotype Score**; associated regions fall out as **statistically significant shifts in the PS distribution**, reported with positions and scores.
   - The headline claim is sample size: it recovered known loci from **a few dozen complete genomes** — the *Sub1A* submergence locus in rice from a **13-individual** graph, and the insertion behind white-headed cattle from a **24-individual** graph — with **no kinship or population panel required**.
   - Current limit is honest and clearly stated: **qualitative phenotypes only**.
   - **Why it matters here:** Erin flagged this for Tian as **an alternative attack on the rare-variant problem** — if the association unit is a graph node rather than a called variant, rare and structural variation stop being systematically invisible, and you stop needing hundreds of individuals to see them. Different lever than the FLARE/ChromBPNet route, worth knowing about.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.64898/2026.07.31.741971v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/07/31/2026.07.31.741971/F1.large.jpg)

---

## Week of 2026-08-02

1. **Locus-Scale Massively Parallel Reporter Assays** (first: McGee; senior: Shendure; *bioRxiv* 2026.07.24.740649, July 28 2026).
   - Conventional MPRA element length was set by **microarray DNA synthesis limits, not biology** — nearly all MPRAs assay **sub-300 bp fragments** butted against a minimal promoter, while validated developmental enhancers are mostly **>300 bp** and super-enhancers span kilobases.
   - **LAMPRA** ("long @$$ MPRA") combines **combinatorial cloning, molecular barcoding, and paired long- + short-read sequencing** to measure regulatory output at **multi-kilobase** scale.
   - Proof of concept assays **36,000 × 5-kb synthetic cis-regulatory loci**, each built as a **5 × 1-kb random combination of enhancers, insulators and spacers** — so the design varies **identity, number, spacing, order and orientation** simultaneously.
   - The point is **combinatorial logic**: rather than scoring one element in isolation, it measures how CREs interact when assembled into a locus, the regime conventional MPRA cannot reach.
   - Why it matters here: this is the **length/architecture axis** our own MPRA platform is bounded by. Directly relevant to `scmpraforge` design space, to the **construct-orientation/promoter-contamination** questions raised by the Engreitz promoter-responsiveness paper, and to how far endogenous PEAR-seq readouts can be cross-checked against episomal ones in the GREGoRi aims.
   - Discovered-pass hit against the MPRA watch-topic.
   https://www.biorxiv.org/content/10.64898/2026.07.24.740649v2
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/07/28/2026.07.24.740649/F1.large.jpg)

2. **Decoding common and rare noncoding variant effects across cellular and developmental contexts** (first: Marderstein; senior: Montgomery; *Nature Genetics*, July 2026).
   - The **published journal version of the FLARE preprint** digested here on 2026-06-24 — worth re-reading now that it is final, since it is the closest published framing to Tian Xia's project.
   - Generates **3 billion deep-learning predictions of chromatin accessibility** across diverse **fetal and adult** cellular contexts, then uses them to prioritize functional noncoding variants.
   - Central dichotomy: **common variants are more cell-type-specific**, while **ultra-rare variants have larger and broader effects across cell types** — the frequency spectrum and the context-specificity spectrum are coupled.
   - **Strongest evidence of purifying selection sits in fetal neurons**, i.e. the constraint signal is developmental, not adult.
   - **FLARE** (Functional Lasso Analysis of Regulatory Evolution) folds evolutionary constraint into the prioritization and generalizes across **de novo mutations in childhood disorders, rare variants behind outlier adult brain expression, and common variants enriched for schizophrenia heritability**.
   - Steve's read in the lab thread: this is "**exactly the right paper**" for the direction Tian is pushing, but it **stops short of linking regulatory effect to trait** — that gap is the opening.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41588-026-02619-6
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41588-026-02619-6/MediaObjects/41588_2026_2619_Fig1_HTML.png)

3. **Characterizing homology-induced data leakage and memorization in genome-trained sequence models** (first: Rafi; senior: de Boer; *bioRxiv* 2025.01.22.634321 v2, May 25 2026).
   - Standard train/test splits of genomic sequence **ignore pervasive within-genome homology**, so test sequences are often near-copies of training sequences — a **leakage** problem, not just a tuning problem.
   - Simulations show this leakage **inflates apparent model performance**; across a range of published genomics models, **test performance varies systematically with similarity to the training set**.
   - The failure mode is diagnostic: models do well on **distant** sequences (real generalizable rules) and well on **highly similar** sequences (memorized associations) — but memorization **breaks when homologs have functionally diverged**, which is exactly the case anyone cares about.
   - Practical consequence: reported benchmark numbers for sequence-to-function models are **not comparable** unless the split is homology-aware.
   - Why it matters here: Mackenzie Noon flagged it and Erin Gilbertson is **building her own training-partition implementation** to compare against — this bears directly on cross-species CRE prediction, where homology *is* the signal being modelled.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.1101/2025.01.22.634321v2
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/05/25/2025.01.22.634321/F1.large.jpg)

4. **The expression modifier score (EMS) v2 enhances regulatory variant prioritization via Enformer-derived features and multi-task learning** (first: Takahashi; senior: Okada; *Communications Biology*, July 22 2026).
   - Rebuilds the Expression Modifier Score for prioritizing **causal regulatory variants**, with the largest gains in **tissues with small eQTL sample sizes, such as brain** — precisely where fine-mapping is weakest.
   - Attributes the improvement to three specific changes: **long-range sequence-interaction features (Enformer-derived)**, a **customized training loss**, and a **multi-task learning framework**.
   - Validated **out-of-population** on independent Japanese eQTL data, where it beat alternatives and supported **functionally informed fine-mapping** — a real portability test, not just held-out folds.
   - Combines with the gene-level **polygenic priority score (PoPS)** to prioritize complex-trait-causal regulatory variants, i.e. variant-level and gene-level evidence stacked.
   - Why it matters here: another entrant in the crowded variant-effect-predictor field that `mpac` must be benchmarked against; the small-sample-tissue claim is the interesting one for brain work.
   - No figure available — the article is currently posted as an unedited accepted manuscript.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s42003-026-10604-2

5. **Leveraging human genetic variation to therapeutically target hundreds of genes with dominant & dispensable disease alleles** (first: Ramey; senior: Capra; *medRxiv* 2026.03.26.26349431, March 27 2026).
   - Defines **"dominant & dispensable" (D&D)** disease alleles: in **haplosufficient** genes, one working copy suffices, so silencing only the pathogenic copy is curative in principle. Over **500 genes** qualify.
   - The trick is **mutation-agnostic targeting**: instead of aiming at the rare pathogenic variant itself, target **common heterozygous variants in linkage with it**, so one therapy covers many patients with different causal mutations.
   - Scale of the payoff: for some disease genes this makes **>80× more patients treatable** than mutation-specific strategies.
   - D&D alleles span **neurodegeneration, cardiomyopathies, retinopathies and diabetes** — the logic is not confined to one organ system.
   - Ships **genome-wide maps of common heterozygous targeting sites** to make the approach broadly usable.
   - Why it matters here: Erin Gilbertson raised it as the **inverse** of what the lab does — we go from common variation to function, this goes from common variation to a *handle* on rare high-effect alleles. Useful framing for the Locium synthetic-CRE/gene-therapy side and for the GREGoRi rare-disease aims.
   Shared `lab DM`.
   https://www.medrxiv.org/content/10.64898/2026.03.26.26349431v1
   ![fig](https://www.medrxiv.org/content/medrxiv/early/2026/03/27/2026.03.26.26349431/F1.large.jpg)

6. **Deciphering complete archaic introgression sequences in modern human genomes** (first: Suo; senior: G. Zhang; *bioRxiv* 2026.07.23.740208, July 24 2026).
   - **ASMaid** is an HMM framework that calls archaic ancestry from **haplotype-resolved pangenome assemblies** rather than short-read alignments to a single reference.
   - Because it integrates **both SNP genotype and structural-variation signals**, it recovers **more intact archaic segments** — the regions reference-based callers systematically lose.
   - Applied to **610 phased human genome assemblies**, non-Africans carry **~79.8 Mbp of Neanderthal** and **~8.3 Mbp of Denisovan** sequence, both **substantial increases over previous estimates**.
   - Reports archaic sequence in **structurally complex regions including centromeric contexts** — a class of introgression essentially invisible to conventional maps.
   - Discovered-pass hit against the archaic-introgression watch-topic; the direct comparison to make is against the **Near Oceania** callset, where the lab reconstructed 1.897 Gbp of archaic sequence including 831.9 Mbp Denisovan — different populations, different method, and a good external check on completeness claims.
   https://www.biorxiv.org/content/10.64898/2026.07.23.740208v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/07/24/2026.07.23.740208/F1.large.jpg)

7. **Balanced polymorphism in a floral transcription factor underlies the ancient rhythm of daily sex alternation in avocado** (first: Groh; senior: Coop; *PNAS* 123(31) e2606876123, July 28 2026).
   - Avocado and wild Lauraceae relatives run **heterodichogamy**: A-type plants open female-phase flowers in the morning and male-phase in the afternoon, B-types do the reverse, and the whole population is synchronized daily.
   - The dimorphism maps to **one locus — a pair of dominant/recessive haplotypes at *SDMYB***, an R2R3 MYB transcription factor from a subgroup tied to floral maturation and circadian hormone signalling.
   - Mechanism is **regulatory, not just coding**: the dominant allele carries nonsynonymous changes in conserved domains **and shows a cis-regulated phase delay** in diel expression that matches the delayed second anthesis of A-type flowers.
   - The haplotypes form an **ancient trans-species polymorphism** maintained by **negative frequency-dependent balancing selection** — whichever type is rarer has the mating advantage, so both persist across species boundaries.
   - Why it matters here: a clean textbook case of **balancing selection preserving a cis-regulatory allele over deep time**, and of a single TF's *expression timing* — not its presence — being the phenotypic switch. Good ammunition for the "regulation as a dial" framing.
   Shared `#interesting_papers`.
   https://www.pnas.org/doi/10.1073/pnas.2606876123
   ![fig](https://www.pnas.org/cms/10.1073/pnas.2606876123/asset/8ffad25f-6360-4faf-a081-bbd1ae0e0f34/assets/images/large/pnas.2606876123fig01.jpg)

---

## Week of 2026-07-27

1. **Massively parallel characterization and predictive modelling of neuronal regulatory variation** (first: Salomon; senior: Kircher; *bioRxiv* 2026.07.16.738760, July 17 2026).
   - A **lentiMPRA in human excitatory neurons** measuring **>46,000 naturally occurring variants across >27,000 candidate CREs** near **524 disease-associated genes** — the scale is what makes the negative results below trustworthy.
   - The resulting catalog **improves regulatory variant-effect prediction beyond state-of-the-art models**, so it functions as **training data and benchmark**, not just a result.
   - **Significant allelic effects occur at comparable rates among common, rare and singleton variants** — within MPRA-measurable effects, **allele frequency carries little information about per-variant regulatory impact**. That directly undercuts frequency-based prioritization of noncoding candidates.
   - What *does* predict effect is the element, not the allele: **baseline activity of the enclosing regulatory element and local sequence context** govern both **detectability and magnitude**.
   - Effects are **distributed across many transcription factors rather than concentrated in master regulators**, consistent with a **combinatorial enhancer architecture**.
   - Why it matters here: same design logic as **brain-celltype-mpra**, and "baseline activity gates detectability" is a hard **power-calculation constraint** for any MPRA screening disease variants — including the endogenous-readout work behind the GREGoRi U01.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.64898/2026.07.16.738760v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/07/17/2026.07.16.738760/F1.large.jpg)

2. **Architectural chromatin interactions provide a framework for context-dependent gene regulation** (first: Likhite; senior: Moore; *bioRxiv* 2026.07.17.739237, July 20 2026).
   - Integrates **Hi-C, RNAPII ChIA-PET and CTCF ChIA-PET** with the **ENCODE cCRE registry** to classify promoter-centric contacts — the premise being that **chromatin interactions are several biologically distinct classes** that no single assay resolves.
   - Identifies a class of **candidate architectural promoter–enhancer interactions**: **recurrent across cellular contexts, broader promoter connectivity, and less dependent on linear genomic proximity**.
   - Many of the anchoring elements **switch between enhancer and CTCF-only states while the interaction itself stays stable** — "**dual-state**" regulatory elements.
   - Those dual-state elements **acquire context-specific TF inputs inside evolutionarily conserved architectural scaffolds**, supporting a model where **stable architecture is repeatedly repurposed for new regulatory programs**.
   - Genes connected to them are **enriched for developmental and signaling pathways** and show **increased expression specificity across cell types**.
   - Why it matters here: a **structural complement** to the lab's enhancer–gene work — architecture supplies the wiring, sequence supplies the switch — built directly on the **ENCODE registry the lab helps functionally validate** as an FCC.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.64898/2026.07.17.739237v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/07/20/2026.07.17.739237/F1.large.jpg)

3. **Genetic trade-offs in fertility and longevity explain the maintenance of disease-associated alleles in humans** (first: Brigos-Barril; senior: Muntané; *Nature Ecology & Evolution*, July 21 2026).
   - Tackles the standing puzzle of **why disease-risk alleles persist** despite costs to health, testing the **life-history / antagonistic-pleiotropy prediction** that they survive by buying reproduction.
   - Across genome-wide data for **62 diseases plus longevity and fertility**, disease-risk alleles are on average associated with **reduced longevity and increased fertility**.
   - The subset that **raises both fertility and disease risk shows evidence of having been favoured by selection over the past ~50,000 years** — the trade-off left a **selection footprint**, not just a correlation.
   - **Mendelian randomization** detects a **causal effect of genetic disease liability on longevity**, but **no robust causal effect on fertility** — so the fertility signal reads as **pleiotropy**, not disease driving reproduction.
   - Why it matters here: supplies the **population-genetic rationale** for deleterious regulatory alleles sitting at appreciable frequency, which is the backdrop for the lab's **archaic-introgression and variant-effect** lines.
   Shared `#interesting_papers`.
   https://www.nature.com/articles/s41559-026-03140-z
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41559-026-03140-z/MediaObjects/41559_2026_3140_Fig1_HTML.png)

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
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/07/08/2026.07.06.736502/F1.large.jpg)

---

## Week of 2026-07-13

1. **Immune context unmasks regulatory effects of Neanderthal and Denisovan introgression** (first: Li; senior: Rotival; *bioRxiv* 2026.05.29.727880, June 1 2026).
   - An **MPRA of 4,161 introgressed variants** (Neanderthal + Denisovan) across three cell types, tested at baseline and under **immune/infectious stimulation**.
   - Central claim: an **immune / activated cell context "unmasks" regulatory effects** invisible at baseline — 94 variants' effects are specifically revealed or modulated by stimulation.
   - The strongest hit, **rs17713054-A** (linked to Neanderthal introgression and COVID-19 severity), boosts a TNF-α-responsive lung enhancer, upregulating **SLC6A20**.
   - Implication: **context-dependent** reporter assays recover **adaptive-introgression regulatory function** that resting-state MPRA misses — a design lesson for the lab's own introgression + single-cell MPRA work.
   - Surfaced while auditing papers affected by the **mpraflow / MPRAnalyze** bug, so worth reading with that caveat in mind.
   Shared `#interesting-papers_evolution`.
   https://www.biorxiv.org/content/10.64898/2026.05.29.727880v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/06/01/2026.05.29.727880/F1.large.jpg)

2. **Genome-wide absolute quantification of chromatin looping** (first: Jusuf; senior: Hansen; *Nature Structural & Molecular Biology*, 2026).
   - **Calibrates Micro-C against live-imaging** to convert contact frequencies into **absolute looping probabilities** across 65,929 loops genome-wide.
   - Loops are **rare**: mean pairwise looping probability **~1.2%**, maximum **~25%** — the looped state is the exception, not the rule.
   - **CTCF–CTCF loops (~2.2%) are stronger than cis-regulatory loops (<1%)**, reframing enhancer–promoter "loops" as **transient, low-probability** contacts.
   - A useful quantitative prior for **3D-genome / cross-species modeling** (why it was flagged in `#xspecies-modeling`).
   Shared `#xspecies-modeling`.
   https://www.nature.com/articles/s41594-026-01819-2
   ![fig](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41594-026-01819-2/MediaObjects/41594_2026_1819_Fig1_HTML.png)

---

## Week of 2026-07-05

1. **Somatic cancer variants enriched in Alzheimer's disease microglia-like cells drive inflammatory and proliferative states** (first: Huang; senior: Walsh; *Cell*, 2026).
   - **Classic cancer-driver somatic mutations accumulate in microglia** in Alzheimer's disease brains, without producing cancer.
   - Mutant microglial clones are **selected for survival and proliferation**, creating a persistent **inflammatory niche**.
   - The resulting chronic inflammation plausibly **kills neighboring "bystander" neurons**, linking clonal somatic selection to neurodegeneration.
   - Extends the somatic-mosaicism-as-disease-driver logic from neurons to **glia** — directly adjacent to the lab's own somatic-mosaicism work.
   Shared `#interesting_papers`.
   https://www.cell.com/cell/fulltext/S0092-8674(26)00341-7

2. **ATLAS — population-level disease locus discovery via differential attention in genomic language models** (first: Liu; senior: Zhang; *bioRxiv* 2026.02.09.704696, February 10 2026).
   - Compares **attention patterns from a pretrained genomic language model** between disease and control cohorts to localize disease loci **without variant calling or supervised training**.
   - Gene-level differential attention prioritizes candidates; a base-level pass **localizes signal to single-haplotype resolution**.
   - Validated on synthetic data and a **β-thalassemia cohort**; recovers known loci with **higher recall than GWAS** at low allele frequencies (down to 10%) and small cohort sizes (<200/group).
   - An unsupervised alternative to MPAC-style variant-effect prediction, worth tracking for rare-variant/small-cohort settings.
   Shared `#interesting_papers`.
   https://www.biorxiv.org/content/10.64898/2026.02.09.704696v1
   ![fig](https://www.biorxiv.org/content/biorxiv/early/2026/02/10/2026.02.09.704696/F1.large.jpg)

---

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

---

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
