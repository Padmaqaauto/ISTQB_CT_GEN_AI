# Chapter 01 – Introduction to Generative AI for Software Testing

**Syllabus time allocation:** 100 minutes  
**Source:** ISTQB® Certified Tester – Testing with Generative AI (CT-GenAI) Syllabus v1.1, Chapter 1

## Table of contents

1. [Chapter at a glance](#chapter-at-a-glance)
2. [Learning objectives](#learning-objectives)
3. [Hands-on exercises](#hands-on-exercises)
4. [Chapter summary](#chapter-summary)
5. [Keywords explained](#keywords-explained)
6. [Key takeaways](#key-takeaways)

## Chapter at a glance

This chapter lays the foundations for the rest of the course. It explains what generative AI (GenAI) and large language models (LLMs) are, how they process text, and which kinds of models exist. It then shows how testers can use them across the test process, either through a chatbot or through LLM-powered testing applications.

| Section | Topic | Learning objectives | Hands-on |
|---|---|---|---|
| 1.1 | Generative AI foundations and key concepts | GenAI-1.1.1 to 1.1.4 | HO-1.1.2, HO-1.1.4 |
| 1.2 | Leveraging generative AI in software testing: core principles | GenAI-1.2.1, 1.2.2 | none |

## Learning objectives

| ID | K-level | Learning objective |
|---|---|---|
| GenAI-1.1.1 | K1 | Recall different types of AI: symbolic AI, classical machine learning, deep learning, and generative AI |
| GenAI-1.1.2 | K2 | Explain the basics of generative AI and large language models |
| GenAI-1.1.3 | K2 | Distinguish between foundation, instruction-tuned and reasoning LLMs |
| GenAI-1.1.4 | K2 | Write and execute a given prompt addressing a test task using a multimodal LLM model |
| GenAI-1.2.1 | K2 | Give examples of key LLM capabilities for test tasks |
| GenAI-1.2.2 | K2 | Compare interaction models when using GenAI for software testing |

## Hands-on exercises

Both exercises are level **H1** (guided exercises that follow the trainer's steps).

| ID | Syllabus HO | Level | Exercise | Linked objective | Status |
|---|---|---|---|---|---|
| HO-01-01 | HO-1.1.2 | H1 | [Tokenization and token count evaluation](hands-on/HO-01-01-tokenization-and-token-count.md) | GenAI-1.1.2 | Not started |
| HO-01-02 | HO-1.1.4 | H1 | [Multimodal prompt with text and image input](hands-on/HO-01-02-multimodal-prompt-text-and-image.md) | GenAI-1.1.4 | Not started |

**What each exercise practices**

- **HO-01-01:** use a tokenizer to split sample text into tokens and see how words, punctuation and phrases are represented. Then measure token counts for different inputs and relate them to context-window limits and efficiency.
- **HO-01-02:** review a given prompt with its text and image inputs, run it on a multimodal LLM, and check the response. Note the benefits and the challenges of combining both input types for a test task.

## Chapter summary

### 1.1.1 The AI spectrum

AI is a broad field. Four approaches matter here, and each has different strengths and limits:

| Approach | How it works | Example use in testing |
|---|---|---|
| Symbolic AI | Rule-based. Knowledge is represented with symbols and logical rules that mimic human decision-making. | Decisions that follow explicit rules |
| Classical machine learning | Data-driven. Needs data preparation, feature selection and model training. | Defect categorization, predicting software problems |
| Deep learning | Neural networks learn features automatically from very large, complex data (images, video, audio, text). Humans may still annotate data, tune models or validate results. | Finding patterns in large, complex datasets |
| Generative AI | Uses deep learning to create new content (text, images, code) by learning and mimicking patterns in training data. | Generating test cases, scripts and test data |

The main advantage of GenAI for testing is that **pre-trained models can be applied directly to test tasks without an extra training phase**. This comes with risks, which Chapter 3 covers.

### 1.1.2 Basics of GenAI and LLMs

- LLMs are based on the **generative pre-trained transformer** model and are trained on very large datasets such as books, articles and websites. **Small language models (SLMs)** are compact models with fewer parameters, designed for lightweight, focused solutions.
- **Tokenization** breaks text into tokens, which can be a character, a sub-word or a whole word. **Embeddings** turn each token into a vector in a high-dimensional space. Tokens with similar meaning or role end up close together, which helps the model understand relationships and keep context.
- LLMs use the **transformer** architecture. At inference time the model **predicts the next token** in a sequence. The result is statistically plausible text, but **plausible is not necessarily correct**.
- LLMs are **non-deterministic**: probabilistic inference and hyperparameter settings can produce different outputs from the same input.
- The **context window** is the amount of preceding text (measured in tokens) the model can consider. A larger window helps with long inputs such as large test logs, but it increases computation and processing time.

### 1.1.3 Foundation, instruction-tuned and reasoning LLMs

LLMs are built in progressively more specialized training stages:

| Type | Description | Typical use |
|---|---|---|
| Foundation LLM | General-purpose model trained on vast, diverse data (text, code, images and other modalities). Powerful and flexible, but usually needs further adaptation for specific tasks. | Base for other models |
| Instruction-tuned LLM | Derived from a foundation model and fine-tuned on pairs of prompts and expected responses. Better at following instructions and interpreting user intent. Sometimes called "non-reasoning". | Everyday test tasks that follow clear instructions |
| Reasoning LLM | Extends instruction-tuned models with structured reasoning: logical inference, multi-step problem solving and chain-of-thought. | High-cognitive-load tasks, including technical ones |

For testing, both instruction-tuned and reasoning LLMs are used. The choice depends on the complexity and the reasoning demands of the test task.

### 1.1.4 Multimodal LLMs and vision-language models

- Multimodal LLMs extend the transformer to handle several modalities: text, images, sound and video. Tokenization is adapted for each data type. For example, images are converted into embeddings by vision-language models before the transformer processes them.
- **Vision-language models** are a subset that combines visual and textual information. They handle tasks such as image captioning, visual question answering and checking consistency between text and image.
- In testing, they can analyze screenshots and GUI wireframes together with text such as defect reports or user stories. This helps find discrepancies between expected results and what a screenshot shows, and helps generate richer test cases that include visual cues, which increases coverage.

### 1.2.1 Key LLM capabilities for test tasks

LLMs can interpret requirements, specifications, screenshots, code, test cases and defect reports. Key capabilities for testing:

| Capability | What the LLM can do |
|---|---|
| Requirements analysis and improvement | Find ambiguities, inconsistencies and missing information in the test basis, and generate questions to clarify requirements with stakeholders |
| Test case creation support | Generate test cases and suggest test objectives from requirements, user stories or other test basis elements |
| Test oracle generation | Generate expected results |
| Test data generation | Generate datasets, set boundary values and create combinations of test data |
| Test automation support | Generate test scripts from test case descriptions and improve existing scripts by suggesting changes and suitable test techniques |
| Test result analysis | Summarize results and classify anomalies by severity and priority |
| Testware creation | Create and keep updated documents such as test plans, test reports and defect reports |

### 1.2.2 AI chatbots and LLM-powered testing applications

| Aspect | AI chatbot | LLM-powered testing application |
|---|---|---|
| Interaction | Conversational interface; the tester types questions, commands or prompts and gets immediate answers | LLM capabilities integrated through APIs into tools and frameworks |
| Strengths | Fast feedback, clarifying test concepts, exploring requirements and test ideas, onboarding new testers; accessible even to non-technical stakeholders | Customization and scalability; automation of well-defined, repetitive or complex tasks such as test case generation, defect analysis or test data synthesis |
| Refinement | Prompt chaining lets the tester improve outputs iteratively | Can grow into AI agents built for specific testing roles (see Chapter 4) |

In both cases, good results depend on **strong prompt engineering** (see Chapter 2): clear, specific instructions make accurate and relevant output more likely.

## Keywords explained

Short definitions in plain language, based on the syllabus text. For the official wording, check the [ISTQB® Glossary](https://glossary.istqb.org/).

| Keyword | Meaning |
|---|---|
| AI chatbot | A conversational interface through which a tester talks to an LLM in natural language |
| Context window | How much preceding text, counted in tokens, the model can consider when it generates a response |
| Deep learning | Machine learning with neural networks that learn features automatically from large, complex data |
| Embedding | A numerical vector that represents a token's meaning and context; similar tokens sit close together |
| Feature | An input characteristic that classical machine learning needs selected before training (deep learning learns features itself) |
| Foundation LLM | A general-purpose model pre-trained on vast, diverse data that usually needs adaptation for specific tasks |
| Generative AI | AI that uses large pre-trained models to create new content such as text, images or code |
| Generative pre-trained transformer | The deep learning model type that LLMs are based on |
| Instruction-tuned LLM | A foundation model fine-tuned on prompt-and-response pairs to follow instructions better |
| Large language model (LLM) | A GenAI model pre-trained on very large text datasets so it can understand context and respond to prompts |
| Machine learning | A data-driven approach that learns from prepared data and trained models |
| Multimodal model | A model that processes several data types, such as text, images, audio and video |
| Reasoning LLM | An instruction-tuned model trained further for logical inference and multi-step problem solving |
| Symbolic AI | A rule-based approach that represents knowledge with symbols and logical rules |
| Tokenization | Breaking text into small units (tokens) so the model can process it |
| Transformer | The neural network architecture LLMs use to learn how tokens relate to each other |

## Key takeaways

- GenAI builds on deep learning and creates new content; pre-trained models can be used for test tasks directly, without an extra training phase.
- LLMs work on tokens and embeddings and predict the next token. Their output is plausible, not guaranteed correct, so results must be verified.
- Outputs can differ between runs because LLMs are non-deterministic.
- Token count matters: the context window limits how much input the model can consider, and longer input increases processing cost and time.
- Foundation, instruction-tuned and reasoning LLMs differ in how they were trained. Pick the type that fits the reasoning demands of the test task.
- Multimodal LLMs let testers combine text and images (screenshots, GUI wireframes) in one prompt.
- LLMs support the whole test process: requirements analysis, test case, oracle and test data generation, automation, result analysis and testware.
- Testers can use GenAI through chatbots (flexible and fast) or LLM-powered applications (automated and scalable). Both depend on good prompt engineering.
