
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Crédito para Investimento | Rodlider</title>

  <style>
    * { box-sizing: border-box; }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: linear-gradient(rgba(0,0,0,.75), rgba(0,0,0,.75)),
      url("https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?q=80&w=2070&auto=format&fit=crop")
      center/cover no-repeat fixed;
      margin: 0;
      padding: 20px;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
      background: #fff;
      width: 100%;
      max-width: 500px;
      padding: 30px;
      border-radius: 16px;
      box-shadow: 0 20px 40px rgba(0,0,0,.4);
    }

    h2 {
      text-align: center;
      margin-bottom: 25px;
    }

    label {
      display: block;
      margin-top: 14px;
      font-weight: bold;
      font-size: 14px;
    }

    input, select {
      width: 100%;
      padding: 14px;
      font-size: 16px;
      border-radius: 8px;
      border: 1px solid #ddd;
      background: #f8f9fa;
    }

    input:focus, select:focus {
      border-color: #25D366;
      outline: none;
    }

    button {
      width: 100%;
      margin-top: 25px;
      padding: 16px;
      background: #25D366;
      color: #fff;
      border: none;
      border-radius: 8px;
      font-size: 18px;
      font-weight: bold;
      cursor: pointer;
    }

    button:disabled {
      background: #ccc;
      cursor: not-allowed;
    }

    .lgpd {
      font-size: 11px;
      text-align: center;
      margin-top: 15px;
      color: #777;
    }
  </style>
</head>

<body>

<div class="container">
  <h2>Crédito para Investimento</h2>

  <form>
    <label>Nome Completo</label>
    <input type="text" id="nome" required>

    <label>Data de Nascimento</label>
    <input type="date" id="nascimento" required>

    <label>CPF</label>
    <input type="text" id="cpf" placeholder="000.000.000-00" maxlength="14" required>

    <label>WhatsApp</label>
    <input type="tel" id="telefone" placeholder="99 99999-9999" required>

    <label>Cidade</label>
    <input type="text" id="cidade" required>

    <label>Possui Entrada?</label>
    <select id="entrada">
      <option>Sim</option>
      <option>Não</option>
    </select>

    <label>Valor da Entrada</label>
    <select id="valorEntrada">
      <option>Não informado</option>
      <option>R$ 2.000</option>
      <option>R$ 3.000</option>
      <option>R$ 5.000</option>
      <option>R$ 8.000</option>
      <option>R$ 10.000</option>
      <option>R$ 20.000</option>
      <option>R$ 30.000</option>
      <option>R$ 40.000</option>
      <option>Acima de R$ 50.000</option>
    </select>

    <label>Renda Mensal</label>
    <select id="renda">
      <option>R$ 1.500</option>
      <option>R$ 2.000</option>
      <option>R$ 4.000</option>
      <option>R$ 5.000</option>
      <option>R$ 8.000</option>
      <option>R$ 10.000</option>
      <option>R$ 20.000</option>
      <option>R$ 30.000</option>
      <option>Mais de R$ 35.000</option>
    </select>

    <label>Previsão</label>
    <select id="previsao">
      <option>Em até 1 mês</option>
      <option>Em 2 meses</option>
      <option>Em 3 meses</option>
      <option>Em até 1 ano</option>
    </select>

    <label>Objetivo do Investimento</label>
    <select id="investimento">
      <option>Área Rural</option>
      <option>Veículo</option>
      <option>Imóvel Urbano</option>
      <option>Construção</option>
      <option>Reforma</option>
      <option>Loja / Ponto Comercial</option>
      <option>Capital de Giro</option>
    </select>

    <label>Valor do Crédito</label>
    <select id="valor">
      <option value="">Selecione</option>
      <option value="100000">R$ 100.000</option>
      <option value="150000">R$ 150.000</option>
      <option value="250000">R$ 250.000</option>
      <option value="350000">R$ 350.000</option>
      <option value="500000">R$ 500.000</option>
      <option value="750000">R$ 750.000</option>
      <option value="1000000">R$ 1.000.000</option>
    </select>

    <label>Parcela Estimada</label>
    <select id="parcela" disabled>
      <option>Selecione o crédito primeiro</option>
    </select>

    <button type="button" id="enviar" disabled>
      Solicitar Simulação
    </button>

    <div class="lgpd">🔒 Dados utilizados apenas para análise de crédito.</div>
  </form>
</div>

<script>
const parcelas = {
  100000: [750, 850, 900, 1000],
  150000: [850, 900, 1000, 1250],
  250000: [1000, 1250, 2300],
  350000: [1250, 2300, 3200],
  500000: [2300, 3200, 4500],
  750000: [3200, 4500, 5200],
  1000000: [5500, 6900]
};

const valor = document.getElementById("valor");
const parcela = document.getElementById("parcela");
const btn = document.getElementById("enviar");

valor.addEventListener("change", () => {
  parcela.innerHTML = '<option value="">Selecione a parcela</option>';
  btn.disabled = true;

  if (parcelas[valor.value]) {
    parcela.disabled = false;
    parcelas[valor.value].forEach(p => {
      const opt = document.createElement("option");
      opt.value = p;
      opt.textContent = `R$ ${p.toLocaleString("pt-BR")}`;
      parcela.appendChild(opt);
    });
  } else {
    parcela.disabled = true;
  }
});

parcela.addEventListener("change", () => {
  btn.disabled = !parcela.value;
});

// Máscara CPF
cpf.addEventListener("input", e => {
  let v = e.target.value.replace(/\D/g, "").slice(0, 11);
  v = v.replace(/(\d{3})(\d)/, "$1.$2");
  v = v.replace(/(\d{3})(\d)/, "$1.$2");
  v = v.replace(/(\d{3})(\d{1,2})$/, "$1-$2");
  e.target.value = v;
});

// Máscara telefone
telefone.addEventListener("input", e => {
  let x = e.target.value.replace(/\D/g, "").slice(0, 11);
  x = x.replace(/^(\d{2})(\d)/, "$1 $2");
  x = x.replace(/(\d{5})(\d)/, "$1-$2");
  e.target.value = x;
});

btn.addEventListener("click", () => {
  const msg =
`Olá! Me chamo *${nome.value}*.

Gostaria de solicitar uma simulação de crédito:
--------------------------------
Nome completo: ${nome.value}
Data de nascimento: ${nascimento.value}
CPF: ${cpf.value}
📍 Cidade: ${cidade.value}
📞 Contato: ${telefone.value}
🏡 Objetivo: ${investimento.value}
💰 Crédito: R$ ${Number(valor.value).toLocaleString("pt-BR")}
💳 Parcela Estimada: R$ ${parcela.value}
💵 Entrada: ${entrada.value} (${valorEntrada.value})
📊 Renda: ${renda.value}
⏳ Previsão: ${previsao.value}`;

  window.open(
    `https://api.whatsapp.com/send?phone=5598984134221&text=${encodeURIComponent(msg)}`,
    "_blank"
  );
});
</script>

</body>
</html>
