# RHINE0724.github.io
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>你喜欢住什么样的民宿 | 性格测试</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
        }

        body {
            background-color: #f3efe9;
            color: #5c5853;
            padding: 20px 15px;
            min-height: 100vh;
        }

        /* 头部文案 */
        .header {
            text-align: center;
            margin-bottom: 24px;
        }
        .header h1 {
            font-size: 23px;
            color: #7c746b;
            margin-bottom: 8px;
        }
        .header p {
            font-size: 14px;
            color: #928a80;
            line-height: 1.6;
        }

        /* 卡片容器 */
        .card {
            background: #ffffff;
            border-radius: 18px;
            padding: 24px 20px;
            box-shadow: 0 3px 12px rgba(124, 116, 107, 0.08);
        }

        /* 题目容器 */
        .question-wrap {
            display: none;
        }
        .question-wrap.active {
            display: block;
        }

        .progress-text {
            font-size: 13px;
            color: #b4aaa0;
            text-align: right;
            margin-bottom: 16px;
        }
        .question-text {
            font-size: 16px;
            line-height: 1.7;
            margin-bottom: 26px;
            color: #645d55;
        }

        /* 选项样式 */
        .option {
            background-color: #f8f5f0;
            border: 1px solid #eae3db;
            border-radius: 14px;
            padding: 15px 18px;
            margin-bottom: 12px;
            cursor: pointer;
            transition: 0.25s ease;
        }
        .option:hover {
            background-color: #efe9e1;
        }
        .option.selected {
            background-color: #e6ddd2;
            border-color: #d1c3b3;
        }

        /* 按钮区域 */
        .btn-box {
            display: flex;
            justify-content: space-between;
            margin-top: 32px;
            gap: 12px;
        }
        .btn {
            width: 48%;
            border: none;
            border-radius: 12px;
            padding: 12px 0;
            font-size: 15px;
            cursor: pointer;
            transition: 0.25s;
        }
        .btn-prev {
            background: #e2dbd1;
            color: #70685e;
        }
        .btn-next {
            background: #b8a99b;
            color: #fff;
        }
        .btn:active {
            opacity: 0.92;
        }

        /* 未选提示 */
        .warn-tip {
            font-size: 13px;
            color: #c97878;
            margin-top: 12px;
            display: none;
        }

        /* 结果页 */
        .result-wrap {
            display: none;
            text-align: center;
        }
        .result-title {
            font-size: 20px;
            color: #8c7b6e;
            margin-bottom: 15px;
        }
        .room-name {
            font-size: 26px;
            color: #a07c68;
            font-weight: bold;
            margin: 18px 0;
        }
        .room-desc {
            text-align: left;
            line-height: 1.9;
            color: #665f56;
            font-size: 15px;
        }
        .reset-btn {
            margin-top: 30px;
            padding: 12px 36px;
            border: none;
            border-radius: 12px;
            background: #b8a99b;
            color: #fff;
            font-size: 15px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>你喜欢住什么样的民宿</h1>
        <p>文创民宿治愈小测试<br>15道小题，匹配专属你的理想民宿房型与性格</p >
    </div>

    <div class="card">
        <!-- 答题区域 -->
        <div id="qContainer">
            <!-- 第1题 -->
            <div class="question-wrap active">
                <div class="progress-text">1 / 15</div>
                <div class="question-text">1. 挑选民宿，你最先看重什么？</div>
                <div class="option" data-type="A">安静氛围，远离喧嚣</div>
                <div class="option" data-type="B">温馨舒适，治愈放松</div>
                <div class="option" data-type="C">设计感强，文创特色</div>
            </div>
            <!-- 第2题 -->
            <div class="question-wrap">
                <div class="progress-text">2 / 15</div>
                <div class="question-text">2. 理想民宿窗外风景是？</div>
                <div class="option" data-type="A">山林小院，草木清幽</div>
                <div class="option" data-type="B">庭院花海，温柔景致</div>
                <div class="option" data-type="C">文艺街巷，复古小店</div>
            </div>
            <!-- 第3题 -->
            <div class="question-wrap">
                <div class="progress-text">3 / 15</div>
                <div class="question-text">3. 房间软装更喜欢？</div>
                <div class="option" data-type="A">原木极简，干净素雅</div>
                <div class="option" data-type="B">毛绒软装，暖光温柔</div>
                <div class="option" data-type="C">手作摆件，文创装饰</div>
            </div>
            <!-- 第4题 -->
            <div class="question-wrap">
                <div class="progress-text">4 / 15</div>
                <div class="question-text">4. 旅行状态更接近？</div>
                <div class="option" data-type="A">独自放空，慢节奏发呆</div>
                <div class="option" data-type="B">结伴闲逛，轻松惬意</div>
                <div class="option" data-type="C">探店打卡，收集小众好物</div>
            </div>
            <!-- 第5题 -->
            <div class="question-wrap">
                <div class="progress-text">5 / 15</div>
                <div class="question-text">5. 夜晚在民宿你会？</div>
                <div class="option" data-type="A">早早休息，享受独处</div>
                <div class="option" data-type="B">泡杯热茶，追剧放松</div>
                <div class="option" data-type="C">翻看书籍，写写随笔</div>
            </div>
            <!-- 第6题 -->
            <div class="question-wrap">
                <div class="progress-text">6 / 15</div>
                <div class="question-text">6. 更喜欢哪种灯光氛围？</div>
                <div class="option" data-type="A">冷调柔光，简约清冷</div>
                <div class="option" data-type="B">暖黄漫射，温柔氛围感</div>
                <div class="option" data-type="C">复古台灯，文艺光影</div>
            </div>
            <!-- 第7题 -->
            <div class="question-wrap">
                <div class="progress-text">7 / 15</div>
                <div class="question-text">7. 面对陌生环境你的感受？</div>
                <div class="option" data-type="A">需要安静缓冲，慢慢适应</div>
                <div class="option" data-type="B">顺其自然，很快放松</div>
                <div class="option" data-type="C">充满好奇，喜欢新鲜感</div>
            </div>
            <!-- 第8题 -->
            <div class="question-wrap">
                <div class="progress-text">8 / 15</div>
                <div class="question-text">8. 民宿配套更想要？</div>
                <div class="option" data-type="A">独立小院，私密空间</div>
                <div class="option" data-type="B">公共客厅，休闲角落</div>
                <div class="option" data-type="C">文创展厅，手作体验</div>
            </div>
            <!-- 第9题 -->
            <div class="question-wrap">
                <div class="progress-text">9 / 15</div>
                <div class="question-text">9. 你的性格偏向？</div>
                <div class="option" data-type="A">内敛慢热，内心细腻</div>
                <div class="option" data-type="B">温和包容，治愈善良</div>
                <div class="option" data-type="C">独特有趣，审美小众</div>
            </div>
            <!-- 第10题 -->
            <div class="question-wrap">
                <div class="progress-text">10 / 15</div>
                <div class="question-text">10. 更排斥哪种住宿体验？</div>
                <div class="option" data-type="A">人多嘈杂，缺少隐私</div>
                <div class="option" data-type="B">冰冷简陋，没有温度</div>
                <div class="option" data-type="C">千篇一律，毫无特色</div>
            </div>
            <!-- 第11题 -->
            <div class="question-wrap">
                <div class="progress-text">11 / 15</div>
                <div class="question-text">11. 休息时更偏爱？</div>
                <div class="option" data-type="A">安静独处，与自己相处</div>
                <div class="option" data-type="B">舒适慵懒，随心所欲</div>
                <div class="option" data-type="C">文艺消遣，充实日常</div>
            </div>
            <!-- 第12题 -->
            <div class="question-wrap">
                <div class="progress-text">12 / 15</div>
                <div class="question-text">12. 色彩偏好？</div>
                <div class="option" data-type="A">莫兰迪冷色、低灰素雅</div>
                <div class="option" data-type="B">奶咖暖调、柔和浅色系</div>
                <div class="option" data-type="C">复古撞色、文艺质感色</div>
            </div>
            <!-- 第13题 -->
            <div class="question-wrap">
                <div class="progress-text">13 / 15</div>
                <div class="question-text">13. 旅行的意义对你来说？</div>
                <div class="option" data-type="A">逃离纷扰，治愈内心</div>
                <div class="option" data-type="B">放松身心，享受生活</div>
                <div class="option" data-type="C">感受人文，遇见新意</div>
            </div>
            <!-- 第14题 -->
            <div class="question-wrap">
                <div class="progress-text">14 / 15</div>
                <div class="question-text">14. 民宿早餐你期待？</div>
                <div class="option" data-type="A">简单清淡，简约健康</div>
                <div class="option" data-type="B">丰盛暖心，家常味道</div>
                <div class="option" data-type="C">特色点心，地域文创美食</div>
            </div>
            <!-- 第15题 -->
            <div class="question-wrap">
                <div class="progress-text">15 / 15</div>
                <div class="question-text">15. 未来理想居住氛围？</div>
                <div class="option" data-type="A">清净山居，与世无争</div>
                <div class="option" data-type="B">烟火小院，温柔日常</div>
                <div class="option" data-type="C">文艺街巷，诗意生活</div>
            </div>

            <div class="warn-tip" id="warnTip">请先选择一个答案再继续</div>
            <div class="btn-box">
                <button class="btn btn-prev" id="prevBtn">上一题</button>
                <button class="btn btn-next" id="nextBtn">下一题</button>
            </div>
        </div>

        <!-- 结果页面 -->
        <div class="result-wrap" id="resultWrap">
            <div class="result-title">你的专属文创民宿房型</div>
            <div class="room-name" id="roomName"></div>
            <div class="room-desc" id="roomDesc"></div>
            <button class="reset-btn" id="resetBtn">重新测试</button>
        </div>
    </div>

    <script>
        const questions = document.querySelectorAll(".question-wrap");
        const options = document.querySelectorAll(".option");
        const prevBtn = document.getElementById("prevBtn");
        const nextBtn = document.getElementById("nextBtn");
        const warnTip = document.getElementById("warnTip");
        const qContainer = document.getElementById("qContainer");
        const resultWrap = document.getElementById("resultWrap");
        const roomName = document.getElementById("roomName");
        const roomDesc = document.getElementById("roomDesc");
        const resetBtn = document.getElementById("resetBtn");

        let current = 0;
        let answerRecord = [];

        // 结果库：三种房型 + 性格解析
        const resultData = {
            A: {
                name:「清寂山舍·独处房」,
                desc:"你最适合安静小众的山系独处民宿。性格清冷温柔、内心丰盈细腻，偏爱低饱和度的简约环境，不喜热闹与人潮。自带疏离又干净的气质，擅长和自己和解，喜欢慢生活、草木与安静时光。追求精神松弛与私密感，是自带诗意的治愈独处型人格。"
            },
            B: {
                name:「暖柔庭院·治愈房」,
                desc:"你适配温柔满满的庭院治愈系民宿。性格温和柔软、包容力强，自带烟火气与亲和力，待人舒服、心思细腻共情力强。喜欢暖光、绿植与柔软的生活氛围，向往安稳松弛的日常。不追求特立独行，只想要温暖踏实的小美好，是身边人的小太阳。"
            },
            C: {
                name:「文创复古·艺术房」,
                desc:"你注定住进充满设计感的文创艺术民宿。审美独特、思想丰富，热爱复古、手作、文创与小众文化。个性鲜明、想法多元，讨厌千篇一律的模板生活。热爱探索新鲜事物，追求仪式感与生活美学，自带文艺气息，是骨子里浪漫的艺术型人格。"
            }
        };

        // 选项选中
        options.forEach(opt => {
            opt.addEventListener("click", () => {
                const parent = opt.parentElement;
                parent.querySelectorAll(".option").forEach(o => o.classList.remove("selected"));
                opt.classList.add("selected");
                warnTip.style.display = "none";
            });
        });

        // 上一题
        prevBtn.onclick = () => {
            if(current <= 0) return;
            questions[current].classList.remove("active");
            current--;
            questions[current].classList.add("active");
        };

        // 下一题 / 提交
        nextBtn.onclick = () => {
            const nowQ = questions[current];
            const selected = nowQ.querySelector(".option.selected");
            if(!selected){
                warnTip.style.display = "block";
                return;
            }
            answerRecord[current] = selected.dataset.type;

            if(current >= 14){
                calcResult();
                return;
            }

            questions[current].classList.remove("active");
            current++;
            questions[current].classList.add("active");
        };

        // 计算结果
        function calcResult(){
            let a = 0, b = 0, c = 0;
            answerRecord.forEach(t => {
                if(t === "A") a++;
                if(t === "B") b++;
                if(t === "C") c++;
            });
            let res = "A";
            if(b >= a && b >= c) res = "B";
            if(c >= a && c >= b) res = "C";

            qContainer.style.display = "none";
            resultWrap.style.display = "block";
            roomName.innerText = resultData[res].name;
            roomDesc.innerText = resultData[res].desc;
        }

        // 重置测试
        resetBtn.onclick = () => {
            current = 0;
            answerRecord = [];
            qContainer.style.display = "block";
            resultWrap.style.display = "none";
            options.forEach(o => o.classList.remove("selected"));
            questions.forEach(q => q.classList.remove("active"));
            questions[0].classList.add("active");
        };
    </script>
</body>
</html>
