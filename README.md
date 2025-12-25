# Chess Move Prediction using LSTM and Transformer Models

## Project Overview
This project focuses on **predicting the next chess move** given a sequence of previous moves using deep learning models. Two sequence-based neural architectures are implemented and compared:

- **Baseline LSTM**
- **Transformer (PyTorch implementation)**

The models are trained on chess games parsed from PGN files, where each move is represented using **Standard Algebraic Notation (SAN)**.

---

## Files Description

### `tokenization.ipynb`
- Parses chess games from PGN format
- Extracts move sequences in SAN notation
- Builds a vocabulary of unique chess moves
- Converts moves to integer token sequences
- Pads sequences to a fixed length
- Splits the dataset into training (80%) and testing (20%) sets
- Saves tensors for model training

---

### `ML_Sem3_Project_Models.ipynb`
- Loads preprocessed datasets
- Implements:
  - Baseline LSTM model
  - Transformer using `torch.nn.Transformer`
- Trains both models on identical data
- Evaluates models using:
  - Training loss
  - Test loss
  - Top-1 accuracy
  - Top-5 accuracy
  - Inference time
- Decodes predicted tokens back to SAN moves
- Performs qualitative analysis by checking predicted move legality

---

### `report.pdf`
Final project report containing:
- Introduction and problem statement
- Motivation and goals
- Literature survey
- Methodology
- Dataset description
- Evaluation metrics
- Results and analysis
- Error analysis
- Limitations and future work
- Conclusion

---

### `proposal.pdf`
Initial project proposal outlining:
- Problem definition
- Motivation
- Planned methodology
- Expected outcomes

---

### `requirements.txt`
Lists Python dependencies required to run the project.
