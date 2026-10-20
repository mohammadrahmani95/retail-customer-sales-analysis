# Validation status

The cleaned notebook contains 30 purposeful cells, reduced from 496 in the original. The original source notebook remains unchanged.

All code cells executed sequentially in a fresh Python 3.12 process through IPython, with no runtime errors. Outputs are saved in the notebook. The runtime included Pandas, NumPy, Matplotlib, SciPy, nbformat, and IPython from the existing Anaconda environment. Notebook structure was validated using nbformat.

Checks passed for overlapping extract equality including multiplicity, required input columns, date parsing, sales duplicate removal, mutually exclusive sales/return classification, return signs, and reconciliation of the Tableau export's gross, return, and net totals. Gross and net merchandise totals match the original project's values.

Six chart PNGs were visually inspected for titles, labels, plotted values, and readability. An HTML preview was generated. The full rendered HTML/notebook page has not been visually inspected in a notebook viewer.

## Remaining Jupyter environment check

The actual Jupyter fresh-kernel execution could not be completed in this restricted desktop environment. A nbclient kernel run stalled before producing outputs; the Jupyter launcher reported Windows error 623 (Illegal System DLL Relocation), and a direct nbconvert invocation also stalled. These attempts were stopped. Sequential execution in a fresh process passed, but this is not a verified Restart Kernel / Run All session.

To verify in the user's normal Anaconda/Jupyter environment, open the notebook from the project folder and choose Restart Kernel → Run All. Alternatively run:

```bash
python -m nbconvert --to notebook --execute --inplace retail_analysis.ipynb
```

## Interpretation repairs

- Return values consistently use positive magnitudes and net revenue subtracts returns once.
- January–November identified customer counts grew by 0.99%; the original conclusion incorrectly described a decline.
- The January–November return comparison is no longer attributed to December cancellations.
- Return ratios are window comparisons, not matched-sale return probabilities.
- Currency symbols were removed because currency documentation was not supplied.
- Unsupported causal explanations were qualified, including product return ratios exceeding 100%.

Project files were published to https://github.com/mohammadrahmani95/retail-customer-sales-analysis on October 20, 2026. Raw CSV files and the large generated Tableau CSV remain local. The supplied Tableau URL is preserved as a profile link; the specific workbook and its freshness remain unverified.

