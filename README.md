# chemistry-test-for-high-school-students.
مراجعة عامة للمادة وخواصها للثانوي
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بنك أسئلة الكيمياء التفاعلي</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #3498db;
            --primary-dark: #2980b9;
            --secondary: #2c3e50;
            --success: #2ecc71;
            --success-dark: #27ae60;
            --danger: #e74c3c;
            --warning: #f39c12;
            --light: #ecf0f1;
            --dark: #34495e;
            --purple: #9b59b6;
            --teal: #1abc9c;
            --orange: #e67e22;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .container {
            max-width: 900px;
            width: 100%;
            background-color: white;
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            position: relative;
        }
        
        header {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 30px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,186.7C384,213,480,235,576,213.3C672,192,768,128,864,128C960,128,1056,192,1152,192C1248,192,1344,128,1392,96L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            background-size: cover;
            background-position: center;
        }
        
        header h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            position: relative;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
        }
        
        header p {
            font-size: 1.1rem;
            opacity: 0.9;
            position: relative;
        }
        
        .progress-container {
            background-color: var(--light);
            height: 12px;
            width: 100%;
            border-radius: 0 0 10px 10px;
            overflow: hidden;
        }
        
        .progress-bar {
            background: linear-gradient(to right, var(--teal), var(--primary));
            height: 100%;
            width: 0%;
            transition: width 0.5s ease;
            border-radius: 0 0 10px 10px;
        }
        
        .info-container {
            padding: 25px;
            background-color: rgba(52, 152, 219, 0.05);
            border-bottom: 1px solid rgba(0,0,0,0.1);
        }
        
        .info-form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        .form-group label {
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--secondary);
        }
        
        .form-group input, .form-group select {
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus, .form-group select:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 2px rgba(52, 152, 219, 0.2);
        }
        
        .start-btn {
            background: linear-gradient(135deg, var(--success), var(--success-dark));
            color: white;
            border: none;
            padding: 14px 25px;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            box-shadow: 0 4px 10px rgba(46, 204, 113, 0.3);
            margin-top: 10px;
            grid-column: 1 / -1;
        }
        
        .start-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(46, 204, 113, 0.4);
        }
        
        .quiz-container {
            padding: 35px;
            position: relative;
            display: none;
        }
        
        .question-number {
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 8px;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .question-number i {
            color: var(--purple);
        }
        
        .question-text {
            font-size: 1.3rem;
            margin-bottom: 25px;
            font-weight: 600;
            color: var(--secondary);
            line-height: 1.5;
            padding: 15px;
            background-color: rgba(52, 152, 219, 0.05);
            border-radius: 10px;
            border-right: 4px solid var(--primary);
        }
        
        .options-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 30px;
        }
        
        .option {
            background-color: var(--light);
            border: 2px solid transparent;
            border-radius: 12px;
            padding: 18px 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
        }
        
        .option:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .option.selected {
            border-color: var(--primary);
            background: linear-gradient(to right, rgba(52, 152, 219, 0.1), rgba(52, 152, 219, 0.05));
        }
        
        .option.correct {
            border-color: var(--success);
            background: linear-gradient(to right, rgba(46, 204, 113, 0.1), rgba(46, 204, 113, 0.05));
        }
        
        .option.incorrect {
            border-color: var(--danger);
            background: linear-gradient(to right, rgba(231, 76, 60, 0.1), rgba(231, 76, 60, 0.05));
        }
        
        .option input[type="radio"] {
            display: none;
        }
        
        .option-letter {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 36px;
            height: 36px;
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            border-radius: 50%;
            margin-left: 15px;
            font-weight: bold;
            font-size: 1.1rem;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
        }
        
        .option.correct .option-letter {
            background: linear-gradient(135deg, var(--success), var(--success-dark));
        }
        
        .option.incorrect .option-letter {
            background: linear-gradient(135deg, var(--danger), #c0392b);
        }
        
        .explanation {
            margin-top: 25px;
            padding: 20px;
            background-color: rgba(155, 89, 182, 0.05);
            border-radius: 10px;
            border-right: 4px solid var(--purple);
            display: none;
        }
        
        .explanation-title {
            font-weight: bold;
            color: var(--purple);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .explanation-text {
            line-height: 1.6;
        }
        
        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 25px;
        }
        
        button {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            border: none;
            padding: 14px 28px;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 4px 10px rgba(52, 152, 219, 0.3);
        }
        
        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(52, 152, 219, 0.4);
        }
        
        button:active {
            transform: translateY(-1px);
        }
        
        button:disabled {
            background: #bdc3c7;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }
        
        #submit-btn {
            background: linear-gradient(135deg, var(--success), var(--success-dark));
            box-shadow: 0 4px 10px rgba(46, 204, 113, 0.3);
        }
        
        #submit-btn:hover {
            box-shadow: 0 6px 15px rgba(46, 204, 113, 0.4);
        }
        
        .result-container {
            text-align: center;
            padding: 50px 30px;
            display: none;
        }
        
        .result-title {
            font-size: 2.5rem;
            margin-bottom: 25px;
            color: var(--secondary);
            position: relative;
            display: inline-block;
        }
        
        .result-title::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--teal));
            border-radius: 2px;
        }
        
        .student-info {
            background-color: rgba(52, 152, 219, 0.1);
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 30px;
            text-align: right;
        }
        
        .student-info h3 {
            color: var(--primary);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: flex-end;
            gap: 10px;
        }
        
        .student-details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }
        
        .student-detail {
            text-align: right;
        }
        
        .student-detail span:first-child {
            font-weight: bold;
            color: var(--secondary);
        }
        
        .score-container {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            width: 200px;
            height: 200px;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            margin: 30px auto;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .score-container::before {
            content: "";
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            background: linear-gradient(135deg, rgba(255,255,255,0.1), rgba(255,255,255,0));
            border-radius: 50%;
            z-index: 0;
        }
        
        .score {
            font-size: 4.5rem;
            font-weight: bold;
            line-height: 1;
            position: relative;
            z-index: 1;
        }
        
        .score-text {
            font-size: 1.2rem;
            position: relative;
            z-index: 1;
        }
        
        .score-details {
            font-size: 1.3rem;
            margin-bottom: 30px;
            color: var(--secondary);
        }
        
        .restart-btn {
            background: linear-gradient(135deg, var(--orange), #d35400);
            margin-top: 20px;
            padding: 16px 35px;
            font-size: 1.1rem;
            box-shadow: 0 4px 15px rgba(230, 126, 34, 0.3);
        }
        
        .restart-btn:hover {
            box-shadow: 0 6px 20px rgba(230, 126, 34, 0.4);
        }
        
        .feedback {
            margin-top: 20px;
            padding: 15px;
            border-radius: 10px;
            display: none;
            font-weight: 600;
            text-align: center;
        }
        
        .feedback.correct {
            background: linear-gradient(to right, rgba(46, 204, 113, 0.1), rgba(46, 204, 113, 0.05));
            color: var(--success);
            border: 1px solid var(--success);
        }
        
        .feedback.incorrect {
            background: linear-gradient(to right, rgba(231, 76, 60, 0.1), rgba(231, 76, 60, 0.05));
            color: var(--danger);
            border: 1px solid var(--danger);
        }
        
        .floating-elements {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }
        
        .floating-element {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }
        
        @media (max-width: 768px) {
            .container {
                border-radius: 15px;
            }
            
            header {
                padding: 25px 15px;
            }
            
            header h1 {
                font-size: 1.8rem;
            }
            
            .info-form {
                grid-template-columns: 1fr;
            }
            
            .quiz-container {
                padding: 25px 15px;
            }
            
            .question-text {
                font-size: 1.2rem;
            }
            
            .navigation {
                flex-direction: column;
                gap: 12px;
            }
            
            button {
                width: 100%;
                justify-content: center;
            }
            
            .score-container {
                width: 170px;
                height: 170px;
            }
            
            .score {
                font-size: 3.8rem;
            }
            
            .student-details {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>بنك أسئلة الكيمياء التفاعلي</h1>
            <p>اختبار إلكتروني شامل لطلاب الثانوية العامة</p>
        </header>
        
        <div class="info-container" id="info-container">
            <h2 style="text-align: center; margin-bottom: 20px; color: var(--secondary);">معلومات الطالب</h2>
            <div class="info-form">
                <div class="form-group">
                    <label for="student-name">الاسم الثلاثي</label>
                    <input type="text" id="student-name" placeholder="أدخل اسمك الثلاثي">
                </div>
                <div class="form-group">
                    <label for="student-class">الشعبة</label>
                    <select id="student-class">
                        <option value="">اختر الشعبة</option>
                        <option value="علمي">علمي</option>
                        <option value="أدبي">أدبي</option>
                        <option value="مختلط">مختلط</option>
                    </select>
                </div>
                <button class="start-btn" id="start-btn">
                    <i class="fas fa-play-circle"></i>
                    بدء الاختبار
                </button>
            </div>
        </div>
        
        <div class="progress-container">
            <div class="progress-bar" id="progress-bar"></div>
        </div>
        
        <div class="quiz-container" id="quiz-container">
            <div class="floating-elements" id="floating-elements"></div>
            
            <div class="question-number">
                <i class="fas fa-question-circle"></i>
                <span id="question-number">السؤال 1 من 50</span>
            </div>
            <div class="question-text" id="question-text"></div>
            
            <div class="options-container" id="options-container">
                <!-- سيتم ملء الخيارات ديناميكيًا -->
            </div>
            
            <div class="explanation" id="explanation">
                <div class="explanation-title">
                    <i class="fas fa-lightbulb"></i>
                    شرح السؤال
                </div>
                <div class="explanation-text" id="explanation-text"></div>
            </div>
            
            <div class="feedback" id="feedback"></div>
            
            <div class="navigation">
                <button id="prev-btn" disabled>
                    <i class="fas fa-arrow-right"></i>
                    السابق
                </button>
                <button id="next-btn">
                    التالي
                    <i class="fas fa-arrow-left"></i>
                </button>
                <button id="submit-btn" style="display: none;">
                    إنهاء الاختبار
                    <i class="fas fa-paper-plane"></i>
                </button>
            </div>
        </div>
        
        <div class="result-container" id="result-container">
            <h2 class="result-title">نتيجة الاختبار</h2>
            
            <div class="student-info">
                <h3><i class="fas fa-user-graduate"></i> معلومات الطالب</h3>
                <div class="student-details">
                    <div class="student-detail">
                        <span>الاسم: </span>
                        <span id="result-name"></span>
                    </div>
                    <div class="student-detail">
                        <span>الشعبة: </span>
                        <span id="result-class"></span>
                    </div>
                </div>
            </div>
            
            <div class="score-container">
                <div class="score" id="score">0/50</div>
                <div class="score-text">درجة</div>
            </div>
            
            <p class="score-details" id="score-details"></p>
            <p class="score-text" id="score-text"></p>
            
            <button class="restart-btn" id="restart-btn">
                <i class="fas fa-redo"></i>
                إعادة الاختبار
            </button>
        </div>
    </div>

    <script>
        // بيانات الأسئلة مع الإجابات الصحيحة والشروح
        const questionsData = [
            {
                question: "أي مما يلي يُعدّ من حالات المادة الأساسية؟",
                options: ["البلازما", "الصلبة", "الغروية"],
                correctAnswer: 1,
                explanation: "حالات المادة الأساسية هي الصلبة، السائلة، والغازية. البلازما تعتبر حالة رابعة للمادة ولكنها ليست أساسية بنفس درجة الحالات الثلاث الأولى."
            },
            {
                question: "أي خاصية تُميز المادة الصلبة؟",
                options: ["ليس لها حجم ثابت", "لها شكل ثابت", "تنضغط بسهولة"],
                correctAnswer: 1,
                explanation: "المادة الصلبة لها شكل ثابت وحجم ثابت بسبب ترتيب جزيئاتها المنتظم وقوى التماسك القوية بينها."
            },
            {
                question: "أي مما يلي يُعدّ من خصائص السوائل؟",
                options: ["شكل ثابت", "حجم ثابت", "يمكن ضغطها بشدة"],
                correctAnswer: 1,
                explanation: "السوائل لها حجم ثابت ولكن ليس لها شكل ثابت، فهي تأخذ شكل الإناء الذي توضع فيه. كما أن السوائل غير قابلة للانضغاط بشكل كبير."
            },
            {
                question: "الغازات تتميز بأنها؟",
                options: ["لها شكل وحجم ثابت", "ليس لها شكل أو حجم ثابت", "لا تتحرك جسيماتها"],
                correctAnswer: 1,
                explanation: "الغازات ليس لها شكل ثابت ولا حجم ثابت، فهي تملأ الوعاء الذي توجد فيه تماماً. جسيمات الغازات في حركة دائمة وعشوائية."
            },
            {
                question: "أي مما يلي مثال على بخار؟",
                options: ["بخار الماء", "غاز الأكسجين", "غاز ثاني أكسيد الكربون"],
                correctAnswer: 0,
                explanation: "البخار هو الحالة الغازية للمادة عندما تكون في درجة حرارة أقل من نقطة الحرجة. بخار الماء هو المثال الأكثر شيوعاً للبخار."
            }
            // يمكن إضافة المزيد من الأسئلة هنا...
        ];

        // متغيرات التطبيق
        let questions = [];
        let currentQuestion = 0;
        let userAnswers = [];
        let score = 0;
        let studentName = "";
        let studentClass = "";

        // عناصر DOM
        const infoContainer = document.getElementById('info-container');
        const startButton = document.getElementById('start-btn');
        const quizContainer = document.getElementById('quiz-container');
        const questionNumberElement = document.getElementById('question-number');
        const questionTextElement = document.getElementById('question-text');
        const optionsContainer = document.getElementById('options-container');
        const explanationElement = document.getElementById('explanation');
        const explanationTextElement = document.getElementById('explanation-text');
        const feedbackElement = document.getElementById('feedback');
        const prevButton = document.getElementById('prev-btn');
        const nextButton = document.getElementById('next-btn');
        const submitButton = document.getElementById('submit-btn');
        const progressBar = document.getElementById('progress-bar');
        const resultContainer = document.getElementById('result-container');
        const resultNameElement = document.getElementById('result-name');
        const resultClassElement = document.getElementById('result-class');
        const scoreElement = document.getElementById('score');
        const scoreTextElement = document.getElementById('score-text');
        const scoreDetailsElement = document.getElementById('score-details');
        const restartButton = document.getElementById('restart-btn');
        const floatingElementsContainer = document.getElementById('floating-elements');

        // تهيئة التطبيق
        function init() {
            // إظهار واجهة إدخال البيانات فقط
            infoContainer.style.display = 'block';
            quizContainer.style.display = 'none';
            resultContainer.style.display = 'none';
            
            // إعادة تعيين المتغيرات
            shuffleQuestions();
            userAnswers = new Array(questions.length).fill(null);
            currentQuestion = 0;
            score = 0;
            
            createFloatingElements();
        }

        // إعادة ترتيب الأسئلة عشوائيًا
        function shuffleQuestions() {
            questions = [...questionsData];
            for (let i = questions.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [questions[i], questions[j]] = [questions[j], questions[i]];
            }
        }

        // إنشاء عناصر عائمة للخلفية
        function createFloatingElements() {
            floatingElementsContainer.innerHTML = '';
            for (let i = 0; i < 15; i++) {
                const element = document.createElement('div');
                element.classList.add('floating-element');
                const size = Math.random() * 30 + 10;
                element.style.width = `${size}px`;
                element.style.height = `${size}px`;
                element.style.top = `${Math.random() * 100}%`;
                element.style.left = `${Math.random() * 100}%`;
                element.style.animation = `float ${Math.random() * 10 + 10}s infinite ease-in-out`;
                element.style.animationDelay = `${Math.random() * 5}s`;
                floatingElementsContainer.appendChild(element);
            }
            
            // إضافة أنيميشن للعناصر العائمة
            const style = document.createElement('style');
            style.textContent = `
                @keyframes float {
                    0%, 100% { transform: translate(0, 0) rotate(0deg); }
                    25% { transform: translate(${Math.random() * 20 - 10}px, ${Math.random() * 20 - 10}px) rotate(5deg); }
                    50% { transform: translate(${Math.random() * 30 - 15}px, ${Math.random() * 30 - 15}px) rotate(-5deg); }
                    75% { transform: translate(${Math.random() * 20 - 10}px, ${Math.random() * 20 - 10}px) rotate(5deg); }
                }
            `;
            document.head.appendChild(style);
        }

        // بدء الاختبار
        function startQuiz() {
            studentName = document.getElementById('student-name').value.trim();
            studentClass = document.getElementById('student-class').value;
            
            if (!studentName || !studentClass) {
                alert("يرجى ملء جميع الحقول قبل بدء الاختبار");
                return;
            }
            
            infoContainer.style.display = 'none';
            quizContainer.style.display = 'block';
            resultContainer.style.display = 'none';
            
            showQuestion();
            updateProgressBar();
        }

        // عرض السؤال الحالي
        function showQuestion() {
            const question = questions[currentQuestion];
            
            // تحديث رقم السؤال
            questionNumberElement.textContent = `السؤال ${currentQuestion + 1} من ${questions.length}`;
            
            // تحديث نص السؤال
            questionTextElement.textContent = question.question;
            
            // مسح الخيارات السابقة
            optionsContainer.innerHTML = '';
            
            // إضافة الخيارات الجديدة
            question.options.forEach((option, index) => {
                const optionElement = document.createElement('div');
                optionElement.classList.add('option');
                
                // تحديد إذا كان الخيار مختارًا
                if (userAnswers[currentQuestion] === index) {
                    optionElement.classList.add('selected');
                }
                
                const radioId = `option-${currentQuestion}-${index}`;
                optionElement.innerHTML = `
                    <input type="radio" id="${radioId}" name="question-${currentQuestion}" value="${index}">
                    <label for="${radioId}">
                        ${option}
                        <span class="option-letter">${String.fromCharCode(65 + index)}</span>
                    </label>
                `;
                
                optionElement.addEventListener('click', () => selectOption(index));
                optionsContainer.appendChild(optionElement);
            });
            
            // تحديث الشرح
            explanationTextElement.textContent = question.explanation;
            explanationElement.style.display = 'block';
            
            // تحديث حالة الأزرار
            prevButton.disabled = currentQuestion === 0;
            nextButton.disabled = userAnswers[currentQuestion] === null;
            
            // إظهار زر إنهاء الاختبار في السؤال الأخير
            if (currentQuestion === questions.length - 1) {
                nextButton.style.display = 'none';
                submitButton.style.display = 'flex';
                submitButton.disabled = userAnswers[currentQuestion] === null;
            } else {
                nextButton.style.display = 'flex';
                submitButton.style.display = 'none';
            }
            
            // إخفاء التغذية الراجعة
            feedbackElement.style.display = 'none';
        }

        // اختيار خيار
        function selectOption(optionIndex) {
            // إلغاء تحديد جميع الخيارات
            document.querySelectorAll('.option').forEach(opt => {
                opt.classList.remove('selected');
            });
            
            // تحديد الخيار المختار
            userAnswers[currentQuestion] = optionIndex;
            document.querySelectorAll('.option')[optionIndex].classList.add('selected');
            
            // تحديث حالة الأزرار
            nextButton.disabled = false;
            if (currentQuestion === questions.length - 1) {
                submitButton.disabled = false;
            }
            
            // التحقق من الإجابة
            const question = questions[currentQuestion];
            const isCorrect = optionIndex === question.correctAnswer;
            
            // عرض التغذية الراجعة
            feedbackElement.textContent = isCorrect ? 
                "إجابة صحيحة! أحسنت!" : 
                "إجابة خاطئة. حاول مرة أخرى!";
            feedbackElement.className = `feedback ${isCorrect ? 'correct' : 'incorrect'}`;
            feedbackElement.style.display = 'block';
        }

        // الانتقال إلى السؤال التالي
        function nextQuestion() {
            if (currentQuestion < questions.length - 1) {
                currentQuestion++;
                showQuestion();
                updateProgressBar();
            }
        }

        // الانتقال إلى السؤال السابق
        function prevQuestion() {
            if (currentQuestion > 0) {
                currentQuestion--;
                showQuestion();
                updateProgressBar();
            }
        }

        // تحديث شريط التقدم
        function updateProgressBar() {
            const progress = ((currentQuestion + 1) / questions.length) * 100;
            progressBar.style.width = `${progress}%`;
        }

        // إنهاء الاختبار وعرض النتيجة
        function submitQuiz() {
            // حساب النتيجة النهائية
            let finalScore = 0;
            userAnswers.forEach((answer, index) => {
                if (answer === questions[index].correctAnswer) {
                    finalScore++;
                }
            });
            
            // عرض معلومات الطالب
            resultNameElement.textContent = studentName;
            resultClassElement.textContent = studentClass;
            
            // عرض النتيجة
            scoreElement.textContent = `${finalScore}/${questions.length}`;
            scoreDetailsElement.textContent = `أجبت بشكل صحيح على ${finalScore} من أصل ${questions.length} سؤال`;
            
            // نص النتيجة بناءً على الأداء
            let scoreText = "";
            const percentage = (finalScore / questions.length) * 100;
            
            if (percentage >= 90) {
                scoreText = "ممتاز! أداء رائع! أنت على مستوى عالٍ من المعرفة الكيميائية.";
            } else if (percentage >= 80) {
                scoreText = "جيد جداً! أحسنت! لديك فهم قوي للمفاهيم الكيميائية.";
            } else if (percentage >= 70) {
                scoreText = "جيد! يمكنك التحسين أكثر بمراجعة بعض النقاط.";
            } else if (percentage >= 60) {
                scoreText = "مقبول. تحتاج للمزيد من الدراسة والمراجعة.";
            } else {
                scoreText = "ضعيف. يجب مراجعة المادة مرة أخرى والتركيز على المفاهيم الأساسية.";
            }
            
            scoreTextElement.textContent = scoreText;
            
            // إخفاء واجهة الاختبار وإظهار النتيجة
            quizContainer.style.display = 'none';
            resultContainer.style.display = 'block';
        }

        // إعادة بدء الاختبار
        function restartQuiz() {
            // إعادة تعيين المتغيرات
            shuffleQuestions();
            userAnswers = new Array(questions.length).fill(null);
            currentQuestion = 0;
            score = 0;
            
            // إعادة تعيين الواجهة
            infoContainer.style.display = 'block';
            quizContainer.style.display = 'none';
            resultContainer.style.display = 'none';
            
            // إعادة تعيين النموذج
            document.getElementById('student-name').value = "";
            document.getElementById('student-class').value = "";
        }

        // إضافة مستمعي الأحداث
        startButton.addEventListener('click', startQuiz);
        nextButton.addEventListener('click', nextQuestion);
        prevButton.addEventListener('click', prevQuestion);
        submitButton.addEventListener('click', submitQuiz);
        restartButton.addEventListener('click', restartQuiz);

        // بدء التطبيق
        init();
    </script>
</body>
</html>
