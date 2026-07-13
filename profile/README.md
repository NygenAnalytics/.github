<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://www.nygen.io/static/img/nygen-logo-white.png">
    <img src="https://www.nygen.io/static/img/nygen-logo.png" alt="Nygen" width="230">
  </picture>

  ### Decode every cell.

  AI for single-cell biology, from computation to annotation to interpretation.

  [Homepage](https://nygen.io) · [Docs](https://www.nygen.io/docs/cytetype) · [Technology](https://www.nygen.io/technology) · [Book a demo](https://calendly.com/nygen/parashar)

</div>

---

👋 Welcome. We're **Nygen Analytics**, an applied AI/ML lab working on single-cell biology, based at Medicon Village in Lund, Sweden.

Single-cell sequencing routinely produces datasets with millions of cells. The bottleneck is no longer the sequencing or the compute, it's the biological interpretation: figuring out what each cell actually is and what it's doing. That's the layer we build. Our tools turn raw single-cell data into cell-level biology you can trace, audit, and defend, with the evidence attached to every call.

Our work is trusted by researchers at institutions including Memorial Sloan Kettering, Harvard, Oxford, Stanford, Cambridge, Helmholtz Munich, and Institut Pasteur.

## What we build

Two products, backed by open-source foundations.

**[CyteType](https://www.nygen.io/products/cytetype)** is our hosted annotation service: a multi-agent system where specialized AI agents debate competing hypotheses, ground them in full expression data, and validate against external databases. Every annotation comes back with marker-level evidence, a Cell Ontology term, and a confidence score, in an audit-ready interactive report with a per-cluster chat interface. You drive it from your own analysis environment through our SDK.

**[ScarfWeb](https://www.nygen.io/products/scarfweb)** is a browser-native workbench for secondary analysis. It runs on distributed, secure infrastructure and is powered by Scarf, our open-source analysis engine.

## Open source

The public repositories, and a good place to start if you want to see how we work:

🧬 **[CyteType](https://github.com/NygenAnalytics/CyteType)** `Python`
The SDK for our hosted annotation service. Submit clusters straight from Scanpy / AnnData and get evidence-backed, ontology-mapped annotations back into your object. No API keys needed to get started.

🧬 **[CyteTypeR](https://github.com/NygenAnalytics/CyteTypeR)** `R`
The same SDK for Seurat workflows.

⚡ **[Scarf](https://github.com/NygenAnalytics/scarf)** `Python`
Memory-efficient analysis of scRNA-seq, scATAC-seq, and CITE-seq data, built to handle atlas-scale datasets with millions of cells on a laptop. This is the engine behind ScarfWeb.

🔬 **[CyteOnto](https://github.com/NygenAnalytics/CyteOnto)** `Python`
Automated semantic comparison of cell type annotations in Cell Ontology embedding space. This is how we benchmark predicted labels against ground truth beyond exact string matching.

The CyteType SDKs are free for academic and non-commercial research (CC BY-NC-SA 4.0).

## Publications

📄 Ahuja G, Antill A, Su Y, Dall'Olio GM, Basnayake S, Karlsson G, Dhapola P. **Multi-agent AI enables evidence-based cell annotation in single-cell transcriptomics.** bioRxiv, 2025. [doi:10.1101/2025.11.06.686964](https://www.biorxiv.org/content/10.1101/2025.11.06.686964v1)

📄 Dhapola P, Rodhe J, Olofzon R, Bonald T, Erlandsson E, Soneji S, Karlsson G. **Scarf enables a highly memory-efficient analysis of large-scale single-cell genomics data.** Nature Communications 13, 4616, 2022. [doi:10.1038/s41467-022-32097-3](https://www.nature.com/articles/s41467-022-32097-3)

## Our stack

The work sits where core bioinformatics meets applied ML:

- **Single-cell bioinformatics.** Scanpy, AnnData, Seurat, and the methods underneath them, from preprocessing and clustering to differential expression and integration.
- **Agentic workflows.** Multi-agent systems that reason over expression data, retrieve and weigh evidence, and self-evaluate their own calls.
- **LLM fine-tuning and evaluation.** Adapting and benchmarking language models for single-cell tasks, including our open benchmarking across 16 LLMs.
- **Scalable infrastructure.** Memory-efficient processing and cloud infrastructure on AWS for atlas-scale data.

## Work with us

If you work on single-cell data, or you want to, we'd like to work with you. That covers a lot of ground: building on top of our tools, extending them to a problem they don't handle yet, benchmarking them against your own datasets, or bringing us a research question or collaboration. If you just want to make the tools better, that counts too. We also take on ambitious interns who want to go deep on single-cell genomics, scalable systems, or applied AI for biology.

Ways to get started:

- **Build with the tools.** `pip install cytetype`, or grab [Scarf](https://github.com/NygenAnalytics/scarf) and [CyteTypeR](https://github.com/NygenAnalytics/CyteTypeR).
- **Extend or improve them.** Open an issue or a pull request on any repo. We read every one.
- **Talk to us** about a collaboration, a role, or an internship: [support@nygen.io](mailto:support@nygen.io) or [nygen.io/contact](https://www.nygen.io/contact).

<div align="center">

[Website](https://nygen.io) · [LinkedIn](https://www.linkedin.com/company/nygen) · [X](https://x.com/NygenAnalytics) · [YouTube](https://www.youtube.com/@NygenAnalytics)

<sub>© Nygen Analytics AB · Lund, Sweden</sub>

</div>
