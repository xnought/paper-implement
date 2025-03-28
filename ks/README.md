# Kolmogorov Smirnov Test

## Links

- https://www.itl.nist.gov/div898/handbook/eda/section3/eda35g.htm
- https://www.wikiwand.com/en/articles/Kolmogorov%E2%80%93Smirnov_test

## Notes

- Goodness of fit test: check whether the data comes from a distribution. Or if two distributions come from the same distribution.
- Similar to Chi squared test, but no assumption about the underlying distributions. Chi squared requires binning which sucks.
- For example, use KS test on voxels to test between task and control in fMRI
- $H_0$ is data come from the same distribution. $H_a$ is that the data don't come from the same distribution.
- Test from the maximal difference between CDF. Critical value computed from KS distribution.
- If you get a critical value below the threshold, then you can reject the null hypothesis that the data came from the same distribution.
- Called D statistic, in practice use with ECDF since we don't have the theoretical CDF
