# Radiolaoif-aqui-e-so-pedrada-
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jornada da Computação: Imersão Ludovicense</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Poppins:wght@300;400;600;800;900&family=Press+Start+2P&display=swap" rel="stylesheet">
    <!-- Canvas Confetti -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        reggae: {
                            green: '#009933',
                            yellow: '#FFCC00',
                            red: '#CC0000',
                            black: '#111111'
                        },
                        guarana: '#E5007D',
                        azulejo: '#0047AB',
                        ouroBoi: '#FFD700',
                    },
                    fontFamily: {
                        sans: ['Poppins', 'sans-serif'],
                        title: ['Cinzel', 'serif'],
                        pixel: ['"Press Start 2P"', 'monospace'],
                    }
                }
            }
        }
    </script>

    <style>
        /* Padrão visual de Azulejos de São Luís no Fundo */
        body {
            background-color: #0b0f19;
            background-image: 
                radial-gradient(rgba(229, 0, 125, 0.15) 2px, transparent 0),
                radial-gradient(rgba(0, 71, 171, 0.2) 2px, transparent 0);
            background-size: 30px 30px;
            background-position: 0 0, 15px 15px;
            color: #f3f4f6;
        }

        /* Borda Reggae Tricolor */
        .reggae-border {
            border-image: linear-gradient(to right, #009933 33%, #FFCC00 33%, #FFCC00 66%, #CC0000 66%) 1;
        }

        /* Animação Fita de Boi */
        @keyframes ribbonSway {
            0%, 100% { transform: rotate(-3deg) translateY(0px); }
            50% { transform: rotate(3deg) translateY(-5px); }
        }
        .ribbon-sway {
            animation: ribbonSway 4s ease-in-out infinite;
        }

        /* Animação Pulso Serpente */
        @keyframes snakeGlow {
            0%, 100% { filter: drop-shadow(0 0 5px rgba(0, 255, 100, 0.6)); }
            50% { filter: drop-shadow(0 0 18px rgba(0, 255, 100, 0.9)); }
        }
        .snake-glow {
            animation: snakeGlow 3s ease-in-out infinite;
        }

        /* Efeito Radiola Neon Glow */
        .radiola-glow {
            box-shadow: 0 0 20px rgba(255, 204, 0, 0.4), inset 0 0 15px rgba(204, 0, 0, 0.5);
        }

        /* Disco Gira-Gira Reggae */
        @keyframes spinSlow {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .spin-vinyl {
            animation: spinSlow 8s linear infinite;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: #111;
        }
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(#009933, #FFCC00, #CC0000);
            border-radius: 5px;
        }
    </style>
</head>
<body class="min-h-screen font-sans pb-16">

    <!-- Fitas Tradicionais Ornamentais (Topo) -->
    <div class="w-full flex justify-around overflow-hidden h-6 bg-black border-b border-reggae-yellow/40">
        <div class="w-3 h-12 bg-reggae-green -rotate-12 transform origin-top ribbon-sway"></div>
        <div class="w-3 h-12 bg-reggae-yellow rotate-6 transform origin-top ribbon-sway" style="animation-delay: 0.5s;"></div>
        <div class="w-3 h-12 bg-reggae-red -rotate-6 transform origin-top ribbon-sway" style="animation-delay: 1s;"></div>
        <div class="w-3 h-12 bg-guarana rotate-12 transform origin-top ribbon-sway" style="animation-delay: 1.5s;"></div>
        <div class="w-3 h-12 bg-azulejo -rotate-12 transform origin-top ribbon-sway" style="animation-delay: 0.7s;"></div>
        <div class="w-3 h-12 bg-ouroBoi rotate-6 transform origin-top ribbon-sway" style="animation-delay: 1.2s;"></div>
        <div class="w-3 h-12 bg-reggae-green -rotate-6 transform origin-top ribbon-sway" style="animation-delay: 0.3s;"></div>
        <div class="w-3 h-12 bg-reggae-red rotate-12 transform origin-top ribbon-sway" style="animation-delay: 1.8s;"></div>
    </div>

    <!-- Header Principal -->
    <header class="relative px-4 py-8 text-center border-b-4 border-reggae-yellow bg-black/80 backdrop-blur-md">
        <div class="max-w-5xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6">
            
            <!-- Logo Radiola Reggae -->
            <div class="flex items-center gap-4">
                <div class="relative w-20 h-20 bg-reggae-black rounded-full border-4 border-reggae-yellow flex items-center justify-center radiola-glow">
                    <i class="fa-solid fa-compact-disc text-4xl text-reggae-red spin-vinyl"></i>
                    <div class="absolute w-6 h-6 bg-reggae-green rounded-full border-2 border-black"></div>
                </div>
                <div class="text-left">
                    <span class="bg-reggae-green text-black px-2 py-0.5 font-bold text-xs uppercase tracking-widest rounded">Reggae & Tech</span>
                    <h1 class="text-3xl font-black text-transparent bg-clip-text bg-gradient-to-r from-reggae-green via-reggae-yellow to-reggae-red">
                        ILHA DA COMPUTAÇÃO
                    </h1>
                    <p class="text-xs text-amber-300 font-semibold">São Luís do Maranhão • Calouros de ADS</p>
                </div>
            </div>

            <!-- Lenda da Serpente / Banner Cultural -->
            <div class="bg-slate-900/90 border-2 border-azulejo rounded-lg p-3 text-left max-w-md snake-glow flex items-center gap-3">
                <div class="text-3xl text-emerald-400">🐍</div>
                <div>
                    <h4 class="text-xs font-bold text-emerald-400 uppercase tracking-wide">Lenda Ludovicense</h4>
                    <p class="text-xs text-gray-300">
                        A <span class="text-reggae-yellow font-bold">Serpente Encantada</span> acorda quando o código compila de primeira! Se falhar, a carruagem de <span class="text-guarana font-bold">Ana Jansen</span> passa!
                    </p>
                </div>
            </div>

        </div>
    </header>

    <!-- Conteúdo Principal -->
    <main class="max-w-6xl mx-auto px-4 mt-8 space-y-12">

        <!-- Seção 1: Mini-Site de Conteúdo Didático -->
        <section>
            <div class="flex items-center gap-3 mb-6">
                <div class="w-4 h-8 bg-reggae-yellow rounded-sm"></div>
                <h2 class="text-2xl font-extrabold text-amber-200 uppercase tracking-wider font-title">
                    <i class="fa-solid fa-book-open text-reggae-green mr-2"></i> Trilha dos 5 Conceitos Fundamentais
                </h2>
            </div>

            <!-- Grid de Cards Maximalistas -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">

                <!-- Conceito 1: ENIAC -->
                <div class="bg-gradient-to-b from-gray-900 to-black border-2 border-reggae-green rounded-xl p-5 shadow-lg relative overflow-hidden group hover:border-reggae-yellow transition">
                    <div class="absolute top-0 right-0 bg-reggae-green text-black font-extrabold px-3 py-1 rounded-bl-lg text-xs">
                        Conceito #01
                    </div>
                    <div class="text-3xl mb-2 text-reggae-green"><i class="fa-solid fa-calculator"></i></div>
                    <h3 class="text-xl font-bold text-reggae-yellow mb-2">1. ENIAC (1946)</h3>
                    <p class="text-sm text-gray-300 leading-relaxed mb-3">
                        O primeiro computador digital eletrônico de grande escala do mundo. Construído com quase 18.000 válvulas, pesava 30 toneladas e ocupava um galpão inteiro. Ele não possuía sistema operacional e sua programação era feita alterando cabos e chaves manualmente.
                    </p>
                    <div class="bg-gray-800/80 p-2.5 rounded border-l-4 border-reggae-green text-xs text-emerald-300">
                        <strong>Visão Ludovicense:</strong> Parecia uma Radiola de Reggae gigante, cheia de cabos e válvulas brilhando no ritmo da batida!
                    </div>
                </div>

                <!-- Conceito 2: Pioneirismo Feminino -->
                <div class="bg-gradient-to-b from-gray-900 to-black border-2 border-guarana rounded-xl p-5 shadow-lg relative overflow-hidden group hover:border-reggae-yellow transition">
                    <div class="absolute top-0 right-0 bg-guarana text-white font-extrabold px-3 py-1 rounded-bl-lg text-xs">
                        Conceito #02
                    </div>
                    <div class="text-3xl mb-2 text-guarana"><i class="fa-solid fa-users-gear"></i></div>
                    <h3 class="text-xl font-bold text-pink-300 mb-2">2. Pioneirismo Feminino no Software</h3>
                    <p class="text-sm text-gray-300 leading-relaxed mb-3">
                        As primeiras programadoras do mundo foram seis mulheres: <strong>Kay McNulty, Betty Jennings, Betty Snyder, Marlyn Wescoff, Frances Bilas e Ruth Lichterman</strong>. Elas calcularam trajetórias de balística e estruturaram a lógica da programação de software sem nenhum manual de instruções preexistente.
                    </p>
                    <div class="bg-gray-800/80 p-2.5 rounded border-l-4 border-guarana text-xs text-pink-300">
                        <strong>Visão Ludovicense:</strong> Uma verdadeira força da mata! Mulheres de garra que teceram a base da programação mundial.
                    </div>
                </div>

                <!-- Conceito 3: Microprocessador -->
                <div class="bg-gradient-to-b from-gray-900 to-black border-2 border-reggae-yellow rounded-xl p-5 shadow-lg relative overflow-hidden group hover:border-reggae-green transition">
                    <div class="absolute top-0 right-0 bg-reggae-yellow text-black font-extrabold px-3 py-1 rounded-bl-lg text-xs">
                        Conceito #03
                    </div>
                    <div class="text-3xl mb-2 text-reggae-yellow"><i class="fa-solid fa-microchip"></i></div>
                    <h3 class="text-xl font-bold text-amber-300 mb-2">3. O Microprocessador (1971)</h3>
                    <p class="text-sm text-gray-300 leading-relaxed mb-3">
                        Com o lançamento do <strong>Intel 4004</strong>, toda a Unidade Central de Processamento (CPU) foi condensada em um único microchip de silício. Isso permitiu a miniaturização dos computadores, reduzindo os custos e viabilizando a revolução dos PCs pessoais.
                    </p>
                    <div class="bg-gray-800/80 p-2.5 rounded border-l-4 border-reggae-yellow text-xs text-amber-200">
                        <strong>Visão Ludovicense:</strong> Compactar um gigante numa pecinha de bolso, como guardar a força de um tambor de crioula em um microchip!
                    </div>
                </div>

                <!-- Conceito 4: Evolução na Programação -->
                <div class="bg-gradient-to-b from-gray-900 to-black border-2 border-azulejo rounded-xl p-5 shadow-lg relative overflow-hidden group hover:border-reggae-yellow transition">
                    <div class="absolute top-0 right-0 bg-azulejo text-white font-extrabold px-3 py-1 rounded-bl-lg text-xs">
                        Conceito #04
                    </div>
                    <div class="text-3xl mb-2 text-cyan-400"><i class="fa-solid fa-code"></i></div>
                    <h3 class="text-xl font-bold text-cyan-300 mb-2">4. Evolução na Programação</h3>
                    <p class="text-sm text-gray-300 leading-relaxed mb-3">
                        A programação evoluiu de linguagens de máquina (código binário `0` e `1`) e Assembly para linguagens de alto nível (como Fortran, C, Python e JavaScript). Em vez de manipular fiação e circuitos elétricos brutos, passamos a escrever comandos estruturados em inglês simples.
                    </p>
                    <div class="bg-gray-800/80 p-2.5 rounded border-l-4 border-azulejo text-xs text-cyan-200">
                        <strong>Visão Ludovicense:</strong> Deixamos de mexer nos fios do circuito da máquina e passamos a conversar na linguagem direta do programador!
                    </div>
                </div>

                <!-- Conceito 5: Computação Atual -->
                <div class="bg-gradient-to-b from-gray-900 to-black border-2 border-reggae-red rounded-xl p-5 shadow-lg relative overflow-hidden group md:col-span-2 lg:col-span-2 hover:border-reggae-yellow transition">
                    <div class="absolute top-0 right-0 bg-reggae-red text-white font-extrabold px-3 py-1 rounded-bl-lg text-xs">
                        Conceito #05
                    </div>
                    <div class="text-3xl mb-2 text-reggae-red"><i class="fa-solid fa-cloud-bolt"></i></div>
                    <h3 class="text-xl font-bold text-red-400 mb-2">5. Computação nos Tempos Atuais (Ubíqua & Nuvem)</h3>
                    <p class="text-sm text-gray-300 leading-relaxed mb-3">
                        Hoje o computador deixou de ser apenas a "caixa cinza de desktop" em cima da mesa. Com a Computação em Nuvem, Internet das Coisas (IoT) e Inteligência Artificial, a tecnologia virou uma infraestrutura invisível que sustenta smartphones, veículos, redes de saúde e o ecossistema digital global.
                    </p>
                    <div class="bg-gray-800/80 p-2.5 rounded border-l-4 border-reggae-red text-xs text-red-200">
                        <strong>Visão Ludovicense:</strong> Está no ar como a pedra de reggae nas praias de São Luís — imperceptível aos olhos, mas movimentando tudo ao nosso redor!
                    </div>
                </div>

            </div>
        </section>

        <!-- Seção 2: O Quiz da Pedra Tocada -->
        <section class="bg-gradient-to-r from-slate-950 via-black to-slate-950 border-4 border-reggae-yellow rounded-2xl p-6 md:p-8 shadow-2xl relative">
            
            <div class="text-center mb-8">
                <span class="bg-reggae-red text-white font-bold text-xs uppercase px-3 py-1 rounded-full tracking-widest">Desafio dos Calouros</span>
                <h2 class="text-3xl md:text-4xl font-extrabold text-reggae-yellow mt-2 font-title">
                    BUMBA-MEU-QUIZ: 10 QUESTÕES ESSENCIAIS
                </h2>
                <p class="text-sm text-gray-300 mt-1">Testes seus conhecimentos sobre a história da computação e mostre que você é pai d'égua!</p>
            </div>

            <!-- Progresso do Quiz -->
            <div class="mb-6">
                <div class="flex justify-between text-xs text-amber-300 font-bold mb-1">
                    <span id="quiz-progress-text">Questão 1 de 10</span>
                    <span id="quiz-score-text">Pontuação: 0</span>
                </div>
                <div class="w-full h-4 bg-gray-800 rounded-full overflow-hidden border border-reggae-yellow/40">
                    <div id="progress-bar" class="h-full bg-gradient-to-r from-reggae-green via-reggae-yellow to-reggae-red transition-all duration-300" style="width: 10%;"></div>
                </div>
            </div>

            <!-- Card de Questão -->
            <div id="quiz-card" class="bg-gray-900/90 border-2 border-azulejo rounded-xl p-6 mb-6">
                <h3 id="question-text" class="text-lg md:text-xl font-bold text-white mb-6">
                    Carregando pergunta...
                </h3>

                <div id="options-container" class="space-y-3">
                    <!-- Opções injetadas via JS -->
                </div>

                <!-- Feedback Visual/Textual -->
                <div id="feedback-box" class="hidden mt-4 p-4 rounded-lg text-sm font-bold flex items-center gap-3">
                    <div id="feedback-icon" class="text-2xl"></div>
                    <div id="feedback-text"></div>
                </div>
            </div>

            <!-- Botões de Controle -->
            <div class="flex justify-between items-center">
                <button id="prev-btn" onclick="prevQuestion()" class="hidden bg-gray-800 hover:bg-gray-700 text-white font-bold px-4 py-2 rounded-lg text-sm transition">
                    <i class="fa-solid fa-arrow-left mr-2"></i> Anterior
                </button>
                <button id="next-btn" onclick="nextQuestion()" disabled class="ml-auto bg-reggae-yellow hover:bg-amber-400 text-black font-extrabold px-6 py-2.5 rounded-lg text-sm transition disabled:opacity-50 disabled:cursor-not-allowed">
                    Próxima Questão <i class="fa-solid fa-arrow-right ml-2"></i>
                </button>
            </div>

            <!-- Tela de Resultado Final (Escondida por padrão) -->
            <div id="result-screen" class="hidden text-center py-8">
                <div class="text-6xl mb-4">🏆</div>
                <h3 class="text-3xl font-extrabold text-reggae-yellow mb-2">Resultado da Pedra Tocada!</h3>
                <p id="final-score-text" class="text-xl text-white font-bold mb-4">Você acertou X de 10 perguntas.</p>
                
                <div id="cultural-badge" class="inline-block bg-gray-900 border-2 border-reggae-green p-4 rounded-xl mb-6 max-w-md">
                    <!-- Selo cultural dinâmico -->
                </div>

                <div>
                    <button onclick="restartQuiz()" class="bg-gradient-to-r from-reggae-green to-reggae-yellow text-black font-black px-8 py-3 rounded-xl hover:scale-105 transition shadow-lg">
                        <i class="fa-solid fa-rotate-right mr-2"></i> Tentar Novamente
                    </button>
                </div>
            </div>

        </section>

        <!-- Seção 3: Glossário de Gírias & Cultura Ludovicense -->
        <section class="bg-black/70 border-2 border-reggae-green rounded-xl p-6">
            <h3 class="text-lg font-bold text-reggae-green mb-4 uppercase tracking-wider flex items-center gap-2">
                <i class="fa-solid fa-comments"></i> Dicionário de Bordo Ludovicense do Desenvolvedor
            </h3>
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-5 gap-3 text-center text-xs">
                <div class="bg-gray-900 p-2.5 rounded border border-gray-800">
                    <span class="block text-reggae-yellow font-bold text-sm">Mermã / Mermão</span>
                    <span class="text-gray-400">Expressão de admiração ou de chamada no código.</span>
                </div>
                <div class="bg-gray-900 p-2.5 rounded border border-gray-800">
                    <span class="block text-reggae-green font-bold text-sm">Pedra Tocada</span>
                    <span class="text-gray-400">Música marcante do Reggae; no Dev: código de sucesso!</span>
                </div>
                <div class="bg-gray-900 p-2.5 rounded border border-gray-800">
                    <span class="block text-guarana font-bold text-sm">Pai d'Égua</span>
                    <span class="text-gray-400">Algoritmo excelente, sem bugs.</span>
                </div>
                <div class="bg-gray-900 p-2.5 rounded border border-gray-800">
                    <span class="block text-azulejo font-bold text-sm">Na Massa</span>
                    <span class="text-gray-400">Tudo funcionando perfeitamente na produção.</span>
                </div>
                <div class="bg-gray-900 p-2.5 rounded border border-gray-800">
                    <span class="block text-reggae-red font-bold text-sm">Radiola</span>
                    <span class="text-gray-400">Equipamento potente; na ti: Servidor de Alta Performance.</span>
                </div>
            </div>
        </section>

    </main>

    <!-- Rodapé -->
    <footer class="mt-16 text-center text-xs text-gray-500 border-t border-gray-800 pt-6">
        <p>Desenvolvido como Ferramenta Educativa de Suporte aos Calouros de Desenvolvimento de Sistemas.</p>
        <p class="text-gray-600 mt-1">São Luís do Maranhão • Cultura, Etnodesign & Tecnologia</p>
    </footer>

    <!-- JavaScript da Aplicação -->
    <script>
        // Dados das 10 Perguntas Essenciais e Verídicas
        const quizData = [
            {
                question: "1. Qual foi a principal característica técnica do ENIAC quando criado em 1946?",
                options: [
                    "Foi o primeiro computador pessoal com tela sensível ao toque.",
                    "Foi o primeiro computador digital eletrônico de grande escala do mundo.",
                    "Foi o primeiro microprocessador construído em um único chip de silício.",
                    "Funcionava exclusivamente utilizando inteligência artificial em nuvem."
                ],
                correct: 1,
                explanation: "Exato! O ENIAC é reconhecido historicamente como o primeiro computador digital eletrônico de grande escala."
            },
            {
                question: "2. Como era realizada a programação original no ENIAC?",
                options: [
                    "Digitando comandos em linguagens como Python ou Java.",
                    "Utilizando cartões magnéticos sem fio.",
                    "Alterando fisicamente a fiação, cabos e chaves da máquina.",
                    "Via comandos de voz sintetizados."
                ],
                correct: 2,
                explanation: "Na massa! Não havia sistema operacional; o programa era configurado mudando cabos e chaves manualmente."
            },
            {
                question: "3. Qual grupo foi responsável por programar integralmente o pioneiro programa do ENIAC?",
                options: [
                    "Um grupo de seis engenheiras conhecidas como as Mulheres do ENIAC.",
                    "A equipe da NASA liderada por Alan Turing.",
                    "Os criadores do sistema operacional Unix.",
                    "Estudantes de mestrado de São Luís em 1950."
                ],
                correct: 0,
                explanation: "Pai d'égua! Seis mulheres (Kay McNulty, Betty Jennings, Betty Snyder, Marlyn Wescoff, Frances Bilas e Ruth Lichterman) foram as pioneiras do software."
            },
            {
                question: "4. Qual inovação fundamental permitiu condensar a CPU inteira em um único chip em 1971?",
                options: [
                    "A válvula termiônica de quartzo.",
                    "O Microprocessador (com o Intel 4004).",
                    "A criação da fibra óptica de alta velocidade.",
                    "A invenção do disco rígido de fita magnética."
                ],
                correct: 1,
                explanation: "Pedra tocada! O microprocessador unificou o cérebro do computador em um único chip de silício."
            },
            {
                question: "5. Na evolução da programação, o que marcou a transição para linguagens de alto nível?",
                options: [
                    "A necessidade de utilizar mais fios elétricos.",
                    "A proibição do uso de caracteres em inglês.",
                    "O salto de operar circuitos brutos para dar ordens estruturadas em inglês simples.",
                    "O fim do uso de qualquer tipo de algoritmo."
                ],
                correct: 2,
                explanation: "Com certeza! Em vez de falar a linguagem direta dos circuitos (0 e 1), os dev programam em instruções inteligíveis."
            },
            {
                question: "6. Qual a definição da Computação Atual nos tempos presentes?",
                options: [
                    "Ficou restrita apenas a grandes computadores de mesa cinzas.",
                    "Tornou-se uma infraestrutura invisível, ubíqua e conectada em nuvem.",
                    "Voltou a depender de cartões perfurados para rodar sistemas.",
                    "Só funciona se estiver desconectada da internet."
                ],
                correct: 1,
                explanation: "Mermã, acertou! Hoje a computação permeia desde dispositivos vestíveis até carros e redes globais em nuvem."
            },
            {
                question: "7. O que representa o termo 'Linguagem de Alto Nível' para um desenvolvedor?",
                options: [
                    "Uma linguagem antiga que só roda no ENIAC.",
                    "Uma linguagem mais próxima do entendimento humano e distante do código de máquina puro.",
                    "Um idioma falado exclusivamente por cientistas na Alemanha.",
                    "O código binário que o processador executa diretamente."
                ],
                correct: 1,
                explanation: "Certíssimo! Quanto maior o nível da linguagem, mais próxima ela é da lógica humana (ex: Python, JS, C#)."
            },
            {
                question: "8. Qual o impacto direto da invenção do microprocessador na sociedade?",
                options: [
                    "Aumentou o tamanho dos computadores para ocuparem prédios.",
                    "Permitiu a popularização dos computadores pessoais (PCs) e dispositivos móveis.",
                    "Eliminou a necessidade de energia elétrica na computação.",
                    "Substituiu todo o software por componentes mecânicos."
                ],
                correct: 1,
                explanation: "Na ponta da agulha! A miniaturização reduziu custos e colocou o computador no bolso das pessoas."
            },
            {
                question: "9. O trabalho das seis programadoras do ENIAC por muito tempo não teve o devido crédito porque:",
                options: [
                    "O trabalho de hardware era visto como principal, enquanto o software era considerado secundário na época.",
                    "Elas preferiram manter segredo sobre o desenvolvimento.",
                    "O ENIAC nunca funcionou de verdade.",
                    "O governo maranhense comprou a patente em 1946."
                ],
                correct: 0,
                explanation: "Histórico e verídico! O trabalho de software foi subestimado por anos antes de ser reconhecido como revolução."
            },
            {
                question: "10. Atualmente, o conceito de 'Internet das Coisas' (IoT) se refere a:",
                options: [
                    "Um site único onde se vende objetos antigos.",
                    "A conexão de objetos cotidianos (geladeiras, relógios, sensores) à rede de computadores.",
                    "A programação exclusiva feita por válvulas do ENIAC.",
                    "Uma lenda urbana ludovicense."
                ],
                correct: 1,
                explanation: "Show de bola! IoT é a prova viva de que a computação virou a infraestrutura invisível do nosso mundo!"
            }
        ];

        let currentQuestion = 0;
        let score = 0;
        let selectedOption = null;
        let answeredQuestions = new Array(quizData.length).fill(null);

        // Inicializar Quiz
        function loadQuestion() {
            const data = quizData[currentQuestion];
            document.getElementById('question-text').innerText = data.question;
            document.getElementById('quiz-progress-text').innerText = `Questão ${currentQuestion + 1} de ${quizData.length}`;
            document.getElementById('progress-bar').style.width = `${((currentQuestion + 1) / quizData.length) * 100}%`;

            const container = document.getElementById('options-container');
            container.innerHTML = '';

            const feedbackBox = document.getElementById('feedback-box');
            feedbackBox.classList.add('hidden');

            data.options.forEach((opt, index) => {
                const btn = document.createElement('button');
                btn.className = `w-full text-left p-4 rounded-lg border-2 border-gray-700 bg-gray-800/60 hover:bg-gray-700/80 transition text-sm text-gray-200 flex items-center justify-between font-medium`;
                btn.onclick = () => selectOption(index);
                btn.innerHTML = `<span>${opt}</span> <i class="fa-regular fa-circle text-gray-500"></i>`;
                
                // Se já respondeu esta questão anteriormente
                if (answeredQuestions[currentQuestion] !== null) {
                    btn.disabled = true;
                    if (index === data.correct) {
                        btn.className = `w-full text-left p-4 rounded-lg border-2 border-reggae-green bg-emerald-950/60 text-emerald-200 text-sm font-bold flex items-center justify-between`;
                        btn.innerHTML = `<span>${opt}</span> <i class="fa-solid fa-circle-check text-reggae-green"></i>`;
                    } else if (index === answeredQuestions[currentQuestion]) {
                        btn.className = `w-full text-left p-4 rounded-lg border-2 border-reggae-red bg-red-950/60 text-red-200 text-sm font-bold flex items-center justify-between`;
                        btn.innerHTML = `<span>${opt}</span> <i class="fa-solid fa-circle-xmark text-reggae-red"></i>`;
                    }
                }

                container.appendChild(btn);
            });

            // Se já respondida, mostrar feedback
            if (answeredQuestions[currentQuestion] !== null) {
                showFeedback(answeredQuestions[currentQuestion] === data.correct, data.explanation);
                document.getElementById('next-btn').disabled = false;
            } else {
                document.getElementById('next-btn').disabled = true;
            }

            // Atualizar botões de navegação
            if (currentQuestion > 0) {
                document.getElementById('prev-btn').classList.remove('hidden');
            } else {
                document.getElementById('prev-btn').classList.add('hidden');
            }
        }

        function selectOption(index) {
            if (answeredQuestions[currentQuestion] !== null) return; // Já respondida

            const data = quizData[currentQuestion];
            answeredQuestions[currentQuestion] = index;

            const isCorrect = index === data.correct;
            if (isCorrect) score++;

            document.getElementById('quiz-score-text').innerText = `Pontuação: ${score}`;

            loadQuestion(); // Recarrega botões com estados de certo/errado
        }

        function showFeedback(isCorrect, explanation) {
            const feedbackBox = document.getElementById('feedback-box');
            const feedbackIcon = document.getElementById('feedback-icon');
            const feedbackText = document.getElementById('feedback-text');

            feedbackBox.classList.remove('hidden', 'bg-red-950/80', 'border-reggae-red', 'bg-emerald-950/80', 'border-reggae-green');

            if (isCorrect) {
                feedbackBox.classList.add('bg-emerald-950/80', 'border', 'border-reggae-green', 'text-emerald-200');
                feedbackIcon.innerHTML = '🎉';
                feedbackText.innerHTML = `<span class="block text-reggae-yellow uppercase tracking-wide">Pedra Tocada! Resposta Certa!</span>${explanation}`;
            } else {
                feedbackBox.classList.add('bg-red-950/80', 'border', 'border-reggae-red', 'text-red-200');
                feedbackIcon.innerHTML = '⚠️';
                feedbackText.innerHTML = `<span class="block text-reggae-red uppercase tracking-wide">Cuidado com a Carruagem de Ana Jansen!</span>${explanation}`;
            }
        }

        function nextQuestion() {
            if (currentQuestion < quizData.length - 1) {
                currentQuestion++;
                loadQuestion();
            } else {
                showFinalResults();
            }
        }

        function prevQuestion() {
            if (currentQuestion > 0) {
                currentQuestion--;
                loadQuestion();
            }
        }

        function showFinalResults() {
            document.getElementById('quiz-card').classList.add('hidden');
            document.getElementById('next-btn').classList.add('hidden');
            document.getElementById('prev-btn').classList.add('hidden');

            const resultScreen = document.getElementById('result-screen');
            resultScreen.classList.remove('hidden');

            document.getElementById('final-score-text').innerText = `Você acertou ${score} de ${quizData.length} perguntas!`;

            const badgeContainer = document.getElementById('cultural-badge');
            if (score >= 8) {
                badgeContainer.innerHTML = `
                    <div class="text-reggae-yellow text-xl font-bold mb-1">🏅 Nível: Mestre da Radiola Dev!</div>
                    <p class="text-xs text-gray-300">Você dominou todos os conceitos fundamentais! A Serpente Encantada aprova seu código!</p>
                `;
                confetti({ particleCount: 150, spread: 80, origin: { y: 0.6 } });
            } else if (score >= 5) {
                badgeContainer.innerHTML = `
                    <div class="text-reggae-green text-xl font-bold mb-1">Boi de Orquestra!</div>
                    <p class="text-xs text-gray-300">Bom desempenho! Mais uma ajustada nos conceitos e seu software fica 100% na massa.</p>
                `;
            } else {
                badgeContainer.innerHTML = `
                    <div class="text-reggae-red text-xl font-bold mb-1">Atenção Calouro!</div>
                    <p class="text-xs text-gray-300">Dê mais uma lida na trilha dos 5 conceitos para não cair na maldição da Ana Jansen!</p>
                `;
            }
        }

        function restartQuiz() {
            currentQuestion = 0;
            score = 0;
            answeredQuestions = new Array(quizData.length).fill(null);
            document.getElementById('quiz-score-text').innerText = `Pontuação: 0`;

            document.getElementById('quiz-card').classList.remove('hidden');
            document.getElementById('next-btn').classList.remove('hidden');
            document.getElementById('result-screen').classList.add('hidden');

            loadQuestion();
        }

        // Inicializar na Carga
        window.onload = () => {
            loadQuestion();
        };
    </script>
</body>
</html>
