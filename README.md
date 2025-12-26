# Chess Move Prediction using LSTM and Transformer Models

## Project Overview
This project focuses on **predicting the next chess move** given a sequence of previous moves using deep learning models. Two sequence-based neural architectures are implemented and compared:

- **Baseline LSTM**
- **Transformer (PyTorch implementation)**

The models are trained on chess games parsed from PGN files, where each move is represented using **Standard Algebraic Notation (SAN)**.

---

## File Structure
```text
Final_Submission/
├── Code/
│   ├── tokenization.ipynb
│   └── ML_Sem3_Project_Models.ipynb
├── ML_Project_Proposal_Sem3.pdf
├── ML_Sem3_Project_Report.pdf
└── requirements.txt

data/
└── processed/
    └── chess_games.csv
```

## Files Description

### `chess_games.csv`
- CSV file that contains data from Lichess games containing player information (names, elo ratings, moves played in the game)

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

### `ML_Sem3_Project_Report.pdf`
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

### `ML_Survey_Paper_Sem3.pdf`
Survey paper based on research papers related to the project topic.

---

### `ML_Project_Proposal_Sem3.pdf`
Initial project proposal outlining:
- Problem definition
- Motivation
- Planned methodology
- Expected outcomes

---

### `requirements.txt`
Lists Python dependencies required to run the project.

---

## How to run the code (preferably on Google Colab using T4 GPU for Runtime)

1. Run the *tokenization.ipynb* file which will generate the *preprocessed_data.pt* (containing vocabulary, inverse vocabulary, X and y tensors)
2. This *preprocessed_data.pt* will have to be uploaded to Colab as it will be used in *ML_Sem3_Project_Models.ipynb* file
3. *ML_Sem3_Project_Models.ipynb* file contains the code for training both the models and evaluating them
4. Run all cells in order without skipping anything
