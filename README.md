# fastai_notebooks
This notebook was inspired by Jeremy's Lesson 2 discussion of Figure 1(a) in the paper "High Temperature and High Humidity Reduce the Transmission of COVID-19" at https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3551767.

We show how to empirically determine the p-value via Monte Carlo simulation, and apply this method to the data from Figure 1(a).

The notebook is organized as follows:

In Section 1 we work out how to generate random synthetic data sets that are consistent with the null hypothesis, and look qualitatively similar to the actual data in Figure 1(a). Because we don't have the actual datapoints, we rely on our eyeballs to tell us when our synthetic data looks close to the actual data.

In Section 2, we examine one of our synthetic data sets.

Next, in Section 3 we perform a Monte Carlo simulation, generating an ensemble of 10,000 randomly drawn synthetic data sets. For each data set, we measure and record the slope of the fitted linear R-value vs. Temperature model.

Then, in Section 4, we determine the p-value for rejection of the null hypothesis, which is the fraction of the 10,000 synthetic data sets for which the slope was steeper than -0.023, the slope in the actual data set.

Finally, in Section 5, we discuss the significance of the p-value obtained.
