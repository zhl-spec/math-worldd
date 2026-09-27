<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brawl Stars Matchmaking Simulator</title>
    <style>
        :root {
            --bg-color: #12131C;
            --card-bg: #1E202E;
            --accent-blue: #2B7FFF;
            --accent-red: #FF4757;
            --text-main: #FFFFFF;
            --text-sub: #A0A5BA;
            --success: #2ED573;
            --warning: #FFA502;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
        }

        h1, h2, h3 { text-align: center; margin-bottom: 10px; }
        p.subtitle { text-align: center; color: var(--text-sub); margin-bottom: 30px; }

        .grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
            position: relative;
        }

        .control-group { margin-bottom: 15px; }

        label {
            display: flex;
            justify-content: space-between;
            font-weight: bold;
            margin-bottom: 5px;
        }

        input[type="range"] {
            width: 100%;
            accent-color: var(--accent-blue);
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 15px;
        }

        .btn {
            width: 100%;
            padding: 12px;
            background: linear-gradient(45deg, #2B7FFF, #1E90FF);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            margin-top: 15px;
            transition: transform 0.1s ease, background 0.3s ease;
        }

        .btn:hover { transform: scale(1.02); }
        .btn-battle { background: linear-gradient(45deg, #FF4757, #FF6B81); }
        .btn-reveal { background: linear-gradient(45deg, #FFA502, #ECCC68); color: #12131C; }

        .team-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 20px;
        }

        .team { border-radius: 8px; padding: 15px; }
        .team-blue { background: rgba(43, 127, 255, 0.15); border: 2px solid var(--accent-blue); }
        .team-red { background: rgba(255, 71, 87, 0.15); border: 2px solid var(--accent-red); }

        .player-card {
            background: rgba(0,0,0,0.2);
            padding: 8px 12px;
            border-radius: 6px;
            margin-bottom: 8px;
            font-size: 13px;
        }

        /* Diagnostic Hide/Reveal Styling */
        .report-locked {
            text-align: center;
            padding: 30px 10px;
            background: rgba(0,0,0,0.2);
            border-radius: 8px;
            border: 2px dashed var(--text-sub);
        }

        .badge-list { list-style: none; padding: 0; }
        .badge-list li {
            padding: 8px 12px;
            border-radius: 6px;
            margin-bottom: 8px;
            font-size: 14px;
        }

        .pro { background: rgba(46, 213, 115, 0.2); border-left: 4px solid var(--success); }
        .con { background: rgba(255, 165, 2, 0.2); border-left: 4px solid var(--warning); }

        /* Battle Arena Styling */
        .arena-box {
            margin-top: 20px;
            background: rgba(0,0,0,0.4);
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            display: none;
        }

        .hp-bar-container {
            display: flex;
            justify-content: space-between;
            gap: 15px;
            margin: 15px 0;
        }

        .hp-bar-wrapper { flex: 1; }
        .hp-bar {
            height: 20px;
            background: #333;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }

        .hp-fill { height: 100%; transition: width 0.3s ease; }
        .hp-fill-blue { background: var(--accent-blue); width: 100%; }
        .hp-fill-red { background: var(--accent-red); width: 100%; }

        .battle-log {
            font-size: 14px;
            font-weight: bold;
            height: 30px;
            color: var(--warning);
        }

        .winner-banner {
            font-size: 22px;
            font-weight: bold;
            margin-top: 10px;
            animation: popIn 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        @keyframes popIn {
            0% { transform: scale(0); }
            100% { transform: scale(1); }
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            20%, 60% { transform: translateX(-5px); }
            40%, 80% { transform: translateX(5px); }
        }

        .shaking { animation: shake 0.3s ease-in-out infinite; }
    </style>
</head>
<body>

<div class="container">
    <h1>🎮 Brawl Stars Matchmaking Lab</h1>
    <p class="subtitle">Design your algorithm, test in battle, and analyze the fairness!</p>

    <div class="grid">
        <!-- CONTROLS PANEL -->
        <div class="card">
            <h2>1. Set Model Weights</h2>
            
            <div class="control-group">
                <label>Brawler Trophies (T<sub>i</sub>) Weight: <span id="w-trophy-val">1.0</span></label>
                <input type="range" id="w-trophy" min="0" max="2" step="0.1" value="1.0">
            </div>

            <div class="control-group">
                <label>Power Level (PL) Weight: <span id="w-power-val">0.5</span></label>
                <input type="range" id="w-power" min="0" max="2" step="0.1" value="0.5">
            </div>

            <div class="control-group">
                <label>Win/Loss Streak Weight: <span id="w-streak-val">0.2</span></label>
                <input type="range" id="w-streak" min="0" max="2" step="0.1" value="0.2">
            </div>

            <div class="control-group">
                <label>Ping / Latency Penalty Weight: <span id="w-ping-val">0.5</span></label>
                <input type="range" id="w-ping" min="0" max="2" step="0.1" value="0.5">
            </div>

            <div class="checkbox-group">
                <input type="checkbox" id="chk-range" checked>
                <label for="chk-range" style="font-weight:normal;">Apply Range Penalty (Prevent Weak Links)</label>
            </div>

            <button class="btn" onclick="runSimulation()">Generate Lobby & Matchmake</button>
        </div>

        <!-- DIAGNOSTIC PANEL -->
        <div class="card">
            <h2>2. Diagnostic Report</h2>
            
            <div id="report-locked-view" class="report-locked">
                <p>💡 <b>Student Challenge:</b> Look at the generated teams first! Do you think this match will be fair?</p>
                <button class="btn btn-reveal" onclick="revealDiagnostics()">🔍 Reveal Diagnostic Report</button>
            </div>

            <div id="report-content-view" style="display: none;">
                <h3>Advantages (Pros)</h3>
                <ul class="badge-list" id="pros-list"></ul>

                <h3>Disadvantages & Flaws (Cons)</h3>
                <ul class="badge-list" id="cons-list"></ul>
                
                <button class="btn" style="background:#444;" onclick="hideDiagnostics()">🔒 Lock Report</button>
            </div>
        </div>
    </div>

    <!-- MATCH TEAMS DISPLAY -->
    <div class="card" style="margin-top: 20px;" id="team-card">
        <h2>3. Team Allocation (3v3)</h2>
        <div class="team-container">
            <div class="team team-blue">
                <h3 style="color: var(--accent-blue);">Blue Team</h3>
                <div id="blue-players"></div>
                <hr>
                <p><b>Group Skill Score (GS):</b> <span id="blue-gs">0</span></p>
                <p><b>Avg Ping:</b> <span id="blue-ping">0</span> ms | <b>Trophy Range:</b> <span id="blue-range">0</span></p>
            </div>
            
            <div class="team team-red">
                <h3 style="color: var(--accent-red);">Red Team</h3>
                <div id="red-players"></div>
                <hr>
                <p><b>Group Skill Score (GS):</b> <span id="red-gs">0</span></p>
                <p><b>Avg Ping:</b> <span id="red-ping">0</span> ms | <b>Trophy Range:</b> <span id="red-range">0</span></p>
            </div>
        </div>

        <button class="btn btn-battle" onclick="startBattle()">⚔️ Start Battle Simulation!</button>

        <!-- BATTLE ANIMATION ARENA -->
        <div class="arena-box" id="arena-box">
            <h3 id="arena-status">Battle in Progress...</h3>
            <div class="hp-bar-container">
                <div class="hp-bar-wrapper">
                    <span>Blue Team HP</span>
                    <div class="hp-bar"><div class="hp-fill hp-fill-blue" id="blue-hp"></div></div>
                </div>
                <div class="hp-bar-wrapper">
                    <span>Red Team HP</span>
                    <div class="hp-bar"><div class="hp-fill hp-fill-red" id="red-hp"></div></div>
                </div>
            </div>
            <div class="battle-log" id="battle-log">Brawlers entering the arena...</div>
            <div id="winner-banner"></div>
        </div>
    </div>
</div>

<script>
    let currentMatchData = null;

    // Update Slider Value Displays
    document.querySelectorAll('input[type="range"]').forEach(input => {
        input.addEventListener('input', (e) => {
            document.getElementById(`${e.target.id}-val`).innerText = e.target.value;
        });
    });

    function generatePlayerPool() {
        const pool = [];
        for(let i = 1; i <= 6; i++) {
            pool.push({
                id: `Player ${i}`,
                trophies: Math.floor(Math.random() * 700) + 100,
                powerLevel: Math.floor(Math.random() * 11) + 1,
                streak: Math.floor(Math.random() * 11) - 5,
                ping: Math.floor(Math.random() * 180) + 20
            });
        }
        return pool;
    }

    function calcSkillScore(p, wTrophy, wPower, wStreak, wPing) {
        return (wTrophy * p.trophies) + 
               (wPower * (p.powerLevel * 50)) + 
               (wStreak * (p.streak * 30)) - 
               (wPing * (p.ping * 2));
    }

    function runSimulation() {
        hideDiagnostics();
        resetArena();

        const wTrophy = parseFloat(document.getElementById('w-trophy').value);
        const wPower = parseFloat(document.getElementById('w-power').value);
        const wStreak = parseFloat(document.getElementById('w-streak').value);
        const wPing = parseFloat(document.getElementById('w-ping').value);
        const applyRangePenalty = document.getElementById('chk-range').checked;

        const players = generatePlayerPool();
        players.forEach(p => { p.score = calcSkillScore(p, wTrophy, wPower, wStreak, wPing); });

        const combinations = [
            [[0,1,2], [3,4,5]], [[0,1,3], [2,4,5]], [[0,1,4], [2,3,5]],
            [[0,1,5], [2,3,4]], [[0,2,3], [1,4,5]], [[0,2,4], [1,3,5]],
            [[0,2,5], [1,3,4]], [[0,3,4], [1,2,5]], [[0,3,5], [1,2,4]],
            [[0,4,5], [1,2,3]]
        ];

        let bestSplit = null;
        let minDiff = Infinity;

        combinations.forEach(combo => {
            const team1 = combo[0].map(i => players[i]);
            const team2 = combo[1].map(i => players[i]);

            const gs1 = team1.reduce((sum, p) => sum + p.score, 0);
            const gs2 = team2.reduce((sum, p) => sum + p.score, 0);

            const r1 = Math.max(...team1.map(p => p.trophies)) - Math.min(...team1.map(p => p.trophies));
            const r2 = Math.max(...team2.map(p => p.trophies)) - Math.min(...team2.map(p => p.trophies));
            const rangePenalty = applyRangePenalty ? Math.abs(r1 - r2) : 0;

            const diff = Math.abs(gs1 - gs2) + rangePenalty;

            if (diff < minDiff) {
                minDiff = diff;
                bestSplit = { team1, team2, gs1, gs2, r1, r2 };
            }
        });

        currentMatchData = bestSplit;
        renderTeams(bestSplit);
        prepareAnalysis(bestSplit, wTrophy, wPower, wStreak, wPing, applyRangePenalty);
    }

    function renderTeams(split) {
        const renderPlayer = p => `
            <div class="player-card">
                <b>${p.id}</b> | 🏆 Trophies: ${p.trophies} | ⚡ Level: ${p.powerLevel}<br>
                🔥 Streak: ${p.streak > 0 ? '+'+p.streak : p.streak} | 📶 Ping: ${p.ping}ms | <b>S Score:</b> ${Math.round(p.score)}
            </div>`;

        document.getElementById('blue-players').innerHTML = split.team1.map(renderPlayer).join('');
        document.getElementById('red-players').innerHTML = split.team2.map(renderPlayer).join('');

        document.getElementById('blue-gs').innerText = Math.round(split.gs1);
        document.getElementById('red-gs').innerText = Math.round(split.gs2);

        document.getElementById('blue-ping').innerText = Math.round(split.team1.reduce((a, b) => a + b.ping, 0) / 3);
        document.getElementById('red-ping').innerText = Math.round(split.team2.reduce((a, b) => a + b.ping, 0) / 3);

        document.getElementById('blue-range').innerText = split.r1;
        document.getElementById('red-range').innerText = split.r2;
    }

    function prepareAnalysis(split, wT, wP, wS, wPing, rangeApplied) {
        const pros = [];
        const cons = [];

        if (Math.abs(split.gs1 - split.gs2) < 100) {
            pros.push("Balanced Model: Group Skill Scores are tightly matched.");
        } else {
            cons.push("Skill Imbalance: Significant difference in overall Group Skill Score.");
        }

        if (!rangeApplied && (split.r1 > 350 || split.r2 > 350)) {
            cons.push("Weak Link Exploit: One team contains a beginner carried by a high-trophy player!");
        } else if (rangeApplied) {
            pros.push("Anti-Exploit Active: Range penalty successfully limited team skill variance.");
        }

        const avgPL1 = split.team1.reduce((a,b) => a + b.powerLevel, 0) / 3;
        const avgPL2 = split.team2.reduce((a,b) => a + b.powerLevel, 0) / 3;
        if (wP === 0 && Math.abs(avgPL1 - avgPL2) >= 3) {
            cons.push("Gear Disadvantage: Ignoring Power Level created an unfair gear gap.");
        } else if (wP > 0) {
            pros.push("Gear Balance: Power level differences were accounted for.");
        }

        const avgPing1 = split.team1.reduce((a,b) => a + b.ping, 0) / 3;
        const avgPing2 = split.team2.reduce((a,b) => a + b.ping, 0) / 3;
        if (wPing === 0 && Math.abs(avgPing1 - avgPing2) > 60) {
            cons.push("High Latency Gap: Ignoring Ping resulted in significant network lag for one team.");
        } else if (wPing > 0) {
            pros.push("Network Optimization: Latency differences were minimized.");
        }

        if (wS === 0) {
            cons.push("Tilt Factor: Players on severe losing streaks were not insulated from high-pressure matches.");
        }

        document.getElementById('pros-list').innerHTML = pros.map(p => `<li class="pro">✔ ${p}</li>`).join('');
        document.getElementById('cons-list').innerHTML = cons.map(c => `<li class="con">⚠ ${c}</li>`).join('');
    }

    function revealDiagnostics() {
        document.getElementById('report-locked-view').style.display = 'none';
        document.getElementById('report-content-view').style.display = 'block';
    }

    function hideDiagnostics() {
        document.getElementById('report-locked-view').style.display = 'block';
        document.getElementById('report-content-view').style.display = 'none';
    }

    function resetArena() {
        document.getElementById('arena-box').style.display = 'none';
        document.getElementById('blue-hp').style.width = '100%';
        document.getElementById('red-hp').style.width = '100%';
        document.getElementById('winner-banner').innerHTML = '';
        document.getElementById('team-card').classList.remove('shaking');
    }

    function startBattle() {
        if (!currentMatchData) return;

        const arena = document.getElementById('arena-box');
        const teamCard = document.getElementById('team-card');
        const blueHp = document.getElementById('blue-hp');
        const redHp = document.getElementById('red-hp');
        const log = document.getElementById('battle-log');
        const banner = document.getElementById('winner-banner');

        arena.style.display = 'block';
        banner.innerHTML = '';
        blueHp.style.width = '100%';
        redHp.style.width = '100%';

        // Calculate Win Probability based on Group Skill (GS)
        const gs1 = Math.max(currentMatchData.gs1, 50);
        const gs2 = Math.max(currentMatchData.gs2, 50);
        const blueWinProb = gs1 / (gs1 + gs2);
        const blueWins = Math.random() < blueWinProb;

        teamCard.classList.add('shaking');

        // Battle Animation Sequence
        log.innerText = "💥 Brawlers charging Supers...";
        
        setTimeout(() => {
            log.innerText = "⚔️ Heavy crossfire in Gem Grab mine!";
            blueHp.style.width = blueWins ? '65%' : '40%';
            redHp.style.width = blueWins ? '40%' : '65%';
        }, 1000);

        setTimeout(() => {
            log.innerText = "💣 Overtime activated! Final clash!";
            blueHp.style.width = blueWins ? '35%' : '10%';
            redHp.style.width = blueWins ? '10%' : '35%';
        }, 2000);

        setTimeout(() => {
            teamCard.classList.remove('shaking');
            if (blueWins) {
                blueHp.style.width = '25%';
                redHp.style.width = '0%';
                log.innerText = "🏆 Team Red KO'd!";
                banner.innerHTML = `<div class="winner-banner" style="color: var(--accent-blue);">🎉 BLUE TEAM VICTORY!</div>`;
            } else {
                blueHp.style.width = '0%';
                redHp.style.width = '25%';
                log.innerText = "🏆 Team Blue KO'd!";
                banner.innerHTML = `<div class="winner-banner" style="color: var(--accent-red);">🎉 RED TEAM VICTORY!</div>`;
            }
        }, 3000);
    }

    // Initial Run
    runSimulation();
</script>

</body>
</html>
