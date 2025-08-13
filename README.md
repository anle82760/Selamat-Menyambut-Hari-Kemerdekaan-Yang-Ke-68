<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Menyambut Hari Kemerdekaan Ke-68</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
            color: #333;
            text-align: center;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            background: linear-gradient(135deg, #cc0000, #000066);
            color: white;
            padding: 30px 0;
            border-radius: 10px 10px 0 0;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .subtitle {
            font-size: 1.2em;
            margin-bottom: 20px;
        }
        
        .content {
            background-color: white;
            padding: 30px;
            border-radius: 0 0 10px 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .flag {
            width: 100%;
            max-width: 400px;
            height: auto;
            margin: 20px auto;
            border: 1px solid #ddd;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .message {
            font-size: 1.1em;
            line-height: 1.6;
            margin-bottom: 20px;
            text-align: left;
        }
        
        .highlight {
            color: #cc0000;
            font-weight: bold;
        }
        
        .footer {
            margin-top: 30px;
            font-size: 0.9em;
            color: #666;
        }
        
        .countdown {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
        }
        
        .countdown-item {
            background-color: #000066;
            color: white;
            padding: 10px 15px;
            border-radius: 5px;
            min-width: 60px;
        }
        
        .countdown-number {
            font-size: 1.8em;
            font-weight: bold;
        }
        
        .countdown-label {
            font-size: 0.8em;
        }
        
        @media (max-width: 600px) {
            h1 {
                font-size: 1.8em;
            }
            
            .content {
                padding: 20px;
            }
            
            .countdown {
                flex-wrap: wrap;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Selamat Menyambut Hari Kemerdekaan</h1>
            <div class="subtitle">Malaysia Yang Ke-68</div>
            <div class="countdown" id="countdown">
                <div class="countdown-item">
                    <div class="countdown-number" id="days">00</div>
                    <div class="countdown-label">Hari</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="hours">00</div>
                    <div class="countdown-label">Jam</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="minutes">00</div>
                    <div class="countdown-label">Minit</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="seconds">00</div>
                    <div class="countdown-label">Saat</div>
                </div>
            </div>
        </div>
        
        <div class="content">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/66/Flag_of_Malaysia.svg/1200px-Flag_of_Malaysia.svg.png" alt="Bendera Malaysia" class="flag">
            
            <div class="message">
                <p>Pada <span class="highlight">31 Ogos 2023</span>, kita menyambut ulang tahun ke-68 kemerdekaan negara kita yang tercinta, Malaysia.</p>
                
                <p>Mari kita bersama-sama menghargai pengorbanan para pejuang kemerdekaan dan bertekad untuk terus memajukan negara kita dengan semangat <span class="highlight">Perpaduan, Kedaulatan, dan Kemakmuran</span>.</p>
                
                <p>Jadikan sambutan kali ini sebagai momentum untuk memperkukuh hubungan antara kaum dan bersama-sama membina Malaysia yang lebih baik untuk generasi akan datang.</p>
                
                <p><span class="highlight">Merdeka! Merdeka! Merdeka!</span></p>
            </div>
            
            <div class="footer">
                <p>© 2023 Sambutan Hari Kemerdekaan Malaysia Ke-68</p>
                <p>Jalur Gemilang Berkibar Megah!</p>
            </div>
        </div>
    </div>
    
    <script>
        // Countdown to Merdeka Day (August 31)
        function updateCountdown() {
            const now = new Date();
            let merdekaDate = new Date(now.getFullYear(), 7, 31); // August is month 7 (0-indexed)
            
            // If Merdeka Day has already passed this year, set for next year
            if (now > merdekaDate) {
                merdekaDate = new Date(now.getFullYear() + 1, 7, 31);
            }
            
            const diff = merdekaDate - now;
            
            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((diff % (1000 * 60)) / 1000);
            
            document.getElementById('days').textContent = days.toString().padStart(2, '0');
            document.getElementById('hours').textContent = hours.toString().padStart(2, '0');
            document.getElementById('minutes').textContent = minutes.toString().padStart(2, '0');
            document.getElementById('seconds').textContent = seconds.toString().padStart(2, '0');
        }
        
        // Update countdown every second
        updateCountdown();
        setInterval(updateCountdown, 1000);
    </script>
</body>
</html>
