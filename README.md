<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kunene Debate Society</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        /* Custom styles for radio buttons to match the theme */
        .form-radio {
            -webkit-appearance: none;
            appearance: none;
            background-color: #374151; /* gray-700 */
            border: 2px solid #4B5563; /* gray-600 */
            width: 1.25em;
            height: 1.25em;
            border-radius: 50%;
            display: grid;
            place-content: center;
        }
        .form-radio::before {
            content: "";
            width: 0.65em;
            height: 0.65em;
            border-radius: 50%;
            transform: scale(0);
            transition: 120ms transform ease-in-out;
            box-shadow: inset 1em 1em #FBBF24; /* yellow-400 */
        }
        .form-radio:checked::before {
            transform: scale(1);
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-200">

    <!-- Header -->
    <header id="home" class="bg-black text-white py-4 shadow-md">
        <div class="max-w-5xl mx-auto px-4 flex justify-center items-center gap-4">
            <h1 class="text-3xl md:text-5xl font-bold text-center">Kunene <span class="text-yellow-400">Debate</span> Society</h1>
        </div>
    </header>

    <!-- Navigation Bar -->
    <nav class="bg-gray-950/80 backdrop-blur-md sticky top-0 z-50 shadow-sm">
        <div class="max-w-5xl mx-auto px-4">
            <div class="flex justify-center items-center h-16">
                <div class="flex flex-wrap justify-center space-x-4 md:space-x-6">
                    <a href="#home" class="text-gray-300 hover:text-yellow-400 transition-colors duration-300 font-medium">Home</a>
                    <a href="#our-team" id="view-team-btn" class="text-gray-300 hover:text-yellow-400 transition-colors duration-300 font-medium cursor-pointer">Our Team</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="max-w-5xl mx-auto p-4 md:p-8 space-y-12">

        <!-- Home Section -->
        <section class="text-center py-16">
            <h2 class="text-3xl font-bold text-yellow-400 mb-4">Welcome!</h2>
            <p class="text-lg text-gray-300 max-w-2xl mx-auto">
                We are the Kunene Debate Society. Join us to improve your debating skills, engage in critical discussions, and connect with fellow thinkers!
            </p>
        </section>

        <!-- About Us Section -->
        <section id="about" class="bg-gray-800 p-8 rounded-lg shadow-lg">
            <h2 class="text-3xl font-bold text-center text-yellow-400 mb-6">About Us</h2>
            <p class="text-gray-300 leading-relaxed text-center max-w-3xl mx-auto">
                Founded on the principles of critical thinking and articulate expression, the Kunene Debate Society provides a vibrant platform for students and community members to hone their public speaking, argumentation, and analytical skills. We believe that healthy debate fosters intellectual growth and is essential for a thriving community. Our society is open to all, from beginners to seasoned debaters.
            </p>
        </section>
        
        <!-- Gemini AI Debate Hub Section -->
        <section id="debate-hub" class="bg-gray-800 p-8 rounded-lg shadow-lg">
            <h2 class="text-3xl font-bold text-center text-yellow-400 mb-8">Debate Hub ✨</h2>
            <p class="text-center text-gray-400 mb-10 max-w-2xl mx-auto">
                Stuck for ideas? Use our AI-powered tools to suggest debate topics and help you build compelling arguments for your case.
            </p>

            <!-- Feature 1: Topic Suggester -->
            <div class="mb-12">
                <h3 class="text-2xl font-semibold text-center text-white mb-4">Topic Suggester</h3>
                <div class="text-center">
                    <button id="suggest-topics-btn" class="bg-yellow-400 text-black font-bold py-2 px-6 rounded-lg hover:bg-yellow-500 transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed">
                        ✨ Suggest New Topics
                    </button>
                </div>
                <div id="topics-output" class="mt-6 bg-gray-900 p-6 rounded-lg border border-gray-700 min-h-[100px] text-gray-300 whitespace-pre-wrap">
                    Click the button to generate debate topics...
                </div>
            </div>

            <!-- Feature 2: Argument Architect -->
            <div>
                <h3 class="text-2xl font-semibold text-center text-white mb-4">Argument Architect</h3>
                <div class="max-w-xl mx-auto bg-gray-900 p-6 rounded-lg border border-gray-700">
                    <div class="space-y-4">
                        <div>
                            <label for="debate-topic" class="block text-sm font-medium text-gray-300 mb-1">Debate Topic:</label>
                            <input type="text" id="debate-topic" class="w-full bg-gray-700 border border-gray-600 rounded-md py-2 px-3 text-white focus:outline-none focus:ring-2 focus:ring-yellow-400" placeholder="e.g., Should social media be banned for children?">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-300 mb-1">Your Stance:</label>
                            <div class="flex gap-4">
                                <label class="flex items-center">
                                    <input type="radio" name="stance" value="For" class="form-radio" checked>
                                    <span class="ml-2 text-white">For / Agree</span>
                                </label>
                                <label class="flex items-center">
                                    <input type="radio" name="stance" value="Against" class="form-radio">
                                    <span class="ml-2 text-white">Against / Disagree</span>
                                </label>
                            </div>
                        </div>
                        <div class="text-center pt-2">
                            <button id="build-arguments-btn" class="bg-yellow-400 text-black font-bold py-2 px-6 rounded-lg hover:bg-yellow-500 transition-all duration-300 w-full disabled:opacity-50 disabled:cursor-not-allowed">
                                ✨ Build My Arguments
                            </button>
                        </div>
                    </div>
                </div>
                <div id="arguments-output" class="mt-6 bg-gray-900 p-6 rounded-lg border border-gray-700 min-h-[200px] text-gray-300 whitespace-pre-wrap">
                    Your generated arguments will appear here...
                </div>
            </div>
        </section>

        <!-- Our Team Section (Initially Hidden) -->
        <section id="our-team" class="bg-gray-900 p-8 rounded-lg shadow-lg hidden">
            <h2 class="text-3xl font-bold text-center text-yellow-400 mb-12">Our Team</h2>

            <!-- Presidency -->
            <h3 class="text-2xl font-semibold text-yellow-300 mb-6 text-center border-b border-gray-700 pb-2">Presidency</h3>
            <div class="max-w-2xl mx-auto grid grid-cols-1 sm:grid-cols-2 gap-8 mb-12">
                <!-- Team Member 1 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Mr. Katjitoorerue Kavari" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Mr. Katjitoorerue Kavari</h3>
                    <p class="text-yellow-400">KDS President</p>
                </div>
                <!-- Team Member 2 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Adv. Divine Mupya" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Adv. Divine Mupya</h3>
                    <p class="text-yellow-400">KDS Vice-President</p>
                </div>
            </div>

            <!-- Secretariat -->
            <h3 class="text-2xl font-semibold text-yellow-300 mb-6 text-center border-b border-gray-700 pb-2">Secretariat</h3>
            <div class="max-w-2xl mx-auto grid grid-cols-1 sm:grid-cols-2 gap-8 mb-12">
                <!-- Team Member 3 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Ms. Repeza Tjiundunda" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Ms. Repeza Tjiundunda</h3>
                    <p class="text-yellow-400">KDS Secretary</p>
                </div>
                <!-- Team Member 4 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Mr. Bet-Sean Maharipo" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Mr. Bet-Sean Maharipo</h3>
                    <p class="text-yellow-400">KDS Vice-Secretary</p>
                </div>
            </div>

            <!-- Treasury -->
            <h3 class="text-2xl font-semibold text-yellow-300 mb-6 text-center border-b border-gray-700 pb-2">Treasury</h3>
            <div class="max-w-2xl mx-auto grid grid-cols-1 sm:grid-cols-2 gap-8 mb-12">
                <!-- Team Member 5 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Mr. Uatirohange Tjiumbua" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Mr. Uatirohange Tjiumbua</h3>
                    <p class="text-yellow-400">KDS Treasurer</p>
                </div>
                <!-- Team Member 6 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Ms. Kuzaha K. L. Mutirua" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Ms. Kuzaha K. L. Mutirua</h3>
                    <p class="text-yellow-400">KDS Vice-Treasurer</p>
                </div>
            </div>

            <!-- Communications -->
            <h3 class="text-2xl font-semibold text-yellow-300 mb-6 text-center border-b border-gray-700 pb-2">Communications</h3>
            <div class="max-w-2xl mx-auto grid grid-cols-1 sm:grid-cols-2 gap-8 mb-12">
                <!-- Team Member 7 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Mr. Ndjamba Mutjavikua" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Mr. Ndjamba Mutjavikua</h3>
                    <p class="text-yellow-400">KDS Spokesperson</p>
                </div>
                <!-- Team Member 8 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Mr. Tjitjekura Kavetu" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Mr. Tjitjekura Kavetu</h3>
                    <p class="text-yellow-400">KDS Publicity Coordinator</p>
                </div>
            </div>

            <!-- Events -->
            <h3 class="text-2xl font-semibold text-yellow-300 mb-6 text-center border-b border-gray-700 pb-2">Events</h3>
            <div class="max-w-4xl mx-auto grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
                 <!-- Team Member 9 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Mr. Kaitike Katjimuine" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Mr. Kaitike Katjimuine</h3>
                    <p class="text-yellow-400">KDS Events Coordinator</p>
                </div>
                 <!-- Team Member 10 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Ms. Sonia Jeremiah" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Ms. Sonia Jeremiah</h3>
                    <p class="text-yellow-400">Director of Spelling Bee</p>
                </div>
                 <!-- Team Member 11 -->
                <div class="text-center bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-md">
                    <img src="https://placehold.co/400x400/1F2937/FBBF24?text=KDS" alt="Photo of Mr. Kapuvitua Mbinge" class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-gray-600">
                    <h3 class="text-xl font-bold text-white">Mr. Kapuvitua Mbinge</h3>
                    <p class="text-yellow-400">KDS Events Coordinator</p>
                </div>
            </div>
        </section>

        <!-- Events Section -->
        <section id="events" class="bg-gray-800 p-8 rounded-lg shadow-lg">
            <h2 class="text-3xl font-bold text-center text-yellow-400 mb-8">Our Events</h2>
            <div class="max-w-2xl mx-auto grid md:grid-cols-2 gap-6">
                <div class="bg-gray-900 p-6 rounded-lg shadow-sm border-l-4 border-yellow-400">
                    <h3 class="font-semibold text-lg mb-2 text-white">Public Debates</h3>
                    <p class="text-gray-400">Engage with thought-provoking topics and watch skilled debaters in action.</p>
                </div>
                 <div class="bg-gray-900 p-6 rounded-lg shadow-sm border-l-4 border-yellow-400">
                    <h3 class="font-semibold text-lg mb-2 text-white">Skill-Building Workshops</h3>
                    <p class="text-gray-400">Join our sessions on public speaking, argumentation, and critical thinking.</p>
                </div>
                 <div class="bg-gray-900 p-6 rounded-lg shadow-sm border-l-4 border-yellow-400">
                    <h3 class="font-semibold text-lg mb-2 text-white">Guest Speaker Sessions</h3>
                    <p class="text-gray-400">Learn from experts in various fields as they share their insights and experiences.</p>
                </div>
                 <div class="bg-gray-900 p-6 rounded-lg shadow-sm border-l-4 border-yellow-400">
                    <h3 class="font-semibold text-lg mb-2 text-white">Internal Tournaments</h3>
                    <p class="text-gray-400">Challenge yourself and compete with fellow members in a friendly environment.</p>
                </div>
            </div>
        </section>
        
        <!-- Past Activities Section -->
        <section id="past-activities" class="bg-gray-800 p-8 rounded-lg shadow-lg">
            <h2 class="text-3xl font-bold text-center text-yellow-400 mb-6">Past Activities</h2>
            <div class="max-w-3xl mx-auto text-center">
                <div class="bg-gray-900 p-6 rounded-lg shadow-sm border border-gray-700">
                    <h3 class="font-semibold text-xl mb-4 text-white">Annual Schools Debate Competition</h3>
                    <p class="text-gray-400">
                        A highlight of our calendar, this competition brings together the brightest young minds from schools across the region to compete, learn, and grow.
                    </p>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="bg-gray-800 p-8 rounded-lg shadow-lg">
            <h2 class="text-3xl font-bold text-center text-yellow-400 mb-6">Contact Us</h2>
            <p class="text-center text-gray-400 mb-8">Have a question or want to get involved? Here's how you can reach us.</p>
            
            <div class="max-w-lg mx-auto text-center mb-10">
                <div class="bg-gray-900 p-6 rounded-lg border border-gray-700 space-y-4">
                     <div class="flex items-center justify-center gap-3">
                         <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path></svg>
                        <p class="text-yellow-400">081 757 0683</p>
                    </div>
                     <div class="flex items-center justify-center gap-3">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                           <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                        </svg>
                        <p class="text-gray-300">Mr. Tjiumbua (Treasurer)</p>
                    </div>
                    <div class="flex items-center justify-center gap-3">
                         <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line></svg>
                        <a href="https://www.instagram.com/KuneneDebate" target="_blank" rel="noopener noreferrer" class="text-yellow-400 hover:underline">@KuneneDebate (Instagram)</a>
                    </div>
                    <div class="flex items-center justify-center gap-3">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-400" viewBox="0 0 24 24" fill="currentColor"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.487 5.235 3.487 8.413C24 18.661 18.664 24 .107 24h-.05.002zM11.953 2.149c-5.464.001-9.908 4.448-9.908 9.914a9.934 9.934 0 0 0 1.513 5.396L1.69 22l6.23-1.648a9.933 9.933 0 0 0 5.215 1.556c5.463 0 9.908-4.448 9.908-9.914 0-5.463-4.446-9.908-9.908-9.908zm4.722 14.353-1.225-1.15c-.171-.16-.4-.251-.629-.251-.23 0-.46.091-.63.252l-.462.438c-.407.386-1.039.318-1.357-.145l-2.454-3.56-1.138-1.657c-.206-.299-.555-.472-.924-.472-.05 0-.1.003-.15.009l-.499.098c-.463.092-.767.53-.641.981l.732 2.767c.189.713.626 1.343 1.258 1.765l1.66 1.134c.632.431 1.422.655 2.227.655.937 0 1.838-.453 2.502-1.368l.19-.265c.23-.32.613-.51 1.018-.492l1.32.067c.473.023.822-.387.693-.846z"></path></svg>
                        <a href="https://wa.me/264817570683" target="_blank" rel="noopener noreferrer" class="text-yellow-400 hover:underline">Chat on WhatsApp</a>
                    </div>
                </div>
            </div>

        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-black text-white text-center py-6 mt-12">
        <p>&copy; 2024 Kunene Debate Society</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const viewTeamBtn = document.getElementById('view-team-btn');
            const teamSection = document.getElementById('our-team');
            const homeBtn = document.querySelector('a[href="#home"]');
            const mainSections = document.querySelectorAll('main > section');
            let isTeamViewActive = false;

            function exitTeamView() {
                mainSections.forEach(section => {
                    section.classList.remove('hidden');
                });
                teamSection.classList.add('hidden');
                viewTeamBtn.innerHTML = "Our Team"; // Changed to innerHTML for arrow
                document.getElementById('about').scrollIntoView({ behavior: 'smooth' });
                isTeamViewActive = false;
            }

            function enterTeamView() {
                mainSections.forEach(section => {
                    if (section.id !== 'our-team') {
                        section.classList.add('hidden');
                    }
                });
                teamSection.classList.remove('hidden');
                viewTeamBtn.innerHTML = `<svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 19l-7-7m0 0l7-7m-7 7h18" /></svg>`;
                teamSection.scrollIntoView({ behavior: 'smooth' });
                isTeamViewActive = true;
            }

            if (viewTeamBtn && teamSection && homeBtn) {
                viewTeamBtn.addEventListener('click', (event) => {
                    event.preventDefault();
                    if (isTeamViewActive) {
                        exitTeamView();
                    } else {
                        enterTeamView();
                    }
                });

                homeBtn.addEventListener('click', (event) => {
                    if (isTeamViewActive) {
                        event.preventDefault(); 
                        exitTeamView();
                    }
                });
            }

            // Gemini API Features
            const suggestTopicsBtn = document.getElementById('suggest-topics-btn');
            const topicsOutput = document.getElementById('topics-output');
            const buildArgumentsBtn = document.getElementById('build-arguments-btn');
            const argumentsOutput = document.getElementById('arguments-output');
            const debateTopicInput = document.getElementById('debate-topic');

            const apiKey = ""; // API key will be provided by the environment
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;

            async function callGemini(payload) {
                let response;
                let delay = 1000;
                for (let i = 0; i < 5; i++) {
                    try {
                        response = await fetch(apiUrl, {
                            method: 'POST',
                            headers: { 'Content-Type': 'application/json' },
                            body: JSON.stringify(payload)
                        });

                        if (response.ok) {
                            const result = await response.json();
                            const candidate = result.candidates?.[0];
                            if (candidate && candidate.content?.parts?.[0]?.text) {
                                return candidate.content.parts[0].text;
                            }
                        }
                    } catch (error) {
                        console.error("Fetch error:", error);
                    }
                    await new Promise(resolve => setTimeout(resolve, delay));
                    delay *= 2;
                }
                throw new Error("Failed to get a valid response from the API after several retries.");
            }

            if (suggestTopicsBtn) {
                suggestTopicsBtn.addEventListener('click', async () => {
                    topicsOutput.textContent = 'Generating topics...';
                    suggestTopicsBtn.disabled = true;

                    const userQuery = "Generate a list of 5 interesting and controversial debate topics suitable for a university-level debate society. The topics should cover a range of subjects like technology, ethics, politics, and social issues. Present them as a numbered list with just the topic, no extra descriptions.";
                    const payload = { contents: [{ parts: [{ text: userQuery }] }] };

                    try {
                        const resultText = await callGemini(payload);
                        topicsOutput.textContent = resultText;
                    } catch (error) {
                        console.error('Error generating topics:', error);
                        topicsOutput.textContent = 'Sorry, I couldn\'t generate topics right now. Please try again later.';
                    } finally {
                        suggestTopicsBtn.disabled = false;
                    }
                });
            }

            if (buildArgumentsBtn) {
                buildArgumentsBtn.addEventListener('click', async () => {
                    const topic = debateTopicInput.value;
                    const stance = document.querySelector('input[name="stance"]:checked').value;

                    if (!topic.trim()) {
                        argumentsOutput.textContent = 'Please enter a debate topic first.';
                        return;
                    }

                    argumentsOutput.textContent = `Building arguments for the stance "${stance}" on the topic "${topic}"...`;
                    buildArgumentsBtn.disabled = true;

                    const systemPrompt = "You are an expert debate coach. Your task is to help a student build a strong, well-structured case for a debate. Provide three distinct arguments to support their given stance on a topic. For each argument, provide a clear claim (as a bolded heading), a brief explanation or reasoning (2-3 sentences), and a bullet point list of suggestions for what kind of evidence they should look for to support it. Do not invent statistics or facts. Format the output clearly using Markdown.";
                    const userQuery = `Debate Topic: "${topic}". My stance is: "${stance}". Please build my arguments.`;

                    const payload = {
                        contents: [{ parts: [{ text: userQuery }] }],
                        systemInstruction: { parts: [{ text: systemPrompt }] }
                    };

                    try {
                        const resultText = await callGemini(payload);
                        argumentsOutput.textContent = resultText;
                    } catch (error) {
                        console.error('Error building arguments:', error);
                        argumentsOutput.textContent = 'Sorry, I couldn\'t build arguments right now. Please try again later.';
                    } finally {
                        buildArgumentsBtn.disabled = false;
                    }
                });
            }
        });
    </script>

</body>
</html>



