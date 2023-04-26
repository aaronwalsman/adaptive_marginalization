# Adaptive Marginalization
Categorical distributions with softmax are ubiquitous in machine learning.
Your model produces a vector of unnormalized log-probabilities for a set of categories, then you use softmax to convert these to a normalized distribution.
If you have a specific target category, you can supervise using a cross-entropy loss, or if instead you have a sample from the distribution and a reward, you can use some form of policy gradient.
Pretty standard stuff.

What do you do though, if you know for a given data point that multiple categories are equivalent to each other?
This may come up if you're not sure which categories are good, but you know 
