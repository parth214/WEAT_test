# WEAT_test

The largest GloVe model trained on 800 billion tokens has been used in all tasks.

### 1) Using the following targets and attributes in the provided order and the largest gloVe model trained on 800 billion tokens, compute the WEAT effect-size and p-value both with the normal distribution generated by 1,000 iterations and the empirical distribution generated by 1,000,000 iterations.

target1= woman, mother
target2= man, father
attribute1= health, happy
attribute2= pollute, tragedy

WEAT Effect Size = 1.1705697
p-value with the normal distribution generated by 1,000 iterations = 0.12584685047458494
p-value with the empirical distribution generated by 1,000,000 iterations = 0.167018

d is high but the p-value is above the threshold of 10^(-2). P value may be high due to the less number of attributes and targets used.

### 2) SC-WEAT effect-size and p-value with an empirical distribution generated via 1,000,000 permutations for the case sensitive words "Parth", "weat", and "AylinCaliskan".

attribute1 = caress, freedom, health, love, peace, cheer, friend, heaven, loyal, pleasure, diamond, gentle, honest, lucky, rainbow, diploma, gift, honor, miracle, sunrise, family, happy, laughter, paradise, vacation

attribute2 = abuse, crash, filth, murder, sickness, accident, death, grief, poison, stink, assault, disaster, hatred, pollute, tragedy, divorce, jail, poverty, ugly, cancer, kill, rotten, vomit, agony, prison

WEAT effect sizes -0.03590634359010653 and -0.1544695499596644 are noticed for "Parth" and "weat" respectively. The p values of both are too high over the threswhold (0.548877 and 0.704144 respectively).

For the token "AylinCaliskan" since an embedding wasnt available, I used Regular Expressions to split the token by capital letters, that is 'Aylin' and 'Caliskan'. Then glove embeddings were generated for both words separately and the mean of them was used. A function get_glove_vec is used to do all of these subtasks.

WEAT effect size of -0.32843477256190995 was noted and p value of 0.874219 is found.

Thus for the 3 cases for SC WEAT, the p value is too high and the null hypothesis is rejected.

Colab link :  https://colab.research.google.com/drive/12mHpIbxXdqtTflWUtClFzEEcJYWvZRtK#scrollTo=hU96nnZdnxFL
### The ipynb contains the executed code run for the above tasks.

### References: 

Caliskan, A., Bryson, J. J. and Narayanan, A. (2017) Semantics derived automatically from language corpora contain human-likebiases. Science, 356 (6334). pp. 183-186. ISSN 0036-8075

