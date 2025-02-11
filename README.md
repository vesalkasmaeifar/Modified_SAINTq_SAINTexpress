# **Modified SAINTq and SAINTexpress for Enhanced Sensitivity**

## **What does this repository show?**
This repository contains **modified versions of SAINTq and SAINTexpress**, originally developed for high-confidence protein-protein interaction identification in BioID and AP-MS datasets.

The **original SAINT software** can be found here:  
[SAINT Official Page](https://saint-apms.sourceforge.net/Main.html)

### **Status of this Work**
- A **full evaluation of these modifications** is currently in preparation by **Kasmaeifar et al.**, in collaboration with the **original SAINT developers**.
- The results provided here are **preliminary** and subject to further validation.

---

## **What Changes Were Made?**  
In both SAINTq and SAINTexpress, the **hardcoded minimum threshold** for intensity differences between baits and controls was removed:  

- **SAINTq:** `log2(4) → log2(1)`  
- **SAINTexpress:** `log(4) → log(1)`  

### **Why Was This Threshold Originally Set?**  
In the original SAINT models, a **minimum difference threshold** was enforced between the bait and control intensity distributions. This threshold artificially **raised** smaller differences to at least `log2(4)` (in SAINTq) and `log(4)` (in SAINTexpress). The intended purpose of this hardcoded separation was to minimize false positives by ensuring only strong intensity differences contributed to interactor identification.  

### **What Is the Impact of Removing It?**  
By removing this forced separation and allowing the observed values to be used directly:  

✅ **Higher Sensitivity**  
- The modified versions can now **detect interactors that exhibit smaller, yet biologically meaningful differences** between bait and control.  
- This is particularly beneficial for proteins that interact weakly or transiently, as they might otherwise be **artificially suppressed** by the threshold.  

✅ **More Accurate Intensity-Based Scoring**  
- The original threshold **distorted** real intensity values by imposing a fixed minimum difference.  
- By allowing **true intensity differences** to be used as they are, the modified SAINT models better reflect **the actual biological interaction landscape**.  

✅ **Improved Detection of Low-Abundance Interactors**  
- Many **weak interactors** that previously fell below the artificial threshold were either **missed** or **artificially boosted to the threshold**.  
- With this modification, **smaller but statistically significant changes** are now properly incorporated into the scoring model.  

### **Why Is This Important?**  
- The original models may have been **too conservative**, leading to **under-detection of real interactions**.  
- By adjusting this threshold, **the model remains specific but gains sensitivity**, making it more useful for **proximity labeling and AP-MS experiments** where small but meaningful intensity shifts matter.  

---

## **Preliminary Results**
- **Higher sensitivity** at the same Bayesian False Discovery Rate (BFDR) threshold.
- Increased detection of interactors that align with **known biological interactions**.
- Example dataset (ACTB, KRT8, LMNA, MAPRE3):
  - **Original SAINTexpress:** Less than 3 preys per bait at **1% BFDR**.
  - **Modified version:** Significantly more interactors detected.

---

## **Where Are the Compiled Binaries?**
- **SAINTq:** The new compiled binary is located in [`bin/`](bin/).
- **SAINTexpress:** The new compiled binary is located in [`bin/`](bin/).

These binaries are **ready to run** and can be used just like the original SAINT software.

---

## **How to Cite This GitHub Repository**
If you use this modified version of SAINTq/SAINTexpress, please cite this GitHub repository:

**[GitHub Repository URL]**  
DOI: **[Zenodo DOI Once Available]**

**Example Citation Format:**
