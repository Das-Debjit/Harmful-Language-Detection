# Harmful Language & Criminal Intent Detector

An NLP-powered web application that classifies text into harmful intent categories using a fine-tuned DistilBERT model.

## Intent Categories
| Label | Category | Description |
|-------|----------|-------------|
| 0 | Neutral | Normal, non-harmful content |
| 1 | Confession | Admission of crimes |
| 2 | Discussing Illegal Activity | Past crime discussion |
| 3 | Planning Crime | Active plotting of crimes |
| 4 | Threatening Action | Explicit threats or coercion |

## Tech Stack
- **Model**: DistilBERT (distilbert-base-uncased), fine-tuned
- **Framework**: HuggingFace Transformers + PyTorch
- **Interface**: Gradio web UI
- **Training Data**: Jigsaw Toxic Comments + Custom synthetic crime dialogues (6K samples)

## Installation

git clone https://github.com/yourusername/harmful-language-detection.git
cd harmful-language-detection
pip install -r requirements.txt

## Run the App

python app.py

Then open: http://127.0.0.1:7860

## System Requirements
- Python 3.8+
- GPU optional (auto-detects, falls back to CPU)

## Project Structure
- app.py — Main Gradio application
- intent_label_mapping_combined.json — Label mappings
- model/ — Fine-tuned DistilBERT weights and tokenizer
- requirements.txt — Python dependencies