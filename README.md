<img src="https://svgshare.com/i/R3P.svg" width="200" height="200" align="right"/> 

# PatternOmatic 0.2.*

**\#AI · \#EvolutionaryComputation · \#NLP**

[![Built with spaCy](https://img.shields.io/badge/made%20with%20❤%20and-spaCy-09a3d5.svg)](https://spacy.io)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Build Status](https://travis-ci.org/revuel/pip-example-pkg-revuel.svg?branch=master)](https://travis-ci.org/revuel/pip-example-pkg-revuel) 
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=revuel_pip-example-pkg-revuel&metric=coverage)](https://sonarcloud.io/dashboard?id=revuel_pip-example-pkg-revuel)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=revuel_pip-example-pkg-revuel&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=revuel_pip-example-pkg-revuel)
[![PyPI](https://img.shields.io/pypi/v/pip-example-pkg-revuel?color=purple&label=latest)](https://pypi.org/project/pip-example-pkg-revuel/)
[![PyPI version](https://badge.fury.io/py/pip-example-pkg-revuel.svg)](https://badge.fury.io/py/pip-example-pkg-revuel)

_Finds patterns matching a given Spacy Doc set_

## Requirements
- [Python 3.7.3](https://www.python.org/downloads/release/python-373/)
- [Spacy 2.3.*](https://spacy.io/usage/v2-3)

## Basic usage

### From sources
*Clone SCM official repository*

`git clone git@github.com:revuel/PatternOmatic.git`

*Play with Makefile*

- `make venv` to activate project's [Virtual Environment](https://docs.python.org/3.7/library/venv.html)
- `make libs` to install dependencies
- `make test` to run Unit Tests
- `make coverage` to run Code Coverage
- `make run` to run PatternOmatic's script with example parameters

### From package
*Install package*

`pip install PatternOmatic`

*Play with the CLI*

```
# Show help 
patternomatic.py -h

# Usage example
patternomatic.py -s Hello world -s Goodbye world
```

*Play with the library*
```
""" PatternOmatic library client example. Find linguistic patterns to be used by the Spacy R.B. Matcher """
from PatternOmatic.api import find_patterns
from PatternOmatic.settings.config import Config

if __name__ == '__main__':

    my_samples = ['I am a cat!', 'You are a dog!', 'She is a rabbit!']

    # Optionally, let it evolve a little bit more!
    config = Config()
    config.max_generations = 100

    patterns_found = find_patterns(my_samples)

    print(f'Patterns found: {str(patterns_found)}')
```
---

## Features

### General purpose

&#9989; No OS dependencies, no storage or database required!

&#9989; Lightweight package with just a few pip dependencies
- Spacy
- Spacy's en_core_web_sm Language Model

&#9989; Easy and highly configurable to boost clever searches

&#9989; Includes basic logging mechanism

&#9989; Includes basic reporting, JSON and CSV format supported. Report file path is configurable

&#9989; Configuration file example provided (config.ini)

&#9989; Default configuration is run if no configuration file provided

&#9989; Given a wrong argument a falling back actions is executed

### Evolutionary

&#9989; Basic Evolutionary (Grammatical Evolution) parameters available and configurable

&#9989; Supports two different Evolutionary Fitness functions

&#9989; Supports Binary Tournament Evolutionary Selection Type

&#9989; Supports Random One Point Crossover Evolutionary Recombination Type

&#9989; Supports "µ + λ" Evolutionary Replacement Type

&#9989; Supports "µ ∪ λ" with elitism Evolutionary Replacement Type

&#9989; Supports "µ ∪ λ" without elitism Evolutionary Replacement Type

&#9989; Evolutionary common performance metrics included:
- Success Rate (SR)
- Mean Best Fitness (MBF)
- Average Evaluations to Solution (AES)

### Linguistic

&#9989; [Compatible with any Spacy Language Model](https://spacy.io/usage/models#languages)

&#9989; [Supports all Spacy's Rule Based Matcher standard Token attributes](https://spacy.io/usage/rule-based-matching#adding-patterns-attributes)

&#9989; [Supports the following Spacy's Rule Based Matcher non standard Token attributes](https://spacy.io/api/token#attributes) [(via undersocre)](https://spacy.io/usage/processing-pipelines#custom-components-attributes)
- ent_id
- ent_iob
- ent_kb_id
- has_vector
- is_bracket
- is_currency
- is_left_punct
- is_oov
- is_quote
- is_right_punct
- lang
- norm
- prefix
- sentiment
- string
- suffix
- text_with_ws
- whitespace

&#9989; Supports skipping boolean Token attributes

&#9989; [Supports Spacy's Rule Based Matcher Extended Pattern Syntax](https://spacy.io/usage/rule-based-matching#adding-patterns-attributes-extended)

&#9989; [Supports Spacy's Rule Based Matcher Grammar Operators and Quantifiers](https://spacy.io/usage/rule-based-matching#quantifiers)

&#9989; [Supports Token Wildcard](https://spacy.io/usage/rule-based-matching#adding-patterns-wildcard)

&#9989; Supports defining the maximum number of features per token to be searched

&#9989; Supports usage of no repeated features


---

Author: [Miguel Revuelta (revuel)](mailto:revuel22@hotmail.com "Contact author"), a humble AI enthusiastic
