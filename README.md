# AI-Virtual-Anesthetist-By-Ezzadeen-Al-Kaiati-
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الملف الذكي لمتخصص التخدير</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        'bg-light': '#FFFFFF',
                        'bg-dark': '#181818'
                    },
                    fontFamily: {
                        arabic: ['Tajawal', 'Arial', 'sans-serif']
                    }
                }
            },
            darkMode: 'class'
        }
    </script>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Tajawal', Arial, sans-serif;
        }
        .rtl-input {
            text-align: right;
        }
        .progress-bar {
            transition: width 0.8s ease-in-out;
        }
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .card-hover {
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .card-hover:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(93, 92, 222, 0.15);
        }
    </style>
</head>
<body class="bg-bg-light dark:bg-bg-dark text-gray-900 dark:text-gray-100 min-h-screen transition-colors duration-300">
    <div class="container mx-auto max-w-4xl p-4 md:p-6">
        <!-- Header -->
        <div class="text-center mb-8">
            <div class="mb-4">
                <span class="text-6xl">🩺</span>
            </div>
            <h1 class="text-3xl md:text-4xl font-bold text-primary mb-2">
                الملف الذكي لمتخصص التخدير
            </h1>
            <p class="text-gray-600 dark:text-gray-400 text-lg">
                قيّم مهاراتك واحصل على خطة تطوير مخصصة
            </p>
        </div>

        <!-- Main Card -->
        <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 md:p-8 card-hover">
            <form id="profileForm" class="space-y-6">
                <!-- Personal Information Section -->
                <div class="mb-8">
                    <h2 class="text-xl font-semibold mb-4 text-primary flex items-center">
                        <span class="ml-2">👤</span>
                        المعلومات الشخصية
                    </h2>
                    <div class="grid md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium mb-2">الاسم الكامل</label>
                            <input 
                                type="text" 
                                name="name" 
                                placeholder="أدخل اسمك الكامل"
                                class="w-full px-4 py-3 text-base border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary bg-white dark:bg-gray-700 rtl-input transition-colors duration-200"
                                required
                            >
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-2">الوظيفة</label>
                            <select 
                                name="role" 
                                class="w-full px-4 py-3 text-base border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary bg-white dark:bg-gray-700 rtl-input transition-colors duration-200"
                                required
                            >
                                <option value="">اختر الوظيفة</option>
                                <option value="طبيب تخدير">طبيب تخدير</option>
                                <option value="فني تخدير">فني تخدير</option>
                                <option value="ممرض تخدير">ممرض تخدير</option>
                                <option value="طالب طب">طالب طب</option>
                                <option value="أخرى">أخرى</option>
                            </select>
                        </div>
                    </div>
                </div>

                <!-- Professional Information Section -->
                <div class="mb-8">
                    <h2 class="text-xl font-semibold mb-4 text-primary flex items-center">
                        <span class="ml-2">🎓</span>
                        المعلومات المهنية
                    </h2>
                    <div class="grid md:grid-cols-2 gap-4 mb-4">
                        <div>
                            <label class="block text-sm font-medium mb-2">المستوى العلمي</label>
                            <select 
                                name="level" 
                                class="w-full px-4 py-3 text-base border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary bg-white dark:bg-gray-700 rtl-input transition-colors duration-200"
                                required
                            >
                                <option value="">اختر المستوى</option>
                                <option value="دبلوم">دبلوم</option>
                                <option value="بكالوريوس">بكالوريوس</option>
                                <option value="ماجستير">ماجستير</option>
                                <option value="دكتوراه">دكتوراه</option>
                                <option value="زمالة">زمالة</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-2">سنوات الخبرة</label>
                            <input 
                                type="number" 
                                name="experience" 
                                placeholder="0"
                                min="0"
                                max="50"
                                class="w-full px-4 py-3 text-base border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary bg-white dark:bg-gray-700 rtl-input transition-colors duration-200"
                                required
                            >
                        </div>
                    </div>
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-medium mb-2">المهارات الحالية</label>
                            <textarea 
                                name="skills" 
                                placeholder="اذكر مهاراتك في التخدير، أجهزة المراقبة، المحاكاة السريرية، إدارة الألم، إلخ..."
                                rows="3"
                                class="w-full px-4 py-3 text-base border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary bg-white dark:bg-gray-700 rtl-input transition-colors duration-200 resize-none"
                                required
                            ></textarea>
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-2">معرفتك في الذكاء الاصطناعي</label>
                            <textarea 
                                name="aiKnowledge" 
                                placeholder="اذكر خبرتك في الذكاء الاصطناعي، التقنيات الطبية الذكية، أنظمة دعم القرار، إلخ..."
                                rows="3"
                                class="w-full px-4 py-3 text-base border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary bg-white dark:bg-gray-700 rtl-input transition-colors duration-200 resize-none"
                                required
                            ></textarea>
                        </div>
                    </div>
                </div>

                <!-- Submit Button -->
                <div class="text-center space-y-4">
                    <button 
                        type="submit" 
                        class="bg-primary hover:bg-primary/90 text-white font-semibold py-4 px-8 rounded-lg text-lg transition-all duration-200 transform hover:scale-105 shadow-lg hover:shadow-xl"
                    >
                        <span class="ml-2">⚡</span>
                        قيّمني الآن
                    </button>
                    <div class="flex justify-center space-x-4 rtl:space-x-reverse">
                        <button 
                            type="button" 
                            id="aiAnalysisBtn"
                            class="bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-700 hover:to-pink-700 text-white font-medium py-2 px-6 rounded-lg text-sm transition-all duration-200 transform hover:scale-105 shadow-md"
                        >
                            <span class="ml-2">🤖</span>
                            تحليل ذكي متقدم
                        </button>
                        <button 
                            type="button" 
                            id="skillsTestBtn"
                            class="bg-gradient-to-r from-green-600 to-blue-600 hover:from-green-700 hover:to-blue-700 text-white font-medium py-2 px-6 rounded-lg text-sm transition-all duration-200 transform hover:scale-105 shadow-md"
                        >
                            <span class="ml-2">🧠</span>
                            اختبار المهارات
                        </button>
                    </div>
                </div>
            </form>
        </div>

        <!-- Results Section -->
        <div id="results" class="hidden mt-8">
            <div class="bg-gradient-to-r from-primary/10 to-purple-600/10 dark:from-primary/20 dark:to-purple-600/20 rounded-2xl p-6 md:p-8 fade-in">
                <div class="text-center mb-6">
                    <h2 class="text-2xl font-bold mb-4 text-primary flex items-center justify-center">
                        <span class="ml-2">📊</span>
                        نتيجة التقييم
                    </h2>
                    
                    <!-- Progress Circle -->
                    <div class="relative w-32 h-32 mx-auto mb-4">
                        <svg class="w-32 h-32 transform -rotate-90" viewBox="0 0 100 100">
                            <circle cx="50" cy="50" r="40" stroke="currentColor" stroke-width="4" fill="none" class="text-gray-300 dark:text-gray-600"/>
                            <circle id="progressCircle" cx="50" cy="50" r="40" stroke="currentColor" stroke-width="4" fill="none" 
                                    class="text-primary progress-bar" stroke-linecap="round" 
                                    stroke-dasharray="251.2" stroke-dashoffset="251.2"/>
                        </svg>
                        <div class="absolute inset-0 flex items-center justify-center">
                            <span id="readinessScore" class="text-3xl font-bold text-primary">0%</span>
                        </div>
                    </div>
                    
                    <p class="text-lg mb-2">مؤشر الجاهزية المستقبلية</p>
                    <p id="readinessLevel" class="text-sm text-gray-600 dark:text-gray-400"></p>
                </div>

                <!-- Recommendations -->
                <div id="recommendationsSection" class="mt-8">
                    <h3 class="text-xl font-semibold mb-4 text-primary flex items-center">
                        <span class="ml-2">🎯</span>
                        خطة التطوير المخصصة
                    </h3>
                    <div id="recommendationsList" class="space-y-3">
                        <!-- Recommendations will be inserted here -->
                    </div>
                </div>

                <!-- Strengths -->
                <div id="strengthsSection" class="mt-8">
                    <h3 class="text-xl font-semibold mb-4 text-green-600 dark:text-green-400 flex items-center">
                        <span class="ml-2">💪</span>
                        نقاط القوة
                    </h3>
                    <div id="strengthsList" class="space-y-3">
                        <!-- Strengths will be inserted here -->
                    </div>
                </div>

                <!-- Skills Map -->
                <div id="skillsMapSection" class="mt-8">
                    <h3 class="text-xl font-semibold mb-4 text-primary flex items-center">
                        <span class="ml-2">🗺️</span>
                        خريطة المهارات التفاعلية
                    </h3>
                    <div id="skillsMap" class="grid grid-cols-2 md:grid-cols-4 gap-4">
                        <!-- Skills map will be inserted here -->
                    </div>
                </div>

                <!-- Achievement Badges -->
                <div id="badgesSection" class="mt-8">
                    <h3 class="text-xl font-semibold mb-4 text-yellow-600 dark:text-yellow-400 flex items-center">
                        <span class="ml-2">🏆</span>
                        شارات الإنجاز
                    </h3>
                    <div id="badgesList" class="flex flex-wrap gap-4 justify-center">
                        <!-- Badges will be inserted here -->
                    </div>
                </div>

                <!-- Learning Path -->
                <div id="learningPathSection" class="mt-8">
                    <h3 class="text-xl font-semibold mb-4 text-indigo-600 dark:text-indigo-400 flex items-center">
                        <span class="ml-2">🛤️</span>
                        مسار التعلم المقترح
                    </h3>
                    <div id="learningPath" class="space-y-4">
                        <!-- Learning path will be inserted here -->
                    </div>
                </div>

                <!-- Action Buttons -->
                <div class="mt-8 text-center space-y-4">
                    <div class="flex flex-wrap justify-center gap-4">
                        <button id="exportBtn" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-lg transition-colors duration-200">
                            <span class="ml-2">📄</span>
                            تصدير التقرير
                        </button>
                        <button id="shareBtn" class="bg-green-600 hover:bg-green-700 text-white px-6 py-2 rounded-lg transition-colors duration-200">
                            <span class="ml-2">📤</span>
                            مشاركة النتائج
                        </button>
                        <button id="retakeBtn" class="bg-gray-600 hover:bg-gray-700 text-white px-6 py-2 rounded-lg transition-colors duration-200">
                            <span class="ml-2">🔄</span>
                            إعادة التقييم
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Skills Test Modal -->
        <div id="skillsTestModal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50">
            <div class="bg-white dark:bg-gray-800 rounded-2xl max-w-2xl w-full max-h-[90vh] overflow-y-auto">
                <div class="p-6">
                    <div class="flex justify-between items-center mb-4">
                        <h3 class="text-xl font-bold">🧠 اختبار المهارات التفاعلي</h3>
                        <button id="closeTestModal" class="text-gray-500 hover:text-gray-700 text-xl">&times;</button>
                    </div>
                    <div id="testContent">
                        <!-- Test questions will be inserted here -->
                    </div>
                </div>
            </div>
        </div>

        <!-- AI Analysis Modal -->
        <div id="aiAnalysisModal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50">
            <div class="bg-white dark:bg-gray-800 rounded-2xl max-w-4xl w-full max-h-[90vh] overflow-y-auto">
                <div class="p-6">
                    <div class="flex justify-between items-center mb-4">
                        <h3 class="text-xl font-bold">🤖 التحليل الذكي المتقدم</h3>
                        <button id="closeAiModal" class="text-gray-500 hover:text-gray-700 text-xl">&times;</button>
                    </div>
                    <div id="aiAnalysisContent" class="space-y-4">
                        <div class="text-center py-8">
                            <div class="inline-block animate-spin rounded-full h-8 w-8 border-b-2 border-primary"></div>
                            <p class="mt-2 text-gray-600 dark:text-gray-400">جاري التحليل باستخدام الذكاء الاصطناعي...</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dark mode setup
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            if (event.matches) {
                document.documentElement.classList.add('dark');
            } else {
                document.documentElement.classList.remove('dark');
            }
        });

        // Global variables
        let currentProfileData = {};
        let currentResults = {};

        // Form handling
        document.getElementById('profileForm').addEventListener('submit', function(e) {
            e.preventDefault();
            evaluateProfile();
        });

        // Modal handlers
        document.getElementById('skillsTestBtn').addEventListener('click', openSkillsTest);
        document.getElementById('aiAnalysisBtn').addEventListener('click', openAiAnalysis);
        document.getElementById('closeTestModal').addEventListener('click', () => {
            document.getElementById('skillsTestModal').classList.add('hidden');
        });
        document.getElementById('closeAiModal').addEventListener('click', () => {
            document.getElementById('aiAnalysisModal').classList.add('hidden');
        });

        // Action button handlers
        document.getElementById('exportBtn').addEventListener('click', exportReport);
        document.getElementById('shareBtn').addEventListener('click', shareResults);
        document.getElementById('retakeBtn').addEventListener('click', retakeAssessment);

        function evaluateProfile() {
            const formData = new FormData(document.getElementById('profileForm'));
            const form = Object.fromEntries(formData);

            // Calculate readiness score
            let score = 0;
            
            // Experience weight (0-30 points)
            const experience = parseInt(form.experience) || 0;
            score += Math.min(30, experience * 3);

            // Education level weight (0-20 points)
            const levelScores = {
                'دبلوم': 10,
                'بكالوريوس': 15,
                'ماجستير': 18,
                'دكتوراه': 20,
                'زمالة': 20
            };
            score += levelScores[form.level] || 0;

            // Skills weight (0-25 points)
            const skillsLength = form.skills.length;
            score += Math.min(25, Math.floor(skillsLength / 10));

            // AI Knowledge weight (0-25 points)
            const aiLength = form.aiKnowledge.length;
            score += Math.min(25, Math.floor(aiLength / 8));

            // Cap at 100
            score = Math.min(100, score);

            // Generate recommendations and strengths
            const { recommendations, strengths } = generateRecommendations(form, experience, score);

            // Store results globally
            currentResults = { score, recommendations, strengths, form };
            currentProfileData = form;

            // Display results
            displayResults(score, recommendations, strengths);
        }

        function openSkillsTest() {
            const modal = document.getElementById('skillsTestModal');
            modal.classList.remove('hidden');
            
            const testContent = document.getElementById('testContent');
            testContent.innerHTML = generateSkillsTest();
        }

        function generateSkillsTest() {
            const questions = [
                {
                    question: "ما هو المعدل الطبيعي لضغط الدم أثناء التخدير العام؟",
                    options: ["80-120/50-80 mmHg", "90-140/60-90 mmHg", "100-160/70-100 mmHg", "70-110/40-70 mmHg"],
                    correct: 1,
                    category: "أساسيات"
                },
                {
                    question: "أي من هذه التقنيات تُستخدم في التخدير الذكي؟",
                    options: ["أجهزة الاستشعار الذكية", "خوارزميات التنبؤ", "أنظمة دعم القرار", "جميع ما سبق"],
                    correct: 3,
                    category: "تقنيات حديثة"
                },
                {
                    question: "ما هي أهمية مراقبة BIS في التخدير؟",
                    options: ["قياس عمق التخدير", "مراقبة ضغط الدم", "قياس الأكسجين", "مراقبة النبض"],
                    correct: 0,
                    category: "مراقبة متقدمة"
                }
            ];

            let html = '<div class="space-y-6">';
            questions.forEach((q, index) => {
                html += `
                    <div class="border border-gray-200 dark:border-gray-600 rounded-lg p-4">
                        <div class="mb-2">
                            <span class="inline-block bg-primary text-white text-xs px-2 py-1 rounded">${q.category}</span>
                        </div>
                        <h4 class="font-medium mb-3">${index + 1}. ${q.question}</h4>
                        <div class="space-y-2">
                            ${q.options.map((option, optIndex) => `
                                <label class="flex items-center cursor-pointer">
                                    <input type="radio" name="q${index}" value="${optIndex}" class="ml-2">
                                    <span>${option}</span>
                                </label>
                            `).join('')}
                        </div>
                    </div>
                `;
            });
            html += `
                <div class="text-center">
                    <button onclick="submitSkillsTest()" class="bg-primary hover:bg-primary/90 text-white px-6 py-2 rounded-lg">
                        إرسال الإجابات
                    </button>
                </div>
            </div>`;
            return html;
        }

        function submitSkillsTest() {
            // Calculate test score and show results
            const correctAnswers = [1, 3, 0];
            let score = 0;
            correctAnswers.forEach((correct, index) => {
                const selected = document.querySelector(`input[name="q${index}"]:checked`);
                if (selected && parseInt(selected.value) === correct) {
                    score++;
                }
            });
            
            const percentage = Math.round((score / correctAnswers.length) * 100);
            document.getElementById('testContent').innerHTML = `
                <div class="text-center py-8">
                    <div class="text-6xl mb-4">${percentage >= 70 ? '🎉' : percentage >= 50 ? '👍' : '📚'}</div>
                    <h3 class="text-2xl font-bold mb-2">نتيجة الاختبار: ${percentage}%</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">
                        ${percentage >= 70 ? 'ممتاز! لديك معرفة قوية' : 
                          percentage >= 50 ? 'جيد، يمكن التحسين' : 
                          'يحتاج المزيد من التعلم'}
                    </p>
                    <p class="text-sm">إجاباتك الصحيحة: ${score} من ${correctAnswers.length}</p>
                </div>
            `;
        }

        async function openAiAnalysis() {
            const modal = document.getElementById('aiAnalysisModal');
            modal.classList.remove('hidden');
            
            if (!currentProfileData.name) {
                document.getElementById('aiAnalysisContent').innerHTML = `
                    <div class="text-center py-8">
                        <p class="text-red-600 dark:text-red-400">يرجى إكمال التقييم الأساسي أولاً</p>
                    </div>
                `;
                return;
            }

            try {
                // Register handler for AI response
                if (window.Poe && window.Poe.registerHandler) {
                    window.Poe.registerHandler("ai-analysis-handler", (result) => {
                        const msg = result.responses[0];
                        const aiContent = document.getElementById('aiAnalysisContent');
                        
                        if (msg.status === "error") {
                            aiContent.innerHTML = `
                                <div class="text-center py-8">
                                    <p class="text-red-600 dark:text-red-400">حدث خطأ في التحليل: ${msg.statusText}</p>
                                </div>
                            `;
                        } else if (msg.status === "incomplete") {
                            aiContent.innerHTML = `
                                <div class="prose dark:prose-invert max-w-none">
                                    ${msg.content.replace(/\n/g, '<br>')}
                                    <div class="inline-block animate-pulse">...</div>
                                </div>
                            `;
                        } else if (msg.status === "complete") {
                            aiContent.innerHTML = `
                                <div class="prose dark:prose-invert max-w-none">
                                    ${msg.content.replace(/\n/g, '<br>')}
                                </div>
                            `;
                        }
                    });

                    // Send analysis request
                    const prompt = `@Claude-3.7-Sonnet قم بتحليل ملف متخصص التخدير التالي وقدم توصيات مفصلة ومخصصة:

الاسم: ${currentProfileData.name}
الوظيفة: ${currentProfileData.role}
المستوى العلمي: ${currentProfileData.level}
سنوات الخبرة: ${currentProfileData.experience}
المهارات: ${currentProfileData.skills}
معرفة الذكاء الاصطناعي: ${currentProfileData.aiKnowledge}
النتيجة الحالية: ${currentResults.score}%

يرجى تقديم:
1. تحليل شامل للقوة والضعف
2. توصيات مفصلة للتطوير المهني
3. مسار تعليمي مقترح للسنوات القادمة
4. أحدث التقنيات في مجال التخدير التي يجب تعلمها
5. نصائح عملية لتطبيق الذكاء الاصطناعي في التخدير

اكتب بالعربية وكن محدداً ومفصلاً.`;

                    await window.Poe.sendUserMessage(prompt, {
                        handler: "ai-analysis-handler",
                        stream: true,
                        openChat: false
                    });
                } else {
                    // Fallback if Poe API not available
                    document.getElementById('aiAnalysisContent').innerHTML = `
                        <div class="space-y-4">
                            <div class="bg-blue-50 dark:bg-blue-900/20 p-4 rounded-lg">
                                <h4 class="font-bold mb-2">🔍 تحليل متقدم للملف الشخصي</h4>
                                <p>بناءً على المعلومات المقدمة، نوصي بالتركيز على تطوير المهارات التقنية المتقدمة.</p>
                            </div>
                            <div class="bg-yellow-50 dark:bg-yellow-900/20 p-4 rounded-lg">
                                <h4 class="font-bold mb-2">💡 توصيات مخصصة</h4>
                                <p>للحصول على تحليل مفصل، يمكنك استخدام ميزة الذكاء الاصطناعي المتكاملة.</p>
                            </div>
                        </div>
                    `;
                }
            } catch (error) {
                document.getElementById('aiAnalysisContent').innerHTML = `
                    <div class="text-center py-8">
                        <p class="text-red-600 dark:text-red-400">خطأ في الاتصال: ${error.message}</p>
                    </div>
                `;
            }
        }

        function exportReport() {
            const reportData = generateReportHTML();
            const blob = new Blob([reportData], { type: 'text/html;charset=utf-8' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `تقرير_التقييم_${currentProfileData.name || 'متخصص_التخدير'}.html`;
            a.click();
            URL.revokeObjectURL(url);
        }

        function generateReportHTML() {
            return `
                <!DOCTYPE html>
                <html dir="rtl" lang="ar">
                <head>
                    <meta charset="UTF-8">
                    <title>تقرير تقييم متخصص التخدير</title>
                    <style>
                        body { font-family: Arial, sans-serif; direction: rtl; margin: 20px; }
                        .header { text-align: center; border-bottom: 2px solid #5D5CDE; padding-bottom: 20px; }
                        .section { margin: 20px 0; padding: 15px; border: 1px solid #ddd; border-radius: 8px; }
                        .score { font-size: 24px; color: #5D5CDE; font-weight: bold; }
                    </style>
                </head>
                <body>
                    <div class="header">
                        <h1>تقرير تقييم متخصص التخدير</h1>
                        <p>الاسم: ${currentProfileData.name}</p>
                        <p>التاريخ: ${new Date().toLocaleDateString('ar-SA')}</p>
                    </div>
                    
                    <div class="section">
                        <h2>نتيجة التقييم</h2>
                        <p class="score">مؤشر الجاهزية: ${currentResults.score}%</p>
                    </div>
                    
                    <div class="section">
                        <h2>التوصيات</h2>
                        <ul>
                            ${currentResults.recommendations.map(rec => `<li>${rec.text}</li>`).join('')}
                        </ul>
                    </div>
                    
                    <div class="section">
                        <h2>نقاط القوة</h2>
                        <ul>
                            ${currentResults.strengths.map(strength => `<li>${strength.text}</li>`).join('')}
                        </ul>
                    </div>
                </body>
                </html>
            `;
        }

        function shareResults() {
            if (navigator.share) {
                navigator.share({
                    title: 'نتيجة تقييم متخصص التخدير',
                    text: `حصلت على ${currentResults.score}% في تقييم جاهزية متخصص التخدير للمستقبل!`,
                    url: window.location.href
                });
            } else {
                // Fallback for browsers that don't support Web Share API
                const shareText = `حصلت على ${currentResults.score}% في تقييم جاهزية متخصص التخدير للمستقبل!`;
                if (navigator.clipboard) {
                    navigator.clipboard.writeText(shareText);
                    alert('تم نسخ النتيجة للحافظة!');
                } else {
                    alert('مشاركة: ' + shareText);
                }
            }
        }

        function retakeAssessment() {
            if (confirm('هل تريد إعادة التقييم؟ سيتم مسح النتائج الحالية.')) {
                document.getElementById('profileForm').reset();
                document.getElementById('results').classList.add('hidden');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }
        }

        function generateRecommendations(form, experience, score) {
            const recommendations = [];
            const strengths = [];

            // Check for AI knowledge
            if (!form.aiKnowledge.toLowerCase().includes('ذكاء') && !form.aiKnowledge.toLowerCase().includes('ai')) {
                recommendations.push({
                    icon: '🤖',
                    text: 'ابدأ بتعلم أساسيات الذكاء الاصطناعي وتطبيقاته في التخدير',
                    priority: 'high'
                });
            } else {
                strengths.push({
                    icon: '🤖',
                    text: 'لديك معرفة جيدة بالذكاء الاصطناعي'
                });
            }

            // Check for monitoring skills
            if (!form.skills.toLowerCase().includes('مراقبة') && !form.skills.toLowerCase().includes('monitoring')) {
                recommendations.push({
                    icon: '📊',
                    text: 'طوّر مهاراتك في أجهزة المراقبة المتقدمة والتحليل الآني للمؤشرات الحيوية',
                    priority: 'medium'
                });
            } else {
                strengths.push({
                    icon: '📊',
                    text: 'تمتلك خبرة في أجهزة المراقبة'
                });
            }

            // Check for simulation skills
            if (!form.skills.toLowerCase().includes('محاكاة') && !form.skills.toLowerCase().includes('simulation')) {
                recommendations.push({
                    icon: '🎮',
                    text: 'اكتسب خبرة في المحاكاة السريرية والتدريب الافتراضي',
                    priority: 'medium'
                });
            } else {
                strengths.push({
                    icon: '🎮',
                    text: 'لديك خبرة في المحاكاة السريرية'
                });
            }

            // Experience-based recommendations
            if (experience < 2) {
                recommendations.push({
                    icon: '⏰',
                    text: 'اكتسب خبرة عملية إضافية تحت إشراف أطباء خبراء',
                    priority: 'high'
                });
            } else if (experience >= 5) {
                strengths.push({
                    icon: '⏰',
                    text: 'تمتلك خبرة عملية قوية في مجال التخدير'
                });
            }

            // Role-specific recommendations
            if (form.role === 'طبيب تخدير' && score < 70) {
                recommendations.push({
                    icon: '🩺',
                    text: 'شارك في مؤتمرات التخدير الدولية واحصل على شهادات متقدمة',
                    priority: 'medium'
                });
            }

            // Add general recommendations based on score
            if (score < 50) {
                recommendations.push({
                    icon: '📚',
                    text: 'ادرس أحدث المراجع في تخدير المستقبل والطب الشخصي',
                    priority: 'high'
                });
            }

            if (score >= 70) {
                strengths.push({
                    icon: '🌟',
                    text: 'تُظهر مستوى متقدم من المعرفة والمهارات'
                });
            }

            if (experience >= 3 && form.skills.length > 50) {
                strengths.push({
                    icon: '💼',
                    text: 'تمتلك تنوعاً جيداً في المهارات المهنية'
                });
            }

            return { recommendations, strengths };
        }

        function displayResults(score, recommendations, strengths) {
            // Show results section
            const resultsSection = document.getElementById('results');
            resultsSection.classList.remove('hidden');
            resultsSection.scrollIntoView({ behavior: 'smooth' });

            // Update score
            const scoreElement = document.getElementById('readinessScore');
            const progressCircle = document.getElementById('progressCircle');
            const readinessLevel = document.getElementById('readinessLevel');

            // Animate score
            let currentScore = 0;
            const increment = score / 50;
            const timer = setInterval(() => {
                currentScore += increment;
                if (currentScore >= score) {
                    currentScore = score;
                    clearInterval(timer);
                }
                scoreElement.textContent = Math.round(currentScore) + '%';
                
                // Update progress circle
                const circumference = 2 * Math.PI * 40;
                const offset = circumference - (currentScore / 100) * circumference;
                progressCircle.style.strokeDashoffset = offset;
            }, 20);

            // Set readiness level
            if (score >= 80) {
                readinessLevel.textContent = 'ممتاز - جاهز للمستقبل';
                readinessLevel.className = 'text-sm text-green-600 dark:text-green-400';
            } else if (score >= 60) {
                readinessLevel.textContent = 'جيد - يحتاج تطوير بسيط';
                readinessLevel.className = 'text-sm text-blue-600 dark:text-blue-400';
            } else if (score >= 40) {
                readinessLevel.textContent = 'متوسط - يحتاج تطوير متوسط';
                readinessLevel.className = 'text-sm text-yellow-600 dark:text-yellow-400';
            } else {
                readinessLevel.textContent = 'ضعيف - يحتاج تطوير كبير';
                readinessLevel.className = 'text-sm text-red-600 dark:text-red-400';
            }

            // Display recommendations
            const recommendationsList = document.getElementById('recommendationsList');
            recommendationsList.innerHTML = '';
            recommendations.forEach(rec => {
                const div = document.createElement('div');
                div.className = `p-4 rounded-lg border-r-4 ${
                    rec.priority === 'high' ? 'border-red-500 bg-red-50 dark:bg-red-900/20' :
                    rec.priority === 'medium' ? 'border-yellow-500 bg-yellow-50 dark:bg-yellow-900/20' :
                    'border-blue-500 bg-blue-50 dark:bg-blue-900/20'
                }`;
                div.innerHTML = `
                    <div class="flex items-start">
                        <span class="text-2xl ml-3">${rec.icon}</span>
                        <p class="text-sm">${rec.text}</p>
                    </div>
                `;
                recommendationsList.appendChild(div);
            });

            // Display strengths
            const strengthsList = document.getElementById('strengthsList');
            strengthsList.innerHTML = '';
            strengths.forEach(strength => {
                const div = document.createElement('div');
                div.className = 'p-4 rounded-lg border-r-4 border-green-500 bg-green-50 dark:bg-green-900/20';
                div.innerHTML = `
                    <div class="flex items-start">
                        <span class="text-2xl ml-3">${strength.icon}</span>
                        <p class="text-sm">${strength.text}</p>
                    </div>
                `;
                strengthsList.appendChild(div);
            });

            // Display skills map
            displaySkillsMap(score);

            // Display achievement badges
            displayAchievementBadges(score, experience, form);

            // Display learning path
            displayLearningPath(recommendations);
        }

        function displaySkillsMap(score) {
            const skillsMap = document.getElementById('skillsMap');
            const skills = [
                { name: 'أساسيات التخدير', level: Math.min(100, score + 10), icon: '💊' },
                { name: 'أجهزة المراقبة', level: Math.min(100, score - 5), icon: '📊' },
                { name: 'الذكاء الاصطناعي', level: Math.max(0, score - 20), icon: '🤖' },
                { name: 'إدارة الطوارئ', level: Math.min(100, score + 5), icon: '🚨' },
                { name: 'المحاكاة السريرية', level: Math.max(0, score - 15), icon: '🎮' },
                { name: 'البحث العلمي', level: Math.max(0, score - 25), icon: '🔬' },
                { name: 'التواصل', level: Math.min(100, score + 15), icon: '💬' },
                { name: 'القيادة', level: Math.max(0, score - 10), icon: '👑' }
            ];

            skillsMap.innerHTML = '';
            skills.forEach(skill => {
                const div = document.createElement('div');
                div.className = 'bg-white dark:bg-gray-700 p-3 rounded-lg text-center border border-gray-200 dark:border-gray-600';
                div.innerHTML = `
                    <div class="text-2xl mb-2">${skill.icon}</div>
                    <div class="text-xs font-medium mb-2">${skill.name}</div>
                    <div class="w-full bg-gray-200 dark:bg-gray-600 rounded-full h-2 mb-1">
                        <div class="bg-primary h-2 rounded-full transition-all duration-1000" style="width: ${skill.level}%"></div>
                    </div>
                    <div class="text-xs text-gray-600 dark:text-gray-400">${skill.level}%</div>
                `;
                skillsMap.appendChild(div);
            });
        }

        function displayAchievementBadges(score, experience, form) {
            const badgesList = document.getElementById('badgesList');
            const badges = [];

            // Score-based badges
            if (score >= 90) badges.push({ name: 'خبير متقدم', icon: '🏆', color: 'gold' });
            if (score >= 70) badges.push({ name: 'محترف معتمد', icon: '🥇', color: 'silver' });
            if (score >= 50) badges.push({ name: 'متخصص نشط', icon: '🥈', color: 'bronze' });

            // Experience-based badges
            if (experience >= 10) badges.push({ name: 'خبير عميق', icon: '🎖️', color: 'purple' });
            if (experience >= 5) badges.push({ name: 'ممارس خبير', icon: '⭐', color: 'blue' });

            // Skill-based badges
            if (form.aiKnowledge.length > 50) badges.push({ name: 'رائد الذكاء الاصطناعي', icon: '🤖', color: 'green' });
            if (form.skills.includes('محاكاة')) badges.push({ name: 'محاكي متقدم', icon: '🎮', color: 'orange' });

            badgesList.innerHTML = '';
            badges.forEach(badge => {
                const div = document.createElement('div');
                div.className = `bg-gradient-to-br from-${badge.color}-400 to-${badge.color}-600 text-white p-4 rounded-lg text-center shadow-lg transform hover:scale-105 transition-transform duration-200`;
                div.innerHTML = `
                    <div class="text-3xl mb-2">${badge.icon}</div>
                    <div class="text-sm font-bold">${badge.name}</div>
                `;
                badgesList.appendChild(div);
            });
        }

        function displayLearningPath(recommendations) {
            const learningPath = document.getElementById('learningPath');
            const pathSteps = [
                { title: 'المرحلة الأولى: الأساسيات', duration: '1-3 أشهر', items: ['مراجعة أساسيات التخدير', 'تعلم أجهزة المراقبة الحديثة'] },
                { title: 'المرحلة الثانية: التقنيات المتقدمة', duration: '3-6 أشهر', items: ['دراسة الذكاء الاصطناعي الطبي', 'تطبيق المحاكاة السريرية'] },
                { title: 'المرحلة الثالثة: التخصص', duration: '6-12 شهر', items: ['تطوير مهارات البحث', 'القيادة والإدارة السريرية'] }
            ];

            learningPath.innerHTML = '';
            pathSteps.forEach((step, index) => {
                const div = document.createElement('div');
                div.className = 'flex items-start';
                div.innerHTML = `
                    <div class="flex-shrink-0 w-8 h-8 bg-primary text-white rounded-full flex items-center justify-center text-sm font-bold ml-4">
                        ${index + 1}
                    </div>
                    <div class="flex-grow">
                        <h4 class="font-semibold text-lg">${step.title}</h4>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-2">المدة المقترحة: ${step.duration}</p>
                        <ul class="text-sm space-y-1">
                            ${step.items.map(item => `<li class="flex items-center"><span class="text-green-500 ml-2">✓</span>${item}</li>`).join('')}
                        </ul>
                    </div>
                `;
                learningPath.appendChild(div);
            });
        }
    </script>
</body>
</html>
