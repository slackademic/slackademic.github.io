---
title: 'Letting Americans Tell Us About What They Think of Politicians In Their Own Words'
subtitle: 'Using Natural Language Processing to Explore and Analyze Responses to Open-Ended Questions About Presidential Candidates'
date: 2020-05-10 12:00:00
description: This page previews my NLP project analyzing responses to open-ended survey questions about presidential candidates.
featured_image: '/images/nlp/candidates_wordcloud.png'
---
<img src="/images/nlp/candidates_wordcloud.png" width="800" height="800" align="center">


## Summary

Using responses to the open-ended questions about the positive and negative attributes of the presidential candidates in the American National Election Studies (ANES), I use Natural Language Processing methods to explore how Americans evaluate the candidates, via:
- Using Bag of Words models to estimate the most popular positive and negative terms in peoples' considerations.
- Comparing how well several supervised learning models predict the sentiment of peoples' responses with Bag of Words and TF-IDF to vectorize the text.
- Employing multiple topic models (LDA, LDA, NNMF) to cluster the responses in the hopes of identifying labels to code individual statements.


[__Check out the project notebook.__](https://github.com/slackademic/Projects/blob/master/nlp_openended_anes.ipynb) But, in the meantime, here are some interesting highlights.

#### Most Frequently Used Bigrams in Candidate Considerations
- I used Bag of Words models to find at the twenty most frequently used bigrams in Americans' positive and negative considerations of the presidential candidates.
- The plots explore popular bigrams from evaluations of the Democratic and Republican candidates, respectively, pooling all three years.
- They also show popular bigrams of Clinton and Trump from 2016 and bigrams of Barack Obama in 2008 and 2012.

<div class="gallery" data-columns="2">
    <img src="/images/nlp/dembigrams_allyears.png">
    <img src="/images/nlp/gopbigrams_allyears.png">
		<img src="/images/nlp/clintonbigrams_2016.png">
    <img src="/images/nlp/trumpbigrams_2016.png">
		<img src="/images/nlp/obamaposbigrams_0812.png">
		<img src="/images/nlp/obamanegbigrams_0812.png">
</div>

#### Topic models
- Pooling positive and negative evaluations, I ran LSA, LDA, and NNMF topic extraction models to cluster the text together (using unigrams, bigrams, and trigrams).
- I explored a range of n's to determine the number of topics.
- I pooled all years and then looked at 2008, 2012, and 2016 separately.
- The figures below reveal a part of this section of the project.

<div class="gallery" data-columns="3">
    <img src="/images/nlp/fourtopics_bigrams_allyears.pdf">
    <img src="/images/nlp/fivetopics_trigrams_allyears.pdf">
    <img src="/images/nlp/fourtopics_bigrams_2016.pdf">
</div>

__See the whole project [here](https://github.com/slackademic/Projects/blob/master/nlp_openended_anes.ipynb).__
