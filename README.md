<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inteligencia Artificial: Fundamentos y Consecuencias</title>
    <style>
        :root {
            --bg-dark: #0b0f19;
            --bg-card: #131b2e;
            --text-main: #e2e8f0;
            --text-muted: #94a3b8;
            --accent-cyan: #00f0ff;
            --accent-purple: #8b5cf6;
            --accent-green: #10b981;
            --accent-red: #ef4444;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        header {
            background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 100%);
            padding: 4rem 1.5rem;
            text-align: center;
            border-bottom: 1px solid rgba(0, 240, 255, 0.2);
        }

        header h1 {
            font-size: 2.8rem;
            background: linear-gradient(90deg, var(--accent-cyan), var(--accent-purple));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
        }

        header p {
            max-width: 700px;
            margin: 0 auto;
            color: var(--text-muted);
            font-size: 1.15rem;
        }

        nav {
            background: rgba(19, 27, 46, 0.9);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 100;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            padding: 1rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            flex-wrap: wrap;
        }

        nav a {
            color: var(--text-main);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--accent-cyan);
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 3rem 1.5rem;
        }

        section {
            margin-bottom: 4.5rem;
        }

        h2 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: var(--accent-cyan);
            border-left: 4px solid var(--accent-purple);
            padding-left: 1rem;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .card {
            background: var(--bg-card);
            padding: 1.5rem;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.08);
            transition: transform 0.3s, border-color 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--accent-cyan);
        }

        .card h3 {
            color: #fff;
            margin-bottom: 0.75rem;
            font-size: 1.25rem;
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        .consequences-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .pro-card { border-top: 4px solid var(--accent-green); }
        .con-card { border-top: 4px solid var(--accent-red); }

        ul {
            list-style: none;
            margin-top: 1rem;
        }

        ul li {
            margin-bottom: 0.75rem;
            padding-left: 1.5rem;
            position: relative;
            color: var(--text-muted);
        }

        .pro-card ul li::before {
            content: "✓";
            color: var(--accent-green);
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        .con-card ul li::before {
            content: "⚠";
            color: var(--accent-red);
            position: absolute;
            left: 0;
        }

        /* Quiz Styles */
        .quiz-box {
            background: var(--bg-card);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid rgba(139, 92, 246, 0.3);
        }

        .quiz-question {
            font-size: 1.2rem;
            margin-bottom: 1.2rem;
            font-weight: 600;
        }

        .quiz-options {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
        }

        .quiz-btn {
            background: rgba(255, 255, 255, 0.05);
            color: var(--text-main);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 0.9rem 1.2rem;
            border-radius: 8px;
            text-align: left;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.2s;
        }

        .quiz-btn:hover {
            background: rgba(0, 240, 255, 0.1);
            border-color: var(--accent-cyan);
        }

        .quiz-feedback {
            margin-top: 1.2rem;
            font-weight: bold;
            min-height: 24px;
        }

        footer {
            text-align: center;
            padding: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            color: var(--text-muted);
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <header>
        <h1>Inteligencia Artificial (IA)</h1>
        <p>Explorando la tecnología que está redefiniendo la humanidad: sus fundamentos, aplicaciones actuales y las profundas consecuencias éticas y sociales de su desarrollo.</p>
    </header>

    <nav>
        <a href="#que-es">¿Qué es la IA?</a>
        <a href="#tipos">Tipos de IA</a>
        <a href="#consecuencias">Consecuencias</a>
        <a href="#quiz">Pon a prueba tu conocimiento</a>
    </nav>

    <div class="container">
        <!-- Sección 1 -->
        <section id="que-es">
            <h2>¿Qué es la Inteligencia Artificial?</h2>
            <p style="color: var(--text-muted); margin-bottom: 1.5rem;">
                La Inteligencia Artificial es una rama de la informática dedicada a crear sistemas capaces de realizar tareas que normalmente requieren inteligencia humana, como el aprendizaje, el razonamiento, la percepción y la toma de decisiones.
            </p>
            <div class="grid">
                <div class="card">
                    <h3>Machine Learning (Aprendizaje Automático)</h3>
                    <p>Algoritmos que permiten a las máquinas aprender patrones a partir de grandes volúmenes de datos sin ser programadas explícitamente para cada regla.</p>
                </div>
                <div class="card">
                    <h3>Deep Learning (Aprendizaje Profundo)</h3>
                    <p>Subcampo basado en redes neuronales artificiales inspiradas en el cerebro humano, clave para el reconocimiento de voz, imágenes y procesamiento de lenguaje.</p>
                </div>
                <div class="card">
                    <h3>IA Generativa</h3>
                    <p>Modelos capaces de crear contenido original —texto, código, imágenes, audio y video— a partir de instrucciones humanas (prompts).</p>
                </div>
            </div>
        </section>

        <!-- Sección 2 -->
        <section id="tipos">
            <h2>Niveles de Capacidad</h2>
            <div class="grid">
                <div class="card">
                    <h3>1. IA Estrecha (ANI)</h3>
                    <p><strong>Estado: Actualidad.</strong> Diseñada para una tarea específica (ej. asistentes de voz, motores de recomendación, diagnóstico médico por imagen).</p>
                </div>
                <div class="card">
                    <h3>2. IA General (AGI)</h3>
                    <p><strong>Estado: Teórico / En investigación.</strong> Una máquina con capacidad cognitiva equivalente a la humana, capaz de razonar y aprender cualquier tarea intelectual.</p>
                </div>
                <div class="card">
                    <h3>3. Superinteligencia (ASI)</h3>
                    <p><strong>Estado: Hipotético.</strong> Intelecto que superaría ampliamente las capacidades cognitivas humanas en prácticamente todos los campos.</p>
                </div>
            </div>
        </section>

        <!-- Sección 3 -->
        <section id="consecuencias">
            <h2>Consecuencias e Impacto Global</h2>
            <div class="consequences-grid">
                <div class="card pro-card">
                    <h3>Beneficios y Oportunidades</h3>
                    <ul>
                        <li><strong>Avances Médicos:</strong> Descubrimiento acelerado de fármacos y detección temprana de enfermedades.</li>
                        <li><strong>Productividad:</strong> Automatización de tareas repetitivas, liberando tiempo humano para labores creativas y estratégicas.</li>
                        <li><strong>Personalización:</strong> Educación adaptada al ritmo de cada estudiante y accesibilidad para personas con discapacidad.</li>
                        <li><strong>Ciencia y Clima:</strong> Optimización de redes energéticas y modelado climático complejo.</li>
                    </ul>
                </div>

                <div class="card con-card">
                    <h3>Riesgos y Dilemas Éticos</h3>
                    <ul>
                        <li><strong>Desplazamiento Laboral:</strong> Transformación rápida del mercado de trabajo y necesidad urgente de reconversión profesional.</li>
                        <li><strong>Sesgos Algorítmicos:</strong> Si los datos de entrenamiento contienen prejuicios humanos, la IA los reproducirá y amplificará.</li>
                        <li><strong>Desinformación (Deepfakes):</strong> Creación de contenido falso hiperrealista que amenaza la privacidad y los procesos democráticos.</li>
                        <li><strong>Impacto Ambiental y Privacidad:</strong> Alto consumo energético de los centros de datos y vigilancia masiva.</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Sección 4: Quiz Interactivo -->
        <section id="quiz">
            <h2>Mini Quiz sobre IA</h2>
            <div class="quiz-box">
                <div class="quiz-question" id="question-text">Cargando pregunta...</div>
                <div class="quiz-options" id="options-container"></div>
                <div class="quiz-feedback" id="feedback"></div>
            </div>
        </section>
    </div>

    <footer>
        <p>Proyecto educativo sobre Inteligencia Artificial • Listo para desplegar en GitHub Pages</p>
    </footer>

    <script>
        const quizData = [
            {
                question: "¿Qué tipo de Inteligencia Artificial existe y utilizamos actualmente en la vida cotidiana?",
                options: [
                    "IA General (AGI)",
                    "IA Estrecha o Débil (ANI)",
                    "Superinteligencia Artificial (ASI)"
                ],
                correct: 1
            },
            {
                question: "¿Cuál es una de las principales consecuencias éticas del entrenamiento de modelos con datos históricos?",
                options: [
                    "La reproducción y amplificación de sesgos humanos",
                    "La eliminación automática de todo consumo eléctrico",
                    "Que la IA adquiere conciencia propia inmediatamente"
                ],
                correct: 0
            },
            {
                question: "¿Qué tecnología permite a la IA generar texto, imágenes y código nuevo?",
                options: [
                    "Computación Cuántica Básica",
                    "IA Generativa",
                    "Sistemas Expertos de los años 70"
                ],
                correct: 1
            }
        ];

        let currentQuestion = 0;
        let score = 0;

        const questionEl = document.getElementById("question-text");
        const optionsEl = document.getElementById("options-container");
        const feedbackEl = document.getElementById("feedback");

        function loadQuestion() {
            feedbackEl.textContent = "";
            const current = quizData[currentQuestion];
            questionEl.textContent = `${currentQuestion + 1}. ${current.question}`;
            optionsEl.innerHTML = "";

            current.options.forEach((option, index) => {
                const btn = document.createElement("button");
                btn.className = "quiz-btn";
                btn.textContent = option;
                btn.onclick = () => checkAnswer(index);
                optionsEl.appendChild(btn);
            });
        }

        function checkAnswer(selectedIndex) {
            const current = quizData[currentQuestion];
            const buttons = optionsEl.querySelectorAll(".quiz-btn");
            buttons.forEach(b => b.disabled = true);

            if (selectedIndex === current.correct) {
                score++;
                feedbackEl.style.color = "var(--accent-green)";
                feedbackEl.textContent = "¡Correcto!";
            } else {
                feedbackEl.style.color = "var(--accent-red)";
                feedbackEl.textContent = `Incorrecto. La respuesta correcta era: "${current.options[current.correct]}".`;
            }

            setTimeout(() => {
                currentQuestion++;
                if (currentQuestion < quizData.length) {
                    loadQuestion();
                } else {
                    showResults();
                }
            }, 1800);
        }

        function showResults() {
            questionEl.textContent = `¡Completado! Obtuviste ${score} de ${quizData.length} respuestas correctas.`;
            optionsEl.innerHTML = `<button class="quiz-btn" style="text-align:center; border-color: var(--accent-cyan);" onclick="restartQuiz()">Volver a intentar</button>`;
            feedbackEl.textContent = "";
        }

        function restartQuiz() {
            currentQuestion = 0;
            score = 0;
            loadQuestion();
        }

        loadQuestion();
    </script>
</body>
</html>
