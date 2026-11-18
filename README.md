# MD-SHAHIN-ALAM
<!DOCTYPE html>
<html lang="bn" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MD SHAHIN ALAM | Portfolio & Curriculum Vitae</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Inter & Hind Siliguri for crisp Bengali + English typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome for Crisp Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'Hind Siliguri', 'sans-serif'],
                    },
                    colors: {
                        navy: {
                            800: '#0f172a',
                            900: '#090d16',
                        },
                        army: {
                            600: '#15803d',
                            700: '#166534',
                            800: '#14532d',
                        },
                        gold: {
                            400: '#fbbf24',
                            500: '#f59e0b',
                            600: '#d97706',
                        }
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Print Styles for Clean CV Export */
        @media print {
            .no-print {
                display: none !important;
            }
            body {
                background: white !important;
                color: black !important;
                font-size: 12px !important;
            }
            .print-shadow-none {
                box-shadow: none !important;
                border: 1px solid #e2e8f0 !important;
            }
            .tab-content {
                display: block !important;
                opacity: 1 !important;
                margin-bottom: 1.5rem !important;
            }
        }

        /* Subtle Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f5f9;
        }
        .dark ::-webkit-scrollbar-track {
            background: #0f172a;
        }
        ::-webkit-scrollbar-thumb {
            background: #94a3b8;
            border-radius: 9999px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #64748b;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-navy-900 dark:text-slate-100 transition-colors duration-300 antialiased selection:bg-emerald-600 selection:text-white">

    <!-- Toast Notification Box (Replaces alert()) -->
    <div id="toast-box" class="fixed bottom-5 right-5 z-50 transform translate-y-24 opacity-0 transition-all duration-300 pointer-events-none no-print">
        <div class="bg-slate-900 dark:bg-emerald-700 text-white px-5 py-3 rounded-xl shadow-2xl flex items-center gap-3 border border-slate-700 dark:border-emerald-500">
            <i class="fa-solid fa-circle-check text-amber-400 text-lg"></i>
            <span id="toast-message" class="text-sm font-medium">Copied to clipboard!</span>
        </div>
    </div>

    <!-- Sticky Navigation Bar -->
    <header class="sticky top-0 z-40 bg-white/90 dark:bg-navy-800/90 backdrop-blur-md border-b border-slate-200 dark:border-slate-800 transition-colors no-print">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Brand / Logo -->
                <a href="#top" class="flex items-center gap-2.5 group">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-emerald-700 to-slate-900 flex items-center justify-center text-amber-400 font-extrabold text-lg shadow-md group-hover:scale-105 transition-transform">
                        SA
                    </div>
                    <div>
                        <span class="font-bold text-base sm:text-lg tracking-tight text-slate-900 dark:text-white block leading-none">MD SHAHIN ALAM</span>
                        <span class="text-[11px] font-medium text-emerald-700 dark:text-emerald-400 tracking-wider uppercase" data-i18n="nav_sub">L/Cpl (Retd) • Bangladesh Army</span>
                    </div>
                </a>

                <!-- Desktop Navigation Links -->
                <nav class="hidden lg:flex items-center gap-6 text-sm font-medium text-slate-600 dark:text-slate-300">
                    <a href="#about" class="hover:text-emerald-700 dark:hover:text-emerald-400 transition-colors" data-i18n="nav_about">পরিচিতি</a>
                    <a href="#achievements" class="hover:text-emerald-700 dark:hover:text-emerald-400 transition-colors" data-i18n="nav_medals">৪২টি পদক</a>
                    <a href="#experience" class="hover:text-emerald-700 dark:hover:text-emerald-400 transition-colors" data-i18n="nav_exp">কর্মঅভিজ্ঞতা</a>
                    <a href="#military" class="hover:text-emerald-700 dark:hover:text-emerald-400 transition-colors" data-i18n="nav_military">সামরিক সেবা</a>
                    <a href="#education" class="hover:text-emerald-700 dark:hover:text-emerald-400 transition-colors" data-i18n="nav_edu">শিক্ষা</a>
                    <a href="#contact" class="hover:text-emerald-700 dark:hover:text-emerald-400 transition-colors" data-i18n="nav_contact">যোগাযোগ</a>
                </nav>

                <!-- Action Controls: Language Toggle, Theme Toggle, Print CV -->
                <div class="flex items-center gap-2">
                    <!-- Bilingual Toggle Button -->
                    <button id="lang-toggle" onclick="toggleLanguage()" class="px-3 py-1.5 rounded-xl text-xs font-semibold bg-emerald-50 text-emerald-800 border border-emerald-200 hover:bg-emerald-100 dark:bg-emerald-950/60 dark:text-emerald-300 dark:border-emerald-800 transition-all flex items-center gap-1.5" title="Switch Language">
                        <i class="fa-solid fa-language text-sm"></i>
                        <span id="lang-label">English</span>
                    </button>

                    <!-- Dark/Light Mode Toggle -->
                    <button id="theme-toggle" onclick="toggleTheme()" class="p-2 rounded-xl bg-slate-100 text-slate-700 hover:bg-slate-200 dark:bg-slate-800 dark:text-amber-400 dark:hover:bg-slate-700 transition-all" title="Toggle Dark/Light Mode">
                        <i id="theme-icon" class="fa-solid fa-moon"></i>
                    </button>

                    <!-- Print / Save PDF Button -->
                    <button onclick="window.print()" class="hidden sm:flex items-center gap-1.5 px-3.5 py-1.5 rounded-xl text-xs font-semibold bg-slate-900 text-white hover:bg-slate-800 dark:bg-amber-500 dark:text-slate-950 dark:hover:bg-amber-400 shadow-sm transition-all">
                        <i class="fa-solid fa-print"></i>
                        <span data-i18n="btn_print">প্রিন্ট / PDF</span>
                    </button>

                    <!-- Mobile Menu Button -->
                    <button onclick="toggleMobileMenu()" class="lg:hidden p-2 rounded-xl bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-200">
                        <i class="fa-solid fa-bars"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Dropdown Navigation -->
        <div id="mobile-menu" class="hidden lg:hidden bg-white dark:bg-navy-800 border-b border-slate-200 dark:border-slate-700 px-4 pt-2 pb-4 space-y-2">
            <a href="#about" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-sm font-medium hover:bg-slate-100 dark:hover:bg-slate-700" data-i18n="nav_about">পরিচিতি</a>
            <a href="#achievements" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-sm font-medium hover:bg-slate-100 dark:hover:bg-slate-700" data-i18n="nav_medals">৪২টি পদক</a>
            <a href="#experience" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-sm font-medium hover:bg-slate-100 dark:hover:bg-slate-700" data-i18n="nav_exp">কর্মঅভিজ্ঞতা</a>
            <a href="#military" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-sm font-medium hover:bg-slate-100 dark:hover:bg-slate-700" data-i18n="nav_military">সামরিক সেবা</a>
            <a href="#education" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-sm font-medium hover:bg-slate-100 dark:hover:bg-slate-700" data-i18n="nav_edu">শিক্ষা</a>
            <a href="#contact" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-sm font-medium hover:bg-slate-100 dark:hover:bg-slate-700" data-i18n="nav_contact">যোগাযোগ</a>
            <button onclick="window.print()" class="w-full mt-2 flex items-center justify-center gap-2 px-4 py-2 rounded-xl text-xs font-semibold bg-slate-900 text-white dark:bg-amber-500 dark:text-slate-950">
                <i class="fa-solid fa-print"></i>
                <span data-i18n="btn_print">প্রিন্ট / PDF</span>
            </button>
        </div>
    </header>

    <!-- Main Container -->
    <main id="top" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-12 space-y-16">

        <!-- 1. HERO & PROFILE HEADER SECTION -->
        <section class="relative rounded-3xl overflow-hidden bg-gradient-to-br from-slate-900 via-slate-800 to-emerald-950 text-white shadow-2xl border border-slate-700/60 print-shadow-none">
            <!-- Decorative Subtle Background Pattern -->
            <div class="absolute inset-0 opacity-10 pointer-events-none" style="background-image: radial-gradient(#fbbf24 1px, transparent 1px); background-size: 24px 24px;"></div>

            <div class="relative p-6 sm:p-10 lg:p-12 grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <!-- Left Column: Portrait & ID Badge -->
                <div class="lg:col-span-4 flex flex-col items-center text-center">
                    <div class="relative group">
                        <div class="w-48 h-56 sm:w-56 sm:h-64 rounded-2xl overflow-hidden border-4 border-amber-400/80 shadow-2xl bg-slate-800 flex items-center justify-center relative">
                            <!-- Embedded Portrait Visual / Graceful Fallback -->
                            <img id="profile-photo" 
                                 src="IMG_2651_2.jpeg" 
                                 alt="MD SHAHIN ALAM" 
                                 onerror="this.onerror=null; if(this.src.indexOf('IMG_2651.jpeg') === -1){ this.src='IMG_2651.jpeg'; } else { this.src='https://placehold.co/450x550/0f172a/fbbf24?text=MD+SHAHIN+ALAM'; }"
                                 class="w-full h-full object-cover object-top group-hover:scale-105 transition-transform duration-500">
                            
                            <!-- Interactive Photo Upload Overlay Button -->
                            <label for="photo-upload-input" class="no-print absolute bottom-2 right-2 px-3 py-1.5 rounded-xl bg-slate-950/85 hover:bg-emerald-700 text-amber-300 hover:text-white text-xs font-semibold border border-amber-400/40 cursor-pointer shadow-lg transition-all flex items-center gap-1.5 backdrop-blur-sm" title="Change Profile Photo">
                                <i class="fa-solid fa-camera"></i>
                                <span data-i18n="btn_photo">ছবি পরিবর্তন</span>
                            </label>
                            <input type="file" id="photo-upload-input" accept="image/*" class="hidden" onchange="handlePhotoUpload(event)">
                        </div>
                        <!-- ID Pill -->
                        <div class="mt-4 inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-slate-950/90 border border-amber-400/40 text-amber-300 text-xs font-mono tracking-wider shadow-lg">
                            <i class="fa-solid fa-id-card"></i>
                            <span>ID: 4174276388</span>
                        </div>
                    </div>

                    <!-- Quick Stat Highlights under photo -->
                    <div class="grid grid-cols-3 gap-2 w-full max-w-xs mt-6">
                        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-2.5 border border-white/10">
                            <div class="text-xl font-extrabold text-amber-400">15</div>
                            <div class="text-[11px] text-slate-300" data-i18n="stat_army">বছর সেনাবাহিনী</div>
                        </div>
                        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-2.5 border border-white/10">
                            <div class="text-xl font-extrabold text-emerald-400">42</div>
                            <div class="text-[11px] text-slate-300" data-i18n="stat_medals">মোট পদক</div>
                        </div>
                        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-2.5 border border-white/10">
                            <div class="text-xl font-extrabold text-sky-400">5+</div>
                            <div class="text-[11px] text-slate-300" data-i18n="stat_guide">বছর গাইড</div>
                        </div>
                    </div>
                </div>

                <!-- Right Column: Name, Roles, Contact Badges & Personal Info -->
                <div class="lg:col-span-8 space-y-6">
                    <div>
                        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-emerald-500/20 border border-emerald-400/30 text-emerald-300 text-xs font-semibold mb-3">
                            <i class="fa-solid fa-shield-halved"></i>
                            <span data-i18n="hero_badge">বাংলাদেশ সেনাবাহিনী (অবসরপ্রাপ্ত ল্যান্স কর্পোরাল)</span>
                        </div>
                        <h1 class="text-3xl sm:text-5xl font-extrabold tracking-tight text-white">
                            MD SHAHIN ALAM
                        </h1>
                        <p class="mt-2 text-base sm:text-lg text-amber-300/95 font-medium leading-relaxed" data-i18n="hero_roles">
                            অবসরপ্রাপ্ত ল্যান্স কর্পোরাল (বাংলাদেশ সেনাবাহিনী) | লোকাল মেডিকেল অ্যাসিস্ট্যান্ট | পেশাদার ড্রাইভার | ট্যুরিস্ট গাইড ও ফটোগ্রাফার
                        </p>
                    </div>

                    <!-- Quick Contact Badges -->
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                        <!-- Phone -->
                        <div class="flex items-center justify-between gap-2 p-3 rounded-xl bg-white/10 border border-white/10 hover:bg-white/15 transition-colors">
                            <a href="tel:+8801352282427" class="flex items-center gap-3 text-sm">
                                <span class="w-9 h-9 rounded-lg bg-emerald-600/30 text-emerald-300 flex items-center justify-center shrink-0">
                                    <i class="fa-solid fa-phone"></i>
                                </span>
                                <div>
                                    <span class="text-[11px] text-slate-400 block" data-i18n="lbl_phone">মোবাইল নম্বর</span>
                                    <span class="font-semibold text-white">(+880) 1352282427</span>
                                </div>
                            </a>
                            <button onclick="copyText('+8801352282427')" class="p-2 text-slate-300 hover:text-amber-400 transition-colors no-print" title="Copy Phone">
                                <i class="fa-regular fa-copy"></i>
                            </button>
                        </div>

                        <!-- WhatsApp -->
                        <div class="flex items-center justify-between gap-2 p-3 rounded-xl bg-white/10 border border-white/10 hover:bg-white/15 transition-colors">
                            <a href="https://wa.me/8801880093666" target="_blank" rel="noopener noreferrer" class="flex items-center gap-3 text-sm">
                                <span class="w-9 h-9 rounded-lg bg-green-600/30 text-green-400 flex items-center justify-center shrink-0">
                                    <i class="fa-brands fa-whatsapp text-lg"></i>
                                </span>
                                <div>
                                    <span class="text-[11px] text-slate-400 block">WhatsApp</span>
                                    <span class="font-semibold text-white">+8801880093666</span>
                                </div>
                            </a>
                            <button onclick="copyText('+8801880093666')" class="p-2 text-slate-300 hover:text-amber-400 transition-colors no-print" title="Copy WhatsApp">
                                <i class="fa-regular fa-copy"></i>
                            </button>
                        </div>

                        <!-- Email -->
                        <div class="flex items-center justify-between gap-2 p-3 rounded-xl bg-white/10 border border-white/10 hover:bg-white/15 transition-colors">
                            <a href="mailto:shahinalam6238@gmail.com" class="flex items-center gap-3 text-sm truncate">
                                <span class="w-9 h-9 rounded-lg bg-amber-500/20 text-amber-300 flex items-center justify-center shrink-0">
                                    <i class="fa-solid fa-envelope"></i>
                                </span>
                                <div class="truncate">
                                    <span class="text-[11px] text-slate-400 block" data-i18n="lbl_email">ইমেইল ঠিকানা</span>
                                    <span class="font-semibold text-white truncate block">shahinalam6238@gmail.com</span>
                                </div>
                            </a>
                            <button onclick="copyText('shahinalam6238@gmail.com')" class="p-2 text-slate-300 hover:text-amber-400 transition-colors no-print" title="Copy Email">
                                <i class="fa-regular fa-copy"></i>
                            </button>
                        </div>

                        <!-- Home Address -->
                        <div class="flex items-center gap-3 p-3 rounded-xl bg-white/10 border border-white/10 text-sm">
                            <span class="w-9 h-9 rounded-lg bg-sky-500/20 text-sky-300 flex items-center justify-center shrink-0">
                                <i class="fa-solid fa-location-dot"></i>
                            </span>
                            <div>
                                <span class="text-[11px] text-slate-400 block" data-i18n="lbl_address">স্থায়ী ঠিকানা</span>
                                <span class="font-medium text-white text-xs sm:text-sm leading-snug">Word No -09, Bijoypasha, Paikkandi, Gopalganj-8100, Bangladesh</span>
                            </div>
                        </div>
                    </div>

                    <!-- Personal Details, Languages & Family Grid -->
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 pt-2">
                        <!-- Personal Info -->
                        <div class="bg-slate-950/50 rounded-2xl p-4 border border-white/10 space-y-2 text-xs">
                            <h3 class="text-amber-400 font-bold uppercase tracking-wider flex items-center gap-1.5">
                                <i class="fa-solid fa-user-check"></i>
                                <span data-i18n="sec_personal">ব্যক্তিগত তথ্য</span>
                            </h3>
                            <p><span class="text-slate-400" data-i18n="lbl_dob">জন্ম তারিখ:</span> <span class="font-semibold text-white">1 Mar 1992</span></p>
                            <p><span class="text-slate-400" data-i18n="lbl_pob">জন্মস্থান:</span> <span class="font-semibold text-white">Gopalganj, Bangladesh</span></p>
                            <p><span class="text-slate-400" data-i18n="lbl_nat">জাতীয়তা:</span> <span class="font-semibold text-white">Bangladeshi</span></p>
                            <p><span class="text-slate-400" data-i18n="lbl_sex">লিঙ্গ:</span> <span class="font-semibold text-white">Male</span></p>
                        </div>

                        <!-- Languages -->
                        <div class="bg-slate-950/50 rounded-2xl p-4 border border-white/10 space-y-2.5 text-xs">
                            <h3 class="text-emerald-400 font-bold uppercase tracking-wider flex items-center gap-1.5">
                                <i class="fa-solid fa-comments"></i>
                                <span data-i18n="sec_lang">ভাষা দক্ষতা</span>
                            </h3>
                            <div class="flex flex-wrap gap-2 pt-1">
                                <span class="px-3 py-1 rounded-lg bg-emerald-600/30 border border-emerald-500/40 text-emerald-200 font-semibold">Bangla (বাংলা)</span>
                                <span class="px-3 py-1 rounded-lg bg-sky-600/30 border border-sky-500/40 text-sky-200 font-semibold">English</span>
                                <span class="px-3 py-1 rounded-lg bg-amber-600/30 border border-amber-500/40 text-amber-200 font-semibold">Hindi</span>
                            </div>
                        </div>

                        <!-- Family Introduction -->
                        <div class="bg-slate-950/50 rounded-2xl p-4 border border-white/10 space-y-2 text-xs">
                            <h3 class="text-sky-400 font-bold uppercase tracking-wider flex items-center gap-1.5">
                                <i class="fa-solid fa-people-roof"></i>
                                <span data-i18n="sec_family">পরিবার পরিচিতি</span>
                            </h3>
                            <p><span class="text-slate-400" data-i18n="lbl_wife">স্ত্রী:</span> <span class="font-semibold text-white">Sharmin Sultana</span></p>
                            <p><span class="text-slate-400" data-i18n="lbl_son1">পুত্র ১:</span> <span class="font-semibold text-white">Ayan Ahsan Sajim</span></p>
                            <p><span class="text-slate-400" data-i18n="lbl_son2">পুত্র ২:</span> <span class="font-semibold text-white">Adrinan Ahsan Ifat</span></p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 2. ABOUT MYSELF SECTION -->
        <section id="about" class="scroll-mt-24">
            <div class="bg-white dark:bg-navy-800 rounded-3xl p-6 sm:p-10 shadow-lg border border-slate-200/80 dark:border-slate-800 print-shadow-none">
                <div class="flex items-center gap-3 mb-4">
                    <div class="w-10 h-10 rounded-xl bg-emerald-100 dark:bg-emerald-950 text-emerald-700 dark:text-emerald-400 flex items-center justify-center text-lg">
                        <i class="fa-solid fa-address-card"></i>
                    </div>
                    <div>
                        <h2 class="text-2xl font-bold text-slate-900 dark:text-white" data-i18n="about_title">আমার সম্পর্কে (About Myself)</h2>
                        <p class="text-xs text-slate-500 dark:text-slate-400" data-i18n="about_sub">পেশাগত নিষ্ঠা, সেবা এবং বহুমুখী দক্ষতার সংক্ষিপ্ত বিবরণ</p>
                    </div>
                </div>
                <p class="text-slate-700 dark:text-slate-300 leading-relaxed text-base sm:text-lg" data-i18n="about_text">
                    আমি মোঃ শাহিন আলম। আমি একজন পরিশ্রমী যোদ্ধা এবং আমার অর্জিত দক্ষতার মাধ্যমে মানুষের সেবা করে আসছি। আমি একজন লোকাল মেডিকেল অ্যাসিস্ট্যান্ট এবং পরিবার পরিকল্পনা প্রশিক্ষণ কোর্সসহ ৬ মাস ধরে চিকিৎসা সেবা প্রদান করেছি। এর পাশাপাশি আমি একজন ট্যুরিস্ট গাইড হিসেবে গত ৫ বছর ধরে পার্ট-টাইম কাজ করছি। ফটোগ্রাফিতে আমার উচ্চমানের দক্ষতা রয়েছে এবং আমি একজন দক্ষ ফটোগ্রাফার। আমি জানি কীভাবে নিখুঁতভাবে কাজ করে মানুষের হৃদয় জয় করতে হয়—আর সে কারণেই আমি আমার কাজে সেরা।
                </p>

                <!-- Core Skill Pillars -->
                <div class="grid grid-cols-2 sm:grid-cols-4 gap-4 mt-6 pt-6 border-t border-slate-100 dark:border-slate-700/60">
                    <div class="flex items-center gap-3 p-3 rounded-2xl bg-slate-50 dark:bg-slate-900/60">
                        <i class="fa-solid fa-person-military-rifle text-emerald-600 text-xl"></i>
                        <span class="text-xs sm:text-sm font-semibold" data-i18n="skill_1">সামরিক শৃঙ্খলা ও নিরাপত্তা</span>
                    </div>
                    <div class="flex items-center gap-3 p-3 rounded-2xl bg-slate-50 dark:bg-slate-900/60">
                        <i class="fa-solid fa-kit-medical text-rose-500 text-xl"></i>
                        <span class="text-xs sm:text-sm font-semibold" data-i18n="skill_2">প্রাথমিক চিকিৎসা ও নার্সিং</span>
                    </div>
                    <div class="flex items-center gap-3 p-3 rounded-2xl bg-slate-50 dark:bg-slate-900/60">
                        <i class="fa-solid fa-car-side text-amber-500 text-xl"></i>
                        <span class="text-xs sm:text-sm font-semibold" data-i18n="skill_3">পেশাদার ড্রাইভিং ও ট্যুর গাইড</span>
                    </div>
                    <div class="flex items-center gap-3 p-3 rounded-2xl bg-slate-50 dark:bg-slate-900/60">
                        <i class="fa-solid fa-camera-retro text-sky-500 text-xl"></i>
                        <span class="text-xs sm:text-sm font-semibold" data-i18n="skill_4">পেশাদার ফটোগ্রাফি</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- 3. ACHIEVEMENTS & MEDALS HIGHLIGHT SECTION -->
        <section id="achievements" class="scroll-mt-24 space-y-6">
            <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-4">
                <div>
                    <span class="text-xs font-bold uppercase tracking-wider text-amber-600 dark:text-amber-400" data-i18n="medal_kicker">ক্রীড়া ও গৌরবময় অর্জন</span>
                    <h2 class="text-2xl sm:text-3xl font-extrabold text-slate-900 dark:text-white mt-1" data-i18n="medal_title">পদক ও সম্মাননা (মোট ৪২টি পদক)</h2>
                </div>
                <div class="inline-flex items-center gap-2 px-4 py-2 rounded-2xl bg-amber-100 dark:bg-amber-500/20 text-amber-900 dark:text-amber-300 font-bold text-sm border border-amber-300 dark:border-amber-500/30">
                    <i class="fa-solid fa-trophy text-amber-500 text-lg"></i>
                    <span data-i18n="medal_total_badge">৩৯টি সাঁতার পদক + ০৩টি অ্যাথলেটিক্স পদক</span>
                </div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                <!-- Swimming Competition Card (39 Medals) -->
                <div class="bg-gradient-to-br from-sky-900 to-slate-900 text-white rounded-3xl p-6 sm:p-8 shadow-xl border border-sky-700/50 relative overflow-hidden">
                    <div class="absolute -right-6 -bottom-6 text-sky-500/10 text-9xl pointer-events-none">
                        <i class="fa-solid fa-person-swimming"></i>
                    </div>
                    <div class="flex items-center justify-between mb-6">
                        <div class="flex items-center gap-3">
                            <div class="w-12 h-12 rounded-2xl bg-sky-500/20 border border-sky-400/30 flex items-center justify-center text-sky-300 text-2xl">
                                <i class="fa-solid fa-person-swimming"></i>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold" data-i18n="swim_title">সাঁতার প্রতিযোগিতা</h3>
                                <p class="text-xs text-sky-300" data-i18n="swim_sub">বাংলাদেশ সেনাবাহিনী আন্তঃডিভিশন সাঁতার</p>
                            </div>
                        </div>
                        <div class="text-right">
                            <span class="text-4xl font-black text-amber-400">39</span>
                            <span class="block text-xs uppercase tracking-wider text-sky-200" data-i18n="lbl_medals">পদক</span>
                        </div>
                    </div>

                    <div class="space-y-3 relative z-10">
                        <div class="flex items-center justify-between p-4 rounded-2xl bg-white/10 border border-white/10">
                            <div>
                                <div class="font-bold text-base">Bogra Division (বগুড়া ডিভিশন)</div>
                                <div class="text-xs text-sky-200" data-i18n="dur_6yr">সময়কাল: ০৬ বছর</div>
                            </div>
                            <span class="px-3.5 py-1.5 rounded-xl bg-amber-400 text-slate-950 font-extrabold text-sm">34 Medals</span>
                        </div>
                        <div class="flex items-center justify-between p-4 rounded-2xl bg-white/10 border border-white/10">
                            <div>
                                <div class="font-bold text-base">Chattagong Division (চট্টগ্রাম ডিভিশন)</div>
                                <div class="text-xs text-sky-200" data-i18n="dur_2yr">সময়কাল: ০২ বছর</div>
                            </div>
                            <span class="px-3.5 py-1.5 rounded-xl bg-amber-400/90 text-slate-950 font-extrabold text-sm">05 Medals</span>
                        </div>
                    </div>
                </div>

                <!-- Athletics Competition Card (03 Medals) -->
                <div class="bg-gradient-to-br from-emerald-900 to-slate-900 text-white rounded-3xl p-6 sm:p-8 shadow-xl border border-emerald-700/50 relative overflow-hidden">
                    <div class="absolute -right-6 -bottom-6 text-emerald-500/10 text-9xl pointer-events-none">
                        <i class="fa-solid fa-person-running"></i>
                    </div>
                    <div class="flex items-center justify-between mb-6">
                        <div class="flex items-center gap-3">
                            <div class="w-12 h-12 rounded-2xl bg-emerald-500/20 border border-emerald-400/30 flex items-center justify-center text-emerald-300 text-2xl">
                                <i class="fa-solid fa-medal"></i>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold" data-i18n="ath_title">অ্যাথলেটিক্স প্রতিযোগিতা</h3>
                                <p class="text-xs text-emerald-300" data-i18n="ath_sub">আন্তঃডিভিশন অ্যাথলেটিক্স ও ক্রীড়া নৈপুণ্য</p>
                            </div>
                        </div>
                        <div class="text-right">
                            <span class="text-4xl font-black text-amber-400">03</span>
                            <span class="block text-xs uppercase tracking-wider text-emerald-200" data-i18n="lbl_medals">পদক</span>
                        </div>
                    </div>

                    <div class="space-y-2.5 relative z-10">
                        <div class="flex items-center justify-between p-3 rounded-2xl bg-white/10 border border-white/10">
                            <div>
                                <div class="font-bold text-sm">Chattagong Division (চট্টগ্রাম ডিভিশন)</div>
                                <div class="text-xs text-emerald-200" data-i18n="dur_2yr">সময়কাল: ০২ বছর</div>
                            </div>
                            <span class="px-3 py-1 rounded-xl bg-amber-400 text-slate-950 font-extrabold text-xs">01 Medal</span>
                        </div>
                        <div class="flex items-center justify-between p-3 rounded-2xl bg-white/10 border border-white/10">
                            <div>
                                <div class="font-bold text-sm">Bogra Division (বগুড়া ডিভিশন)</div>
                                <div class="text-xs text-emerald-200" data-i18n="dur_6yr">সময়কাল: ০৬ বছর</div>
                            </div>
                            <span class="px-3 py-1 rounded-xl bg-amber-400 text-slate-950 font-extrabold text-xs">01 Medal</span>
                        </div>
                        <div class="flex items-center justify-between p-3 rounded-2xl bg-white/10 border border-white/10">
                            <div>
                                <div class="font-bold text-sm">Ghatail Division (ঘাটাইল ডিভিশন)</div>
                                <div class="text-xs text-emerald-200" data-i18n="dur_4yr">সময়কাল: ০৪ বছর</div>
                            </div>
                            <span class="px-3 py-1 rounded-xl bg-amber-400 text-slate-950 font-extrabold text-xs">01 Medal</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 4. WORK EXPERIENCE TIMELINE (ALL 6 ROLES) -->
        <section id="experience" class="scroll-mt-24 space-y-6">
            <div>
                <span class="text-xs font-bold uppercase tracking-wider text-emerald-700 dark:text-emerald-400" data-i18n="exp_kicker">পেশাগত ইতিহাস</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-slate-900 dark:text-white mt-1" data-i18n="exp_title">কর্মঅভিজ্ঞতা (Work Experience)</h2>
            </div>

            <div class="relative border-l-2 border-emerald-600/40 dark:border-emerald-500/40 ml-3 sm:ml-6 space-y-8 pl-6 sm:pl-8">
                
                <!-- Role 1: Driver (Current) -->
                <div class="relative bg-white dark:bg-navy-800 rounded-2xl p-6 shadow-md border border-slate-200 dark:border-slate-800 print-shadow-none">
                    <span class="absolute -left-[33px] sm:-left-[41px] top-6 w-4 h-4 rounded-full bg-emerald-500 ring-4 ring-emerald-100 dark:ring-emerald-950"></span>
                    <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                        <div>
                            <span class="inline-block px-3 py-1 rounded-full text-xs font-bold bg-emerald-100 text-emerald-800 dark:bg-emerald-900/60 dark:text-emerald-300 mb-1">
                                05/05/2025 – CURRENT
                            </span>
                            <h3 class="text-xl font-bold text-slate-900 dark:text-white">Driver (পেশাদার ড্রাইভার)</h3>
                        </div>
                        <span class="text-xs font-semibold px-3 py-1 rounded-lg bg-slate-100 dark:bg-slate-700 text-slate-600 dark:text-slate-300">Active Role</span>
                    </div>
                    <ul class="space-y-2 text-sm text-slate-600 dark:text-slate-300 list-disc list-inside">
                        <li>Skillfully driving and ensuring safe driving while strictly adhering to traffic law.</li>
                        <li>Identifying minor vehicle issues and ensuring regular maintenance and servicing.</li>
                        <li>Maintaining excellent professional relationships with local and foreign tourists and ensuring a comfortable journey for them.</li>
                    </ul>
                </div>

                <!-- Role 2: Bangladesh Army -->
                <div class="relative bg-white dark:bg-navy-800 rounded-2xl p-6 shadow-md border border-amber-400/50 dark:border-amber-500/30 print-shadow-none">
                    <span class="absolute -left-[33px] sm:-left-[41px] top-6 w-4 h-4 rounded-full bg-amber-500 ring-4 ring-amber-100 dark:ring-amber-950"></span>
                    <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                        <div>
                            <span class="inline-block px-3 py-1 rounded-full text-xs font-bold bg-amber-100 text-amber-900 dark:bg-amber-900/50 dark:text-amber-300 mb-1">
                                10 Jul 2010 – 5 Apr 2025 (Nearly 15 Years)
                            </span>
                            <h3 class="text-xl font-bold text-slate-900 dark:text-white">Bangladesh Army — Lance Corporal (RETD)</h3>
                            <p class="text-xs font-medium text-slate-500 dark:text-slate-400">Dhaka & Various Cantonments, Bangladesh</p>
                        </div>
                        <span class="text-xs font-bold px-3 py-1 rounded-lg bg-emerald-800 text-amber-300">26 BIR</span>
                    </div>
                    <ul class="space-y-2 text-sm text-slate-600 dark:text-slate-300 list-disc list-inside">
                        <li>Served as a Sainik in the Bangladesh Army for nearly 15 years (from July 2010 to April 2025), gaining robust experience across various cantonments.</li>
                        <li>Accomplished athlete and swimmer, winning <strong>39 medals in swimming</strong> and <strong>3 medals in athletics</strong>.</li>
                        <li>Successfully completed specialized courses including basic military training, Drill Instructor Course (DIC), WIPON course, and Signal cadre.</li>
                        <li>Strong background in <strong>VVIP/VIP protection duty</strong> and served as a <strong>Regiment Police (RP)</strong> member for several years.</li>
                        <li>Hands-on experience working as a company clerk, computer/camera operator, local medical assistant, and tour guide.</li>
                    </ul>
                </div>

                <!-- Role 3: Jim Clinic -->
                <div class="relative bg-white dark:bg-navy-800 rounded-2xl p-6 shadow-md border border-slate-200 dark:border-slate-800 print-shadow-none">
                    <span class="absolute -left-[33px] sm:-left-[41px] top-6 w-4 h-4 rounded-full bg-rose-500 ring-4 ring-rose-100 dark:ring-rose-950"></span>
                    <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                        <div>
                            <span class="inline-block px-3 py-1 rounded-full text-xs font-bold bg-rose-100 text-rose-800 dark:bg-rose-900/50 dark:text-rose-300 mb-1">
                                11/07/2021 – 05/05/2025
                            </span>
                            <h3 class="text-xl font-bold text-slate-900 dark:text-white">Jim Clinic — Nurse (Part-time Job)</h3>
                            <p class="text-xs font-medium text-slate-500 dark:text-slate-400">Ghatail, Dhaka, Bangladesh • Local Medical Assistant & Family Planning Training Course</p>
                        </div>
                    </div>
                    <div class="grid grid-cols-2 sm:grid-cols-4 gap-2 pt-2">
                        <span class="px-3 py-1.5 rounded-xl bg-slate-50 dark:bg-slate-900 text-xs font-medium border border-slate-200 dark:border-slate-700"><i class="fa-solid fa-temperature-half text-rose-500 mr-1.5"></i>Fever measurement</span>
                        <span class="px-3 py-1.5 rounded-xl bg-slate-50 dark:bg-slate-900 text-xs font-medium border border-slate-200 dark:border-slate-700"><i class="fa-solid fa-heart-pulse text-rose-500 mr-1.5"></i>Blood pressure</span>
                        <span class="px-3 py-1.5 rounded-xl bg-slate-50 dark:bg-slate-900 text-xs font-medium border border-slate-200 dark:border-slate-700"><i class="fa-solid fa-kit-medical text-rose-500 mr-1.5"></i>Suturing cut area</span>
                        <span class="px-3 py-1.5 rounded-xl bg-slate-50 dark:bg-slate-900 text-xs font-medium border border-slate-200 dark:border-slate-700"><i class="fa-solid fa-band-aid text-rose-500 mr-1.5"></i>Dressing & Bandage</span>
                        <span class="px-3 py-1.5 rounded-xl bg-slate-50 dark:bg-slate-900 text-xs font-medium border border-slate-200 dark:border-slate-700"><i class="fa-solid fa-droplet text-rose-500 mr-1.5"></i>Saline pushing</span>
                        <span class="px-3 py-1.5 rounded-xl bg-slate-50 dark:bg-slate-900 text-xs font-medium border border-slate-200 dark:border-slate-700"><i class="fa-solid fa-syringe text-rose-500 mr-1.5"></i>Injection pushing</span>
                        <span class="px-3 py-1.5 rounded-xl bg-slate-50 dark:bg-slate-900 text-xs font-medium border border-slate-200 dark:border-slate-700 col-span-2"><i class="fa-solid fa-stethoscope text-rose-500 mr-1.5"></i>Chest Examination</span>
                    </div>
                </div>

                <!-- Role 4: Ema Art's Cameraman -->
                <div class="relative bg-white dark:bg-navy-800 rounded-2xl p-6 shadow-md border border-slate-200 dark:border-slate-800 print-shadow-none">
                    <span class="absolute -left-[33px] sm:-left-[41px] top-6 w-4 h-4 rounded-full bg-sky-500 ring-4 ring-sky-100 dark:ring-sky-950"></span>
                    <div class="flex flex-wrap items-center justify-between gap-2 mb-2">
                        <div>
                            <span class="inline-block px-3 py-1 rounded-full text-xs font-bold bg-sky-100 text-sky-800 dark:bg-sky-900/50 dark:text-sky-300 mb-1">
                                15/01/2011 – 10/05/2016
                            </span>
                            <h3 class="text-lg font-bold text-slate-900 dark:text-white">Ema Art's — Cameraman (Part-time Job)</h3>
                            <p class="text-xs text-slate-500 dark:text-slate-400">Gopalganj, Dhaka, Bangladesh</p>
                        </div>
                    </div>
                    <p class="text-sm text-slate-600 dark:text-slate-300">• Photography in cameraman (04 hours/week)</p>
                </div>

                <!-- Role 5: Comport Tour & Travels -->
                <div class="relative bg-white dark:bg-navy-800 rounded-2xl p-6 shadow-md border border-slate-200 dark:border-slate-800 print-shadow-none">
                    <span class="absolute -left-[33px] sm:-left-[41px] top-6 w-4 h-4 rounded-full bg-indigo-500 ring-4 ring-indigo-100 dark:ring-indigo-950"></span>
                    <div class="flex flex-wrap items-center justify-between gap-2 mb-2">
                        <div>
                            <span class="inline-block px-3 py-1 rounded-full text-xs font-bold bg-indigo-100 text-indigo-800 dark:bg-indigo-900/50 dark:text-indigo-300 mb-1">
                                01/02/2008 – 31/12/2010
                            </span>
                            <h3 class="text-lg font-bold text-slate-900 dark:text-white">Comport Tour & Travels — Tourist Guide</h3>
                            <p class="text-xs text-slate-500 dark:text-slate-400">Dhaka, Bangladesh</p>
                        </div>
                    </div>
                    <ul class="space-y-1 text-sm text-slate-600 dark:text-slate-300 list-disc list-inside">
                        <li>Maintenance of tourism operations</li>
                        <li>Building strong relations with tourists</li>
                        <li>Coaching a junior employee team (2 hours/week)</li>
                    </ul>
                </div>

                <!-- Role 6: Decle Company -->
                <div class="relative bg-white dark:bg-navy-800 rounded-2xl p-6 shadow-md border border-slate-200 dark:border-slate-800 print-shadow-none">
                    <span class="absolute -left-[33px] sm:-left-[41px] top-6 w-4 h-4 rounded-full bg-slate-400 ring-4 ring-slate-200 dark:ring-slate-800"></span>
                    <div class="flex flex-wrap items-center justify-between gap-2 mb-2">
                        <div>
                            <span class="inline-block px-3 py-1 rounded-full text-xs font-bold bg-slate-100 text-slate-800 dark:bg-slate-700 dark:text-slate-300 mb-1">
                                06/06/2007 – 30/12/2007
                            </span>
                            <h3 class="text-lg font-bold text-slate-900 dark:text-white">Decle Company — Sales Man</h3>
                            <p class="text-xs text-slate-500 dark:text-slate-400">Dhaka, Bangladesh</p>
                        </div>
                    </div>
                    <ul class="space-y-1 text-sm text-slate-600 dark:text-slate-300 list-disc list-inside">
                        <li>Maintenance of computers</li>
                        <li>Maintaining relations with suppliers</li>
                        <li>Coaching a junior Ice Hockey team (8 hours/week)</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- 5. MILITARY SERVICE HISTORY, APPOINTMENTS, COURSES & VVIP DUTIES (INTERACTIVE TABS) -->
        <section id="military" class="scroll-mt-24 space-y-6">
            <div>
                <span class="text-xs font-bold uppercase tracking-wider text-emerald-700 dark:text-emerald-400" data-i18n="mil_kicker">১৫ বছরের সামরিক রেকর্ড</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-slate-900 dark:text-white mt-1" data-i18n="mil_title">সামরিক পোস্টিং, দায়িত্বসমূহ, কোর্স ও ভিভিআইপি ডিউটি</h2>
            </div>

            <!-- Interactive Filter Tabs -->
            <div class="flex flex-wrap gap-2 no-print" id="military-tabs">
                <button onclick="switchMilitaryTab('all')" data-tab="all" class="mil-tab-btn active px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold bg-emerald-700 text-white shadow-md transition-all">
                    <i class="fa-solid fa-layer-group mr-1.5"></i><span data-i18n="tab_all">সকল তথ্য</span>
                </button>
                <button onclick="switchMilitaryTab('postings')" data-tab="postings" class="mil-tab-btn px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold bg-white dark:bg-navy-800 text-slate-700 dark:text-slate-300 border border-slate-200 dark:border-slate-700 hover:bg-slate-100 transition-all">
                    <i class="fa-solid fa-calendar-days mr-1.5"></i><span data-i18n="tab_postings">চাকরির মেয়াদ ও পোস্টিং (৬টি)</span>
                </button>
                <button onclick="switchMilitaryTab('appointments')" data-tab="appointments" class="mil-tab-btn px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold bg-white dark:bg-navy-800 text-slate-700 dark:text-slate-300 border border-slate-200 dark:border-slate-700 hover:bg-slate-100 transition-all">
                    <i class="fa-solid fa-user-shield mr-1.5"></i><span data-i18n="tab_app">গুরুত্বপূর্ণ নিয়োগ (৭টি)</span>
                </button>
                <button onclick="switchMilitaryTab('courses')" data-tab="courses" class="mil-tab-btn px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold bg-white dark:bg-navy-800 text-slate-700 dark:text-slate-300 border border-slate-200 dark:border-slate-700 hover:bg-slate-100 transition-all">
                    <i class="fa-solid fa-award mr-1.5"></i><span data-i18n="tab_courses">কোর্স, ক্যাডার ও VVIP ডিউটি</span>
                </button>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                <!-- Panel 1: Duration of Job / Postings -->
                <div id="panel-postings" class="mil-panel bg-white dark:bg-navy-800 rounded-3xl p-6 shadow-md border border-slate-200 dark:border-slate-800 print-shadow-none">
                    <h3 class="text-lg font-bold text-slate-900 dark:text-white mb-4 flex items-center gap-2">
                        <span class="w-8 h-8 rounded-lg bg-emerald-100 dark:bg-emerald-950 text-emerald-700 dark:text-emerald-400 flex items-center justify-center">
                            <i class="fa-solid fa-building-shield"></i>
                        </span>
                        <span data-i18n="hd_postings">চাকরির মেয়াদ ও ক্যান্টনমেন্ট পোস্টিং (Duration of Job)</span>
                    </h3>
                    <div class="overflow-x-auto">
                        <table class="w-full text-left border-collapse text-sm">
                            <thead>
                                <tr class="border-b border-slate-200 dark:border-slate-700 text-xs uppercase text-slate-500">
                                    <th class="py-2.5 pr-3">Unit / Cantonment</th>
                                    <th class="py-2.5 text-right">Duration</th>
                                </tr>
                            </thead>
                            <tbody class="divide-y divide-slate-100 dark:divide-slate-800">
                                <tr>
                                    <td class="py-3 pr-3 font-semibold text-slate-800 dark:text-slate-200">Rajshahi Training Center</td>
                                    <td class="py-3 text-right font-mono text-xs text-emerald-700 dark:text-emerald-400">11-07-2010 to 23-12-2010</td>
                                </tr>
                                <tr>
                                    <td class="py-3 pr-3 font-semibold text-slate-800 dark:text-slate-200">26 BIR (Chattagong Cantt.)</td>
                                    <td class="py-3 text-right font-mono text-xs text-emerald-700 dark:text-emerald-400">25-12-2010 to 18-02-2013</td>
                                </tr>
                                <tr>
                                    <td class="py-3 pr-3 font-semibold text-slate-800 dark:text-slate-200">26 BIR (Bogra Cantt.)</td>
                                    <td class="py-3 text-right font-mono text-xs text-emerald-700 dark:text-emerald-400">18-02-2013 to 20-11-2018</td>
                                </tr>
                                <tr>
                                    <td class="py-3 pr-3 font-semibold text-slate-800 dark:text-slate-200">Army Swimming Team (Dhaka)</td>
                                    <td class="py-3 text-right font-mono text-xs text-sky-600 dark:text-sky-400 font-bold">15-04-2013 to 02-02-2015</td>
                                </tr>
                                <tr>
                                    <td class="py-3 pr-3 font-semibold text-slate-800 dark:text-slate-200">26 BIR (Bandarban Cantt.)</td>
                                    <td class="py-3 text-right font-mono text-xs text-emerald-700 dark:text-emerald-400">21-12-2018 to 20-11-2021</td>
                                </tr>
                                <tr>
                                    <td class="py-3 pr-3 font-semibold text-slate-800 dark:text-slate-200">26 BIR (Ghatail Cantt.)</td>
                                    <td class="py-3 text-right font-mono text-xs text-emerald-700 dark:text-emerald-400">21-11-2021 to 05-04-2025</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>

                <!-- Panel 2: Important Appointments -->
                <div id="panel-appointments" class="mil-panel bg-white dark:bg-navy-800 rounded-3xl p-6 shadow-md border border-slate-200 dark:border-slate-800 print-shadow-none">
                    <h3 class="text-lg font-bold text-slate-900 dark:text-white mb-4 flex items-center gap-2">
                        <span class="w-8 h-8 rounded-lg bg-amber-100 dark:bg-amber-950 text-amber-700 dark:text-amber-400 flex items-center justify-center">
                            <i class="fa-solid fa-star"></i>
                        </span>
                        <span data-i18n="hd_app">গুরুত্বপূর্ণ নিয়োগসমূহ (Important Appointments)</span>
                    </h3>
                    <ul class="space-y-2.5 text-sm">
                        <li class="flex items-center justify-between p-3 rounded-xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                            <span class="font-semibold">RP (Regiment Police) — 26 BIR, Chattagong Cantt.</span>
                            <span class="px-2.5 py-1 rounded-lg bg-amber-100 dark:bg-amber-900/40 text-amber-800 dark:text-amber-300 text-xs font-bold shrink-0">02 Years</span>
                        </li>
                        <li class="flex items-center justify-between p-3 rounded-xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                            <span class="font-semibold">Company Clerk — 26 BIR, Chattagong Cantt.</span>
                            <span class="px-2.5 py-1 rounded-lg bg-slate-200 dark:bg-slate-800 text-slate-700 dark:text-slate-300 text-xs font-bold shrink-0">03 Months</span>
                        </li>
                        <li class="flex items-center justify-between p-3 rounded-xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                            <span class="font-semibold">Drill Instructor — Rajshahi Cantt.</span>
                            <span class="px-2.5 py-1 rounded-lg bg-amber-100 dark:bg-amber-900/40 text-amber-800 dark:text-amber-300 text-xs font-bold shrink-0">02 Years</span>
                        </li>
                        <li class="flex items-center justify-between p-3 rounded-xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                            <span class="font-semibold">Drill Instructor (DIC Course-16) — Ghatail Cantt.</span>
                            <span class="px-2.5 py-1 rounded-lg bg-slate-200 dark:bg-slate-800 text-slate-700 dark:text-slate-300 text-xs font-bold shrink-0">03 Months</span>
                        </li>
                        <li class="flex items-center justify-between p-3 rounded-xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                            <span class="font-semibold">RP (Regiment Police) — 26 BIR, Ghatail Cantt.</span>
                            <span class="px-2.5 py-1 rounded-lg bg-emerald-100 dark:bg-emerald-900/40 text-emerald-800 dark:text-emerald-300 text-xs font-bold shrink-0">05 Years</span>
                        </li>
                        <li class="flex items-center justify-between p-3 rounded-xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                            <span class="font-semibold">INT (Computer/Camera Operator) — Bogra Cantt.</span>
                            <span class="px-2.5 py-1 rounded-lg bg-amber-100 dark:bg-amber-900/40 text-amber-800 dark:text-amber-300 text-xs font-bold shrink-0">03 Years</span>
                        </li>
                        <li class="flex items-center justify-between p-3 rounded-xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                            <span class="font-semibold">Company Clerk — 26 BIR, Ghatail Cantt.</span>
                            <span class="px-2.5 py-1 rounded-lg bg-amber-100 dark:bg-amber-900/40 text-amber-800 dark:text-amber-300 text-xs font-bold shrink-0">03 Years</span>
                        </li>
                    </ul>
                </div>

                <!-- Panel 3: Courses, Cadres & VVIP Protection Duty -->
                <div id="panel-courses" class="mil-panel lg:col-span-2 grid grid-cols-1 md:grid-cols-12 gap-6">
                    <!-- Courses & Cadres (7 Cols) -->
                    <div class="md:col-span-7 bg-white dark:bg-navy-800 rounded-3xl p-6 shadow-md border border-slate-200 dark:border-slate-800 print-shadow-none">
                        <h3 class="text-lg font-bold text-slate-900 dark:text-white mb-4 flex items-center gap-2">
                            <span class="w-8 h-8 rounded-lg bg-sky-100 dark:bg-sky-950 text-sky-700 dark:text-sky-400 flex items-center justify-center">
                                <i class="fa-solid fa-certificate"></i>
                            </span>
                            <span data-i18n="hd_courses">সামরিক কোর্স ও ক্যাডার (Course and Cadre)</span>
                        </h3>
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 text-sm">
                            <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                                <div class="font-bold text-emerald-700 dark:text-emerald-400">DIC (Drill Instructor Course)</div>
                                <div class="text-xs text-slate-500 dark:text-slate-400 mt-0.5">Rajshahi Cantt.</div>
                            </div>
                            <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                                <div class="font-bold text-emerald-700 dark:text-emerald-400">WIPON Course (82 mm Mortar)</div>
                                <div class="text-xs text-slate-500 dark:text-slate-400 mt-0.5">Ghatail Cantt.</div>
                            </div>
                            <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                                <div class="font-bold text-emerald-700 dark:text-emerald-400">RL/GF Cadre</div>
                                <div class="text-xs text-slate-500 dark:text-slate-400 mt-0.5">Rocket Launcher / Grenade Launcher • Chattagong Cantt.</div>
                            </div>
                            <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                                <div class="font-bold text-emerald-700 dark:text-emerald-400">Signal Cadre</div>
                                <div class="text-xs text-slate-500 dark:text-slate-400 mt-0.5">Seven Signal • Chattagong Cantt.</div>
                            </div>
                            <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                                <div class="font-bold text-emerald-700 dark:text-emerald-400">RP Cadre (Unit Security)</div>
                                <div class="text-xs text-slate-500 dark:text-slate-400 mt-0.5">Bogra Cantt.</div>
                            </div>
                            <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800">
                                <div class="font-bold text-emerald-700 dark:text-emerald-400">MT Cadre (Motor Transport)</div>
                                <div class="text-xs text-slate-500 dark:text-slate-400 mt-0.5">Bogra Cantt.</div>
                            </div>
                            <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-900/70 border border-slate-100 dark:border-slate-800 sm:col-span-2">
                                <div class="font-bold text-emerald-700 dark:text-emerald-400">MT Course (Motor Transport Training)</div>
                                <div class="text-xs text-slate-500 dark:text-slate-400 mt-0.5">Khulna Cantt.</div>
                            </div>
                        </div>
                    </div>

                    <!-- VVIP / VIP Protection Duty (5 Cols) -->
                    <div class="md:col-span-5 bg-gradient-to-br from-slate-900 to-navy-800 text-white rounded-3xl p-6 shadow-md border border-slate-700 flex flex-col justify-between">
                        <div>
                            <h3 class="text-lg font-bold text-amber-400 mb-2 flex items-center gap-2">
                                <i class="fa-solid fa-shield-cat"></i>
                                <span data-i18n="hd_vvip">VVIP / VIP প্রোটেকশন ডিউটি</span>
                            </h3>
                            <p class="text-xs text-slate-300 mb-5" data-i18n="vvip_desc">
                                দেশের গুরুত্বপূর্ণ ৭টি জেলা ও অঞ্চলে রাষ্ট্রীয় অতিগুরুত্বপূর্ণ ব্যক্তিদের (VVIP/VIP) নিরাপত্তা প্রদানের অভিজ্ঞতা:
                            </p>
                            <div class="flex flex-wrap gap-2.5">
                                <span class="px-3.5 py-2 rounded-xl bg-white/10 border border-amber-400/30 text-sm font-semibold flex items-center gap-2">
                                    <i class="fa-solid fa-location-crosshairs text-amber-400 text-xs"></i>Rajshahi
                                </span>
                                <span class="px-3.5 py-2 rounded-xl bg-white/10 border border-amber-400/30 text-sm font-semibold flex items-center gap-2">
                                    <i class="fa-solid fa-location-crosshairs text-amber-400 text-xs"></i>Cox's Bazar
                                </span>
                                <span class="px-3.5 py-2 rounded-xl bg-white/10 border border-amber-400/30 text-sm font-semibold flex items-center gap-2">
                                    <i class="fa-solid fa-location-crosshairs text-amber-400 text-xs"></i>Tungipara
                                </span>
                                <span class="px-3.5 py-2 rounded-xl bg-white/10 border border-amber-400/30 text-sm font-semibold flex items-center gap-2">
                                    <i class="fa-solid fa-location-crosshairs text-amber-400 text-xs"></i>Barishal
                                </span>
                                <span class="px-3.5 py-2 rounded-xl bg-white/10 border border-amber-400/30 text-sm font-semibold flex items-center gap-2">
                                    <i class="fa-solid fa-location-crosshairs text-amber-400 text-xs"></i>Bogra
                                </span>
                                <span class="px-3.5 py-2 rounded-xl bg-white/10 border border-amber-400/30 text-sm font-semibold flex items-center gap-2">
                                    <i class="fa-solid fa-location-crosshairs text-amber-400 text-xs"></i>Jessore
                                </span>
                                <span class="px-3.5 py-2 rounded-xl bg-white/10 border border-amber-400/30 text-sm font-semibold flex items-center gap-2">
                                    <i class="fa-solid fa-location-crosshairs text-amber-400 text-xs"></i>Chattagong
                                </span>
                            </div>
                        </div>
                        <div class="mt-6 pt-4 border-t border-white/10 text-xs text-slate-400 flex items-center justify-between">
                            <span>Regiment Police (RP) & Security</span>
                            <span class="text-emerald-400 font-bold">7 Key Zones</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 6. EDUCATION & TRAINING SECTION -->
        <section id="education" class="scroll-mt-24 space-y-6">
            <div>
                <span class="text-xs font-bold uppercase tracking-wider text-emerald-700 dark:text-emerald-400" data-i18n="edu_kicker">একাডেমিক যোগ্যতা</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-slate-900 dark:text-white mt-1" data-i18n="edu_title">শিক্ষাগত যোগ্যতা ও প্রশিক্ষণ (Education & Training)</h2>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5">
                <!-- Masters -->
                <div class="bg-white dark:bg-navy-800 rounded-3xl p-6 shadow-md border border-slate-200 dark:border-slate-800 hover:-translate-y-1 transition-transform print-shadow-none">
                    <div class="flex items-center justify-between mb-4">
                        <span class="w-11 h-11 rounded-2xl bg-emerald-100 dark:bg-emerald-950 text-emerald-700 dark:text-emerald-400 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-graduation-cap"></i>
                        </span>
                        <span class="px-3 py-1 rounded-full bg-emerald-600 text-white text-xs font-extrabold">2020</span>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 dark:text-white">Masters</h3>
                    <p class="text-sm text-slate-600 dark:text-slate-300 mt-1">Govt. Bangabandhu College, Gopalganj, Bangladesh.</p>
                </div>

                <!-- B.A (Pass) -->
                <div class="bg-white dark:bg-navy-800 rounded-3xl p-6 shadow-md border border-slate-200 dark:border-slate-800 hover:-translate-y-1 transition-transform print-shadow-none">
                    <div class="flex items-center justify-between mb-4">
                        <span class="w-11 h-11 rounded-2xl bg-sky-100 dark:bg-sky-950 text-sky-700 dark:text-sky-400 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-user-graduate"></i>
                        </span>
                        <span class="px-3 py-1 rounded-full bg-sky-600 text-white text-xs font-extrabold">2014</span>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 dark:text-white">B.A (Pass)</h3>
                    <p class="text-sm text-slate-600 dark:text-slate-300 mt-1">Govt. Bangabandhu College, Gopalganj, Bangladesh.</p>
                </div>

                <!-- H.S.C -->
                <div class="bg-white dark:bg-navy-800 rounded-3xl p-6 shadow-md border border-slate-200 dark:border-slate-800 hover:-translate-y-1 transition-transform print-shadow-none">
                    <div class="flex items-center justify-between mb-4">
                        <span class="w-11 h-11 rounded-2xl bg-amber-100 dark:bg-amber-950 text-amber-700 dark:text-amber-400 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-book-open"></i>
                        </span>
                        <span class="px-3 py-1 rounded-full bg-amber-500 text-slate-950 text-xs font-extrabold">2009</span>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 dark:text-white">H.S.C</h3>
                    <p class="text-sm text-slate-600 dark:text-slate-300 mt-1">Govt. Bangabandhu College, Gopalganj, Bangladesh.</p>
                </div>

                <!-- S.S.C -->
                <div class="bg-white dark:bg-navy-800 rounded-3xl p-6 shadow-md border border-slate-200 dark:border-slate-800 hover:-translate-y-1 transition
