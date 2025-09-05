# Datasets

## Overview

This section documents datasets relevant to prompt engineering and transformer-based function approximation research. The datasets are organized by their primary application: prompt engineering evaluation, function approximation benchmarks, in-context learning assessment, and standard language model benchmarks.

The focus aligns with theoretical frameworks for prompt engineering that approximate smooth functions with transformer prompts, building on recent advances in configurable computational systems and mathematical function learning.

## Available Datasets

### Prompt Engineering & Evaluation

#### 10k_prompts_ranked
- **Name**: 10k_prompts_ranked
- **Source**: Hugging Face - data-is-better-together/10k_prompts_ranked
- **Size**: 10,331 examples with quality rankings
- **Features**: Synthetic and human-generated prompts from various sources, community-ranked quality scores
- **License**: Open source (check HuggingFace for specific terms)
- **Preprocessing**: Prompts collected from existing datasets, ranked by 314 ML community members using Argilla
- **Use Case**: Training and evaluating language models on prompt ranking tasks, studying prompt quality
- **Access**: \`from datasets import load_dataset; ds = load_dataset("DIBT/10k_prompts_ranked")\`

#### Prompt-Perfect Dataset
- **Name**: Prompt-Perfect (scored datasets)
- **Source**: Hugging Face - 0-hero/prompt-perfect
- **Size**: 35+ datasets, >6B tokens scored
- **Features**: Popular datasets scored with "Self-Alignment with Instruction Backtranslation" prompt, includes extracted scores
- **License**: Varies by component dataset
- **Preprocessing**: Datasets scored using GPT-3.5-turbo variants with Chain-of-Thought reasoning
- **Use Case**: Prompt quality assessment, instruction backtranslation research
- **Access**: Available through Hugging Face datasets library

### Function Approximation & Mathematical Learning

#### Symbolic Regression Datasets
- **Name**: Scientific Discovery Symbolic Regression
- **Source**: Multiple sources (Feynman equations, physics formulas)
- **Size**: Varies (typically 100-10,000 equations per dataset)
- **Features**: Mathematical expressions, variable relationships, physical constants
- **License**: Mixed (academic use typically permitted)
- **Preprocessing**: Symbolic expressions converted to numerical datasets with noise handling
- **Use Case**: Testing transformer ability to discover mathematical relationships and function approximation
- **Access**: Available through symbolic regression research repositories

#### NIERT Interpolation Datasets
- **Name**: Numerical Interpolation datasets (TFRD, Mathit, PhysioNet, PTV)
- **Source**: Research paper implementations
- **Size**: Varies by subdataset
- **Features**: Scattered data points for numerical interpolation tasks
- **License**: Academic research use
- **Preprocessing**: Unified encoder representation for observed and target points
- **Use Case**: Testing numerical interpolation capabilities of transformers
- **Access**: Available at https://github.com/DingShizhe/NIERT

### In-Context Learning Assessment

#### ICLEval Benchmark
- **Name**: ICLEval (In-Context Learning Evaluation)
- **Source**: Research implementation
- **Size**: Multiple task categories with varying sizes
- **Features**: Exact copying and rule learning subtasks
- **License**: Open source (check repository)
- **Preprocessing**: Designed to isolate ICL-specific capabilities
- **Use Case**: Evaluating in-context learning abilities separate from general knowledge
- **Access**: Available at https://github.com/yiye3/ICLEval

#### Context Tuning Datasets
- **Name**: CrossFit, UnifiedQA, MMLU, BIG-Bench Hard, ARC
- **Source**: Multiple benchmark sources
- **Size**: Varies (MMLU: 15,908 questions, BIG-Bench: thousands of tasks)
- **Features**: Multi-domain tasks for few-shot adaptation
- **License**: Academic research use
- **Preprocessing**: Task-specific demonstration examples for context initialization
- **Use Case**: Context tuning and in-context optimization research
- **Access**: Standard benchmark repositories

### Standard Language Model Benchmarks

#### GLUE & SuperGLUE
- **Name**: General Language Understanding Evaluation / SuperGLUE
- **Source**: https://gluebenchmark.com / https://super.gluebenchmark.com
- **Size**: GLUE: 9 tasks, SuperGLUE: 8 more challenging tasks
- **Features**: Natural language understanding tasks (classification, QA, inference)
- **License**: Mixed (check individual task licenses)
- **Preprocessing**: Standardized formats across tasks
- **Use Case**: General language understanding evaluation baseline
- **Access**: \`datasets.load_dataset("glue", task_name)\` or \`datasets.load_dataset("super_glue", task_name)\`

#### MMLU (Massive Multitask Language Understanding)
- **Name**: MMLU
- **Source**: https://github.com/hendrycks/test
- **Size**: 15,908 multiple-choice questions across 57 subjects
- **Features**: Academic subjects from elementary to professional levels
- **License**: MIT License
- **Preprocessing**: Standardized multiple-choice format
- **Use Case**: Broad knowledge and reasoning evaluation
- **Access**: \`datasets.load_dataset("lukaemon/mmlu")\`

#### BIG-Bench
- **Name**: Beyond the Imitation Game Benchmark
- **Source**: https://github.com/google/BIG-bench
- **Size**: 200+ tasks across diverse domains
- **Features**: Novel evaluation tasks beyond current model capabilities
- **License**: Apache 2.0
- **Preprocessing**: Standardized API across diverse task types
- **Use Case**: Pushing boundaries of language model evaluation
- **Access**: BIG-Bench repository with standardized evaluation framework

## Specialized Datasets for Function Approximation

### FIND (Function INterpretation and Description)
- **Name**: FIND Benchmark
- **Source**: Research implementation (OpenReview)
- **Size**: Procedurally constructed functions across domains
- **Features**: Black-box functions resembling neural network components with descriptions
- **License**: Research use
- **Preprocessing**: Functions involve noise, composition, approximation, and bias
- **Use Case**: Automated interpretability methods, function behavior description
- **Access**: Check OpenReview paper for implementation details

### Deep Symbolic Regression Datasets
- **Name**: Meta Symbolic Regression Dataset
- **Source**: https://symbolicregression.metademolab.com
- **Size**: Large-scale synthetic mathematical functions
- **Features**: End-to-end symbolic regression with transformers
- **License**: Research use
- **Preprocessing**: Data points (x∈R^D, y∈R) for function discovery
- **Use Case**: Testing transformer ability to output mathematical functions from data points
- **Access**: Interactive web interface and downloadable datasets

## Benchmarks & Evaluation Protocols

### Function Approximation Benchmarks
- **Feynman Equations Dataset**: Physics-based symbolic regression
- **SRBench**: Comprehensive symbolic regression benchmark
- **AI Feynman Dataset**: Automated physics equation discovery

### Prompt Engineering Benchmarks
- **Prompt Benchmark**: Systematic evaluation across ARC, HellaSwag, TruthfulQA, MMLU
- **SafetyPrompts.com**: 149 datasets for LLM safety evaluation
- **StyleRec**: Prompt recovery in writing style transformation

### In-Context Learning Benchmarks
- **ICLEval**: Copying and rule learning assessment
- **Long-Context ICL**: Evaluation with thousands of demonstrations
- **Meta-ICL**: Training for improved in-context learning

## Data Access Instructions

### General Access Patterns

#### Hugging Face Datasets
\`\`\`python
from datasets import load_dataset

# Load prompt ranking dataset
ds = load_dataset("DIBT/10k_prompts_ranked")

# Load SuperGLUE benchmark
ds = load_dataset("super_glue", "boolq")  # specific task

# Load MMLU benchmark
ds = load_dataset("lukaemon/mmlu", "abstract_algebra")  # specific subject
\`\`\`

#### Repository-Based Datasets
\`\`\`bash
# Clone symbolic regression repositories
git clone https://github.com/DingShizhe/NIERT
git clone https://github.com/yiye3/ICLEval
git clone https://github.com/google/BIG-bench

# Follow repository-specific setup instructions
cd repository_name
pip install -r requirements.txt
python setup.py install
\`\`\`

#### API-Based Access
\`\`\`python
# For datasets requiring special handling
import requests

# Example: Accessing symbolic regression data
url = "https://symbolicregression.metademolab.com/api/dataset"
response = requests.get(url, params={"dataset": "feynman"})
data = response.json()
\`\`\`

### Preprocessing Requirements

1. **Prompt Datasets**: Tokenization, length filtering, quality score normalization
2. **Function Datasets**: Numerical stability checks, range normalization, symbolic parsing
3. **Benchmark Datasets**: Task-specific formatting, evaluation metric alignment
4. **ICL Datasets**: Demonstration selection, context length management

### License Compliance

- **Academic Use**: Most datasets permit academic research
- **Commercial Use**: Check individual dataset licenses
- **Attribution**: Cite original papers and dataset creators
- **Data Sharing**: Respect redistribution terms

### Storage and Computing Requirements

- **Small Datasets** (<1GB): Local storage sufficient
- **Medium Datasets** (1-10GB): Consider cloud storage for team access
- **Large Datasets** (>10GB): Distributed storage and processing recommended
- **Computational Requirements**: Function approximation tasks may require GPU resources