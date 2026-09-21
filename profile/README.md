<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://www.nygen.io/static/img/nygen-logo-white.png">
    <img src="https://www.nygen.io/static/img/nygen-logo.png" alt="Nygen" width="230">
  </picture>

  Open-source tools and AI agents for single-cell biology.

  [Website](https://nygen.io) · [CyteType docs](https://www.nygen.io/docs/cytetype) · [Scarf docs](https://scarf.readthedocs.io)

</div>

---

We are **Nygen Analytics**, an applied AI lab in Lund, Sweden. Single-cell experiments now produce millions of cells per study, and the bottleneck has moved from sequencing and compute to interpretation: what each cell is, and what it is doing. We build tools for that layer, and we keep the evidence attached to every result so you can trace it and defend it.

## Start here

| Repository | What it does | Install |
| :-- | :-- | :-- |
| **[CyteType](https://github.com/NygenAnalytics/CyteType)** | Evidence-backed cell type annotation for Scanpy / AnnData. Returns cell type, state, Cell Ontology ID, confidence, and an interactive HTML report for every cluster. | `pip install cytetype` |
| **[CyteTypeR](https://github.com/NygenAnalytics/CyteTypeR)** | The same annotation workflow for Seurat objects. | `devtools::install_github("NygenAnalytics/CyteTypeR")` |
| **[Scarf](https://github.com/NygenAnalytics/scarf)** | Memory-efficient analysis of scRNA-seq, scATAC-seq, CITE-seq, and multi-omic data. Streams from local or remote Zarr stores, so millions of cells fit on a laptop. | `pip install scarf` |
| **[CyteOnto](https://github.com/NygenAnalytics/CyteOnto)** | Semantic comparison of cell type labels in Cell Ontology embedding space. This is how we score predicted annotations against ground truth beyond exact string matches. | Hosted service, no key needed. See the repo. |

### Annotate a clustered dataset

```bash
pip install cytetype
cytetype setup   # browser sign-in; free for academic and non-commercial research
```

```python
from cytetype import CyteType

annotator = CyteType(adata, group_key="clusters", rank_key="rank_genes_clusters", n_top_genes=100)
adata = annotator.run(study_context="Human PBMC from a healthy donor")
```

Each cluster comes back with an annotation, a Cell Ontology term, a confidence score, and the marker-level evidence behind the call. [Try it in Colab](https://colab.research.google.com/drive/1aRLsI3mx8JR8u5BKHs48YUbLsqRsh2N7?usp=sharing) or [open an example report](https://cytetype.nygen.io/report/e70e2883-7713-4121-94f2-5b57eabd1468?v=260303).

### Analyse atlas-scale data

Scarf runs quality control, feature selection, graph building, embedding, clustering, and marker search out of core, inside a memory budget you set. Results are fingerprinted by their inputs and parameters, so changing one setting recomputes only what depends on it. Start with the [scRNA-seq tutorial](https://scarf.readthedocs.io/en/latest/tutorials/scrna_seq.html).

## How the pieces fit

- **Scarf** is the analysis engine. It also powers **[ScarfWeb](https://www.nygen.io/products/scarfweb)**, our browser-based workbench for secondary analysis.
- **CyteType** and **CyteTypeR** are clients for our hosted annotation service. Specialised agents weigh competing hypotheses against the full expression data and external databases, and a review step checks every call.
- **CyteOnto** is the benchmark layer. We use it to evaluate CyteType against other annotators, and you can use it to evaluate yours.

## Publications

- Ahuja G, Antill A, Su Y, Dall'Olio GM, Basnayake S, Karlsson G, Dhapola P. **Multi-agent AI enables evidence-based cell annotation in single-cell transcriptomics.** bioRxiv, 2025. [doi:10.1101/2025.11.06.686964](https://www.biorxiv.org/content/10.1101/2025.11.06.686964v1)
- Dhapola P, Rodhe J, Olofzon R, Bonald T, Erlandsson E, Soneji S, Karlsson G. **Scarf enables a highly memory-efficient analysis of large-scale single-cell genomics data.** Nature Communications 13, 4616, 2022. [doi:10.1038/s41467-022-32097-3](https://www.nature.com/articles/s41467-022-32097-3)

Scripts and notebooks behind the CyteType paper are in [CyteType_manuscript](https://github.com/NygenAnalytics/CyteType_manuscript).

## Get help, contribute, or work with us

- **Bugs and feature requests:** open an issue on the relevant repository. We read every one.
- **Questions and discussion:** join the [Discord](https://discord.gg/V6QFM4AN).
- **Collaborations, benchmarking on your data, roles, and internships:** [contact@nygen.io](mailto:contact@nygen.io) or [nygen.io/contact](https://www.nygen.io/contact).

<div align="center">

[Website](https://nygen.io) · [LinkedIn](https://www.linkedin.com/company/nygen) · [X](https://x.com/NygenAnalytics) · [YouTube](https://www.youtube.com/@NygenAnalytics)

<sub>© Nygen Analytics AB · Medicon Village, Lund, Sweden</sub>

</div>
