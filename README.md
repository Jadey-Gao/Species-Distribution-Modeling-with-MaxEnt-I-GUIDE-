# Species Distribution Modeling with MaxEnt: Predicting Suitable Coffee Cultivation Areas on Hawaii Island

**Author:** Yibin Gao ([@Jadey-Gao](https://github.com/Jadey-Gao))

A single-notebook workflow for teaching MaxEnt species distribution modeling on the [I-GUIDE Platform](https://i-guide.io/).

- **Question:** where can coffee be grown on Hawaii Island?
- **Inputs:** 6,014 coffee presence points + 18 environmental raster layers (EPSG:26905).
- **Approach:** a baseline vs. tuned comparison, so the effect of feature classes, regularization, background size, and variable selection stays visible.
- **Goal:** unpack the MaxEnt "black box" by exposing the choices between input and suitability map.

![Jackknife variable importance](jackknife_importance.png)

## Contents

| Path | Description |
| --- | --- |
| [Species_Distribution_Modeling_with_MaxEnt.ipynb](Species_Distribution_Modeling_with_MaxEnt.ipynb) | The complete workflow |
| [Data_HawaiiCropProject/](Data_HawaiiCropProject/) | Crop presence points and environmental rasters |
| [MaxEnt_Baseline/](MaxEnt_Baseline/) | Baseline suitability raster |
| [MaxEnt_Tuned/](MaxEnt_Tuned/) | Tuned suitability rasters (cloglog and raw) |
| [jackknife_importance.png](jackknife_importance.png) | Pre-saved jackknife chart |

## Roadmap

1. **Introduction** — what MaxEnt is, and why coffee.
2. **Data and Operational Inputs** — presence points and the raster stack, with verification steps.
3. **Scenario 1 — Baseline** — linear + quadratic features, β = 1.0, 10,000 background points, all 18 variables.
4. **Scenario 2 — Tuned** — 90-combination grid search, then maps, ROC curves, permutation and jackknife importance, and response curves.
5. **Key Takeaways, Limitations, and References.**

## References

- Melrose, J., & Delparte, D. (2012). *Hawaii County Food Self-Sufficiency Baseline 2012.* University of Hawaii at Hilo.
- Kemp, K. K. (2012). *The Hawai'i Island Crop Probability Map.* Los Angeles: USC GIS Research Lab.
- Anderson, C. B. (2023). elapid: Species distribution modeling tools for Python. *Journal of Open Source Software*, 8(84), 4930. https://doi.org/10.21105/joss.04930
