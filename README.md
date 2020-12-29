# Ethics in Data: Bias in Machine Learning Algortihms

This was a talk I gave to my fellow students at CodeClan on the topic  of bias in Machine Learning algorithms. The inspiration for the talk came from Cathy O'Neil's book: [Weapons of Math Destruction](https://weaponsofmathdestructionbook.com/).

Contents:

* Machine Learning overview
* Sources of bias
* Removing existing bias
* Avoiding bias

## Machine Learning

What is machine learning (ML) and how does it work?

Machine learning is a subset of Artificial Intelegence (AI). Machine learning algorithms can be found in almost all areas of society. They are guiding and promoting users' recommendations on media platforms like Netflix and YouTube; they are detecting fraudulent transactions; tracking and predicting your shopping trends; and performing financial market analysis; they are automatically filtering candidates before job interviews. But how do they work - how do machines learn?

A definition:

> Machine learning algorithms are algorithms that improve automatically through experience. [^1]

Traditional computer algorithms work more like a set of instructions that take in an input and produce an output. This is similar to a recipe in baking a cake - the inputs are the ingredients, the algorithm is the recipe, and the output is the baked cake.

```{r}
bake_cake <- function(ingredients) {
    cake_mix_measured <- measure(ingredients)
    cake_mix_mixed <- mix(cake_mix_measured)
    return(bake(cake_mix_mixed))
}
```

ML algorithms differ from conventional algorithms in that the instructions are not explicitly coded. The ML algorithm is not told exactly how to produce a certain output, but is instead trained on what an expected output would be if given a specific input. There are many ways to "teach" a machine learning algorithm. One of the ways is supervised learning.

### Supervised learning

In supervised learning, the ML algorithm is taught by example. The ML algorithm is provided with labelled data from a training (example) dataset, with input-output pairs. and the expected outputs. The ML algorithm must find a method to determine how to produce the desired output. The algorithm is then corrected by the developer. This process of feeding and tuning the algorithm is repeated.

Advancements in technology, specifically in computational power and data storage, mean that it's easier to run and train ML algorithms over larger and larger sets of data.

n.b. There are other types of machine learning are: unsupervised learning, reinforcement learning, and semi-supervised learning. This presentation will only focus on avoiding bias in supervised learning.

## Sources of bias

People often associate computer algorithms as being unbiased and impartial when informing decisions but algorithms taught by humans are vulnerable to many sources of biases. Importantly, algorithms will not remove existing bias, only reflect and perpetuate it.

There are three main sources of bias in ML algorithms - **technical** bias which relates to software or hardware limitations; **established** bias which relates to bias that exists within the training data; and **emergent** bias which relates to bias created by the success criteria.

### Technical bias

Technical bias relates to the limitations of the system, e.g. computational power. Technical bias can also be a limitation of the design of the program. A search engine which displays a limited number of resutls could be viewed as favouring certain results.

Another example case is upon the reliance of random number generation - if the RNG is predictable (not random) then the algorithm can be biased by favouring certain outcomes.

Because human behaviour and decision making is complex and reliant on many latent factors, technical bias can also emerge when trying to explicitly declare instructions to mimic human behaviour.

### Established bias

Machine Learning algorithms have to be trained with an initial training dataset during supervised learning. If there exists any underlying bias (which could related to age, sex, gender, race, socio-economic status etc.) within the training data, the algorithm will retain and perpetuate the same bias if not corrected. 

### Emergent bias

Emergent bias is the bias occuring due to the use and reliance on the ML algorithm. Algorithms may not have been adjusted to consider new or changing knowledge. Similarly, problems may emerge when training data do not align with contexts that an algorithm encounters with real world data.

Types of emergent biases include unanticipated uses and feedback loops.

<u>Unanticipated Uses</u>
<br>
> Unanticipated uses may emerge from the end user relying on the software rather than their own knowledge.[^2]

<u>Feedback Loops</u>
<br>
If data collected for an algorithm results in real-world responses which are fed back into the algorithm, a feedback loop can be created which would further enforce any bias created by the dataset the algorithm is acting on.

> Recommender systems such as those used to recommend online videos or news articles can create feedback loops.[^3]

## Removing existing bias

How is bias removed from ML algorithms?

This is difficult. The algorithm must be investigated to detect potential sources of bias. The results (the output/recommendation) of the algorithm must be inspected as well as the inputs (the training data) and the algorithm design and architecture. If there is favour toward a particular group/outcome then the success criteria, algorithm design, and architecture will need to reviewed. If, after inspecting the trainning data, the data is found to be biased then the seed data will need to be reviewed. Either the data or algorithm will need to wrangled to accomodate for the inherent bias, or a different seed data will need to be chosen.

## Avoiding bias

Instead of removing bias from an ML algorithm, it may be easier to attempt to avoid bias initially. This can be achieved by, first, being aware of the potential sources of bias - technical, established, emergent. With this awareness the algorithm can be designed in a way that allows for developers to examine the results and inspect for bias. The algorithm can be designed and built in a way that allows for developers to update the algorithm - to make changes to success criteria to avoid or reduce the existence of feedback loops or to cater to users not initially considered. The training data can also be examined for bias and reviewed before the algorithm is live.

Cathy O'Neil has an excellent quote that algorithm developers and architects should consider throughout algorithm development and review:

> For whom does this fail?

Summarised:

* Include transparency in results  
* Consider carefully your success criteria
* Identify sources of bias within training data and account for them 
* Find for whom the algorithm fails 


[^1]: https://en.wikipedia.org/wiki/Machine_learning
[^2]: https://en.wikipedia.org/wiki/Algorithmic_bias
[^3]: https://en.wikipedia.org/wiki/Algorithmic_bias