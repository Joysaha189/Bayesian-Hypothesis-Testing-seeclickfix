#  Bayesian Hypothesis Testing

Bayes-optimal classification of 529 citizen service requests from the SeeClickFix 311 platform (Albany County) across four categories: Parking Enforcement, Code Violations, Signs, and Traffic Signal Repairs. This project was completed as a part of **IECE 672: Foundations of Statistical Inference** course(Spring 2026) at UAlbany.

Two likelihood models are implemented and compared:
- **Multi-variate Bernoulli** — binary word presence
- **Multinomial** — raw term frequencies

Both use Laplace-smoothed maximum-likelihood estimates over a 2,535-word vocabulary.

## Tasks

- **Task 1** — Binary LRT between two macro-classes: (Parking ∪ Code) vs. (Signs ∪ Traffic).
- **Task 2** — 4-hypothesis test via three pairwise LRTs against a baseline with a shared threshold.

For each task: $P_F$, $P_D$, $P_M$, $P_\epsilon$ are reported across a grid of cost tuples, with full ROC sweep and AUC.

## Results

| Task | Model       | AUC    | Test error |
|------|-------------|--------|------------|
| 1    | Bernoulli   | 0.9907 | 2.6%       |
| 1    | Multinomial | 0.9866 | 3.4%       |
| 2    | Bernoulli   | 0.9916 | 3.8%       |
| 2    | Multinomial | 0.9951 | 1.9%       |

## Layout

├── Code/        Implementation (Bernoulli & multinomial models, metrics, ROC)\
├── Data/        Dataset ((SeeClickFixAlbanyCountyFebruary2018.csv)\
├── Figures/     Generated plots (ROC curves, confusion matrices)\
├── Report/      Final PDF report


The notebook loads the dataset from `Data/` — adjust the file path at the top of the notebook if needed.

See the report PDF in `Report/` for derivations and discussion.


## Author

**Joy Saha**  
Department of Electrical and Computer Engineering\
University at Albany, SUNY  

---

## License

This project is for **academic and educational purposes only**.
