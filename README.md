## Overview

A simple NLP pipeline that trains a CNN to perform sentiment analysis on movie reviews. Built using SpaCy.

## Installation

First set up dependencies in a virtual environment:

```
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

Download English model for spaCy and the movie review dataset:

```
python -m spacy download en_core_web_sm
curl -s https://ai.stanford.edu/~amaas/data/sentiment/aclImdb_v1.tar.gz | tar xvz
```

## Example Usage

Set the `TEST_REVIEW` variable and then run:

```console
$ python sentiment_analyzer.py
Training model
Beginning training
Loss    Precision       Recall  F-score
11.293997120810673      0.7816593886121546      0.7584745762390477      0.7698924730851658
1.979159922178951       0.8083333332996527      0.8220338982702527      0.8151260503859189
[...]
0.000415042785704145    0.7926829267970453      0.8262711864056664      0.8091286306718204
Testing model
Review text:
Transcendently beautiful in moments outside the office, it seems almost
sitcom-like in those scenes. When Toni Colette walks out and ponders
life silently, it's gorgeous.<br /><br />The movie doesn't seem to decide
whether it's slapstick, farce, magical realism, or drama, but the best of it
doesn't matter. (The worst is sort of tedious - like Office Space with less humor.)

Predicted sentiment: Positive   Score: 0.8773064017295837
```
