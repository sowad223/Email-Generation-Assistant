# Email Generation Assistant: Project Documentation

## 1. Project Overview
This project implements an **AI-Powered Email Generation Assistant** designed for professional corporate environments. The system transforms raw inputs (Intent, Facts, and Tone) into structured, ready-to-send business emails using advanced LLM prompting techniques.

## 2. Technical Implementation
- **Engine**: Groq API
- **Models Compared**:
    - **Model A**: Llama 3.3 70B (Few-Shot + Chain-of-Thought)
    - **Model B**: Llama 3.1 8B (Zero-Shot)
- **Architecture**: A pipeline consisting of a prompt engine, a custom evaluation suite, and a visualization module.

## 3. Custom Evaluation Suite
To ensure production quality, three automated metrics were developed:
1. **Fact Recall**: Measures the percentage of input facts successfully integrated into the email using keyword density analysis.
2. **Tone Accuracy**: Utilizes an LLM-as-a-Judge approach to score adherence to the requested stylistic tone.
3. **Conciseness Score**: A penalty-based metric that rewards emails for maintaining professional brevity around a 100-word target.

## 4. Key Findings
Based on the comparative testing across 10 business scenarios:
- **Model A** demonstrated superior structural reliability and conciseness.
- **Model B** was faster but exhibited higher verbosity and lower factual density.

## 5. Deployment Recommendation
**Model A (70B Few-Shot)** is recommended for production deployment due to its high factual integrity and professional stylistic consistency.
