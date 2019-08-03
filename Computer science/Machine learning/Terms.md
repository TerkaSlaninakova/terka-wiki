# Terms

## Curse of dimensionality
Idea: The more columns you have, the more 'empty space'. The more dimensions i have, the more all of the points sit on the edge of that space. So basically in high dimensions everything sits on edge and the distance between points is much less meaningful and this encourages us to remove as many columns as possible to avoid this.

**BUT** actually points do still have meaningful distances, k-NN and k means still work really well in high dimensions, so this is really a theoretical idea that's not supported by what we see in practice.


## No free lunch theorem
Claim: There is no type of model that wokrs well for any kind of dataset. This is true for **random datasets**. In practice we work with datasets that were created with a purpose, there's a structure, relationships there. So we're not using random ones, and there are techniques that work better than others (a lot of the times it's ensembles of decision trees).