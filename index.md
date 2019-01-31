ciFAIR
======

A duplicate-free variant of the CIFAR test set
----------------------------------------------

The test sets of the popular [CIFAR-10 and CIFAR-100 datasets][1] contain 3.25% and 10% duplicate images, respectively, i.e., images that can also be found in very similar form in the training set or the test set itself.
ciFAIR-10 and ciFAIR-100 are variants of these datasets with modified test sets, where all these duplicates have been replaced with new images.

The training sets have remained unchanged and are identical to those of CIFAR.

We encourage everyone training models on CIFAR to evaluate them on the ciFAIR test sets for an unbiased comparison.


Leaderboard & Pre-Trained Models
--------------------------------

| Model | CIFAR-10 | ciFAIR-10 | CIFAR-100 | ciFAIR-100 | Ressources |
|-------|---------:|----------:|----------:|-----------:|------------|
{% for model_hash in site.data.models %}
{% assign model = model_hash[1] %}
| {{ model.name }} | {{ model.cifar10_perf }}% | {{ model.cifair10_perf }}% | {{ model.cifar100_perf }}% | {{ model.cifair100_perf }}% | [paper]({{ model.paper }}) / [code]({{ model.code }}) / [CIFAR-10 model]({{ model.cifar10_model }}) / [CIFAR-100 model]({{ model.cifar100_model }})
{% endfor %}



[1]: https://www.cs.toronto.edu/~kriz/cifar.html