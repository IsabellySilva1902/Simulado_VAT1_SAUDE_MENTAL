[simulado_saude_mental-3.html](https://github.com/user-attachments/files/32220195/simulado_saude_mental-3.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simulado Interativo: Saude Mental - Disciplina Completa</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            indigoBrand: {
              50: '#eef2ff',
              100: '#e0e7ff',
              500: '#6366f1',
              600: '#4f46e5',
              700: '#4338ca',
              800: '#3730a3',
              900: '#312e81',
            },
            night: {
              900: '#0f172a',
              950: '#020617',
            }
          }
        }
      }
    }
  </script>
  <!-- Google Fonts Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Inter', sans-serif;
    }
    .custom-scroll::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    .custom-scroll::-webkit-scrollbar-track {
      background: #f1f5f9;
    }
    .custom-scroll::-webkit-scrollbar-thumb {
      background: #cbd5e1;
      border-radius: 9999px;
    }
    .custom-scroll::-webkit-scrollbar-thumb:hover {
      background: #94a3b8;
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 min-h-screen flex flex-col antialiased selection:bg-indigoBrand-500 selection:text-white">

  <header class="bg-white border-b border-slate-200 sticky top-0 z-40 shadow-sm">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
      <div class="flex items-center space-x-3">
        <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-indigoBrand-600 to-sky-500 flex items-center justify-center text-white font-bold shadow-md shadow-indigoBrand-500/20">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"/>
          </svg>
        </div>
        <div>
          <h1 class="font-bold text-slate-900 text-lg leading-tight">Simulado: Saude Mental</h1>
          <p class="text-xs text-slate-500 font-medium">Introducao - Delirium - Esquizofrenia - TEA - TDAH - Transt. Alimentares - Sono</p>
        </div>
      </div>

      <!-- Live Quiz Meta -->
      <div id="quizMetaNav" class="hidden flex items-center space-x-3 sm:space-x-6">
        <div class="flex items-center space-x-2 bg-slate-100 py-1.5 px-3 rounded-lg border border-slate-200">
          <svg class="w-4 h-4 text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
          </svg>
          <span id="timerDisplay" class="font-mono text-sm font-semibold text-slate-700">00:00</span>
        </div>

        <div class="hidden sm:flex items-center space-x-2 text-xs font-semibold bg-indigoBrand-50 text-indigoBrand-700 border border-indigoBrand-200 py-1.5 px-3 rounded-lg">
          <span id="progressPill">Questao 1/1</span>
        </div>

        <button id="btnFinishEarly" class="text-xs font-semibold text-red-600 hover:text-red-700 hover:bg-red-50 px-3 py-1.5 rounded-lg border border-red-200 transition-colors">
          Encerrar
        </button>
      </div>
    </div>
  </header>

  <main class="flex-1 max-w-5xl w-full mx-auto p-4 sm:p-6 lg:p-8">

    <!-- Screen 1: Start Screen / Settings -->
    <div id="startScreen" class="space-y-8 py-6">
      <div class="bg-gradient-to-br from-night-950 via-night-900 to-indigoBrand-900 rounded-3xl p-8 sm:p-12 text-white shadow-xl relative overflow-hidden">
        <div class="absolute -right-12 -bottom-12 w-64 h-64 bg-indigoBrand-500/15 rounded-full blur-3xl pointer-events-none"></div>
        <div class="relative z-10 max-w-2xl">
          <span class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full text-xs font-semibold bg-indigoBrand-500/30 text-indigoBrand-200 border border-indigoBrand-400/30 mb-4">
            Restrito ao conteudo das aulas de Saude Mental (UNEXMED)
          </span>
          <h2 class="text-3xl sm:text-4xl font-extrabold tracking-tight mb-4 leading-tight">
            Simulado Completo: Saude Mental
          </h2>
          <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
            78 questoes autorais, no estilo ENAMED, cobrindo os 7 assuntos das aulas: Introducao a Saude Mental (entrevista psiquiatrica, anamnese e exame do estado mental), Delirium, Esquizofrenia, Transtorno do Espectro Autista (TEA), TDAH, Transtornos Alimentares e Transtornos do Sono-Vigilia. As questoes sao sorteadas em ordem aleatoria a cada tentativa, como em uma prova real, e os assuntos podem se cruzar nos enunciados (diagnostico diferencial entre aulas).
          </p>

          <div class="grid grid-cols-2 sm:grid-cols-3 gap-3 text-xs sm:text-sm font-medium text-slate-200">
            <div class="bg-white/10 rounded-xl p-3 border border-white/10 backdrop-blur-sm">
              <span class="block text-xl font-bold text-white mb-0.5">78</span>
              Questoes no total (7 assuntos)
            </div>
            <div class="bg-white/10 rounded-xl p-3 border border-white/10 backdrop-blur-sm">
              <span class="block text-xl font-bold text-white mb-0.5">4 Opcoes</span>
              Multipla Escolha (A, B, C, D)
            </div>
            <div class="bg-white/10 rounded-xl p-3 border border-white/10 backdrop-blur-sm col-span-2 sm:col-span-1">
              <span class="block text-xl font-bold text-white mb-0.5">100%</span>
              Gabarito Comentado
            </div>
          </div>
        </div>
      </div>

      <!-- Settings Card -->
      <div class="bg-white rounded-2xl border border-slate-200 p-6 sm:p-8 shadow-sm">
        <h3 class="text-lg font-bold text-slate-900 mb-4 flex items-center gap-2">
          <svg class="w-5 h-5 text-indigoBrand-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"/>
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/>
          </svg>
          Modo e Selecao de Conteudo
        </h3>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div>
            <label class="block text-sm font-semibold text-slate-700 mb-2">Modo de Resolucao</label>
            <div class="grid grid-cols-2 gap-3">
              <label class="flex flex-col p-3.5 border-2 rounded-xl cursor-pointer transition-all hover:border-indigoBrand-500 border-indigoBrand-600 bg-indigoBrand-50/40" id="labelModeExam">
                <input type="radio" name="quizMode" value="exam" checked class="sr-only">
                <span class="font-bold text-sm text-slate-900 flex items-center gap-1.5">
                  Simulado Real
                </span>
                <span class="text-xs text-slate-500 mt-1">Gabarito e estatisticas apresentados somente ao termino.</span>
              </label>

              <label class="flex flex-col p-3.5 border-2 rounded-xl cursor-pointer transition-all hover:border-indigoBrand-500 border-slate-200 bg-white" id="labelModeTutor">
                <input type="radio" name="quizMode" value="tutor" class="sr-only">
                <span class="font-bold text-sm text-slate-900 flex items-center gap-1.5">
                  Modo Tutor
                </span>
                <span class="text-xs text-slate-500 mt-1">Explicacoes clinicas imediatas a cada escolha.</span>
              </label>
            </div>
          </div>

          <div>
            <label class="block text-sm font-semibold text-slate-700 mb-2">Foco Tematico</label>
            <select id="topicFilter" class="w-full bg-white border border-slate-300 rounded-xl px-4 py-2.5 text-sm font-medium text-slate-700 focus:outline-none focus:ring-2 focus:ring-indigoBrand-500 focus:border-indigoBrand-500">
              <option value="all">Todos os 7 Assuntos (Simulado Completo)</option>
              <option value="Introducao">Foco: Introducao a Saude Mental (entrevista, anamnese, EEM)</option>
              <option value="Delirium">Foco: Delirium</option>
              <option value="Esquizofrenia">Foco: Esquizofrenia</option>
              <option value="TEA">Foco: Transtorno do Espectro Autista (TEA)</option>
              <option value="TDAH">Foco: TDAH</option>
              <option value="Alimentares">Foco: Transtornos Alimentares</option>
              <option value="Sono">Foco: Transtornos do Sono-Vigilia</option>
            </select>
            <p class="text-xs text-slate-400 mt-2">Ordem sorteada aleatoriamente a cada tentativa, como numa prova.</p>
          </div>
        </div>

        <div class="mt-8 pt-6 border-t border-slate-100 flex flex-col sm:flex-row items-center justify-between gap-4">
          <div class="text-xs text-slate-500 flex items-center gap-2">
            <svg class="w-4 h-4 text-emerald-500" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
            </svg>
            Cada assunto tem no minimo 10 questoes; os enunciados podem cruzar temas (ex.: Delirium x Esquizofrenia, TEA x TDAH, Sono x Humor).
          </div>
          <button id="btnStartQuiz" class="w-full sm:w-auto px-8 py-3.5 bg-indigoBrand-600 hover:bg-indigoBrand-700 active:scale-98 text-white font-bold rounded-xl shadow-lg shadow-indigoBrand-600/25 transition-all text-sm flex items-center justify-center gap-2">
            Comecar Simulado
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/>
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Screen 2: Active Question Card -->
    <div id="quizScreen" class="hidden space-y-6">
      <div class="bg-white rounded-2xl p-4 sm:p-5 border border-slate-200 shadow-sm flex flex-col gap-4">
        <div class="flex items-center justify-between text-xs font-semibold text-slate-500">
          <span id="labelQuestionNumber" class="text-slate-800 font-bold text-sm">Questao 1 de 1</span>
          <div class="flex items-center gap-2">
            <button id="btnFlagQuestion" class="flex items-center gap-1 text-slate-500 hover:text-amber-600 transition-colors">
              <svg id="flagIcon" class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 21v-4m0 0V5a2 2 0 012-2h6.5l1 1H21l-3 6 3 6h-8.5l-1-1H5a2 2 0 00-2 2zm9-13.5V9"/>
              </svg>
              <span id="flagText">Marcar para revisar</span>
            </button>
          </div>
        </div>

        <div class="w-full bg-slate-100 rounded-full h-2 overflow-hidden">
          <div id="progressBar" class="bg-indigoBrand-600 h-full transition-all duration-300 rounded-full" style="width: 1%;"></div>
        </div>

        <div id="questionPillPalette" class="flex flex-wrap gap-1.5 pt-1 overflow-x-auto custom-scroll pb-1"></div>
      </div>

      <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden transition-all">
        <div class="px-6 py-4 bg-slate-50/80 border-b border-slate-100 flex flex-wrap items-center justify-between gap-2">
          <div class="flex items-center gap-2">
            <span id="badgeTheme" class="px-2.5 py-1 text-xs font-bold rounded-lg bg-indigo-100 text-indigo-800 border border-indigo-200">
              Categoria
            </span>
            <span id="badgeDifficulty" class="px-2.5 py-1 text-xs font-semibold rounded-lg bg-slate-200 text-slate-700">
              Intermediaria
            </span>
          </div>
          <span class="text-xs text-slate-400 font-mono">ID: <span id="questionCode">COD-01</span></span>
        </div>

        <div class="p-6 sm:p-8">
          <p id="questionPrompt" class="text-slate-800 text-base sm:text-lg leading-relaxed font-medium mb-6"></p>
          <div id="optionsContainer" class="space-y-3"></div>
          <div id="immediateFeedbackBox" class="hidden mt-6 p-5 rounded-xl border"></div>
        </div>

        <div class="px-6 py-4 bg-slate-50 border-t border-slate-100 flex items-center justify-between">
          <button id="btnPrevQuestion" class="px-4 py-2 text-sm font-semibold text-slate-600 hover:text-slate-900 bg-white hover:bg-slate-100 rounded-xl border border-slate-200 transition-all disabled:opacity-40 disabled:cursor-not-allowed">
            &larr; Anterior
          </button>
          <div class="flex items-center gap-2">
            <button id="btnNextQuestion" class="px-6 py-2 text-sm font-bold text-white bg-indigoBrand-600 hover:bg-indigoBrand-700 rounded-xl shadow-md shadow-indigoBrand-600/20 transition-all">
              Proxima &rarr;
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Screen 3: Results & Review -->
    <div id="resultsScreen" class="hidden space-y-8 py-4">
      <div class="bg-white rounded-3xl border border-slate-200 p-6 sm:p-10 shadow-sm">
        <div class="text-center max-w-xl mx-auto mb-8">
          <div id="scoreBadgeIcon" class="w-16 h-16 mx-auto mb-4 rounded-2xl bg-indigoBrand-100 text-indigoBrand-600 flex items-center justify-center font-black text-2xl shadow-inner"></div>
          <h2 class="text-2xl sm:text-3xl font-black text-slate-900 mb-2">Desempenho no Simulado</h2>
          <p id="scoreFeedbackSummary" class="text-slate-600 text-sm">
            Avaliacao comparativa segundo o conteudo das 7 aulas de Saude Mental.
          </p>
        </div>

        <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 sm:gap-4 mb-8">
          <div class="bg-slate-50 rounded-2xl p-4 border border-slate-100 text-center">
            <span class="text-xs font-semibold text-slate-500 uppercase tracking-wider block mb-1">Aproveitamento</span>
            <span id="metricScorePercent" class="text-2xl sm:text-3xl font-black text-slate-900">0%</span>
          </div>
          <div class="bg-emerald-50 rounded-2xl p-4 border border-emerald-100 text-center">
            <span class="text-xs font-semibold text-emerald-600 uppercase tracking-wider block mb-1">Acertos</span>
            <span id="metricCorrectCount" class="text-2xl sm:text-3xl font-black text-emerald-700">0</span>
          </div>
          <div class="bg-rose-50 rounded-2xl p-4 border border-rose-100 text-center">
            <span class="text-xs font-semibold text-rose-600 uppercase tracking-wider block mb-1">Erros</span>
            <span id="metricWrongCount" class="text-2xl sm:text-3xl font-black text-rose-700">0</span>
          </div>
          <div class="bg-amber-50 rounded-2xl p-4 border border-amber-100 text-center">
            <span class="text-xs font-semibold text-amber-600 uppercase tracking-wider block mb-1">Tempo Total</span>
            <span id="metricTotalTime" class="text-2xl sm:text-3xl font-black text-amber-700">00:00</span>
          </div>
        </div>

        <div class="mb-8">
          <h3 class="text-base font-bold text-slate-900 mb-4 flex items-center gap-2">
            <svg class="w-5 h-5 text-indigoBrand-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"/>
            </svg>
            Desempenho por Assunto
          </h3>
          <div id="topicPerformanceList" class="space-y-3"></div>
        </div>

        <div class="flex flex-col sm:flex-row items-center justify-center gap-4 pt-4 border-t border-slate-100">
          <button id="btnRestartQuiz" class="w-full sm:w-auto px-6 py-3 rounded-xl bg-indigoBrand-600 hover:bg-indigoBrand-700 text-white font-bold text-sm shadow-md transition-all">
            Refazer Simulado
          </button>
          <button id="btnReviewAllDetailed" class="w-full sm:w-auto px-6 py-3 rounded-xl bg-slate-100 hover:bg-slate-200 text-slate-700 font-bold text-sm transition-all">
            Revisar Gabarito Completo e Justificativas
          </button>
        </div>
      </div>

      <div id="reviewDetailedSection" class="bg-white rounded-3xl border border-slate-200 p-6 sm:p-8 shadow-sm space-y-6">
        <h3 class="text-xl font-bold text-slate-900 flex items-center justify-between">
          <span>Caderno de Resolucoes Detalhadas</span>
          <span class="text-xs text-slate-500 font-normal">Todas as 4 alternativas comentadas</span>
        </h3>
        <div id="reviewQuestionsContainer" class="space-y-6"></div>
      </div>
    </div>
  </main>

  <!-- Modal confirmation -->
  <div id="customModal" class="hidden fixed inset-0 z-50 bg-slate-900/50 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white rounded-2xl max-w-md w-full p-6 shadow-2xl border border-slate-100">
      <h4 class="text-lg font-bold text-slate-900 mb-2">Encerrar Simulado?</h4>
      <p id="modalMessage" class="text-sm text-slate-600 mb-6">
        Voce ainda possui questoes sem resposta. Deseja finalizar agora?
      </p>
      <div class="flex items-center justify-end gap-3">
        <button id="btnModalCancel" class="px-4 py-2 text-sm font-semibold text-slate-600 hover:bg-slate-100 rounded-xl transition-all">
          Continuar Respondendo
        </button>
        <button id="btnModalConfirm" class="px-4 py-2 text-sm font-bold text-white bg-red-600 hover:bg-red-700 rounded-xl transition-all">
          Sim, Finalizar
        </button>
      </div>
    </div>
  </div>

  <script>
    const QUESTIONS_DATABASE = [
  {
    "id": 2,
    "code": "INTRO-02",
    "category": "Introducao",
    "subcategory": "Exame do Estado Mental: Sensopercepção",
    "difficulty": "Intermediária",
    "prompt": "Vagner, 29 anos, operário de fábrica, é atendido em um ambulatório de Feira de Santana relatando ansiedade e insônia há duas semanas. Durante a entrevista, ele hesita antes de responder a uma pergunta e, por fim, admite que, à noite, ouve um sussurro repetindo seu nome, mesmo estando sozinho em casa. Diante disso, o médico pergunta: \"Você tem ouvido ou visto coisas que outras pessoas não percebem?\" Segundo o roteiro do Exame do Estado Mental apresentado na disciplina, essa pergunta investiga qual domínio, e o que mais deve ser explorado diante de uma resposta positiva como a de Vagner?",
    "options": [
      {
        "letter": "A",
        "text": "Pensamento — Conteúdo; deve-se investigar apenas se há delírios associados.",
        "rationale": "Incorreta. O Pensamento — Conteúdo refere-se a delírios, ideação suicida e obsessões; a pergunta sobre ouvir ou ver coisas que outras pessoas não percebem investiga outro domínio, embora os dois possam coexistir no mesmo paciente."
      },
      {
        "letter": "B",
        "text": "Sensopercepção; deve-se investigar a modalidade (auditiva, visual, tátil), o conteúdo e se ocorre durante a própria entrevista.",
        "rationale": "CORRETA. Essa é exatamente a pergunta-modelo apresentada para investigar o domínio de Sensopercepção (alucinações e ilusões); diante de resposta positiva, o roteiro da disciplina orienta explorar a modalidade (auditiva, visual, tátil), o conteúdo relatado e se o fenômeno ocorre durante a própria entrevista."
      },
      {
        "letter": "C",
        "text": "Cognição; deve-se avaliar apenas orientação e memória imediata.",
        "rationale": "Incorreta. A Cognição é avaliada por meio de orientação (tempo, espaço, pessoa), memória e atenção — não pela pergunta sobre ouvir/ver coisas que os outros não percebem."
      },
      {
        "letter": "D",
        "text": "Insight e Julgamento; deve-se avaliar se o paciente reconhece o próprio adoecimento.",
        "rationale": "Incorreta. Insight e Julgamento são avaliados por perguntas como \"O senhor acredita que está passando por algum problema de saúde?\", e não pela investigação de alucinações."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Domínio de Sensopercepção no EEM: investiga alucinações e ilusões. Pergunta-modelo: \"Você tem ouvido/visto coisas que outras pessoas não percebem?\" — diante de resposta positiva, explorar modalidade, conteúdo, e se ocorre durante a própria entrevista."
  },
  {
    "id": 3,
    "code": "INTRO-03",
    "category": "Introducao",
    "subcategory": "Entrevista psiquiátrica: técnicas de vínculo",
    "difficulty": "Intermediária",
    "prompt": "Dona Zenaide, 58 anos, dona de casa, está internada em um hospital de Ilhéus para investigação de uma dor abdominal recorrente sem causa clínica identificada até o momento. Durante a entrevista, ela chora ao relatar que está com medo de ter uma doença grave e de não conseguir mais cuidar da casa sozinha. Atento ao estado emocional dela, o médico residente diz: \"Imagino como isso deve estar sendo difícil para você.\" Segundo as técnicas de vínculo na entrevista apresentadas na disciplina, essa fala exemplifica qual tipo de vínculo?",
    "options": [
      {
        "letter": "A",
        "text": "Vínculo de Autenticidade.",
        "rationale": "Incorreta. O vínculo de autenticidade refere-se a apresentar-se de forma simples e genuína, como \"pessoa comum\", reduzindo a tensão inicial da entrevista (ex.: comentar sobre a cidade natal do paciente)."
      },
      {
        "letter": "B",
        "text": "Vínculo de Empatia.",
        "rationale": "CORRETA. O vínculo de empatia consiste em reconhecer a perspectiva emocional do paciente, mantendo a própria objetividade — \"sentir a dor do outro\" sem se confundir com ela. A fala \"Imagino como isso deve estar sendo difícil para você\" é o exemplo clássico apresentado em aula para esse tipo de vínculo."
      },
      {
        "letter": "C",
        "text": "Vínculo de Conhecimento.",
        "rationale": "Incorreta. O vínculo de conhecimento consiste em validar os sintomas relatados e conduzir perguntas pertinentes, transmitindo preparo técnico para ajudar (ex.: \"A senhora tem notado também perda de interesse e de sono?\")."
      },
      {
        "letter": "D",
        "text": "Vínculo de Autoridade Técnica.",
        "rationale": "Incorreta. Essa categoria não foi descrita na aula; as três técnicas de vínculo apresentadas foram autenticidade, empatia e conhecimento."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "As três técnicas de vínculo na entrevista psiquiátrica: Autenticidade (apresentação genuína), Empatia (reconhecer a perspectiva emocional do paciente) e Conhecimento (validar sintomas com perguntas pertinentes)."
  },
  {
    "id": 4,
    "code": "INTRO-04",
    "category": "Introducao",
    "subcategory": "Roteiro de anamnese psiquiátrica",
    "difficulty": "Intermediária",
    "prompt": "Ronaldo, 34 anos, mecânico, é atendido pela primeira vez no ambulatório de Saúde Mental de Feira de Santana por episódios de tristeza e desânimo. Ao conduzir a anamnese, o estudante de medicina já registrou a queixa principal e a história da doença atual, e chega agora à seção de Antecedentes Familiares do roteiro. Segundo esse roteiro, apresentado na disciplina, qual conjunto de informações deve sempre ser investigado nessa seção?",
    "options": [
      {
        "letter": "A",
        "text": "Medicamentos atuais em uso pelo próprio paciente e possíveis efeitos adversos.",
        "rationale": "Incorreta. Medicamentos em uso pelo paciente compõem a seção específica de Medicamentos em Uso, não a de Antecedentes Familiares."
      },
      {
        "letter": "B",
        "text": "Suicídio, dependência química e causas de morte na família.",
        "rationale": "CORRETA. O roteiro de anamnese apresentado destaca explicitamente que, nos Antecedentes Familiares, deve-se SEMPRE investigar suicídio, dependência química e causas de morte na família, além de doenças clínicas ou psiquiátricas relevantes e condições hereditárias."
      },
      {
        "letter": "C",
        "text": "Alergias medicamentosas do próprio paciente.",
        "rationale": "Incorreta. Alergias compõem uma seção própria da anamnese (Alergias), distinta dos Antecedentes Familiares."
      },
      {
        "letter": "D",
        "text": "Rotina de sono e alimentação do paciente.",
        "rationale": "Incorreta. Sono, alimentação e atividade física compõem a seção de Hábitos de Vida, não a de Antecedentes Familiares."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Antecedentes Familiares: sempre investigar suicídio, dependência química e causas de morte na família, além de doenças clínicas/psiquiátricas e condições hereditárias relevantes."
  },
  {
    "id": 5,
    "code": "INTRO-05",
    "category": "Introducao",
    "subcategory": "Exame do Estado Mental: humor x afeto",
    "difficulty": "Intermediária",
    "prompt": "Marcelo, 41 anos, comerciante, é atendido em Vitória da Conquista após a esposa notar longos períodos de isolamento em casa. No Exame do Estado Mental, ele relata sentir-se \"vazio\" quando questionado sobre como está se sentindo emocionalmente, falando em tom monocórdico, enquanto o examinador observa, ao longo de toda a entrevista, expressão facial pouco variável e reduzida amplitude emocional, mesmo ao relatar assuntos que antes o emocionariam. Esses dois achados — o relato de \"vazio\" e a expressão facial pouco variável — correspondem, respectivamente, a quais domínios do exame psíquico?",
    "options": [
      {
        "letter": "A",
        "text": "Ambos correspondem exclusivamente ao domínio de Afeto.",
        "rationale": "Incorreta. O relato subjetivo do paciente sobre como se sente corresponde ao Humor, não ao Afeto."
      },
      {
        "letter": "B",
        "text": "Humor (subjetivo) e Afeto (objetivo), respectivamente.",
        "rationale": "CORRETA. O Humor é o que o paciente relata sentir (\"vazio\", nas palavras do paciente), enquanto o Afeto é a expressão emocional observada objetivamente pelo examinador durante a entrevista — no caso, a expressividade facial reduzida."
      },
      {
        "letter": "C",
        "text": "Afeto (objetivo) e Humor (subjetivo), respectivamente.",
        "rationale": "Incorreta. A ordem está invertida: o relato subjetivo do paciente é o Humor, e a observação objetiva do examinador é o Afeto."
      },
      {
        "letter": "D",
        "text": "Ambos correspondem ao domínio de Pensamento — Conteúdo.",
        "rationale": "Incorreta. Pensamento — Conteúdo refere-se a delírios, ideação suicida e obsessões, não à esfera afetiva."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "No Exame do Estado Mental: Humor é subjetivo (o que o paciente relata sentir, idealmente entre aspas, com as palavras do paciente); Afeto é objetivo (expressão emocional observada e sua congruência com o humor relatado)."
  },
  {
    "id": 6,
    "code": "INTRO-06",
    "category": "Introducao",
    "subcategory": "Avaliação de risco de suicídio",
    "difficulty": "Intermediária",
    "prompt": "João Pedro, estudante do 4º ano de Medicina em estágio na emergência de um hospital de Salvador, atende um paciente de humor visivelmente deprimido, fala lenta e olhar baixo. Apesar de notar sinais de sofrimento intenso, ele evita perguntar diretamente sobre ideação suicida, com medo de \"plantar a ideia\" na cabeça do paciente. Segundo as boas práticas discutidas na disciplina de Saúde Mental sobre avaliação de risco, essa conduta de João Pedro está correta?",
    "options": [
      {
        "letter": "A",
        "text": "Sim, perguntar sobre suicídio pode induzir comportamento autolesivo e deve sempre ser evitado.",
        "rationale": "Incorreta. A aula é explícita ao afirmar que perguntar sobre suicídio NÃO induz o comportamento — o paciente frequentemente espera que essa porta seja aberta pelo entrevistador."
      },
      {
        "letter": "B",
        "text": "Não; a pergunta direta sobre ideação suicida não aumenta o risco e é indispensável para o manejo seguro do paciente.",
        "rationale": "CORRETA. A avaliação de risco (ideação, planejamento, acesso a meios, tentativas anteriores) deve ser sistemática em toda entrevista psiquiátrica; comportamentos passados são o maior preditor de risco futuro, e a pergunta direta deve sempre ser feita, mesmo sem sinais evidentes."
      },
      {
        "letter": "C",
        "text": "Sim, mas apenas em pacientes sem qualquer histórico psiquiátrico prévio.",
        "rationale": "Incorreta. A recomendação de perguntar diretamente vale para toda avaliação de risco, independentemente de histórico prévio."
      },
      {
        "letter": "D",
        "text": "A pergunta só deve ser feita se o paciente mencionar espontaneamente tristeza ou desesperança.",
        "rationale": "Incorreta. A avaliação de risco de suicídio deve ser ativa e sistemática, não condicionada a uma menção espontânea do paciente."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Perguntar sobre suicídio não induz o comportamento; comportamentos passados são o maior preditor de risco futuro — a investigação ativa deve fazer parte de toda entrevista psiquiátrica."
  },
  {
    "id": 7,
    "code": "INTRO-07",
    "category": "Introducao",
    "subcategory": "Técnicas de vínculo: autenticidade e conhecimento",
    "difficulty": "Intermediária",
    "prompt": "Seu Antônio, pescador de 61 anos, chega visivelmente tenso à primeira consulta em um ambulatório de Ilhéus, mal olhando para o médico. Buscando reduzir a tensão inicial, o médico comenta de forma descontraída: \"Vi que o senhor é lá da Barra — adoro aquela região!\", apresentando-se de forma simples e genuína. Aos poucos, Seu Antônio relaxa e passa a falar mais abertamente; então o médico pergunta: \"O senhor tem notado também perda de interesse e de sono?\", conduzindo perguntas pertinentes que transmitem preparo técnico para ajudar. Essas duas falas exemplificam, respectivamente, quais técnicas de vínculo na entrevista psiquiátrica?",
    "options": [
      {
        "letter": "A",
        "text": "Vínculo de Empatia e Vínculo de Autenticidade.",
        "rationale": "Incorreta. Nenhuma das duas falas corresponde ao vínculo de empatia (que envolveria reconhecer a perspectiva emocional do paciente, como em \"imagino como isso deve estar sendo difícil para você\")."
      },
      {
        "letter": "B",
        "text": "Vínculo de Autenticidade e Vínculo de Conhecimento.",
        "rationale": "CORRETA. O comentário sobre a cidade natal do paciente exemplifica o vínculo de Autenticidade (apresentar-se de forma simples e genuína, como \"pessoa comum\", reduzindo a tensão inicial da entrevista); a pergunta sobre sintomas específicos exemplifica o vínculo de Conhecimento (validar os sintomas relatados e conduzir perguntas pertinentes, transmitindo preparo técnico para ajudar)."
      },
      {
        "letter": "C",
        "text": "Vínculo de Conhecimento e Vínculo de Empatia.",
        "rationale": "Incorreta. A ordem e a correspondência estão erradas: a primeira fala é de Autenticidade, e a segunda é de Conhecimento, não de Empatia."
      },
      {
        "letter": "D",
        "text": "Ambas as falas correspondem ao mesmo tipo de vínculo (Empatia).",
        "rationale": "Incorreta. As duas falas exemplificam técnicas distintas de vínculo, nenhuma delas sendo a de Empatia."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "As três técnicas de vínculo na entrevista psiquiátrica: Autenticidade (apresentação genuína, como \"pessoa comum\"), Empatia (reconhecer a perspectiva emocional do paciente) e Conhecimento (validar sintomas com perguntas pertinentes, transmitindo preparo técnico)."
  },
  {
    "id": 8,
    "code": "INTRO-08",
    "category": "Introducao",
    "subcategory": "Relação médico-paciente",
    "difficulty": "Intermediária",
    "prompt": "Durante a supervisão de um atendimento em Feira de Santana, a preceptora nota que a interna Camila dedicou os primeiros dez minutos da consulta apenas a ouvir a história do paciente, sem interrompê-lo nem partir direto para perguntas objetivas, mesmo com a agenda do ambulatório cheia. Questionada sobre essa escolha, Camila responde que, em Psiquiatria, compreender a vivência do paciente já é parte do próprio tratamento. Segundo a fundamentação teórica apresentada na aula introdutória de Saúde Mental, qual afirmação melhor resume o raciocínio de Camila sobre o papel da relação médico-paciente?",
    "options": [
      {
        "letter": "A",
        "text": "A relação médico-paciente é dispensável diante da disponibilidade de exames complementares confirmatórios em Psiquiatria.",
        "rationale": "Incorreta. A aula destaca que, diferente de outras especialidades, não existe exame laboratorial ou de imagem confirmatório para a maioria dos transtornos mentais — o diagnóstico permanece essencialmente clínico."
      },
      {
        "letter": "B",
        "text": "Diferente de outras especialidades, a entrevista psiquiátrica se apoia fortemente na relação interpessoal, sendo a compreensão empática do sofrimento do paciente, ela própria, parte do método diagnóstico e terapêutico.",
        "rationale": "CORRETA. Conforme citado de Kaplan & Sadock (2017), \"a entrevista psiquiátrica é o elemento mais importante na avaliação e no tratamento de pessoas com doença mental\"; o psiquiatra é, antes de tudo, um especialista em relações interpessoais."
      },
      {
        "letter": "C",
        "text": "A relação médico-paciente só é relevante em contextos de internação psiquiátrica involuntária.",
        "rationale": "Incorreta. A relação médico-paciente é apresentada como o alicerce de toda a prática em Saúde Mental, não restrita a contextos de internação."
      },
      {
        "letter": "D",
        "text": "O vínculo terapêutico deve ser evitado para preservar a objetividade clínica do examinador.",
        "rationale": "Incorreta. Princípios como respeito, paciência, cordialidade, empatia e interesse genuíno são descritos como decisivos — eles constroem, e não comprometem, a relação clínica."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "\"A entrevista psiquiátrica é o elemento mais importante na avaliação e no tratamento de pessoas com doença mental\" (Kaplan & Sadock, 2017) — o psiquiatra é, antes de tudo, um especialista em relações interpessoais."
  },
  {
    "id": 9,
    "code": "INTRO-09",
    "category": "Introducao",
    "subcategory": "Exame do Estado Mental: forma x conteúdo do pensamento",
    "difficulty": "Intermediária",
    "prompt": "Severino, 47 anos, agricultor, é atendido no ambulatório de Juazeiro após a família notar mudanças de comportamento. Durante a entrevista, ele relata, de forma coerente e com sequência lógica de ideias, uma crença fixa e irredutível de que vizinhos estariam se reunindo para prejudicá-lo, sem que o médico consiga demovê-lo dessa ideia por meio de argumentos. Esses dois achados — a crença fixa e irredutível, e a organização lógica do discurso — correspondem, respectivamente, a quais domínios do Exame do Estado Mental?",
    "options": [
      {
        "letter": "A",
        "text": "Pensamento — Forma alterada e Pensamento — Conteúdo normal.",
        "rationale": "Incorreta. A ordem está invertida: a crença fixa e irredutível é uma alteração de Conteúdo, e o discurso organizado indica Forma preservada."
      },
      {
        "letter": "B",
        "text": "Pensamento — Conteúdo alterado (delírio persecutório) e Pensamento — Forma preservada (discurso organizado).",
        "rationale": "CORRETA. O Pensamento — Conteúdo refere-se a delírios, ideação suicida e obsessões (aqui, delírio persecutório); o Pensamento — Forma refere-se ao curso e à organização das ideias, que neste caso está preservada (discurso organizado, sem saltos ou bloqueios)."
      },
      {
        "letter": "C",
        "text": "Sensopercepção alterada e Cognição preservada.",
        "rationale": "Incorreta. Sensopercepção refere-se a alucinações e ilusões, não a crenças fixas; o caso não menciona alterações perceptivas."
      },
      {
        "letter": "D",
        "text": "Insight preservado e Julgamento alterado.",
        "rationale": "Incorreta. Insight e Julgamento referem-se à consciência de adoecimento, não descritos no caso apresentado."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Pensamento — Forma: curso e organização das ideias (ex.: organizado, acelerado, tangencial). Pensamento — Conteúdo: delírios, ideação suicida, obsessões."
  },
  {
    "id": 10,
    "code": "INTRO-10",
    "category": "Introducao",
    "subcategory": "Anamnese: registro da queixa principal",
    "difficulty": "Intermediária",
    "prompt": "Ao atender Dona Marlene, 63 anos, costureira, em sua primeira consulta na UBS de Alagoinhas, o estudante de medicina ouve dela: \"Estou sem dormir e sem vontade de fazer nada há um mês.\" Na hora de registrar a Queixa Principal no prontuário, ele hesita entre transcrever exatamente essa frase ou reescrevê-la em termos técnicos, como \"paciente refere insônia e anedonia\". Segundo a rotina de anamnese apresentada na disciplina, como essa queixa deve ser preferencialmente registrada?",
    "options": [
      {
        "letter": "A",
        "text": "Sempre reformulada em termos técnicos médicos, mesmo que o paciente não os utilize.",
        "rationale": "Incorreta. O roteiro de anamnese recomenda registrar a queixa preferencialmente com as palavras do próprio paciente, não em jargão técnico."
      },
      {
        "letter": "B",
        "text": "Preferencialmente com as palavras do próprio paciente, sempre que possível.",
        "rationale": "CORRETA. O roteiro de anamnese é explícito: a Queixa Principal deve registrar o motivo principal da consulta, preferencialmente com as palavras do próprio paciente (exemplo dado em aula: \"Estou sem dormir e sem vontade de fazer nada há um mês\")."
      },
      {
        "letter": "C",
        "text": "Exclusivamente como um código diagnóstico da CID-10, sem descrição textual.",
        "rationale": "Incorreta. A anamnese não se resume a um código de classificação; a queixa principal deve ser registrada de forma descritiva."
      },
      {
        "letter": "D",
        "text": "Apenas como uma lista de sintomas, sem qualquer relação com o motivo da consulta.",
        "rationale": "Incorreta. A queixa principal deve refletir o motivo da consulta, contextualizando o restante da entrevista."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Queixa Principal: motivo da consulta, preferencialmente registrado com as palavras do próprio paciente."
  },
  {
    "id": 11,
    "code": "INTRO-11",
    "category": "Introducao",
    "subcategory": "Anamnese e organicidade (integração com Delirium)",
    "difficulty": "Avançada",
    "prompt": "Durante a supervisão de um caso em Camaçari, o preceptor pergunta ao interno Diego por que ele insistiu tanto em perguntar sobre o início exato dos sintomas e sobre quais medicamentos o paciente estava usando, antes mesmo de cogitar um diagnóstico psiquiátrico. Diego explica que queria primeiro descartar uma causa orgânica para a confusão mental do paciente, tema que será aprofundado na aula de Delirium. Qual conjunto de informações da anamnese é classicamente mais relevante para esse raciocínio?",
    "options": [
      {
        "letter": "A",
        "text": "História psicossocial detalhada, incluindo relacionamentos e rede de apoio.",
        "rationale": "Incorreta. Embora relevante para o cuidado global, a história psicossocial não é o elemento mais diretamente associado ao levantamento de suspeita de organicidade em um quadro confusional agudo."
      },
      {
        "letter": "B",
        "text": "Início e curso temporal dos sintomas (agudo e flutuante), associados aos antecedentes pessoais patológicos e aos medicamentos em uso.",
        "rationale": "CORRETA. Dentro do mapa geral da anamnese, os itens \"História da Doença Atual\" (início, duração, evolução), \"Antecedentes Pessoais Patológicos\" e \"Medicamentos em Uso\" são os que mais diretamente apontam para uma causa orgânica — exatamente os elementos que, na aula de Delirium, caracterizam o início agudo e o curso flutuante típicos dessa síndrome, em contraste com o curso insidioso dos transtornos psiquiátricos primários."
      },
      {
        "letter": "C",
        "text": "Hábitos de vida relacionados ao consumo de cafeína.",
        "rationale": "Incorreta. Embora integre a anamnese, o consumo de cafeína isoladamente tem relevância muito menor do que o curso temporal dos sintomas e os antecedentes patológicos para a suspeita de organicidade."
      },
      {
        "letter": "D",
        "text": "Condições socioeconômicas, culturais e ambientais.",
        "rationale": "Incorreta. Esses dados contextualizam o cuidado, mas não são o elemento central para diferenciar um quadro orgânico agudo de um transtorno psiquiátrico primário."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "A anamnese (início/curso dos sintomas, antecedentes patológicos, medicações em uso) é a ferramenta central tanto para o raciocínio diagnóstico geral quanto para identificar sinais de alerta de organicidade — tema retomado na aula de Delirium."
  },
  {
    "id": 12,
    "code": "DELIRIUM-01",
    "category": "Delirium",
    "subcategory": "Espectro da consciência",
    "difficulty": "Avançada",
    "prompt": "Osvaldo, 66 anos, é internado em um hospital de Vitória da Conquista para uma cirurgia ortopédica eletiva. Minutos após o término do procedimento, ainda sob efeito residual da anestesia geral, ele não abre os olhos nem responde quando chamado pelo nome, mas apresenta movimentos motores desorganizados dos braços. A equipe de recuperação pós-anestésica discute se já é possível classificar esse quadro como delirium. Segundo o conceito de delirium como um espectro contínuo entre a consciência plena e o coma, é correto afirmar que:",
    "options": [
      {
        "letter": "A",
        "text": "O diagnóstico de delirium pode ser firmado neste momento, pois os movimentos motores desorganizados já são suficientes.",
        "rationale": "Incorreta. Movimentos motores isolados, na ausência de resposta a estímulos verbais, não substituem o critério de excitação cortical mínima exigido para o diagnóstico."
      },
      {
        "letter": "B",
        "text": "O diagnóstico de delirium não deve ser firmado enquanto o paciente estiver em nível de consciência compatível com coma/sedação profunda, pois é necessário grau suficiente de excitação cortical para resposta a estímulos verbais.",
        "rationale": "CORRETA. O delirium situa-se em um espectro contínuo entre a consciência plena e o coma; para que exista delirium, é necessário grau suficiente de excitação cortical para resposta a estímulos verbais — por isso o diagnóstico não é feito no contexto de coma, embora possa surgir na recuperação de um estado comatoso ou de sedação profunda."
      },
      {
        "letter": "C",
        "text": "A ausência de resposta a estímulos verbais já é, por si só, suficiente para diagnosticar delirium hipoativo.",
        "rationale": "Incorreta. O delirium hipoativo cursa com lentificação e sonolência, mas ainda dentro do espectro em que há alguma resposta a estímulos verbais — não equivale à ausência completa de resposta compatível com coma/sedação profunda."
      },
      {
        "letter": "D",
        "text": "O delirium está sempre excluído em qualquer paciente no pós-operatório imediato.",
        "rationale": "Incorreta. O período pós-operatório é, ao contrário, um contexto clássico de alto risco para delirium — a exclusão aqui se refere apenas ao momento específico de sedação profunda, não ao pós-operatório como um todo."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "O delirium situa-se em um espectro contínuo entre consciência plena e coma; o diagnóstico exige excitação cortical suficiente para resposta a estímulos verbais, não sendo feito durante coma ou sedação profunda, embora possa emergir na fase de recuperação."
  },
  {
    "id": 13,
    "code": "DELIRIUM-02",
    "category": "Delirium",
    "subcategory": "Epidemiologia e subdiagnóstico",
    "difficulty": "Intermediária",
    "prompt": "Durante uma aula de revisão sobre delirium em um hospital-escola de Salvador, um residente relata o caso de uma paciente idosa que ficou \"mais quietinha\" por dias na enfermaria, sem qualquer investigação, até ser identificada tardiamente com delirium hipoativo em estágio avançado. O preceptor usa o caso para discutir por que tantos episódios de delirium passam despercebidos. Segundo os dados epidemiológicos apresentados na disciplina, a taxa de não reconhecimento do delirium por profissionais de saúde pode chegar a até:",
    "options": [
      {
        "letter": "A",
        "text": "10%, principalmente nos casos hiperativos.",
        "rationale": "Incorreta. A taxa relatada em aula é muito superior a 10%, e o subtipo mais associado ao subdiagnóstico é justamente o oposto do hiperativo."
      },
      {
        "letter": "B",
        "text": "30%, igualmente distribuída entre os subtipos hiperativo e hipoativo.",
        "rationale": "Incorreta. A taxa relatada é maior do que 30%, e a distribuição não é igualitária entre os subtipos."
      },
      {
        "letter": "C",
        "text": "70%, principalmente nos casos hipoativos.",
        "rationale": "CORRETA. A aula destaca que a taxa de não reconhecimento do delirium por profissionais de saúde pode chegar a 70%, principalmente nos casos hipoativos — reforçando que o delirium não é raro, mas sim subdiagnosticado, sobretudo quando não há agitação psicomotora evidente."
      },
      {
        "letter": "D",
        "text": "90%, exclusivamente em unidades de terapia intensiva.",
        "rationale": "Incorreta. A cifra de 70% não é restrita à UTI, e a taxa citada em aula é de até 70%, não 90%."
      }
    ],
    "correctLetter": "C",
    "clinicalPointers": "A taxa de não reconhecimento do delirium por profissionais de saúde pode chegar a 70%, principalmente nos casos hipoativos — o delirium não é raro, é subdiagnosticado."
  },
  {
    "id": 14,
    "code": "DELIRIUM-03",
    "category": "Delirium",
    "subcategory": "Categorias etiológicas do DSM-5-TR",
    "difficulty": "Intermediária",
    "prompt": "Dona Célia, 74 anos, aposentada, está internada em Itabuna há 5 dias para tratamento de uma exacerbação de doença pulmonar obstrutiva crônica, em uso de corticosteroide em dose adequada e corretamente prescrita. No terceiro dia de internação, ela passa a apresentar desorientação temporal, atenção francamente flutuante durante a entrevista e relatos de ver \"formiguinhas andando na parede\", sem qualquer alteração aguda em outros exames. Segundo a classificação etiológica do DSM-5-TR para delirium, esse quadro deve ser categorizado como:",
    "options": [
      {
        "letter": "A",
        "text": "Delirium por intoxicação por substância.",
        "rationale": "Incorreta. Essa categoria refere-se a intoxicação por substâncias como álcool, cocaína, cannabis ou alucinógenos, não ao uso terapêutico e correto de um medicamento prescrito."
      },
      {
        "letter": "B",
        "text": "Delirium induzido por medicamento.",
        "rationale": "CORRETA. O DSM-5-TR reconhece explicitamente essa categoria para quadros decorrentes do uso apropriado de medicamentos como anticolinérgicos, corticosteroides ou opioides — ao avaliar um paciente delirante, deve-se presumir que qualquer fármaco em uso, mesmo corretamente prescrito, possa ser etiologicamente relevante."
      },
      {
        "letter": "C",
        "text": "Delirium por abstinência de substância.",
        "rationale": "Incorreta. Essa categoria refere-se a quadros desencadeados pela retirada de substâncias (ex.: álcool, benzodiazepínicos), não ao uso ativo de um medicamento."
      },
      {
        "letter": "D",
        "text": "Delirium devido a múltiplas etiologias, obrigatoriamente.",
        "rationale": "Incorreta. Não há, no enunciado, indicação de mais de uma causa concomitante identificada; a categoria mais específica e correta é a de delirium induzido por medicamento."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "As cinco categorias etiológicas do DSM-5-TR: intoxicação por substância, abstinência de substância, induzido por medicamento (inclusive uso apropriado/prescrito), devido a outra condição médica, e devido a múltiplas etiologias."
  },
  {
    "id": 15,
    "code": "DELIRIUM-04",
    "category": "Delirium",
    "subcategory": "Fatores predisponentes x precipitantes",
    "difficulty": "Intermediária",
    "prompt": "Seu Raimundo, 79 anos, com diagnóstico prévio de demência leve, é internado em Feira de Santana para tratamento de uma infecção respiratória. No segundo dia de internação, a equipe percebe que ele não conseguiu urinar nas últimas 10 horas e está com a bexiga distendida ao exame. Horas depois, ele desenvolve um quadro agudo de confusão mental e agitação. Nesse contexto, a retenção urinária não identificada precocemente deve ser classificada como:",
    "options": [
      {
        "letter": "A",
        "text": "Fator predisponente.",
        "rationale": "Incorreta. Fatores predisponentes refletem a vulnerabilidade basal do paciente (ex.: idade avançada, demência prévia), não o gatilho agudo do episódio atual."
      },
      {
        "letter": "B",
        "text": "Fator precipitante.",
        "rationale": "CORRETA. Fatores precipitantes são os gatilhos agudos que desencadeiam o episódio de delirium; em pacientes vulneráveis (idosos, dementados), pequenos fatores — como retenção urinária ou constipação — já podem desencadear o quadro, mesmo diante de agressões leves."
      },
      {
        "letter": "C",
        "text": "Critério de exclusão diagnóstica.",
        "rationale": "Incorreta. A retenção urinária não exclui o diagnóstico de delirium; pelo contrário, funciona como possível causa etiológica a ser corrigida."
      },
      {
        "letter": "D",
        "text": "Especificador de curso temporal (agudo ou persistente).",
        "rationale": "Incorreta. Os especificadores de curso temporal referem-se à duração do quadro (agudo: horas a dias; persistente: semanas a meses), não aos fatores de risco."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "O risco de delirium resulta da interação entre vulnerabilidade basal (fatores predisponentes) e a intensidade do insulto atual (fatores precipitantes); pacientes vulneráveis desenvolvem delirium mesmo com gatilhos discretos."
  },
  {
    "id": 16,
    "code": "DELIRIUM-05",
    "category": "Delirium",
    "subcategory": "Fisiopatologia: desequilíbrio de neurotransmissores",
    "difficulty": "Avançada",
    "prompt": "Em uma discussão de caso sobre delirium pós-operatório em um hospital de Salvador, um interno pergunta ao preceptor por que um paciente previamente lúcido pode, em poucas horas, apresentar um quadro tão exuberante de confusão mental, agitação e alucinações, e por que esse quadro costuma ser reversível assim que a causa de base é tratada. Em relação à fisiopatologia do delirium, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O delirium decorre de hiperatividade colinérgica generalizada associada a hipoatividade dopaminérgica.",
        "rationale": "Incorreta. A relação é inversa: há hipoatividade colinérgica associada a hiperatividade dopaminérgica."
      },
      {
        "letter": "B",
        "text": "O desequilíbrio central envolve hipoatividade das vias colinérgicas associada a hiperatividade das vias dopaminérgicas, com o sistema reticular ativador ascendente (SRAA) como estrutura central envolvida.",
        "rationale": "CORRETA. A acetilcolina é o neurotransmissor mais implicado, e o SRAA — que regula atenção e nível de consciência — é a estrutura mais envolvida; por reduzirem a atividade colinérgica, fármacos anticolinérgicos aumentam a vulnerabilidade ao delirium. Outros neurotransmissores envolvidos incluem dopamina, serotonina, glutamato e GABA."
      },
      {
        "letter": "C",
        "text": "A acetilcolina não tem qualquer papel reconhecido na fisiopatologia do delirium.",
        "rationale": "Incorreta. A acetilcolina é justamente o neurotransmissor mais implicado na fisiopatologia do delirium."
      },
      {
        "letter": "D",
        "text": "O delirium sempre decorre de dano estrutural irreversível no córtex pré-frontal.",
        "rationale": "Incorreta. O delirium é, na maioria dos casos, reversível: não há necessariamente dano estrutural, mas uma disfunção neuroquímica transitória, desde que a causa subjacente seja identificada e corrigida a tempo."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Fisiopatologia do delirium: hipoatividade colinérgica + hiperatividade dopaminérgica, com o sistema reticular ativador ascendente (SRAA) como estrutura central — geralmente reversível, pois reflete disfunção neuroquímica transitória, não dano estrutural."
  },
  {
    "id": 17,
    "code": "DELIRIUM-06",
    "category": "Delirium",
    "subcategory": "Critérios diagnósticos DSM-5-TR (A a E)",
    "difficulty": "Intermediária",
    "prompt": "Ao preparar um resumo sobre os critérios diagnósticos do delirium para a prova, a estudante Priscila lista os critérios A a E do DSM-5-TR e pede a um colega que confira se algum item da lista está incorreto antes de decorá-la. Qual das alternativas abaixo NÃO corresponde a um critério diagnóstico oficial do DSM-5-TR para delirium?",
    "options": [
      {
        "letter": "A",
        "text": "Perturbação da atenção e da consciência, desenvolvida em curto período e com tendência a flutuar em gravidade ao longo do dia.",
        "rationale": "Incorreta como resposta a esta pergunta (ou seja, ESTE item É um critério real): corresponde aos Critérios A e B do DSM-5-TR."
      },
      {
        "letter": "B",
        "text": "Perturbação adicional na cognição, como déficit de memória, desorientação, linguagem ou percepção.",
        "rationale": "Incorreta como resposta a esta pergunta (ESTE item É um critério real): corresponde ao Critério C do DSM-5-TR."
      },
      {
        "letter": "C",
        "text": "Confirmação obrigatória por exame de neuroimagem estrutural (tomografia ou ressonância magnética de crânio).",
        "rationale": "CORRETA (é a alternativa que NÃO corresponde a um critério real). O diagnóstico de delirium é clínico; exames complementares (incluindo neuroimagem) servem para identificar a causa de base, mas resultados negativos não excluem o diagnóstico, e a neuroimagem não é exigida como critério diagnóstico formal."
      },
      {
        "letter": "D",
        "text": "Evidências de que a perturbação é consequência fisiológica direta de outra condição médica, intoxicação, abstinência de substância, exposição a toxina, ou de múltiplas etiologias.",
        "rationale": "Incorreta como resposta a esta pergunta (ESTE item É um critério real): corresponde ao Critério E do DSM-5-TR."
      }
    ],
    "correctLetter": "C",
    "clinicalPointers": "Critérios A-E do DSM-5-TR para delirium: (A) atenção/consciência; (B) curso agudo e flutuante; (C) cognição adicional; (D) não explicado por outro transtorno neurocognitivo nem por coma; (E) evidência de causa fisiológica. O diagnóstico é clínico — não exige neuroimagem obrigatória."
  },
  {
    "id": 18,
    "code": "DELIRIUM-07",
    "category": "Delirium",
    "subcategory": "Especificadores de atividade psicomotora",
    "difficulty": "Intermediária",
    "prompt": "Na enfermaria de geriatria de um hospital de Ilhéus, a equipe de enfermagem descreve Dona Alzira, 78 anos, internada por pneumonia, apenas como \"mais quieta e sonolenta que o normal nos últimos dias\", dormindo bastante e respondendo de forma lenta e monossilábica, sem qualquer agitação. O médico plantonista é chamado para reavaliá-la. Em relação aos especificadores de atividade psicomotora do delirium (hiperativo, hipoativo e misto), assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O subtipo hiperativo é o mais subdiagnosticado, por ser frequentemente confundido com quadro funcional normal.",
        "rationale": "Incorreta. É o subtipo hipoativo, e não o hiperativo, que é mais frequentemente não reconhecido."
      },
      {
        "letter": "B",
        "text": "O subtipo hipoativo é mais comum em idosos e o mais frequentemente não reconhecido, sendo frequentemente confundido com depressão ou fadiga.",
        "rationale": "CORRETA. O subtipo hipoativo caracteriza-se por lentificação psicomotora e sonolência que se aproxima do estupor; por não apresentar agitação, é o principal responsável pelas altas taxas de subdiagnóstico do delirium."
      },
      {
        "letter": "C",
        "text": "O subtipo misto é definido pela ausência completa de qualquer sintoma psicomotor.",
        "rationale": "Incorreta. O subtipo misto caracteriza-se por atividade normal ou oscilação rápida entre os padrões hiperativo e hipoativo, não pela ausência completa de sintomas."
      },
      {
        "letter": "D",
        "text": "A agitação psicomotora é obrigatória para o diagnóstico de delirium, em qualquer subtipo.",
        "rationale": "Incorreta. A ausência de agitação NÃO exclui o diagnóstico de delirium — o subtipo hipoativo é justamente definido pela lentificação, não pela agitação."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "O subtipo hipoativo é mais comum em idosos e o principal responsável pelo subdiagnóstico do delirium, por ser confundido com depressão ou cansaço; a ausência de agitação não exclui o diagnóstico."
  },
  {
    "id": 19,
    "code": "DELIRIUM-08",
    "category": "Delirium",
    "subcategory": "Confusion Assessment Method (CAM)",
    "difficulty": "Intermediária",
    "prompt": "Ao aplicar o Confusion Assessment Method (CAM) em Sr. Osvaldo, internado em Juazeiro após cirurgia cardíaca, o médico confirma que o quadro surgiu ao longo de poucas horas e piorou à noite (início agudo e curso flutuante), além de notar que o paciente dispersa a atenção a cada poucos segundos (distúrbio da atenção). Antes de fechar o diagnóstico, ele revisa o algoritmo do CAM para saber quais outros achados, associados aos dois primeiros, confirmariam delirium. Quais são esses itens?",
    "options": [
      {
        "letter": "A",
        "text": "Alucinações visuais OU alterações do apetite.",
        "rationale": "Incorreta. Nenhum desses dois itens compõe o algoritmo central do CAM (1+2, associados a 3 e/ou 4)."
      },
      {
        "letter": "B",
        "text": "Pensamento desorganizado OU alteração do nível de consciência.",
        "rationale": "CORRETA. O algoritmo do CAM exige a presença simultânea de (1) início agudo e curso flutuante e (2) distúrbio da atenção, associados a pelo menos um dos itens: (3) pensamento desorganizado OU (4) alteração do nível de consciência. O CAM completo avalia nove domínios ao todo, mas esses quatro compõem o algoritmo diagnóstico central."
      },
      {
        "letter": "C",
        "text": "Agitação psicomotora OU alterações do ciclo sono-vigília.",
        "rationale": "Incorreta. Embora esses domínios façam parte da avaliação clínica ampla do delirium, não integram o algoritmo central de 4 itens do CAM."
      },
      {
        "letter": "D",
        "text": "Desorientação espacial OU ideação delirante persecutória.",
        "rationale": "Incorreta. Esses itens não compõem o algoritmo diagnóstico central do CAM."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Algoritmo do CAM: (1) início agudo e curso flutuante + (2) distúrbio da atenção, associados a (3) pensamento desorganizado OU (4) alteração do nível de consciência. Sensibilidade e especificidade superiores a 90% quando aplicado por examinador treinado."
  },
  {
    "id": 20,
    "code": "DELIRIUM-09",
    "category": "Delirium",
    "subcategory": "Diagnóstico diferencial: delirium x demência",
    "difficulty": "Avançada",
    "prompt": "Dona Iracema, 81 anos, é levada por familiares ao pronto-socorro de Vitória da Conquista com queixa de \"confusão mental\". Os filhos relatam que a mãe já esquecia nomes e repetia perguntas havia cerca de dois anos, de forma estável, mas que nas últimas 48 horas ela passou a não reconhecer o próprio quarto e a alternar entre momentos de lucidez e de completa desorientação, piorando bastante à noite. A médica plantonista precisa diferenciar se esse agravamento agudo representa um delirium sobreposto à demência prévia ou apenas a progressão natural da demência. Em relação ao diagnóstico diferencial entre essas duas condições — descrito como \"o problema diagnóstico diferencial mais comum\" na avaliação de confusão mental em idosos — assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "Na demência, a atenção costuma estar mantida e o curso é estável ao longo do dia; no delirium, a atenção é oscilante/flutuante e o curso piora frequentemente à noite.",
        "rationale": "CORRETA. Os principais eixos distintivos são o tempo de instalação (demência: lento e insidioso; delirium: rápido, horas a dias) e a flutuação da atenção (demência: geralmente mantida; delirium: oscilante). As duas condições podem coexistir (delirium sobreposto à demência, DSD), situação em que o manejo do delirium deve ser priorizado."
      },
      {
        "letter": "B",
        "text": "O delirium tem início lento e insidioso, enquanto a demência tem início rápido, em horas a dias.",
        "rationale": "Incorreta. A relação está invertida: o delirium tem início rápido (horas a dias), enquanto a demência tem início lento e insidioso."
      },
      {
        "letter": "C",
        "text": "Na demência, a memória imediata e recente costuma estar mais prejudicada do que a memória remota.",
        "rationale": "Incorreta. Na demência, a memória remota costuma ser mais prejudicada; no delirium, é a memória recente e imediata que está mais comprometida."
      },
      {
        "letter": "D",
        "text": "O delirium e a demência nunca coexistem no mesmo paciente.",
        "rationale": "Incorreta. As duas condições podem coexistir — o chamado delirium sobreposto à demência (DSD), com prevalência que varia de 1,4% a 70% — sendo o prejuízo cognitivo prévio um fator que pode mascarar o novo quadro agudo."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Delirium x demência: início (rápido x lento), duração (horas-semanas x meses-anos), atenção (oscilante x geralmente mantida), consciência (reduzida x inalterada), curso ao longo do dia (flutuante, pior à noite x estável). As duas podem coexistir (DSD)."
  },
  {
    "id": 21,
    "code": "DELIRIUM-10",
    "category": "Delirium",
    "subcategory": "Manejo farmacológico",
    "difficulty": "Intermediária",
    "prompt": "Wellington, 55 anos, motorista de caminhão, é hospitalizado em Camaçari por pancreatite aguda e, sem qualquer história de abstinência alcoólica ou de benzodiazepínicos, desenvolve delirium hiperativo com agitação intensa, tentando arrancar o acesso venoso, mesmo após a equipe já ter otimizado a iluminação, reorientado o paciente e controlado a dor. Diante da necessidade de tratamento farmacológico para conter o risco à sua segurança, qual classe de fármacos deve ser EVITADA nesse contexto, por risco de agravar a confusão mental?",
    "options": [
      {
        "letter": "A",
        "text": "Antipsicóticos de alta potência, em dose baixa, como o haloperidol.",
        "rationale": "Incorreta. O haloperidol em dose baixa é justamente a opção com maior respaldo de evidência para agitação/sintomas psicóticos no delirium, não devendo ser evitado nesse contexto."
      },
      {
        "letter": "B",
        "text": "Benzodiazepínicos, exceto no contexto específico de abstinência alcoólica ou de sedativo-hipnóticos.",
        "rationale": "CORRETA. Fora do contexto de abstinência, os benzodiazepínicos devem ser evitados no delirium, pois podem agravar a confusão mental; são, entretanto, indicados especificamente no delirium por abstinência alcoólica ou de benzodiazepínicos."
      },
      {
        "letter": "C",
        "text": "Antipsicóticos atípicos, como a risperidona, quetiapina ou olanzapina.",
        "rationale": "Incorreta. Esses fármacos são citados como alternativas ao haloperidol em caso de intolerância, com evidência mais limitada, mas não são a classe classicamente contraindicada."
      },
      {
        "letter": "D",
        "text": "Medidas não farmacológicas de reorientação temporo-espacial e correção de déficits sensoriais.",
        "rationale": "Incorreta. Essas medidas são recomendadas como primeira linha de manejo do delirium, e não devem ser evitadas."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Fora do contexto de abstinência alcoólica/sedativa, benzodiazepínicos devem ser evitados no delirium por poderem agravar a confusão mental; fenotiazinas de baixa potência também devem ser evitadas pelo risco anticolinérgico."
  },
  {
    "id": 22,
    "code": "DELIRIUM-11",
    "category": "Delirium",
    "subcategory": "Prevenção do delirium",
    "difficulty": "Intermediária",
    "prompt": "Após perceber um número alto de casos de delirium na enfermaria de clínica médica de um hospital de Salvador, a equipe multiprofissional decide implementar um protocolo estruturado de prevenção para todos os pacientes idosos internados, incluindo correção de déficits sensoriais, revisão de medicações de risco e estímulo à mobilização precoce. Em relação à prevenção do delirium em idosos hospitalizados, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "Não existe estratégia com boa evidência para reduzir a incidência de delirium em pacientes de risco.",
        "rationale": "Incorreta. Existem estratégias com boa evidência, descritas na alternativa correta."
      },
      {
        "letter": "B",
        "text": "Fármacos profiláticos, como antipsicóticos em baixa dose administrados rotineiramente, são a intervenção mais custo-efetiva para prevenção do delirium.",
        "rationale": "Incorreta. Não existe fármaco eficaz reconhecido para prevenir delirium; as estratégias não farmacológicas multicomponentes são a intervenção com melhor evidência."
      },
      {
        "letter": "C",
        "text": "Programas multicomponentes não farmacológicos (otimização sensorial, revisão de medicações, mobilização precoce e vigilância clínica regular) reduzem em cerca de um terço a incidência de delirium em idosos hospitalizados.",
        "rationale": "CORRETA. Programas como o Hospital Elder Life Program reduzem em cerca de um terço a incidência de delirium em idosos hospitalizados, sendo uma das intervenções mais custo-efetivas disponíveis na medicina hospitalar."
      },
      {
        "letter": "D",
        "text": "A prevenção do delirium deve focar exclusivamente na restrição ao leito, para evitar quedas.",
        "rationale": "Incorreta. A imobilização prolongada e a contenção física são, na verdade, fatores precipitantes de delirium; a mobilização precoce e segura é a conduta recomendada."
      }
    ],
    "correctLetter": "C",
    "clinicalPointers": "Programas multicomponentes de prevenção (otimização sensorial, revisão de medicações de alto risco, reabilitação/mobilidade, acompanhamento clínico regular) reduzem em cerca de um terço a incidência de delirium em idosos hospitalizados."
  },
  {
    "id": 23,
    "code": "ESQ-01",
    "category": "Esquizofrenia",
    "subcategory": "Espectro dos transtornos psicóticos: classificação temporal",
    "difficulty": "Intermediária",
    "prompt": "Anderson, 26 anos, vendedor, é avaliado em um ambulatório de Salvador. A família relata que, há cerca de 4 meses, ele começou a se isolar e a acreditar que colegas de trabalho estavam conspirando contra ele; nas últimas semanas, passou também a ouvir vozes comentando o que fazia. Ele nega uso de álcool ou drogas e não apresenta, em nenhum momento da história, sintomas de humor associados. Segundo a classificação temporal dos transtornos psicóticos primários, o diagnóstico mais provável é:",
    "options": [
      {
        "letter": "A",
        "text": "Transtorno psicótico breve.",
        "rationale": "Incorreta. O transtorno psicótico breve exige sintomas com duração inferior a 1 mês, com retorno completo ao funcionamento prévio."
      },
      {
        "letter": "B",
        "text": "Transtorno esquizofreniforme.",
        "rationale": "CORRETA. O transtorno esquizofreniforme apresenta os mesmos sintomas da fase ativa da esquizofrenia, com duração total entre 1 e 6 meses — exatamente o intervalo do caso descrito (4 meses)."
      },
      {
        "letter": "C",
        "text": "Esquizofrenia.",
        "rationale": "Incorreta. A esquizofrenia exige sintomas ativos por ≥1 mês e prejuízo funcional total por ≥6 meses (incluindo pródromo e fase residual) — o quadro descrito ainda não ultrapassou essa duração total."
      },
      {
        "letter": "D",
        "text": "Transtorno esquizoafetivo.",
        "rationale": "Incorreta. O transtorno esquizoafetivo exige episódio de humor concomitante à fase ativa da psicose — ausente neste caso."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Classificação temporal: <1 mês = transtorno psicótico breve; 1-6 meses = transtorno esquizofreniforme; >6 meses com prejuízo funcional amplo = esquizofrenia; presença de episódio de humor concomitante = transtorno esquizoafetivo."
  },
  {
    "id": 24,
    "code": "ESQ-02",
    "category": "Esquizofrenia",
    "subcategory": "Contexto histórico: Bleuler e os quatro As",
    "difficulty": "Intermediária",
    "prompt": "Estudando para a prova, Larissa revisa o histórico conceitual da esquizofrenia e anota que, em 1911, o psiquiatra suíço Eugen Bleuler cunhou o termo \"esquizofrenia\" para expressar a cisão entre pensamento, emoção e comportamento, sem exigir o curso deteriorante que Kraepelin havia descrito anteriormente para a dementia precox. Ao revisar seus resumos, ela tenta lembrar os chamados \"quatro As\" que Bleuler descreveu como sintomas fundamentais do transtorno. Quais são eles?",
    "options": [
      {
        "letter": "A",
        "text": "Alucinações, Apatia, Agitação e Ambivalência.",
        "rationale": "Incorreta. Alucinações e Agitação não fazem parte dos quatro As de Bleuler, que descreveu sintomas fundamentais sem exigir curso deteriorante."
      },
      {
        "letter": "B",
        "text": "Associação (frouxa), Afeto (alterado), Autismo e Ambivalência.",
        "rationale": "CORRETA. Bleuler cunhou o termo \"esquizofrenia\" e descreveu os sintomas fundamentais: Associação frouxa, Afeto alterado, Autismo e Ambivalência — sem exigir o curso deteriorante que Kraepelin havia descrito para a dementia precox."
      },
      {
        "letter": "C",
        "text": "Anedonia, Alogia, Avolição e Associabilidade.",
        "rationale": "Incorreta. Esses quatro termos, junto ao embotamento afetivo, compõem o modelo mais atual dos cinco domínios de sintomas negativos do NIMH, e não os quatro As históricos de Bleuler."
      },
      {
        "letter": "D",
        "text": "Amnésia, Afasia, Apraxia e Agnosia.",
        "rationale": "Incorreta. Esses são achados clássicos de síndromes demenciais (como a doença de Alzheimer), não os quatro As de Bleuler."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Contexto histórico: Kraepelin (1899) descreveu a dementia precox com curso deteriorante; Bleuler (1911) cunhou \"esquizofrenia\" e descreveu os quatro As (Associação, Afeto, Autismo, Ambivalência); Schneider descreveu sintomas de primeira ordem (não patognomônicos)."
  },
  {
    "id": 25,
    "code": "ESQ-03",
    "category": "Esquizofrenia",
    "subcategory": "Sintomas negativos: os cinco domínios do NIMH",
    "difficulty": "Intermediária",
    "prompt": "Ao reavaliar um paciente em fase residual de esquizofrenia acompanhado há anos em Itabuna, o médico nota que ele já não apresenta mais delírios ou alucinações, mas segue sem iniciativa para retomar o trabalho, os estudos ou até mesmo atividades simples do dia a dia, apesar de clinicamente estável há meses. Ele explica à família que esse domínio específico costuma ser o que mais compromete a funcionalidade a longo prazo. Segundo o modelo do National Institute of Mental Health (NIMH), qual dos cinco domínios de sintomas negativos da esquizofrenia é considerado o principal preditor de prejuízo funcional?",
    "options": [
      {
        "letter": "A",
        "text": "Alogia.",
        "rationale": "Incorreta. A alogia é a restrição na fluência e na produtividade do discurso, mas não é apontada como o principal preditor de prejuízo funcional."
      },
      {
        "letter": "B",
        "text": "Embotamento afetivo.",
        "rationale": "Incorreta. O embotamento afetivo é a redução da amplitude e intensidade da expressão emocional, mas não é o principal preditor de prejuízo funcional."
      },
      {
        "letter": "C",
        "text": "Avolição.",
        "rationale": "CORRETA. A avolição — redução da motivação e da persistência para iniciar comportamentos dirigidos a metas — é explicitamente descrita como o principal preditor de prejuízo funcional entre os cinco domínios de sintomas negativos do NIMH."
      },
      {
        "letter": "D",
        "text": "Anedonia.",
        "rationale": "Incorreta. A anedonia é a redução da capacidade de sentir prazer; embora relevante, não é apontada como o principal preditor de prejuízo funcional."
      }
    ],
    "correctLetter": "C",
    "clinicalPointers": "Os cinco domínios de sintomas negativos (NIMH): alogia, embotamento afetivo, associabilidade, avolição (principal preditor de prejuízo funcional) e anedonia — devem ser investigados preferencialmente com informações de familiares."
  },
  {
    "id": 26,
    "code": "ESQ-04",
    "category": "Esquizofrenia",
    "subcategory": "Critério A do DSM-5-TR",
    "difficulty": "Intermediária",
    "prompt": "Ao revisar os critérios diagnósticos do DSM-5-TR para esquizofrenia antes de uma prova, o estudante Thiago destaca que são necessários dois ou mais sintomas da fase ativa (Critério A), cada um presente por parte significativa de um período de um mês, mas fica em dúvida se qualquer combinação de dois sintomas da lista já seria suficiente para fechar o critério. Segundo o DSM-5-TR, pelo menos um dos sintomas presentes deve obrigatoriamente ser:",
    "options": [
      {
        "letter": "A",
        "text": "Sintomas negativos (expressão emocional diminuída ou avolição).",
        "rationale": "Incorreta. Os sintomas negativos, isoladamente, não satisfazem a exigência de que pelo menos um dos sintomas seja um dos três primeiros itens do Critério A."
      },
      {
        "letter": "B",
        "text": "Comportamento grosseiramente desorganizado ou catatônico.",
        "rationale": "Incorreta. Esse item corresponde ao quarto dos cinco sintomas do Critério A, mas não é, isoladamente, o exigido como obrigatório."
      },
      {
        "letter": "C",
        "text": "Delírios, alucinações ou discurso desorganizado.",
        "rationale": "CORRETA. O Critério A do DSM-5-TR lista cinco sintomas (delírios, alucinações, discurso desorganizado, comportamento grosseiramente desorganizado/catatônico e sintomas negativos), mas exige que pelo menos um dos dois (ou mais) sintomas presentes seja delírios, alucinações ou discurso desorganizado — os três primeiros itens da lista."
      },
      {
        "letter": "D",
        "text": "Qualquer um dos cinco sintomas, sem preferência entre eles.",
        "rationale": "Incorreta. Há, sim, uma exigência específica: ao menos um dos sintomas deve ser delírios, alucinações ou discurso desorganizado."
      }
    ],
    "correctLetter": "C",
    "clinicalPointers": "Critério A do DSM-5-TR: ≥2 sintomas da fase ativa (delírios, alucinações, discurso desorganizado, comportamento grosseiramente desorganizado/catatônico, sintomas negativos), sendo pelo menos um deles delírios, alucinações ou discurso desorganizado."
  },
  {
    "id": 27,
    "code": "ESQ-05",
    "category": "Esquizofrenia",
    "subcategory": "Pródromo e síndromes de ultra alto risco (UHR)",
    "difficulty": "Avançada",
    "prompt": "Durante o acompanhamento de um adolescente de 16 anos com sintomas positivos atenuados (desconfiança leve, percepções incomuns sem convicção delirante plena) em um serviço de Feira de Santana, os pais perguntam à equipe qual é, de fato, a chance real de que o quadro evolua para uma psicose franca nos próximos meses ou anos. Em relação às síndromes de ultra alto risco (UHR) para psicose, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "A taxa de conversão para psicose franca varia de cerca de 18% em 6 meses a 36% em 3 anos.",
        "rationale": "CORRETA. Esses são os valores de conversão para psicose apresentados em aula para as síndromes UHR, que incluem sintomas positivos atenuados, psicose breve intermitente, ou risco genético com declínio funcional."
      },
      {
        "letter": "B",
        "text": "Todo paciente com síndrome UHR converte inevitavelmente para esquizofrenia em até 1 ano.",
        "rationale": "Incorreta. A conversão não é inevitável; a taxa relatada é de 18% em 6 meses a 36% em 3 anos, o que significa que a maioria dos pacientes com síndrome UHR não converte para psicose franca nesse período."
      },
      {
        "letter": "C",
        "text": "As síndromes UHR não têm qualquer valor preditivo para psicose futura.",
        "rationale": "Incorreta. As síndromes UHR foram especificamente descritas por seu valor preditivo, com taxas de conversão relatadas de 18% a 36% conforme o intervalo de seguimento."
      },
      {
        "letter": "D",
        "text": "O pródromo é sempre assintomático, sem qualquer alteração comportamental perceptível.",
        "rationale": "Incorreta. O pródromo cursa com sintomas inespecíficos, como alterações de sono, irritabilidade, isolamento e desconfiança não estruturada."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Síndromes UHR: sintomas positivos atenuados, psicose breve intermitente ou risco genético com declínio funcional; taxa de conversão para psicose de 18% em 6 meses a 36% em 3 anos."
  },
  {
    "id": 28,
    "code": "ESQ-06",
    "category": "Esquizofrenia",
    "subcategory": "Síndromes delirantes classicamente nomeadas",
    "difficulty": "Intermediária",
    "prompt": "Wagner, 52 anos, técnico em eletrônica, é levado por familiares a uma consulta em Salvador porque, há cerca de duas semanas, afirma com convicção inabalável que a esposa com quem vive há 20 anos foi substituída por uma impostora fisicamente idêntica, chegando a evitar dormir no mesmo quarto que ela por desconfiança. Essa síndrome delirante é classicamente denominada:",
    "options": [
      {
        "letter": "A",
        "text": "Síndrome de Cotard.",
        "rationale": "Incorreta. A síndrome de Cotard corresponde à crença de estar morto, apodrecendo, ou de que órgãos internos deixaram de existir — não à crença de substituição por um impostor."
      },
      {
        "letter": "B",
        "text": "Síndrome de Capgras.",
        "rationale": "CORRETA. A síndrome de Capgras corresponde à crença de que familiares (ou, como no caso, o cônjuge) foram substituídos por impostores/sósias — uma das síndromes delirantes classicamente nomeadas, frequentes no transtorno delirante persistente, mas que também podem ocorrer na esquizofrenia."
      },
      {
        "letter": "C",
        "text": "Síndrome de Fregoli.",
        "rationale": "Incorreta. A síndrome de Fregoli corresponde à crença de que uma mesma pessoa se disfarça sob diferentes identidades para persegui-lo — um padrão diferente do descrito."
      },
      {
        "letter": "D",
        "text": "Síndrome de Ekbom.",
        "rationale": "Incorreta. A síndrome de Ekbom (delírio de parasitose) corresponde à convicção de infestação cutânea por parasitas, sem relação com o caso descrito."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Síndromes delirantes nomeadas: persecutório (perseguição); erotomaníaco/Clérambault (paixão secreta); Ekbom (parasitose); grandeza/megalomania; Capgras (impostores); Fregoli (mesma pessoa disfarçada); Cotard (estar morto); Otelo (ciúme/infidelidade)."
  },
  {
    "id": 29,
    "code": "ESQ-07",
    "category": "Esquizofrenia",
    "subcategory": "Subtipos clássicos: sinal do travesseiro psíquico",
    "difficulty": "Intermediária",
    "prompt": "Elias, 33 anos, é internado com suspeita de catatonia em um hospital de Ilhéus, apresentando mutismo e negativismo importantes. Ao examiná-lo, o médico residente retira o travesseiro sob a cabeça do paciente deitado, que permanece com a cabeça suspensa no ar, sem qualquer apoio, por longos períodos, sem sinal de desconforto. Esse achado semiológico clássico é conhecido como:",
    "options": [
      {
        "letter": "A",
        "text": "Sinal de Russell.",
        "rationale": "Incorreta. O sinal de Russell refere-se a ulcerações no dorso da mão associadas à indução mecânica de vômitos, um achado da bulimia nervosa, sem relação com a catatonia."
      },
      {
        "letter": "B",
        "text": "Sinal do travesseiro psíquico, expressão da flexibilidade cérea e da obediência automática.",
        "rationale": "CORRETA. Essa manobra semiológica clássica da catatonia demonstra a flexibilidade cérea (manutenção de posturas impostas) e a obediência automática — achados do especificador \"com catatonia\", hoje não mais considerado subtipo isolado, mas ainda cobrado em provas pelo valor descritivo."
      },
      {
        "letter": "C",
        "text": "Sinal de Chvostek.",
        "rationale": "Incorreta. O sinal de Chvostek é um achado de hipocalcemia (contração da musculatura facial à percussão do nervo facial), sem relação com a catatonia."
      },
      {
        "letter": "D",
        "text": "Sinal de Babinski invertido.",
        "rationale": "Incorreta. Não existe essa denominação para o achado descrito; o sinal de Babinski refere-se a um reflexo cutâneo-plantar patológico."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Sinal do travesseiro psíquico: manobra clássica da catatonia — expressão da flexibilidade cérea e da obediência automática. Subtipos clássicos (paranoide, desorganizado/hebefrênico, catatônico, indiferenciado, residual) foram retirados do DSM-5-TR e da CID-11, mas ainda cobrados por valor descritivo."
  },
  {
    "id": 30,
    "code": "ESQ-08",
    "category": "Esquizofrenia",
    "subcategory": "Fisiopatologia: modelo de saliência aberrante de Kapur",
    "difficulty": "Avançada",
    "prompt": "Durante um seminário sobre fisiopatologia da esquizofrenia em uma universidade de Salvador, a professora explica por que um paciente psicótico pode atribuir um significado ameaçador e persecutório a um gesto banal de um estranho na rua, enquanto ignora estímulos que deveriam ser mais relevantes no momento. Ela apresenta o modelo de saliência aberrante proposto por Kapur para explicar esse fenômeno. Segundo esse modelo, os sintomas positivos da esquizofrenia decorrem de:",
    "options": [
      {
        "letter": "A",
        "text": "Deficiência colinérgica generalizada no sistema reticular ativador ascendente.",
        "rationale": "Incorreta. Esse mecanismo é característico da fisiopatologia do delirium, não do modelo dopaminérgico da esquizofrenia proposto por Kapur."
      },
      {
        "letter": "B",
        "text": "Liberação dopaminérgica excessiva e fora de contexto, que atribui relevância a estímulos irrelevantes (gerando delírios/alucinações) e falha em atribuir saliência a estímulos relevantes.",
        "rationale": "CORRETA. O modelo de Kapur representa a evolução da hipótese dopaminérgica clássica: a hiperatividade dopaminérgica subcortical (via mesolímbica) associada à hipoatividade na via mesocortical (que projeta para o córtex pré-frontal) explica, respectivamente, os sintomas positivos e os sintomas negativos/cognitivos."
      },
      {
        "letter": "C",
        "text": "Excesso de atividade do receptor NMDA glutamatérgico.",
        "rationale": "Incorreta. A hipótese glutamatérgica propõe justamente o oposto: hipofunção (não excesso) do receptor NMDA, implicada tanto em sintomas positivos quanto negativos."
      },
      {
        "letter": "D",
        "text": "Hiperatividade exclusiva da via dopaminérgica mesocortical.",
        "rationale": "Incorreta. A via mesocortical está associada a hipoatividade (relacionada a sintomas negativos e cognitivos); é a via mesolímbica que apresenta hiperatividade, relacionada aos sintomas positivos."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Evolução da hipótese dopaminérgica: formulação clássica (excesso global) → 2ª formulação (hiperatividade mesolímbica/sintomas positivos + hipoatividade mesocortical/sintomas negativos-cognitivos) → modelo de Kapur (saliência aberrante)."
  },
  {
    "id": 31,
    "code": "ESQ-09",
    "category": "Esquizofrenia",
    "subcategory": "Esquizofrenia resistente ao tratamento e clozapina",
    "difficulty": "Avançada",
    "prompt": "Josenildo, 30 anos, é acompanhado em um serviço de Vitória da Conquista com diagnóstico de esquizofrenia. Já foram testados dois antipsicóticos distintos, cada um em dose adequada por mais de 6 semanas, com adesão documentada superior a 80% (incluindo um período com antipsicótico injetável de longa duração), mas ele mantém sintomas positivos e negativos moderados, com melhora inferior a 20% em escala padronizada (PANSS). Qual é a conduta farmacológica mais apropriada neste momento?",
    "options": [
      {
        "letter": "A",
        "text": "Associar dois antipsicóticos de segunda geração em altas doses.",
        "rationale": "Incorreta. Estratégias de associação de antipsicóticos têm evidência fraca e não são recomendadas rotineiramente neste cenário."
      },
      {
        "letter": "B",
        "text": "Iniciar clozapina, medicação de escolha na esquizofrenia resistente ao tratamento (ERT).",
        "rationale": "CORRETA. O quadro preenche os critérios de esquizofrenia resistente ao tratamento (falha de resposta a ≥2 antipsicóticos distintos, em doses e tempo adequados, com adesão documentada); a clozapina é a medicação de escolha nesse cenário, com eficácia superior, exigindo monitorização hematológica pelo risco de agranulocitose (~1%)."
      },
      {
        "letter": "C",
        "text": "Trocar por um terceiro antipsicótico não-clozapina, em monoterapia.",
        "rationale": "Incorreta. Não há evidência consistente de benefício em testar um terceiro antipsicótico não-clozapina após falha documentada de dois tratamentos adequados — essa conduta apenas posterga o tratamento eficaz."
      },
      {
        "letter": "D",
        "text": "Aumentar a dose do antipsicótico atual acima do limite máximo recomendado.",
        "rationale": "Incorreta. Doses acima do máximo recomendado aumentam o risco de efeitos adversos graves, sem ganho consistente de eficácia."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Critérios de ERT: falha de ≥2 antipsicóticos distintos, cada um por ≥6 semanas, em dose ≥600mg equivalentes de clorpromazina/dia, com adesão ≥80% e melhora <20% em escala padronizada. Clozapina é a medicação de escolha; tabagismo altera seus níveis séricos (indução CYP1A2)."
  },
  {
    "id": 32,
    "code": "ESQ-10",
    "category": "Esquizofrenia",
    "subcategory": "Fatores prognósticos",
    "difficulty": "Intermediária",
    "prompt": "Dois pacientes com esquizofrenia são comparados em uma discussão de caso em Feira de Santana: Renato, cujos sintomas surgiram de forma abrupta após a perda do emprego, aos 29 anos, com bom funcionamento prévio e forte apoio da família; e Cauã, cujos sintomas se instalaram de forma insidiosa desde a adolescência, sem qualquer fator desencadeante identificável e com histórico de isolamento social prévio. O residente é questionado sobre quais fatores tornam o prognóstico de Renato potencialmente mais favorável. Assinale a alternativa que reúne corretamente fatores de MELHOR prognóstico:",
    "options": [
      {
        "letter": "A",
        "text": "Início precoce, funcionamento pré-mórbido pobre e sintomas negativos predominantes.",
        "rationale": "Incorreta. Todos esses três fatores estão associados a prognóstico MENOS favorável, não melhor."
      },
      {
        "letter": "B",
        "text": "Início tardio, início agudo, fator precipitante identificável e bom suporte social e familiar.",
        "rationale": "CORRETA. Esses quatro fatores estão associados a prognóstico mais favorável, assim como sintomas de humor associados, sintomas positivos predominantes e remissão nos primeiros 3 anos."
      },
      {
        "letter": "C",
        "text": "Ausência de fator precipitante, início insidioso e múltiplas recaídas precoces.",
        "rationale": "Incorreta. Esses três fatores estão associados a prognóstico menos favorável, não melhor."
      },
      {
        "letter": "D",
        "text": "Sinais neurológicos associados e suporte social insatisfatório.",
        "rationale": "Incorreta. Ambos os fatores estão associados a prognóstico menos favorável."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Fatores de melhor prognóstico: início tardio, fator precipitante identificável, início agudo, bom funcionamento pré-mórbido, sintomas de humor associados, sintomas positivos predominantes, bom suporte social, remissão nos primeiros 3 anos."
  },
  {
    "id": 33,
    "code": "ESQ-11",
    "category": "Esquizofrenia",
    "subcategory": "Exclusão de organicidade (integração com Delirium)",
    "difficulty": "Avançada",
    "prompt": "Dona Rosália, 68 anos, é avaliada em um pronto-socorro de Salvador por alucinações visuais de início há 72 horas, associadas a desorientação temporal flutuante e períodos de rebaixamento do nível de consciência, cerca de 5 dias depois de tratar uma infecção urinária. Um interno sugere iniciar antipsicótico e investigar esquizofrenia de início tardio. Antes de considerar qualquer hipótese de transtorno psicótico primário, qual conduta é obrigatória, segundo o raciocínio de exclusão discutido na disciplina?",
    "options": [
      {
        "letter": "A",
        "text": "Firmar diagnóstico de esquizofrenia de início tardio e iniciar antipsicótico imediatamente.",
        "rationale": "Incorreta. A esquizofrenia de início tardio, apesar de clinicamente indistinguível da esquizofrenia clássica quanto ao quadro psicótico, não cursa com flutuação do nível de consciência — achado que aponta para outra hipótese."
      },
      {
        "letter": "B",
        "text": "Investigar ativamente causa orgânica subjacente (como delirium relacionado à infecção urinária), já que idade atípica de início, rebaixamento/flutuação do nível de consciência e curso agudo são sinais de alerta clássicos para organicidade.",
        "rationale": "CORRETA. Antes de firmar qualquer hipótese psiquiátrica primária, é obrigatório excluir causas orgânicas: idade atípica de início, rebaixamento ou flutuação do nível de consciência, deterioração cognitiva rápida e alterações neurológicas focais são sinais de alerta que, associados ao contexto de infecção recente, sugerem fortemente delirium — tema aprofundado na aula específica sobre o assunto."
      },
      {
        "letter": "C",
        "text": "Firmar diagnóstico de transtorno esquizoafetivo.",
        "rationale": "Incorreta. Não há relato de sintomas de humor, e o quadro de flutuação da consciência não é compatível com transtorno psicótico primário."
      },
      {
        "letter": "D",
        "text": "Iniciar clozapina diretamente, por se tratar de caso clinicamente grave.",
        "rationale": "Incorreta. A clozapina é reservada para esquizofrenia resistente ao tratamento, após falha de dois antipsicóticos — situação totalmente distinta da apresentada, na qual sequer o diagnóstico psiquiátrico primário foi estabelecido."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Sinais de alerta para organicidade em quadros psicóticos: idade atípica de início, rebaixamento/flutuação do nível de consciência, deterioração cognitiva rápida e sinais neurológicos focais exigem investigação clínica ativa antes de qualquer diagnóstico psiquiátrico primário — o mesmo raciocínio central da aula de Delirium."
  },
  {
    "id": 34,
    "code": "TEA-01",
    "category": "TEA",
    "subcategory": "Contexto histórico",
    "difficulty": "Intermediária",
    "prompt": "Estudando a história do conceito de TEA para a prova, o estudante Rodrigo se depara com três nomes que se confundem em seus resumos — Bleuler, Kanner e Asperger — e não tem certeza de quem descreveu o quê, nem em que ordem cronológica. Em relação ao histórico conceitual do Transtorno do Espectro Autista, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O termo \"autismo\" foi criado originalmente por Leo Kanner, em 1943, para descrever crianças com isolamento social intenso.",
        "rationale": "Incorreta. O termo \"autismo\" foi cunhado antes, no início do século XX, pelo psiquiatra suíço Eugen Bleuler, para descrever o retraimento da esquizofrenia — sem qualquer relação, na época, com o que hoje chamamos de TEA."
      },
      {
        "letter": "B",
        "text": "Eugen Bleuler cunhou originalmente o termo \"autismo\" para descrever o retraimento da esquizofrenia; anos depois, Leo Kanner (1943, Baltimore) e Hans Asperger (1944, Viena) descreveram, de forma independente, quadros hoje reconhecidos como TEA.",
        "rationale": "CORRETA. O termo foi reaproveitado e ressignificado ao longo de quase um século: Bleuler (início do século XX) descreveu o retraimento esquizofrênico; Kanner (1943) descreveu os \"distúrbios autísticos do contato afetivo\"; Asperger (1944), sem conhecer o trabalho de Kanner, descreveu crianças com padrão semelhante, mas com linguagem e cognição preservadas."
      },
      {
        "letter": "C",
        "text": "Hans Asperger e Leo Kanner publicaram, em coautoria, o primeiro estudo sobre autismo em 1943.",
        "rationale": "Incorreta. Os dois trabalhos foram publicados de forma independente, em locais e anos diferentes (Kanner em 1943, em Baltimore; Asperger em 1944, em Viena), sem que um conhecesse o trabalho do outro."
      },
      {
        "letter": "D",
        "text": "O DSM-5 manteve, em 2013, a separação entre transtorno autista, Asperger e transtorno desintegrativo da infância como categorias diagnósticas distintas.",
        "rationale": "Incorreta. O DSM-5 (2013) unificou essas categorias (transtorno autista, Asperger, transtorno desintegrativo da infância, síndrome de Rett e TGD-SOE) em um único espectro dimensional, com especificadores de gravidade."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Histórico: Bleuler cunhou \"autismo\" para a esquizofrenia; Kanner (1943) e Asperger (1944) descreveram, independentemente, quadros hoje reconhecidos como TEA; o DSM-5 (2013) unificou as antigas categorias em um espectro único."
  },
  {
    "id": 35,
    "code": "TEA-02",
    "category": "TEA",
    "subcategory": "Critério A do DSM-5: os três subdomínios",
    "difficulty": "Intermediária",
    "prompt": "Bernardo, 3 anos, é avaliado em um serviço de neurodesenvolvimento de Feira de Santana. A equipe observa que ele tem dificuldade em iniciar e responder a interações sociais, apresenta contato visual reduzido e pouco uso de gestos, além de não demonstrar interesse em brincar com outras crianças da mesma idade. Ao aplicar o Critério A do DSM-5 para TEA (déficits na comunicação e interação social), quantos dos três subdomínios listados devem estar presentes para o diagnóstico?",
    "options": [
      {
        "letter": "A",
        "text": "Apenas 1 dos 3 subdomínios, isoladamente.",
        "rationale": "Incorreta. O Critério A exige a presença dos três subdomínios, não apenas de um deles isoladamente."
      },
      {
        "letter": "B",
        "text": "Pelo menos 2 dos 3 subdomínios.",
        "rationale": "Incorreta. Diferentemente do Critério B (que exige ao menos 2 de 4 itens), o Critério A exige a presença dos TRÊS subdomínios, obrigatoriamente."
      },
      {
        "letter": "C",
        "text": "Os 3 subdomínios, obrigatoriamente: reciprocidade socioemocional, comportamentos comunicativos não verbais, e desenvolvimento/manutenção/compreensão de relacionamentos.",
        "rationale": "CORRETA. O Critério A do DSM-5 exige a presença dos três subdomínios: A1 (reciprocidade socioemocional), A2 (comunicação não verbal) e A3 (desenvolver, manter e compreender relacionamentos) — diferentemente do Critério B, que exige apenas 2 de 4 itens."
      },
      {
        "letter": "D",
        "text": "Nenhum subdomínio específico é exigido, bastando prejuízo funcional global inespecífico.",
        "rationale": "Incorreta. O DSM-5 especifica claramente os três subdomínios do Critério A, todos obrigatórios."
      }
    ],
    "correctLetter": "C",
    "clinicalPointers": "Critério A do DSM-5 (obrigatórios os 3 subdomínios): A1 reciprocidade socioemocional, A2 comunicação não verbal, A3 desenvolver/manter/compreender relacionamentos. Critério B (mínimo 2 de 4 itens): estereotipias, mesmice/rotinas, interesses restritos, alterações sensoriais."
  },
  {
    "id": 36,
    "code": "TEA-03",
    "category": "TEA",
    "subcategory": "Especificadores de gravidade: níveis de suporte",
    "difficulty": "Avançada",
    "prompt": "Os pais de Heitor, 6 anos, recém-diagnosticado com TEA em Salvador, leem no laudo que ele foi classificado como \"nível 2 de suporte\" e perguntam ao médico se isso significa que o quadro é \"moderado\" e vai permanecer exatamente assim para sempre, inclusive na escola e em casa. Em relação aos especificadores de gravidade do TEA (níveis de suporte 1 a 3), assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "Os níveis de suporte equivalem diretamente à classificação \"leve/moderado/grave\", podendo ser usados como sinônimos na prática clínica.",
        "rationale": "Incorreta. Essa é descrita explicitamente como uma tradução popular que simplifica demais e pode induzir erro conceitual — a nomenclatura oficial é sempre \"requer suporte / suporte substancial / suporte muito substancial\"."
      },
      {
        "letter": "B",
        "text": "O nível de suporte é avaliado separadamente para os dois domínios do TEA (comunicação social e comportamentos restritos/repetitivos), podendo variar entre esses domínios, entre ambientes (casa x escola) e ao longo do tempo.",
        "rationale": "CORRETA. \"Nível 1, 2 ou 3\" não é uma nota de gravidade global, mas sim uma descrição de quanto suporte a pessoa precisa em cada domínio separadamente; não é um rótulo fixo e vitalício, podendo variar entre domínios, ambientes e ao longo do tempo."
      },
      {
        "letter": "C",
        "text": "O nível de suporte é um rótulo fixo e vitalício, definido uma única vez, no momento do diagnóstico.",
        "rationale": "Incorreta. O nível de suporte pode variar entre os dois domínios, entre ambientes e ao longo do tempo, não sendo um rótulo fixo e vitalício."
      },
      {
        "letter": "D",
        "text": "O funcionamento adaptativo e a presença de deficiência intelectual associada não influenciam o prognóstico além do nível de suporte.",
        "rationale": "Incorreta. Funcionamento adaptativo, presença de linguagem funcional e de deficiência intelectual associada são avaliados separadamente e influenciam o prognóstico tanto quanto — ou mais do que — o nível de suporte isolado."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Os níveis de suporte (1: requer suporte; 2: requer suporte substancial; 3: requer suporte muito substancial) são avaliados separadamente para comunicação social e comportamentos restritos/repetitivos, e podem variar entre domínios, ambientes e ao longo do tempo — não equivalem a \"leve/moderado/grave\"."
  },
  {
    "id": 37,
    "code": "TEA-04",
    "category": "TEA",
    "subcategory": "Investigação genética recomendada",
    "difficulty": "Intermediária",
    "prompt": "Após a confirmação diagnóstica de TEA em Valentina, 3 anos, atendida em Itabuna, sem dismorfismos evidentes ao exame físico, perímetro cefálico normal e desenvolvimento motor grosseiro adequado para a idade, os pais perguntam se algum exame complementar é necessário, já que \"ela parece perfeitamente normal fisicamente\". Qual investigação é recomendada, independentemente da presença de fenótipo sindrômico evidente?",
    "options": [
      {
        "letter": "A",
        "text": "Ressonância magnética de crânio, como exame de rotina obrigatório para todo paciente com TEA.",
        "rationale": "Incorreta. A neuroimagem estrutural não é exame de rotina recomendado para todo paciente com TEA, na ausência de indicação clínica específica (sinais neurológicos focais, macrocefalia importante, entre outros)."
      },
      {
        "letter": "B",
        "text": "Investigação genética (teste para síndrome do X frágil e exame cromossômico por microarray/CGH array).",
        "rationale": "CORRETA. Essa investigação é recomendada para todo paciente com diagnóstico de TEA, independentemente da presença de dismorfismos, dado que causas monogênicas identificáveis (X frágil em 2-3% dos casos e esclerose tuberosa em até 2%) podem estar presentes mesmo sem fenótipo sindrômico evidente; até 15% dos casos de TEA associam-se a mutações genéticas conhecidas."
      },
      {
        "letter": "C",
        "text": "Eletroencefalograma de rotina, mesmo na ausência de suspeita clínica de epilepsia.",
        "rationale": "Incorreta. Embora a frequência de convulsões e alterações eletrencefalográficas esteja aumentada no TEA, o EEG de rotina não é a investigação complementar sistematicamente recomendada para todo paciente ao diagnóstico."
      },
      {
        "letter": "D",
        "text": "Nenhuma investigação complementar é recomendada, pois o TEA nunca tem causa genética identificável.",
        "rationale": "Incorreta. A herdabilidade do TEA é elevada (~74%), com síndromes monogênicas identificáveis em parcela relevante dos casos, justificando a investigação genética sistemática."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Investigação genética (X frágil + CGH array) deve ser oferecida a todo paciente com diagnóstico de TEA, independentemente de dismorfismos — X frágil em 2-3% e esclerose tuberosa em até 2% dos casos são as causas monogênicas mais comumente identificadas."
  },
  {
    "id": 38,
    "code": "TEA-05",
    "category": "TEA",
    "subcategory": "Diagnóstico diferencial: transtorno da comunicação social",
    "difficulty": "Avançada",
    "prompt": "Kauã, 14 anos, é encaminhado a um ambulatório de Vitória da Conquista pela escola, que relata dificuldade dele em compreender ironias, manter o turno em conversas e ajustar a linguagem ao contexto social, o que gera constrangimentos frequentes entre os colegas. Segundo os pais e os registros escolares, revisados cuidadosamente pela equipe, ele nunca apresentou, em qualquer momento do desenvolvimento, movimentos repetitivos, interesses restritos incomuns, insistência em rotinas ou alterações de reatividade sensorial. Qual é o diagnóstico mais adequado?",
    "options": [
      {
        "letter": "A",
        "text": "Transtorno do Espectro Autista, nível 1 (requer suporte).",
        "rationale": "Incorreta. O diagnóstico de TEA, em qualquer nível de gravidade, exige a presença de comportamentos restritos e repetitivos (Critério B) em algum momento do desenvolvimento — explicitamente ausentes neste caso."
      },
      {
        "letter": "B",
        "text": "Transtorno da comunicação social (pragmática).",
        "rationale": "CORRETA. Esse transtorno é diagnóstico de exclusão em relação ao TEA: só pode ser firmado quando não há, nem atual nem pregressamente, qualquer padrão restrito e repetitivo de comportamento — exatamente a situação descrita, que envolve exclusivamente dificuldade no uso pragmático da linguagem para interação social."
      },
      {
        "letter": "C",
        "text": "Transtorno de Déficit de Atenção/Hiperatividade, apresentação predominantemente desatenta.",
        "rationale": "Incorreta. O TDAH desatento não explica o padrão específico de dificuldade pragmática (compreensão de ironias, turnos de conversa, ajuste ao contexto social) descrito no caso."
      },
      {
        "letter": "D",
        "text": "Transtorno da personalidade esquiva.",
        "rationale": "Incorreta. O transtorno da personalidade esquiva centra-se em inibição social por medo de rejeição e sentimento de inadequação, não em déficit pragmático primário da comunicação."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "O transtorno da comunicação social (pragmática) é diagnóstico de exclusão em relação ao TEA: só é firmado na ausência completa, atual e pregressa, de qualquer padrão restrito e repetitivo de comportamento (Critério B)."
  },
  {
    "id": 39,
    "code": "TEA-06",
    "category": "TEA",
    "subcategory": "Diagnóstico diferencial: TEA x Síndrome de Rett",
    "difficulty": "Avançada",
    "prompt": "Isis, hoje com 3 anos, é levada a um ambulatório de Salvador porque, segundo a mãe, \"ela estava se desenvolvendo normalmente até os 18 meses\" — falava algumas palavras e usava as mãos para brincar —, quando começou a perder progressivamente essas habilidades, associada a uma desaceleração perceptível do crescimento da cabeça. Esse padrão de regressão contínua, associado à desaceleração do perímetro cefálico, é mais sugestivo de:",
    "options": [
      {
        "letter": "A",
        "text": "Transtorno do Espectro Autista típico, sem necessidade de investigação adicional.",
        "rationale": "Incorreta. No TEA, quando há regressão (minoria dos casos, presente em até 25%), ela costuma ser mais discreta e não progressiva, podendo inclusive haver recuperação parcial com intervenção — padrão diferente do descrito."
      },
      {
        "letter": "B",
        "text": "Síndrome de Rett.",
        "rationale": "CORRETA. A síndrome de Rett é praticamente exclusiva do sexo feminino; o desenvolvimento é tipicamente normal até os 6 meses–4 anos, quando ocorre desaceleração do crescimento do perímetro cefálico e perda evidente e progressiva de habilidades manuais e de linguagem — um padrão de regressão CONTÍNUA, e não de estabilização, como classicamente descrito para o TEA."
      },
      {
        "letter": "C",
        "text": "Transtorno da comunicação social (pragmática).",
        "rationale": "Incorreta. Esse transtorno não cursa com regressão de habilidades previamente adquiridas nem com desaceleração do perímetro cefálico."
      },
      {
        "letter": "D",
        "text": "Desenvolvimento normal, dentro da variação individual esperada.",
        "rationale": "Incorreta. A perda progressiva de habilidades associada à desaceleração do perímetro cefálico deve sempre levantar suspeita diagnóstica, não sendo interpretada como variação normal."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "TEA x Síndrome de Rett: na Rett (quase exclusiva do sexo feminino), há regressão CONTÍNUA de habilidades associada a desaceleração do perímetro cefálico; no TEA, o prejuízo já está presente desde o início e, quando há regressão, costuma ser mais discreta e não progressiva."
  },
  {
    "id": 40,
    "code": "TEA-07",
    "category": "TEA",
    "subcategory": "Comorbidades",
    "difficulty": "Intermediária",
    "prompt": "Durante a consulta de retorno de Davi, 8 anos, com TEA, acompanhado em Feira de Santana, a mãe relata que, além das dificuldades sociais já conhecidas, ele tem se mostrado extremamente desatento e agitado em sala de aula, e pergunta se é possível ele também ter TDAH junto com o TEA, ou se um diagnóstico exclui o outro. Em relação às comorbidades do Transtorno do Espectro Autista, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O TDAH é uma das comorbidades mais frequentemente associadas ao TEA, com tratamento da hiperatividade seguindo princípios semelhantes aos da população geral.",
        "rationale": "CORRETA. O TDAH é descrita como uma das comorbidades mais frequentes no TEA; o tratamento da hiperatividade nesses pacientes segue princípios semelhantes aos utilizados na população geral."
      },
      {
        "letter": "B",
        "text": "A deficiência intelectual está presente em praticamente 100% dos casos de TEA.",
        "rationale": "Incorreta. A deficiência intelectual está presente em cerca de um terço (não na totalidade) dos casos que preenchem critérios de TEA pelo DSM-5."
      },
      {
        "letter": "C",
        "text": "Transtornos de ansiedade são raros em indivíduos com TEA.",
        "rationale": "Incorreta. Transtornos de ansiedade são descritos como extremamente comuns no TEA, podendo se manifestar de forma atípica, o que dificulta o reconhecimento clínico."
      },
      {
        "letter": "D",
        "text": "A frequência de convulsões e de alterações eletrencefalográficas no TEA é inferior à da população geral.",
        "rationale": "Incorreta. A frequência de convulsões e anormalidades de EEG está acima da população geral em indivíduos com TEA."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Comorbidades do TEA: TDAH (uma das mais frequentes), deficiência intelectual (~1/3 dos casos), transtornos de ansiedade (extremamente comuns), transtornos do humor (mais frequentes em adolescentes/adultos), epilepsia/EEG alterado, síndromes genéticas específicas."
  },
  {
    "id": 41,
    "code": "TEA-08",
    "category": "TEA",
    "subcategory": "Tratamento farmacológico: irritabilidade/agressividade",
    "difficulty": "Avançada",
    "prompt": "Matheus, 7 anos, com TEA, está em intervenção comportamental estruturada mantida de forma consistente há mais de um ano em Ilhéus, com bons ganhos em comunicação funcional. Recentemente, porém, os pais relatam piora progressiva de episódios de agressividade heterodirigida diante de frustrações, com risco de lesão a colegas na escola, mesmo com o programa comportamental já otimizado. Qual conduta farmacológica tem maior respaldo de evidência para esse sintoma-alvo específico?",
    "options": [
      {
        "letter": "A",
        "text": "Iniciar ISRS em dose plena, pela evidência robusta de benefício sobre comportamentos repetitivos e agressividade no TEA.",
        "rationale": "Incorreta. Ensaios randomizados controlados com ISRSs falharam em demonstrar benefício consistente para comportamentos repetitivos no TEA."
      },
      {
        "letter": "B",
        "text": "Considerar antipsicótico (risperidona ou aripiprazol), com discussão explícita dos efeitos colaterais metabólicos e de sedação com a família, mantendo a intervenção comportamental.",
        "rationale": "CORRETA. Antipsicóticos, particularmente risperidona e aripiprazol, têm benefício demonstrado em ensaios randomizados controlados especificamente para irritabilidade/agressividade no TEA — devendo ser usados com cautela pelo perfil de efeitos colaterais (sedação, ganho de peso, alterações metabólicas), e sempre associados à intervenção comportamental contínua, nunca como tratamento dos sintomas nucleares do transtorno."
      },
      {
        "letter": "C",
        "text": "Iniciar ocitocina intranasal em uso repetido, pela evidência consistente de benefício em estudos de dose única.",
        "rationale": "Incorreta. Estudos com ocitocina intranasal não confirmaram, em uso repetido, os benefícios sugeridos por estudos iniciais de dose única."
      },
      {
        "letter": "D",
        "text": "Não há qualquer indicação de tratamento farmacológico no TEA, em nenhuma circunstância.",
        "rationale": "Incorreta. Embora a farmacoterapia no TEA seja secundária e dirigida a sintomas-alvo (não ao núcleo do transtorno), ela é indicada para sintomas-alvo específicos, como irritabilidade/agressividade significativa, quando a intervenção psicossocial isoladamente é insuficiente."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "A farmacoterapia no TEA é dirigida a sintomas-alvo de condições coocorrentes, não ao núcleo do transtorno. Risperidona e aripiprazol têm a evidência mais consistente especificamente para irritabilidade/agressividade, sempre associados à intervenção comportamental."
  },
  {
    "id": 42,
    "code": "TEA-09",
    "category": "TEA",
    "subcategory": "Sinais de alerta precoces (12-24 meses)",
    "difficulty": "Intermediária",
    "prompt": "Na consulta de puericultura de Théo, 14 meses, em uma UBS de Camaçari, a pediatra nota que ele não busca compartilhar interesse com os pais, nunca estendendo o dedo para mostrar algo que lhe chama atenção, embora já ande sozinho e coma bem. Qual dos achados abaixo é considerado um sinal de alerta relevante para encaminhamento oportuno na investigação de TEA?",
    "options": [
      {
        "letter": "A",
        "text": "Ausência de apontar para compartilhar interesse (\"apontar protodeclarativo\").",
        "rationale": "CORRETA. A ausência do apontar protodeclarativo é explicitamente citada como sinal de alerta relacionado a contato e atenção compartilhada, junto ao contato visual reduzido, sendo relevante para o encaminhamento oportuno na puericultura."
      },
      {
        "letter": "B",
        "text": "Uso excessivo de gestos e expressividade facial marcadamente aumentada.",
        "rationale": "Incorreta. Os sinais de alerta descritos vão na direção oposta: comunicação não verbal reduzida, não aumentada."
      },
      {
        "letter": "C",
        "text": "Interesse intenso e recorrente por brincadeiras compartilhadas com outras crianças.",
        "rationale": "Incorreta. O padrão de alerta é o desinteresse por brincadeiras compartilhadas, e não o interesse intenso por elas."
      },
      {
        "letter": "D",
        "text": "Aumento expressivo do vocabulário verbal já aos 12 meses de idade.",
        "rationale": "Incorreta. Os sinais de alerta relacionados à linguagem são justamente a ausência de balbucio aos 12 meses e a ausência de palavras aos 16 meses — atraso, não avanço, no desenvolvimento da linguagem."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Sinais de alerta (12-24 meses): não responder ao nome, ausência de balbucio/palavras nos marcos esperados, ausência de sorriso social, contato visual reduzido, ausência de apontar protodeclarativo, estereotipias motoras, alinhar objetos, e regressão de habilidades (até 25% dos casos)."
  },
  {
    "id": 43,
    "code": "TEA-10",
    "category": "TEA",
    "subcategory": "Curso e prognóstico",
    "difficulty": "Intermediária",
    "prompt": "Em um serviço de referência de Salvador, comparam-se dois casos de TEA com comprometimento intelectual associado: Enzo, diagnosticado aos 2 anos e meio, com intervenção multidisciplinar iniciada imediatamente após o diagnóstico; e Miguel, diagnosticado apenas aos 9 anos, sem qualquer intervenção especializada antes disso. Com base na evidência disponível sobre curso e prognóstico do TEA, qual afirmação está correta em relação aos desfechos esperados na vida adulta desses dois pacientes?",
    "options": [
      {
        "letter": "A",
        "text": "A idade de início da intervenção não influencia os desfechos funcionais na vida adulta.",
        "rationale": "Incorreta. Diagnóstico e intervenção precoces estão associados a desfechos mais favoráveis, contrariando essa afirmação."
      },
      {
        "letter": "B",
        "text": "Diagnóstico e intervenção precoces (2-3 anos) associam-se a desfechos mais favoráveis na vida adulta, mesmo em indivíduos com comprometimento intelectual associado.",
        "rationale": "CORRETA. Estudos longitudinais mostram que diagnóstico e intervenção iniciados aos 2-3 anos associam-se a desfechos mais positivos na vida adulta, inclusive em indivíduos com comprometimento intelectual — reforçando a importância do diagnóstico e da intervenção precoces independentemente do perfil cognitivo."
      },
      {
        "letter": "C",
        "text": "A intervenção precoce só traz benefício em indivíduos com TEA sem comprometimento intelectual associado.",
        "rationale": "Incorreta. O benefício da intervenção e do diagnóstico precoces foi documentado inclusive em indivíduos com comprometimento intelectual, não se restringindo a pacientes sem esse comprometimento."
      },
      {
        "letter": "D",
        "text": "O funcionamento adaptativo tende a piorar progressivamente ao longo do desenvolvimento, independentemente de qualquer intervenção.",
        "rationale": "Incorreta. Na maior parte dos indivíduos, o funcionamento adaptativo tende a apresentar melhora progressiva, ainda que os sintomas nucleares tendam a se manter relativamente estáveis a partir dos 2 anos até a adolescência."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Diagnóstico e intervenção precoces (2-3 anos) são o fator prognóstico mais consistentemente associado a melhores desfechos funcionais no TEA ao longo da vida, mesmo em pacientes com comprometimento intelectual associado."
  },
  {
    "id": 44,
    "code": "TEA-11",
    "category": "TEA",
    "subcategory": "Comorbidade TEA-TDAH (integração com a aula de TDAH)",
    "difficulty": "Avançada",
    "prompt": "Gael, 5 anos, é atendido em um ambulatório de Feira de Santana. Desde os 2 anos, apresenta prejuízo importante na reciprocidade socioemocional, contato visual reduzido, ausência de apontar protodeclarativo e estereotipias motoras (\"flapping\") quando animado. Além disso, tanto os pais quanto a professora relatam desatenção marcante e inquietude motora significativa, presentes tanto em casa quanto na escola, levantando a suspeita de mais de um diagnóstico associado. Considerando a sobreposição entre TEA e TDAH discutida ao longo da disciplina, qual é a conduta mais apropriada?",
    "options": [
      {
        "letter": "A",
        "text": "Diagnosticar apenas TDAH, já que a presença de desatenção exclui, por definição, o diagnóstico de TEA.",
        "rationale": "Incorreta. A presença de sintomas de desatenção não exclui o diagnóstico de TEA — pelo contrário, o TDAH é reconhecido como uma das comorbidades mais frequentes do TEA."
      },
      {
        "letter": "B",
        "text": "Reconhecer que o TDAH é uma das comorbidades mais frequentes do TEA, investigando e tratando ambas as condições, já que a presença de um transtorno não exclui o outro.",
        "rationale": "CORRETA. Tanto a aula de TEA (que lista o TDAH entre as comorbidades mais frequentes) quanto a aula de TDAH (que descreve que TEA e TDAH coexistem com frequência, sem que isso os torne sinônimos) convergem para essa conclusão: diante de um quadro com déficits sociais centrais característicos de TEA associados a sintomas de desatenção/hiperatividade em múltiplos contextos, ambos os diagnósticos devem ser considerados e tratados."
      },
      {
        "letter": "C",
        "text": "Diagnosticar apenas TEA, pois a coexistência com TDAH é formalmente impossível segundo o DSM-5.",
        "rationale": "Incorreta. O DSM-5 reconhece explicitamente que os dois diagnósticos podem coexistir; historicamente essa coexistência era vedada apenas no DSM-IV, não no DSM-5."
      },
      {
        "letter": "D",
        "text": "Aguardar a resolução espontânea dos sintomas de desatenção antes de qualquer avaliação adicional.",
        "rationale": "Incorreta. A investigação ativa e oportuna de comorbidades é recomendada, não a postergação da avaliação."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "TDAH é uma das comorbidades mais frequentes do TEA; didaticamente, o TEA cursa com prejuízo central na comunicação social e comportamentos restritos/repetitivos (ausentes no TDAH isolado), mas os dois quadros coexistem com frequência, o que não os torna sinônimos."
  },
  {
    "id": 45,
    "code": "TDAH-01",
    "category": "TDAH",
    "subcategory": "Conceito: extremo de um espectro dimensional",
    "difficulty": "Intermediária",
    "prompt": "Ao explicar o diagnóstico de TDAH para os pais de um paciente em Salvador, o médico é interrompido pelo avô da criança, que insiste: \"Isso é falta de educação, no meu tempo resolvia-se de outro jeito.\" Em relação ao conceito atual do TDAH, apresentado na disciplina, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O TDAH é considerado uma falha de caráter, disciplina ou educação, sem base biológica reconhecida.",
        "rationale": "Incorreta. O TDAH é atualmente entendido como a expressão fenotípica de alterações em processos normais do desenvolvimento cerebral, e não como uma falha de caráter, disciplina ou educação."
      },
      {
        "letter": "B",
        "text": "O TDAH é entendido como a expressão fenotípica de alterações em processos normais do desenvolvimento cerebral, representando o extremo de um espectro dimensional presente, em menor grau, também na população geral.",
        "rationale": "CORRETA. Essa é exatamente a definição apresentada na disciplina; para configurar diagnóstico formal, os sintomas precisam causar prejuízo social, familiar ou acadêmico/ocupacional claro — sintomas isolados, sem prejuízo funcional, não bastam."
      },
      {
        "letter": "C",
        "text": "O diagnóstico de TDAH depende obrigatoriamente de exame de neuroimagem, SPECT, PET ou EEG confirmatório.",
        "rationale": "Incorreta. O diagnóstico é inteiramente clínico; esses exames complementares não têm papel definido no diagnóstico de rotina, sendo reservados para pesquisa ou suspeita de diagnóstico neurológico diferencial."
      },
      {
        "letter": "D",
        "text": "Sintomas isolados de desatenção ou hiperatividade, mesmo sem qualquer prejuízo funcional, já são suficientes para o diagnóstico.",
        "rationale": "Incorreta. O Critério D do DSM-5 exige evidências claras de prejuízo funcional; sintomas isolados, sem esse prejuízo, não bastam para o diagnóstico."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "TDAH: expressão fenotípica de alterações em processos normais do desenvolvimento cerebral; extremo de um espectro dimensional; diagnóstico clínico, exigindo prejuízo funcional claro (não apenas presença de sintomas)."
  },
  {
    "id": 46,
    "code": "TDAH-02",
    "category": "TDAH",
    "subcategory": "Critério A: limiar dentro de um mesmo domínio",
    "difficulty": "Avançada",
    "prompt": "Rian, 10 anos, é avaliado em Vitória da Conquista. Segundo os pais e a professora, ele apresenta 4 sintomas de desatenção (esquece materiais, distrai-se facilmente, não termina tarefas e comete erros por descuido) e mais 4 sintomas de hiperatividade/impulsividade (remexe-se na cadeira, fala em excesso, interrompe os colegas e tem dificuldade de esperar a vez), totalizando 8 sintomas ao todo, presentes desde os 7 anos, em casa e na escola, com prejuízo funcional evidente. Em relação ao Critério A do DSM-5 para TDAH, é correto afirmar que:",
    "options": [
      {
        "letter": "A",
        "text": "O critério está preenchido, pois a soma de 8 sintomas ultrapassa amplamente o limiar mínimo exigido.",
        "rationale": "Incorreta. Os domínios não são somados; a soma de sintomas de domínios diferentes não substitui a exigência de atingir o limiar dentro de um único domínio."
      },
      {
        "letter": "B",
        "text": "O critério NÃO está preenchido, pois o limiar de 6 sintomas (5 a partir dos 17 anos) deve ser atingido dentro de um mesmo domínio — desatenção OU hiperatividade/impulsividade —, e não pela soma dos dois domínios.",
        "rationale": "CORRETA. Esse é um erro conceitual clássico: 4 sintomas de desatenção mais 4 de hiperatividade/impulsividade totalizam 8, mas os domínios não são somados — é necessário atingir 6 (ou 5, a partir dos 17 anos) dentro de um mesmo domínio para preencher o Critério A."
      },
      {
        "letter": "C",
        "text": "O critério está preenchido apenas se os sintomas ocorrerem em um único ambiente.",
        "rationale": "Incorreta. Pelo contrário, o Critério C exige que os sintomas ocorram em pelo menos 2 contextos diferentes, e não em um único ambiente."
      },
      {
        "letter": "D",
        "text": "Não é necessário atingir nenhum limiar mínimo de sintomas, bastando a presença de prejuízo funcional isolado.",
        "rationale": "Incorreta. O Critério A exige explicitamente um número mínimo de sintomas (≥6, ou ≥5 a partir dos 17 anos) dentro de um mesmo domínio."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Os domínios de desatenção e de hiperatividade/impulsividade do Critério A do DSM-5 NÃO são somados entre si — o limiar de ≥6 sintomas (≥5 a partir dos 17 anos) deve ser atingido dentro de um único domínio para caracterizar o transtorno."
  },
  {
    "id": 47,
    "code": "TDAH-03",
    "category": "TDAH",
    "subcategory": "Critério C: múltiplos contextos",
    "difficulty": "Intermediária",
    "prompt": "Yasmin, 7 anos, passou a apresentar sintomas intensos de desatenção e agitação exclusivamente em casa, desde que os pais iniciaram um processo de separação litigiosa há 3 meses em Feira de Santana. Na escola, porém, os professores garantem que ela continua concentrada, tranquila e sem qualquer alteração de comportamento ou de desempenho. Qual é a interpretação mais apropriada para este quadro?",
    "options": [
      {
        "letter": "A",
        "text": "Confirmar TDAH, apresentação combinada, e iniciar tratamento farmacológico.",
        "rationale": "Incorreta. O Critério C do DSM-5 exige sintomas em ≥2 contextos; neste caso, os sintomas ocorrem exclusivamente em casa, o que não sustenta o diagnóstico de TDAH."
      },
      {
        "letter": "B",
        "text": "Considerar reação ao conflito familiar, não TDAH, já que os sintomas estão restritos a um único ambiente e temporalmente associados a um estressor psicossocial identificável.",
        "rationale": "CORRETA. Sintomas restritos a um único ambiente e/ou claramente desencadeados por um estressor psicossocial identificável (como a separação litigiosa dos pais) não sustentam o diagnóstico de TDAH — reação a estressor/transtorno adaptativo deve ser investigada antes de firmar TDAH."
      },
      {
        "letter": "C",
        "text": "Iniciar imediatamente tratamento com estimulante, dada a intensidade dos sintomas relatados pelos pais.",
        "rationale": "Incorreta. Iniciar estimulante sem diagnóstico firmado, diante de sinais claros de causa contextual, não é apropriado."
      },
      {
        "letter": "D",
        "text": "Solicitar eletroencefalograma para confirmação diagnóstica antes de qualquer conduta.",
        "rationale": "Incorreta. O EEG não tem papel definido no diagnóstico de rotina do TDAH e não seria a conduta indicada, mesmo se o diagnóstico fosse confirmado."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Sintomas restritos a um único ambiente e/ou claramente ligados a um estressor psicossocial identificável não sustentam o diagnóstico de TDAH — desenvolvimento normal e reações contextuais são os principais diagnósticos diferenciais nessa situação."
  },
  {
    "id": 48,
    "code": "TDAH-04",
    "category": "TDAH",
    "subcategory": "Genética: herdabilidade e escore poligênico",
    "difficulty": "Intermediária",
    "prompt": "Durante uma consulta em Salvador, o pai de um menino recém-diagnosticado com TDAH conta que ele mesmo sempre foi \"disperso e inquieto\" na infância, embora nunca tenha sido avaliado, e pergunta ao médico se isso significa que ele \"passou o problema\" para o filho. Em relação à etiologia genética do TDAH, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "A herdabilidade estimada é baixa, em torno de 20-30%, o que dificulta o reconhecimento de sua base biológica.",
        "rationale": "Incorreta. A herdabilidade estimada é muito superior, entre 70-80% — uma das mais altas da Psiquiatria."
      },
      {
        "letter": "B",
        "text": "Estudos de gêmeos mostram herdabilidade de 70-80%, entre as mais altas da Psiquiatria, com um escore poligênico que se correlaciona linearmente com a intensidade dos sintomas.",
        "rationale": "CORRETA. Pais de crianças com TDAH têm risco 2 a 8 vezes maior de também ter o diagnóstico; estudos de GWAS identificaram variantes comuns associadas, compondo um escore poligênico que aumenta o risco em até 5 vezes e se correlaciona linearmente com a intensidade dos sintomas — mais uma evidência de que o TDAH representa o extremo de um espectro dimensional."
      },
      {
        "letter": "C",
        "text": "Pais de crianças com TDAH não apresentam risco aumentado de também terem o diagnóstico.",
        "rationale": "Incorreta. Pais de crianças com TDAH têm risco de 2 a 8 vezes maior de também apresentar o diagnóstico."
      },
      {
        "letter": "D",
        "text": "Já foram identificados genes específicos, isolados, de grande efeito individual, como causa determinante do TDAH.",
        "rationale": "Incorreta. Genes específicos são difíceis de identificar isoladamente; o modelo atual é o de uma doença poligênica complexa, com centenas a milhares de variantes de pequeno efeito individual."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "TDAH: herdabilidade de 70-80% (uma das mais altas da Psiquiatria); modelo poligênico complexo, com escore poligênico que se correlaciona linearmente com a intensidade dos sintomas — reforçando o TDAH como extremo de um espectro dimensional."
  },
  {
    "id": 49,
    "code": "TDAH-05",
    "category": "TDAH",
    "subcategory": "Estudo MTA (Multimodal Treatment Study)",
    "difficulty": "Avançada",
    "prompt": "Preparando um seminário sobre tratamento do TDAH, a estudante Bianca apresenta aos colegas os resultados do Estudo MTA (Multimodal Treatment Study), ensaio clínico randomizado multicêntrico com 579 crianças que comparou tratamento farmacológico, tratamento comportamental, a combinação dos dois e o tratamento comunitário padrão. Em relação aos achados desse estudo após 14 meses de seguimento, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O tratamento comportamental isolado foi superior ao tratamento farmacológico com metilfenidato na redução dos sintomas nucleares do TDAH.",
        "rationale": "Incorreta. Foi o tratamento farmacológico que se mostrou superior ao comportamental isolado na redução de sintomas nucleares após 14 meses."
      },
      {
        "letter": "B",
        "text": "O tratamento farmacológico com metilfenidato foi superior ao tratamento comportamental isolado na redução de sintomas nucleares; a combinação com tratamento comportamental não acrescentou eficácia significativa na redução desses sintomas em relação à farmacoterapia isolada.",
        "rationale": "CORRETA. Após 14 meses de seguimento, o tratamento farmacológico foi superior ao comportamental isolado na redução dos sintomas nucleares; a combinação de tratamentos não acrescentou eficácia significativa na redução dos sintomas centrais, embora subgrupos com comorbidades (ansiedade, transtornos disruptivos) tenham respondido melhor ao tratamento combinado."
      },
      {
        "letter": "C",
        "text": "Subgrupos com comorbidades, como ansiedade e transtornos disruptivos, não apresentaram qualquer diferença de resposta entre tratamento combinado e farmacológico isolado.",
        "rationale": "Incorreta. Subgrupos com comorbidades responderam melhor ao tratamento combinado, reforçando a importância da avaliação individualizada."
      },
      {
        "letter": "D",
        "text": "O estudo não teve qualquer seguimento de longo prazo além dos 14 meses iniciais.",
        "rationale": "Incorreta. Houve seguimentos de longo prazo (3, 8 e 16 anos), nos quais os grupos convergiram em desfechos clínicos, embora revisões sistemáticas de estudos ≥2 anos confirmem benefício do tratamento em longo prazo."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Estudo MTA: farmacoterapia com metilfenidato superior ao tratamento comportamental isolado na redução de sintomas nucleares; combinação não acrescenta eficácia significativa nos sintomas centrais, mas beneficia subgrupos com comorbidades."
  },
  {
    "id": 50,
    "code": "TDAH-06",
    "category": "TDAH",
    "subcategory": "Estimulantes como primeira escolha",
    "difficulty": "Intermediária",
    "prompt": "A mãe de Emanuel, 9 anos, recém-diagnosticado com TDAH em Ilhéus, chega à consulta com uma lista de medicamentos que encontrou pesquisando na internet e pergunta ao médico qual deles tem, de fato, o maior respaldo de evidência científica como primeira escolha de tratamento. Em relação ao tratamento farmacológico de primeira escolha para o TDAH, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "Estimulantes como metilfenidato e lisdexanfetamina são a primeira escolha, apresentando o maior tamanho de efeito entre as opções farmacológicas disponíveis.",
        "rationale": "CORRETA. O metilfenidato tem tamanho de efeito de 0,78 em crianças/adolescentes e 0,49 em adultos — o maior entre as opções disponíveis; a lisdexanfetamina tem evidência de eficácia comparável ou superior, com menor potencial de abuso do que doses equivalentes de d-anfetamina."
      },
      {
        "letter": "B",
        "text": "A atomoxetina é sempre a primeira escolha farmacológica, por ausência completa de efeitos colaterais relevantes.",
        "rationale": "Incorreta. A atomoxetina apresenta eficácia moderada, geralmente inferior à dos estimulantes, sendo reservada para situações de contraindicação, intolerância ou risco de uso inadequado dos estimulantes."
      },
      {
        "letter": "C",
        "text": "Antidepressivos tricíclicos, como a imipramina, são primeira linha no tratamento do TDAH em qualquer faixa etária.",
        "rationale": "Incorreta. Os antidepressivos tricíclicos não são primeira escolha, sendo considerados apenas quando não há resposta a estimulantes ou há tiques/enurese associados."
      },
      {
        "letter": "D",
        "text": "A modafinila é aprovada no Brasil especificamente para o tratamento do TDAH.",
        "rationale": "Incorreta. A modafinila é estudada para TDAH, mas aprovada no Brasil apenas para narcolepsia, carregando risco raro, porém grave, de síndrome de Stevens-Johnson."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Estimulantes (metilfenidato e lisdexanfetamina) são primeira escolha farmacológica no TDAH, com o maior tamanho de efeito entre as opções disponíveis, titulados por peso e resposta clínica."
  },
  {
    "id": 51,
    "code": "TDAH-07",
    "category": "TDAH",
    "subcategory": "Segurança dos estimulantes: tiques e crescimento",
    "difficulty": "Avançada",
    "prompt": "Os pais de Otávio, 8 anos, em uso de metilfenidato há 1 ano em Feira de Santana, retornam preocupados: notaram que ele cresceu pouco no último ano e que, recentemente, começou a piscar os olhos repetidamente, um tique que nunca havia apresentado antes. Eles perguntam se é preciso suspender a medicação imediatamente. Em relação à segurança e à monitorização dos estimulantes no tratamento do TDAH, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "Tiques e epilepsia controlada são contraindicações formais absolutas ao uso de estimulantes.",
        "rationale": "Incorreta. Tiques e epilepsia controlada não são mais consideradas contraindicação formal ao uso de estimulantes — apenas monitorização clínica atenta é recomendada."
      },
      {
        "letter": "B",
        "text": "O uso contínuo de estimulantes por anos pode associar-se a uma redução discreta (cerca de 2 cm) na altura final, justificando o acompanhamento periódico de peso e altura; tiques e epilepsia controlada não são mais contraindicação formal, exigindo apenas monitorização clínica.",
        "rationale": "CORRETA. Existe associação dose-dependente com redução de apetite, e o uso contínuo por anos pode associar-se a cerca de 2 cm a menos na altura final; efeitos cardiovasculares são pequenos e pouco significativos (PA <5 mmHg, FC <5 bpm); tiques e epilepsia não são mais contraindicação absoluta."
      },
      {
        "letter": "C",
        "text": "Estimulantes causam aumento significativo e clinicamente preocupante da pressão arterial e da frequência cardíaca na maioria dos pacientes.",
        "rationale": "Incorreta. Os aumentos observados em PA (<5 mmHg) e FC (<5 bpm) são pequenos e pouco significativos, ainda que a história cardiovascular pessoal/familiar deva ser avaliada antes de iniciar o tratamento."
      },
      {
        "letter": "D",
        "text": "O potencial de abuso dos estimulantes impede completamente seu uso em qualquer paciente com TDAH.",
        "rationale": "Incorreta. Embora exista potencial de abuso, estudos prospectivos não mostram aumento do risco de transtorno por uso de substâncias com tratamento adequado; formulações de longa ação têm menor risco de uso inadequado."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Monitorização de estimulantes: acompanhar peso/altura (redução de apetite, dose-dependente), avaliar história cardiovascular antes de iniciar (efeitos pequenos em PA/FC); tiques e epilepsia controlada não são mais contraindicação formal, apenas monitorização clínica."
  },
  {
    "id": 52,
    "code": "TDAH-08",
    "category": "TDAH",
    "subcategory": "Comorbidades: TOD x Transtorno de Conduta x TEI",
    "difficulty": "Intermediária",
    "prompt": "Kevin, 11 anos, é avaliado em Salvador por comportamento opositor frequente em casa, além de episódios recentes de agressão física a colegas e destruição deliberada de objetos na escola, o que já resultou em suspensão. A equipe discute se esse padrão mais grave de comportamento representa apenas TOD associado ao TDAH ou algo além disso. Em relação às comorbidades e diagnósticos diferenciais do TDAH, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O transtorno de oposição desafiante (TOD) envolve necessariamente violação grave de direitos de terceiros, como agressão física ou destruição de propriedade.",
        "rationale": "Incorreta. No TOD há oposição e desafio (humor irritável, comportamento argumentativo, recusa a regras), mas não necessariamente violação grave dos direitos de outras pessoas — essa é a característica que define, de forma mais grave, o transtorno da conduta."
      },
      {
        "letter": "B",
        "text": "O transtorno da conduta caracteriza-se por padrão repetitivo e persistente de comportamentos que violam direitos básicos de outras pessoas ou normas sociais importantes, representando maior gravidade comportamental do que o TOD.",
        "rationale": "CORRETA. O transtorno da conduta envolve agressão, destruição de propriedade, furtos/enganos e violações graves de regras — maior gravidade do que o TOD, que se caracteriza por oposição, irritabilidade e desafio dirigidos principalmente a figuras de autoridade, sem necessariamente violar gravemente os direitos de outras pessoas."
      },
      {
        "letter": "C",
        "text": "O transtorno explosivo intermitente (TEI) caracteriza-se por oposição e irritabilidade contínuas, sem explosões episódicas.",
        "rationale": "Incorreta. O TEI caracteriza-se por explosões de raiva EPISÓDICAS (não contínuas), desproporcionais e seguidas de arrependimento — diferente do padrão contínuo do TOD."
      },
      {
        "letter": "D",
        "text": "TOD, transtorno de conduta e TEI são sinônimos e podem ser usados de forma intercambiável na prática clínica.",
        "rationale": "Incorreta. São condições distintas, com características predominantes diferentes: TOD (oposição/desafio), transtorno de conduta (violação de direitos/normas, mais grave) e TEI (explosões episódicas desproporcionais)."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "TOD: oposição, irritabilidade e desafio, sem violação grave de direitos. Transtorno da conduta: mais grave, com agressão/destruição/furtos. TEI: explosões episódicas, desproporcionais, seguidas de arrependimento. Comorbidade presente em até 80% dos casos clínicos de TDAH."
  },
  {
    "id": 53,
    "code": "TDAH-09",
    "category": "TDAH",
    "subcategory": "TDAH em adultos",
    "difficulty": "Avançada",
    "prompt": "Alan, 28 anos, analista financeiro, procura avaliação em uma clínica de Salvador após perder dois empregos no último ano por \"falta de foco\" e atrasos constantes. Ele relata que sempre foi \"disperso\" desde criança, mas nunca chegou a ser avaliado por um médico, e comenta, de forma quase despreocupada, que costuma beber socialmente nos fins de semana, sem preencher critérios para transtorno por uso de álcool. Em relação à avaliação e conduta neste caso, é correto afirmar que:",
    "options": [
      {
        "letter": "A",
        "text": "O diagnóstico de TDAH em adultos é inválido, pois os critérios do DSM-5 aplicam-se apenas a crianças.",
        "rationale": "Incorreta. O DSM-5 reconhece explicitamente o diagnóstico de TDAH em adultos, exigindo apenas que os sintomas tenham iniciado antes dos 12 anos, ainda que o diagnóstico formal só seja feito na vida adulta."
      },
      {
        "letter": "B",
        "text": "A ausência de diagnóstico formal na infância exclui definitivamente a possibilidade de TDAH no adulto.",
        "rationale": "Incorreta. Estudos mostram que grande parte dos adultos com TDAH nunca foi diagnosticada na infância (em um estudo brasileiro de base populacional, apenas 12,6% dos adultos com TDAH tinham diagnóstico antes dos 12 anos), apesar de sintomas retrospectivamente identificáveis."
      },
      {
        "letter": "C",
        "text": "Deve-se investigar retrospectivamente sintomas de início precoce (antes dos 12 anos) e avaliar sistematicamente comorbidades, incluindo uso de substâncias, antes de definir a conduta.",
        "rationale": "CORRETA. A avaliação de TDAH em adultos exige investigação cuidadosa do início retrospectivo dos sintomas e avaliação sistemática de comorbidades; em adultos, uso de substâncias chega a até 40% e transtornos de personalidade (clusters B/C) a cerca de 50% dos casos."
      },
      {
        "letter": "D",
        "text": "O uso recreativo ocasional de álcool, sem critérios para transtorno por uso de substância, contraindica de forma absoluta qualquer investigação para TDAH.",
        "rationale": "Incorreta. Uso recreativo sem critérios para transtorno por uso de substância não contraindica a investigação — ao contrário, o TDAH aumenta o risco de uso problemático de substâncias e deve ser cuidadosamente avaliado."
      }
    ],
    "correctLetter": "C",
    "clinicalPointers": "TDAH em adultos exige confirmação retrospectiva de sintomas com início antes dos 12 anos e investigação sistemática de comorbidades (uso de substâncias, transtornos de humor, ansiedade e de personalidade), frequentes nessa faixa etária."
  },
  {
    "id": 54,
    "code": "TDAH-10",
    "category": "TDAH",
    "subcategory": "Diagnóstico diferencial: privação de sono",
    "difficulty": "Intermediária",
    "prompt": "Sarah, 9 anos, é encaminhada por desatenção e irritabilidade crescentes na escola de Vitória da Conquista. Ao investigar a rotina em casa, o pediatra descobre que ela dorme, em média, menos de 6 horas por noite, pois divide o quarto com irmãos mais velhos que ficam acordados até tarde assistindo televisão. Segundo o diagnóstico diferencial do TDAH discutido na disciplina, qual condição pode reproduzir desatenção, irritabilidade e agitação em crianças, constituindo uma causa reversível e subdiagnosticada que deve ser investigada antes de firmar o diagnóstico de TDAH?",
    "options": [
      {
        "letter": "A",
        "text": "Privação de sono ou sono de má qualidade.",
        "rationale": "CORRETA. Sono insuficiente ou de má qualidade reproduz desatenção, irritabilidade e agitação em crianças; investigar a rotina e a higiene do sono antes de firmar o diagnóstico de TDAH é recomendado, por se tratar de causa reversível e subdiagnosticada."
      },
      {
        "letter": "B",
        "text": "Transtorno do Espectro Autista.",
        "rationale": "Incorreta. O TEA cursa com prejuízo central na comunicação social e padrões restritos/repetitivos de comportamento, ausentes no TDAH isolado — é um diagnóstico diferencial/comórbido distinto, não uma causa reversível de sintomas mimetizando o TDAH."
      },
      {
        "letter": "C",
        "text": "Deficiência intelectual leve, isoladamente.",
        "rationale": "Incorreta. Embora deva ser considerada no raciocínio diagnóstico amplo, não é a condição citada especificamente como causa reversível que reproduz desatenção/irritabilidade/agitação a ser investigada antes do diagnóstico de TDAH."
      },
      {
        "letter": "D",
        "text": "Síndrome de Tourette.",
        "rationale": "Incorreta. A síndrome de Tourette caracteriza-se por múltiplos tiques motores e ao menos um tique vocal, um quadro distinto, embora possa ser comórbida ao TDAH."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Privação de sono/má qualidade do sono reproduz desatenção, irritabilidade e agitação — causa reversível e subdiagnosticada que deve ser sistematicamente investigada (rotina e higiene do sono) antes de firmar o diagnóstico de TDAH."
  },
  {
    "id": 55,
    "code": "TDAH-11",
    "category": "TDAH",
    "subcategory": "TDAH x TEA: diferencial (integração com a aula de TEA)",
    "difficulty": "Avançada",
    "prompt": "Em uma aula de revisão em Feira de Santana, os estudantes discutem o caso de um menino que preenche critérios tanto para TDAH quanto para TEA ao mesmo tempo, e se perguntam se isso é sequer possível segundo o DSM-5, já que um colega afirma ter lido em um material antigo que os dois diagnósticos seriam mutuamente excludentes. Em relação ao diagnóstico diferencial entre TDAH e Transtorno do Espectro Autista (TEA), assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O TEA cursa com prejuízo central na comunicação social e padrões restritos/repetitivos de comportamento, ausentes no TDAH isolado; entretanto, os dois quadros podem coexistir com frequência, como comorbidade.",
        "rationale": "CORRETA. Essa é exatamente a formulação apresentada na aula de TDAH; de forma convergente, a aula de TEA descreve o TDAH como uma das comorbidades mais frequentemente associadas ao TEA — ou seja, a coexistência dos dois diagnósticos não os torna sinônimos, mas também não é uma contraindicação diagnóstica."
      },
      {
        "letter": "B",
        "text": "TDAH e TEA nunca coexistem no mesmo paciente, sendo diagnósticos mutuamente excludentes pelo DSM-5.",
        "rationale": "Incorreta. O DSM-5 admite explicitamente a coexistência dos dois diagnósticos, ao contrário do que ocorria em classificações anteriores."
      },
      {
        "letter": "C",
        "text": "A presença isolada de desatenção e impulsividade já é suficiente para diagnosticar TEA, dispensando avaliação dos critérios sociais.",
        "rationale": "Incorreta. O diagnóstico de TEA exige, obrigatoriamente, os três subdomínios do Critério A relacionados à comunicação e interação social, além de pelo menos 2 dos 4 itens do Critério B — desatenção e impulsividade isoladas não satisfazem esses critérios."
      },
      {
        "letter": "D",
        "text": "O TDAH sempre envolve déficits de reciprocidade socioemocional idênticos aos observados no TEA.",
        "rationale": "Incorreta. O TDAH, isoladamente, não cursa com os déficits centrais de reciprocidade socioemocional e comunicação não verbal característicos do TEA."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "TDAH x TEA: o TEA exige prejuízo central na comunicação social e comportamentos restritos/repetitivos (ausentes no TDAH isolado); os dois transtornos coexistem com frequência como comorbidade, sem que isso os torne sinônimos."
  },
  {
    "id": 56,
    "code": "TA-01",
    "category": "Alimentares",
    "subcategory": "Classificação: AN, BN e TCA",
    "difficulty": "Intermediária",
    "prompt": "Estudando os Transtornos Alimentares para a prova, a estudante Camila tenta montar um quadro comparativo entre anorexia nervosa, bulimia nervosa e transtorno de compulsão alimentar, mas se confunde sobre qual deles exige a presença de comportamentos compensatórios e qual não exige. Em relação à classificação desses transtornos, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "A anorexia nervosa é caracterizada por episódios recorrentes de compulsão alimentar, sem qualquer restrição alimentar associada.",
        "rationale": "Incorreta. A anorexia nervosa (AN) é caracterizada por restrição alimentar levando a baixo peso significativo, medo intenso de ganhar peso e perturbação na vivência do peso/forma corporal — a compulsão alimentar, quando presente, ocorre apenas no subtipo compulsão/purgação."
      },
      {
        "letter": "B",
        "text": "A bulimia nervosa envolve episódios recorrentes de compulsão alimentar seguidos de comportamentos compensatórios inadequados, como vômitos, laxantes, jejum ou exercício excessivo.",
        "rationale": "CORRETA. Essa é exatamente a definição de bulimia nervosa (BN) apresentada em aula, que a diferencia do transtorno de compulsão alimentar (TCA) justamente pela presença desses comportamentos compensatórios recorrentes."
      },
      {
        "letter": "C",
        "text": "O transtorno de compulsão alimentar (TCA) é definido pela presença obrigatória de comportamentos compensatórios purgativos regulares.",
        "rationale": "Incorreta. O TCA é definido, ao contrário, pela AUSÊNCIA de comportamentos compensatórios inadequados regulares — essa ausência é justamente o que o diferencia da bulimia nervosa."
      },
      {
        "letter": "D",
        "text": "O TARE (Transtorno Alimentar Restritivo/Evitativo) é sinônimo de anorexia nervosa quando diagnosticado em crianças.",
        "rationale": "Incorreta. O TARE é uma categoria diagnóstica distinta, definida centralmente pela AUSÊNCIA de preocupação com peso ou imagem corporal — elemento que o diferencia da anorexia nervosa, mesmo diante de quadros clínicos de desnutrição semelhantes."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Classificação dos TAs: AN (restrição → baixo peso), BN (compulsão + comportamento compensatório inadequado recorrente), TCA (compulsão SEM comportamento compensatório regular), TARE (restrição/evitação sem preocupação com peso/forma corporal)."
  },
  {
    "id": 57,
    "code": "TA-02",
    "category": "Alimentares",
    "subcategory": "TARE: ausência de preocupação com peso/forma",
    "difficulty": "Avançada",
    "prompt": "Pietro, 8 anos, é levado a um ambulatório de Salvador porque recusa praticamente todos os alimentos com textura pastosa ou cheiro forte, mantendo uma dieta extremamente restrita a poucos itens, o que já causou perda de peso e baixa estatura para a idade. Questionado com cuidado, ele demonstra não ter qualquer preocupação com peso ou forma corporal — apenas nojo declarado de certas texturas. Qual é o diagnóstico mais provável?",
    "options": [
      {
        "letter": "A",
        "text": "Anorexia nervosa, subtipo restritivo.",
        "rationale": "Incorreta. O medo intenso de ganhar peso e a perturbação na vivência do peso/forma corporal são critérios centrais e obrigatórios da anorexia nervosa, explicitamente ausentes neste caso."
      },
      {
        "letter": "B",
        "text": "Transtorno Alimentar Restritivo/Evitativo (TARE).",
        "rationale": "CORRETA. O TARE é definido por alteração persistente na alimentação que resulta em desnutrição/perda de peso significativas, SEM preocupação com peso ou imagem corporal — elemento que o distingue centralmente da anorexia nervosa; entre as motivações possíveis estão justamente a evitação por características sensoriais do alimento (sabor, textura, cheiro)."
      },
      {
        "letter": "C",
        "text": "Transtorno de ruminação.",
        "rationale": "Incorreta. O transtorno de ruminação caracteriza-se por regurgitação repetida de alimentos com nova mastigação/deglutição/expulsão, quadro distinto do descrito."
      },
      {
        "letter": "D",
        "text": "Bulimia nervosa.",
        "rationale": "Incorreta. Não há relato de episódios de compulsão alimentar nem de comportamentos compensatórios, elementos centrais da bulimia nervosa."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "TARE: alteração persistente na alimentação com desnutrição/perda de peso/prejuízo, SEM preocupação com peso ou imagem corporal — pode decorrer de evitação sensorial, apetite diminuído ou medo de consequências negativas da alimentação (engasgar, vomitar)."
  },
  {
    "id": 58,
    "code": "TA-03",
    "category": "Alimentares",
    "subcategory": "Classificação de gravidade da AN por IMC",
    "difficulty": "Intermediária",
    "prompt": "Renata, 21 anos, com diagnóstico confirmado de anorexia nervosa há 8 meses, comparece à consulta de reavaliação em Feira de Santana. O nutricionista calcula seu IMC atual em 16,5 kg/m², uma discreta melhora em relação à última consulta. Segundo os critérios de gravidade do DSM-5-TR para adultos, qual é a classificação atual de Renata?",
    "options": [
      {
        "letter": "A",
        "text": "Leve.",
        "rationale": "Incorreta. A classificação leve corresponde a IMC ≥17 kg/m², valor superior ao apresentado pela paciente."
      },
      {
        "letter": "B",
        "text": "Moderada.",
        "rationale": "CORRETA. O DSM-5-TR classifica a gravidade da AN em adultos com base no IMC atual: moderada corresponde à faixa de 16 a 16,99 kg/m² — intervalo em que se encaixa exatamente o IMC de 16,5 kg/m² da paciente."
      },
      {
        "letter": "C",
        "text": "Grave.",
        "rationale": "Incorreta. A classificação grave corresponde à faixa de 15 a 15,99 kg/m², inferior ao IMC apresentado."
      },
      {
        "letter": "D",
        "text": "Extrema.",
        "rationale": "Incorreta. A classificação extrema corresponde a IMC <15 kg/m², valor bem inferior ao apresentado pela paciente."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Classificação de gravidade da AN pelo IMC (DSM-5-TR, adultos): leve ≥17; moderada 16-16,99; grave 15-15,99; extrema <15 kg/m². A classificação pode ser elevada diante de maior comprometimento clínico/funcional."
  },
  {
    "id": 59,
    "code": "TA-04",
    "category": "Alimentares",
    "subcategory": "Quadro clínico: egossintonia e o mito da \"perda de apetite\"",
    "difficulty": "Intermediária",
    "prompt": "Ao acompanhar Luana, 19 anos, estudante universitária em tratamento de anorexia nervosa em Salvador, o psiquiatra nota que ela descreve com orgulho sua rotina alimentar extremamente restritiva, dizendo se sentir \"finalmente no controle\" da própria vida, e minimiza qualquer preocupação da família com sua magreza acentuada. Em relação ao quadro clínico da anorexia nervosa apresentado na disciplina, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "A restrição alimentar e a perda de peso costumam ser vivenciadas pela paciente como problema e motivo de sofrimento imediato, facilitando a adesão ao tratamento.",
        "rationale": "Incorreta. Ao contrário, a perda de peso e o controle alimentar costumam ser vivenciados como conquista e autodisciplina (egossintonia) — o que dificulta, e não facilita, a adesão ao tratamento."
      },
      {
        "letter": "B",
        "text": "A perda de peso e o controle alimentar costumam ser vivenciados como conquista e autodisciplina (egossintonia); relato de perda real do apetite fala CONTRA o diagnóstico de anorexia nervosa.",
        "rationale": "CORRETA. A denominação \"anorexia\" (perda do apetite) é considerada imprecisa: a paciente típica preserva a fome e restringe apesar dela; um relato de anorexia real (perda de apetite) é uma armadilha clássica de prova e fala CONTRA o diagnóstico."
      },
      {
        "letter": "C",
        "text": "A amenorreia é, no DSM-5-TR, critério diagnóstico obrigatório para o diagnóstico de anorexia nervosa.",
        "rationale": "Incorreta. A amenorreia é frequente, mas não é mais critério diagnóstico obrigatório no DSM-5-TR."
      },
      {
        "letter": "D",
        "text": "Pacientes com anorexia nervosa tipicamente reduzem a atividade física à medida que emagrecem, por fadiga.",
        "rationale": "Incorreta. Ao contrário, há tendência a aumentar a atividade física mesmo diante do emagrecimento — a chamada hiperatividade física."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "A restrição e a perda de peso na AN costumam ser egossintônicas (vividas como conquista), dificultando a adesão ao tratamento. \"Perda de apetite\" é armadilha de prova: a paciente típica preserva a fome e restringe apesar dela."
  },
  {
    "id": 60,
    "code": "TA-05",
    "category": "Alimentares",
    "subcategory": "Complicações: síndrome de realimentação",
    "difficulty": "Avançada",
    "prompt": "Beatriz, 17 anos, é internada em um hospital de Vitória da Conquista com anorexia nervosa grave, após meses de restrição alimentar progressiva: apresenta bradicardia e hipotensão postural ao exame, além de perda ponderal acentuada. A equipe decide iniciar a renutrição de forma cautelosa, começando com um aporte calórico baixo e aumentos graduais semanais, monitorando os eletrólitos de perto. Qual é a complicação mais temida desse início de renutrição, que justifica essa cautela?",
    "options": [
      {
        "letter": "A",
        "text": "Síndrome de realimentação, caracterizada por hipofosfatemia grave, com risco cardiológico, neurológico e hematológico.",
        "rationale": "CORRETA. A síndrome de realimentação é explicitamente descrita como a complicação mais temida do início da renutrição; por isso, recomenda-se iniciar com valores baixos (cerca de 1.000 kcal/dia), com aumentos graduais semanais (500-750 kcal), até atingir cerca de 3.000 kcal/dia, sempre com monitorização cuidadosa dos eletrólitos."
      },
      {
        "letter": "B",
        "text": "Síndrome de Mallory-Weiss.",
        "rationale": "Incorreta. A síndrome de Mallory-Weiss (laceração da mucosa esofágica) é uma complicação gastrintestinal associada aos vômitos recorrentes da bulimia nervosa, não à renutrição da anorexia nervosa."
      },
      {
        "letter": "C",
        "text": "Hipertrofia parotídea bilateral.",
        "rationale": "Incorreta. A hipertrofia parotídea bilateral (sialoadenose) é um achado associado aos vômitos recorrentes da bulimia nervosa, não à renutrição."
      },
      {
        "letter": "D",
        "text": "Perimólise (erosão do esmalte dentário).",
        "rationale": "Incorreta. A perimólise decorre da exposição repetida do esmalte dentário ao ácido gástrico dos vômitos recorrentes, achado da bulimia nervosa, não complicação da renutrição."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Síndrome de realimentação: hipofosfatemia grave (risco cardiológico, neurológico, hematológico) ao iniciar renutrição em paciente gravemente desnutrida. Recomenda-se início com ~1.000 kcal/dia, aumentos graduais semanais, até ~3.000 kcal/dia, com monitorização cuidadosa dos eletrólitos."
  },
  {
    "id": 61,
    "code": "TA-06",
    "category": "Alimentares",
    "subcategory": "Sinal de Russell e repercussões orais da BN",
    "difficulty": "Intermediária",
    "prompt": "Nathália, 24 anos, com bulimia nervosa e vômitos autoinduzidos frequentes há meses, procura atendimento em Ilhéus por queixas dentárias. Ao exame físico, o médico nota calosidades no dorso da mão direita de Nathália, decorrentes do atrito repetido com os incisivos durante a indução mecânica do vômito. Esse achado semiológico clássico é conhecido como:",
    "options": [
      {
        "letter": "A",
        "text": "Sinal de Russell.",
        "rationale": "CORRETA. O sinal de Russell corresponde a calosidades/ulcerações no dorso da mão, decorrentes do uso repetido dos dedos para indução mecânica do vômito — achado clássico ao exame físico na bulimia nervosa. Com a evolução do quadro, a paciente aprende a induzir o vômito sem estimulação mecânica, podendo o sinal desaparecer."
      },
      {
        "letter": "B",
        "text": "Sinal do travesseiro psíquico.",
        "rationale": "Incorreta. Esse sinal é um achado semiológico da catatonia, associado à esquizofrenia, sem relação com a bulimia nervosa."
      },
      {
        "letter": "C",
        "text": "Sinal de Chvostek.",
        "rationale": "Incorreta. O sinal de Chvostek é um achado clássico de hipocalcemia, sem relação com a bulimia nervosa."
      },
      {
        "letter": "D",
        "text": "Sinal de Trousseau.",
        "rationale": "Incorreta. O sinal de Trousseau também é um achado clássico de hipocalcemia, sem relação com a bulimia nervosa."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Repercussões orais/salivares da BN: hipertrofia parotídea bilateral (sialoadenose, não inflamatória), elevação da amilase sérica (fração salivar), erosão do esmalte dentário (perimólise, face lingual dos dentes) e sinal de Russell (calosidades no dorso da mão)."
  },
  {
    "id": 62,
    "code": "TA-07",
    "category": "Alimentares",
    "subcategory": "Distúrbio hidroeletrolítico dos vômitos recorrentes",
    "difficulty": "Avançada",
    "prompt": "Fernanda, 27 anos, com bulimia nervosa e vômitos autoinduzidos múltiplos por dia há vários meses, chega ao pronto-socorro de Salvador com fraqueza intensa, cãibras musculares e um traçado eletrocardiográfico alterado. Os exames mostram potássio sérico de 2,8 mEq/L. Qual é o mecanismo fisiopatológico associado a esse distúrbio hidroeletrolítico?",
    "options": [
      {
        "letter": "A",
        "text": "Hipocalemia e alcalose metabólica, decorrentes da perda de ácido gástrico pelos vômitos recorrentes.",
        "rationale": "CORRETA. Vômitos autoinduzidos recorrentes causam perda de ácido clorídrico gástrico, levando classicamente a alcalose metabólica hipoclorêmica e hipocalemia — padrão hidroeletrolítico mais característico e mais cobrado na bulimia nervosa com padrão purgativo por vômitos."
      },
      {
        "letter": "B",
        "text": "Hipercalemia e acidose metabólica, decorrentes do uso de laxantes.",
        "rationale": "Incorreta. O uso de laxantes tende a causar acidose metabólica (por perda de bicarbonato intestinal), mas o quadro descrito é de vômitos recorrentes, não de uso de laxantes; além disso, a alteração de potássio esperada com vômitos é a hipocalemia, não a hipercalemia."
      },
      {
        "letter": "C",
        "text": "Hipernatremia e hipervolemia, decorrentes de retenção hídrica compensatória.",
        "rationale": "Incorreta. Vômitos recorrentes tendem a causar desidratação e depleção de volume, não hipervolemia ou hipernatremia."
      },
      {
        "letter": "D",
        "text": "Hipocalcemia isolada, sem outras alterações hidroeletrolíticas associadas.",
        "rationale": "Incorreta. A hipocalcemia isolada não é o padrão hidroeletrolítico típico da bulimia nervosa; a alteração clássica e clinicamente mais relevante é a hipocalemia associada à alcalose metabólica."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Vômitos autoinduzidos recorrentes → hipocalemia + alcalose metabólica (perda de ácido gástrico); abuso de laxantes → tende a acidose metabólica — distinção fisiopatológica relevante para interpretação de exames complementares na BN."
  },
  {
    "id": 63,
    "code": "TA-08",
    "category": "Alimentares",
    "subcategory": "Tratamento farmacológico da BN: fluoxetina",
    "difficulty": "Intermediária",
    "prompt": "Ao definir o tratamento farmacológico de Patrícia, 25 anos, com bulimia nervosa, acompanhada em Feira de Santana, o psiquiatra explica à paciente que, entre as diversas opções disponíveis, apenas uma tem aprovação regulatória específica para essa condição, com dose bem estabelecida. Em relação ao tratamento farmacológico da bulimia nervosa, apresentado na disciplina, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "Não há nenhum fármaco aprovado especificamente para o tratamento da bulimia nervosa.",
        "rationale": "Incorreta. A fluoxetina, na dose de 60 mg/dia, é o agente aprovado especificamente para BN pelas agências reguladoras."
      },
      {
        "letter": "B",
        "text": "A fluoxetina, na dose de 60 mg/dia, é o único ISRS aprovado especificamente para bulimia nervosa, reduzindo episódios bulímicos, vômitos autoinduzidos e sintomas depressivos associados.",
        "rationale": "CORRETA. A fluoxetina 60 mg/dia é o agente farmacológico mais estudado e o único aprovado pelas agências reguladoras especificamente para BN; o topiramato também se mostrou eficaz na redução de sintomas bulímicos, mas com evidência mais limitada."
      },
      {
        "letter": "C",
        "text": "Benzodiazepínicos são a primeira escolha farmacológica para bulimia nervosa.",
        "rationale": "Incorreta. Benzodiazepínicos não são citados como tratamento farmacológico da bulimia nervosa; a primeira escolha terapêutica global é a psicoterapia (TCC focada em transtornos alimentares)."
      },
      {
        "letter": "D",
        "text": "A lisdexanfetamina é o fármaco aprovado especificamente para bulimia nervosa.",
        "rationale": "Incorreta. A lisdexanfetamina é o fármaco aprovado (FDA e Anvisa) especificamente para o transtorno de compulsão alimentar (TCA), não para a bulimia nervosa."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "BN: TCC-TA é a psicoterapia de primeira escolha; fluoxetina 60mg/dia é o único ISRS aprovado especificamente para BN (também reduz sintomas depressivos associados); topiramato é opção adjuvante com evidência mais limitada."
  },
  {
    "id": 64,
    "code": "TA-09",
    "category": "Alimentares",
    "subcategory": "TCA: ausência de comportamento compensatório",
    "difficulty": "Intermediária",
    "prompt": "Simone, 33 anos, relata em consulta em Salvador episódios recorrentes, pelo menos duas vezes por semana nos últimos 4 meses, em que come grandes quantidades de comida em poucos minutos, sentindo que \"não consegue parar\", geralmente escondida dos filhos por vergonha. Questionada diretamente, ela nega qualquer método para \"compensar\" — não vomita, não usa laxante, não faz jejum nem exercício excessivo depois desses episódios. Qual é o diagnóstico mais provável?",
    "options": [
      {
        "letter": "A",
        "text": "Bulimia nervosa.",
        "rationale": "Incorreta. A BN exige a presença de comportamentos compensatórios inadequados recorrentes (vômitos, laxantes, jejum, exercício excessivo) associados à compulsão alimentar — explicitamente ausentes neste caso."
      },
      {
        "letter": "B",
        "text": "Transtorno de Compulsão Alimentar (TCA).",
        "rationale": "CORRETA. O caso apresenta episódios recorrentes de compulsão alimentar com indicadores de perda de controle (comer sozinha por vergonha), na ausência de qualquer comportamento compensatório inadequado — critério que define o TCA e o diferencia especificamente da BN."
      },
      {
        "letter": "C",
        "text": "Anorexia nervosa, subtipo compulsão alimentar/purgação.",
        "rationale": "Incorreta. A AN exige peso corporal significativamente baixo como critério central, não mencionado no caso."
      },
      {
        "letter": "D",
        "text": "Transtorno Alimentar Restritivo/Evitativo (TARE).",
        "rationale": "Incorreta. O TARE não cursa com episódios de compulsão alimentar; é definido por evitação/restrição alimentar, sem preocupação com peso ou forma corporal."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "O TCA se diferencia da BN especificamente pela AUSÊNCIA de comportamentos compensatórios inadequados recorrentes — ambos compartilham a presença de episódios de compulsão alimentar com perda de controle."
  },
  {
    "id": 65,
    "code": "TA-10",
    "category": "Alimentares",
    "subcategory": "Tratamento farmacológico do TCA: lisdexanfetamina",
    "difficulty": "Intermediária",
    "prompt": "Ao discutir o tratamento farmacológico de Cristiano, 38 anos, com TCA moderado a grave e resposta parcial à psicoterapia isolada, acompanhado em Ilhéus, o psiquiatra explica que existe um único fármaco aprovado, tanto no Brasil quanto nos Estados Unidos, especificamente para essa condição. Em relação ao tratamento farmacológico do transtorno de compulsão alimentar (TCA) moderado a grave, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "A lisdexanfetamina é a única droga atualmente aprovada tanto pelo FDA quanto pela Anvisa especificamente para o tratamento do TCA moderado a grave.",
        "rationale": "CORRETA. A lisdexanfetamina, psicoestimulante também usado no TDAH, é a única droga aprovada por ambas as agências reguladoras especificamente para o TCA moderado a grave, com efetividade demonstrada na redução de episódios de compulsão e no peso corporal."
      },
      {
        "letter": "B",
        "text": "A sibutramina é isenta de risco cardiovascular e considerada a primeira linha absoluta para o TCA.",
        "rationale": "Incorreta. A sibutramina, apesar de aprovada no Brasil e eficaz em ensaios, exige cautela pelo risco cardiovascular, não sendo isenta de risco nem considerada primeira linha frente à TCC e à lisdexanfetamina."
      },
      {
        "letter": "C",
        "text": "Antipsicóticos de alta potência constituem o tratamento farmacológico padrão para o TCA.",
        "rationale": "Incorreta. Antipsicóticos não são citados como tratamento padrão do TCA; a farmacoterapia de referência é a lisdexanfetamina."
      },
      {
        "letter": "D",
        "text": "Não há qualquer opção farmacológica com evidência estabelecida para o tratamento do TCA.",
        "rationale": "Incorreta. Além da lisdexanfetamina (única aprovada por FDA e Anvisa), há evidência para ISRS em dose alta, topiramato (off-label) e sibutramina (off-label no Brasil), com diferentes perfis de evidência e tolerabilidade."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "TCA: TCC é a psicoterapia mais estudada; lisdexanfetamina é a única droga aprovada (FDA + Anvisa) especificamente para TCA moderado a grave, reduzindo episódios de compulsão e auxiliando na perda de peso."
  },
  {
    "id": 66,
    "code": "TA-11",
    "category": "Alimentares",
    "subcategory": "Prognóstico: mortalidade entre os transtornos psiquiátricos",
    "difficulty": "Avançada",
    "prompt": "Durante uma aula de revisão sobre prognóstico dos Transtornos Alimentares em Feira de Santana, um estudante se surpreende ao saber que um transtorno de prevalência relativamente baixa na população pode, ainda assim, ser um dos mais letais entre todos os diagnósticos psiquiátricos. Em relação ao prognóstico dos Transtornos Alimentares, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O transtorno de compulsão alimentar apresenta a maior taxa de mortalidade entre todos os transtornos psiquiátricos.",
        "rationale": "Incorreta. É a anorexia nervosa, e não o TCA, que apresenta a maior taxa de mortalidade entre todos os transtornos psiquiátricos."
      },
      {
        "letter": "B",
        "text": "A anorexia nervosa, apesar de sua prevalência relativamente baixa (0,3-0,6% na população geral), é o transtorno psiquiátrico com maior taxa de mortalidade, chegando a 5-18% no subgrupo de evolução desfavorável.",
        "rationale": "CORRETA. Apesar da baixa prevalência, a AN é explicitamente descrita como o transtorno psiquiátrico com maior taxa de mortalidade; fatores de pior prognóstico incluem TOC comórbido, comportamento suicida, impulsividade e transtorno da personalidade borderline, especialmente na AN e na BN."
      },
      {
        "letter": "C",
        "text": "A bulimia nervosa tem taxa de mortalidade superior à da anorexia nervosa.",
        "rationale": "Incorreta. A mortalidade da BN (0,3-3%) é substancialmente inferior à da AN (5-18% no subgrupo de evolução desfavorável)."
      },
      {
        "letter": "D",
        "text": "Nenhum dos Transtornos Alimentares apresenta risco de suicídio aumentado em relação à população geral.",
        "rationale": "Incorreta. O risco de suicídio é elevado nos TAs, especialmente na AN, devendo ser sistematicamente avaliado."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Prognóstico: AN tem a maior mortalidade entre transtornos psiquiátricos (5-18% no subgrupo desfavorável); BN 0,3-3%. Fatores de pior prognóstico: TOC comórbido, comportamento suicida, impulsividade, TPB. Fatores de melhor prognóstico: bom suporte familiar, admissão da fome, boa autoestima."
  },
  {
    "id": 67,
    "code": "SONO-01",
    "category": "Sono",
    "subcategory": "Modelo de dois processos (Processo S e Processo C)",
    "difficulty": "Intermediária",
    "prompt": "Preparando uma apresentação sobre fisiologia do sono em Salvador, o estudante Igor tenta explicar aos colegas por que sentimos sono principalmente à noite, mesmo que tenhamos ficado acordados o dia inteiro sem grande esforço físico. Ele recorre ao modelo de dois processos apresentado na disciplina. Segundo esse modelo, o que representam o processo homeostático (Processo S) e o processo circadiano (Processo C), respectivamente?",
    "options": [
      {
        "letter": "A",
        "text": "O Processo S depende do acúmulo progressivo de adenosina ao longo da vigília, criando propensão ao sono; o Processo C é regulado por um sistema molecular endógeno de cerca de 24 horas, sincronizado principalmente pela luz ambiental via núcleo supraquiasmático (NSQ).",
        "rationale": "CORRETA. O sono resulta da interação entre esses dois processos: no Processo S, a adenosina se acumula progressivamente ao longo da vigília; o Processo C é regulado pelo NSQ (\"relógio-mestre\"), que recebe informação luminosa da retina e regula a secreção de melatonina pela glândula pineal, rapidamente inibida pela luz — em especial a luz azul de telas e LEDs."
      },
      {
        "letter": "B",
        "text": "O Processo S é regulado pela luz ambiental; o Processo C depende do acúmulo de melatonina ao longo da vigília.",
        "rationale": "Incorreta. A relação está invertida: é o Processo C que é sincronizado pela luz ambiental (via NSQ e melatonina), enquanto o Processo S depende do acúmulo de adenosina."
      },
      {
        "letter": "C",
        "text": "Ambos os processos dependem exclusivamente da temperatura corporal, sem relação com neurotransmissores ou luz.",
        "rationale": "Incorreta. A alimentação, a temperatura ambiente, a atividade física e a interação social funcionam apenas como Zeitgebers auxiliares do Processo C; a luz é o principal sincronizador, e o Processo S depende da adenosina."
      },
      {
        "letter": "D",
        "text": "O Processo S é fixo e imutável ao longo da vida; o Processo C depende exclusivamente da alimentação.",
        "rationale": "Incorreta. Nenhum dos dois processos é descrito dessa forma; o Processo S varia com o tempo de vigília acumulado, e o Processo C depende principalmente da luz (Zeitgeber principal), não exclusivamente da alimentação."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Modelo de dois processos: Processo S (homeostático — acúmulo de adenosina durante a vigília) e Processo C (circadiano — regulado pelo núcleo supraquiasmático, sincronizado principalmente pela luz, que inibe a secreção de melatonina pineal)."
  },
  {
    "id": 68,
    "code": "SONO-02",
    "category": "Sono",
    "subcategory": "Neuroquímica: sistemas que promovem o sono",
    "difficulty": "Avançada",
    "prompt": "Durante uma discussão sobre neuroquímica do sono em uma aula de revisão em Feira de Santana, os estudantes tentam montar um mapa de quais substâncias \"ligam\" e quais \"desligam\" o cérebro para o sono, e se confundem sobre o papel específico da hipocretina/orexina nesse processo. Em relação à neuroquímica do sono, apresentada na disciplina, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "A hipocretina/orexina, produzida no hipotálamo lateral, promove o sono; sua deficiência causaria insônia grave.",
        "rationale": "Incorreta. A hipocretina/orexina promove e estabiliza a VIGÍLIA (não o sono); sua deficiência é o mecanismo central da narcolepsia tipo 1, que cursa com sonolência excessiva, não insônia."
      },
      {
        "letter": "B",
        "text": "O GABA, atuando no núcleo pré-óptico ventrolateral do hipotálamo anterior, funciona como o \"interruptor\" que inibe os sistemas de vigília, promovendo o sono.",
        "rationale": "CORRETA. O GABA, nesse núcleo, é descrito exatamente como o \"interruptor\" que inibe os sistemas promotores de vigília (histamina, acetilcolina, hipocretina, dopamina/noradrenalina/serotonina do SRAA); a adenosina (que se acumula ao longo da vigília) e a melatonina (que sincroniza o ritmo circadiano) também promovem o sono."
      },
      {
        "letter": "C",
        "text": "A histamina do núcleo tuberomamilar promove o sono, sendo inibida durante a vigília.",
        "rationale": "Incorreta. A histamina do núcleo tuberomamilar é um sistema que promove a VIGÍLIA, e não o sono."
      },
      {
        "letter": "D",
        "text": "A adenosina se dissipa progressivamente ao longo da vigília, reduzindo a propensão ao sono.",
        "rationale": "Incorreta. A relação é inversa: a adenosina se ACUMULA progressivamente ao longo da vigília, aumentando (e não reduzindo) a propensão ao sono — essa é a base do processo homeostático (Processo S)."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Sistemas que promovem a vigília: histamina, acetilcolina, hipocretina/orexina, dopamina/noradrenalina/serotonina (SRAA). Sistemas que promovem o sono: GABA (o \"interruptor\"), adenosina (acumula na vigília) e melatonina (sincroniza o ritmo circadiano)."
  },
  {
    "id": 69,
    "code": "SONO-03",
    "category": "Sono",
    "subcategory": "Estágios do sono: N2, fusos e complexos K",
    "difficulty": "Intermediária",
    "prompt": "Analisando o traçado de uma polissonografia em um laboratório do sono de Salvador, o técnico aponta para o monitor e diz ao residente: \"Esse é o estágio que domina a maior parte da noite — repare nos fusos do sono e nos complexos K.\" Em relação aos estágios do sono (NREM e REM), apresentados na disciplina, assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "O estágio N2 representa cerca de 45-55% do tempo total de sono e é caracterizado, ao eletroencefalograma, por fusos do sono e complexos K.",
        "rationale": "CORRETA. O estágio N2 (NREM) corresponde à maior parte do sono (45-55%) e representa a fase de consolidação, caracterizada eletrograficamente por fusos do sono e complexos K — os dois marcadores gráficos característicos desse estágio."
      },
      {
        "letter": "B",
        "text": "O sono REM representa a maior parte do tempo total de sono em adultos jovens, correspondendo a 45-55% da noite.",
        "rationale": "Incorreta. O sono REM corresponde a apenas 20-25% do tempo total de sono; é o estágio N2 (NREM) que representa a maior parte, com 45-55%."
      },
      {
        "letter": "C",
        "text": "O estágio N3 é caracterizado por atividade cortical dessincronizada e atonia muscular.",
        "rationale": "Incorreta. Atividade cortical dessincronizada e atonia muscular são características do sono REM, não do estágio N3 (sono de ondas lentas, profundo e restaurador)."
      },
      {
        "letter": "D",
        "text": "Durante o sono REM predomina atividade parassimpática, com redução da pressão arterial e da frequência cardíaca.",
        "rationale": "Incorreta. É durante o sono NREM que predomina atividade parassimpática (redução de PA, FC e débito cardíaco); no sono REM há elevação da atividade simpática (aumento de PA e FC)."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Estágios do sono: N1 (3-8%, transição); N2 (45-55%, fusos do sono e complexos K); N3 (15-23%, ondas lentas, sono profundo/restaurador); REM (20-25%, atividade cortical dessincronizada, atonia muscular, sonhos vívidos, predomínio simpático)."
  },
  {
    "id": 70,
    "code": "SONO-04",
    "category": "Sono",
    "subcategory": "Transtorno de insônia: diagnóstico clínico",
    "difficulty": "Intermediária",
    "prompt": "Adriana, 39 anos, relata em consulta em Vitória da Conquista dificuldade para iniciar o sono e despertares noturnos frequentes há 4 meses, ocorrendo pelo menos 4 noites por semana, mesmo indo para a cama no mesmo horário todos os dias e em um ambiente que ela descreve como \"tranquilo e escuro\". Ela relata fadiga diurna significativa e já pesquisou por conta própria se precisaria fazer uma polissonografia para confirmar o diagnóstico. Qual é a conduta apropriada quanto à confirmação diagnóstica do transtorno de insônia?",
    "options": [
      {
        "letter": "A",
        "text": "É obrigatória a realização de polissonografia para confirmar o diagnóstico de transtorno de insônia.",
        "rationale": "Incorreta. O diagnóstico de insônia é essencialmente clínico; a polissonografia NÃO é indicada de rotina para sua confirmação — diferentemente do que ocorre na apneia obstrutiva do sono."
      },
      {
        "letter": "B",
        "text": "O transtorno de insônia é diagnóstico clínico, baseado na natureza subjetiva do sintoma; a polissonografia NÃO é indicada de rotina para sua confirmação.",
        "rationale": "CORRETA. O quadro descrito preenche os critérios diagnósticos do DSM-5-TR (dificuldade para iniciar/manter o sono, ≥3 noites/semana, por ≥3 meses, com oportunidade adequada para dormir e prejuízo funcional). O diagnóstico tem natureza subjetiva e é exclusivamente clínico."
      },
      {
        "letter": "C",
        "text": "É necessária a realização de actigrafia por pelo menos 4 semanas antes de qualquer conduta terapêutica.",
        "rationale": "Incorreta. A actigrafia é útil para avaliar ritmo circadiano e resposta ao tratamento em situações específicas, mas não é exigência diagnóstica de rotina para a insônia."
      },
      {
        "letter": "D",
        "text": "O diagnóstico exige obrigatoriamente teste de latências múltiplas do sono (TLMS).",
        "rationale": "Incorreta. O TLMS é utilizado para diferenciar narcolepsia de hipersonia idiopática, não fazendo parte da investigação diagnóstica de rotina da insônia."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "O transtorno de insônia é diagnóstico exclusivamente clínico (dificuldade de início/manutenção do sono ou despertar precoce, ≥3 noites/semana por ≥3 meses, com prejuízo funcional) — a polissonografia NÃO é indicada de rotina."
  },
  {
    "id": 71,
    "code": "SONO-05",
    "category": "Sono",
    "subcategory": "Modelo 3P de Spielman: fatores perpetuadores",
    "difficulty": "Avançada",
    "prompt": "Roberval, 45 anos, desenvolveu insônia há dois anos, logo após um período de grande estresse no trabalho que já foi resolvido há meses, mas o problema de sono persiste em Feira de Santana. Ao investigar a rotina dele, o psiquiatra descobre que ele passa cerca de 10 horas na cama todas as noites tentando dormir, mesmo quando sabe que não vai conseguir, na esperança de que \"em algum momento o sono vem\". Qual das alternativas abaixo exemplifica um fator PERPETUADOR (e não predisponente ou precipitante) da insônia de Roberval, segundo o modelo 3P de Spielman?",
    "options": [
      {
        "letter": "A",
        "text": "Tendência à ruminação e hiperalerta, presentes como características psicológicas prévias do paciente.",
        "rationale": "Incorreta. Essa é uma característica de vulnerabilidade prévia, correspondendo a um fator PREDISPONENTE (fator psicológico), não a um fator perpetuador."
      },
      {
        "letter": "B",
        "text": "Início de um evento estressante, como uma perda ou uma ruptura recente.",
        "rationale": "Incorreta. Eventos de vida estressantes que desencadeiam o episódio agudo de insônia correspondem a fatores PRECIPITANTES, não perpetuadores."
      },
      {
        "letter": "C",
        "text": "Prática de permanecer excessivamente no leito mesmo quando acordado, mantendo o ciclo de insônia mesmo após a resolução do fator precipitante inicial.",
        "rationale": "CORRETA. Fatores perpetuadores são práticas não relacionadas ao sono no quarto, a tendência a permanecer na cama quando acordado, e a permanência excessiva no leito — mantendo e cronificando a insônia mesmo depois que o fator precipitante original já foi resolvido."
      },
      {
        "letter": "D",
        "text": "Metabolismo basal elevado, como característica biológica prévia do paciente.",
        "rationale": "Incorreta. Características biológicas prévias (metabolismo basal elevado, hiperalerta, alterações em neurotransmissores) correspondem a fatores PREDISPONENTES, não perpetuadores."
      }
    ],
    "correctLetter": "C",
    "clinicalPointers": "Modelo 3P de Spielman: Predisponentes (biológicos/psicológicos/sociais, vulnerabilidade prévia); Precipitantes (eventos estressantes, doenças, que desencadeiam o episódio agudo); Perpetuadores (comportamentos como permanência excessiva no leito, que cronificam a insônia mesmo após resolução do fator inicial)."
  },
  {
    "id": 72,
    "code": "SONO-06",
    "category": "Sono",
    "subcategory": "TCC-i como tratamento de primeira escolha",
    "difficulty": "Intermediária",
    "prompt": "Denise, 42 anos, com insônia crônica há mais de um ano, já tentou sozinha diversas medidas de higiene do sono (reduzir cafeína, escurecer o quarto, evitar telas à noite) sem melhora significativa, e é encaminhada para tratamento especializado em Salvador. Segundo as principais diretrizes internacionais citadas na disciplina, qual é o tratamento de primeira escolha para a insônia persistente de Denise?",
    "options": [
      {
        "letter": "A",
        "text": "Benzodiazepínicos em uso contínuo e prolongado, por tempo indeterminado.",
        "rationale": "Incorreta. A recomendação geral é não ultrapassar 2-4 semanas de uso contínuo de hipnótico; o uso benzodiazepínico prolongado não é o tratamento de primeira escolha recomendado pelas diretrizes."
      },
      {
        "letter": "B",
        "text": "Terapia cognitivo-comportamental para insônia (TCC-i), incluindo restrição de sono, controle de estímulos, técnicas de relaxamento e reestruturação cognitiva.",
        "rationale": "CORRETA. A TCC-i é recomendada como tratamento de primeira escolha para insônia persistente pelas principais diretrizes internacionais, combinando restrição de sono (modelo de Spielman), controle de estímulos (modelo de Bootzin), técnicas de relaxamento e intervenções cognitivas/psicoeducação (modelo de Aaron Beck)."
      },
      {
        "letter": "C",
        "text": "Antipsicóticos atípicos em baixa dose, pelo efeito sedativo.",
        "rationale": "Incorreta. Antipsicóticos e anti-histamínicos não são apropriados para insônia primária, pelo risco de efeitos anticolinérgicos, sedação excessiva e quedas, especialmente em idosos."
      },
      {
        "letter": "D",
        "text": "Melatonina exógena isoladamente, por ser considerada opção \"natural\" e eficaz de primeira linha.",
        "rationale": "Incorreta. A eficácia da melatonina exógena para insônia é controversa; diversos ensaios e diretrizes de consenso não sustentam seu uso como tratamento de primeira linha, apesar da percepção popular de eficácia."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "TCC-i (restrição de sono, controle de estímulos, técnicas de relaxamento, reestruturação cognitiva e psicoeducação) é o tratamento de primeira escolha para insônia persistente. Hipnóticos: não ultrapassar 2-4 semanas de uso contínuo; eficácia da melatonina é controversa."
  },
  {
    "id": 73,
    "code": "SONO-07",
    "category": "Sono",
    "subcategory": "AOS: fisiopatologia (obstrutiva x central)",
    "difficulty": "Intermediária",
    "prompt": "Ao explicar a um grupo de estudantes de Feira de Santana por que o parceiro de cama de um paciente com apneia relata vê-lo \"lutando para respirar\" durante os episódios noturnos, apesar do ar não passar, o professor destaca o que ocorre com o esforço respiratório torácico e abdominal nesse momento. Em relação à fisiopatologia da apneia obstrutiva do sono (AOS), assinale a alternativa correta:",
    "options": [
      {
        "letter": "A",
        "text": "Na apneia obstrutiva, o esforço respiratório torácico/abdominal continua durante o evento, mas o fluxo de ar cessa pela perda de patência da via aérea superior; na apneia central, o esforço respiratório está reduzido ou ausente.",
        "rationale": "CORRETA. Essa é a distinção fisiopatológica central e um item clássico de prova: a AOS caracteriza-se por obstrução repetitiva (completa ou parcial) da via aérea superior durante o sono, apesar da continuidade dos esforços respiratórios; um episódio de apneia é definido como cessação do fluxo aéreo por 10 segundos ou mais."
      },
      {
        "letter": "B",
        "text": "Na apneia obstrutiva, o esforço respiratório está sempre ausente durante o evento, de forma idêntica à apneia central.",
        "rationale": "Incorreta. Essa descrição corresponde à apneia central, não à obstrutiva, na qual o esforço respiratório CONTINUA, apenas o fluxo de ar cessa."
      },
      {
        "letter": "C",
        "text": "A apneia central é definida por obstrução mecânica da via aérea superior, com esforço respiratório mantido.",
        "rationale": "Incorreta. Essa descrição corresponde à apneia obstrutiva; na apneia central, o esforço respiratório está reduzido ou ausente, sem relação com obstrução mecânica da via aérea."
      },
      {
        "letter": "D",
        "text": "Não há diferença fisiopatológica relevante entre apneia obstrutiva e apneia central.",
        "rationale": "Incorreta. Há uma distinção fisiopatológica central e clinicamente relevante entre os dois tipos, relacionada à presença ou ausência de esforço respiratório durante o evento."
      }
    ],
    "correctLetter": "A",
    "clinicalPointers": "Item clássico de prova: na apneia OBSTRUTIVA, o esforço respiratório torácico/abdominal CONTINUA (só o fluxo cessa); na apneia CENTRAL, o esforço respiratório está reduzido ou ausente. Apneia = cessação do fluxo por ≥10s; hipopneia = redução (não cessação) do fluxo, com dessaturação e/ou despertar."
  },
  {
    "id": 74,
    "code": "SONO-08",
    "category": "Sono",
    "subcategory": "Gravidade da AOS pelo IAH",
    "difficulty": "Intermediária",
    "prompt": "Edmilson, 50 anos, com queixa de ronco alto e sonolência diurna, é submetido à polissonografia em uma clínica do sono de Salvador, que revela índice de apneia-hipopneia (IAH) de 22 eventos por hora de sono. Segundo a classificação de gravidade da apneia obstrutiva do sono apresentada na disciplina, qual é a classificação correspondente ao resultado de Edmilson?",
    "options": [
      {
        "letter": "A",
        "text": "Leve.",
        "rationale": "Incorreta. A classificação leve corresponde a IAH de 5 a 15 eventos/hora, faixa inferior ao valor apresentado."
      },
      {
        "letter": "B",
        "text": "Moderada.",
        "rationale": "CORRETA. O índice de apneia-hipopneia (IAH) — número de eventos respiratórios obstrutivos por hora de sono — classifica a AOS como moderada na faixa de 16 a 30 eventos/hora; o valor de 22 eventos/hora do paciente se encaixa exatamente nessa faixa."
      },
      {
        "letter": "C",
        "text": "Grave.",
        "rationale": "Incorreta. A classificação grave corresponde a IAH acima de 30 eventos/hora, valor superior ao apresentado pelo paciente."
      },
      {
        "letter": "D",
        "text": "Não há eventos suficientes para caracterizar AOS.",
        "rationale": "Incorreta. Um IAH de 22 eventos/hora já caracteriza AOS (o limiar mínimo geral é de 5 eventos/hora associados a sintomas, ou 15 eventos/hora isoladamente), na faixa moderada."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Gravidade da AOS pelo IAH: 5 a 15 eventos/hora = leve; 16 a 30 = moderada; acima de 30 = grave. A gravidade objetiva (IAH) nem sempre se correlaciona diretamente com a intensidade dos sintomas subjetivos."
  },
  {
    "id": 75,
    "code": "SONO-09",
    "category": "Sono",
    "subcategory": "Narcolepsia: deficiência de hipocretina",
    "difficulty": "Avançada",
    "prompt": "Yago, 19 anos, estudante, procura atendimento em Ilhéus relatando episódios diários de sonolência irreprimível ao longo do dia, mesmo dormindo bem à noite. Relata também que, ao rir de uma piada com os amigos, chegou a sentir as pernas \"falharem\" de repente e quase caiu, mantendo-se plenamente consciente durante o episódio. Qual achado, se identificado no líquido cerebrospinal de Yago, confirmaria de forma mais específica o diagnóstico de narcolepsia tipo 1?",
    "options": [
      {
        "letter": "A",
        "text": "Elevação de proteína tau.",
        "rationale": "Incorreta. A elevação de proteína tau é achado associado a processos neurodegenerativos (como doença de Alzheimer), não à narcolepsia."
      },
      {
        "letter": "B",
        "text": "Deficiência de hipocretina (orexina), decorrente da perda dos neurônios hipocretinérgicos hipotalâmicos.",
        "rationale": "CORRETA. O quadro de sonolência irreprimível associada a cataplexia (perda súbita do tônus muscular desencadeada por emoção positiva, com consciência preservada) é característico da narcolepsia tipo 1; segundo os critérios diagnósticos do DSM-5-TR, um dos elementos adicionais que confirma o diagnóstico é justamente a deficiência de hipocretina no líquido cerebrospinal."
      },
      {
        "letter": "C",
        "text": "Elevação de beta-amiloide.",
        "rationale": "Incorreta. A elevação de beta-amiloide é achado associado a processos neurodegenerativos, como a doença de Alzheimer, não à narcolepsia."
      },
      {
        "letter": "D",
        "text": "Elevação de proteína 14-3-3.",
        "rationale": "Incorreta. A elevação de proteína 14-3-3 no líquido cerebrospinal é achado associado a doenças priônicas, como a doença de Creutzfeldt-Jakob, não à narcolepsia."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Critérios do DSM-5-TR para narcolepsia: necessidade irreprimível de dormir ≥3x/semana por ≥3 meses, associada a pelo menos 1 de: (1) cataplexia; (2) deficiência de hipocretina no líquido cerebrospinal; (3) latência REM ≤15 min na PSG OU latência média ≤8 min com ≥2 SOREMP no TLMS."
  },
  {
    "id": 76,
    "code": "SONO-10",
    "category": "Sono",
    "subcategory": "Síndrome das pernas inquietas: investigação do ferro",
    "difficulty": "Intermediária",
    "prompt": "Conceição, 48 anos, cozinheira, relata em consulta em Feira de Santana uma sensação desagradável de formigamento profundo nas pernas, associada a uma urgência quase incontrolável de movimentá-las, que piora sempre que ela se senta para descansar à noite e melhora quando ela se levanta para caminhar pela casa. Antes de iniciar tratamento farmacológico dopaminérgico para a síndrome das pernas inquietas de Conceição, qual investigação inicial é mais importante?",
    "options": [
      {
        "letter": "A",
        "text": "Polissonografia obrigatória para confirmação diagnóstica.",
        "rationale": "Incorreta. O diagnóstico da síndrome das pernas inquietas é clínico, baseado em critérios comportamentais característicos (urgência de movimentar as pernas, piora no repouso/à noite, alívio com movimento), não exigindo polissonografia de rotina."
      },
      {
        "letter": "B",
        "text": "Avaliação do metabolismo do ferro (ferritina), já que a deficiência de ferro é fator de risco tratável associado à síndrome das pernas inquietas.",
        "rationale": "CORRETA. A avaliação do metabolismo do ferro é etapa fundamental na investigação inicial, já que a deficiência de ferro é fator de risco tratável para a síndrome das pernas inquietas; em casos leves a moderados associados a deficiência de ferro, a reposição pode ser suficiente antes de se considerar o tratamento dopaminérgico, que carrega risco de complicação específica (aumentação)."
      },
      {
        "letter": "C",
        "text": "Dosagem de hipocretina no líquido cerebrospinal.",
        "rationale": "Incorreta. A dosagem de hipocretina relaciona-se à investigação da narcolepsia, não da síndrome das pernas inquietas."
      },
      {
        "letter": "D",
        "text": "Eletroencefalograma de rotina.",
        "rationale": "Incorreta. O EEG não é exame de rotina indicado na investigação inicial da síndrome das pernas inquietas."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "SPI: investigação inicial deve incluir avaliação do metabolismo do ferro (ferritina), fator de risco tratável. Tratamento: α2δ-ligantes (gabapentina/pregabalina) preferenciais; agonistas dopaminérgicos (pramipexol/ropinirol/rotigotina) com risco de aumentação; benzodiazepínicos não recomendados de rotina."
  },
  {
    "id": 77,
    "code": "SONO-11",
    "category": "Sono",
    "subcategory": "Relação bidirecional sono-saúde mental (integração geral)",
    "difficulty": "Avançada",
    "prompt": "Encerrando a aula de Transtornos do Sono-Vigília em Salvador, o professor retoma casos discutidos ao longo de toda a disciplina de Saúde Mental — como o de um paciente com quadro depressivo que piorou após meses de insônia mal tratada, e o de uma criança cuja desatenção melhorou assim que sua privação de sono foi corrigida — para explicar como o sono se relaciona com os demais transtornos mentais. Segundo essas considerações finais, a relação entre os transtornos do sono e os demais transtornos mentais é melhor descrita como:",
    "options": [
      {
        "letter": "A",
        "text": "Unidirecional: os transtornos do sono são sempre consequência de outro transtorno mental, nunca sua causa ou fator de agravamento.",
        "rationale": "Incorreta. A relação não é unidirecional; os transtornos do sono podem funcionar tanto como causa quanto como consequência de outros transtornos mentais."
      },
      {
        "letter": "B",
        "text": "Bidirecional: os transtornos do sono podem funcionar como causa, consequência ou fator de manutenção/agravamento de outros transtornos mentais, devendo ser tratados especificamente, e não apenas como sintoma secundário.",
        "rationale": "CORRETA. A aula é explícita: os transtornos do sono-vigília mantêm relação bidirecional com praticamente todos os transtornos mentais, incluindo a evidência de que a insônia preexistente eleva o risco de desenvolvimento ou recidiva de depressão. Esse mesmo princípio aparece de forma transversal na disciplina — por exemplo, na aula de TDAH, a privação/má qualidade do sono é descrita como causa reversível capaz de mimetizar desatenção e agitação."
      },
      {
        "letter": "C",
        "text": "Inexistente: não há relação cientificamente estabelecida entre sono e saúde mental.",
        "rationale": "Incorreta. A aula descreve extensa evidência de relação entre sono e regulação emocional, cognição, metabolismo e imunidade, contrariando essa afirmação."
      },
      {
        "letter": "D",
        "text": "Restrita exclusivamente à insônia, sem qualquer relação de outros transtornos do sono com a saúde mental.",
        "rationale": "Incorreta. A relação bidirecional é descrita para os transtornos do sono-vigília de forma geral, não restrita apenas à insônia."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Os transtornos do sono-vigília mantêm relação bidirecional com praticamente todos os transtornos mentais (causa, consequência ou fator de manutenção/agravamento) e devem ser tratados especificamente — tema que conecta a aula de Sono às de Humor, TDAH e Transtornos Alimentares."
  },
  {
    "id": 78,
    "code": "INTRO-12",
    "category": "Introducao",
    "subcategory": "Definição e papel da anamnese",
    "difficulty": "Intermediária",
    "prompt": "Durante a supervisão de um atendimento em Feira de Santana, a preceptora pergunta ao interno Bruno por que ele insiste em ouvir toda a história do paciente, incluindo detalhes que parecem não ter relação direta com a queixa, antes de sequer cogitar hipóteses diagnósticas. Bruno responde que, em Psiquiatria, muitas vezes não há exame que confirme o diagnóstico, e que a própria história bem contada já aponta o caminho. Segundo a definição de anamnese apresentada na disciplina, qual afirmação melhor explica esse raciocínio, especialmente em Saúde Mental?",
    "options": [
      {
        "letter": "A",
        "text": "A anamnese é apenas um formulário burocrático, sem relação direta com o raciocínio diagnóstico.",
        "rationale": "Incorreta. A anamnese é descrita como a base de todo o raciocínio diagnóstico, permitindo formular hipóteses antes mesmo do exame físico ou complementar — não é um mero formulário burocrático."
      },
      {
        "letter": "B",
        "text": "A anamnese é a reconstrução organizada da história de saúde do paciente, obtida pela entrevista clínica, e é a base de todo o raciocínio diagnóstico; em Saúde Mental, ganha papel ainda mais central, sendo em grande parte a própria ferramenta diagnóstica.",
        "rationale": "CORRETA. Essa é exatamente a definição apresentada na disciplina: a anamnese organiza, em sequência lógica, tudo o que o paciente relata sobre si — queixa, história e contexto de vida — permitindo formular hipóteses diagnósticas. Em Saúde Mental, ela ganha papel ainda mais central, pois não há exame confirmatório para a maioria dos transtornos mentais."
      },
      {
        "letter": "C",
        "text": "A anamnese só é necessária quando os exames complementares não estão disponíveis no serviço.",
        "rationale": "Incorreta. A anamnese é central independentemente da disponibilidade de exames complementares — em Saúde Mental, ela é, em grande parte, a própria ferramenta diagnóstica."
      },
      {
        "letter": "D",
        "text": "Em Saúde Mental, a anamnese tem papel secundário, sendo o exame físico o elemento central do diagnóstico.",
        "rationale": "Incorreta. É o contrário: em Saúde Mental, a anamnese tem papel ainda mais central do que em outras áreas da Medicina, dado que o diagnóstico psiquiátrico é essencialmente clínico."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "A anamnese é a reconstrução organizada da história de saúde do paciente, obtida pela entrevista clínica — base de todo o raciocínio diagnóstico. Em Saúde Mental, é em grande parte a própria ferramenta diagnóstica: \"a história bem contada é metade do diagnóstico\"."
  },
  {
    "id": 79,
    "code": "INTRO-13",
    "category": "Introducao",
    "subcategory": "Atitudes essenciais na relação médico-paciente",
    "difficulty": "Intermediária",
    "prompt": "No primeiro atendimento a Dona Neuza, 70 anos, visivelmente desconfiada e pouco à vontade, o médico residente em Vitória da Conquista evita pressa, trata-a com respeito e paciência, fala com clareza e demonstra interesse genuíno pelo que ela relata, mesmo diante de uma consulta que se estende além do previsto. Ao final, Dona Neuza, antes reticente, já conversa abertamente sobre seus sintomas. Segundo a disciplina, qual é o papel dessas atitudes essenciais na entrevista psiquiátrica, ilustrado pela mudança de postura de Dona Neuza?",
    "options": [
      {
        "letter": "A",
        "text": "São gestos apenas protocolares, sem impacto real no resultado da consulta.",
        "rationale": "Incorreta. Essas atitudes são descritas como princípios simples, mas decisivos, para o desfecho da relação terapêutica — não como formalidades sem efeito prático."
      },
      {
        "letter": "B",
        "text": "São princípios simples, mas decisivos: constroem — ou, quando ausentes, comprometem — o vínculo desde o primeiro contato com o paciente.",
        "rationale": "CORRETA. A disciplina lista respeito, paciência, cordialidade, empatia, muita educação, falar com clareza e ter interesse genuíno como atitudes essenciais, descrevendo-as exatamente dessa forma: princípios simples, mas decisivos, que constroem ou comprometem o vínculo desde o primeiro contato com o paciente."
      },
      {
        "letter": "C",
        "text": "Só são necessárias quando o paciente já demonstra confiança no médico.",
        "rationale": "Incorreta. É justamente no primeiro contato — antes de qualquer confiança estabelecida — que essas atitudes são mais decisivas para construir o vínculo."
      },
      {
        "letter": "D",
        "text": "Devem ser reservadas a pacientes com quadros psiquiátricos graves, sendo dispensáveis nos demais casos.",
        "rationale": "Incorreta. Essas atitudes são apresentadas como fundamento de toda entrevista psiquiátrica, independentemente da gravidade do quadro clínico."
      }
    ],
    "correctLetter": "B",
    "clinicalPointers": "Atitudes essenciais na relação médico-paciente: respeito, paciência, cordialidade, empatia, muita educação, falar com clareza, ter interesse genuíno — constroem (ou, se ausentes, comprometem) o vínculo desde o primeiro contato."
  }
];

    const CATEGORY_LABELS = {
  "Introducao": "Introdução à Saúde Mental",
  "Delirium": "Delirium",
  "Esquizofrenia": "Esquizofrenia",
  "TEA": "Transtorno do Espectro Autista",
  "TDAH": "TDAH",
  "Alimentares": "Transtornos Alimentares",
  "Sono": "Transtornos do Sono-Vigília"
};

    let currentQuestions = [];
    let currentIndex = 0;
    let userAnswers = {};
    let flaggedQuestions = new Set();
    let quizMode = 'exam';
    let timerInterval = null;
    let secondsElapsed = 0;
    let isQuizSubmitted = false;

    // DOM References
    const startScreen = document.getElementById('startScreen');
    const quizScreen = document.getElementById('quizScreen');
    const resultsScreen = document.getElementById('resultsScreen');
    const quizMetaNav = document.getElementById('quizMetaNav');
    const timerDisplay = document.getElementById('timerDisplay');
    const progressPill = document.getElementById('progressPill');
    const progressBar = document.getElementById('progressBar');
    const labelQuestionNumber = document.getElementById('labelQuestionNumber');
    const questionPillPalette = document.getElementById('questionPillPalette');
    const badgeTheme = document.getElementById('badgeTheme');
    const badgeDifficulty = document.getElementById('badgeDifficulty');
    const questionCode = document.getElementById('questionCode');
    const questionPrompt = document.getElementById('questionPrompt');
    const optionsContainer = document.getElementById('optionsContainer');
    const immediateFeedbackBox = document.getElementById('immediateFeedbackBox');
    const btnPrevQuestion = document.getElementById('btnPrevQuestion');
    const btnNextQuestion = document.getElementById('btnNextQuestion');
    const btnFlagQuestion = document.getElementById('btnFlagQuestion');
    const flagIcon = document.getElementById('flagIcon');
    const flagText = document.getElementById('flagText');
    const btnFinishEarly = document.getElementById('btnFinishEarly');
    const btnStartQuiz = document.getElementById('btnStartQuiz');

    const labelModeExam = document.getElementById('labelModeExam');
    const labelModeTutor = document.getElementById('labelModeTutor');

    labelModeExam.addEventListener('click', () => {
      labelModeExam.classList.add('border-indigoBrand-600', 'bg-indigoBrand-50/40');
      labelModeExam.classList.remove('border-slate-200', 'bg-white');
      labelModeTutor.classList.remove('border-indigoBrand-600', 'bg-indigoBrand-50/40');
      labelModeTutor.classList.add('border-slate-200', 'bg-white');
      quizMode = 'exam';
    });

    labelModeTutor.addEventListener('click', () => {
      labelModeTutor.classList.add('border-indigoBrand-600', 'bg-indigoBrand-50/40');
      labelModeTutor.classList.remove('border-slate-200', 'bg-white');
      labelModeExam.classList.remove('border-indigoBrand-600', 'bg-indigoBrand-50/40');
      labelModeExam.classList.add('border-slate-200', 'bg-white');
      quizMode = 'tutor';
    });

    btnStartQuiz.addEventListener('click', () => {
      const topic = document.getElementById('topicFilter').value;

      let filtered = [...QUESTIONS_DATABASE];
      if (topic !== 'all') {
        filtered = QUESTIONS_DATABASE.filter(q => q.category === topic);
      }

      currentQuestions = filtered.sort(() => Math.random() - 0.5);

      currentIndex = 0;
      userAnswers = {};
      flaggedQuestions.clear();
      secondsElapsed = 0;
      isQuizSubmitted = false;

      clearInterval(timerInterval);
      timerInterval = setInterval(() => {
        secondsElapsed++;
        const mins = String(Math.floor(secondsElapsed / 60)).padStart(2, '0');
        const secs = String(secondsElapsed % 60).padStart(2, '0');
        timerDisplay.textContent = `${mins}:${secs}`;
      }, 1000);

      startScreen.classList.add('hidden');
      resultsScreen.classList.add('hidden');
      quizScreen.classList.remove('hidden');
      quizMetaNav.classList.remove('hidden');

      renderPalette();
      loadQuestion(currentIndex);
    });

    function renderPalette() {
      questionPillPalette.innerHTML = '';
      currentQuestions.forEach((q, idx) => {
        const btn = document.createElement('button');
        btn.id = `pill-btn-${idx}`;
        btn.className = `w-7 h-7 rounded-lg text-xs font-bold transition-all flex items-center justify-center border ${
          idx === currentIndex
            ? 'ring-2 ring-indigoBrand-500 border-indigoBrand-600 bg-indigoBrand-600 text-white'
            : 'border-slate-200 bg-white text-slate-700 hover:bg-slate-100'
        }`;
        btn.textContent = idx + 1;
        btn.addEventListener('click', () => {
          currentIndex = idx;
          loadQuestion(currentIndex);
        });
        questionPillPalette.appendChild(btn);
      });
      updatePaletteStatus();
    }

    function updatePaletteStatus() {
      currentQuestions.forEach((q, idx) => {
        const pill = document.getElementById(`pill-btn-${idx}`);
        if (!pill) return;

        const isAnswered = userAnswers[q.id] !== undefined;
        const isFlagged = flaggedQuestions.has(q.id);
        const isCurrent = idx === currentIndex;

        if (isCurrent) {
          pill.className = 'w-7 h-7 rounded-lg text-xs font-bold transition-all flex items-center justify-center border ring-2 ring-indigoBrand-500 border-indigoBrand-600 bg-indigoBrand-600 text-white shadow-sm';
        } else if (isFlagged) {
          pill.className = 'w-7 h-7 rounded-lg text-xs font-bold transition-all flex items-center justify-center border border-amber-400 bg-amber-100 text-amber-800';
        } else if (isAnswered) {
          pill.className = 'w-7 h-7 rounded-lg text-xs font-bold transition-all flex items-center justify-center border border-emerald-300 bg-emerald-100 text-emerald-800';
        } else {
          pill.className = 'w-7 h-7 rounded-lg text-xs font-bold transition-all flex items-center justify-center border border-slate-200 bg-white text-slate-700 hover:bg-slate-100';
        }
      });
    }

    function loadQuestion(idx) {
      const q = currentQuestions[idx];
      const total = currentQuestions.length;

      labelQuestionNumber.textContent = `Questao ${idx + 1} de ${total}`;
      progressPill.textContent = `Questao ${idx + 1}/${total}`;
      const pct = ((idx + 1) / total) * 100;
      progressBar.style.width = `${pct}%`;

      const catLabel = CATEGORY_LABELS[q.category] || q.category;
      badgeTheme.textContent = `${catLabel.toUpperCase()} - ${q.subcategory}`;
      badgeDifficulty.textContent = q.difficulty;
      questionCode.textContent = q.code;
      questionPrompt.textContent = q.prompt;

      if (flaggedQuestions.has(q.id)) {
        flagIcon.setAttribute('fill', 'currentColor');
        flagIcon.classList.add('text-amber-500');
        flagText.textContent = 'Marcada para revisao';
        flagText.classList.add('text-amber-600', 'font-bold');
      } else {
        flagIcon.setAttribute('fill', 'none');
        flagIcon.classList.remove('text-amber-500');
        flagText.textContent = 'Marcar para revisar';
        flagText.classList.remove('text-amber-600', 'font-bold');
      }

      btnPrevQuestion.disabled = idx === 0;
      if (idx === total - 1) {
        btnNextQuestion.textContent = 'Finalizar Simulado';
        btnNextQuestion.classList.remove('bg-indigoBrand-600', 'hover:bg-indigoBrand-700');
        btnNextQuestion.classList.add('bg-emerald-600', 'hover:bg-emerald-700');
      } else {
        btnNextQuestion.innerHTML = 'Proxima &rarr;';
        btnNextQuestion.classList.add('bg-indigoBrand-600', 'hover:bg-indigoBrand-700');
        btnNextQuestion.classList.remove('bg-emerald-600', 'hover:bg-emerald-700');
      }

      optionsContainer.innerHTML = '';
      const selected = userAnswers[q.id];

      q.options.forEach(opt => {
        const optionBtn = document.createElement('button');
        optionBtn.className = `w-full text-left p-4 rounded-xl border-2 transition-all flex items-start gap-3.5 ${
          selected === opt.letter
            ? 'border-indigoBrand-600 bg-indigoBrand-50/50 text-slate-900 shadow-sm'
            : 'border-slate-200 bg-white text-slate-700 hover:border-slate-300 hover:bg-slate-50/60'
        }`;

        optionBtn.innerHTML = `
          <span class="w-8 h-8 rounded-lg flex-shrink-0 flex items-center justify-center font-bold text-sm ${
            selected === opt.letter
              ? 'bg-indigoBrand-600 text-white'
              : 'bg-slate-100 text-slate-700 border border-slate-200'
          }">
            ${opt.letter}
          </span>
          <span class="text-sm sm:text-base leading-relaxed pt-0.5">${opt.text}</span>
        `;

        optionBtn.addEventListener('click', () => {
          if (isQuizSubmitted) return;
          userAnswers[q.id] = opt.letter;
          loadQuestion(currentIndex);
          updatePaletteStatus();

          if (quizMode === 'tutor') {
            showTutorFeedback(q);
          }
        });

        optionsContainer.appendChild(optionBtn);
      });

      if (quizMode === 'tutor' && selected) {
        showTutorFeedback(q);
      } else {
        immediateFeedbackBox.classList.add('hidden');
      }

      updatePaletteStatus();
    }

    function showTutorFeedback(q) {
      const selectedLetter = userAnswers[q.id];
      const isCorrect = selectedLetter === q.correctLetter;

      immediateFeedbackBox.classList.remove('hidden');
      immediateFeedbackBox.className = `mt-6 p-5 rounded-xl border ${
        isCorrect ? 'bg-emerald-50 border-emerald-200 text-emerald-900' : 'bg-rose-50 border-rose-200 text-rose-900'
      }`;

      let optionsListHtml = q.options.map(opt => `
        <div class="mt-2 text-xs sm:text-sm pl-3 border-l-2 ${
          opt.letter === q.correctLetter ? 'border-emerald-500 font-medium text-emerald-800' : 'border-slate-300 text-slate-600'
        }">
          <span class="font-bold">${opt.letter}:</span> ${opt.rationale}
        </div>
      `).join('');

      immediateFeedbackBox.innerHTML = `
        <div class="flex items-center gap-2 mb-2 font-bold text-sm sm:text-base">
          ${isCorrect
            ? '<svg class="w-5 h-5 text-emerald-600" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/></svg> Resposta Correta!'
            : '<svg class="w-5 h-5 text-rose-600" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z" clip-rule="evenodd"/></svg> Resposta Incorreta!'}
        </div>
        <p class="text-xs sm:text-sm font-semibold mb-2">Gabarito Oficial: Alternativa ${q.correctLetter}</p>
        <p class="text-xs text-slate-500 italic mb-3">${q.clinicalPointers}</p>
        <div class="space-y-1 mt-2">
          ${optionsListHtml}
        </div>
      `;
    }

    btnPrevQuestion.addEventListener('click', () => {
      if (currentIndex > 0) {
        currentIndex--;
        loadQuestion(currentIndex);
      }
    });

    btnNextQuestion.addEventListener('click', () => {
      if (currentIndex < currentQuestions.length - 1) {
        currentIndex++;
        loadQuestion(currentIndex);
      } else {
        requestFinishQuiz();
      }
    });

    btnFlagQuestion.addEventListener('click', () => {
      const q = currentQuestions[currentIndex];
      if (flaggedQuestions.has(q.id)) {
        flaggedQuestions.delete(q.id);
      } else {
        flaggedQuestions.add(q.id);
      }
      loadQuestion(currentIndex);
    });

    btnFinishEarly.addEventListener('click', () => {
      requestFinishQuiz();
    });

    function requestFinishQuiz() {
      const unanswered = currentQuestions.filter(q => userAnswers[q.id] === undefined).length;
      if (unanswered > 0) {
        document.getElementById('modalMessage').textContent = `Voce ainda tem ${unanswered} questao(oes) sem resposta. Deseja realmente finalizar o simulado agora?`;
        document.getElementById('customModal').classList.remove('hidden');
      } else {
        finishQuiz();
      }
    }

    document.getElementById('btnModalCancel').addEventListener('click', () => {
      document.getElementById('customModal').classList.add('hidden');
    });

    document.getElementById('btnModalConfirm').addEventListener('click', () => {
      document.getElementById('customModal').classList.add('hidden');
      finishQuiz();
    });

    function finishQuiz() {
      clearInterval(timerInterval);
      isQuizSubmitted = true;

      quizScreen.classList.add('hidden');
      quizMetaNav.classList.add('hidden');
      resultsScreen.classList.remove('hidden');

      let correctCount = 0;
      let wrongCount = 0;
      let topicStats = {};

      currentQuestions.forEach(q => {
        const chosen = userAnswers[q.id];
        const isRight = chosen === q.correctLetter;

        if (isRight) correctCount++;
        else wrongCount++;

        if (!topicStats[q.category]) {
          topicStats[q.category] = { total: 0, correct: 0 };
        }
        topicStats[q.category].total++;
        if (isRight) topicStats[q.category].correct++;
      });

      const totalQ = currentQuestions.length;
      const scorePct = Math.round((correctCount / totalQ) * 100);

      document.getElementById('metricScorePercent').textContent = `${scorePct}%`;
      document.getElementById('metricCorrectCount').textContent = correctCount;
      document.getElementById('metricWrongCount').textContent = wrongCount;

      const mins = String(Math.floor(secondsElapsed / 60)).padStart(2, '0');
      const secs = String(secondsElapsed % 60).padStart(2, '0');
      document.getElementById('metricTotalTime').textContent = `${mins}:${secs}`;

      const scoreBadge = document.getElementById('scoreBadgeIcon');
      const summaryText = document.getElementById('scoreFeedbackSummary');

      if (scorePct >= 80) {
        scoreBadge.className = 'w-16 h-16 mx-auto mb-4 rounded-2xl bg-emerald-100 text-emerald-600 flex items-center justify-center font-black text-2xl shadow-inner';
        scoreBadge.textContent = '\ud83c\udfc6';
        summaryText.textContent = "Excelente aproveitamento! Dominio consistente dos 7 assuntos da disciplina de Saude Mental.";
      } else if (scorePct >= 60) {
        scoreBadge.className = 'w-16 h-16 mx-auto mb-4 rounded-2xl bg-indigoBrand-100 text-indigoBrand-600 flex items-center justify-center font-black text-2xl shadow-inner';
        scoreBadge.textContent = '\ud83d\udc4d';
        summaryText.textContent = "Bom resultado! Os conceitos essenciais estao consolidados. Revise os topicos com menor aproveitamento abaixo.";
      } else {
        scoreBadge.className = 'w-16 h-16 mx-auto mb-4 rounded-2xl bg-amber-100 text-amber-600 flex items-center justify-center font-black text-2xl shadow-inner';
        scoreBadge.textContent = '\ud83d\udcda';
        summaryText.textContent = "Revisao recomendada. Priorize os assuntos com menor aproveitamento na lista abaixo antes da proxima tentativa.";
      }

      const topicListContainer = document.getElementById('topicPerformanceList');
      topicListContainer.innerHTML = '';

      for (const [topicKey, stats] of Object.entries(topicStats)) {
        const topicPct = Math.round((stats.correct / stats.total) * 100);
        const item = document.createElement('div');
        item.className = 'bg-slate-50 p-3.5 rounded-xl border border-slate-200 flex flex-col sm:flex-row sm:items-center justify-between gap-2';

        const label = CATEGORY_LABELS[topicKey] || topicKey;

        item.innerHTML = `
          <div>
            <span class="font-bold text-sm text-slate-800">${label}</span>
            <span class="text-xs text-slate-500 block">${stats.correct} de ${stats.total} acertos</span>
          </div>
          <div class="flex items-center gap-3">
            <div class="w-32 bg-slate-200 h-2.5 rounded-full overflow-hidden">
              <div class="h-full rounded-full ${topicPct >= 70 ? 'bg-emerald-500' : topicPct >= 50 ? 'bg-indigoBrand-500' : 'bg-rose-500'}" style="width: ${topicPct}%;"></div>
            </div>
            <span class="font-bold text-xs w-10 text-right text-slate-700">${topicPct}%</span>
          </div>
        `;
        topicListContainer.appendChild(item);
      }

      renderDetailedReview();
    }

    function renderDetailedReview() {
      const container = document.getElementById('reviewQuestionsContainer');
      container.innerHTML = '';

      currentQuestions.forEach((q, idx) => {
        const chosen = userAnswers[q.id];
        const isCorrect = chosen === q.correctLetter;

        const card = document.createElement('div');
        card.className = `p-6 rounded-2xl border-2 transition-all ${
          isCorrect ? 'border-emerald-200 bg-emerald-50/20' : 'border-rose-200 bg-rose-50/20'
        }`;

        let optionsMarkup = q.options.map(opt => {
          let badgeClass = 'bg-slate-100 text-slate-600 border border-slate-200';
          let borderHighlight = 'border-slate-200 bg-white';

          if (opt.letter === q.correctLetter) {
            badgeClass = 'bg-emerald-600 text-white font-bold';
            borderHighlight = 'border-emerald-400 bg-emerald-50 text-emerald-950 font-medium';
          } else if (opt.letter === chosen && !isCorrect) {
            badgeClass = 'bg-rose-600 text-white font-bold';
            borderHighlight = 'border-rose-400 bg-rose-50 text-rose-950';
          }

          return `
            <div class="p-3.5 rounded-xl border ${borderHighlight} text-sm">
              <div class="flex items-center gap-2 mb-1.5">
                <span class="w-6 h-6 rounded-md text-xs flex items-center justify-center ${badgeClass}">${opt.letter}</span>
                <span class="font-bold text-xs uppercase tracking-wider ${
                  opt.letter === q.correctLetter ? 'text-emerald-700' : opt.letter === chosen ? 'text-rose-700' : 'text-slate-500'
                }">
                  ${opt.letter === q.correctLetter ? '\u2713 Alternativa Correta' : opt.letter === chosen ? '\u2717 Sua Escolha Incorreta' : 'Alternativa Incorreta'}
                </span>
              </div>
              <p class="mb-2 text-slate-800">${opt.text}</p>
              <div class="text-xs bg-white/80 p-2.5 rounded-lg border border-slate-200 text-slate-600 leading-relaxed">
                <strong class="text-slate-800 font-semibold">Justificativa:</strong> ${opt.rationale}
              </div>
            </div>
          `;
        }).join('');

        const catLabel = CATEGORY_LABELS[q.category] || q.category;

        card.innerHTML = `
          <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
            <span class="text-xs font-bold px-2.5 py-1 rounded-lg ${isCorrect ? 'bg-emerald-100 text-emerald-800' : 'bg-rose-100 text-rose-800'}">
              Questao ${idx + 1} - ${isCorrect ? 'Acertou' : chosen ? 'Errou' : 'Nao Respondida'}
            </span>
            <span class="text-xs text-slate-500 font-medium">${catLabel.toUpperCase()} - ${q.subcategory}</span>
          </div>

          <p class="text-slate-800 font-medium text-sm sm:text-base mb-4 leading-relaxed">${q.prompt}</p>

          <div class="space-y-3 mb-4">
            ${optionsMarkup}
          </div>

          <div class="p-3 bg-indigoBrand-50 rounded-xl border border-indigoBrand-100 text-xs text-indigoBrand-900 flex items-start gap-2">
            <span class="font-bold">\ud83d\udca1 Ponto-Chave:</span>
            <span>${q.clinicalPointers}</span>
          </div>
        `;

        container.appendChild(card);
      });
    }

    document.getElementById('btnRestartQuiz').addEventListener('click', () => {
      resultsScreen.classList.add('hidden');
      startScreen.classList.remove('hidden');
    });

    document.getElementById('btnReviewAllDetailed').addEventListener('click', () => {
      document.getElementById('reviewDetailedSection').scrollIntoView({ behavior: 'smooth' });
    });
  </script>
</body>
</html>
