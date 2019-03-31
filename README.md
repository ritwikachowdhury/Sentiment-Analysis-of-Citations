# Sentiment-Analysis-of-Citations

This project aims to identify the positive and negative sentiment polarity of
citations to research papers. We have done literature survey on this topic and
found out that though this sounds quite similar to the sentence based sentiment
analysis, the sentence based sentiment analysis does not work quite well in this
case due to numerous reasons. To list a few of them:-
a) Sentiments are not explicitly depicted in most citations because of two
major reasons. Firstly citations mostly describe an approach or state a fact.
Secondly, works are cited mostly in a neural way.
b) The lexical items used to express sentiments is different in scientific texts
and general sentences.
c) The scope of influence of citations varies widely from a single clause to
several paragraphs.
All of these reasons make the task more challenging.
We are using a sentiment annotated corpus of scientific text. We have seen that
the current state of the art features for sentiment analysis are:-
Ngrams: An n-gram is a contiguous sequence of words in a given text. The
character n refers to the length of this sequence. If n = 1, the sequence is called a
unigram, if n = 2 or 3, it is called a bigram or trigram, respectively. N-grams of
length 1 and 2 have been shown to perform well in existing sentiment
classification tasks for movie reviews (Pang et al., 2002).
Parts of speech tag: POS tags as features help the classifier distinguish between
word forms with different parts-of-speech. In some cases, this is correlated with
the word form having different senses.
Dependency structures: Dependency structures describe the grammatical
relationships between words. We aim to capture the long distance relationships
between words.
Sentence splitting: Removing irrelevant polar phrases around a citation improves
results. For this purpose, each sentence is splitted by trimming its parse tree.
Walking from the citation node (<CIT>) towards the root, the subtree rooted at
the first sentence node (S) is selected and the rest is ignored.
Window based negotiation:- Das and Chen (2001) used a window-based
approach, where they orthographically modify all words within a fixed window
which follow a negation word. Councill et al. (2010) used features from a
dependency parser in a CRF framework to detect the scope of negation.
A k-fold cross validation method is used and the metrics to be used for comparing
the results are both the macro-F and micro-F scores. The n gram with n=3 works
the best. The window based negation method improves the performance as well.
There are numerous applications of the sentiment citation analysis. We are
planning to present an application on improving the bibliometric measures. In
traditional bibliometrics, the impact of a research article is usually measured by
citation frequency. Citation sentiment analysis could be used to improve the
existing bibliometrics measures by introducing different weights, based on the
specific sentiments of the citations.
