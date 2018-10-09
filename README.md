The Great Pacific Garbage Patch is a collection of garbage that sits between California and Hawaii. It is about about twice the size of Texas and its filled mostly with plastic.  

The Great Pacific Garbage Patch is the largest of 5 oceanic gyres. Gyres are systems of circulating ocean currents that have the effect of corralling garbage.   

In Fall 2018, the Ocean Cleanup Project launched a ground breaking effort to clean up the Great Pacific Garbage Patch, with projections to reduce the area by 50 percent in 5 years.

But several issues remain. First, some scientists estimate that only 3 – 5 percent of total oceanic garbage ends up in one of these gyres so targeting these areas will only solve part of the problem.Second, the clean up systems don't capture dangerous microplastics.

Microplastics are pieces of plastic that are under a half a centimeter. Some common examples are small fragments of plastics that have broken off of larger pieces, microbeads that are common in personal hygiene products like toothpaste and face wash, and microfibres that come off clothing in the wash.

But there is very limited data available on the worldwide prevalence of microplastics. Even the largest datasets are limited to about 2500 samples while there are about 4.6 times 10 the 12 possible locations where microplastics could be. So this leads to a problem. We need to clean up plastic in earth's rivers and oceans, but how can we do that if we don't know where to look?

For my passion project at Metis, I decided to tackle this problem by predicting densities of microplastics in rivers and oceans. My approach was to use the data we have, which is admittedly imperfect, to predict locations where microplastics are likely to be found, and thus help target clean up efforts.  

Because detailed information on microplastics is limited, I decided to bring in several external sources of data for feature engineeriing, for example location and population of cities as well as location and amount of water discharge from major river mouths worldwide. I used this information to supplement densities of microplastics.

First I mapped locations where microplastics were found in rivers and oceans. You may notice that they are concentrated mostly in North American and in the Atlantic Ocean, which likely reflects the sampling methods. In other words, its easier to collect data closer to home. But there are samples taken from within oceanic gyres as well as from river and coastal locations, and even from more remote locations off of Madagascar and Antartica.

Next I did some exploratory analyses which showed that microplastics were more likely to be found in ocean samples than river samples. This makes intuitive sense because one mechanism by which microplastics are thought to end up in the ocean is via drainage systems which carry them to rivers, which carry them eventually out to sea.  

To best predict densities of microplastics, I iterated through a series of different types of regressions. The features that I used were the latitude and longitude where the samples were collected, whether samples were collected in salt or freshwater, the samples' proximity to major cities and the population in those cities, and finally the samples' proximity to major river mouths and the annual amount of water discharge from those rivers. For quantifying model error, I focused on the root mean squared error or RMSE.

The RMSE for the highest performing model, which was a gradient boosted regression, showed that the model was off by about 19 pieces of microplastic per litre. Relative to the RMSE of the  baseline model (30 pieces/litre), this was a big improvement.  

Lastly, I used the model to make predictions for locations wherein we don't have data. One example came from a location about 500 km south east of Tai Pei. The model predicts that a sample taken here would have about 30 pieces of microplastic per liter. Given that the model estimates are off by about 19 pieces per liter, the exact number of pieces of plastics is likely to be slightly off, but its also likely that this is a good place to look.

So while the model might not perfectly predict the exact densities of microplastics in a given location, it can provide us with a rough idea of whether or not plastics will be present, and so its a good place to start.
