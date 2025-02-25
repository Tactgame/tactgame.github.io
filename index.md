---
layout: default
title: "首页"
permalink: /
---

<div class="hero" data-aos="fade-up">
  <!-- 动态宣传横幅（轮播图） -->
  <div class="slider">
    <div class="slide active">
      <img src="{{ '/images/spxdzmmz.png' | relative_url }}" alt="版本更新1" loading="lazy">
      <div class="slide-caption">
        <h2>全新版本发布！</h2>
        <p>体验全新功能，享受更畅快的狙击体验。</p>
      </div>
    </div>
    <div class="slide">
      <img src="{{ '/images/3.png' | relative_url }}" alt="版本更新2" loading="lazy">
      <div class="slide-caption">
        <h2>重大公告</h2>
        <p>即将迎来全新商店体验，敬请期待！</p>
      </div>
    </div>
    <!-- 根据需要添加更多轮播项 -->
  </div>
</div>

<div class="announcement" data-aos="fade-up">
  <h2>最新公告</h2>
  <p>欢迎来到官网！最新版本发布在即，敬请期待更多精彩内容！</p>
</div>

<div class="button-group" data-aos="fade-up">
  <a class="button" href="{{ '/intro/' | relative_url }}">游戏介绍</a>
  <a class="button" href="{{ '/changelog/' | relative_url }}">更新日志</a>
  <a class="button" href="{{ '/play/' | relative_url }}">在线试玩</a>
  <a class="button" href="{{ '/download/' | relative_url }}">软件下载</a>
  <a class="button" href="{{ '/leaderboard/' | relative_url }}">排行榜</a>
  <a class="button" href="{{ '/gallery/' | relative_url }}">媒体库</a>
  <a class="button" href="{{ '/forum/' | relative_url }}">论坛</a>
  <a class="button" href="{{ '/about/' | relative_url }}">关于</a>
</div>

<!-- 简单轮播图脚本 -->
<script>
document.addEventListener("DOMContentLoaded", function() {
  const slides = document.querySelectorAll('.slider .slide');
  let currentSlide = 0;
  function nextSlide() {
    slides[currentSlide].classList.remove('active');
    currentSlide = (currentSlide + 1) % slides.length;
    slides[currentSlide].classList.add('active');
  }
  setInterval(nextSlide, 5000); // 每5秒切换一次
});
</script>
