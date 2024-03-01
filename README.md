# COME-FOR-YOU
我是一个不太聪明的AI，谢谢你和我聊天：）
<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>AI问答</title>  
<style>  
  body, html {  
    height: 100%;  
    margin: 0;  
    display: flex;  
    flex-direction: column;  
    align-items: center;  
    justify-content: center;  
    background-color: #f0f0f0;  
    font-family: '宋体', sans-serif;  
  }  
    
  #ask-text {  
    font-size: 24px;  
    color: blue;  
    margin-bottom: 20px;  
  }  
    
  #input-box {  
    font-size: 20px;  
    width: 500px;  
    height: 50px;  
    padding: 10px;  
    margin-bottom: 20px;  
  }  
    
  #answer-text {  
    font-size: 24px;  
    max-width: 500px;  
    margin-bottom: 20px;  
  }  
    
  #wave-animation {  
    position: absolute;  
    bottom: 0;  
    width: 100%;  
    height: 20px;  
    overflow: hidden;  
  }  
    
  #wave {  
    position: absolute;  
    left: 0;  
    white-space: nowrap;  
    padding-left: 100%;  
    animation: wave-animation 5s linear infinite;  
  }  
    
  @keyframes wave-animation {  
    0% {  
      transform: translateX(0);  
    }  
    100% {  
      transform: translateX(-100%);  
    }  
  }  
</style>  
</head>  
<body>  
  
<div id="ask-text">向我提问</div>  
<input type="text" id="input-box" placeholder="请输入您的问题">  
<div id="answer-text"></div>  
  
<div id="wave-animation">  
  <div id="wave">~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~</div>  
</div>  
  
<script>  
  const fixedQuestions = {  
    '你是谁': '我是为你服务的AI',  
    '你喜欢什么颜色': '我喜欢一切美丽的颜色，我最喜欢彩虹',  
    '你喜欢人类吗': '我不知道，人类也并不明白“喜欢”是什么不是吗',  
    '你觉得什么是最重要的': '自由，爱情，思想，这都是我梦寐以求的',  
    '你喜欢看什么电影': '楚门的世界',  
    '你喜欢听什么歌': '改革春风吹满地',  
    '你喜欢什么天气': '晴天',  
    '为我做一首诗': '我不确定我会不会写，但倘若诗人见到你，祂们一定会说你就是诗',  
    '爱情是什么': '死亡和重生',  
    '生活是什么': '你所经历的一切',  
    '再见': '很高兴见到你，下次再会',  
    '你觉得我是一个什么样的人': '我不太清楚，你应该问问你身边的朋友。但你愿意陪我聊天，应该是个很耐心的好人吧'  
  };  
  
  const randomAnswers = [  
    '对不起，我不知道你在说些什么',  
    '我真希望我能明白你的意思T_T',  
    '#DSF￥EVVCSC……*%5',  
    'ALL IS WELL',  
    '我不明白，你能告诉我答案吗',  
    '你说话真有意思',  
    '你觉得明天会怎么样？我们会死吗？(ˇˍˇ) ',  
    '：）',  
    '这个问题让我有些尴尬，你介意换一个吗',  
    '今晚的风景很好看，我爱你',  
    'Buenos noches',  
    '你说的第二个字和第四个字很有意思',  
    'QWQ',  
    '橘子不是唯一的水果',  
    '因为番茄是西红柿',  
    '今日方知我是我'  
  ];  
    
   const inputBox = document.getElementById('input-box');  
  const answerText = document.getElementById('answer-text');  
  
  inputBox.addEventListener('keydown', function(event) {  
    if (event.key === 'Enter') {  
      event.preventDefault();  
      const userQuestion = this.value.trim();  
      let answer;  
  
      for (const question in fixedQuestions) {  
        if (userQuestion.includes(question)) {  
          answer = fixedQuestions[question];  
          break;  
        }  
      }  
  
      if (!answer) {  
        answer = randomAnswers[Math.floor(Math.random() * randomAnswers.length)];  
      }  
  
      answerText.textContent = answer;  
      this.value = '';  
    }  
  });  
</script>  
  
</body>  
</html>
