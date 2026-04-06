<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JK Gaming - Ultimate Game Download Platform</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        gaming: {
                            dark: '#0a0a0f',
                            purple: '#6d28d9',
                            neon: '#00f3ff',
                            accent: '#ff00ff',
                            surface: '#1a1a2e'
                        }
                    },
                    animation: {
                        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'glow': 'glow 2s ease-in-out infinite alternate',
                        'float': 'float 6s ease-in-out infinite',
                        'slide-up': 'slideUp 0.5s ease-out',
                        'spin-slow': 'spin 3s linear infinite'
                    },
                    keyframes: {
                        glow: {
                            '0%': { boxShadow: '0 0 5px #00f3ff, 0 0 10px #00f3ff, 0 0 15px #00f3ff' },
                            '100%': { boxShadow: '0 0 10px #00f3ff, 0 0 20px #00f3ff, 0 0 30px #00f3ff' }
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' }
                        },
                        slideUp: {
                            '0%': { transform: 'translateY(30px)', opacity: '0' },
                            '100%': { transform: 'translateY(0)', opacity: '1' }
                        }
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;500;700&display=swap');

        body {
            font-family: 'Rajdhani', sans-serif;
            background-color: #0a0a0f;
            overflow-x: hidden;
        }

        .font-orbitron {
            font-family: 'Orbitron', sans-serif;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: #0a0a0f;
        }
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(180deg, #6d28d9, #00f3ff);
            border-radius: 5px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(180deg, #00f3ff, #6d28d9);
        }

        /* Neon Glow Effects */
        .neon-text {
            text-shadow: 0 0 10px rgba(0, 243, 255, 0.5), 0 0 20px rgba(0, 243, 255, 0.3);
        }
        .neon-border {
            box-shadow: 0 0 10px rgba(0, 243, 255, 0.3), inset 0 0 10px rgba(0, 243, 255, 0.1);
        }
        .neon-purple {
            text-shadow: 0 0 10px rgba(109, 40, 217, 0.8);
        }

        /* Card Hover Effects */
        .game-card {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            transform-style: preserve-3d;
        }
        .game-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(0, 243, 255, 0.2), 0 0 30px rgba(109, 40, 217, 0.3);
        }
        .game-card:hover .card-image {
            transform: scale(1.1);
        }
        .game-card:hover .download-btn {
            background: linear-gradient(45deg, #00f3ff, #6d28d9);
            box-shadow: 0 0 20px rgba(0, 243, 255, 0.6);
        }

        /* Loading Animation */
        .loader {
            border: 3px solid rgba(0, 243, 255, 0.1);
            border-top: 3px solid #00f3ff;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Particle Background */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }
        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: #00f3ff;
            border-radius: 50%;
            opacity: 0.5;
            animation: float-particle 10s infinite linear;
        }
        @keyframes float-particle {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100vh) rotate(720deg); opacity: 0; }
        }

        /* Glitch Effect */
        .glitch {
            position: relative;
        }
        .glitch::before,
        .glitch::after {
            content: attr(data-text);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        .glitch::before {
            left: 2px;
            text-shadow: -2px 0 #ff00ff;
            clip: rect(24px, 550px, 90px, 0);
            animation: glitch-anim-1 3s infinite linear alternate-reverse;
        }
        .glitch::after {
            left: -2px;
            text-shadow: -2px 0 #00f3ff;
            clip: rect(85px, 550px, 140px, 0);
            animation: glitch-anim-2 2.5s infinite linear alternate-reverse;
        }
        @keyframes glitch-anim-1 {
            0% { clip: rect(20px, 9999px, 15px, 0); }
            20% { clip: rect(50px, 9999px, 80px, 0); }
            40% { clip: rect(10px, 9999px, 65px, 0); }
            60% { clip: rect(90px, 9999px, 30px, 0); }
            80% { clip: rect(40px, 9999px, 95px, 0); }
            100% { clip: rect(70px, 9999px, 20px, 0); }
        }
        @keyframes glitch-anim-2 {
            0% { clip: rect(65px, 9999px, 100px, 0); }
            20% { clip: rect(15px, 9999px, 60px, 0); }
            40% { clip: rect(85px, 9999px, 20px, 0); }
            60% { clip: rect(30px, 9999px, 75px, 0); }
            80% { clip: rect(95px, 9999px, 40px, 0); }
            100% { clip: rect(10px, 9999px, 85px, 0); }
        }

        /* Search Input Focus */
        .search-input:focus {
            box-shadow: 0 0 20px rgba(0, 243, 255, 0.4);
        }

        /* Mobile Menu */
        .mobile-menu {
            transform: translateX(100%);
            transition: transform 0.3s ease-in-out;
        }
        .mobile-menu.active {
            transform: translateX(0);
        }

        /* Category Filter Active State */
        .category-btn.active {
            background: linear-gradient(45deg, #00f3ff, #6d28d9);
            color: #0a0a0f;
            box-shadow: 0 0 20px rgba(0, 243, 255, 0.5);
        }
    </style>
</head>
<body class="text-gray-100 relative">

    <!-- Particle Background -->
    <div class="particles" id="particles"></div>

    <!-- Loading Screen -->
    <div id="loading-screen" class="fixed inset-0 bg-gaming-dark z-50 flex items-center justify-center transition-opacity duration-500">
        <div class="text-center">
            <div class="loader mx-auto mb-4"></div>
            <h2 class="font-orbitron text-2xl text-gaming-neon animate-pulse">LOADING...</h2>
        </div>
    </div>

    <!-- Navigation -->
    <nav class="fixed w-full z-40 bg-gaming-dark/90 backdrop-blur-md border-b border-gaming-purple/30 transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Logo -->
                <div class="flex-shrink-0 flex items-center gap-3 cursor-pointer group" onclick="window.scrollTo(0,0)">
                    <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-gaming-purple to-gaming-neon flex items-center justify-center group-hover:animate-pulse-slow">
                        <i class="fas fa-gamepad text-2xl text-white"></i>
                    </div>
                    <span class="font-orbitron text-2xl font-bold bg-gradient-to-r from-gaming-neon to-gaming-purple bg-clip-text text-transparent">
                        JK GAMING
                    </span>
                </div>

                <!-- Desktop Menu -->
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-8">
                        <a href="#home" class="nav-link hover:text-gaming-neon transition-colors duration-300 px-3 py-2 rounded-md text-lg font-medium relative group">
                            Home
                            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gaming-neon transition-all duration-300 group-hover:w-full"></span>
                        </a>
                        <a href="#games" class="nav-link hover:text-gaming-neon transition-colors duration-300 px-3 py-2 rounded-md text-lg font-medium relative group">
                            Games
                            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gaming-neon transition-all duration-300 group-hover:w-full"></span>
                        </a>
                        <a href="#categories" class="nav-link hover:text-gaming-neon transition-colors duration-300 px-3 py-2 rounded-md text-lg font-medium relative group">
                            Categories
                            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gaming-neon transition-all duration-300 group-hover:w-full"></span>
                        </a>
                        <a href="#about" class="nav-link hover:text-gaming-neon transition-colors duration-300 px-3 py-2 rounded-md text-lg font-medium relative group">
                            About
                            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gaming-neon transition-all duration-300 group-hover:w-full"></span>
                        </a>
                        <a href="#contact" class="nav-link hover:text-gaming-neon transition-colors duration-300 px-3 py-2 rounded-md text-lg font-medium relative group">
                            Contact
                            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gaming-neon transition-all duration-300 group-hover:w-full"></span>
                        </a>
                    </div>
                </div>

                <!-- Mobile Menu Button -->
                <div class="md:hidden">
                    <button id="mobile-menu-btn" class="text-gray-300 hover:text-gaming-neon focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="mobile-menu fixed top-0 right-0 h-full w-64 bg-gaming-surface border-l border-gaming-purple/30 md:hidden z-50 p-6">
            <button id="close-menu" class="absolute top-4 right-4 text-gray-400 hover:text-gaming-neon">
                <i class="fas fa-times text-2xl"></i>
            </button>
            <div class="mt-12 space-y-4">
                <a href="#home" class="block text-lg hover:text-gaming-neon transition-colors">Home</a>
                <a href="#games" class="block text-lg hover:text-gaming-neon transition-colors">Games</a>
                <a href="#categories" class="block text-lg hover:text-gaming-neon transition-colors">Categories</a>
                <a href="#about" class="block text-lg hover:text-gaming-neon transition-colors">About</a>
                <a href="#contact" class="block text-lg hover:text-gaming-neon transition-colors">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="relative min-h-screen flex items-center justify-center overflow-hidden pt-20">
        <!-- Background Effects -->
        <div class="absolute inset-0 bg-gradient-to-b from-gaming-purple/20 via-transparent to-gaming-dark"></div>
        <div class="absolute inset-0 bg-[url('data:image/svg+xml,%3Csvg%20width%3D%2260%22%20height%3D%2260%22%20viewBox%3D%220%200%2060%2060%22%20xmlns%3D%22http%3A//www.w3.org/2000/svg%22%3E%3Cg%20fill%3D%22none%22%20fill-rule%3D%22evenodd%22%3E%3Cg%20fill%3D%22%236d28d9%22%20fill-opacity%3D%220.1%22%3E%3Cpath%20d%3D%22M36%2034v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6%2034v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6%204V0H4v4H0v2h4v4h2V6h4V4H6z%22/%3E%3C/g%3E%3C/g%3E%3C/svg%3E')] opacity-20"></div>
        
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <div class="animate-slide-up">
                <h1 class="font-orbitron text-5xl md:text-7xl lg:text-8xl font-black mb-6 glitch" data-text="JK GAMING">
                    <span class="bg-gradient-to-r from-gaming-neon via-white to-gaming-purple bg-clip-text text-transparent">
                        JK GAMING
                    </span>
                </h1>
                <p class="text-xl md:text-2xl text-gray-400 mb-8 max-w-3xl mx-auto font-light tracking-wide">
                    Download the latest and greatest games. Experience gaming like never before with our premium collection.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                    <button onclick="document.getElementById('games').scrollIntoView({behavior: 'smooth'})" 
                            class="group relative px-8 py-4 bg-transparent border-2 border-gaming-neon text-gaming-neon font-orbitron font-bold text-lg rounded-full overflow-hidden transition-all duration-300 hover:text-gaming-dark">
                        <span class="absolute inset-0 w-full h-full bg-gaming-neon transform -translate-x-full group-hover:translate-x-0 transition-transform duration-300"></span>
                        <span class="relative flex items-center gap-2">
                            EXPLORE GAMES <i class="fas fa-arrow-right group-hover:translate-x-1 transition-transform"></i>
                        </span>
                    </button>
                    <button class="px-8 py-4 bg-gradient-to-r from-gaming-purple to-gaming-accent text-white font-orbitron font-bold text-lg rounded-full hover:shadow-[0_0_30px_rgba(109,40,217,0.5)] transition-all duration-300 transform hover:scale-105">
                        JOIN COMMUNITY
                    </button>
                </div>
            </div>

            <!-- Stats -->
            <div class="mt-16 grid grid-cols-2 md:grid-cols-4 gap-8 max-w-4xl mx-auto">
                <div class="text-center p-4 rounded-lg bg-gaming-surface/50 border border-gaming-purple/20 backdrop-blur-sm">
                    <div class="text-3xl font-orbitron font-bold text-gaming-neon">500+</div>
                    <div class="text-gray-400 text-sm mt-1">Games</div>
                </div>
                <div class="text-center p-4 rounded-lg bg-gaming-surface/50 border border-gaming-purple/20 backdrop-blur-sm">
                    <div class="text-3xl font-orbitron font-bold text-gaming-purple">1M+</div>
                    <div class="text-gray-400 text-sm mt-1">Downloads</div>
                </div>
                <div class="text-center p-4 rounded-lg bg-gaming-surface/50 border border-gaming-purple/20 backdrop-blur-sm">
                    <div class="text-3xl font-orbitron font-bold text-gaming-accent">50+</div>
                    <div class="text-gray-400 text-sm mt-1">Categories</div>
                </div>
                <div class="text-center p-4 rounded-lg bg-gaming-surface/50 border border-gaming-purple/20 backdrop-blur-sm">
                    <div class="text-3xl font-orbitron font-bold text-white">24/7</div>
                    <div class="text-gray-400 text-sm mt-1">Support</div>
                </div>
            </div>
        </div>

        <!-- Scroll Indicator -->
        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
            <i class="fas fa-chevron-down text-gaming-neon text-2xl"></i>
        </div>
    </section>

    <!-- Search & Filter Section -->
    <section id="categories" class="py-12 bg-gaming-surface/30 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row gap-6 items-center justify-between mb-8">
                <!-- Search Bar -->
                <div class="relative w-full md:w-96 group">
                    <input type="text" id="search-input" placeholder="Search games..." 
                           class="search-input w-full px-6 py-4 bg-gaming-dark border-2 border-gaming-purple/30 rounded-full text-white placeholder-gray-500 focus:outline-none focus:border-gaming-neon transition-all duration-300 pl-12">
                    <i class="fas fa-search absolute left-4 top-1/2 transform -translate-y-1/2 text-gray-500 group-focus-within:text-gaming-neon transition-colors"></i>
                </div>

                <!-- Category Filters -->
                <div class="flex flex-wrap gap-3 justify-center" id="category-filters">
                    <button class="category-btn active px-6 py-2 rounded-full border border-gaming-purple/50 text-gray-300 hover:border-gaming-neon hover:text-gaming-neon transition-all duration-300 font-medium" data-category="all">
                        All Games
                    </button>
                    <button class="category-btn px-6 py-2 rounded-full border border-gaming-purple/50 text-gray-300 hover:border-gaming-neon hover:text-gaming-neon transition-all duration-300 font-medium" data-category="action">
                        <i class="fas fa-fist-raised mr-2"></i>Action
                    </button>
                    <button class="category-btn px-6 py-2 rounded-full border border-gaming-purple/50 text-gray-300 hover:border-gaming-neon hover:text-gaming-neon transition-all duration-300 font-medium" data-category="racing">
                        <i class="fas fa-car mr-2"></i>Racing
                    </button>
                    <button class="category-btn px-6 py-2 rounded-full border border-gaming-purple/50 text-gray-300 hover:border-gaming-neon hover:text-gaming-neon transition-all duration-300 font-medium" data-category="shooting">
                        <i class="fas fa-crosshairs mr-2"></i>Shooting
                    </button>
                    <button class="category-btn px-6 py-2 rounded-full border border-gaming-purple/50 text-gray-300 hover:border-gaming-neon hover:text-gaming-neon transition-all duration-300 font-medium" data-category="adventure">
                        <i class="fas fa-compass mr-2"></i>Adventure
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Games Section -->
    <section id="games" class="py-16 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="font-orbitron text-4xl md:text-5xl font-bold mb-4">
                    <span class="bg-gradient-to-r from-gaming-neon to-gaming-purple bg-clip-text text-transparent">
                        Featured Games
                    </span>
                </h2>
                <p class="text-gray-400 text-lg">Discover your next favorite game</p>
            </div>

            <!-- Games Grid -->
            <div id="games-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                <!-- Games will be inserted here by JavaScript -->
            </div>

            <!-- No Results Message -->
            <div id="no-results" class="hidden text-center py-16">
                <i class="fas fa-search text-6xl text-gray-600 mb-4"></i>
                <h3 class="text-2xl font-orbitron text-gray-400 mb-2">No games found</h3>
                <p class="text-gray-500">Try adjusting your search or category filter</p>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-gaming-surface/20 relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-gaming-purple/10 to-gaming-neon/10"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <h2 class="font-orbitron text-4xl font-bold mb-6">
                        About <span class="text-gaming-neon">JK Gaming</span>
                    </h2>
                    <p class="text-gray-300 text-lg leading-relaxed">
                        JK Gaming is your ultimate destination for premium game downloads. We curate the best titles from around the world, ensuring every gamer finds their perfect match.
                    </p>
                    <p class="text-gray-300 text-lg leading-relaxed">
                        From high-octane racing to immersive RPGs, our platform offers secure, fast downloads with 24/7 support. Join millions of gamers who trust JK Gaming for their entertainment needs.
                    </p>
                    <div class="flex gap-4 pt-4">
                        <div class="flex items-center gap-2 text-gaming-neon">
                            <i class="fas fa-check-circle"></i>
                            <span>Secure Downloads</span>
                        </div>
                        <div class="flex items-center gap-2 text-gaming-neon">
                            <i class="fas fa-check-circle"></i>
                            <span>Fast Servers</span>
                        </div>
                        <div class="flex items-center gap-2 text-gaming-neon">
                            <i class="fas fa-check-circle"></i>
                            <span>Regular Updates</span>
                        </div>
                    </div>
                </div>
                <div class="relative">
                    <div class="absolute inset-0 bg-gradient-to-r from-gaming-neon to-gaming-purple rounded-2xl blur-2xl opacity-30 animate-pulse"></div>
                    <div class="relative bg-gaming-surface border border-gaming-purple/30 rounded-2xl p-8 backdrop-blur-sm">
                        <div class="grid grid-cols-2 gap-6">
                            <div class="text-center p-4 rounded-lg bg-gaming-dark/50">
                                <i class="fas fa-shield-alt text-3xl text-gaming-neon mb-2"></i>
                                <div class="font-bold text-lg">100% Safe</div>
                            </div>
                            <div class="text-center p-4 rounded-lg bg-gaming-dark/50">
                                <i class="fas fa-bolt text-3xl text-gaming-purple mb-2"></i>
                                <div class="font-bold text-lg">Fast Speed</div>
                            </div>
                            <div class="text-center p-4 rounded-lg bg-gaming-dark/50">
                                <i class="fas fa-headset text-3xl text-gaming-accent mb-2"></i>
                                <div class="font-bold text-lg">24/7 Support</div>
                            </div>
                            <div class="text-center p-4 rounded-lg bg-gaming-dark/50">
                                <i class="fas fa-sync text-3xl text-white mb-2"></i>
                                <div class="font-bold text-lg">Auto Updates</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 relative">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="font-orbitron text-4xl font-bold mb-4">
                    <span class="bg-gradient-to-r from-gaming-neon to-gaming-purple bg-clip-text text-transparent">
                        Get In Touch
                    </span>
                </h2>
                <p class="text-gray-400">Have questions? We're here to help!</p>
            </div>

            <form id="contact-form" class="space-y-6 bg-gaming-surface/30 p-8 rounded-2xl border border-gaming-purple/20 backdrop-blur-sm">
                <div class="grid md:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-gray-400 mb-2">Name</label>
                        <input type="text" required class="w-full px-4 py-3 bg-gaming-dark border border-gaming-purple/30 rounded-lg focus:outline-none focus:border-gaming-neon text-white transition-colors">
                    </div>
                    <div>
                        <label class="block text-gray-400 mb-2">Email</label>
                        <input type="email" required class="w-full px-4 py-3 bg-gaming-dark border border-gaming-purple/30 rounded-lg focus:outline-none focus:border-gaming-neon text-white transition-colors">
                    </div>
                </div>
                <div>
                    <label class="block text-gray-400 mb-2">Subject</label>
                    <input type="text" required class="w-full px-4 py-3 bg-gaming-dark border border-gaming-purple/30 rounded-lg focus:outline-none focus:border-gaming-neon text-white transition-colors">
                </div>
                <div>
                    <label class="block text-gray-400 mb-2">Message</label>
                    <textarea rows="5" required class="w-full px-4 py-3 bg-gaming-dark border border-gaming-purple/30 rounded-lg focus:outline-none focus:border-gaming-neon text-white transition-colors resize-none"></textarea>
                </div>
                <button type="submit" class="w-full py-4 bg-gradient-to-r from-gaming-purple to-gaming-neon text-white font-orbitron font-bold text-lg rounded-lg hover:shadow-[0_0_30px_rgba(0,243,255,0.4)] transition-all duration-300 transform hover:scale-[1.02] active:scale-95">
                    SEND MESSAGE <i class="fas fa-paper-plane ml-2"></i>
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gaming-dark border-t border-gaming-purple/30 pt-16 pb-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-4 gap-8 mb-12">
                <div class="col-span-2">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 rounded-lg bg-gradient-to-br from-gaming-purple to-gaming-neon flex items-center justify-center">
                            <i class="fas fa-gamepad text-xl text-white"></i>
                        </div>
                        <span class="font-orbitron text-xl font-bold text-white">JK GAMING</span>
                    </div>
                    <p class="text-gray-400 mb-6 max-w-md">
                        Your premier destination for game downloads. Experience gaming without limits.
                    </p>
                    <div class="flex gap-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-gaming-surface border border-gaming-purple/30 flex items-center justify-center text-gray-400 hover:text-gaming-neon hover:border-gaming-neon transition-all duration-300">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gaming-surface border border-gaming-purple/30 flex items-center justify-center text-gray-400 hover:text-gaming-neon hover:border-gaming-neon transition-all duration-300">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gaming-surface border border-gaming-purple/30 flex items-center justify-center text-gray-400 hover:text-gaming-neon hover:border-gaming-neon transition-all duration-300">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gaming-surface border border-gaming-purple/30 flex items-center justify-center text-gray-400 hover:text-gaming-neon hover:border-gaming-neon transition-all duration-300">
                            <i class="fab fa-discord"></i>
                        </a>
                    </div>
                </div>
                <div>
                    <h4 class="font-orbitron text-lg font-bold text-white mb-4">Quick Links</h4>
                    <ul class="space-y-2 text-gray-400">
                        <li><a href="#home" class="hover:text-gaming-neon transition-colors">Home</a></li>
                        <li><a href="#games" class="hover:text-gaming-neon transition-colors">Games</a></li>
                        <li><a href="#categories" class="hover:text-gaming-neon transition-colors">Categories</a></li>
                        <li><a href="#about" class="hover:text-gaming-neon transition-colors">About</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-orbitron text-lg font-bold text-white mb-4">Support</h4>
                    <ul class="space-y-2 text-gray-400">
                        <li><a href="#" class="hover:text-gaming-neon transition-colors">Help Center</a></li>
                        <li><a href="#" class="hover:text-gaming-neon transition-colors">Terms of Service</a></li>
                        <li><a href="#" class="hover:text-gaming-neon transition-colors">Privacy Policy</a></li>
                        <li><a href="#contact" class="hover:text-gaming-neon transition-colors">Contact Us</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gaming-purple/20 pt-8 text-center">
                <p class="text-gray-500 font-orbitron">
                    &copy; 2026 JK Gaming. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- Toast Notification -->
    <div id="toast" class="fixed bottom-4 right-4 transform translate-y-20 opacity-0 transition-all duration-300 z-50">
        <div class="bg-gaming-surface border border-gaming-neon text-white px-6 py-4 rounded-lg shadow-[0_0_20px_rgba(0,243,255,0.3)] flex items-center gap-3">
            <i class="fas fa-check-circle text-gaming-neon text-xl"></i>
            <span id="toast-message">Operation successful!</span>
        </div>
    </div>

    <script>
        // Games Data
        const games = [
            {
                id: 1,
                title: "Cyber Odyssey 2077",
                category: "action",
                description: "Navigate through a neon-lit cyberpunk metropolis in this action-packed RPG adventure.",
                image: "https://images.unsplash.com/photo-1542751371-adc38448a05e?w=400&h=300&fit=crop",
                size: "45 GB",
                rating: 4.8
            },
            {
                id: 2,
                title: "Velocity X",
                category: "racing",
                description: "High-speed racing with customizable supercars on tracks around the world.",
                image: "https://images.unsplash.com/photo-1511512578047-dfb367046420?w=400&h=300&fit=crop",
                size: "32 GB",
                rating: 4.6
            },
            {
                id: 3,
                title: "Tactical Ops: Elite",
                category: "shooting",
                description: "Team-based tactical shooter with realistic combat mechanics and strategy.",
                image: "https://images.unsplash.com/photo-1552820728-8b83bb6b2b0a?w=400&h=300&fit=crop",
                size: "28 GB",
                rating: 4.7
            },
            {
                id: 4,
                title: "Lost Realms",
                category: "adventure",
                description: "Explore ancient ruins and solve mysteries in this epic adventure game.",
                image: "https://images.unsplash.com/photo-1518709268805-4e9042af9f23?w=400&h=300&fit=crop",
                size: "38 GB",
                rating: 4.9
            },
            {
                id: 5,
                title: "Shadow Warrior",
                category: "action",
                description: "Master the art of stealth and combat in feudal Japan.",
                image: "https://images.unsplash.com/photo-1538481199705-c710c4e965fc?w=400&h=300&fit=crop",
                size: "25 GB",
                rating: 4.5
            },
            {
                id: 6,
                title: "Drift Kings",
                category: "racing",
                description: "Master the art of drifting in this arcade-style racing game.",
                image: "https://images.unsplash.com/photo-1568605117036-5fe5e7bab0b7?w=400&h=300&fit=crop",
                size: "15 GB",
                rating: 4.3
            },
            {
                id: 7,
                title: "Sniper Ghost",
                category: "shooting",
                description: "Long-range tactical shooting with realistic ballistics.",
                image: "https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=400&h=300&fit=crop",
                size: "42 GB",
                rating: 4.4
            },
            {
                id: 8,
                title: "Mystic Quest",
                category: "adventure",
                description: "Embark on a magical journey through enchanted forests and castles.",
                image: "https://images.unsplash.com/photo-1519669556878-63bdad8a1a49?w=400&h=300&fit=crop",
                size: "35 GB",
                rating: 4.7
            },
            {
                id: 9,
                title: "Combat Zone",
                category: "action",
                description: "Intense hand-to-hand combat and melee action.",
                image: "https://images.unsplash.com/photo-1493711662062-fa541f7f3d24?w=400&h=300&fit=crop",
                size: "22 GB",
                rating: 4.2
            },
            {
                id: 10,
                title: "Street Racer Pro",
                category: "racing",
                description: "Underground street racing with deep customization.",
                image: "https://images.unsplash.com/photo-1568605114967-8130f3a36994?w=400&h=300&fit=crop",
                size: "30 GB",
                rating: 4.5
            },
            {
                id: 11,
                title: "Battlefield Zero",
                category: "shooting",
                description: "Massive multiplayer battles in destructible environments.",
                image: "https://images.unsplash.com/photo-1509198397868-475647b2a1e5?w=400&h=300&fit=crop",
                size: "55 GB",
                rating: 4.6
            },
            {
                id: 12,
                title: "Pirate's Treasure",
                category: "adventure",
                description: "Sail the high seas and hunt for legendary treasures.",
                image: "https://images.unsplash.com/photo-1534447677768-be436bb09401?w=400&h=300&fit=crop",
                size: "40 GB",
                rating: 4.8
            }
        ];

        // DOM Elements
        const gamesGrid = document.getElementById('games-grid');
        const searchInput = document.getElementById('search-input');
        const categoryBtns = document.querySelectorAll('.category-btn');
        const noResults = document.getElementById('no-results');
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const closeMenuBtn = document.getElementById('close-menu');
        const loadingScreen = document.getElementById('loading-screen');
        const navbar = document.getElementById('navbar');

        let currentCategory = 'all';
        let searchTerm = '';

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            createParticles();
            renderGames();
            
            // Hide loading screen
            setTimeout(() => {
                loadingScreen.style.opacity = '0';
                setTimeout(() => {
                    loadingScreen.style.display = 'none';
                }, 500);
            }, 1500);
        });

        // Create Background Particles
        function createParticles() {
            const container = document.getElementById('particles');
            for (let i = 0; i < 50; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 10 + 's';
                particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
                container.appendChild(particle);
            }
        }

        // Render Games
        function renderGames() {
            const filtered = games.filter(game => {
                const matchesCategory = currentCategory === 'all' || game.category === currentCategory;
                const matchesSearch = game.title.toLowerCase().includes(searchTerm.toLowerCase()) ||
                                    game.description.toLowerCase().includes(searchTerm.toLowerCase());
                return matchesCategory && matchesSearch;
            });

            if (filtered.length === 0) {
                gamesGrid.innerHTML = '';
                noResults.classList.remove('hidden');
            } else {
                noResults.classList.add('hidden');
                gamesGrid.innerHTML = filtered.map(game => `
                    <div class="game-card bg-gaming-surface rounded-2xl overflow-hidden border border-gaming-purple/20 group relative">
                        <div class="relative overflow-hidden h-48">
                            <img src="${game.image}" alt="${game.title}" class="card-image w-full h-full object-cover transition-transform duration-500">
                            <div class="absolute inset-0 bg-gradient-to-t from-gaming-dark to-transparent opacity-60"></div>
                            <div class="absolute top-4 right-4 bg-gaming-dark/80 backdrop-blur-sm px-3 py-1 rounded-full border border-gaming-neon/30">
                                <i class="fas fa-star text-yellow-400 text-sm"></i>
                                <span class="text-sm font-bold ml-1">${game.rating}</span>
                            </div>
                            <div class="absolute bottom-4 left-4">
                                <span class="text-xs uppercase tracking-wider text-gaming-neon font-bold">${game.category}</span>
                            </div>
                        </div>
                        <div class="p-6">
                            <h3 class="font-orbitron text-xl font-bold text-white mb-2 group-hover:text-gaming-neon transition-colors">${game.title}</h3>
                            <p class="text-gray-400 text-sm mb-4 line-clamp-2">${game.description}</p>
                            <div class="flex items-center justify-between mb-4">
                                <span class="text-xs text-gray-500"><i class="fas fa-hdd mr-1"></i> ${game.size}</span>
                                <span class="text-xs text-gray-500"><i class="fas fa-download mr-1"></i> ${Math.floor(Math.random() * 500 + 100)}k</span>
                            </div>
                            <button onclick="downloadGame('${game.title}')" class="download-btn w-full py-3 bg-gaming-purple text-white font-bold rounded-lg transition-all duration-300 flex items-center justify-center gap-2 group-hover:shadow-lg">
                                <i class="fas fa-download"></i>
                                DOWNLOAD NOW
                            </button>
                        </div>
                    </div>
                `).join('');
            }
        }

        // Download Handler
        function downloadGame(title) {
            showToast(`Starting download: ${title}`);
            
            // Simulate download progress
            const btn = event.target.closest('button');
            const originalContent = btn.innerHTML;
            btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> DOWNLOADING...';
            btn.disabled = true;
            
            setTimeout(() => {
                btn.innerHTML = '<i class="fas fa-check"></i> INSTALLED';
                btn.classList.remove('bg-gaming-purple');
                btn.classList.add('bg-green-600');
                showToast(`${title} downloaded successfully!`);
                
                setTimeout(() => {
                    btn.innerHTML = originalContent;
                    btn.classList.add('bg-gaming-purple');
                    btn.classList.remove('bg-green-600');
                    btn.disabled = false;
                }, 3000);
            }, 2000);
        }

        // Toast Notification
        function showToast(message) {
            const toast = document.getElementById('toast');
            const toastMessage = document.getElementById('toast-message');
            toastMessage.textContent = message;
            toast.classList.remove('translate-y-20', 'opacity-0');
            
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3000);
        }

        // Search Handler
        searchInput.addEventListener('input', (e) => {
            searchTerm = e.target.value;
            renderGames();
        });

        // Category Filter Handler
        categoryBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                categoryBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                currentCategory = btn.dataset.category;
                renderGames();
            });
        });

        // Mobile Menu
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.add('active');
        });

        closeMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.remove('active');
        });

        // Close mobile menu when clicking on a link
        mobileMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.remove('active');
            });
        });

        // Navbar Scroll Effect
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('shadow-lg', 'shadow-gaming-purple/20');
            } else {
                navbar.classList.remove('shadow-lg', 'shadow-gaming-purple/20');
            }
        });

        // Smooth Scroll for Navigation Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Contact Form Handler
        document.getElementById('contact-form').addEventListener('submit', (e) => {
            e.preventDefault();
            showToast('Message sent successfully! We will contact you soon.');
            e.target.reset();
        });

        // Intersection Observer for Animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-slide-up');
                    entry.target.style.opacity = '1';
                }
            });
        }, observerOptions);

        // Observe game cards
        setTimeout(() => {
            document.querySelectorAll('.game-card').forEach(card => {
                card.style.opacity = '0';
                observer.observe(card);
            });
        }, 100);
    </script>
</body>
</html>
