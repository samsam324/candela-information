# Candela

An AI-assisted platform for quantitative strategy research, backtesting, and iterative model development.

## Overview

Candela is a project I built to reduce the friction between an investment idea and a testable quantitative strategy. The goal is to let a user describe a research hypothesis in natural language, translate it into a structured strategy specification, and evaluate it through a backtesting workflow backed by historical market data.

Rather than acting as a generic chatbot, the system is designed around a concrete research loop:

1. define a hypothesis
2. map it to a tradable universe and signal logic
3. run historical simulation
4. inspect results and diagnostics
5. refine and retest

## What it does

- **Natural-language strategy specification**  
  Converts user prompts into structured strategy definitions, including universe selection, filters, signal logic, and test parameters.

- **Backtesting workflow**  
  Runs historical simulations and returns performance metrics, trade history, and equity curves.

- **Research tooling**  
  Surfaces supporting datasets and documents, including market data, filings, and strategy-related research inputs.

- **Iterative experimentation**  
  Supports refining strategies through repeated prompt-based edits and re-running tests.

- **Advanced modeling workflows**  
  Explores more complex pipelines such as walk-forward validation, regime detection, and model-driven statistical arbitrage.

## Example use cases

- Build and test a mid-cap Canadian biotech screen with founder-based filters
- Prototype a pairs trading pipeline with in-sample pair selection and out-of-sample execution
- Evaluate a regime-aware strategy using Hidden Markov Models and model ensembles
- Combine research inputs such as filings, insider activity, and macro data into a unified testing workflow

## System design

Candela is organized around four main components:

- **AI strategy layer**  
  Interprets prompts and produces structured strategy specifications

- **Research/data layer**  
  Aggregates market and auxiliary research inputs used in strategy construction

- **Backtesting engine**  
  Simulates strategy execution on historical data and computes evaluation metrics

- **User interface**  
  Presents strategy definitions, charts, diagnostics, and supporting research in one workspace

## Why I built it

I wanted a faster way to go from raw market intuition to a reproducible research workflow. Most tools separate idea generation, data exploration, modeling, and backtesting into different systems. Candela is an attempt to unify those steps into a single interface.

## Tech focus

This project emphasizes:

- strategy specification from natural language
- structured research workflows
- reproducible backtesting
- walk-forward evaluation
- integration of ML-driven and statistical strategies

## Screenshots

### Strategy generation

The assistant translates your idea into a strategy specification. You don't need to write code—just review and refine the strategy through conversation. It handles everything from universe selection to signal construction.

> *"Make me a strategy to invest in mid cap Canadian biotech stocks with second time founders."*

![Strategy generation](Screenshot%202026-03-06%20162015.png)

### Backtesting and evaluation

Start by chatting with the AI assistant. Describe your trading idea in plain English. The assistant maps the idea to a concrete universe of assets and builds a strategy specification automatically.

> *"Using a social graph of Donald Trump, his family, and known business associates, build a strategy that invests in companies that they currently run or are actively involved with."*

![Backtesting and evaluation](Screenshot%202026-03-06%20161825.png)

### Research workspace

Dig into SEC filings, insider trading activity, congressional trades, and macroeconomic indicators—all surfaced alongside your charts in a unified workspace.

![Research workspace](Screenshot%202026-03-06%20163510.png)

### Advanced modeling pipeline

Based on the results, you can refine your strategy. Try different parameters, add conditions, or explore entirely new approaches—including advanced methods like walk-forward validation with Hidden Markov Models and XGBoost ensembles.

> *"Run a walkforward test that uses Engle-Granger and other statistical methods to choose pairs in-sample, then train a Hidden Markov Model with 4 states and 4 XGBoost models and use them in a Mixture of Experts to run a statistical arbitrage strategy."*

![Model pipeline](Screenshot%202026-03-06%20165723.png)

## Status

This repository represents an actively developed prototype / research platform. Some components are fully implemented, while others are being expanded as part of the broader system.
