# Ethics in Data: Bias in Machine Learning Algortihms

This was a brief talk I gave to my fellow students at CodeClan on the topic  of bias in Machine Learning algorithms. The inspiration for the talk came from Cathy O'Neil's book: [Weapons of Math Destruction](https://weaponsofmathdestructionbook.com/).

Contents:

* Machine Learning overview
* Sources of bias
* Removing existing bias
* Avoiding bias

## Machine Learning

What is machine learning (ML) and how does it work?

Machine learning is a subset of Artificial Intelegence (AI). At this current moment in time, machine learning algorithms can be found in almost all areas of society. They are guiding users' recommendations on media platforms like Netflix and YouTube. They are detecting fraudulent transactions; tracking and predicting your shopping trends; and performing financial market analysis. They are automatically filtering candidates before job interviews. But how do they work - how do machines learn?

A definition:

> Machine learning algorithms are algorithms that improve automatically through experience. [^1]

Traditional computer algorithms work more like a set of instructions that take in an input and produce an output. This is similar to a recipe in baking a cake. The inputs are the ingredients, the algorithm is the recipe, and the output is the baked cake.

```{r}
bake_cake <- function(ingredients) {
    cake_mix_measured <- measure(ingredients)
    cake_mix_mixed <- mix(cake_mix_measured)
    return(bake(cake_mix_mixed))
}
```

ML algorithms differ from conventional algorithms in that the instructions are not explicitly coded. The ML algorithm is not told exactly how to produce a certain output, but is instead trained on what an expected output would be if given a specific input. There are many ways to "teach" a machine learning algorithm. One of the ways is supervised learning:

### Supervised learning

In supervised learning, the ML algorithm is taught by example. The ML algorithm is provided with labelled data from a training (example) dataset, with input-output pairs. and the expected outputs. The ML algorithm must find a method to determine how to produce the desired output. The algorithm is then corrected by the developer. This process of feeding and tuning the algorithm is repeated.

There are other types of machine learning are: unsupervised learning, reinforcement learning, and semi-supervised learning. This presentation will only focus on avoiding bias in supervised learning.

Advancements in technology, specifically in computational power and data storage, mean that it's easier to run and train ML algorithms over larger and larger sets of data. 

## Sources of bias

While people often associate computer algorithms as unbiased and impartial decision makers, they are vulnerable to many sources of biases. Importantly, algorithms will not remove existing bias, only reflect and perpetuate it.

There are three main sources of bias in ML algorithms - **technical** bias which relates to software or hardware limitations; **established** bias which relates to bias that exists within the training data; and **emergent** bias which relates to bias created by the success criteria.

### Technical bias

Technical bias is associated with the limitations of the system. If your algorithm is only able to look at the first thousand rows of a dataset that contains millions, or if your face recognition technology can only examine a certain degree, then you are likely to get an incorrect and possibly biased product as a result.

### Established bias

Bias may already exist within the training data.

### Emergent bias

What is your success criteria? If Facebook wants to keep you engaged, it's only going to favour content that you spend time looking at.

## Removing existing bias

How do you remove bias that exists in your ML algorithm?

This is difficult. First, you must investigate your algorithm to detect potential sources of bias. Inspect the results (the output/recommendation) of the algorithm. If there is favour toward a particular group/outcome then perhaps you need to consider and adjust your success criteria.

Since another potential source of bias is established bias, the training data should also be inspected. If there is a biased sample then some wrangling of the seed data to remove the bias may be necessary. It's important, also, to consider proxies at this stage. Proxies refer to the occurence of related data. It can be the case that what appears to be unrelated unbiased data is the opposite. An example could be location data. The company Amazon used what they thought was unbiased data in determing who was eligible for prime delivery. The data they used was based on location and it was found to be the case that people living in Black neighbourhoods were further from Amazon distribution centres and therefore less likely to be eligible for prime delivery than White customers.

## Avoiding bias

Be aware of the potential sources of bias - technical, established, emergent.

* Include transparency in results  
* Consider carefully your success criteria
* Identify sources of bias within training data and account for them 
* Find for whom the algorithm fails 


[^1]: https://en.wikipedia.org/wiki/Machine_learning