<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Teste: Qualidade do Sono</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #1a2e4a;
    --gold: #b8922a;
    --white: #ffffff;
    --cream: #faf8f5;
    --gold-light: #d4a843;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Cormorant Garamond', Georgia, serif;
    background: var(--white);
    color: var(--navy);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding: 20px;
  }

  .card {
    width: 480px;
    background: var(--white);
    border: 2.5px solid var(--navy);
    overflow: hidden;
  }

  .header {
    background: var(--navy);
    padding: 28px 32px 24px;
    text-align: center;
  }

  .header-tag {
    font-size: 11px;
    letter-spacing: 3px;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .header h1 {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 26px;
    color: var(--white);
    line-height: 1.25;
    margin-bottom: 6px;
  }

  .header-sub {
    font-size: 13px;
    color: rgba(255,255,255,0.65);
  }

  .gold-line {
    width: 48px;
    height: 2px;
    background: var(--gold);
    margin: 14px auto 0;
  }

  .intro {
    padding: 28px 32px 20px;
    border-bottom: 1.5px solid rgba(26,46,74,0.1);
    text-align: center;
  }

  .intro-icon { font-size: 28px; display: block; margin-bottom: 10px; }

  .intro p { font-size: 15px; line-height: 1.65; opacity: 0.85; }

  .intro-note {
    font-size: 12px;
    color: var(--gold);
    margin-top: 10px;
    letter-spacing: 0.5px;
    font-style: italic;
  }

  .questions-area { padding: 24px 32px 20px; }

  .progress-bar-wrap {
    height: 3px;
    background: rgba(26,46,74,0.1);
    border-radius: 2px;
    margin-bottom: 22px;
    overflow: hidden;
  }

  .progress-bar-fill {
    height: 100%;
    background: var(--gold);
    border-radius: 2px;
    transition: width 0.5s ease;
    width: 0%;
  }

  .q-counter {
    font-size: 11px;
    letter-spacing: 2px;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 6px;
  }

  .q-section {
    font-size: 11px;
    letter-spacing: 1px;
    color: rgba(26,46,74,0.45);
    text-transform: uppercase;
    margin-bottom: 10px;
    font-style: italic;
  }

  .question-text {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 17.5px;
    color: var(--navy);
    line-height: 1.5;
    margin-bottom: 20px;
    min-height: 50px;
  }

  /* Input para texto livre */
  .text-input-wrap { margin-bottom: 20px; }

  .text-input {
    width: 100%;
    border: 1.5px solid rgba(26,46,74,0.2);
    background: var(--cream);
    padding: 12px 16px;
    font-family: 'Cormorant Garamond', serif;
    font-size: 16px;
    color: var(--navy);
    outline: none;
    transition: border-color 0.2s;
  }

  .text-input:focus { border-color: var(--gold); }

  .text-input-label {
    font-size: 12px;
    color: rgba(26,46,74,0.5);
    margin-bottom: 6px;
    display: block;
    letter-spacing: 0.5px;
  }

  .options {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .option-btn {
    background: var(--cream);
    border: 1.5px solid rgba(26,46,74,0.18);
    padding: 13px 18px;
    text-align: left;
    font-family: 'Cormorant Garamond', serif;
    font-size: 15px;
    color: var(--navy);
    cursor: pointer;
    transition: all 0.22s ease;
    line-height: 1.4;
  }

  .option-btn:hover { border-color: var(--gold); background: white; }
  .option-btn.selected { border-color: var(--gold); background: var(--navy); color: var(--white); }

  .option-letter {
    font-size: 11px;
    letter-spacing: 1.5px;
    color: var(--gold);
    margin-right: 8px;
  }

  .option-btn.selected .option-letter { color: var(--gold-light); }

  .nav-area {
    padding: 16px 32px 28px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .btn-nav {
    font-family: 'Cormorant Garamond', serif;
    font-size: 13px;
    letter-spacing: 2px;
    text-transform: uppercase;
    border: 1.5px solid var(--navy);
    background: transparent;
    color: var(--navy);
    padding: 10px 22px;
    cursor: pointer;
    transition: all 0.2s;
  }

  .btn-nav:hover { background: var(--navy); color: var(--white); }
  .btn-nav.primary { background: var(--gold); border-color: var(--gold); color: var(--white); }
  .btn-nav.primary:hover { background: #9a7820; border-color: #9a7820; }
  .btn-nav:disabled { opacity: 0.3; cursor: default; }

  .skip-note {
    font-size: 12px;
    color: rgba(26,46,74,0.4);
    text-align: center;
    padding: 0 32px 16px;
    font-style: italic;
  }

  /* RESULT */
  .result-area {
    padding: 32px;
    display: none;
    animation: fadeUp 0.5s ease;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .result-label {
    font-size: 11px;
    letter-spacing: 3px;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 6px;
  }

  .result-title {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 21px;
    color: var(--navy);
    line-height: 1.3;
    margin-bottom: 16px;
  }

  .result-bar-wrap {
    background: rgba(26,46,74,0.08);
    height: 8px;
    border-radius: 4px;
    overflow: hidden;
    margin-bottom: 20px;
  }

  .result-bar-fill {
    height: 100%;
    border-radius: 4px;
    transition: width 1.2s ease;
  }

  .result-text {
    font-size: 15px;
    line-height: 1.7;
    opacity: 0.85;
    margin-bottom: 22px;
  }

  .result-cta {
    background: var(--navy);
    padding: 18px 20px;
    border-left: 4px solid var(--gold);
    margin-bottom: 20px;
  }

  .result-cta p {
    font-size: 14px;
    color: var(--white);
    line-height: 1.6;
    opacity: 0.9;
  }

  .result-cta strong { color: var(--gold-light); }

  .disclaimer {
    font-size: 11px;
    color: rgba(26,46,74,0.4);
    line-height: 1.6;
    text-align: center;
    margin-bottom: 18px;
    font-style: italic;
    padding: 0 8px;
  }

  .divider-gold {
    display: flex;
    align-items: center;
    gap: 12px;
    margin: 20px 0;
  }

  .divider-gold span { display: block; flex: 1; height: 1px; background: var(--gold); opacity: 0.4; }
  .divider-gold i { color: var(--gold); font-size: 10px; }

  .restart-btn {
    font-family: 'Cormorant Garamond', serif;
    font-size: 12px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: rgba(26,46,74,0.5);
    background: none;
    border: none;
    cursor: pointer;
    display: block;
    margin: 0 auto;
  }

  .restart-btn:hover { color: var(--gold); }

  .footer {
    background: var(--navy);
    padding: 14px 32px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-handle { font-size: 13px; color: var(--gold); letter-spacing: 1px; }
  .footer-name { font-size: 11px; color: rgba(255,255,255,0.4); letter-spacing: 1px; text-transform: uppercase; }

  .screen { transition: opacity 0.3s; }
  .screen.hidden { display: none; }
</style>
</head>
<body>

<div class="card">

  <div class="header">
    <div class="header-tag">Avaliação Clínica · Saúde Mental</div>
    <h1>Seu sono está<br>te recuperando?</h1>
    <div class="header-sub">Índice de Qualidade do Sono de Pittsburgh</div>
    <div class="gold-line"></div>
  </div>

  <!-- INTRO -->
  <div id="screen-intro" class="screen">
    <div class="intro">
      <span class="intro-icon">🌙</span>
      <p>Instrumento clínico validado internacionalmente para avaliação da qualidade do sono. Responda pensando nos seus hábitos do <strong>último mês</strong>.</p>
      <p class="intro-note">⏱ Duração aproximada: 5 minutos</p>
    </div>
    <div class="nav-area" style="justify-content:center; padding-top:24px;">
      <button class="btn-nav primary" onclick="startQuiz()">Começar avaliação</button>
    </div>
  </div>

  <!-- QUIZ -->
  <div id="screen-quiz" class="screen hidden">
    <div class="questions-area">
      <div class="progress-bar-wrap">
        <div class="progress-bar-fill" id="progress-bar"></div>
      </div>
      <div class="q-counter" id="q-counter"></div>
      <div class="q-section" id="q-section"></div>
      <div class="question-text" id="question-text"></div>
      <div id="input-area"></div>
    </div>
    <div class="skip-note" id="skip-note" style="display:none;">Esta pergunta é opcional</div>
    <div class="nav-area">
      <button class="btn-nav" id="btn-prev" onclick="prevQ()" disabled>← Voltar</button>
      <button class="btn-nav primary" id="btn-next" onclick="nextQ()" disabled>Próxima →</button>
    </div>
  </div>

  <!-- RESULT -->
  <div id="screen-result" class="screen hidden">
    <div class="result-area" id="result-area"></div>
  </div>

  <div class="footer">
    <span class="footer-handle">@psi_liviamelo</span>
    <span class="footer-name">Psicologia · Saúde Mental</span>
  </div>

</div>

<script>
// Tipos: 'time' = campo de texto, 'number' = campo número, 'choice' = opções, 'optional' = opção + pode pular
const freqOpts = [
  { label: "Nenhuma vez no último mês", score: 0 },
  { label: "Menos de 1 vez por semana", score: 1 },
  { label: "1 a 2 vezes por semana", score: 2 },
  { label: "3 ou mais vezes por semana", score: 3 }
];

const questions = [
  // BLOCO 1 — Perguntas abertas (sem pontuação, apenas registro)
  {
    num: "1", section: "Horários de sono",
    text: "Qual é o seu horário usual de deitar à noite?",
    type: "time", placeholder: "Ex: 23:00", scored: false
  },
  {
    num: "2", section: "Latência do sono",
    text: "Quanto tempo (em minutos) você geralmente leva para adormecer?",
    type: "number", placeholder: "Ex: 30", scored: false,
    scoreCalc: true // calculado depois
  },
  {
    num: "3", section: "Horários de sono",
    text: "Qual é o seu horário usual de levantar de manhã?",
    type: "time", placeholder: "Ex: 07:00", scored: false
  },
  {
    num: "4", section: "Duração do sono",
    text: "Quantas horas de sono você realmente dorme por noite? (pode ser diferente do tempo que fica na cama)",
    type: "number", placeholder: "Ex: 6", scored: false,
    scoreCalc: true
  },

  // BLOCO 2 — Perturbações do sono (Questão 5)
  {
    num: "5A", section: "Perturbações do sono",
    text: "Com que frequência você não conseguiu adormecer em até 30 minutos?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "5B", section: "Perturbações do sono",
    text: "Com que frequência você acordou no meio da noite ou de manhã cedo?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "5C", section: "Perturbações do sono",
    text: "Com que frequência você precisou levantar para ir ao banheiro?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "5D", section: "Perturbações do sono",
    text: "Com que frequência você não conseguiu respirar confortavelmente durante o sono?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "5E", section: "Perturbações do sono",
    text: "Com que frequência você tossiu ou roncou forte?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "5F", section: "Perturbações do sono",
    text: "Com que frequência você sentiu muito frio durante o sono?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "5G", section: "Perturbações do sono",
    text: "Com que frequência você sentiu muito calor durante o sono?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "5H", section: "Perturbações do sono",
    text: "Com que frequência você teve sonhos ruins ou pesadelos?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "5I", section: "Perturbações do sono",
    text: "Com que frequência você sentiu dor que prejudicou seu sono?",
    type: "choice", options: freqOpts, scored: true
  },

  // BLOCO 3 — Qualidade subjetiva
  {
    num: "6", section: "Qualidade geral do sono",
    text: "Como você classificaria a qualidade geral do seu sono no último mês?",
    type: "choice", scored: true,
    options: [
      { label: "Muito boa", score: 0 },
      { label: "Boa", score: 1 },
      { label: "Ruim", score: 2 },
      { label: "Muito ruim", score: 3 }
    ]
  },

  // BLOCO 4 — Uso de medicamento
  {
    num: "7", section: "Uso de medicamento",
    text: "Com que frequência você tomou medicamento para dormir (prescrito ou por conta própria)?",
    type: "choice", options: freqOpts, scored: true
  },

  // BLOCO 5 — Disfunção diurna
  {
    num: "8", section: "Funcionamento diurno",
    text: "Com que frequência você teve dificuldade para ficar acordado(a) enquanto dirigia, comia ou participava de atividade social?",
    type: "choice", options: freqOpts, scored: true
  },
  {
    num: "9", section: "Funcionamento diurno",
    text: "Quão problemático foi para você manter o ânimo e entusiasmo para suas atividades habituais?",
    type: "choice", scored: true,
    options: [
      { label: "Nenhuma dificuldade", score: 0 },
      { label: "Um problema leve", score: 1 },
      { label: "Um problema razoável", score: 2 },
      { label: "Um grande problema", score: 3 }
    ]
  },

  // BLOCO 6 — Parceiro
  {
    num: "10", section: "Parceiro de quarto",
    text: "Você tem um(a) parceiro(a), esposo(a) ou colega de quarto?",
    type: "choice", scored: false, isPartnerQ: true,
    options: [
      { label: "Não", score: 0 },
      { label: "Parceiro(a) ou colega em outro quarto", score: 0 },
      { label: "Parceiro(a) no mesmo quarto, outra cama", score: 0 },
      { label: "Parceiro(a) na mesma cama", score: 0 }
    ]
  },
  {
    num: "10E", section: "Observação do parceiro",
    text: "Seu(sua) parceiro(a) relatou: com que frequência você roncou forte?",
    type: "choice", options: freqOpts, scored: false, partnerOnly: true
  },
  {
    num: "10F", section: "Observação do parceiro",
    text: "Seu(sua) parceiro(a) relatou: com que frequência você teve longas pausas na respiração enquanto dormia?",
    type: "choice", options: freqOpts, scored: false, partnerOnly: true
  },
  {
    num: "10G", section: "Observação do parceiro",
    text: "Seu(sua) parceiro(a) relatou: com que frequência você teve contrações ou puxões nas pernas?",
    type: "choice", options: freqOpts, scored: false, partnerOnly: true
  },
  {
    num: "10H", section: "Observação do parceiro",
    text: "Seu(sua) parceiro(a) relatou: com que frequência você ficou desorientado(a) ou confuso(a) durante o sono?",
    type: "choice", options: freqOpts, scored: false, partnerOnly: true
  },
];

const results = [
  {
    range: [0, 4],
    level: "Sono Saudável",
    color: "#2e7d52",
    emoji: "🌙",
    title: "Seu sono está te recuperando bem",
    text: "Sua qualidade de sono está dentro do esperado. Seu organismo está conseguindo se recuperar durante a noite, o que é fundamental para saúde mental, imunidade e equilíbrio emocional. Continue cuidando dos seus hábitos noturnos.",
    cta: "Mesmo com um sono saudável, períodos de estresse podem comprometer rapidamente o descanso. Se notar mudanças, não espere para buscar orientação profissional."
  },
  {
    range: [5, 10],
    level: "Qualidade Comprometida",
    color: "#b8922a",
    emoji: "⚠️",
    title: "Seu sono está comprometendo sua recuperação",
    text: "Seu resultado indica que o sono não está te recuperando como deveria. Isso afeta diretamente concentração, humor, imunidade e saúde emocional. O corpo e a mente precisam de um sono reparador para funcionar bem.",
    cta: "Distúrbios do sono raramente se resolvem sozinhos. Quanto antes você identificar o que está por trás disso, mais fácil será retomar um descanso de qualidade. Podemos conversar sobre isso."
  },
  {
    range: [11, 16],
    level: "Privação Significativa",
    color: "#c0392b",
    emoji: "🔴",
    title: "Você está em privação de sono — isso é sério",
    text: "Seu padrão de sono indica privação significativa. Noites mal dormidas de forma crônica aumentam o risco de ansiedade, depressão, problemas cardiovasculares e queda na imunidade. Seu corpo está pedindo atenção.",
    cta: "Privação de sono crônica não é frescura — é um problema de saúde que precisa de atenção. Uma avaliação profissional pode identificar as causas e te ajudar a dormir melhor com muito mais rapidez."
  },
  {
    range: [17, 100],
    level: "Distúrbio do Sono",
    color: "#7b1a1a",
    emoji: "🆘",
    title: "Seus padrões indicam distúrbio do sono",
    text: "Seu resultado é preocupante e sugere um distúrbio do sono estabelecido. Esse nível de comprometimento afeta todas as áreas da sua vida — emocional, física e cognitiva. Seu corpo está pedindo ajuda.",
    cta: "Esse resultado merece atenção profissional. Não se trata de força de vontade — existem intervenções eficazes que podem transformar sua qualidade de sono e de vida. Me manda uma mensagem."
  }
];

let current = 0;
let answers = {};
let hasPartner = false;

// Filtra as perguntas com base em ter parceiro ou não
function getActiveQuestions() {
  return questions.filter(q => {
    if (q.partnerOnly) return hasPartner;
    return true;
  });
}

function startQuiz() {
  document.getElementById('screen-intro').classList.add('hidden');
  document.getElementById('screen-quiz').classList.remove('hidden');
  renderQuestion();
}

function renderQuestion() {
  const qs = getActiveQuestions();
  const q = qs[current];
  const total = qs.length;

  document.getElementById('q-counter').textContent = `Pergunta ${current + 1} de ${total}`;
  document.getElementById('q-section').textContent = q.section || '';
  document.getElementById('question-text').textContent = q.text;
  document.getElementById('progress-bar').style.width = `${(current / total) * 100}%`;
  document.getElementById('btn-prev').disabled = current === 0;

  const isLast = current === total - 1;
  document.getElementById('btn-next').textContent = isLast ? 'Ver resultado →' : 'Próxima →';

  const inputArea = document.getElementById('input-area');
  inputArea.innerHTML = '';

  const skipNote = document.getElementById('skip-note');

  if (q.type === 'time' || q.type === 'number') {
    skipNote.style.display = 'none';
    const wrap = document.createElement('div');
    wrap.className = 'text-input-wrap';
    const label = document.createElement('span');
    label.className = 'text-input-label';
    label.textContent = q.type === 'time' ? 'Informe o horário:' : 'Informe o número:';
    const inp = document.createElement('input');
    inp.type = q.type === 'time' ? 'text' : 'number';
    inp.className = 'text-input';
    inp.placeholder = q.placeholder;
    inp.value = answers[q.num] || '';
    inp.oninput = () => {
      answers[q.num] = inp.value;
      document.getElementById('btn-next').disabled = inp.value.trim() === '';
    };
    wrap.appendChild(label);
    wrap.appendChild(inp);
    inputArea.appendChild(wrap);
    document.getElementById('btn-next').disabled = !answers[q.num];

  } else if (q.type === 'choice') {
    skipNote.style.display = q.partnerOnly ? 'block' : 'none';
    const opts = document.createElement('div');
    opts.className = 'options';
    const letters = ['A','B','C','D'];
    q.options.forEach((opt, i) => {
      const btn = document.createElement('button');
      btn.className = 'option-btn' + (answers[q.num] === i ? ' selected' : '');
      btn.innerHTML = `<span class="option-letter">${letters[i]}.</span>${opt.label}`;
      btn.onclick = () => {
        answers[q.num] = i;
        // Se for pergunta do parceiro (10), registra se tem parceiro
        if (q.isPartnerQ) {
          hasPartner = (i >= 1); // opções 1,2,3 = tem parceiro
        }
        opts.querySelectorAll('.option-btn').forEach((b, idx) => b.classList.toggle('selected', idx === i));
        document.getElementById('btn-next').disabled = false;
      };
      opts.appendChild(btn);
    });
    inputArea.appendChild(opts);

    // Pular opcionais de parceiro
    if (q.partnerOnly) {
      document.getElementById('btn-next').disabled = false;
    } else {
      document.getElementById('btn-next').disabled = answers[q.num] === undefined;
    }
  }
}

function nextQ() {
  const qs = getActiveQuestions();
  if (current < qs.length - 1) {
    current++;
    renderQuestion();
  } else {
    showResult();
  }
}

function prevQ() {
  if (current > 0) { current--; renderQuestion(); }
}

function calcScore() {
  let score = 0;

  // C1 — Qualidade subjetiva (Q6)
  const q6 = questions.find(q => q.num === '6');
  if (answers['6'] !== undefined) score += q6.options[answers['6']].score;

  // C2 — Latência do sono (Q2 + 5A)
  let c2 = 0;
  const mins = parseInt(answers['2']) || 0;
  if (mins <= 15) c2 += 0;
  else if (mins <= 30) c2 += 1;
  else if (mins <= 60) c2 += 2;
  else c2 += 3;
  if (answers['5A'] !== undefined) c2 += freqOpts[answers['5A']].score;
  if (c2 === 0) score += 0;
  else if (c2 <= 2) score += 1;
  else if (c2 <= 4) score += 2;
  else score += 3;

  // C3 — Duração do sono (Q4)
  const hrs = parseFloat(answers['4']) || 0;
  if (hrs > 7) score += 0;
  else if (hrs >= 6) score += 1;
  else if (hrs >= 5) score += 2;
  else score += 3;

  // C4 — Eficiência habitual (simplificado)
  score += 0;

  // C5 — Perturbações do sono (5B a 5I)
  const distItems = ['5B','5C','5D','5E','5F','5G','5H','5I'];
  let distSum = 0;
  distItems.forEach(k => { if (answers[k] !== undefined) distSum += freqOpts[answers[k]].score; });
  if (distSum === 0) score += 0;
  else if (distSum <= 9) score += 1;
  else if (distSum <= 18) score += 2;
  else score += 3;

  // C6 — Uso de medicamento (Q7)
  if (answers['7'] !== undefined) score += freqOpts[answers['7']].score;

  // C7 — Disfunção diurna (Q8 + Q9)
  let c7 = 0;
  if (answers['8'] !== undefined) c7 += freqOpts[answers['8']].score;
  const q9 = questions.find(q => q.num === '9');
  if (answers['9'] !== undefined) c7 += q9.options[answers['9']].score;
  if (c7 === 0) score += 0;
  else if (c7 <= 2) score += 1;
  else if (c7 <= 4) score += 2;
  else score += 3;

  return score;
}

function showResult() {
  const total = calcScore();
  const result = results.find(r => total >= r.range[0] && total <= r.range[1]) || results[results.length - 1];
  const maxScore = 21;
  const pct = Math.min(Math.round((total / maxScore) * 100), 100);

  document.getElementById('screen-quiz').classList.add('hidden');
  document.getElementById('screen-result').classList.remove('hidden');

  const area = document.getElementById('result-area');
  area.style.display = 'block';
  area.innerHTML = `
    <div class="result-label">Resultado da avaliação</div>
    <div class="result-title">${result.emoji} ${result.title}</div>
    <div style="display:flex; align-items:center; gap:10px; margin-bottom:6px;">
      <span style="font-size:12px; letter-spacing:1.5px; text-transform:uppercase; color:var(--gold);">Qualidade do sono</span>
      <span style="font-size:13px; color:${result.color}; font-weight:600;">${result.level}</span>
    </div>
    <div style="display:flex; align-items:center; gap:8px; margin-bottom:16px;">
      <span style="font-size:12px; color:rgba(26,46,74,0.5);">Pontuação PSQI:</span>
      <span style="font-size:14px; color:${result.color}; font-weight:700;">${total} / 21</span>
      <span style="font-size:11px; color:rgba(26,46,74,0.4);">(acima de 5 = sono ruim)</span>
    </div>
    <div class="result-bar-wrap">
      <div class="result-bar-fill" id="res-bar" style="width:0%; background:${result.color};"></div>
    </div>
    <p class="result-text">${result.text}</p>
    <div class="result-cta">
      <p><strong>O que você pode fazer agora:</strong><br>${result.cta}</p>
    </div>
    <p class="disclaimer">Baseado no Índice de Qualidade do Sono de Pittsburgh (PSQI — Buysse et al., 1989), validado no Brasil por Bertolazi et al. (2011). Pontuação acima de 5 indica qualidade de sono ruim. Este teste não substitui avaliação clínica profissional.</p>
    <div class="divider-gold"><span></span><i>♦</i><span></span></div>
    <p style="font-size:13px; text-align:center; color:rgba(26,46,74,0.55); margin-bottom:18px;">Salve e compartilhe com quem também precisa avaliar seu sono 🌙</p>
    <button class="restart-btn" onclick="restartQuiz()">↺ Refazer a avaliação</button>
  `;

  setTimeout(() => {
    document.getElementById('res-bar').style.width = pct + '%';
  }, 200);
}

function restartQuiz() {
  current = 0;
  answers = {};
  hasPartner = false;
  document.getElementById('screen-result').classList.add('hidden');
  document.getElementById('screen-quiz').classList.remove('hidden');
  renderQuestion();
}
</script>
</body>
</html>
