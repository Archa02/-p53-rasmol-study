# -p53-rasmol-study
# 🧬 Effect of Point Mutations on Protein Structure Stability
### A RasMol-based Study


---

## 📌 Overview

This project investigates the structural consequences of point mutations in the **p53 tumor suppressor protein** using **RasMol**, a molecular graphics visualization tool. By comparing the wild-type and mutant (R273H) forms of p53, the study demonstrates how even a single amino acid substitution can significantly disrupt protein conformation and impair biological function.

---

## 🎯 Objectives

- To understand how point mutations alter protein 3D structure
- To visualize structural differences between wild-type and mutant p53 using RasMol
- To analyze the functional consequences of the R273H mutation
- To demonstrate the utility of RasMol for educational structural bioinformatics

---

## 🦠 Protein of Interest: p53 Tumor Suppressor

| Property | Details |
|----------|---------|
| **Protein** | p53 Tumor Suppressor |
| **Wild-type PDB ID** | [1TUP](https://www.rcsb.org/structure/1TUP) – Human p53 bound to DNA |
| **Mutant PDB ID** | [2OCJ](https://www.rcsb.org/structure/2OCJ) – p53 with R273H point mutation |
| **Mutation** | Arginine (R) → Histidine (H) at position 273 |
| **Significance** | One of the most common mutations in human cancers |

---

## 🛠️ Tools & Software

| Tool | Version | Purpose |
|------|---------|---------|
| **RasMol** | v2.7.5 | 3D visualization and structural comparison |
| **RCSB Protein Data Bank** | — | Source for `.pdb` structure files |
| **Notepad++** | — | Writing and editing RasMol scripts |
| **MS Paint / Photoshop** | — | Annotating and labeling screenshots |

---

## 📁 Repository Structure

```
p53-rasmol-study/
│
├── README.md                   # Project overview (this file)
│
├── data/                       # PDB structure files
│   ├── 1TUP.pdb                # Wild-type p53
│   └── 2OCJ.pdb                # Mutant p53 (R273H)
│
├── scripts/                    # RasMol command scripts
│   ├── wildtype_visualization.rasmol
│   ├── mutant_visualization.rasmol
│   └── comparison_commands.rasmol
│
├── results/                    # Output images and analysis
│   ├── wildtype_p53.jpg        # RasMol screenshot - wild-type
│   ├── mutant_p53.jpg          # RasMol screenshot - mutant
│   └── structural_comparison.md
│
└── images/                     # Figures and diagrams
```

---

## 🔬 Methodology

### 1. Protein Selection
Both wild-type (1TUP) and mutant (2OCJ) p53 structures were downloaded from the **RCSB Protein Data Bank** in `.pdb` format.

### 2. Visualization Pipeline

```bash
# Load wild-type structure
load 1TUP.pdb

# Render secondary structures
cartoons

# Highlight alpha helices in red
select helix; color red

# Highlight beta sheets in yellow
select sheet; color yellow

# Zoom for close-up view
zoom 150

# Export visualization
write image.jpg
```

### 3. Structural Observations
- **Mutation site** location and environment assessed visually
- **Alpha helices and beta sheets** compared for presence/integrity
- **Surface accessibility** and residue exposure changes noted
- Screenshots taken for side-by-side comparison

---

## 📊 Key Results

### Structural Feature Comparison

| Structural Feature | Wild-type p53 (1TUP) | Mutant p53 R273H (2OCJ) |
|-------------------|---------------------|------------------------|
| **Alpha Helices** | Seven well-formed helices, stable | Partial unravelling near residue 273 |
| **Beta Sheets** | Tightly aligned, no gaps | Slight misalignment; less compact |
| **Residue at 273** | Arginine — small, hydrophilic, buried | Histidine — bulkier, hydrophobic, exposed |
| **Surface Accessibility** | Position 273 shielded from solvent | Noticeably greater solvent exposure |
| **Hydrogen Bond Network** | Intact; anchors DNA-binding loop firmly | Several bonds broken; loop destabilised |
| **DNA Binding Capacity** | Fully functional | Severely impaired |

### Key Finding
> The R273H mutation introduces a **bulkier, more hydrophobic histidine** in place of the small, hydrophilic arginine. This disrupts the local hydrogen bond network, increases surface exposure, and impairs the protein's ability to bind DNA — ultimately leading to loss of tumor-suppressing function.

---

## 🖼️ Figures

**Figure 1:** Wild-type p53 highlighting the R273 residue (red) within the DNA-binding surface.

**Figure 2:** Mutant p53 structure with H273 showing outward orientation and solvent exposure.

*(See `/results/` folder for full-resolution RasMol screenshots)*

---

## ⚠️ Limitations

While RasMol provides valuable qualitative insights, it lacks:
- Simulation of protein flexibility or motion over time
- Quantification of energetic penalties due to mutation
- Visualization of interaction dynamics with DNA or ligands

**Future work** could incorporate tools like **GROMACS** (molecular dynamics) or **PyMOL / Swiss-Model** for quantitative and dynamic analysis.

---

## 📖 Conclusion

This study demonstrates that even a **single amino acid change** (R273H) can significantly alter protein conformation in functionally critical regions such as the DNA-binding domain of p53. The findings align with established literature on loss-of-function p53 mutations in cancer, and reinforce the value of computational visualization in structural biology education.

---

## 📚 References

1. Cho, Y. et al. (1994). Crystal structure of a p53 tumor suppressor-DNA complex. *Science*, 265(5170), 346–355.
2. Joerger, A. C., & Fersht, A. R. (2008). Structural Biology of the Tumor Suppressor p53. *Annual Review of Biochemistry*, 77, 557–579.
3. Berman, H. M. et al. (2000). The Protein Data Bank. *Nucleic Acids Research*, 28(1), 235–242.
4. Sayle, R. A., & Milner-White, E. J. (1995). RasMol: Biomolecular graphics for all. *Trends in Biochemical Sciences*, 20(9), 374–376.
5. Petsko, G. A., & Ringe, D. (2004). *Protein Structure and Function*. New Science Press.

---

## 👩‍🔬 Author

**Archa S**
