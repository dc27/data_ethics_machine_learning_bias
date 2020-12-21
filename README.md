# Ethics in Data: Bias in Machine Learning Algortihms

This was a brief talk I gave to my fellow students at CodeClan on the topic  of bias in Machine Learning algorithms. The inspiration for the talk came from Cathy O'Neil's book: [Weapons of Math Destruction](https://weaponsofmathdestructionbook.com/).

Contents:

* Machine Learning overview
* Sources of bias
* Removing existing bias
* Avoiding bias

## Machine Learning

What is machine learning (ML) and how does it work?

Machine learning is a subset of Artificial Intelegence (AI). At this point in time, machine learning algorithms are everywhere. They areguiding user recommendations on media platforms like Netflix and YouTube. They are detecting fraudulent transactions. They are tracking and predicting your shopping trends. They are deciding who gets interviewed for jobs. But how do they work - how do machines learn?

A definition:

> Machine learning algorithms are algorithms that improve automatically through experience. [^1]

Traditional computer algorithms work more like following a set of instructions, taking an input and producing an output. The example often used to illustrate this is that of baking a cake. You have your inputs - the ingredients; the set of instructions - the recipe, and finally you have your output - a cake.

ML makes use of algorithms that take a set of input data, analyse the data, and use the analysis to produce/predict a measurable output. New data is input to the ML algorithm, and it optimises its operations. The more times this process is repeated, the greater the degree of optimasation of the ML algorithm.

### Supervised learning

In supervised learning, the ML algorithm is "taught" by example. The ML algorithm is provided with labelled data from a training (example) dataset, with input-output pairs. and the expected outputs (success criteria). The ML algorithm must find a method to determine how to produce the desired output. The algorithm is then corrected by the developer. This process of feeding and tuning the algorithm is repeated.

There are other types of machine learning are: unsupervised learning, reinforcement learning, and semi-supervised learning. This presentation will only focus on avoiding bias in supervised learning.

* potential to introduce you to a new type of cake based on your preferences
* work out how much weight you put on the uses/quantitiies of certain ingredients
* you never need to explicitly code a recipe

Advancements in technology, specifically in computational power and data storage, mean that it's easier to run and train ML algorithms over larger and larger sets of data. 

## Sources of bias

People associate and promote machines as unbiased decision makers. As uncaring, impar

Algorithms will not remove existing bias, only reflect and perpetuate it.


There are three main sources of bias in ML algorithms - **Technical** bias relating to software or hardware limitations; **Established** bias relating to bias that exists within the data; and **Emergent** bias which relates to bias in the success criteria.

### Technical bias



### Established bias

It's not the algorithm that's biased, it's your training data.

### Emergent bias

What is your success criteria? If Facebook wants to keep you engaged, it's only going to favour content that you spend time looking at.

Sometimes, decisions made by systems aimed at personalization will end up creating bias "bubbles" around us. We can look no further than the current state of Facebook to see this bias at play. At the top layer, Facebook users see the posts of their friends and can share information with them. Unfortunately, any algorithm that uses analysis of a data feed to then present other content will provide content that matches the idea set that a user has already seen. This effect is amplified as users open, like, and share content. The result is a flow of information that is skewedd toward a user's existing belief set.

while it is certainly personalized, and often reassuring, it is no longer what we would tend to think of as news. It is a bubble of information that is an algorithmic version of "confirmation bias." Users don't have to shielf themselves from information that conflicts with their beliefs because the system is automatically doing it for them.

The impace of these information biases on the world of news is troubling. But as we look to social media models as a way to support decision making in the enterprise, systems that support the emergence of information bubbles have the potential to skey our thinking. A knowledge worker who is only getting information from people who think like them will never see contrasting points of view and will tend to ignore and deny alternatives.

## Removing existing bias

How do you remove bias that exists in your ML algorithm?

This is difficult. First, you must investigate your algorithm to detect potential sources of bias. Inspect the results (the output/recommendation) of the algorithm. If there is favour toward a particular group/outcome then perhaps you need to consider and adjust your success criteria.

Since another potential source of bias is established bias, the training data should also be inspected. If there is a biased sample then some wrangling of the seed data to remove the bias may be necessary. It's important, also, to consider proxies at this stage. Proxies refer to the occurence of related data. It can be the case that what appears to be unrelated unbiased data is the opposite. An example could be location data. The company Amazon used what they thought was unbiased data in determing who was eligible for prime delivery. The data they used was based on location and it was found to be the case that people living in Black neighbourhoods were further from Amazon distribution centres and therefore less likely to be eligible for prime delivery than White customers.

## Avoiding bias

Be aware of the potential sources of bias - technical, established, emergent.

* Include transparency in results  
* Consider carefully your success criteria  
* Find for whom the algorithm fails 


Technical bias: increase algorithm transparency. Test edge cases.


[^1]: https://en.wikipedia.org/wiki/Machine_learning