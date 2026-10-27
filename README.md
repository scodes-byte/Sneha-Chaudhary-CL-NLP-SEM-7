# CL & NLP Assignment: LSTM Practice Questions

## 📌 About

This repository has my solutions to the LSTM practice questions for the Computational Linguistics & Natural Language Processing (CL & NLP) course, Semester 7.

The questions cover how an LSTM cell works internally, how many parameters an LSTM layer has, why LSTMs handle long sequences better than simple RNNs, and how LSTMs are used in two real-world problems: electricity load forecasting and predictive maintenance.

The complete step-by-step working is in **`CL&NLP Assignment_Sneha Chaudhary.pdf`**.

## 📚 Questions Covered

**Q1. Single-cell LSTM forward pass**
Calculating the forget gate, input gate, candidate cell state, new cell state, output gate and hidden state for one time step, using sigmoid and tanh.

**Q2. Parameter count**
Counting the trainable weights and biases in an LSTM layer with 10 inputs and 32 hidden units, using both the standard single-bias formula and PyTorch's two-bias convention.

**Q3. Vanishing gradient**
Seeing how quickly the gradient shrinks through the cell state for different forget-gate values (f^k), and why the LSTM's additive cell state helps compared with a vanilla RNN.

**Q4. Electricity load forecasting**
Preparing hourly data for an LSTM: number of records, sliding windows, tensor shapes, train split, mini-batches per epoch, and layer parameters.

**Q5. Predictive maintenance**
Min-max normalisation, applying a decision threshold, building a confusion matrix, and calculating precision, recall, F1-score and accuracy for an imbalanced dataset.

## ✅ Final Answers

| Question | Answer |
|---|---|
| Q1 | f_t = 0.6248, i_t = 0.5939, C~_t = 0.4542, C_t = 0.5196, o_t = 0.6106, h_t = 0.2915 |
| Q2 | (a) 5,504 parameters, (b) 5,632 parameters |
| Q3 | 0.9^10 = 0.3487, 0.9^50 = 0.0052, 0.5^50 ≈ 8.88 × 10^-16, 0.99^50 = 0.6050 |
| Q4 | 26,280 records, 26,089 windows, input (64, 168, 3), output (64, 24), 18,205 training windows, 285 mini-batches, 17,408 parameters |
| Q5 | Normalised value 0.75, prediction = Failure, TP 30, FP 15, FN 10, TN 945, Precision 0.6667, Recall 0.75, F1 0.7059, Accuracy 0.975 |

## 🧠 What I Learned

- How the gates in an LSTM decide what to forget, what to add and what to output at each step
- Why the cell state lets gradients flow over long sequences, and how the forget gate controls this
- How the number of parameters depends on input size, hidden size and the bias convention
- How time-series data is turned into input/output windows and batches for training
- Why accuracy can look high on imbalanced data even when a model misses most failures, and why recall matters more for maintenance problems

## 📂 Files

```
├── README.md
└── CL&NLP Assignment_Sneha Chaudhary.pdf
```

## 👩‍💻 Author

**Sneha Chaudhary**
B.Tech CSE (Data Science), UPES Dehradun
