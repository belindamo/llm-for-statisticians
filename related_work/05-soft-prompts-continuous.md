# Soft Prompts and Continuous Prompting

## SoftCoT: Soft Chain-of-Thought for Efficient Reasoning (Xu et al., 2025)

**ArXiv ID:** 2502.12134  
**Authors:** Yige Xu et al.

### 6-Point Analysis Framework

**1. Problem**
- Hard token decoding constrains reasoning within discrete vocabulary space
- Continuous-space reasoning methods require full-model fine-tuning
- Catastrophic forgetting limits applicability to well-performing LLMs
- Need for continuous reasoning without modifying core LLM parameters

**2. Prior Assumptions**
- Hard token decoding is optimal for reasoning tasks
- Continuous reasoning requires extensive model modification
- Discrete vocabulary space is sufficient for complex reasoning

**3. Insight**
- Lightweight fixed assistant model can generate instance-specific soft thought tokens
- Continuous reasoning possible without modifying core LLM architecture
- Trainable projection module can map soft tokens to LLM representation space

**4. Technical Approach**
- Fixed assistant model for speculative soft thought token generation
- Trainable projection module for representation space mapping
- Parameter-efficient fine-tuning approach
- Black-box LLM compatibility maintained

**5. Evaluation**
- Enhanced performance on five reasoning benchmarks
- Supervised, parameter-efficient fine-tuning demonstrates improvements
- Maintains LLM performance while adding reasoning capabilities
- Effective across different reasoning task types

**6. Impact**
- Enables continuous-space reasoning without full model fine-tuning
- Provides parameter-efficient approach to reasoning enhancement
- Maintains compatibility with existing high-performing LLMs

## Leveraging Self-Attention for Input-Dependent Soft Prompting (Muppidi et al., 2025)

**ArXiv ID:** 2506.05629  
**Authors:** Ananth Muppidi, Abhilash Nandy, Sambaran Bandyopadhyay

### 6-Point Analysis Framework

**1. Problem**
- Traditional soft prompting uses static prompts regardless of input
- Parameter-efficient fine-tuning needs better adaptation to input variations
- Limited effectiveness of existing soft prompting approaches for diverse inputs

**2. Prior Assumptions**
- Static soft prompts are sufficient for task adaptation
- Input-independent prompting can handle task variations effectively
- Uniform attention to prompt tokens is optimal

**3. Insight**
- Input-dependent soft prompts can better adapt to specific input characteristics
- Self-attention mechanism can dynamically weight prompt token importance
- Generating prompts based on input tokens improves adaptability

**4. Technical Approach**
- Input Dependent Soft Prompting with self-Attention Mechanism (ID-SPAM)
- Generates soft prompts based on input tokens
- Varies attention importance across different tokens dynamically
- Maintains small number of trainable parameters

**5. Evaluation**
- Compared to state-of-the-art techniques across various tasks
- Improved zero-shot domain transfer capability
- Demonstrates superior performance with minimal parameter increase
- Enhanced feature separability in latent space

**6. Impact**
- Introduces dynamic adaptation to soft prompting approaches
- Improves domain transfer capabilities significantly
- Maintains parameter efficiency while enhancing adaptability

## CIE: Controlling Language Model Text Generations Using Continuous Signals (Samuel et al., 2025)

**ArXiv ID:** 2505.13448  
**Authors:** Vinay Samuel, Harshita Diddee, Yiming Zhang, Daphne Ippolito

### 6-Point Analysis Framework

**1. Problem**
- Limited control over language model generation properties (length, complexity, sentiment)
- Natural language prompts and discrete signals are brittle and hard to scale
- Need for fine-grained control along continuous spectrums

**2. Prior Assumptions**
- Natural language prompts provide sufficient control
- Discrete control signals can capture all necessary variations
- Binary or categorical controls are adequate for generation properties

**3. Insight**
- Continuous control signals enable precise property control along spectrums
- Vector interpolation between "low" and "high" embeddings provides fine-grained control
- After fine-tuning, continuous signals can reliably control model behaviors

**4. Technical Approach**
- Continuous control signals as interpolated vectors between embeddings
- Case study in controlling precise response length
- Fine-tuning approach for learning continuous control mappings
- Vector representation of control properties

**5. Evaluation**
- More reliable response-length control than in-context learning
- Superior performance compared to discrete signal fine-tuning methods
- Demonstrates effectiveness of continuous control paradigm
- Precise control over generation properties

**6. Impact**
- Establishes new paradigm for continuous generation control
- Enables fine-grained property control in language models  
- Provides reliable alternative to discrete control approaches