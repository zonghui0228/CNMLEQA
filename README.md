# CNMLEQA

**CNMLEQA** is a benchmark dataset developed to evaluate the performance of large language models (LLMs) on Chinese National Medical Licensing Examinations. The dataset is designed to support structured, fine-grained analysis of LLM capabilities in factual medical knowledge, clinical reasoning, and exam-level competency.

## 🔍 Overview

- **Total questions answer pairs**: 9,890
- **Subsets**:
  - `CNMLEQA-10k`: Full dataset with 9,890 questions
  - `CNMLEQA-3k`: Curated subset with 2,949 questions
- **Question Type**:
  - Knowledge-based questions
  - Case-based clinical questions
- **Format**: Multiple-choice (5 options: A–E, single correct answer)
- **Language**: Chinese

## 📦 Dataset Structure

Each entry in the dataset includes the following fields:

```json
{
  "id": "unique-id",
  "question": "Question text in Chinese",
  "opa": "Option A",
  "opb": "Option B",
  "opc": "Option C",
  "opd": "Option D",
  "ope": "Option E",
  "answer": "Correct option (e.g., 'opc')",
  "question_type": "Knowledge-based / Case-based",
  "year": "Exam year (if available)",
  "source": "Original data source (if available)"
}
```

Example:

```json
{
  "id":"3e8a9708-7df9-5066-ab4c-ea5c813227cc",
  "question":"女，34岁，右尺骨骨折2小时，予手法复位，管型石膏固定5小时后，患者感觉右手指麻木，肿胀，活动不灵，查体：生命体征平稳，心肺腹未见异常，目前最恰当的处理方法是",
  "opa":"脱水",
  "opb":"立即手术",
  "opc":"止痛",
  "opd":"立即松解外固定",
  "ope":"扩血管药物治疗",
  "answer":"opd",
  "year":2017,
  "question_type":"案例分析",
  "source":"pubmed-38355517;github-llm-chinese-nmle"
}
```


```json
{
  "id":"da2084d0-8702-5af8-bf7c-7f7b76e3b208",
  "question":"下列哪项疾病属于遗传性心肌病",
  "opa":"扩张型心肌病",
  "opb":"肥厚型心肌病",
  "opc":"限制型心肌病",
  "opd":"甲亢性心肌病",
  "ope":"病毒性心肌病",
  "answer":"opb",
  "year":2021,
  "question_type":"知识问答",
  "source":"pubmed-38355517;github-llm-chinese-nmle"
}
```