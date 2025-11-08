[Uploading vinod_singh_portfolio.html…]()
<!DOCTYPE html>
<html lang="hi" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vinod Singh | Motion Graphics Designer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700;900&family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    
    <!-- Chosen Palette: Dark Navy (#0F172A), Neon Blue (#00A9FF), Warm Orange (#FF914D) -->
    <!-- Application Structure Plan: The multi-page plan from the source file was synthesized into a single-page scrolling application. This structure is more modern and user-friendly for a portfolio, allowing a client to get a complete picture of the designer in a single, linear flow without page loads. The navigation bar is sticky and tracks the user's scroll position, highlighting the active section. The user flow is designed as a conversion funnel: Hero (Intro) -> Services (Value) -> Work (Proof) -> About (Trust) -> Contact (Conversion). This is the most logical and effective structure for usability and achieving the goal of landing a project. -->
    <!-- Visualization & Content Choices: 
        1. Report Info: "Tools I Master" list from the 'About' section. Goal: Visually quantify the designer's proficiency. Viz/Presentation: Polar Area Chart. Interaction: Tooltip on hover shows tool name and proficiency percentage. Justification: A chart is far more engaging and visually appropriate for a designer's portfolio than a static bullet list, turning skills into compelling data. Library: Chart.js (Canvas).
        2. Report Info: "Project Card Structure" from the 'Work' section. Goal: Showcase detailed project information without cluttering the main gallery. Viz/Presentation: HTML/Tailwind Modal (Lightbox). Interaction: User clicks a project thumbnail, which triggers a JS function to populate and display a modal with project details. A close button hides the modal. Justification: This is a standard, user-friendly UI pattern for galleries that keeps the main page clean while allowing for a content-rich deep-dive on demand. Library: Vanilla JS.
        3. Report Info: Key stats ("4 years experience," "45% increase in click-through"). Goal: Highlight key achievements immediately. Viz/Presentation: HTML/Tailwind "Stat Cards". Interaction: None (static display). Justification: Presents high-impact numbers in a clean, easily digestible format to build trust quickly. Library: HTML/Tailwind.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'dark-navy': '#0F172A',
                        'neon-blue': '#00A9FF',
                        'warm-orange': '#FF914D',
                    },
                    fontFamily: {
                        sans: ['Poppins', 'Montserrat', 'sans-serif'],
                        title: ['Montserrat', 'sans-serif'],
                    },
                },
            },
        };
    </script>
    <style>
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 450px;
            margin-left: auto;
            margin-right: auto;
            height: 40vh;
            max-height: 450px;
        }
        .nav-link.active {
            color: #00A9FF;
            font-weight: 700;
        }
        .modal-content {
            background-color: #1a2641;
        }
    </style>
