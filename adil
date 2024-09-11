const express = require('express');
const bodyParser = require('body-parser');
const cors = require('cors');

const app = express();
const PORT = 5000;

app.use(bodyParser.json());
app.use(cors());

// Sample transaction data
let transactions = [];

// GET all transactions
app.get('/api/transactions', (req, res) => {
  res.json(transactions);
});

// POST a new transaction
app.post('/api/transactions', (req, res) => {
  const transaction = req.body;
  transactions.push(transaction);
  res.status(201).json(transaction);
});

app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});
