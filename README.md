<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <title>Crédito para Investimento | Rodlider</title>
  <meta name="description" content="Solicite crédito para investimento de forma rápida e segura." />

  <style>
    /* Reset e Fontes */
    * { box-sizing: border-box; outline: none; }
    
    body {
      font-family: 'Segoe UI', 'Roboto', Helvetica, Arial, sans-serif;
      /* Imagem de fundo profissional e overlay escuro para contraste */
      background: linear-gradient(rgba(0,0,0,0.75), rgba(0,0,0,0.75)),
        url('https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?q=80&w=2070&auto=format&fit=crop') center/cover no-repeat fixed;
      margin: 0;
      padding: 20px;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #333;
    }

    .container {
      background: #ffffff;
      width: 100%;
      max-width: 500px;
      padding: 35px;
      border-radius: 16px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.4);
      animation: fadeIn 0.5s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h2 { 
      margin-top: 0; 
      color: #1a1a1a;
      text-align: center;
      margin-bottom: 25px;
      font-size: 26px;
      font-weight: 700;
    }

    label { 
      display: block; 
      margin-top: 16px; 
      font-weight: 600; 
      color: #444;
      font-size: 14px;
      margin-bottom: 6px;
    }

    input, select {
      width: 100%;
      padding: 14px;
      font-size: 16px; /* Tamanho 16px evita zoom automático no iPhone */
      border-radius: 8px;
      border: 1px solid #ddd;
      background-color: #f8f9fa;
      transition: all 0.3s ease;
      -webkit-appearance: none; /* Remove estilo padrão iOS */
    }

    /* Setas customizadas para selects no CSS moderno */
    select {
      background-image: url("data:image/svg+xml;charset=US-ASCII,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20width%3D%22292.4%22%20height%3D%22292.4%22%3E%3Cpath%20fill%3D%22%23333%22%20d%3D%22M287%2069.4a17.6%2017.6%200%200%200-13-5.4H18.4c-5%200-9.3%201.8-12.9%205.4A17.6%2017.6%200%200%200%200%2082.2c0%205%201.8%209.3%205.4%2012.9l128%20127.9c3.6%203.6%207.8%205.4%2012.8%205.4s9.2-1.8%2012.8-5.4L287%2095c3.5-3.5%205.4-7.8%205.4-12.8%200-5-1.9-9.2-5.5-12.8z%22%2F%3E%3C%2Fsvg%3E");
      background-repeat: no-repeat;
      background-position: right 1rem center;
      background-size: .65em auto;
    }

    input:focus, select:focus {
      border-color: #25D366;
      box-shadow: 0 0 0 3px rgba(37, 211, 102, 0.2);
      background-color: #fff;
    }

    button {
      width: 100%;
      margin-top: 30px;
      padding: 16px;
      background: #25D366;
      color: #fff;
      border: none;
      border-radius: 8px;
      font-size: 18px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s, transform 0.1s;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      box-shadow: 0 4px 6px rgba(37, 211, 102, 0.3);
    }

    button:hover:not(:disabled) {
      background: #20bd5a;
      transform: translateY(-2px);
    }

    button:active:not(:disabled) {
      transform: translateY(0);
    }

    button:disabled { 
      background: #ccc; 
      cursor: not-allowed; 
      opacity: 0.7;
      box-shadow: none;
    }

    .lgpd { 
      font-size: 11px; 
      color: #888; 
      margin-top: 20px; 
      text-align: center; 
      line-height: 1.4;
      padding-top: 10px;
      border-top: 1px solid #eee;
    }

    /* Ícone simples do WhatsApp via CSS */
    .icon-wa::before {
      content: "💬"; 
      margin-right: 8px;
    }

    @media (max-width: 480px) {
      body { padding: 10px; align-items: flex-start; }
      .container { padding: 25px 20px; border-radius: 12px; margin-top: 10px; }
      h2 { font-size: 22px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Crédito para Investimento</h2>

    <form id="creditoForm">
      <label for="nome">Nome Completo</label>
      <input type="text" id="nome" placeholder="Digite seu nome" required />

      <label for="telefone">WhatsApp</label>
      <!-- Placeholder atualizado para o formato solicitado -->
      <input type="tel" id="telefone" placeholder="99 99999-9999" maxlength="13" required />

      <label for="cidade">Cidade</label>
      <input type="text" id="cidade" placeholder="Sua cidade" required />

      <label for="entrada">Possui Entrada?</label>
      <select id="entrada">
        <option value="Sim">Sim</option>
        <option value="Não">Não</option>
      </select>

      <label for="valorEntrada">Valor Disponível para Entrada</label>
      <select id="valorEntrada">
        <option value="Não informado">Selecione</option>
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

      <label for="renda">Renda Mensal Aproximada</label>
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

      <label for="previsao">Previsão para Realizar</label>
      <select id="previsao">
        <option>Em até 1 mês</option>
        <option>Em 2 meses</option>
        <option>Em 3 meses</option>
        <option>Em até 1 ano</option>
      </select>

      <label for="investimento">Objetivo do Investimento</label>
      <select id="investimento">
        <option>Área Rural</option>
        <option>Veículo (Carro/Caminhão)</option>
        <option>Imóvel Urbano</option>
        <option>Construção</option>
        <option>Reforma</option>
        <option>Loja / Ponto Comercial</option>
        <option>Capital de Giro</option>
      </select>

      <label for="valor">Valor do Crédito Desejado</label>
      <select id="valor">
        <option value="">Selecione o valor</option>
        <option value="100000">R$ 100.000</option>
        <option value="150000">R$ 150.000</option>
        <option value="250000">R$ 250.000</option>
        <option value="350000">R$ 350.000</option>
        <option value="500000">R$ 500.000</option>
        <option value="750000">R$ 750.000</option>
        <option value="1000000">R$ 1.000.000</option>
      </select>

      <label for="parcela">Sugestão de Parcela</label>
      <select id="parcela" disabled>
        <option value="">Selecione o valor do crédito primeiro</option>
      </select>

      <button type="button" id="btnEnviar" disabled>
        <span class="icon-wa"></span> Solicitar Simulação
      </button>

      <div class="lgpd">🔒 Seus dados estão seguros e serão utilizados apenas para contato comercial referente a esta simulação.</div>
    </form>
  </div>

  <script>
    // Configuração das parcelas
    const parcelas = {
      100000: [750, 850, 900, 1000],
      150000: [850, 900, 1000, 1250],
      250000: [1000, 1250, 2300],
      350000: [1250, 2300, 3200],
      500000: [2300, 3200, 4500],
      750000: [3200, 4500, 5200],
      1000000: [5500, 6900]
    };

    // Seleção segura de elementos do DOM
    const nomeInput = document.getElementById('nome');
    const telefoneInput = document.getElementById('telefone');
    const cidadeInput = document.getElementById('cidade');
    const entradaSelect = document.getElementById('entrada');
    const valorEntradaSelect = document.getElementById('valorEntrada');
    const rendaSelect = document.getElementById('renda');
    const previsaoSelect = document.getElementById('previsao');
    const investimentoSelect = document.getElementById('investimento');
    const valorSelect = document.getElementById('valor');
    const parcelaSelect = document.getElementById('parcela');
    const btn = document.getElementById('btnEnviar');

    // Lógica para atualizar as parcelas quando o valor muda
    valorSelect.addEventListener('change', () => {
      parcelaSelect.innerHTML = '<option value="">Selecione a parcela</option>';
      
      if (parcelas[valorSelect.value]) {
        parcelaSelect.disabled = false;
        parcelas[valorSelect.value].forEach(p => {
          const opt = document.createElement('option');
          opt.value = p;
          opt.textContent = `R$ ${p.toLocaleString('pt-BR')}`;
          parcelaSelect.appendChild(opt);
        });
        // Foca no campo de parcela para melhor UX
        parcelaSelect.focus();
      } else {
        parcelaSelect.disabled = true;
        parcelaSelect.innerHTML = '<option value="">Selecione o crédito primeiro</option>';
        btn.disabled = true;
      }
    });

    // Habilita o botão apenas quando a parcela é escolhida
    parcelaSelect.addEventListener('change', () => {
      btn.disabled = !parcelaSelect.value;
    });

    // --- NOVA MÁSCARA DE TELEFONE (Formato: 98 98526-3537) ---
    telefoneInput.addEventListener('input', (e) => {
      // Remove tudo que não é dígito
      let x = e.target.value.replace(/\D/g, '');
      
      // Limita a 11 números
      if (x.length > 11) x = x.slice(0, 11);

      // Aplica a máscara:
      // (\d{0,2}) -> Pega os 2 primeiros (DDD)
      // (\d{0,5}) -> Pega os próximos 5
      // (\d{0,4}) -> Pega os últimos 4
      const match = x.match(/^(\d{0,2})(\d{0,5})(\d{0,4})$/);
      
      if (match) {
        // Constrói a string: "DDD" + espaço + "XXXXX" + hífen + "XXXX"
        e.target.value = !match[2] ? match[1] 
                         : match[1] + ' ' + match[2] + (match[3] ? '-' + match[3] : '');
      }
    });

    // Enviar para WhatsApp
    btn.addEventListener('click', () => {
      // Validação Básica
      if (nomeInput.value.length < 3) {
        alert("Por favor, digite seu nome completo.");
        nomeInput.focus();
        return;
      }
      if (telefoneInput.value.length < 12) { // Ajustado para o tamanho mínimo da nova máscara
        alert("Por favor, digite um WhatsApp válido com DDD.");
        telefoneInput.focus();
        return;
      }
      if (cidadeInput.value.length < 2) {
        alert("Por favor, informe sua cidade.");
        cidadeInput.focus();
        return;
      }

      // Montagem da mensagem
      const msg = 
        `Olá! Me chamo *${nomeInput.value}*.%0A%0A` +
        `Gostaria de solicitar uma simulação de crédito:%0A` +
        `--------------------------------%0A` +
        `📍 *Cidade:* ${cidadeInput.value}%0A` +
        `📞 *Contato:* ${telefoneInput.value}%0A` +
        `🏡 *Objetivo:* ${investimentoSelect.value}%0A` +
        `💰 *Crédito:* R$ ${Number(valorSelect.value).toLocaleString('pt-BR')}%0A` +
        `💳 *Parcela Estimada:* R$ ${Number(parcelaSelect.value).toLocaleString('pt-BR')}%0A` +
        `💵 *Entrada:* ${entradaSelect.value} (${valorEntradaSelect.value})%0A` +
        `📊 *Renda:* ${rendaSelect.value}%0A` +
        `⏳ *Previsão:* ${previsaoSelect.value}`;

      // Abre WhatsApp
      window.open(`https://api.whatsapp.com/send?phone=5598984134221&text=${msg}`, '_blank');
    });
  </script>
</body>
</html>


