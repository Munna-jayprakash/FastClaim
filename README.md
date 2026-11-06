# ClaimFast – AI-Powered Insurance Claim Classification

## Project Overview

**ClaimFast** is an AI-powered insurance claim classification system that uses Large Language Models (LLMs) to extract structured information from unstructured insurance claim descriptions.

The project uses **Ollama** with the **Llama 3.2 (3B)** model to classify insurance claims and extract important details using different prompting techniques.

The main objective is to compare the performance of **Zero-Shot Prompting** and **Few-Shot Prompting** approaches in terms of accuracy, F1-score, JSON validity, and response latency.

---

##Project Objectives

- Automatically classify insurance claims using an LLM.
- Extract important information from unstructured claim descriptions.
- Compare Zero-Shot and Few-Shot prompting techniques.
- Evaluate model performance using accuracy and macro F1-score.
- Measure response latency and JSON output validity.
- Identify the most effective prompting strategy for insurance claim classification.

---

##Technologies Used

- **Python** – Main programming language
- **Ollama** – Local LLM execution environment
- **Llama 3.2 (3B)** – Large Language Model
- **Requests** – API communication with Ollama
- **Matplotlib** – Data visualization
- **JSON / JSONL** – Dataset and structured output format
- **Git & GitHub** – Version control and project hosting

---

##Prompting Approaches

This project evaluates four different prompting configurations.

### 1. Zero-Shot Prompting

The model receives instructions and a claim description without any examples.

### 2. Few-Shot Prompting – 3 Examples

The model receives three example insurance claims before processing the actual claim.

### 3. Few-Shot Prompting – 5 Examples

The model receives five examples to improve its understanding of the expected output format and classification patterns.

### 4. Few-Shot Prompting – 8 Examples

The model receives eight examples to provide more contextual guidance and improve classification performance.

---

## 📊 Experimental Results

Each experiment was evaluated using 20 test records.

### Overall Performance Comparison

| Experiment | Accuracy | Macro F1-Score |
|---|---:|---:|
| Zero-Shot | 75% | 0.7783 |
| Few-Shot (3 Examples) | 85% | 0.8434 |
| Few-Shot (5 Examples) | 80% | 0.8278 |
| Few-Shot (8 Examples) | **90%** | **0.9101** |

### Additional Performance Metrics

| Experiment | JSON Validity | Average Latency (Seconds) |
|---|---:|---:|
| Zero-Shot | 100% | 1.3288 |
| Few-Shot (3 Examples) | 100% | 1.5361 |
| Few-Shot (5 Examples) | 100% | **1.2067** |
| Few-Shot (8 Examples) | 100% | 1.7231 |

---

##Key Findings

- **Few-Shot (8 Examples)** achieved the highest accuracy of **90%** and the highest macro F1-score of approximately **0.9101**.
- **Few-Shot (5 Examples)** achieved the lowest average response latency of approximately **1.2067 seconds**.
- All four experiments achieved **100% JSON validity**.
- Few-Shot prompting generally improved classification performance compared with Zero-Shot prompting.
- Increasing the number of examples does not always guarantee better performance or lower latency.

### Best Performing Configuration

Based on the experimental results, **Few-Shot Prompting with 8 Examples** was the best-performing configuration in terms of classification accuracy and macro F1-score.

---

##Project Structure

```text
ClaimFast/
│
├── code/
│   ├── compare_experiments.py
│   ├── evaluate_zero_shot.py
│   ├── few_shot_3.py
│   ├── few_shot_5.py
│   ├── few_shot_8.py
│   ├── generate_dataset.py
│   ├── generate_report.py
│   ├── validate_dataset.py
│   ├── visualize_results.py
│   └── zero_shot.py
│
├── data/
│   ├── dev.jsonl
│   ├── test.jsonl
│   └── labelling_guide.md
│
├── demo/
│
├── outputs/
│
├── prompts/
│
├── report/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

##Installation and Setup

### 1. Clone the Repository

```bash
git clone "https://github.com/Munna-jayprakash/FastClaim.git"

### 2. Navigate to the Project Directory

```bash
cd ClaimFast
```

### 3. Install Python Dependencies

```bash
pip install -r requirements.txt
```

### 4. Install and Run Ollama

Download and install Ollama from:

https://ollama.com/

### 5. Download the Llama 3.2 Model

```bash
ollama pull llama3.2:3b
```

Make sure the Ollama service is running before executing the Python scripts.

---

##Running the Project

Navigate to the `code` directory:

```bash
cd code
```

Run the experiments using the following commands:

### Zero-Shot Experiment

```bash
python zero_shot.py
```

### Few-Shot Experiment – 3 Examples

```bash
python few_shot_3.py
```

### Few-Shot Experiment – 5 Examples

```bash
python few_shot_5.py
```

### Few-Shot Experiment – 8 Examples

```bash
python few_shot_8.py
```

### Compare Experiments

```bash
python compare_experiments.py
```

### Visualize Results

```bash
python visualize_results.py
```

### Generate Report

```bash
python generate_report.py
```

*Note: Run each script from the directory and environment expected by the project. Adjust file paths or commands if your local implementation uses a different execution path.*

---

##Evaluation Metrics

The project uses the following evaluation metrics:

| Metric | Description |
|---|---|
| Accuracy | Measures the percentage of correctly classified records. |
| Macro F1-Score | Measures the average F1-score across classes, giving equal weight to each class. |
| JSON Validity | Measures whether the model produces valid JSON output. |
| Average Latency | Measures the average time taken by the model to generate a response. |
| Field Accuracy | Measures the correctness of individual extracted fields. |

---

##Limitations

- The experiments use a relatively small test dataset of 20 records.
- Model performance may vary depending on the claim description and prompting strategy.
- Response latency depends on the local hardware and Ollama environment.
- The system is intended as an experimental classification tool and not as a replacement for professional insurance claim assessment.
- Predictions should be reviewed by a qualified human before being used in real insurance workflows.

---

##Future Improvements

- Increase the size and diversity of the insurance claim dataset.
- Evaluate additional LLM models.
- Explore advanced prompting and prompt optimization techniques.
- Improve extraction accuracy for individual claim fields.
- Develop a web-based user interface for easier interaction.
- Add confidence scoring and human review workflows.
- Evaluate the system on larger and more diverse real-world datasets.

---

##Conclusion

ClaimFast demonstrates how Large Language Models can be used to automate insurance claim classification and structured information extraction.

The experiments show that prompting strategy has a significant impact on model performance. Among the tested configurations, **Few-Shot Prompting with 8 Examples** achieved the best classification accuracy and macro F1-score.

The project provides a foundation for further exploration of LLM-based automation in insurance claim processing.

Author
MUNNA JAY PRAKASH THAKUR
GitHub Repository: "https://github.com/Munna-jayprakash/FastClaim.git"
 # FastClaim
