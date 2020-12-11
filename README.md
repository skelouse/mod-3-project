<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Model-Selection-on-Telecom's-Dataset" data-toc-modified-id="Model-Selection-on-Telecom's-Dataset-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Model Selection on Telecom's Dataset</a></span><ul class="toc-item"><li><span><a href="#This-repository-contains" data-toc-modified-id="This-repository-contains-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>This repository contains</a></span></li><li><span><a href="#Questions" data-toc-modified-id="Questions-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Questions</a></span></li><li><span><a href="#Using-the-OSEMN-Process" data-toc-modified-id="Using-the-OSEMN-Process-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Using the OSEMN Process</a></span></li><li><span><a href="#Results" data-toc-modified-id="Results-1.4"><span class="toc-item-num">1.4&nbsp;&nbsp;</span>Results</a></span></li><li><span><a href="#Recommendations" data-toc-modified-id="Recommendations-1.5"><span class="toc-item-num">1.5&nbsp;&nbsp;</span>Recommendations</a></span></li><li><span><a href="#Next-Steps" data-toc-modified-id="Next-Steps-1.6"><span class="toc-item-num">1.6&nbsp;&nbsp;</span>Next Steps</a></span><ul class="toc-item"><li><span><a href="#Repository-Structure" data-toc-modified-id="Repository-Structure-1.6.1"><span class="toc-item-num">1.6.1&nbsp;&nbsp;</span>Repository Structure</a></span></li></ul></li></ul></li></ul></div>

# Model Selection on Telecom's Dataset

![output_115_1.png](/md/output_115_1.png)

**Author**: <a href="https://sites.google.com/skelouse.com/home/">Sam Stoltenberg</a>

## This repository contains
 -  A Jupyter notebook <a href="https://github.com/skelouse/mod-3-project/blob/master/student.ipynb">`student.ipynb`</a> showing our analysis of the King's county housing dataset.
 - The dataset <a href="https://github.com/skelouse/mod-3-project/blob/master/customer_churn_data.csv">itself</a> Obtained from <a href="https://www.kaggle.com/becksddf/churn-in-telecoms-dataset">Customer Churn Dataset</a>
 - A PowerPoint <a href="https://github.com/skelouse/mod-3-project/blob/master/presentation.pdf">presentation</a> of the data
 - Scraped phone number location  <a href="https://github.com/skelouse/mod-3-project/blob/master/phone_prefix_loc.json">data</a>



## Questions

 - Why does a customer decide to leave their provider?
 - What Model will perform the best for the given data?
 - How can this company improve their customer retention?
 - What locations should the company focus on?


## Using the OSEMN Process
- Obtain the data
- Scrub the data
- Explore the data
- Model the data
- Interpret the data
- <a href="https://machinelearningmastery.com/how-to-work-through-a-problem-like-a-data-scientist/">Reference</a>


## Results

![output_79_2.png](/md/output_79_2.png)
<div class="alert alert-info">
    <ul><b>From the model:</b>
<li>The best model yet, and spoiler alert: the best model overall</li>
<li>Only misses 32 classifications of the training data coming out at a 96% prediction</li>
        <li>False positive rate is excellent compared to the other models at 29 - 102</li>
<li>Overfitting the training data</li>
</ul>
</div>


![output_136_1.png](/md/output_136_1.png)
<div class="alert alert-warning">
    <ul><b>From the plot:</b>
<li>The more minutes someone uses the more likely they are to leave their provider</li>
        <li>As minutes correlates to charge, maybe the company should lower their day rate.</li>
</ul>
</div>

<h2>Recommendations:</h2>
<div class="alert alert-success">
  <ul>
    <li>The more minutes a customer uses the more likely they are to switch providers</li>
    <li>Gradient Boosting performed the best on the given data</li>
      <li>The company can improve their customer retention by<ul>
          <li>Charge less for day minutes, as the more minutes someone uses the more likely they are to leave</li>
          <li>Leave more voice mails</li>
          <li>Improve customer service, as people who make more service calls are more likely to change providers.</li></ul></li>
</ul>
</div>


## Next Steps
- Spending more processing power tuning the models, as all the models ran in under 30 seconds.
- Try different models like XGBoost, Extra Trees, and Logistic Classification.
- Running a Linear Regression on some of the important features to extract coefficients.





For any additional questions, please contact <a href="mailto:sam@skelouse.com">Sam Stoltenberg</a>)


### Repository Structure

```
|   customer_churn_data.csv
|   phone_prefix_loc.json
|   presentation.pdf
|   README.md
|   student.ipynb
|   readme.ipynb
|       
\--- styles
|      custom.css

\--- md
|      student.md
|      .png files of all graphs

```
