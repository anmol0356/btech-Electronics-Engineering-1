<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Electronics Engineering Important Questions & Answers</title>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #0f172a;
            --secondary: #1e293b;
            --accent: #3b82f6;
            --accent-dark: #2563eb;
            --bg-dark: #0f172a;
            --bg-light: #f8fafc;
            --text-dark: #0f172a;
            --text-light: #64748b;
            --border: #e2e8f0;
            --success: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(to bottom, #f8fafc 0%, #e0f2fe 100%);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .header {
            background: linear-gradient(135deg, #0f172a 0%, #1e40af 50%, #3b82f6 100%);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(45deg, transparent 30%, rgba(255,255,255,0.05) 30%, rgba(255,255,255,0.05) 70%, transparent 70%),
                linear-gradient(-45deg, transparent 30%, rgba(255,255,255,0.05) 30%, rgba(255,255,255,0.05) 70%, transparent 70%);
            background-size: 100px 100px;
            animation: slide 20s linear infinite;
        }

        @keyframes slide {
            0% { transform: translate(0, 0); }
            100% { transform: translate(100px, 100px); }
        }

        .header h1 {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            position: relative;
            z-index: 1;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .header p {
            font-size: 1.2rem;
            opacity: 0.95;
            position: relative;
            z-index: 1;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 2rem;
            display: grid;
            grid-template-columns: 300px 1fr;
            gap: 2rem;
            align-items: start;
        }

        .sidebar {
            position: sticky;
            top: 2rem;
            background: white;
            border-radius: 20px;
            padding: 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            border: 1px solid var(--border);
        }

        .sidebar h3 {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
            border-bottom: 3px solid var(--accent);
            padding-bottom: 0.75rem;
        }

        .nav-link {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 0.875rem 1.25rem;
            margin: 0.5rem 0;
            color: var(--text-light);
            text-decoration: none;
            border-radius: 12px;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            font-weight: 500;
            position: relative;
        }

        .nav-link::before {
            content: '';
            width: 6px;
            height: 6px;
            background: var(--text-light);
            border-radius: 50%;
            transition: all 0.3s ease;
        }

        .nav-link:hover {
            background: linear-gradient(135deg, #eff6ff 0%, #dbeafe 100%);
            color: var(--accent);
            transform: translateX(8px);
        }

        .nav-link:hover::before {
            background: var(--accent);
            transform: scale(1.5);
        }

        .nav-link.active {
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
            color: white;
            box-shadow: 0 4px 12px rgba(59, 130, 246, 0.3);
        }

        .nav-link.active::before {
            background: white;
        }

        .main-content {
            min-height: 100vh;
        }

        .subject-section {
            background: white;
            border-radius: 20px;
            padding: 3rem;
            margin-bottom: 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            border: 1px solid var(--border);
            animation: fadeInUp 0.6s ease;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .subject-title {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .subject-title::before {
            content: '';
            width: 5px;
            height: 3rem;
            background: linear-gradient(180deg, var(--accent) 0%, var(--accent-dark) 100%);
            border-radius: 3px;
        }

        .subject-desc {
            color: var(--text-light);
            margin-bottom: 2.5rem;
            font-size: 1.1rem;
        }

        .question-card {
            border: 2px solid var(--border);
            border-radius: 16px;
            margin-bottom: 1.5rem;
            overflow: hidden;
            transition: all 0.3s ease;
            background: white;
        }

        .question-card:hover {
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            border-color: var(--accent);
        }

        .question-header {
            background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
            padding: 1.75rem;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 1rem;
            transition: all 0.3s ease;
        }

        .question-header:hover {
            background: linear-gradient(135deg, #eff6ff 0%, #dbeafe 100%);
        }

        .question-text {
            font-weight: 600;
            color: var(--text-dark);
            font-size: 1.1rem;
            flex: 1;
        }

        .toggle-icon {
            font-size: 1.75rem;
            color: var(--accent);
            transition: transform 0.3s ease;
            font-weight: bold;
            min-width: 30px;
            text-align: center;
        }

        .question-card.active .toggle-icon {
            transform: rotate(45deg);
        }

        .answer-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease, padding 0.4s ease;
        }

        .question-card.active .answer-content {
            max-height: 3000px;
            padding: 2rem;
            border-top: 2px solid var(--border);
        }

        .answer-content h4 {
            color: var(--primary);
            margin-top: 1.5rem;
            margin-bottom: 0.75rem;
            font-size: 1.2rem;
            font-family: 'Space Grotesk', sans-serif;
        }

        .answer-content h4:first-child {
            margin-top: 0;
        }

        .answer-content p {
            color: var(--text-dark);
            margin-bottom: 1.25rem;
            line-height: 1.8;
        }

        .answer-content ul, .answer-content ol {
            margin-left: 1.75rem;
            margin-bottom: 1.25rem;
            color: var(--text-dark);
        }

        .answer-content li {
            margin-bottom: 0.75rem;
            line-height: 1.8;
        }

        .answer-content code {
            background: #1e293b;
            color: #60a5fa;
            padding: 0.25rem 0.6rem;
            border-radius: 6px;
            font-family: 'Courier New', monospace;
            font-size: 0.9rem;
        }

        .answer-content pre {
            background: #1e293b;
            color: #e2e8f0;
            padding: 1.5rem;
            border-radius: 12px;
            overflow-x: auto;
            margin: 1.25rem 0;
            border-left: 4px solid var(--accent);
        }

        .answer-content pre code {
            background: transparent;
            color: #e2e8f0;
            padding: 0;
        }

        .formula-box {
            background: linear-gradient(135deg, #eff6ff 0%, #dbeafe 100%);
            border-left: 4px solid var(--accent);
            padding: 1.25rem;
            margin: 1.25rem 0;
            border-radius: 8px;
            font-family: 'Courier New', monospace;
            font-size: 1.1rem;
            color: var(--primary);
        }

        .key-point {
            background: linear-gradient(135deg, #fef3c7 0%, #fde68a 100%);
            border-left: 4px solid var(--warning);
            padding: 1.25rem;
            margin: 1.25rem 0;
            border-radius: 8px;
        }

        .note-box {
            background: linear-gradient(135deg, #ecfdf5 0%, #d1fae5 100%);
            border-left: 4px solid var(--success);
            padding: 1.25rem;
            margin: 1.25rem 0;
            border-radius: 8px;
        }

        .difficulty {
            display: inline-block;
            padding: 0.4rem 1rem;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-left: 0.75rem;
        }

        .difficulty.easy {
            background: linear-gradient(135deg, #d1fae5 0%, #a7f3d0 100%);
            color: #047857;
        }

        .difficulty.medium {
            background: linear-gradient(135deg, #fed7aa 0%, #fdba74 100%);
            color: #c2410c;
        }

        .difficulty.hard {
            background: linear-gradient(135deg, #fecaca 0%, #fca5a5 100%);
            color: #b91c1c;
        }

        @media (max-width: 968px) {
            .container {
                grid-template-columns: 1fr;
            }

            .sidebar {
                position: static;
            }

            .header h1 {
                font-size: 2.5rem;
            }

            .subject-title {
                font-size: 2rem;
            }
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .stat-card {
            background: linear-gradient(135deg, #0f172a 0%, #1e40af 100%);
            color: white;
            padding: 2rem;
            border-radius: 16px;
            text-align: center;
            box-shadow: 0 8px 20px rgba(15, 23, 42, 0.3);
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            font-family: 'Space Grotesk', sans-serif;
        }

        .stat-label {
            opacity: 0.9;
            margin-top: 0.5rem;
            font-size: 1.1rem;
        }

        .circuit-diagram {
            background: white;
            border: 2px solid var(--border);
            border-radius: 12px;
            padding: 1.5rem;
            margin: 1.25rem 0;
            text-align: center;
            font-family: monospace;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1.25rem 0;
            background: white;
        }

        table th {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            padding: 1rem;
            text-align: left;
            font-weight: 600;
        }

        table td {
            padding: 1rem;
            border: 1px solid var(--border);
        }

        table tr:nth-child(even) {
            background: #f8fafc;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>⚡ Electronics Engineering Q&A</h1>
        <p>Comprehensive guide with detailed explanations for core electronics subjects</p>
    </div>

    <div class="container">
        <aside class="sidebar">
            <h3>📚 Subjects</h3>
            <a href="#circuit" class="nav-link">Circuit Theory</a>
            <a href="#digital" class="nav-link">Digital Electronics</a>
            <a href="#analog" class="nav-link">Analog Electronics</a>
            <a href="#devices" class="nav-link">Electronic Devices</a>
            <a href="#microprocessor" class="nav-link">Microprocessors</a>
            <a href="#communication" class="nav-link">Communication</a>
            <a href="#control" class="nav-link">Control Systems</a>
            <a href="#power" class="nav-link">Power Electronics</a>
        </aside>

        <main class="main-content">
            <div class="stats">
                <div class="stat-card">
                    <div class="stat-number">8</div>
                    <div class="stat-label">Core Subjects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">75+</div>
                    <div class="stat-label">Important Questions</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Detailed Solutions</div>
                </div>
            </div>

            <!-- Circuit Theory -->
            <section id="circuit" class="subject-section">
                <h2 class="subject-title">Circuit Theory</h2>
                <p class="subject-desc">Fundamental concepts of electric circuits, network theorems, and AC/DC analysis</p>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">1. State and explain Kirchhoff's Current Law (KCL) and Kirchhoff's Voltage Law (KVL).
                            <span class="difficulty easy">Easy</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>Kirchhoff's Current Law (KCL):</h4>
                        <p>The algebraic sum of all currents entering and leaving a node (junction) is zero. In other words, the total current entering a node equals the total current leaving it.</p>
                        
                        <div class="formula-box">
                            ΣI<sub>in</sub> = ΣI<sub>out</sub><br>
                            or<br>
                            ΣI = 0 (at a node)
                        </div>

                        <p><strong>Physical Basis:</strong> Law of conservation of charge - charge cannot accumulate at a node.</p>
                        
                        <p><strong>Example:</strong> If currents I₁ = 5A and I₂ = 3A enter a node, and I₃ = 2A and I₄ leave the node, then:</p>
                        <ul>
                            <li>I₁ + I₂ = I₃ + I₄</li>
                            <li>5 + 3 = 2 + I₄</li>
                            <li>I₄ = 6A</li>
                        </ul>

                        <h4>Kirchhoff's Voltage Law (KVL):</h4>
                        <p>The algebraic sum of all voltages around any closed loop in a circuit is zero.</p>

                        <div class="formula-box">
                            ΣV = 0 (around a closed loop)
                        </div>

                        <p><strong>Physical Basis:</strong> Law of conservation of energy - energy supplied equals energy consumed in a closed path.</p>

                        <p><strong>Sign Convention:</strong></p>
                        <ul>
                            <li>Voltage rise (- to +): Positive</li>
                            <li>Voltage drop (+ to -): Negative</li>
                        </ul>

                        <div class="key-point">
                            <strong>Applications:</strong> KCL and KVL are fundamental for circuit analysis and form the basis for methods like Mesh Analysis and Nodal Analysis.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">2. Explain Thevenin's Theorem with an example.
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>Thevenin's Theorem states that any linear electrical network with voltage sources, current sources, and resistances can be replaced by an equivalent circuit consisting of a single voltage source (V<sub>TH</sub>) in series with a single resistance (R<sub>TH</sub>).</p>

                        <h4>Steps to Find Thevenin Equivalent:</h4>
                        <ol>
                            <li><strong>Remove Load Resistance:</strong> Identify and remove the load resistance where you want to find the equivalent</li>
                            <li><strong>Find V<sub>TH</sub>:</strong> Calculate open-circuit voltage across the terminals</li>
                            <li><strong>Find R<sub>TH</sub>:</strong>
                                <ul>
                                    <li>Deactivate all independent sources (short voltage sources, open current sources)</li>
                                    <li>Calculate resistance seen from the terminals</li>
                                </ul>
                            </li>
                            <li><strong>Draw Equivalent:</strong> Connect V<sub>TH</sub> in series with R<sub>TH</sub></li>
                        </ol>

                        <h4>Example Problem:</h4>
                        <p>Consider a circuit with a 12V source, two resistors R₁ = 4Ω and R₂ = 6Ω in series, and load R<sub>L</sub> = 10Ω connected across R₂.</p>

                        <p><strong>Step 1:</strong> Remove R<sub>L</sub></p>
                        
                        <p><strong>Step 2:</strong> Find V<sub>TH</sub> (voltage across R₂)</p>
                        <div class="formula-box">
                            V<sub>TH</sub> = V × R₂/(R₁ + R₂)<br>
                            V<sub>TH</sub> = 12 × 6/(4 + 6)<br>
                            V<sub>TH</sub> = 7.2V
                        </div>

                        <p><strong>Step 3:</strong> Find R<sub>TH</sub> (short the voltage source)</p>
                        <div class="formula-box">
                            R<sub>TH</sub> = R₁ || R₂ = (R₁ × R₂)/(R₁ + R₂)<br>
                            R<sub>TH</sub> = (4 × 6)/(4 + 6)<br>
                            R<sub>TH</sub> = 2.4Ω
                        </div>

                        <div class="key-point">
                            <strong>Advantage:</strong> Simplifies analysis when calculating current/voltage for different load values. Particularly useful in power transfer calculations.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">3. Explain the difference between AC and DC. Derive RMS value of sinusoidal waveform.
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>AC vs DC Comparison:</h4>
                        
                        <table>
                            <tr>
                                <th>Aspect</th>
                                <th>DC (Direct Current)</th>
                                <th>AC (Alternating Current)</th>
                            </tr>
                            <tr>
                                <td>Direction</td>
                                <td>Unidirectional</td>
                                <td>Bidirectional (changes periodically)</td>
                            </tr>
                            <tr>
                                <td>Magnitude</td>
                                <td>Constant</td>
                                <td>Varies sinusoidally</td>
                            </tr>
                            <tr>
                                <td>Frequency</td>
                                <td>0 Hz</td>
                                <td>50/60 Hz (power), higher for signals</td>
                            </tr>
                            <tr>
                                <td>Transmission</td>
                                <td>Higher losses over long distance</td>
                                <td>Lower losses (can use transformers)</td>
                            </tr>
                            <tr>
                                <td>Generation</td>
                                <td>Batteries, solar cells, DC generators</td>
                                <td>AC generators (alternators)</td>
                            </tr>
                            <tr>
                                <td>Applications</td>
                                <td>Electronics, batteries, EV</td>
                                <td>Power distribution, motors, heating</td>
                            </tr>
                        </table>

                        <h4>RMS (Root Mean Square) Value Derivation:</h4>
                        <p>RMS value is the equivalent DC value that produces the same heating effect as AC.</p>

                        <p>For sinusoidal AC voltage: v(t) = V<sub>m</sub> sin(ωt)</p>

                        <div class="formula-box">
                            V<sub>RMS</sub> = √(1/T ∫₀ᵀ v²(t) dt)<br><br>
                            V<sub>RMS</sub> = √(1/T ∫₀ᵀ V<sub>m</sub>² sin²(ωt) dt)<br><br>
                            V<sub>RMS</sub> = V<sub>m</sub> √(1/T ∫₀ᵀ sin²(ωt) dt)<br><br>
                            Using: sin²(θ) = (1 - cos(2θ))/2<br><br>
                            V<sub>RMS</sub> = V<sub>m</sub> √(1/2)<br><br>
                            <strong>V<sub>RMS</sub> = V<sub>m</sub>/√2 = 0.707 V<sub>m</sub></strong>
                        </div>

                        <p><strong>Example:</strong> If peak voltage V<sub>m</sub> = 340V, then V<sub>RMS</sub> = 340/√2 ≈ 240V</p>

                        <div class="note-box">
                            <strong>Important:</strong> Similarly for current: I<sub>RMS</sub> = I<sub>m</sub>/√2. Power calculations in AC use RMS values: P = V<sub>RMS</sub> × I<sub>RMS</sub> × cos(φ)
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">4. What is Resonance in RLC circuits? Explain series and parallel resonance.
                            <span class="difficulty hard">Hard</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>Resonance occurs when the inductive reactance (X<sub>L</sub>) equals capacitive reactance (X<sub>C</sub>), resulting in purely resistive impedance.</p>

                        <h4>Series Resonance (RLC Series Circuit):</h4>
                        
                        <p><strong>Condition:</strong> X<sub>L</sub> = X<sub>C</sub></p>
                        
                        <div class="formula-box">
                            ωL = 1/(ωC)<br>
                            ω₀ = 1/√(LC)<br>
                            f₀ = 1/(2π√(LC)) Hz
                        </div>

                        <p><strong>Characteristics at Resonance:</strong></p>
                        <ul>
                            <li><strong>Impedance:</strong> Z = R (minimum, purely resistive)</li>
                            <li><strong>Current:</strong> Maximum (I = V/R)</li>
                            <li><strong>Voltage across L and C:</strong> Equal and opposite, can be >> source voltage</li>
                            <li><strong>Power Factor:</strong> Unity (cos φ = 1)</li>
                            <li><strong>Phase Angle:</strong> φ = 0° (voltage and current in phase)</li>
                        </ul>

                        <p><strong>Quality Factor (Q):</strong></p>
                        <div class="formula-box">
                            Q = ω₀L/R = 1/(ω₀CR) = (1/R)√(L/C)
                        </div>
                        <ul>
                            <li>Higher Q → Sharper resonance curve</li>
                            <li>Voltage magnification = Q</li>
                        </ul>

                        <p><strong>Bandwidth:</strong></p>
                        <div class="formula-box">
                            BW = f₀/Q = R/(2πL) Hz
                        </div>

                        <h4>Parallel Resonance (RLC Parallel Circuit):</h4>
                        
                        <p><strong>Condition:</strong> Same as series (X<sub>L</sub> = X<sub>C</sub>)</p>

                        <p><strong>Characteristics at Resonance:</strong></p>
                        <ul>
                            <li><strong>Impedance:</strong> Maximum (Z = L/CR for ideal case)</li>
                            <li><strong>Current:</strong> Minimum (from source)</li>
                            <li><strong>Branch Currents:</strong> Can be much larger than source current</li>
                            <li><strong>Power Factor:</strong> Unity</li>
                            <li><strong>Acts as:</strong> Current rejector (high impedance)</li>
                        </ul>

                        <h4>Comparison:</h4>
                        <table>
                            <tr>
                                <th>Parameter</th>
                                <th>Series Resonance</th>
                                <th>Parallel Resonance</th>
                            </tr>
                            <tr>
                                <td>Impedance</td>
                                <td>Minimum (= R)</td>
                                <td>Maximum</td>
                            </tr>
                            <tr>
                                <td>Current</td>
                                <td>Maximum</td>
                                <td>Minimum</td>
                            </tr>
                            <tr>
                                <td>Type</td>
                                <td>Voltage magnifier</td>
                                <td>Current magnifier</td>
                            </tr>
                            <tr>
                                <td>Application</td>
                                <td>Voltage selection, filters</td>
                                <td>Impedance matching, tank circuits</td>
                            </tr>
                        </table>

                        <div class="key-point">
                            <strong>Applications:</strong> Radio tuning circuits, filters, oscillators, impedance matching networks, wireless power transfer.
                        </div>
                    </div>
                </div>
            </section>

            <!-- Digital Electronics -->
            <section id="digital" class="subject-section">
                <h2 class="subject-title">Digital Electronics</h2>
                <p class="subject-desc">Logic gates, Boolean algebra, combinational and sequential circuits</p>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">1. Explain all basic logic gates with truth tables and symbols.
                            <span class="difficulty easy">Easy</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>1. AND Gate:</h4>
                        <p>Output is HIGH only when all inputs are HIGH.</p>
                        <div class="formula-box">
                            Y = A · B (or A AND B)
                        </div>
                        <table>
                            <tr><th>A</th><th>B</th><th>Y</th></tr>
                            <tr><td>0</td><td>0</td><td>0</td></tr>
                            <tr><td>0</td><td>1</td><td>0</td></tr>
                            <tr><td>1</td><td>0</td><td>0</td></tr>
                            <tr><td>1</td><td>1</td><td>1</td></tr>
                        </table>

                        <h4>2. OR Gate:</h4>
                        <p>Output is HIGH when at least one input is HIGH.</p>
                        <div class="formula-box">
                            Y = A + B (or A OR B)
                        </div>
                        <table>
                            <tr><th>A</th><th>B</th><th>Y</th></tr>
                            <tr><td>0</td><td>0</td><td>0</td></tr>
                            <tr><td>0</td><td>1</td><td>1</td></tr>
                            <tr><td>1</td><td>0</td><td>1</td></tr>
                            <tr><td>1</td><td>1</td><td>1</td></tr>
                        </table>

                        <h4>3. NOT Gate (Inverter):</h4>
                        <p>Output is complement of input.</p>
                        <div class="formula-box">
                            Y = Ā (or NOT A)
                        </div>
                        <table>
                            <tr><th>A</th><th>Y</th></tr>
                            <tr><td>0</td><td>1</td></tr>
                            <tr><td>1</td><td>0</td></tr>
                        </table>

                        <h4>4. NAND Gate:</h4>
                        <p>Output is complement of AND gate. Universal gate.</p>
                        <div class="formula-box">
                            Y = (A · B)' or NAND(A,B)
                        </div>
                        <table>
                            <tr><th>A</th><th>B</th><th>Y</th></tr>
                            <tr><td>0</td><td>0</td><td>1</td></tr>
                            <tr><td>0</td><td>1</td><td>1</td></tr>
                            <tr><td>1</td><td>0</td><td>1</td></tr>
                            <tr><td>1</td><td>1</td><td>0</td></tr>
                        </table>

                        <h4>5. NOR Gate:</h4>
                        <p>Output is complement of OR gate. Universal gate.</p>
                        <div class="formula-box">
                            Y = (A + B)' or NOR(A,B)
                        </div>
                        <table>
                            <tr><th>A</th><th>B</th><th>Y</th></tr>
                            <tr><td>0</td><td>0</td><td>1</td></tr>
                            <tr><td>0</td><td>1</td><td>0</td></tr>
                            <tr><td>1</td><td>0</td><td>0</td></tr>
                            <tr><td>1</td><td>1</td><td>0</td></tr>
                        </table>

                        <h4>6. XOR Gate (Exclusive OR):</h4>
                        <p>Output is HIGH when inputs are different.</p>
                        <div class="formula-box">
                            Y = A ⊕ B = A'B + AB'
                        </div>
                        <table>
                            <tr><th>A</th><th>B</th><th>Y</th></tr>
                            <tr><td>0</td><td>0</td><td>0</td></tr>
                            <tr><td>0</td><td>1</td><td>1</td></tr>
                            <tr><td>1</td><td>0</td><td>1</td></tr>
                            <tr><td>1</td><td>1</td><td>0</td></tr>
                        </table>

                        <h4>7. XNOR Gate (Exclusive NOR):</h4>
                        <p>Output is HIGH when inputs are same.</p>
                        <div class="formula-box">
                            Y = (A ⊕ B)' = AB + A'B'
                        </div>
                        <table>
                            <tr><th>A</th><th>B</th><th>Y</th></tr>
                            <tr><td>0</td><td>0</td><td>1</td></tr>
                            <tr><td>0</td><td>1</td><td>0</td></tr>
                            <tr><td>1</td><td>0</td><td>0</td></tr>
                            <tr><td>1</td><td>1</td><td>1</td></tr>
                        </table>

                        <div class="key-point">
                            <strong>Universal Gates:</strong> NAND and NOR are called universal gates because any logic function can be implemented using only NAND or only NOR gates.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">2. State and prove De Morgan's Theorems.
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>De Morgan's Theorems:</h4>
                        <p>Two fundamental theorems in Boolean algebra that show relationship between AND, OR, and NOT operations.</p>

                        <h4>First Theorem:</h4>
                        <div class="formula-box">
                            (A + B)' = A' · B'
                        </div>
                        <p>The complement of OR equals AND of complements.</p>
                        <p>"Break the bar, change the sign"</p>

                        <h4>Second Theorem:</h4>
                        <div class="formula-box">
                            (A · B)' = A' + B'
                        </div>
                        <p>The complement of AND equals OR of complements.</p>

                        <h4>Proof using Truth Table (First Theorem):</h4>
                        <table>
                            <tr>
                                <th>A</th>
                                <th>B</th>
                                <th>A + B</th>
                                <th>(A + B)'</th>
                                <th>A'</th>
                                <th>B'</th>
                                <th>A' · B'</th>
                            </tr>
                            <tr><td>0</td><td>0</td><td>0</td><td>1</td><td>1</td><td>1</td><td>1</td></tr>
                            <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td><td>0</td><td>0</td></tr>
                            <tr><td>1</td><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td><td>0</td></tr>
                            <tr><td>1</td><td>1</td><td>1</td><td>0</td><td>0</td><td>0</td><td>0</td></tr>
                        </table>
                        <p>Columns (A + B)' and A' · B' are identical ✓</p>

                        <h4>Proof using Truth Table (Second Theorem):</h4>
                        <table>
                            <tr>
                                <th>A</th>
                                <th>B</th>
                                <th>A · B</th>
                                <th>(A · B)'</th>
                                <th>A'</th>
                                <th>B'</th>
                                <th>A' + B'</th>
                            </tr>
                            <tr><td>0</td><td>0</td><td>0</td><td>1</td><td>1</td><td>1</td><td>1</td></tr>
                            <tr><td>0</td><td>1</td><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
                            <tr><td>1</td><td>0</td><td>0</td><td>1</td><td>0</td><td>1</td><td>1</td></tr>
                            <tr><td>1</td><td>1</td><td>1</td><td>0</td><td>0</td><td>0</td><td>0</td></tr>
                        </table>
                        <p>Columns (A · B)' and A' + B' are identical ✓</p>

                        <h4>Applications:</h4>
                        <ul>
                            <li>Simplifying Boolean expressions</li>
                            <li>Converting between NAND and NOR implementations</li>
                            <li>Logic circuit minimization</li>
                            <li>Complementing complex functions</li>
                        </ul>

                        <h4>Extended Form (for n variables):</h4>
                        <div class="formula-box">
                            (A + B + C + ... + N)' = A' · B' · C' · ... · N'<br>
                            (A · B · C · ... · N)' = A' + B' + C' + ... + N'
                        </div>

                        <div class="key-point">
                            <strong>Memory Tip:</strong> "Break the line, change the sign" - When you break the overline (complement), change the operation (+ ↔ ·).
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">3. What is a Flip-Flop? Explain different types of flip-flops.
                            <span class="difficulty hard">Hard</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>A flip-flop is a bistable multivibrator - a sequential circuit with two stable states that can store one bit of information. It's the basic storage element in sequential logic circuits.</p>

                        <h4>1. SR Flip-Flop (Set-Reset):</h4>
                        <p><strong>Inputs:</strong> S (Set), R (Reset), CLK (optional)</p>
                        <p><strong>Operation:</strong></p>
                        <ul>
                            <li>S = 1, R = 0: Set (Q = 1)</li>
                            <li>S = 0, R = 1: Reset (Q = 0)</li>
                            <li>S = 0, R = 0: Hold (No change)</li>
                            <li>S = 1, R = 1: Invalid/Forbidden state</li>
                        </ul>

                        <h4>2. D Flip-Flop (Data/Delay):</h4>
                        <p><strong>Inputs:</strong> D (Data), CLK</p>
                        <p><strong>Operation:</strong></p>
                        <ul>
                            <li>Q follows D at clock edge</li>
                            <li>D = 0 → Q = 0</li>
                            <li>D = 1 → Q = 1</li>
                            <li>No invalid states</li>
                        </ul>
                        <p><strong>Applications:</strong> Data storage, shift registers, frequency division</p>

                        <h4>3. JK Flip-Flop:</h4>
                        <p><strong>Inputs:</strong> J, K, CLK</p>
                        <p><strong>Operation:</strong></p>
                        <ul>
                            <li>J = 0, K = 0: Hold (No change)</li>
                            <li>J = 0, K = 1: Reset (Q = 0)</li>
                            <li>J = 1, K = 0: Set (Q = 1)</li>
                            <li>J = 1, K = 1: Toggle (Q → Q')</li>
                        </ul>
                        <p><strong>Characteristic Equation:</strong></p>
                        <div class="formula-box">
                            Q<sub>next</sub> = JQ' + K'Q
                        </div>
                        <p><strong>Advantage:</strong> No invalid state (solves SR flip-flop problem)</p>

                        <h4>4. T Flip-Flop (Toggle):</h4>
                        <p><strong>Inputs:</strong> T (Toggle), CLK</p>
                        <p><strong>Operation:</strong></p>
                        <ul>
                            <li>T = 0: Hold (Q<sub>next</sub> = Q)</li>
                            <li>T = 1: Toggle (Q<sub>next</sub> = Q')</li>
                        </ul>
                        <p><strong>Characteristic Equation:</strong></p>
                        <div class="formula-box">
                            Q<sub>next</sub> = TQ' + T'Q = T ⊕ Q
                        </div>
                        <p><strong>Applications:</strong> Counters, frequency dividers</p>

                        <h4>Clock Triggering:</h4>
                        <ul>
                            <li><strong>Level Triggered:</strong> Responds during entire clock pulse</li>
                            <li><strong>Edge Triggered:</strong> Responds only at clock edge
                                <ul>
                                    <li>Positive Edge: 0 → 1 transition</li>
                                    <li>Negative Edge: 1 → 0 transition</li>
                                </ul>
                            </li>
                        </ul>

                        <h4>Comparison Table:</h4>
                        <table>
                            <tr>
                                <th>Type</th>
                                <th>Inputs</th>
                                <th>Key Feature</th>
                                <th>Application</th>
                            </tr>
                            <tr>
                                <td>SR</td>
                                <td>S, R</td>
                                <td>Has invalid state</td>
                                <td>Basic latches</td>
                            </tr>
                            <tr>
                                <td>D</td>
                                <td>D</td>
                                <td>Single input, no invalid state</td>
                                <td>Data storage, registers</td>
                            </tr>
                            <tr>
                                <td>JK</td>
                                <td>J, K</td>
                                <td>No invalid state, can toggle</td>
                                <td>General purpose</td>
                            </tr>
                            <tr>
                                <td>T</td>
                                <td>T</td>
                                <td>Toggle mode</td>
                                <td>Counters, dividers</td>
                            </tr>
                        </table>

                        <div class="key-point">
                            <strong>Master-Slave Configuration:</strong> Used to prevent race conditions in level-triggered flip-flops. Two flip-flops in series with inverted clocks.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">4. Design a 4-bit binary counter using JK flip-flops.
                            <span class="difficulty hard">Hard</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>A 4-bit binary counter counts from 0000 to 1111 (0 to 15) and then repeats.</p>

                        <h4>Design Steps:</h4>
                        
                        <p><strong>Step 1: State Table</strong></p>
                        <table>
                            <tr>
                                <th>Count</th>
                                <th>Q₃</th>
                                <th>Q₂</th>
                                <th>Q₁</th>
                                <th>Q₀</th>
                            </tr>
                            <tr><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td></tr>
                            <tr><td>1</td><td>0</td><td>0</td><td>0</td><td>1</td></tr>
                            <tr><td>2</td><td>0</td><td>0</td><td>1</td><td>0</td></tr>
                            <tr><td>...</td><td>...</td><td>...</td><td>...</td><td>...</td></tr>
                            <tr><td>15</td><td>1</td><td>1</td><td>1</td><td>1</td></tr>
                        </table>

                        <p><strong>Step 2: JK Excitation</strong></p>
                        <p>For JK flip-flop transitions:</p>
                        <ul>
                            <li>0 → 0: J = 0, K = X (don't care)</li>
                            <li>0 → 1: J = 1, K = X</li>
                            <li>1 → 0: J = X, K = 1</li>
                            <li>1 → 1: J = X, K = 0</li>
                        </ul>

                        <p><strong>Step 3: Circuit Implementation</strong></p>
                        <p>For asynchronous (ripple) counter:</p>
                        <ul>
                            <li>All J and K inputs tied HIGH (J = K = 1 for toggle mode)</li>
                            <li>LSB (Q₀) receives clock directly</li>
                            <li>Each subsequent FF is clocked by previous FF output</li>
                            <li>Q₁ clocked by Q₀, Q₂ clocked by Q₁, Q₃ clocked by Q₂</li>
                        </ul>

                        <div class="circuit-diagram">
                            <pre>
CLK ──┐
      ├──> FF0 (Q₀) ──┐
      │               ├──> FF1 (Q₁) ──┐
      │               │                ├──> FF2 (Q₂) ──┐
      │               │                │                ├──> FF3 (Q₃)
    All JK = 1                                          
            </pre>
                        </div>

                        <p><strong>For Synchronous Counter:</strong></p>
                        <ul>
                            <li>All FFs receive same clock</li>
                            <li>Logic equations:
                                <div class="formula-box">
                                    J₀ = K₀ = 1<br>
                                    J₁ = K₁ = Q₀<br>
                                    J₂ = K₂ = Q₀ · Q₁<br>
                                    J₃ = K₃ = Q₀ · Q₁ · Q₂
                                </div>
                            </li>
                        </ul>

                        <h4>Comparison:</h4>
                        <table>
                            <tr>
                                <th>Feature</th>
                                <th>Asynchronous Counter</th>
                                <th>Synchronous Counter</th>
                            </tr>
                            <tr>
                                <td>Clock</td>
                                <td>Different for each FF</td>
                                <td>Same for all FFs</td>
                            </tr>
                            <tr>
                                <td>Speed</td>
                                <td>Slower (propagation delay)</td>
                                <td>Faster</td>
                            </tr>
                            <tr>
                                <td>Complexity</td>
                                <td>Simple</td>
                                <td>More complex</td>
                            </tr>
                            <tr>
                                <td>Power</td>
                                <td>Lower</td>
                                <td>Higher</td>
                            </tr>
                        </table>

                        <div class="note-box">
                            <strong>Modulus:</strong> For mod-N counter, use N states and reset when count reaches N. For mod-10 (decade counter), reset at count 10 (1010).
                        </div>
                    </div>
                </div>
            </section>

            <!-- Analog Electronics -->
            <section id="analog" class="subject-section">
                <h2 class="subject-title">Analog Electronics</h2>
                <p class="subject-desc">Operational amplifiers, oscillators, and analog circuit design</p>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">1. Explain ideal and practical characteristics of an Operational Amplifier (Op-Amp).
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>An operational amplifier is a high-gain differential amplifier with very high input impedance and very low output impedance.</p>

                        <h4>Ideal Op-Amp Characteristics:</h4>
                        <ul>
                            <li><strong>Open-loop gain (A<sub>OL</sub>):</strong> Infinite (∞)</li>
                            <li><strong>Input impedance (Z<sub>in</sub>):</strong> Infinite (∞)</li>
                            <li><strong>Output impedance (Z<sub>out</sub>):</strong> Zero (0)</li>
                            <li><strong>Bandwidth:</strong> Infinite</li>
                            <li><strong>Input bias current:</strong> Zero</li>
                            <li><strong>Input offset voltage:</strong> Zero</li>
                            <li><strong>CMRR (Common Mode Rejection Ratio):</strong> Infinite</li>
                            <li><strong>Slew rate:</strong> Infinite</li>
                            <li><strong>Power consumption:</strong> Zero</li>
                            <li><strong>Output can swing:</strong> Full supply voltage range</li>
                        </ul>

                        <h4>Practical Op-Amp Characteristics (e.g., 741):</h4>
                        <table>
                            <tr>
                                <th>Parameter</th>
                                <th>Typical Value</th>
                            </tr>
                            <tr>
                                <td>Open-loop gain</td>
                                <td>100,000 to 200,000 (100 dB)</td>
                            </tr>
                            <tr>
                                <td>Input impedance</td>
                                <td>1-10 MΩ</td>
                            </tr>
                            <tr>
                                <td>Output impedance</td>
                                <td>50-100 Ω</td>
                            </tr>
                            <tr>
                                <td>Bandwidth</td>
                                <td>1 MHz (unity gain)</td>
                            </tr>
                            <tr>
                                <td>Input bias current</td>
                                <td>20-500 nA</td>
                            </tr>
                            <tr>
                                <td>Input offset voltage</td>
                                <td>1-5 mV</td>
                            </tr>
                            <tr>
                                <td>CMRR</td>
                                <td>70-90 dB</td>
                            </tr>
                            <tr>
                                <td>Slew rate</td>
                                <td>0.5-2 V/μs</td>
                            </tr>
                        </table>

                        <h4>Golden Rules of Op-Amp (in negative feedback):</h4>
                        <ol>
                            <li><strong>No current flows into the input terminals</strong> (I<sub>in</sub> = 0)</li>
                            <li><strong>The voltage difference between inputs is zero</strong> (V<sub>+</sub> = V<sub>-</sub>)</li>
                        </ol>

                        <h4>Important Definitions:</h4>
                        <p><strong>CMRR (Common Mode Rejection Ratio):</strong></p>
                        <div class="formula-box">
                            CMRR = 20 log(A<sub>d</sub>/A<sub>c</sub>) dB
                        </div>
                        <p>Where A<sub>d</sub> = differential gain, A<sub>c</sub> = common mode gain</p>

                        <p><strong>Slew Rate:</strong> Maximum rate of change of output voltage</p>
                        <div class="formula-box">
                            SR = dV<sub>out</sub>/dt (V/μs)
                        </div>

                        <div class="key-point">
                            <strong>Gain-Bandwidth Product:</strong> Constant for a given op-amp. GBW = A × BW. Higher gain → Lower bandwidth.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">2. Design and analyze Inverting and Non-Inverting amplifiers.
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>1. Inverting Amplifier:</h4>
                        <p>Input applied to inverting terminal (-), non-inverting terminal (+) grounded.</p>

                        <p><strong>Circuit Configuration:</strong></p>
                        <ul>
                            <li>Input through resistor R₁ to inverting input</li>
                            <li>Feedback resistor R<sub>f</sub> from output to inverting input</li>
                            <li>Non-inverting input grounded</li>
                        </ul>

                        <p><strong>Voltage Gain:</strong></p>
                        <div class="formula-box">
                            A<sub>v</sub> = V<sub>out</sub>/V<sub>in</sub> = -R<sub>f</sub>/R₁
                        </div>
                        <p>Negative sign indicates 180° phase shift</p>

                        <p><strong>Input Impedance:</strong></p>
                        <div class="formula-box">
                            Z<sub>in</sub> = R₁
                        </div>

                        <p><strong>Output Impedance:</strong></p>
                        <div class="formula-box">
                            Z<sub>out</sub> ≈ 0 (very low)
                        </div>

                        <p><strong>Example:</strong> If R₁ = 10kΩ, R<sub>f</sub> = 100kΩ</p>
                        <ul>
                            <li>Gain = -100k/10k = -10</li>
                            <li>For V<sub>in</sub> = 1V, V<sub>out</sub> = -10V</li>
                        </ul>

                        <h4>2. Non-Inverting Amplifier:</h4>
                        <p>Input applied to non-inverting terminal (+), inverting terminal (-) connected to feedback network.</p>

                        <p><strong>Circuit Configuration:</strong></p>
                        <ul>
                            <li>Input directly to non-inverting input</li>
                            <li>R₁ from inverting input to ground</li>
                            <li>R<sub>f</sub> from output to inverting input</li>
                        </ul>

                        <p><strong>Voltage Gain:</strong></p>
                        <div class="formula-box">
                            A<sub>v</sub> = V<sub>out</sub>/V<sub>in</sub> = 1 + (R<sub>f</sub>/R₁)
                        </div>
                        <p>No phase shift (0°)</p>

                        <p><strong>Input Impedance:</strong></p>
                        <div class="formula-box">
                            Z<sub>in</sub> = Very High (MΩ range)
                        </div>

                        <p><strong>Output Impedance:</strong></p>
                        <div class="formula-box">
                            Z<sub>out</sub> ≈ 0 (very low)
                        </div>

                        <p><strong>Example:</strong> If R₁ = 10kΩ, R<sub>f</sub> = 90kΩ</p>
                        <ul>
                            <li>Gain = 1 + 90k/10k = 10</li>
                            <li>For V<sub>in</sub> = 1V, V<sub>out</sub> = 10V</li>
                        </ul>

                        <h4>Comparison:</h4>
                        <table>
                            <tr>
                                <th>Parameter</th>
                                <th>Inverting</th>
                                <th>Non-Inverting</th>
                            </tr>
                            <tr>
                                <td>Gain</td>
                                <td>-R<sub>f</sub>/R₁</td>
                                <td>1 + R<sub>f</sub>/R₁</td>
                            </tr>
                            <tr>
                                <td>Phase Shift</td>
                                <td>180°</td>
                                <td>0°</td>
                            </tr>
                            <tr>
                                <td>Input Impedance</td>
                                <td>R₁ (Low)</td>
                                <td>Very High</td>
                            </tr>
                            <tr>
                                <td>Minimum Gain</td>
                                <td>Can be < 1</td>
                                <td>Minimum = 1</td>
                            </tr>
                        </table>

                        <h4>Voltage Follower (Unity Gain Buffer):</h4>
                        <p>Special case of non-inverting amplifier with R<sub>f</sub> = 0, R₁ = ∞</p>
                        <div class="formula-box">
                            Gain = 1, V<sub>out</sub> = V<sub>in</sub>
                        </div>
                        <p><strong>Use:</strong> Impedance matching, buffering</p>

                        <div class="note-box">
                            <strong>Design Tip:</strong> Choose non-inverting for high input impedance applications. Choose inverting when you need virtual ground or gain < 1.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">3. Explain different types of oscillators and their applications.
                            <span class="difficulty hard">Hard</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>An oscillator is a circuit that generates periodic waveforms (sine, square, triangle) without any external input signal.</p>

                        <h4>Barkhausen Criterion for Oscillation:</h4>
                        <p>For sustained oscillations:</p>
                        <ul>
                            <li><strong>Loop gain:</strong> |Aβ| = 1 (magnitude condition)</li>
                            <li><strong>Phase shift:</strong> ∠(Aβ) = 0° or 360° (phase condition)</li>
                        </ul>
                        <p>Where A = amplifier gain, β = feedback factor</p>

                        <h4>1. RC Phase Shift Oscillator:</h4>
                        <p><strong>Frequency:</strong></p>
                        <div class="formula-box">
                            f = 1/(2π√6 RC)
                        </div>
                        <p><strong>Features:</strong></p>
                        <ul>
                            <li>Uses 3 RC networks for 180° phase shift</li>
                            <li>Amplifier provides another 180°</li>
                            <li>Total = 360° (0°)</li>
                            <li>Produces sine wave</li>
                        </ul>
                        <p><strong>Applications:</strong> Audio frequency oscillators (20 Hz - 20 kHz)</p>

                        <h4>2. Wien Bridge Oscillator:</h4>
                        <p><strong>Frequency:</strong></p>
                        <div class="formula-box">
                            f = 1/(2πRC)
                        </div>
                        <p><strong>Features:</strong></p>
                        <ul>
                            <li>Uses RC bridge network</li>
                            <li>Low distortion sine wave</li>
                            <li>Requires gain = 3</li>
                            <li>Most popular audio frequency oscillator</li>
                        </ul>
                        <p><strong>Applications:</strong> Audio signal generators, test equipment</p>

                        <h4>3. Colpitts Oscillator:</h4>
                        <p><strong>Frequency:</strong></p>
                        <div class="formula-box">
                            f = 1/(2π√(LC<sub>eq</sub>))
                        </div>
                        <p>Where C<sub>eq</sub> = C₁C₂/(C₁+C₂)</p>
                        <p><strong>Features:</strong></p>
                        <ul>
                            <li>Uses two capacitors and one inductor</li>
                            <li>Feedback through capacitive divider</li>
                            <li>Good frequency stability</li>
                            <li>Higher frequency range</li>
                        </ul>
                        <p><strong>Applications:</strong> RF oscillators, radio transmitters</p>

                        <h4>4. Hartley Oscillator:</h4>
                        <p><strong>Frequency:</strong></p>
                        <div class="formula-box">
                            f = 1/(2π√(L<sub>eq</sub>C))
                        </div>
                        <p>Where L<sub>eq</sub> = L₁ + L₂ + 2M</p>
                        <p><strong>Features:</strong></p>
                        <ul>
                            <li>Uses two inductors and one capacitor</li>
                            <li>Feedback through inductive divider</li>
                            <li>Frequency adjustment using variable capacitor</li>
                        </ul>
                        <p><strong>Applications:</strong> Radio receivers, RF generators</p>

                        <h4>5. Crystal Oscillator:</h4>
                        <p><strong>Features:</strong></p>
                        <ul>
                            <li>Uses piezoelectric crystal (usually quartz)</li>
                            <li>Extremely high frequency stability (±0.001%)</li>
                            <li>Fixed frequency (cannot be easily varied)</li>
                            <li>High Q factor (10,000 to 100,000)</li>
                        </ul>
                        <p><strong>Applications:</strong> Microprocessor clocks, digital watches, communication systems</p>

                        <h4>6. Astable Multivibrator (Square Wave):</h4>
                        <p><strong>Using 555 Timer:</strong></p>
                        <div class="formula-box">
                            f = 1.44/((R₁ + 2R₂)C)<br>
                            Duty Cycle = (R₁ + R₂)/(R₁ + 2R₂)
                        </div>
                        <p><strong>Applications:</strong> Pulse generation, LED flashers, clock signals</p>

                        <h4>Comparison:</h4>
                        <table>
                            <tr>
                                <th>Type</th>
                                <th>Frequency Range</th>
                                <th>Waveform</th>
                                <th>Stability</th>
                            </tr>
                            <tr>
                                <td>RC Phase Shift</td>
                                <td>Audio (20Hz-20kHz)</td>
                                <td>Sine</td>
                                <td>Moderate</td>
                            </tr>
                            <tr>
                                <td>Wien Bridge</td>
                                <td>Audio</td>
                                <td>Sine (low distortion)</td>
                                <td>Good</td>
                            </tr>
                            <tr>
                                <td>Colpitts</td>
                                <td>RF (>1MHz)</td>
                                <td>Sine</td>
                                <td>Good</td>
                            </tr>
                            <tr>
                                <td>Hartley</td>
                                <td>RF</td>
                                <td>Sine</td>
                                <td>Good</td>
                            </tr>
                            <tr>
                                <td>Crystal</td>
                                <td>Fixed</td>
                                <td>Sine</td>
                                <td>Excellent</td>
                            </tr>
                            <tr>
                                <td>Astable (555)</td>
                                <td>1Hz-500kHz</td>
                                <td>Square</td>
                                <td>Moderate</td>
                            </tr>
                        </table>

                        <div class="key-point">
                            <strong>Selection Guide:</strong> Use RC oscillators for audio, LC oscillators for RF, crystal for precision timing, 555 for square waves.
                        </div>
                    </div>
                </div>
            </section>

            <!-- Electronic Devices -->
            <section id="devices" class="subject-section">
                <h2 class="subject-title">Electronic Devices & Circuits</h2>
                <p class="subject-desc">Semiconductor devices, diodes, transistors, and amplifiers</p>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">1. Explain PN junction diode characteristics and applications.
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>PN Junction Diode:</h4>
                        <p>Formed by joining P-type and N-type semiconductors. Allows current in one direction (forward bias) and blocks in opposite direction (reverse bias).</p>

                        <h4>Formation:</h4>
                        <ul>
                            <li><strong>Depletion Region:</strong> Formed at junction due to diffusion and drift</li>
                            <li><strong>Barrier Potential:</strong> ~0.7V for Silicon, ~0.3V for Germanium</li>
                            <li><strong>Width:</strong> Depends on doping concentration</li>
                        </ul>

                        <h4>Forward Bias (P positive, N negative):</h4>
                        <ul>
                            <li>Depletion region narrows</li>
                            <li>Barrier potential reduced</li>
                            <li>Current flows when V > V<sub>barrier</sub></li>
                            <li>Low resistance (~25Ω)</li>
                            <li>Exponential I-V relationship</li>
                        </ul>

                        <h4>Reverse Bias (P negative, N positive):</h4>
                        <ul>
                            <li>Depletion region widens</li>
                            <li>Barrier potential increases</li>
                            <li>Only small leakage current (~μA)</li>
                            <li>High resistance (~MΩ)</li>
                            <li>Breakdown at high reverse voltage</li>
                        </ul>

                        <h4>Diode Equation:</h4>
                        <div class="formula-box">
                            I = I<sub>S</sub>(e<sup>V/ηV<sub>T</sub></sup> - 1)
                        </div>
                        <p>Where:</p>
                        <ul>
                            <li>I<sub>S</sub> = Saturation current</li>
                            <li>η = Ideality factor (1-2)</li>
                            <li>V<sub>T</sub> = Thermal voltage ≈ 26mV at 25°C</li>
                        </ul>

                        <h4>V-I Characteristics:</h4>
                        <ul>
                            <li><strong>Forward region:</strong> Exponential increase after barrier voltage</li>
                            <li><strong>Reverse region:</strong> Small constant leakage current</li>
                            <li><strong>Breakdown region:</strong> Sharp current increase (Zener/Avalanche)</li>
                        </ul>

                        <h4>Types of Diodes:</h4>
                        <ol>
                            <li><strong>Zener Diode:</strong> Operates in breakdown region, voltage regulation</li>
                            <li><strong>LED:</strong> Emits light in forward bias</li>
                            <li><strong>Photodiode:</strong> Generates current from light</li>
                            <li><strong>Schottky Diode:</strong> Fast switching, low forward voltage drop</li>
                            <li><strong>Varactor Diode:</strong> Variable capacitance, tuning circuits</li>
                        </ol>

                        <h4>Applications:</h4>
                        <ul>
                            <li><strong>Rectification:</strong> AC to DC conversion</li>
                            <li><strong>Clipping & Clamping:</strong> Waveform shaping</li>
                            <li><strong>Voltage Regulation:</strong> Using Zener diodes</li>
                            <li><strong>Demodulation:</strong> Extracting signals</li>
                            <li><strong>Protection:</strong> Preventing reverse polarity damage</li>
                        </ul>

                        <div class="key-point">
                            <strong>Important Parameters:</strong> Maximum forward current (I<sub>F</sub>), Peak inverse voltage (PIV), Power dissipation (P<sub>max</sub>), Switching time
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">2. Explain BJT (Bipolar Junction Transistor) working and configurations.
                            <span class="difficulty hard">Hard</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>BJT is a three-terminal semiconductor device with two PN junctions, used for amplification and switching.</p>

                        <h4>Structure & Types:</h4>
                        <ul>
                            <li><strong>NPN:</strong> N-P-N layers (Emitter-Base-Collector)</li>
                            <li><strong>PNP:</strong> P-N-P layers</li>
                            <li>Base is lightly doped and thin</li>
                            <li>Emitter is heavily doped</li>
                            <li>Collector is moderately doped and largest</li>
                        </ul>

                        <h4>Operating Principle (NPN in Active Mode):</h4>
                        <ol>
                            <li>Base-Emitter junction forward biased</li>
                            <li>Base-Collector junction reverse biased</li>
                            <li>Electrons injected from Emitter to Base</li>
                            <li>Most electrons (>98%) reach Collector</li>
                            <li>Small base current controls large collector current</li>
                        </ol>

                        <h4>Current Relationships:</h4>
                        <div class="formula-box">
                            I<sub>E</sub> = I<sub>B</sub> + I<sub>C</sub><br><br>
                            β (Current Gain) = I<sub>C</sub>/I<sub>B</sub> (typically 50-300)<br><br>
                            α = I<sub>C</sub>/I<sub>E</sub> (typically 0.95-0.99)<br><br>
                            β = α/(1-α)
                        </div>

                        <h4>Three Configurations:</h4>

                        <p><strong>1. Common Emitter (CE) - Most Popular:</strong></p>
                        <ul>
                            <li>Input: Base-Emitter, Output: Collector-Emitter</li>
                            <li>Voltage Gain: High (A<sub>v</sub> ≈ 100-500)</li>
                            <li>Current Gain: β (50-300)</li>
                            <li>Input Impedance: Medium (1-5 kΩ)</li>
                            <li>Output Impedance: High (20-50 kΩ)</li>
                            <li>Phase Shift: 180°</li>
                            <li><strong>Use:</strong> Voltage amplification</li>
                        </ul>

                        <p><strong>2. Common Base (CB):</strong></p>
                        <ul>
                            <li>Input: Emitter-Base, Output: Collector-Base</li>
                            <li>Voltage Gain: High (A<sub>v</sub> ≈ 200-1000)</li>
                            <li>Current Gain: α < 1 (≈0.98)</li>
                            <li>Input Impedance: Very Low (20-200 Ω)</li>
                            <li>Output Impedance: Very High (>100 kΩ)</li>
                            <li>Phase Shift: 0°</li>
                            <li><strong>Use:</strong> High-frequency applications, impedance matching</li>
                        </ul>

                        <p><strong>3. Common Collector (CC) - Emitter Follower:</strong></p>
                        <ul>
                            <li>Input: Base-Collector, Output: Emitter-Collector</li>
                            <li>Voltage Gain: <1 (A<sub>v</sub> ≈ 0.95-0.99)</li>
                            <li>Current Gain: High (1+β)</li>
                            <li>Input Impedance: Very High (50-500 kΩ)</li>
                            <li>Output Impedance: Very Low (25-100 Ω)</li>
                            <li>Phase Shift: 0°</li>
                            <li><strong>Use:</strong> Impedance matching, buffering</li>
                        </ul>

                        <h4>Comparison Table:</h4>
                        <table>
                            <tr>
                                <th>Parameter</th>
                                <th>CE</th>
                                <th>CB</th>
                                <th>CC</th>
                            </tr>
                            <tr>
                                <td>Voltage Gain</td>
                                <td>High</td>
                                <td>Very High</td>
                                <td><1</td>
                            </tr>
                            <tr>
                                <td>Current Gain</td>
                                <td>β</td>
                                <td>α (<1)</td>
                                <td>1+β</td>
                            </tr>
                            <tr>
                                <td>Z<sub>in</sub></td>
                                <td>Medium</td>
                                <td>Low</td>
                                <td>High</td>
                            </tr>
                            <tr>
                                <td>Z<sub>out</sub></td>
                                <td>High</td>
                                <td>Very High</td>
                                <td>Low</td>
                            </tr>
                            <tr>
                                <td>Phase Shift</td>
                                <td>180°</td>
                                <td>0°</td>
                                <td>0°</td>
                            </tr>
                            <tr>
                                <td>Application</td>
                                <td>Audio amp</td>
                                <td>RF amp</td>
                                <td>Buffer</td>
                            </tr>
                        </table>

                        <h4>Operating Regions:</h4>
                        <ul>
                            <li><strong>Active:</strong> Both junctions properly biased, for amplification</li>
                            <li><strong>Saturation:</strong> Both junctions forward biased, switch ON</li>
                            <li><strong>Cutoff:</strong> Both junctions reverse biased, switch OFF</li>
                            <li><strong>Inverse Active:</strong> Roles of E and C reversed (rarely used)</li>
                        </ul>

                        <div class="note-box">
                            <strong>Design Tip:</strong> Use CE for general amplification, CB for RF/high-frequency, CC for impedance matching and driving low-impedance loads.
                        </div>
                    </div>
                </div>
            </section>

            <!-- Microprocessor -->
            <section id="microprocessor" class="subject-section">
                <h2 class="subject-title">Microprocessors & Microcontrollers</h2>
                <p class="subject-desc">8085/8086 architecture, programming, and interfacing</p>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">1. Explain the architecture of 8085 microprocessor.
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>8085 is an 8-bit microprocessor manufactured by Intel, with 16-bit address bus and 8-bit data bus.</p>

                        <h4>Key Features:</h4>
                        <ul>
                            <li>8-bit data bus (D0-D7)</li>
                            <li>16-bit address bus (A0-A15), can address 64KB memory</li>
                            <li>Single +5V power supply</li>
                            <li>Clock frequency: 3 MHz</li>
                            <li>40-pin DIP package</li>
                            <li>Supports 256 I/O ports</li>
                            <li>5 hardware interrupts (TRAP, RST 7.5, RST 6.5, RST 5.5, INTR)</li>
                        </ul>

                        <h4>Internal Architecture:</h4>

                        <p><strong>1. Arithmetic Logic Unit (ALU):</strong></p>
                        <ul>
                            <li>Performs arithmetic operations (ADD, SUB)</li>
                            <li>Performs logical operations (AND, OR, XOR, NOT)</li>
                            <li>8-bit operations</li>
                            <li>Updates flags</li>
                        </ul>

                        <p><strong>2. Registers:</strong></p>
                        <ul>
                            <li><strong>Accumulator (A):</strong> 8-bit, primary register for arithmetic/logical operations</li>
                            <li><strong>General Purpose:</strong> B, C, D, E, H, L (8-bit each)
                                <ul>
                                    <li>Can be paired: BC, DE, HL (16-bit pairs)</li>
                                    <li>HL pair used for memory addressing</li>
                                </ul>
                            </li>
                            <li><strong>Program Counter (PC):</strong> 16-bit, holds next instruction address</li>
                            <li><strong>Stack Pointer (SP):</strong> 16-bit, points to top of stack</li>
                            <li><strong>Flag Register:</strong> 8-bit
                                <ul>
                                    <li>S (Sign), Z (Zero), AC (Auxiliary Carry)</li>
                                    <li>P (Parity), CY (Carry)</li>
                                </ul>
                            </li>
                        </ul>

                        <p><strong>3. Control Unit:</strong></p>
                        <ul>
                            <li>Generates control signals</li>
                            <li>Coordinates operations</li>
                            <li>Manages timing</li>
                        </ul>

                        <p><strong>4. Instruction Register & Decoder:</strong></p>
                        <ul>
                            <li>Holds current instruction</li>
                            <li>Decodes opcode</li>
                        </ul>

                        <p><strong>5. Timing & Control:</strong></p>
                        <ul>
                            <li>Generates clock signals</li>
                            <li>Synchronizes operations</li>
                        </ul>

                        <h4>Pin Configuration (Important Pins):</h4>
                        <ul>
                            <li><strong>AD0-AD7:</strong> Multiplexed Address/Data bus (lower byte)</li>
                            <li><strong>A8-A15:</strong> Higher order address bus</li>
                            <li><strong>ALE:</strong> Address Latch Enable (demultiplexing)</li>
                            <li><strong>RD, WR:</strong> Read/Write control signals</li>
                            <li><strong>IO/M:</strong> Distinguishes I/O and Memory operations</li>
                            <li><strong>RESET IN/OUT:</strong> Reset signals</li>
                            <li><strong>INTR, INTA:</strong> Interrupt request/acknowledge</li>
                            <li><strong>HOLD, HLDA:</strong> DMA signals</li>
                        </ul>

                        <h4>Interrupts (Priority Order):</h4>
                        <ol>
                            <li><strong>TRAP:</strong> Non-maskable, edge & level triggered, highest priority</li>
                            <li><strong>RST 7.5:</strong> Maskable, edge triggered</li>
                            <li><strong>RST 6.5:</strong> Maskable, level triggered</li>
                            <li><strong>RST 5.5:</strong> Maskable, level triggered</li>
                            <li><strong>INTR:</strong> Maskable, level triggered, lowest priority</li>
                        </ol>

                        <div class="key-point">
                            <strong>Memory Mapped I/O:</strong> 8085 uses separate instructions (IN/OUT) for I/O operations, but can also use memory-mapped I/O where I/O devices are treated as memory locations.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">2. Write an 8085 program to add two 8-bit numbers and explain instruction set.
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>Program: Add two 8-bit numbers</h4>
                        <p><strong>Problem:</strong> Add data at memory location 2050H and 2051H, store result at 2052H</p>

                        <pre><code>Address   Label   Opcode  Operand   Comments
2000H     START:  LDA     2050H     ; Load first number in accumulator
2003H             MOV     B, A      ; Copy to register B
2004H             LDA     2051H     ; Load second number in accumulator
2007H             ADD     B         ; Add B to A
2008H             STA     2052H     ; Store result
200BH             HLT               ; Stop execution</code></pre>

                        <h4>Explanation:</h4>
                        <ol>
                            <li><strong>LDA 2050H:</strong> Load Accumulator with data from address 2050H (3 bytes, 13 T-states)</li>
                            <li><strong>MOV B, A:</strong> Move data from A to register B (1 byte, 4 T-states)</li>
                            <li><strong>LDA 2051H:</strong> Load second number in A (3 bytes, 13 T-states)</li>
                            <li><strong>ADD B:</strong> Add contents of B to A, result in A (1 byte, 4 T-states)</li>
                            <li><strong>STA 2052H:</strong> Store result from A to memory (3 bytes, 13 T-states)</li>
                            <li><strong>HLT:</strong> Halt execution (1 byte, 7 T-states)</li>
                        </ol>

                        <h4>8085 Instruction Set Categories:</h4>

                        <p><strong>1. Data Transfer Instructions:</strong></p>
                        <ul>
                            <li><strong>MOV r1, r2:</strong> Move data between registers</li>
                            <li><strong>MVI r, data:</strong> Move immediate data to register</li>
                            <li><strong>LDA addr:</strong> Load accumulator direct</li>
                            <li><strong>STA addr:</strong> Store accumulator direct</li>
                            <li><strong>LHLD addr:</strong> Load H-L pair direct</li>
                            <li><strong>SHLD addr:</strong> Store H-L pair direct</li>
                            <li><strong>LXI rp, 16-bit:</strong> Load register pair immediate</li>
                        </ul>

                        <p><strong>2. Arithmetic Instructions:</strong></p>
                        <ul>
                            <li><strong>ADD r/M:</strong> Add register or memory to A</li>
                            <li><strong>ADI data:</strong> Add immediate data to A</li>
                            <li><strong>SUB r/M:</strong> Subtract from A</li>
                            <li><strong>INR r/M:</strong> Increment register or memory</li>
                            <li><strong>DCR r/M:</strong> Decrement register or memory</li>
                            <li><strong>DAD rp:</strong> Add register pair to HL</li>
                        </ul>

                        <p><strong>3. Logical Instructions:</strong></p>
                        <ul>
                            <li><strong>ANA r/M:</strong> AND with accumulator</li>
                            <li><strong>ORA r/M:</strong> OR with accumulator</li>
                            <li><strong>XRA r/M:</strong> XOR with accumulator</li>
                            <li><strong>CMP r/M:</strong> Compare with accumulator</li>
                            <li><strong>RLC, RRC:</strong> Rotate accumulator left/right</li>
                        </ul>

                        <p><strong>4. Branch Instructions:</strong></p>
                        <ul>
                            <li><strong>JMP addr:</strong> Unconditional jump</li>
                            <li><strong>JZ, JNZ:</strong> Jump if zero/not zero</li>
                            <li><strong>JC, JNC:</strong> Jump if carry/no carry</li>
                            <li><strong>CALL addr:</strong> Call subroutine</li>
                            <li><strong>RET:</strong> Return from subroutine</li>
                        </ul>

                        <p><strong>5. Stack Instructions:</strong></p>
                        <ul>
                            <li><strong>PUSH rp:</strong> Push register pair on stack</li>
                            <li><strong>POP rp:</strong> Pop register pair from stack</li>
                        </ul>

                        <p><strong>6. Machine Control:</strong></p>
                        <ul>
                            <li><strong>HLT:</strong> Halt processor</li>
                            <li><strong>NOP:</strong> No operation</li>
                            <li><strong>EI, DI:</strong> Enable/Disable interrupts</li>
                        </ul>

                        <h4>Addressing Modes:</h4>
                        <ol>
                            <li><strong>Direct:</strong> LDA 2050H (address specified)</li>
                            <li><strong>Register:</strong> MOV A, B</li>
                            <li><strong>Immediate:</strong> MVI A, 50H</li>
                            <li><strong>Indirect:</strong> MOV A, M (M = memory pointed by HL)</li>
                            <li><strong>Implied:</strong> CMA (A is implied)</li>
                        </ol>

                        <div class="note-box">
                            <strong>Timing:</strong> Total T-states = 13+4+13+4+13+7 = 54 T-states. At 3 MHz clock, one T-state = 1/(3×10⁶) = 0.33 μs. Total time = 54 × 0.33 = 18 μs
                        </div>
                    </div>
                </div>
            </section>

            <!-- Communication Systems -->
            <section id="communication" class="subject-section">
                <h2 class="subject-title">Communication Systems</h2>
                <p class="subject-desc">Modulation techniques, transmission, and signal processing</p>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">1. Explain Amplitude Modulation (AM) and its types.
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>Amplitude Modulation is a technique where the amplitude of carrier signal is varied in accordance with the instantaneous amplitude of the modulating (message) signal.</p>

                        <h4>AM Equation:</h4>
                        <p>Message signal: m(t) = A<sub>m</sub> cos(ω<sub>m</sub>t)</p>
                        <p>Carrier signal: c(t) = A<sub>c</sub> cos(ω<sub>c</sub>t)</p>
                        
                        <div class="formula-box">
                            s(t) = [A<sub>c</sub> + m(t)] cos(ω<sub>c</sub>t)<br><br>
                            s(t) = A<sub>c</sub>[1 + μ cos(ω<sub>m</sub>t)] cos(ω<sub>c</sub>t)
                        </div>

                        <p>Where μ = Modulation Index = A<sub>m</sub>/A<sub>c</sub></p>

                        <h4>Modulation Index (μ):</h4>
                        <ul>
                            <li><strong>μ < 1:</strong> Under-modulation (good)</li>
                            <li><strong>μ = 1:</strong> 100% modulation (ideal)</li>
                            <li><strong>μ > 1:</strong> Over-modulation (distortion)</li>
                        </ul>

                        <div class="formula-box">
                            μ = (V<sub>max</sub> - V<sub>min</sub>)/(V<sub>max</sub> + V<sub>min</sub>)
                        </div>

                        <h4>Frequency Spectrum:</h4>
                        <p>AM wave contains three frequencies:</p>
                        <ul>
                            <li><strong>Carrier:</strong> f<sub>c</sub> with amplitude A<sub>c</sub></li>
                            <li><strong>Upper Sideband (USB):</strong> f<sub>c</sub> + f<sub>m</sub> with amplitude μA<sub>c</sub>/2</li>
                            <li><strong>Lower Sideband (LSB):</strong> f<sub>c</sub> - f<sub>m</sub> with amplitude μA<sub>c</sub>/2</li>
                        </ul>

                        <p><strong>Bandwidth:</strong> BW = 2f<sub>m</sub></p>

                        <h4>Power Relations:</h4>
                        <div class="formula-box">
                            P<sub>total</sub> = P<sub>c</sub> + P<sub>USB</sub> + P<sub>LSB</sub><br><br>
                            P<sub>total</sub> = P<sub>c</sub>(1 + μ²/2)<br><br>
                            P<sub>sideband</sub> = P<sub>c</sub>μ²/2<br><br>
                            Efficiency η = (μ²/2)/(1 + μ²/2) × 100%
                        </div>

                        <p>For μ = 1, maximum efficiency = 33.33%</p>

                        <h4>Types of AM:</h4>

                        <p><strong>1. Double Sideband Full Carrier (DSB-FC) - Standard AM:</strong></p>
                        <ul>
                            <li>Both sidebands + carrier transmitted</li>
                            <li>Simple demodulation</li>
                            <li>Low efficiency (33% max)</li>
                            <li>Used in AM radio broadcasting</li>
                        </ul>

                        <p><strong>2. Double Sideband Suppressed Carrier (DSB-SC):</strong></p>
                        <ul>
                            <li>Both sidebands, carrier suppressed</li>
                            <li>100% efficiency</li>
                            <li>Complex demodulation (needs carrier recovery)</li>
                            <li>Used in color TV (NTSC)</li>
                        </ul>

                        <p><strong>3. Single Sideband (SSB):</strong></p>
                        <ul>
                            <li>One sideband only, carrier suppressed</li>
                            <li>Bandwidth = f<sub>m</sub> (half of DSB)</li>
                            <li>Most efficient</li>
                            <li>Used in two-way radio, military communication</li>
                        </ul>

                        <p><strong>4. Vestigial Sideband (VSB):</strong></p>
                        <ul>
                            <li>One full sideband + trace of other</li>
                            <li>Compromise between DSB and SSB</li>
                            <li>Used in TV video transmission</li>
                        </ul>

                        <h4>Advantages of AM:</h4>
                        <ul>
                            <li>Simple transmitter and receiver design</li>
                            <li>Low cost</li>
                            <li>Good for long-distance communication</li>
                        </ul>

                        <h4>Disadvantages:</h4>
                        <ul>
                            <li>Low efficiency (power wastage)</li>
                            <li>Noise susceptible</li>
                            <li>Requires more bandwidth than FM for same modulation</li>
                        </ul>

                        <div class="key-point">
                            <strong>Applications:</strong> AM radio broadcasting (535-1605 kHz), aircraft communication, citizen band (CB) radio, two-way mobile communication.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">2. Compare Amplitude Modulation (AM) and Frequency Modulation (FM).
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>Frequency Modulation (FM):</h4>
                        <p>Frequency of carrier is varied in accordance with instantaneous amplitude of modulating signal.</p>

                        <div class="formula-box">
                            s(t) = A<sub>c</sub> cos[ω<sub>c</sub>t + β sin(ω<sub>m</sub>t)]<br><br>
                            Modulation Index: β = Δf/f<sub>m</sub><br><br>
                            Bandwidth (Carson's Rule): BW ≈ 2(Δf + f<sub>m</sub>)
                        </div>

                        <p>Where Δf = frequency deviation</p>

                        <h4>Comprehensive Comparison:</h4>
                        <table>
                            <tr>
                                <th>Parameter</th>
                                <th>AM</th>
                                <th>FM</th>
                            </tr>
                            <tr>
                                <td>Modulated Parameter</td>
                                <td>Amplitude varies</td>
                                <td>Frequency varies</td>
                            </tr>
                            <tr>
                                <td>Bandwidth</td>
                                <td>2f<sub>m</sub> (narrow)</td>
                                <td>2(Δf + f<sub>m</sub>) (wide)</td>
                            </tr>
                            <tr>
                                <td>Efficiency</td>
                                <td>Low (33% max)</td>
                                <td>High (100%)</td>
                            </tr>
                            <tr>
                                <td>Noise Immunity</td>
                                <td>Poor (noise affects amplitude)</td>
                                <td>Excellent (noise doesn't affect frequency)</td>
                            </tr>
                            <tr>
                                <td>Audio Quality</td>
                                <td>Good</td>
                                <td>Excellent (Hi-Fi)</td>
                            </tr>
                            <tr>
                                <td>Transmission Range</td>
                                <td>Long (ground wave)</td>
                                <td>Short (line of sight)</td>
                            </tr>
                            <tr>
                                <td>Equipment Cost</td>
                                <td>Low</td>
                                <td>High</td>
                            </tr>
                            <tr>
                                <td>Power Required</td>
                                <td>Varies with modulation</td>
                                <td>Constant</td>
                            </tr>
                            <tr>
                                <td>Frequency Range</td>
                                <td>535-1605 kHz (MW)</td>
                                <td>88-108 MHz (VHF)</td>
                            </tr>
                            <tr>
                                <td>Number of Stations</td>
                                <td>More (narrow BW)</td>
                                <td>Less (wide BW)</td>
                            </tr>
                            <tr>
                                <td>Fading</td>
                                <td>Severe</td>
                                <td>Less</td>
                            </tr>
                            <tr>
                                <td>Applications</td>
                                <td>AM radio, aviation</td>
                                <td>FM radio, TV audio</td>
                            </tr>
                        </table>

                        <h4>Signal Representation:</h4>
                        <p><strong>AM Signal:</strong></p>
                        <ul>
                            <li>Amplitude changes with message</li>
                            <li>Frequency remains constant</li>
                            <li>Envelope follows message signal</li>
                        </ul>

                        <p><strong>FM Signal:</strong></p>
                        <ul>
                            <li>Amplitude remains constant</li>
                            <li>Frequency changes with message</li>
                            <li>Zero crossings vary</li>
                        </ul>

                        <h4>Advantages of FM over AM:</h4>
                        <ul>
                            <li><strong>Noise Immunity:</strong> Amplitude-based noise easily removed by limiters</li>
                            <li><strong>Better SNR:</strong> Signal-to-Noise ratio significantly higher</li>
                            <li><strong>No Fading:</strong> Constant amplitude prevents fading issues</li>
                            <li><strong>Power Efficiency:</strong> Transmit power constant, independent of modulation</li>
                            <li><strong>Guard Bands:</strong> Interference between stations minimized</li>
                        </ul>

                        <h4>Disadvantages of FM:</h4>
                        <ul>
                            <li>Requires more bandwidth</li>
                            <li>Complex and expensive equipment</li>
                            <li>Limited transmission range</li>
                            <li>Requires line-of-sight propagation</li>
                        </ul>

                        <div class="key-point">
                            <strong>Selection Guide:</strong> Use AM for long-distance, simple, low-cost communication. Use FM for high-quality audio, noise immunity, and where bandwidth is available.
                        </div>
                    </div>
                </div>
            </section>

            <!-- Control Systems -->
            <section id="control" class="subject-section">
                <h2 class="subject-title">Control Systems</h2>
                <p class="subject-desc">Feedback systems, transfer functions, and stability analysis</p>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">1. Explain Open Loop and Closed Loop Control Systems with examples.
                            <span class="difficulty easy">Easy</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>Open Loop Control System:</h4>
                        <p>A system where output has no effect on the control action. No feedback path exists.</p>

                        <p><strong>Block Diagram:</strong></p>
                        <div class="circuit-diagram">
                            Input → Controller → Process → Output
                        </div>

                        <p><strong>Characteristics:</strong></p>
                        <ul>
                            <li>No feedback path</li>
                            <li>Output is independent of control action</li>
                            <li>Simple and economical</li>
                            <li>Less accurate</li>
                            <li>Affected by disturbances</li>
                            <li>No error correction</li>
                        </ul>

                        <p><strong>Examples:</strong></p>
                        <ul>
                            <li><strong>Traffic Lights:</strong> Time-based, no feedback from traffic</li>
                            <li><strong>Washing Machine:</strong> Fixed wash cycle</li>
                            <li><strong>Electric Toaster:</strong> Time-based heating</li>
                            <li><strong>Stepper Motor:</strong> Runs for fixed steps</li>
                            <li><strong>Manual Voltage Regulator</strong></li>
                        </ul>

                        <h4>Closed Loop (Feedback) Control System:</h4>
                        <p>A system where output is fed back and compared with input. Error signal used for control.</p>

                        <p><strong>Block Diagram:</strong></p>
                        <div class="circuit-diagram">
                            <pre>
Input → ⊕ → Controller → Process → Output
        ↑                            |
        ← ← ← Feedback ← ← ← ← ← ← ←
            </pre>
                        </div>

                        <p><strong>Characteristics:</strong></p>
                        <ul>
                            <li>Feedback path exists</li>
                            <li>Output compared with input</li>
                            <li>Error signal = Input - Feedback</li>
                            <li>Self-correcting</li>
                            <li>More accurate</li>
                            <li>Complex and expensive</li>
                            <li>May become unstable</li>
                        </ul>

                        <p><strong>Examples:</strong></p>
                        <ul>
                            <li><strong>Air Conditioner:</strong> Thermostat monitors temperature</li>
                            <li><strong>Voltage Regulator:</strong> Maintains constant output voltage</li>
                            <li><strong>Cruise Control:</strong> Maintains car speed</li>
                            <li><strong>Servo Motor:</strong> Position controlled by feedback</li>
                            <li><strong>Automatic Water Level Controller</strong></li>
                        </ul>

                        <h4>Comparison Table:</h4>
                        <table>
                            <tr>
                                <th>Aspect</th>
                                <th>Open Loop</th>
                                <th>Closed Loop</th>
                            </tr>
                            <tr>
                                <td>Feedback</td>
                                <td>No feedback</td>
                                <td>Feedback present</td>
                            </tr>
                            <tr>
                                <td>Accuracy</td>
                                <td>Less accurate</td>
                                <td>More accurate</td>
                            </tr>
                            <tr>
                                <td>Stability</td>
                                <td>Always stable</td>
                                <td>May be unstable</td>
                            </tr>
                            <tr>
                                <td>Complexity</td>
                                <td>Simple</td>
                                <td>Complex</td>
                            </tr>
                            <tr>
                                <td>Cost</td>
                                <td>Low</td>
                                <td>High</td>
                            </tr>
                            <tr>
                                <td>Reliability</td>
                                <td>Less reliable</td>
                                <td>More reliable</td>
                            </tr>
                            <tr>
                                <td>Disturbance Effect</td>
                                <td>Highly affected</td>
                                <td>Less affected</td>
                            </tr>
                            <tr>
                                <td>Response</td>
                                <td>Fast</td>
                                <td>Slower due to feedback</td>
                            </tr>
                        </table>

                        <div class="key-point">
                            <strong>Selection Criteria:</strong> Use open loop for simple, low-cost applications where accuracy is not critical. Use closed loop for precision, automatic error correction, and when disturbances must be minimized.
                        </div>
                    </div>
                </div>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">2. Explain Routh-Hurwitz Stability Criterion.
                            <span class="difficulty hard">Hard</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <p>Routh-Hurwitz criterion is an algebraic method to determine system stability without actually solving the characteristic equation.</p>

                        <h4>Characteristic Equation:</h4>
                        <div class="formula-box">
                            a<sub>n</sub>s<sup>n</sup> + a<sub>n-1</sub>s<sup>n-1</sup> + ... + a<sub>1</sub>s + a<sub>0</sub> = 0
                        </div>

                        <h4>Routh Array Formation:</h4>
                        <p>Arrange coefficients in rows alternately:</p>
                        <div class="circuit-diagram">
                            <pre>
s<sup>n</sup>     a<sub>n</sub>   a<sub>n-2</sub>   a<sub>n-4</sub>   ...
s<sup>n-1</sup>   a<sub>n-1</sub> a<sub>n-3</sub>   a<sub>n-5</sub>   ...
s<sup>n-2</sup>   b<sub>1</sub>   b<sub>2</sub>     b<sub>3</sub>     ...
s<sup>n-3</sup>   c<sub>1</sub>   c<sub>2</sub>     c<sub>3</sub>     ...
...
s<sup>1</sup>     ...
s<sup>0</sup>     ...
            </pre>
                        </div>

                        <p>Where:</p>
                        <div class="formula-box">
                            b<sub>1</sub> = (a<sub>n-1</sub>a<sub>n-2</sub> - a<sub>n</sub>a<sub>n-3</sub>)/a<sub>n-1</sub><br>
                            b<sub>2</sub> = (a<sub>n-1</sub>a<sub>n-4</sub> - a<sub>n</sub>a<sub>n-5</sub>)/a<sub>n-1</sub><br>
                            c<sub>1</sub> = (b<sub>1</sub>a<sub>n-3</sub> - a<sub>n-1</sub>b<sub>2</sub>)/b<sub>1</sub>
                        </div>

                        <h4>Stability Conditions:</h4>
                        <p>System is stable if and only if:</p>
                        <ol>
                            <li>All coefficients of characteristic equation are positive</li>
                            <li>All elements in first column of Routh array are positive</li>
                            <li>No sign changes in first column</li>
                        </ol>

                        <p><strong>Number of poles in RHP (unstable poles) = Number of sign changes in first column</strong></p>

                        <h4>Example: Third Order System</h4>
                        <p>Characteristic equation: s³ + 3s² + 2s + 6 = 0</p>

                        <p><strong>Routh Array:</strong></p>
                        <div class="circuit-diagram">
                            <pre>
s³    1    2
s²    3    6
s¹    0    0  ← Problem: Zero in first column
s⁰    6
            </pre>
                        </div>

                        <p>For s¹: b₁ = (3×2 - 1×6)/3 = 0</p>

                        <h4>Special Cases:</h4>

                        <p><strong>1. Zero in First Column (non-zero in row):</strong></p>
                        <ul>
                            <li>Replace zero with small ε (ε → 0⁺)</li>
                            <li>Complete array</li>
                            <li>Check signs</li>
                        </ul>

                        <p><strong>2. Entire Row Zero:</strong></p>
                        <ul>
                            <li>Form auxiliary polynomial from row above</li>
                            <li>Differentiate auxiliary polynomial</li>
                            <li>Use coefficients to replace zero row</li>
                        </ul>

                        <h4>Worked Example:</h4>
                        <p>s⁴ + 2s³ + 3s² + 4s + 5 = 0</p>

                        <div class="circuit-diagram">
                            <pre>
s⁴    1      3      5
s³    2      4      0
s²    1      5      0
s¹    -6     0      0
s⁰    5
            </pre>
                        </div>

                        <p>Calculations:</p>
                        <ul>
                            <li>s²: (2×3 - 1×4)/2 = 1</li>
                            <li>s²: (2×5 - 1×0)/2 = 5</li>
                            <li>s¹: (1×4 - 2×5)/1 = -6</li>
                            <li>s⁰: 5</li>
                        </ul>

                        <p><strong>Result:</strong> Two sign changes (1 to -6, -6 to 5) → 2 poles in RHP → System is UNSTABLE</p>

                        <h4>Applications:</h4>
                        <ul>
                            <li>Quick stability check without solving roots</li>
                            <li>Determining range of parameters for stability</li>
                            <li>Counting unstable poles</li>
                            <li>Design of stable control systems</li>
                        </ul>

                        <div class="note-box">
                            <strong>Limitation:</strong> Routh-Hurwitz only tells if system is stable, not how stable. For relative stability, use root locus or Nyquist criterion.
                        </div>
                    </div>
                </div>
            </section>

            <!-- Power Electronics -->
            <section id="power" class="subject-section">
                <h2 class="subject-title">Power Electronics</h2>
                <p class="subject-desc">Power semiconductor devices, converters, and applications</p>

                <div class="question-card">
                    <div class="question-header">
                        <span class="question-text">1. Explain different Power Semiconductor Devices (SCR, MOSFET, IGBT).
                            <span class="difficulty medium">Medium</span>
                        </span>
                        <span class="toggle-icon">+</span>
                    </div>
                    <div class="answer-content">
                        <h4>1. Silicon Controlled Rectifier (SCR/Thyristor):</h4>
                        
                        <p><strong>Structure:</strong> PNPN four-layer device with three terminals: Anode (A), Cathode (K), Gate (G)</p>

                        <p><strong>Working Principle:</strong></p>
                        <ul>
                            <li>Normally OFF state (blocking)</li>
                            <li>Turned ON by gate pulse when anode positive</li>
                            <li>Remains ON even after gate signal removed (latching)</li>
                            <li>Turned OFF only when current < holding current</li>
                        </ul>

                        <p><strong>Key Ratings:</strong></p>
                        <ul>
                            <li><strong>Holding Current (I<sub>H</sub>):</strong> Minimum anode current to keep ON</li>
                            <li><strong>Latching Current (I<sub>L</sub>):</strong> Minimum anode current to turn ON</li>
                            <li><strong>Peak Reverse Voltage (PRV)</strong></li>
                            <li><strong>dv/dt rating:</strong> Maximum voltage rise rate</li>
                            <li><strong>di/dt rating:</strong> Maximum current rise rate</li>
                        </ul>

                        <p><strong>Advantages:</strong></p>
                        <ul>
                            <li>High power handling (>5000V, >5000A)</li>
                            <li>Low ON-state voltage drop</li>
                            <li>Simple gate control</li>
                        </ul>

                        <p><strong>Disadvantages:</strong></p>
                        <ul>
                            <li>Slow switching speed</li>
                            <li>No turn-off capability from gate</li>
                            <li>Commutation circuits needed</li>
                        </ul>

                        <p><strong>Applications:</strong> AC-DC converters, motor drives, HVDC transmission, lamp dimmers</p>

                        <h4>2. Power MOSFET (Metal-Oxide-Semiconductor FET):</h4>
                        
                        <p><strong>Structure:</strong> Three terminals: Drain (D), Source (S), Gate (G)</p>

                        <p><strong>Working Principle:</strong></p>
                        <ul>
                            <li>Voltage-controlled device</li>
                            <li>ON state: Apply V<sub>GS</sub> > V<sub>th</sub> (threshold voltage)</li>
                            <li>OFF state: V<sub>GS</sub> < V<sub>th</sub></li>
                            <li>Very high input impedance</li>
                        </ul>

                        <p><strong>Characteristics:</strong></p>
                        <ul>
                            <li>Fast switching (ns range)</li>
                            <li>Low gate power requirement</li>
                            <li>Positive temperature coefficient (parallel operation safe)</li>
                            <li>No second breakdown</li>
                        </ul>

                        <p><strong>Advantages:</strong></p>
                        <ul>
                            <li>Very fast switching speed</li>
                            <li>Simple gate drive circuit</li>
                            <li>Low ON-state resistance (R<sub>DS(ON)</sub>)</li>
                            <li>No minority carrier storage</li>
                        </ul>

                        <p><strong>Disadvantages:</strong></p>
                        <ul>
                            <li>Lower voltage rating compared to SCR</li>
                            <li>Higher ON-state losses at high voltage</li>
                            <li>Body diode reverse recovery</li>
                        </ul>

                        <p><strong>Applications:</strong> Switch-mode power supplies (SMPS), DC-DC converters, motor drives (low voltage)</p>

                        <h4>3. Insulated Gate Bipolar Transistor (IGBT):</h4>
                        
                        <p><strong>Structure:</strong> Hybrid device combining MOSFET and BJT. Terminals: Collector (C), Emitter (E), Gate (G)</p>

                        <p><strong>Working Principle:</strong></p>
                        <ul>
                            <li>Voltage-controlled like MOSFET</li>
                            <li>Conduction like BJT</li>
                            <li>Best of both worlds</li>
                        </ul>

                        <p><strong>Characteristics:</strong></p>
                        <ul>
                            <li>High voltage capability (up to 6.5kV)</li>
                            <li>High current capability (up to 3kA)</li>
                            <li>Fast switching (μs range)</li>
                            <li>Low ON-state voltage</li>
                        </ul>

                        <p><strong>Advantages:</strong></p>
                        <ul>
                            <li>High input impedance (like MOSFET)</li>
                            <li>Low ON-state losses (like BJT)</li>
                            <li>Simpler gate drive than BJT</li>
                            <li>High voltage and current ratings</li>
                        </ul>

                        <p><strong>Disadvantages:</strong></p>
                        <ul>
                            <li>Slower than MOSFET</li>
                            <li>Tail current during turn-off</li>
                            <li>More expensive</li>
                        </ul>

                        <p><strong>Applications:</strong> Inverters, UPS, motor drives, traction, induction heating</p>

                        <h4>Comparison Table:</h4>
                        <table>
                            <tr>
                                <th>Parameter</th>
                                <th>SCR</th>
                                <th>MOSFET</th>
                                <th>IGBT</th>
                            </tr>
                            <tr>
                                <td>Control Type</td>
                                <td>Current</td>
                                <td>Voltage</td>
                                <td>Voltage</td>
                            </tr>
                            <tr>
                                <td>Switching Speed</td>
                                <td>Slow (ms)</td>
                                <td>Very Fast (ns)</td>
                                <td>Fast (μs)</td>
                            </tr>
                            <tr>
                                <td>Voltage Rating</td>
                                <td>Very High</td>
                                <td>Medium</td>
                                <td>High</td>
                            </tr>
                            <tr>
                                <td>Current Rating</td>
                                <td>Very High</td>
                                <td>Medium</td>
                                <td>High</td>
                            </tr>
                            <tr>
                                <td>ON-state Loss</td>
                                <td>Very Low</td>
                                <td>Medium</td>
                                <td>Low</td>
                            </tr>
                            <tr>
                                <td>Gate Power</td>
                                <td>Low</td>
                                <td>Very Low</td>
                                <td>Very Low</td>
                            </tr>
                            <tr>
                                <td>Turn-off</td>
                                <td>No gate control</td>
                                <td>Gate controlled</td>
                                <td>Gate controlled</td>
                            </tr>
                            <tr>
                                <td>Cost</td>
                                <td>Low</td>
                                <td>Medium</td>
                                <td>High</td>
                            </tr>
                            <tr>
                                <td>Best For</td>
                                <td>AC control</td>
                                <td>High frequency</td>
                                <td>Medium power</td>
                            </tr>
                        </table>

                        <div class="key-point">
                            <strong>Selection Guide:</strong> SCR for line-frequency AC control, MOSFET for high-frequency low-voltage, IGBT for medium-power high-voltage applications.
                        </div>
                    </div>
                </div>
            </section>

        </main>
    </div>

    <script>
        // Toggle question answers
        document.querySelectorAll('.question-header').forEach(header => {
            header.addEventListener('click', function() {
                const card = this.parentElement;
                card.classList.toggle('active');
            });
        });

        // Smooth scrolling for navigation
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetSection = document.querySelector(targetId);
                
                // Update active link
                document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
                this.classList.add('active');
                
                // Scroll to section
                targetSection.scrollIntoView({ behavior: 'smooth', block: 'start' });
            });
        });

        // Highlight active section on scroll
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.subject-section');
            const navLinks = document.querySelectorAll('.nav-link');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (window.pageYOffset >= sectionTop - 100) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
