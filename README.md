
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kunene Debate Society</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .hero-bg {
            background: linear-gradient(rgba(17, 24, 39, 0.9), rgba(17, 24, 39, 0.9)), url('https://placehold.co/1200x800/fef08a/ca8a04?text=Debate+in+Action');
            background-size: cover;
            background-position: center;
        }
        .cta-button {
            transition: all 0.3s ease;
        }
        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }
        .dark-input {
            background-color: #374151; /* bg-gray-700 */
            color: white;
            border-color: #4b5563; /* border-gray-600 */
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-200">

    <!-- Header & Navigation -->
    <header class="bg-gray-900 shadow-lg sticky top-0 z-50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-yellow-400">
                <i class="fas fa-gavel mr-2"></i>Kunene Debate Society
            </a>
            <div class="hidden md:flex space-x-6">
                <a href="#home" class="text-gray-300 hover:text-yellow-400 transition duration-300">Home</a>
                <a href="#about" class="text-gray-300 hover:text-yellow-400 transition duration-300">About Us</a>
                <a href="#events" class="text-gray-300 hover:text-yellow-400 transition duration-300">Events</a>
                <a href="#join-us" class="text-gray-300 hover:text-yellow-400 transition duration-300">Join Us</a>
            </div>
            <button class="md:hidden" id="mobile-menu-button">
                <i class="fas fa-bars text-2xl text-gray-300"></i>
            </button>
        </nav>
        <!-- Mobile Menu -->
        <div class="md:hidden hidden bg-gray-800" id="mobile-menu">
            <a href="#home" class="block py-2 px-4 text-sm text-gray-300 hover:bg-gray-700">Home</a>
            <a href="#about" class="block py-2 px-4 text-sm text-gray-300 hover:bg-gray-700">About Us</a>
            <a href="#events" class="block py-2 px-4 text-sm text-gray-300 hover:bg-gray-700">Events</a>
            <a href="#join-us" class="block py-2 px-4 text-sm text-gray-300 hover:bg-gray-700">Join Us</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero-bg py-24 md:py-32">
        <div class="container mx-auto px-6 text-center">
            <h1 class="text-4xl md:text-6xl font-bold text-white leading-tight mb-4">Sharpen Your Mind, Find Your Voice.</h1>
            <p class="text-lg md:text-xl text-gray-300 mb-8 max-w-3xl mx-auto">Join the Kunene Debate Society to engage in meaningful discourse, develop critical thinking, and become a confident public speaker.</p>
            <a href="#join-us" class="bg-yellow-500 text-gray-900 font-bold py-3 px-8 rounded-full text-lg cta-button">Become a Member</a>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="py-20 bg-gray-800">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center mb-12 text-white">Who We Are</h2>
            <div class="flex flex-col md:flex-row items-center gap-12">
                <div class="md:w-1/2">
                    <img src="https://placehold.co/600x400/1f2937/ca8a04?text=Our+Mission" alt="Group of debaters" class="rounded-lg shadow-lg w-full">
                </div>
                <div class="md:w-1/2">
                    <h3 class="text-2xl font-semibold mb-4 text-yellow-400">Our Mission</h3>
                    <p class="text-gray-300 mb-4">To foster a vibrant community of critical thinkers who can articulate their ideas persuasively and respectfully. We provide a platform for students and community members to explore complex issues from multiple perspectives.</p>
                    <h3 class="text-2xl font-semibold mb-4 text-yellow-400">Our Vision</h3>
                    <p class="text-gray-300">We envision a future where informed and reasoned debate is a cornerstone of our community, empowering individuals to become active and engaged citizens who can drive positive change.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Upcoming Events Section -->
    <section id="events" class="py-20">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center mb-12 text-white">Upcoming Events</h2>
            <div class="text-center max-w-2xl mx-auto">
                <div class="bg-gray-800 rounded-lg shadow-lg p-8">
                    <i class="fas fa-calendar-alt text-5xl text-yellow-400 mb-4"></i>
                    <h3 class="text-2xl font-semibold text-white mb-4">Stay Tuned!</h3>
                    <p class="text-gray-300 mb-6 text-lg">
                        Our event calendar for the upcoming season is currently being finalized. Details about our next debate, workshop, and championship will be announced very soon.
                    </p>
                    <p class="text-gray-300 mb-8">
                         The best way to get instant notifications is by joining our community.
                    </p>
                    <a href="#join-us" class="bg-yellow-500 text-gray-900 font-bold py-3 px-8 rounded-full text-lg cta-button">Join for Updates</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Join Us Section -->
    <section id="join-us" class="py-20 bg-gray-800">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center mb-12 text-white">Become a Part of Our Society</h2>
            <div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-12 items-start">

                <!-- Column 1: Join WhatsApp & Contact Info -->
                <div class="space-y-8">
                    <div class="bg-gray-700 p-6 rounded-lg shadow-lg text-center">
                        <i class="fab fa-whatsapp text-5xl text-green-500 mb-4"></i>
                        <h3 class="text-xl font-bold mb-2 text-white">Join our WhatsApp Group</h3>
                        <p class="text-gray-300 mb-4">Get the latest updates on events, practice sessions, and engage in daily discussions with fellow members.</p>
                        <!-- ACTION REQUIRED: Replace '#' with your WhatsApp group invite link -->
                        <a href="#" class="bg-green-500 text-white font-bold py-3 px-6 rounded-full text-md cta-button inline-block">Join via Link</a>
                        <p class="text-gray-400 mt-4 text-sm">Or contact <a href="tel:0817570683" class="font-medium text-yellow-400 hover:underline">081 757 0683</a> to be added.</p>
                    </div>

                    <div class="bg-gray-700 p-6 rounded-lg shadow-lg text-center">
                        <h3 class="text-xl font-semibold mb-4 text-white">Contact Us Directly</h3>
                        <div class="flex flex-col justify-center items-center space-y-4">
                            <p class="text-gray-300">
                                <i class="fas fa-phone mr-2 text-yellow-400"></i>
                                <a href="tel:0817570683" class="hover:text-yellow-400">081 757 0683</a>
                            </p>
                            <p class="text-gray-300">
                                <i class="fas fa-envelope mr-2 text-yellow-400"></i>
                                <a href="mailto:tuatirohange@gmail.com" class="hover:text-yellow-400">tuatirohange@gmail.com</a>
                            </p>
                        </div>
                    </div>
                </div>

                <!-- Column 2: Membership Application Form -->
                <div class="bg-gray-700 p-8 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-semibold mb-6 text-center text-white">Apply for Membership</h3>
                     <!-- 
                        ACTION REQUIRED: 
                        1. Go to https://formspree.io/ and create a free account.
                        2. Create a new form and point it to your email address.
                        3. Replace the URL below with your unique Formspree form URL.
                    -->
                    <form action="https://formspree.io/f/YOUR_UNIQUE_FORM_ID" method="POST">
                        <div class="grid grid-cols-1 gap-6 mb-6">
                            <div>
                                <label for="name" class="block text-gray-300 font-medium mb-2">Full Name</label>
                                <input type="text" id="name" name="name" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-yellow-400 dark-input" required>
                            </div>
                            <div>
                                <label for="email" class="block text-gray-300 font-medium mb-2">Email Address</label>
                                <input type="email" id="email" name="email" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-yellow-400 dark-input" required>
                            </div>
                        </div>
                        <div class="mb-6">
                            <label for="reason" class="block text-gray-300 font-medium mb-2">Why do you want to join?</label>
                            <textarea id="reason" name="reason" rows="5" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-yellow-400 dark-input" placeholder="Tell us a bit about your interest in debate..." required></textarea>
                        </div>
                        <div class="text-center">
                            <button type="submit" class="bg-yellow-500 text-gray-900 font-bold py-3 px-8 rounded-full text-lg cta-button">Submit Application</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-10">
        <div class="container mx-auto px-6 text-center">
            <div class="flex justify-center space-x-6 mb-4">
                <a href="#" class="text-gray-400 hover:text-white transition duration-300"><i class="fab fa-facebook-f text-2xl"></i></a>
                <a href="#" class="text-gray-400 hover:text-white transition duration-300"><i class="fab fa-twitter text-2xl"></i></a>
                <a href="https://www.instagram.com/kunene_debate_society?igsh=MXY5MXF4aFleno2Mg==" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-white transition duration-300"><i class="fab fa-instagram text-2xl"></i></a>
            </div>
            <p>&copy; 2025 Kunene Debate Society. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
    </script>

</body>
</html>


