## Chapter 4. Acquire Initial Dataset
### Iterate on Datasets
choosing an initial dataset, updating it, and augmenting it. 

### Explore Your First Dataset
1. starting with <span style="color:blue">small</span> dataset

2. checking data <span style="color:blue">quality</span>.
- format?
- which data is _noisy_ or _incorrect_?
- how many inputs are hard to _understand_?
- if the data has labels, do you _agree_ with them

3. checking data <span style="color:blue">quantity</span> and <span style="color:blue">distribution</span>
- if _large_, extract a small dataset
- if _small_, the model risks being biased as the data
- for _small_ dataset, increase the diversity by data _gathering_ and _augmentation_ (add more data for small cluster/outliers, the best way to deal with such biased examples is to gather **additional data** to make your training set more representative)

| Quality| Format|Quantity and Distribution|
| -------| ------|-------------------|
| Are any relevant fields ever <span style="color:red">empty</span>?| How many <span style="color:red">processing</span> steps does your data require? | How many <span style="color:red">examples</span> do you have?|
| Are there potential <span style="color:red">errors</span> of measurement? | Will you be able to preprocess it the <span style="color:red">same</span> way in production? | How many examples <span style="color:red">per</span> class? Are any <span style="color:red">absent</span>? |

### Label to Find Data Trends
1. <span style="color:blue">summary</span> statistics for <span style="color:blue">each</span> of the <span style="color:blue">features</span> you have, such as average and histogram plots
2. visualing <span style="color:blue">individual data points</span>
- clustring (both here and evaluate model performance)
>How **many** clusters do you identify in your dataset?
>
>Do each of these clusters seem **different** to you? In which way?
>
>Are any clusters much more **dense** than others? If so, your model is likely to struggle to perform on the sparser areas. Adding features and data can help alleviate this problem.
>
>Do all clusters represent data that seems as “hard” to model? If some clusters seem to represent more **complex** data points, make note of them so you can revisit them when we evaluate our model’s performance.

- vectorizing, tabular data (normalize continuous feature (mean is zero, variance is one), one-hot encoding for categorized feature)
**Use the mean and standard deviation from training for testing and validation**

- dimension reduction
>identifying groups of similar data points and explore them

3. Be the <span style="color:blue">algorithm</span>
- **labeling** the data yourself
- Choosing a modeling approach involves making almost as many **assumptions** about our data as building heuristics, so it makes sense for these assumptions to be data driven
>separate a dataset into few meaningful clusters
>label few data points per cluster
>identifying trends and discover important predictors
>update data processing strategy 
>back to step 1

4. after knowing the trend
- creating a **feature** that characterizes that trend or by using a model that will easily **leverage** it.

5. building features out of patterns 
- adding additional features, the more data you have the less feature engineering you need
- feature crosses: nonlinear combination of features 