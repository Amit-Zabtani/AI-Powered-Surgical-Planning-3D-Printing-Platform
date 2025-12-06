<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CustoMED | AI-Powered Surgical Solutions on Google Cloud</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a73e8;
            --primary-dark: #0d47a1;
            --accent: #34a853;
            --light: #ffffff;
            --gray-light: #f8f9fa;
            --gray: #5f6368;
            --dark: #202124;
            --transition: all 0.3s ease;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            --radius: 8px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
            overflow-x: hidden;
        }

        h1, h2, h3, h4, h5 {
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
            line-height: 1.3;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            background-color: var(--light);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }

        .logo-text {
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            font-size: 24px;
            color: var(--primary);
            margin-left: 10px;
        }

        .logo-text span {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            font-size: 16px;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--primary);
            left: 0;
            bottom: -5px;
            transition: var(--transition);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 24px;
            color: var(--dark);
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            padding: 100px 0 80px;
            background: linear-gradient(135deg, #f8f9fa 0%, #ffffff 100%);
            position: relative;
            overflow: hidden;
        }

        .hero:before {
            content: '';
            position: absolute;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(26, 115, 232, 0.05) 0%, rgba(52, 168, 83, 0.05) 100%);
            top: -100px;
            right: -100px;
        }

        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .hero-text {
            flex: 1;
            max-width: 600px;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .hero-image img {
            max-width: 100%;
            height: auto;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }

        .hero h1 {
            font-size: 42px;
            margin-bottom: 20px;
            color: var(--dark);
        }

        .hero h1 span {
            color: var(--primary);
        }

        .hero p {
            font-size: 18px;
            color: var(--gray);
            margin-bottom: 30px;
            max-width: 550px;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary);
            color: var(--light);
            padding: 14px 32px;
            border-radius: var(--radius);
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(26, 115, 232, 0.2);
        }

        .btn-outline {
            background-color: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
            margin-left: 15px;
        }

        .btn-outline:hover {
            background-color: rgba(26, 115, 232, 0.05);
        }

        /* Section Common */
        .section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 36px;
            color: var(--dark);
            margin-bottom: 15px;
        }

        .section-title p {
            font-size: 18px;
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
        }

        /* Google Cloud Integration */
        .integration {
            background-color: var(--gray-light);
        }

        .integration-item {
            background-color: var(--light);
            border-radius: var(--radius);
            padding: 30px;
            box-shadow: var(--shadow);
            margin-bottom: 30px;
            transition: var(--transition);
        }

        .integration-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .integration-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .integration-icon {
            width: 60px;
            height: 60px;
            background-color: rgba(26, 115, 232, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
        }

        .integration-icon i {
            font-size: 24px;
            color: var(--primary);
        }

        .integration-item h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--dark);
        }

        .integration-item p {
            color: var(--gray);
            margin-bottom: 15px;
        }

        /* How It Works */
        .steps {
            display: flex;
            justify-content: space-between;
            position: relative;
            margin-top: 50px;
        }

        .step {
            flex: 1;
            text-align: center;
            padding: 0 15px;
            position: relative;
        }

        .step-number {
            width: 60px;
            height: 60px;
            background-color: var(--primary);
            color: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: 700;
            margin: 0 auto 20px;
            position: relative;
            z-index: 2;
        }

        .step h3 {
            font-size: 20px;
            margin-bottom: 15px;
            color: var(--dark);
        }

        .step p {
            color: var(--gray);
        }

        .steps:before {
            content: '';
            position: absolute;
            top: 30px;
            left: 10%;
            right: 10%;
            height: 3px;
            background-color: rgba(26, 115, 232, 0.2);
            z-index: 1;
        }

        /* Solution Benefits */
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }

        .benefit-item {
            text-align: center;
            padding: 30px 20px;
            border-radius: var(--radius);
            background-color: var(--light);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }

        .benefit-item:hover {
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
        }

        .benefit-icon {
            font-size: 40px;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .benefit-item h3 {
            font-size: 20px;
            margin-bottom: 15px;
            color: var(--dark);
        }

        /* CTA Section */
        .cta {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: var(--light);
            text-align: center;
            padding: 80px 0;
        }

        .cta h2 {
            font-size: 36px;
            margin-bottom: 20px;
        }

        .cta p {
            font-size: 18px;
            margin-bottom: 30px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0.9;
        }

        .cta .btn {
            background-color: var(--light);
            color: var(--primary);
        }

        .cta .btn:hover {
            background-color: rgba(255, 255, 255, 0.9);
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: var(--light);
            padding: 60px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 20px;
            margin-bottom: 20px;
            color: var(--light);
        }

        .footer-column p, .footer-column a {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-column a:hover {
            color: var(--light);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
            font-size: 14px;
        }

        /* Responsive */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-text {
                margin-bottom: 50px;
            }
            
            .steps {
                flex-direction: column;
            }
            
            .step {
                margin-bottom: 40px;
            }
            
            .steps:before {
                display: none;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background-color: var(--light);
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 10px 0;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .section-title h2 {
                font-size: 28px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">
                <div class="logo-text">Custo<span>MED</span></div>
            </a>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#solution">Solution</a></li>
                <li><a href="#integration">Google Cloud Integration</a></li>
                <li><a href="#how-it-works">How It Works</a></li>
                <li><a href="#benefits">Benefits</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>AI-Powered Surgical Planning on <span>Google Cloud</span></h1>
                    <p>CustoMED revolutionizes surgical planning and execution by leveraging a surgeon-first intuitive interface powered by automation and AI to transform medical imaging into 3D visualizations, plan procedures, and generate personalized 3D-printed surgical solutions within minutes at scale.</p>
                    <div>
                        <a href="#solution" class="btn">Explore Our Solution</a>
                        <a href="#integration" class="btn btn-outline">Google Cloud Integration</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1559757148-5c350d0d3c56?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="CustoMED Surgical Planning Interface">
                </div>
            </div>
        </div>
    </section>

    <!-- Solution Section -->
    <section class="section" id="solution">
        <div class="container">
            <div class="section-title">
                <h2>Our AI-Powered Surgical Solution</h2>
                <p>CustoMED transforms surgical planning and execution by converting medical imaging into 3D visualizations, planning procedures, and producing customized 3D-printed surgical solutions at scale in minutes.</p>
            </div>
            
            <div class="integration-grid">
                <div class="integration-item">
                    <div class="integration-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3>AI-Driven 3D Reconstruction</h3>
                    <p>Our proprietary AI algorithms transform 2D medical scans into interactive 3D models with unprecedented accuracy and speed.</p>
                </div>
                
                <div class="integration-item">
                    <div class="integration-icon">
                        <i class="fas fa-procedures"></i>
                    </div>
                    <h3>Surgical Planning Interface</h3>
                    <p>Surgeon-first intuitive interface allows precise planning, simulation, and visualization of complex surgical procedures.</p>
                </div>
                
                <div class="integration-item">
                    <div class="integration-icon">
                        <i class="fas fa-print"></i>
                    </div>
                    <h3>Personalized 3D Printing</h3>
                    <p>Generate patient-specific surgical guides, implants, and tools ready for 3D printing within minutes.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Google Cloud Integration -->
    <section class="section integration" id="integration">
        <div class="container">
            <div class="section-title">
                <h2>Google Cloud Integration</h2>
                <p>Our solution is built on Google Cloud to deliver scalability, security, and intelligence at every step of the surgical planning process.</p>
            </div>
            
            <div class="integration-grid">
                <div class="integration-item">
                    <div class="integration-icon">
                        <i class="fas fa-robot"></i>
                    </div>
                    <h3>Vertex AI for Medical Imaging</h3>
                    <p>Proprietary deep-learning models on Vertex AI segment anatomical structures from 2D scans and reconstruct high-fidelity 3D visualizations in real time.</p>
                    <p><strong>Impact:</strong> Reduces manual reconstruction time from hours to seconds.</p>
                </div>
                
                <div class="integration-item">
                    <div class="integration-icon">
                        <i class="fas fa-database"></i>
                    </div>
                    <h3>Healthcare API & Cloud Storage</h3>
                    <p>DICOM/imaging data is securely stored in Cloud Storage with metadata managed via Healthcare API for structured interoperability with hospital systems.</p>
                    <p><strong>Impact:</strong> HIPAA-compliant data handling with full audit trails.</p>
                </div>
                
                <div class="integration-item">
                    <div class="integration-icon">
                        <i class="fas fa-server"></i>
                    </div>
                    <h3>GKE & Compute Engine</h3>
                    <p>The web-based 3D planning environment runs on GKE for high availability. Compute Engine with GPU acceleration handles intensive mesh processing.</p>
                    <p><strong>Impact:</strong> Elastic scaling during concurrent user sessions.</p>
                </div>
                
                <div class="integration-item">
                    <div class="integration-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>BigQuery & Looker Analytics</h3>
                    <p>Aggregated, de-identified procedure data analyzed in BigQuery provides insights into surgical outcomes and process efficiency via Looker dashboards.</p>
                    <p><strong>Impact:</strong> Data-driven continuous improvement of surgical workflows.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- How It Works -->
    <section class="section" id="how-it-works">
        <div class="container">
            <div class="section-title">
                <h2>How It Works</h2>
                <p>From medical imaging to 3D-printed surgical solutions in minutes</p>
            </div>
            
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Medical Imaging Upload</h3>
                    <p>Surgeons upload DICOM files via our secure, HIPAA-compliant web portal integrated with Google Healthcare API.</p>
                </div>
                
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>AI-Powered 3D Reconstruction</h3>
                    <p>Vertex AI models automatically convert 2D scans into interactive 3D anatomical models with precision.</p>
                </div>
                
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>Surgical Planning</h3>
                    <p>Surgeons interact with 3D models in our GKE-hosted interface to plan and simulate procedures with AI assistance.</p>
                </div>
                
                <div class="step">
                    <div class="step-number">4</div>
                    <h3>3D Printing & Delivery</h3>
                    <p>Patient-specific surgical guides are generated and sent to 3D printing facilities, ready for surgery within hours.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits -->
    <section class="section" id="benefits">
        <div class="container">
            <div class="section-title">
                <h2>Key Benefits</h2>
                <p>How CustoMED powered by Google Cloud delivers surgical excellence</p>
            </div>
            
            <div class="benefits-grid">
                <div class="benefit-item">
                    <div class="benefit-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3>Time Efficiency</h3>
                    <p>Reduce planning time from days to minutes with automated 3D reconstruction and AI assistance.</p>
                </div>
                
                <div class="benefit-item">
                    <div class="benefit-icon">
                        <i class="fas fa-bullseye"></i>
                    </div>
                    <h3>Precision & Accuracy</h3>
                    <p>AI-driven models provide millimeter-accurate anatomical reconstructions for better surgical outcomes.</p>
                </div>
                
                <div class="benefit-item">
                    <div class="benefit-icon">
                        <i class="fas fa-expand-arrows-alt"></i>
                    </div>
                    <h3>Scalability</h3>
                    <p>Google Cloud infrastructure allows us to serve hospitals worldwide with consistent performance.</p>
                </div>
                
                <div class="benefit-item">
                    <div class="benefit-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Security & Compliance</h3>
                    <p>Built on Google Cloud's secure infrastructure with HIPAA and GDPR compliance by design.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="contact">
        <div class="container">
            <h2>Ready to Transform Surgical Planning?</h2>
            <p>Join leading hospitals and surgical centers using CustoMED on Google Cloud to deliver personalized surgical excellence.</p>
            <a href="mailto:amit@customed.info" class="btn">Contact Our Team</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>CustoMED</h3>
                    <p>Revolutionizing surgical planning and execution with AI-powered solutions on Google Cloud.</p>
                    <p>Tel Aviv, Israel</p>
                </div>
                
                <div class="footer-column">
                    <h3>Contact</h3>
                    <a href="mailto:amit@customed.info">amit@customed.info</a>
                    <a href="https://customed.info" target="_blank">customed.info</a>
                </div>
                
                <div class="footer-column">
                    <h3>Google Cloud Integration</h3>
                    <a href="#integration">Vertex AI</a>
                    <a href="#integration">Healthcare API</a>
                    <a href="#integration">Google Kubernetes Engine</a>
                    <a href="#integration">BigQuery & Looker</a>
                </div>
                
                <div class="footer-column">
                    <h3>Resources</h3>
                    <a href="#solution">Our Solution</a>
                    <a href="#how-it-works">How It Works</a>
                    <a href="#benefits">Benefits</a>
                    <a href="#contact">Request Demo</a>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 CustoMED. All rights reserved. | AI-Powered Surgical Solutions on Google Cloud</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navLinks = document.getElementById('navLinks');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            mobileMenuBtn.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
