# In-Context Learning

## Understanding Prompt Tuning and In-Context Learning via Meta-Learning (Genewein et al., 2025)

**ArXiv ID:** 2505.17010  
**Authors:** Tim Genewein, Kevin Wenliang Li, Jordi Grau-Moya, et al.

### 6-Point Analysis Framework

**1. Problem**  
- Limited conceptual understanding of prompting despite empirical success
- Gap between prompt optimization methods and theoretical foundations
- Need to understand optimal prompting conditions and limitations

**2. Prior Assumptions**
- Prompting methods developed primarily through empirical observation
- Manual prompt construction or optimization without theoretical guidance
- Limited understanding of when prompting can/cannot work optimally

**3. Insight**
- Optimal prompting can be understood through Bayesian view of meta-trained networks
- Meta-trained neural networks behave as Bayesian predictors with rapid in-context adaptation
- Formal criteria can determine when optimal prompting is possible for target tasks

**4. Technical Approach**
- Bayesian formulation of reasoning problems
- Both model-based and model-free approaches for slow-thinking framework
- Educational experiments on LSTMs and Transformers comparing prefix-tuning and weight-tuning
- Analysis of soft prefixes manipulating activations beyond hard tokens

**5. Evaluation**
- Theoretical analysis supported by experiments
- Comparison of different prefix-tuning versions and weight-tuning methods
- Demonstrates soft prefixes effectiveness for trained and untrained networks

**6. Impact**
- Provides theoretical foundation for understanding prompting limitations
- Bridges conceptual gap between empirical methods and formal understanding
- Establishes criteria for optimal prompting applicability

## Context Tuning for In-Context Optimization (Lu, 2025)

**ArXiv ID:** 2507.04221

### 6-Point Analysis Framework

**1. Problem**
- Traditional prompt adaptation initializes with irrelevant tokens
- Limited effectiveness of few-shot adaptation without parameter fine-tuning
- Need for improved lightweight adaptation methods

**2. Prior Assumptions**
- Random or irrelevant token initialization is acceptable for prompt training
- Prompt-based adaptation effectiveness is inherently limited
- In-Context Learning ability cannot be better leveraged for adaptation

**3. Insight**
- Initializing trainable prompts with task-specific demonstration examples
- Leveraging model's inherent ICL ability for improved few-shot learning
- Task-specific initialization provides better starting point than random tokens

**4. Technical Approach**
- Context Tuning method with demonstration-initialized prompts
- Utilizes task-specific examples for prompt initialization
- Maintains model parameters frozen while optimizing context-initialized prompts

**5. Evaluation**
- Extensive evaluation on CrossFit, UnifiedQA, MMLU, BIG-Bench Hard, ARC
- Outperforms traditional prompt-based adaptation methods
- Competitive accuracy to Test-Time Training with higher training efficiency

**6. Impact**
- Significantly enhances few-shot adaptation effectiveness
- Maintains computational efficiency while improving performance
- Demonstrates better utilization of model's inherent capabilities

## The Broader Spectrum of In-Context Learning (Lampinen et al., 2024)

**ArXiv ID:** 2412.03782

### 6-Point Analysis Framework

**1. Problem**
- Limited perspective on in-context learning focusing only on supervised few-shot learning
- Need for unified understanding of diverse in-context abilities
- Gap between different manifestations of in-context learning

**2. Prior Assumptions**
- In-context learning primarily refers to supervised few-shot learning
- Different in-context abilities are separate phenomena  
- Limited connection to broader learning and adaptation concepts

**3. Insight**
- Any sequence distribution where context decreases subsequent prediction loss can be interpreted as in-context learning
- Unified perspective encompasses instructions, role play, time series extrapolation, and more
- Generalization can be studied across multiple dimensions: novelty, flexibility, and application

**4. Technical Approach**
- Formalized broader definition of in-context learning
- Analysis of various in-context capabilities including instructions and role play
- Connection to linguistic dependencies like coreference and parallel structures
- Framework for studying generalization dimensions

**5. Evaluation**
- Theoretical framework supported by analysis of existing literature
- Demonstrates connections between diverse in-context phenomena
- Identifies generalization patterns across different manifestations

**6. Impact**
- Provides unified theoretical framework for understanding in-context learning
- Connects to broader literature in meta-learning and goal-conditioned agents
- Establishes foundation for studying generalization in in-context capabilities