</head>
<body class="bg-dark-navy text-gray-200 font-sans">

    <header class="bg-dark-navy/90 backdrop-blur-md sticky top-0 z-50 w-full shadow-lg">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#home" class="text-2xl font-title font-bold text-white">
                VS <span class="text-neon-blue">Motion</span>
            </a>
            <div class="hidden md:flex space-x-6">
                <a href="#home" class="nav-link text-gray-300 hover:text-neon-blue transition duration-300" data-section="home">Home</a>
                <a href="#services" class="nav-link text-gray-300 hover:text-neon-blue transition duration-300" data-section="services">Services</a>
                <a href="#work" class="nav-link text-gray-300 hover:text-neon-blue transition duration-300" data-section="work">Work</a>
                <a href="#about" class="nav-link text-gray-300 hover:text-neon-blue transition duration-300" data-section="about">About</a>
                <a href="#contact" class="nav-link text-gray-300 hover:text-neon-blue transition duration-300" data-section="contact">Contact</a>
            </div>
            <a href="#contact" class="hidden md:inline-block bg-neon-blue text-dark-navy font-bold py-2 px-5 rounded-full hover:bg-white transition duration-300">
                Hire Me
            </a>
        </nav>
    </header>

    <main>
        <section id="home" class="h-screen min-h-[700px] flex items-center justify-center text-center relative px-4" style="background: linear-gradient(rgba(15, 23, 42, 0.8), rgba(15, 23, 42, 1)), url('https://placehold.co/1920x1080/0F172A/1E293B?text=Motion+Reel+Placeholder') no-repeat center center; background-size: cover;">
            <div class="max-w-3xl">
                <h1 class="text-5xl md:text-7xl font-title font-black text-white mb-4">
                    Hi, I’m <span class="text-neon-blue">Vinod Singh</span>.
                </h1>
                <p class="text-xl md:text-2xl text-gray-300 mb-8">
                    Motion Graphic Designer crafting visuals that move. I bring brands to life, frame by frame.
                </p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#work" class="bg-neon-blue text-dark-navy font-bold py-3 px-8 rounded-full text-lg hover:bg-white transition duration-300">
                        Watch My Showreel
                    </a>
                    <a href="#contact" class="bg-transparent border-2 border-warm-orange text-warm-orange font-bold py-3 px-8 rounded-full text-lg hover:bg-warm-orange hover:text-dark-navy transition duration-300">
                        Start a Project
                    </a>
                </div>
            </div>
        </section>

        <section id="services" class="py-20 md:py-32 px-4 bg-dark-navy">
            <div class="container mx-auto text-center">
                <h2 class="text-4xl md:text-5xl font-title font-bold text-white mb-4">What I Offer</h2>
                <p class="text-lg text-gray-400 max-w-2xl mx-auto mb-16">
                    Specialized motion graphic services designed to meet your every need, from quick social reels to full-scale brand campaigns.
                </p>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div class="bg-gray-900/50 p-8 rounded-lg shadow-xl border border-gray-700 hover:border-neon-blue transition duration-300 transform hover:-translate-y-2">
                        <h3 class="text-2xl font-bold text-white mb-3">Brand & Logo Animation</h3>
                        <p class="text-gray-400">Creating memorable, impactful logo reveals, animated intros, and complete brand identity packages.</p>
                    </div>
                    <div class="bg-gray-900/50 p-8 rounded-lg shadow-xl border border-gray-700 hover:border-neon-blue transition duration-300 transform hover:-translate-y-2">
                        <h3 class="text-2xl font-bold text-white mb-3">Product Explainer Videos</h3>
                        <p class="text-gray-400">Simplifying complex ideas with 2D and 3D explainer videos that clearly communicate your product's value.</p>
                    </div>
                    <div class="bg-gray-900/50 p-8 rounded-lg shadow-xl border border-gray-700 hover:border-neon-blue transition duration-300 transform hover:-translate-y-2">
                        <h3 class="text-2xl font-bold text-white mb-3">Social Media & Digital Ads</h3>
                        <p class="text-gray-400">High-impact, short-form motion graphics optimized for Instagram Reels, YouTube Shorts, and paid ads.</p>
                    </div>
                    <div class="bg-gray-900/50 p-8 rounded-lg shadow-xl border border-gray-700 hover:border-neon-blue transition duration-300 transform hover:-translate-y-2">
                        <h3 class="text-2xl font-bold text-white mb-3">Visual Effects & Compositing</h3>
                        <p class="text-gray-400">Post-production magic, including screen replacements, motion tracking, and advanced compositing.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="work" class="py-20 md:py-32 px-4 bg-gray-900/50">
            <div class="container mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-4xl md:text-5xl font-title font-bold text-white mb-4">Our Moving Stories</h2>
                    <p class="text-lg text-gray-400 max-w-2xl mx-auto">
                        A curated selection of my best work across brand explainer videos, digital advertising, and comprehensive visual effects projects.
                    </p>
                </div>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div class="group relative rounded-lg overflow-hidden cursor-pointer" onclick="openModal('jainShikanji')">
                        <img src="https://placehold.co/600x400/FF914D/0F172A?text=Jain+Shikanji+Ad" alt="Project Thumbnail" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                        <div class="absolute inset-0 bg-dark-navy bg-opacity-0 group-hover:bg-opacity-80 transition duration-500 flex items-center justify-center">
                            <div class="text-center p-4 opacity-0 group-hover:opacity-100 transition duration-500 transform translate-y-4 group-hover:translate-y-0">
                                <h3 class="text-2xl font-bold text-white">Brand Explainer Ad</h3>
                                <p class="text-neon-blue">Jain Shikanji</p>
                            </div>
                        </div>
                    </div>
                    <div class="group relative rounded-lg overflow-hidden cursor-pointer" onclick="openModal('techProduct')">
                        <img src="https://placehold.co/600x400/00A9FF/0F172A?text=Tech+Product+Launch" alt="Project Thumbnail" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                        <div class="absolute inset-0 bg-dark-navy bg-opacity-0 group-hover:bg-opacity-80 transition duration-500 flex items-center justify-center">
                            <div class="text-center p-4 opacity-0 group-hover:opacity-100 transition duration-500 transform translate-y-4 group-hover:translate-y-0">
                                <h3 class="text-2xl font-bold text-white">Tech Product Launch</h3>
                                <p class="text-neon-blue">Social Media Ad</p>
                            </div>
                        </div>
                    </div>
                    <div class="group relative rounded-lg overflow-hidden cursor-pointer" onclick="openModal('logoReel')">
                        <img src="https://placehold.co/600x400/EEEEEE/0F172A?text=Logo+Animation+Reel" alt="Project Thumbnail" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                        <div class="absolute inset-0 bg-dark-navy bg-opacity-0 group-hover:bg-opacity-80 transition duration-500 flex items-center justify-center">
                            <div class="text-center p-4 opacity-0 group-hover:opacity-100 transition duration-500 transform translate-y-4 group-hover:translate-y-0">
                                <h3 class="text-2xl font-bold text-white">Logo Animation Reel</h3>
                                <p class="text-neon-blue">Brand Identity</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="about" class="py-20 md:py-32 px-4">
            <div class="container mx-auto">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
                    <div>
                        <h2 class="text-4xl md:text-5xl font-title font-bold text-white mb-6">Frame by Frame, Story by Story.</h2>
                        <p class="text-lg text-gray-300 mb-6">
                            Hello! I’m <strong>Vinod Singh</strong>—a passionate and dedicated motion graphic designer based in Delhi NCR, working with clients globally.
                        </p>
                        <p class="text-gray-400 mb-8">
                            My career is built on the belief that animation is the most powerful tool for visual storytelling. My work is driven by a simple goal: helping businesses connect with their audience through dynamic, visually compelling motion.
                        </p>
                        <div class="grid grid-cols-2 gap-6 text-center">
                            <div class="bg-gray-900/50 p-6 rounded-lg">
                                <span class="text-5xl font-bold text-neon-blue">4+</span>
                                <p class="text-gray-400 mt-2">Years of Experience</p>
                            </div>
                            <div class="bg-gray-900/50 p-6 rounded-lg">
                                <span class="text-5xl font-bold text-warm-orange">45%</span>
                                <p class="text-gray-400 mt-2">Avg. CTR Boost (for clients)</p>
                            </div>
                        </div>
                    </div>
                    <div>
                        <h3 class="text-3xl font-bold text-white mb-8 text-center lg:text-left">Tools I Master</h3>
                        <div class="chart-container">
                            <canvas id="toolkitChart"></canvas>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="contact" class="py-20 md:py-32 px-4 bg-gray-900/50">
            <div class="container mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-4xl md:text-5xl font-title font-bold text-white mb-4">Let’s Create Something Amazing.</h2>
                    <p class="text-lg text-gray-400 max-w-2xl mx-auto">
                        Please share a few details about your project, your estimated budget, and the desired timeline. I will respond within 24 hours.
                    </p>
                </div>
                <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-12">
                    <form action="#" method="POST" class="space-y-6">
                        <div>
                            <label for="name" class="block text-sm font-medium text-gray-300">Your Name</label>
                            <input type="text" id="name" name="name" class="mt-1 block w-full bg-gray-800 border-gray-700 rounded-md shadow-sm py-3 px-4 text-white focus:border-neon-blue focus:ring-neon-blue">
                        </div>
                        <div>
                            <label for="email" class="block text-sm font-medium text-gray-300">Your Email</label>
                            <input type="email" id="email" name="email" class="mt-1 block w-full bg-gray-800 border-gray-700 rounded-md shadow-sm py-3 px-4 text-white focus:border-neon-blue focus:ring-neon-blue">
                        </div>
                        <div>
                            <label for="message" class="block text-sm font-medium text-gray-300">Project Details</label>
                            <textarea id="message" name="message" rows="5" class="mt-1 block w-full bg-gray-800 border-gray-700 rounded-md shadow-sm py-3 px-4 text-white focus:border-neon-blue focus:ring-neon-blue"></textarea>
                        </div>
                        <div>
                            <button type="submit" class="w-full bg-neon-blue text-dark-navy font-bold py-3 px-6 rounded-full text-lg hover:bg-white transition duration-300">
                                Send Message
                            </button>
                        </div>
                    </form>
                    <div class="space-y-6 pt-6">
                        <h3 class="text-2xl font-bold text-white">Contact Details</h3>
                        <a href="mailto:vinod@yourdomain.com" class="flex items-center group">
                            <div class="p-3 bg-gray-800 rounded-full mr-4 group-hover:bg-warm-orange transition duration-300">
                                <span class="text-warm-orange group-hover:text-dark-navy text-xl">✉️</span>
                            </div>
                            <div>
                                <p class="text-gray-400">Email Directly</p>
                                <p class="text-white text-lg font-medium group-hover:text-warm-orange transition duration-300">vinod@yourdomain.com</p>
                            </div>
                        </a>
                        <a href="https://wa.me/91XXXXXXXXXX" target="_blank" class="flex items-center group">
                            <div class="p-3 bg-gray-800 rounded-full mr-4 group-hover:bg-neon-blue transition duration-300">
                                <span class="text-neon-blue group-hover:text-dark-navy text-xl">💬</span>
                            </div>
                            <div>
                                <p class="text-gray-400">WhatsApp Chat</p>
                                <p class="text-white text-lg font-medium group-hover:text-neon-blue transition duration-300">wa.me/91XXXXXXXXXX</p>
                            </div>
                        </a>
                        <div class="flex items-center">
                            <div class="p-3 bg-gray-800 rounded-full mr-4">
                                <span class="text-gray-400 text-xl">📍</span>
                            </div>
                            <div>
                                <p class="text-gray-400">Location</p>
                                <p class="text-white text-lg font-medium">Delhi NCR, India (Working Globally)</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-dark-navy border-t border-gray-800 py-8 px-4">
        <div class="container mx-auto text-center text-gray-500">
            <div class="flex justify-center space-x-6 mb-4">
                <a href="#" class="hover:text-neon-blue transition duration-300">Behance</a>
                <a href="#" class="hover:text-neon-blue transition duration-300">Dribbble</a>
                <a href="#" class="hover:text-neon-blue transition duration-300">Instagram</a>
                <a href="#" class="hover:text-neon-blue transition duration-300">YouTube</a>
            </div>
            <p>&copy; 2025 Vinod Singh. All Rights Reserved.</p>
        </div>
    </footer>

    <div id="projectModal" class="fixed inset-0 z-[100] flex items-center justify-center bg-black bg-opacity-80 p-4 hidden" onclick="closeModal()">
        <div class="modal-content w-full max-w-3xl max-h-[90vh] rounded-lg shadow-2xl overflow-hidden" onclick="event.stopPropagation()">
            <div class="flex justify-between items-center p-5 border-b border-gray-700">
                <h3 id="modalTitle" class="text-2xl font-bold text-white">Project Title</h3>
                <button onclick="closeModal()" class="text-gray-400 hover:text-white text-3xl">&times;</button>
            </div>
            <div class="p-6 md:p-8 overflow-y-auto max-h-[calc(90vh-140px)]">
                <div class="w-full h-auto aspect-video bg-gray-900 rounded-lg mb-6 flex items-center justify-center">
                    <span class="text-gray-500">Video Placeholder (16:9)</span>
                </div>
                <h4 class="text-lg font-semibold text-neon-blue" id="modalCategory">Category</h4>
                <p class="text-gray-300 my-4" id="modalDescription">Project description...</p>
                <div class="grid grid-cols-2 gap-4">
                    <div>
                        <strong class="text-gray-400 block mb-1">Tools Used:</strong>
                        <p id="modalTools" class="text-white"></p>
                    </div>
                    <div>
                        <strong class="text-gray-400 block mb-1">Key Result:</strong>
                        <p id="modalResult" class="text-white"></p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const projectData = {
            jainShikanji: {
                title: "Brand Explainer Ad - Jain Shikanji",
                category: "Explainer Video / Social Media Ad",
                description: "A vibrant, 60-second animated explainer video created to boost online engagement and product clarity for a major FMCG brand.",
                tools: "Adobe After Effects, Illustrator, Premiere Pro",
                result: "Achieved a 45% increase in click-through rate on digital platforms."
            },
            techProduct: {
                title: "Tech Product Launch",
                category: "Social Media Ad / 3D Animation",
                description: "A series of high-impact, 15-second vertical videos for an international tech product launch. Focused on dynamic 3D rendering and kinetic typography.",
                tools: "Blender, After Effects, Photoshop",
                result: "Contributed to a record-breaking launch day sales target."
            },
            logoReel: {
                title: "Logo Animation Reel 2024",
                category: "Brand Identity / Logo Animation",
                description: "A compilation of my best logo animations from the past year, showcasing various styles from minimal and corporate to complex 3D reveals.",
                tools: "After Effects, Blender, Illustrator",
                result: "Featured on a prominent design inspiration blog."
            }
        };

        const modal = document.getElementById('projectModal');
        const modalTitle = document.getElementById('modalTitle');
        const modalCategory = document.getElementById('modalCategory');
        const modalDescription = document.getElementById('modalDescription');
        const modalTools = document.getElementById('modalTools');
        const modalResult = document.getElementById('modalResult');

        function openModal(projectId) {
            if (projectData[projectId]) {
                const data = projectData[projectId];
                modalTitle.textContent = data.title;
                modalCategory.textContent = data.category;
                modalDescription.textContent = data.description;
                modalTools.textContent = data.tools;
                modalResult.textContent = data.result;
                modal.classList.remove('hidden');
            }
        }

        function closeModal() {
            modal.classList.add('hidden');
        }

        const ctx = document.getElementById('toolkitChart').getContext('2d');
        const toolkitChart = new Chart(ctx, {
            type: 'polarArea',
            data: {
                labels: ['Adobe After Effects', 'Adobe Premiere Pro', 'Blender (3D)', 'Adobe Illustrator & Photoshop'],
                datasets: [{
                    label: 'Proficiency',
                    data: [95, 90, 80, 85],
                    backgroundColor: [
                        'rgba(0, 169, 255, 0.7)',  
                        'rgba(255, 145, 77, 0.7)',
                        'rgba(0, 169, 255, 0.5)',
                        'rgba(255, 145, 77, 0.5)'
                    ],
                    borderColor: [
                        '#00A9FF',
                        '#FF914D',
                        '#00A9FF',
                        '#FF914D'
                    ],
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    r: {
                        grid: { color: 'rgba(255, 255, 255, 0.1)' },
                        angleLines: { color: 'rgba(255, 255, 255, 0.1)' },
                        pointLabels: {
                            color: '#FFFFFF',
                            font: {
                                size: 13,
                                family: 'Poppins'
                            }
                        },
                        ticks: {
                            display: false,
                            backdropColor: 'transparent'
                        }
                    }
                },
                plugins: {
                    legend: {
                        position: 'bottom',
                        labels: {
                            color: '#FFFFFF',
                            font: {
                                size: 14,
                                family: 'Poppins'
                            }
                        }
                    },
                    tooltip: {
                        callbacks: {
                            label: function(context) {
                                return context.label + ': ' + context.raw + '%';
                            }
                        }
                    }
                }
            }
        });

        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('.nav-link');

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    navLinks.forEach(link => {
                        link.classList.remove('active');
                        if (link.dataset.section === entry.target.id) {
                            link.classList.add('active');
                        }
                    });
                }
            });
        }, { rootMargin: '-30% 0px -70% 0px' }); 

        sections.forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>
