# Crypto-RNN

CryptoRNN is a deep learning project that uses a Recurrent Neural Network (RNN) with LSTM layers to predict cryptocurrency price movements. The model is trained on historical price and volume data for multiple cryptocurrencies and attempts to classify whether the price will go up (buy) or not (don't buy) in the near future.

## Features
- Loads and preprocesses historical crypto data (BTC, LTC, BCH, ETH)
- Normalizes and sequences data for RNN input
- Trains an LSTM-based neural network to classify future price movement
- Uses TensorBoard for training visualization
- Saves the best model checkpoints and final model in the Keras format

## Project Structure
```
CryptoRNN/
├── CryptoRNN.py         # Main training and evaluation script
├── requirements.txt     # Python dependencies
├── crypto_data/         # Folder containing historical crypto CSV files
├── models/              # Saved models and checkpoints
├── logs/                # TensorBoard logs
└── RNN/                 # (Optional) Virtual environment or additional code
```

## Setup
1. **Clone the repository**
2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
3. **Prepare data**
   - Place your historical crypto CSV files (BTC-USD.csv, LTC-USD.csv, BCH-USD.csv, ETH-USD.csv) in the `crypto_data/` folder.
   - Each CSV should have columns: `time, low, high, open, close, volume` (no header row).

## Usage
Run the main script to train and evaluate the model:
```bash
python CryptoRNN.py
```
- Training and validation progress will be logged to the `logs/` directory for TensorBoard visualization.
- The best model checkpoints will be saved in the `models/` directory with the `.keras` extension.

## Requirements
- Python 3.8+
- TensorFlow 2.x / Keras
- pandas
- numpy
- scikit-learn

Install all dependencies with:
```bash
pip install -r requirements.txt
```

## Notes
- The model uses a sequence length of 60 and predicts 3 steps into the future by default. You can adjust these parameters in `CryptoRNN.py`.
- The script balances the dataset between 'buy' and 'don't buy' classes for robust training.
- For best results, ensure your data is clean and covers a significant time range.

## License
This project is for educational and research purposes. 
