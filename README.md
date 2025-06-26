<!DOCTYPE html> -->
<!-- <html lang="ar"> -->
<!-- <head> -->
  <!-- <meta charset="UTF-8"> -->
  <!-- <title>فيديو تفاعلي تعليمي</title> -->
  <!-- <style> -->
    <!-- body { font-family: Tahoma, Arial; background: #f4f4f4; direction: rtl; padding: 30px;} -->
    <!-- .container { max-width: 800px; margin: auto; background: #fff; border-radius: 10px; box-shadow: 0 0 10px #ccc; padding: 20px;} -->
    <!-- .question, .note, .choice { display: none; margin: 20px 0; } -->
    <!-- .show { display: block; } -->
    <!-- .btn { padding: 8px 15px; margin: 5px; border-radius: 5px; border: none; background: #1976d2; color: #fff; cursor: pointer;} -->
    <!-- .btn:hover { background: #0d47a1; } -->
  <!-- </style> -->
<!-- </head> -->
<!-- <body> -->
  <!-- <div class="container"> -->
    <!-- <h2>شاهد الفيديو وتفاعل مع الأسئلة والملاحظات</h2> -->
    مشغل يوتيوب
    <!-- <div style="text-align:center;"> -->
      <!-- <iframe id="ytplayer" width="700" height="400" src="https://www.youtube.com/embed/7zdt7tMOqkc?enablejsapi=1"  -->
        <!-- frameborder="0" allowfullscreen></iframe> -->
    <!-- </div> -->
    
    ملاحظة تظهر في الدقيقة الأولى
    <!-- <div class="note" id="note1"> -->
      <!-- <strong>ملاحظة:</strong> ركز على الخطوات المذكورة في بداية الفيديو. -->
    <!-- </div> -->
    
    سؤال تفاعلي يظهر بعد 40 ثانية
    <!-- <div class="question" id="q1"> -->
      <!-- <b>سؤال:</b> ما هو اسم البرنامج المستخدم في الشرح؟ -->
      <!-- <div> -->
        <!-- <button class="btn" onclick="answer(true, 'q1')">أدوبي بريمير</button> -->
        <!-- <button class="btn" onclick="answer(false, 'q1')">مايكروسوفت وورد</button> -->
        <!-- <button class="btn" onclick="answer(false, 'q1')">إكسل</button> -->
      <!-- </div> -->
      <!-- <div id="feedback-q1"></div> -->
    <!-- </div> -->
    
    خيار مسار يظهر بعد دقيقة ونصف
    <!-- <div class="choice" id="choice1"> -->
      <!-- <b>ماذا تريد أن تشاهد بعد ذلك؟</b> -->
      <!-- <div> -->
        <!-- <button class="btn" onclick="seekTo(180)">شرح متقدم</button> -->
        <!-- <button class="btn" onclick="seekTo(240)">نصائح للمبتدئين</button> -->
      <!-- </div> -->
    <!-- </div> -->
  <!-- </div> -->

  <!-- <script> -->
    <!-- // تحميل واجهة API لليوتيوب -->
    <!-- var tag = document.createElement('script'); -->
    <!-- tag.src = "https://www.youtube.com/iframe_api"; -->
    <!-- document.body.appendChild(tag); -->

    <!-- var player; -->
    <!-- function onYouTubeIframeAPIReady() { -->
      <!-- player = new YT.Player('ytplayer', { -->
        <!-- events: { 'onStateChange': onPlayerStateChange } -->
      <!-- }); -->
    <!-- } -->

    <!-- // مراقبة الوقت لعرض العناصر التفاعلية -->
    <!-- var shown = {}; -->
    <!-- function onPlayerStateChange(event) { -->
      <!-- if (event.data == YT.PlayerState.PLAYING) { -->
        <!-- setInterval(checkInteraction, 500); -->
      <!-- } -->
    <!-- } -->
    <!-- function checkInteraction() { -->
      <!-- if (!player || typeof player.getCurrentTime !== 'function') return; -->
      <!-- var t = player.getCurrentTime(); -->

      <!-- // ملاحظة تظهر بعد 10 ثواني وتختفي بعد 25 ثانية -->
      <!-- if (t > 10 && t < 35 && !shown.note1) { -->
        <!-- document.getElementById('note1').classList.add('show'); -->
        <!-- shown.note1 = true; -->
      <!-- } -->
      <!-- if (t > 35 && shown.note1) { -->
        <!-- document.getElementById('note1').classList.remove('show'); -->
      <!-- } -->

      <!-- // سؤال يظهر بعد 40 ثانية -->
      <!-- if (t > 40 && t < 70 && !shown.q1) { -->
        <!-- document.getElementById('q1').classList.add('show'); -->
        <!-- shown.q1 = true; -->
      <!-- } -->
      <!-- if (t > 70 && shown.q1) { -->
        <!-- document.getElementById('q1').classList.remove('show'); -->
      <!-- } -->

      <!-- // خيار مسار يظهر بعد 90 ثانية -->
      <!-- if (t > 90 && t < 120 && !shown.choice1) { -->
        <!-- document.getElementById('choice1').classList.add('show'); -->
        <!-- shown.choice1 = true; -->
      <!-- } -->
      <!-- if (t > 120 && shown.choice1) { -->
        <!-- document.getElementById('choice1').classList.remove('show'); -->
      <!-- } -->
    <!-- } -->

    <!-- // معالجة الإجابة على السؤال -->
    <!-- function answer(correct, id) { -->
      <!-- var feedback = document.getElementById('feedback-' + id); -->
      <!-- if (correct) { -->
        <!-- feedback.innerHTML = '<span style="color:green">إجابة صحيحة!</span>'; -->
      <!-- } else { -->
        <!-- feedback.innerHTML = '<span style="color:red">إجابة خاطئة، حاول مرة أخرى.</span>'; -->
      <!-- } -->
    <!-- } -->

    <!-- // الذهاب لجزء معين من الفيديو -->
    <!-- function seekTo(seconds) { -->
      <!-- if (player) player.seekTo(seconds, true); -->
    <!-- } -->
  <!-- </script> -->
<!-- </body> -->
<!-- </html>
