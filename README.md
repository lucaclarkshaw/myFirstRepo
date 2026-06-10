# myFirstRepo

A learning repo from my summer bootcamp — using GitHub to track code as I go.

---

## Sampling Distribution of the Mean

The main project here is an R notebook (`sampling_distribution.Rmd`) that builds intuition for one of the most important ideas in statistics: **the sampling distribution of the mean**.

### The question it answers

If you draw a random sample from a population and calculate the mean, you get one number. Draw another sample and you get a slightly different number. So what does the *distribution* of all those possible sample means look like — and how does it change as your sample gets bigger?

### What the notebook does

1. **Creates a skewed population** of 100,000 values (a mix of exponential and uniform distributions). It's deliberately non-normal so the results are more interesting.

2. **Simulates 1,000 samples** at three different sample sizes — small (n=5), medium (n=30), and large (n=200) — recording the mean of each sample.

3. **Plots the sampling distributions** side by side so you can see the shape changing as n grows.

4. **Compares observed vs. theoretical standard error** using the formula SE = σ/√n, showing the simulation matches theory closely.

5. **Uses Q-Q plots** to show normality emerging — the Central Limit Theorem made visual.

### Key takeaways

- No matter how skewed the population, the distribution of sample means becomes bell-shaped as n grows — this is the **Central Limit Theorem**.
- Larger samples produce more precise estimates (smaller spread), but with diminishing returns: you need to quadruple n to halve the standard error.
- The mean of all sample means equals the true population mean — the estimator is **unbiased**.

### Files

| File | Description |
|---|---|
| `sampling_distribution.Rmd` | R Markdown source notebook |
| `sampling_distribution.html` | Rendered HTML report (open in browser) |
| `plot1_population.png` | Population distribution |
| `plot2_sampling_distributions.png` | Sampling distributions at n=5, 30, 200 |
| `plot3_se_comparison.png` | Observed vs. theoretical standard error |
| `plot4_qq_plots.png` | Q-Q plots showing normality emerging |
| `analysis.r` | Earlier R scripts from bootcamp exercises |

### Requirements

R packages: `ggplot2`, `dplyr`, `tidyr`, `rmarkdown`

To render the notebook yourself:
```r
rmarkdown::render("sampling_distribution.Rmd", output_format = "html_document")
```
