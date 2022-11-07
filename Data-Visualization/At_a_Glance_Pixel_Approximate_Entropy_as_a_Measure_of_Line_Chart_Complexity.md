# At a Glance: Pixel Approximate Entropy as a Measure of Line Chart Complexity

[G. Ryan  (2019)](https://ieeexplore.ieee.org/document/8440849)


## Introduction

This research proposes a measure of visual complexity, Pixel Approximate Entropy (PAE), to examine the line charts. The correlation between PAE values and users' judgement is found.

## Method
* PAE
    * Distance $d(w^m_i,w^m_j)$: ![](https://i.imgur.com/3EqhO4s.png)
    * Similarity $S^m_i(r)$: the percentage of windows whose distance is below a threshold $r$
    * Similarity Score $\Phi^m(r)={\frac{1}{W}\Sigma^W_{i=1}\log(S^m_i(r))}$: sum the similarity scores in log form for all possible windows (**log probability** that windows will be closer than $r$)
    * Approximate entropy $E(m,r,N)=[\Phi^m(r)-\Phi^{m+1}(r)]$: the increased probability that the distance will be greater than $r$ apart when sequences length (windows) $+1$


## Results

* PAE is correlated with noise added to chart
* PAE is correlated with perceived complexity
* Identify changes: hard to find difference as the entropy increases
* Identify base function: hard to identify shapes as the entropy increases
* Glance time is important on identify differenece

## Discussion
Modify PAE to other types of data visualizations, such as bar charts, may be possible extensions.
Doing research on deriving measures to guide designers in making understandable charts or to generate charts automatically can be considered.
