<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Digital Portfolio | Zulfan Fikri</title>
    <link href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            min-height: 100vh;
            background: #0a0a0a;
            color: rgba(255,255,255,0.9);
            overflow: hidden;
        }

        .container {
            width: 100vw;
            height: 100vh;
            padding: 2rem;
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 2rem;
            background: rgba(16,16,16,0.95);
            backdrop-filter: blur(15px);
            overflow: hidden;  /* Tambahkan ini */
            display: flex;     /* Tambahkan ini */
            align-items: center;  /* Tambahkan ini */
            justify-content: center;  /* Tambahkan ini */
        }
        
        .profile-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;    /* Tambahkan ini */
            border-radius: 50%;
            object-position: center 35%;  /* Sesuaikan angka ini */
        }
        /* Profile Section */
        .profile-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            border-right: 1px solid rgba(255,255,255,0.1);
            padding-right: 2rem;
        }
        .profile-name {
            font-size: 2 rem;
            text-align: left;
            margin-bottom: 1rem;
            white-space: nowrap;
        }
        .profile-frame {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 3px solid #6a00ff;
            padding: 5px;
            margin-bottom: 1.5rem;
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .profile-frame:hover {
            transform: scale(1.05);
        }

        /* Content Section */
        .content-section {
            display: grid;
            grid-template-rows: auto auto 1fr auto;
            height: 100%;
        }

        .glass-card {
            background: rgba(255,255,255,0.05);
            border-radius: 15px;
            padding: 1.5rem;
            margin-bottom: 1rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
        }

        .glass-card:hover {
            background: rgba(255,255,255,0.08);
            transform: translateY(-3px);
        }
        .running-text {
            font-size: 2.5rem;  /* Ukuran font diperbesar */
            color: #ffffff;
            white-space: nowrap;
            overflow: hidden;
            position: relative;
            padding: 10px 0;
        }
        
        @keyframes runText {
            0% {
                transform: translateX(-100%);
            }
            100% {
                transform: translateX(100%);
            }
        }
        
        .running-text span {
            display: inline-block;
            animation: runText 8s linear infinite;  /* Kecepatan dipercepat dari 15s ke 8s */
            font-weight: bold;
            font-style: italic;  /* Menambahkan italic */
        }
        /* Footer Styles */
        .footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
            border-top: 1px solid rgba(255,255,255,0.1);
            margin-top: auto;
        }

        .social-links a {
            color: rgba(255,255,255,0.7);
            font-size: 1.5rem;
            margin: 0 0.5rem;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            color: #6a00ff;
            transform: scale(1.2);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
                padding: 1rem;
            }
            
            .profile-section {
                border-right: none;
                padding-right: 0;
                margin-bottom: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Profile Section -->
        <section class="profile-section">
            <div class="glass-card">
                <div class="profile-frame">
                    <img src="fotokyu.jpg" alt="Your Name" style="width:100%; border-radius:50%">
                </div>
                <h1 style="font-size: 2rem; text-align: center; margin-bottom: 1rem">Zulfan Fikri</h1>

                <div class="social-links">
                    <a href="https://www.linkedin.com/in/zulfan-fikri-75134524a/"><i class='bx bxl-linkedin'></i></a>
                    <a href="https://www.instagram.com/fikri.fanani/"><i class='bx bxl-instagram'></i></a>
                </div>
            </div>
        </section>

        <!-- Content Section -->
        <section class="content-section">
            <!-- Summary -->
            <div class="glass-card">
                <h2>About Me</h2>
                <p>Aku, Zulfan Fikri, berusia 17 tahun dan memiliki minat yang besar dalam bidang Matematika dan Teknologi. Aku berambisi untuk mengembangkan keterampilanku lebih lanjut di bidang ini, terutama dalam ilmu komputer, dengan fokus pada machine learning dan AI.</p>
            </div>

            <!-- Experience & Education -->
            <div class="grid-container" style="display: grid; gap: 1rem; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr))">
                

                <div class="glass-card">
                    <h2>Education</h2>
                    <ul style="list-style: none;">
                        <li>SMA Negeri 7 Yogyakarta (2022-2025)</li>
                        <li>Certified AWS Developer</li>
                    </ul>
                </div>
            </div>

            <!-- Collaboration CTA -->
            <!--<div class="glass-card" style="text-align: center; background: rgba(106,0,255,0.1);">
                <div class="running-text">
                    <span>Create Your System.</span>
                </div>
                <h2>Let's Create Something Amazing!</h2>
                <p>Ready to collaborate on your next project?</p>
                <button style="background: #6a00ff; color: white; border: none; padding: 0.8rem 2rem; 
                    border-radius: 25px; margin-top: 1rem; cursor: pointer;">Get in Touch</button>
            </div>


            <!Footer -->
            <footer class="footer">
                <div>© 2025</div>
                <nav>
                    <a href="#" style="color: rgba(255,255,255,0.7); margin: 0 1rem; text-decoration: none">Contact</a>
                </nav>
            </footer>
        </section>
    </div>

    <script>
        // Smooth hover effects
        document.querySelectorAll('.glass-card').forEach(card => {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                card.style.setProperty('--x', `${x}px`);
                card.style.setProperty('--y', `${y}px`);
            });
        });

        // Responsive layout handling
        window.addEventListener('resize', () => {
            document.documentElement.style.setProperty('--window-height', `${window.innerHeight}px`);
        });
    </script>
</body>
</html>
