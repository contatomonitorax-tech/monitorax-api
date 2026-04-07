const express = require('express');
const app = express();

const PORT = process.env.PORT || 3000;

app.get('/', (req, res) => {
  res.send("Monitorax API Online 🚀");
});

app.get('/api', (req, res) => {
  const status = req.query.status;
  const bateria = req.query.bateria;

  console.log("Recebido:");
  console.log("Status:", status);
  console.log("Bateria:", bateria);

  res.send("OK");
});

app.listen(PORT, () => {
  console.log(`Servidor rodando na porta ${PORT}`);
});
