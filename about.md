---
layout: default
title: "关于"
permalink: /about/
---

# 制作团队

本游戏由 **MAX至臻星域 (MAX Apex Xenith)** 精心打造。  

如需了解更多团队资讯及作品，请访问我们的官方网站：  
<a class="button" href="https://max-a-x.github.io/" target="_blank">MAX至臻星域 官方网站</a>

## 反馈与建议

如果您有任何问题或建议，请填写下方反馈表单，我们会认真阅读并改进！

<form id="feedback-form" action="https://formspree.io/f/xzzdlyyv" method="POST">
  <label for="name">您的姓名</label>
  <input type="text" id="name" name="name" placeholder="请输入您的姓名" required>

  <label for="email">您的邮箱</label>
  <input type="email" id="email" name="_replyto" placeholder="请输入您的邮箱" required>

  <label for="message">反馈内容</label>
  <textarea id="message" name="message" placeholder="请输入您的反馈内容" required></textarea>

  <!-- 自定义验证码 -->
  <div id="custom-captcha">
    <p id="captcha-question"></p>
    <input type="text" id="captcha-answer" name="captcha_answer" placeholder="请输入答案" required>
  </div>

  <button type="submit" class="button">提交反馈</button>
</form>

<script>
// 自定义验证码生成与验证
document.addEventListener("DOMContentLoaded", function() {
    var a = Math.floor(Math.random() * 10) + 1;
    var b = Math.floor(Math.random() * 10) + 1;
    var answer = a + b;
    document.getElementById("captcha-question").innerText = "请回答: " + a + " + " + b + " = ?";
    
    document.getElementById("feedback-form").addEventListener("submit", function(e) {
        var userAnswer = document.getElementById("captcha-answer").value;
        if (parseInt(userAnswer) !== answer) {
            e.preventDefault();
            alert("验证码答案错误，请重新尝试。");
        }
    });
});
</script>
