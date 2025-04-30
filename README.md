<script>
  // الانتقال بين الصفحات
  function goToPage2() {
    document.getElementById('page1').classList.add('hidden');
    document.getElementById('page2').classList.remove('hidden');
  }

  function showQuestion2() {
    document.getElementById('page2').classList.add('hidden');
    document.getElementById('question2').classList.remove('hidden');
  }

  function showQuestion3() {
    document.getElementById('question2').classList.add('hidden');
    document.getElementById('question3').classList.remove('hidden');
  }

  function showQuestion4() {
    document.getElementById('question3').classList.add('hidden');
    document.getElementById('question4').classList.remove('hidden');
  }

  function showQuestion5() {
    document.getElementById('question4').classList.add('hidden');
    document.getElementById('question5').classList.remove('hidden');
  }

  function finish() {
    document.getElementById('question5').classList.add('hidden');
    document.getElementById('finishPage').classList.remove('hidden');
  }

  // إرسال الإجابات إلى صبحي عبر واتساب
  function sendToWhatsApp() {
    const answers = {
      age: "١٦",  // على سبيل المثال
      favoriteDish: "جميع ما سبق",  // على سبيل المثال
      prefersSugar: "لا يفضل ريتاج عن السكر",
      lovesRetaj: "نعم",
      location: "بالبيت نايم"
    };

    const message = `إجابات الأسئلة:\n
      ١. كم عمر صبحي؟: ${answers.age}\n
      ٢. أفضل أكلة لدى صبحي؟: ${answers.favoriteDish}\n
      ٣. هل صبحي يفضل السكر على ريتاج؟: ${answers.prefersSugar}\n
      ٤. هل صبحي يعشق ريتاج؟: ${answers.lovesRetaj}\n
      ٥. أين يكون صبحي الساعة ١٢:٠٠؟: ${answers.location}`;

    const whatsappUrl = `https://wa.me/966557073705?text=${encodeURIComponent(message)}`;
    window.open(whatsappUrl, "_blank");
  }

  // إرسال الإجابات إلى صبحي عبر إنستغرام
  function sendToInstagram() {
    const message = `إجابات الأسئلة:  
      ١. كم عمر صبحي؟: ١٦  
      ٢. أفضل أكلة لدى صبحي؟: جميع ما سبق  
      ٣. هل صبحي يفضل السكر على ريتاج؟: لا يفضل ريتاج عن السكر  
      ٤. هل صبحي يعشق ريتاج؟: نعم  
      ٥. أين يكون صبحي الساعة ١٢:٠٠؟: بالبيت نايم`;

    const instagramUrl = `https://www.instagram.com/messages/compose/?text=${encodeURIComponent(message)}`;
    window.open(instagramUrl, "_blank");
  }

  // مشاركة النتائج عبر التطبيقات
  function shareResults() {
    const message = `إجابات الأسئلة:
      ١. كم عمر صبحي؟: ١٦
      ٢. أفضل أكلة لدى صبحي؟: جميع ما سبق
      ٣. هل صبحي يفضل السكر على ريتاج؟: لا يفضل ريتاج عن السكر
      ٤. هل صبحي يعشق ريتاج؟: نعم
      ٥. أين يكون صبحي الساعة ١٢:٠٠؟: بالبيت نايم`;

    // ستفتح نافذة المشاركة عبر التطبيقات
    navigator.share({
      title: "إجابات الأسئلة",
      text: message,
    }).catch((error) => console.error('Error sharing:', error));
  }

  // نسخ النتائج
  function copyResults() {
    const message = `إجابات الأسئلة:
      ١. كم عمر صبحي؟: ١٦
      ٢. أفضل أكلة لدى صبحي؟: جميع ما سبق
      ٣. هل صبحي يفضل السكر على ريتاج؟: لا يفضل ريتاج عن السكر
      ٤. هل صبحي يعشق ريتاج؟: نعم
      ٥. أين يكون صبحي الساعة ١٢:٠٠؟: بالبيت نايم`;

    navigator.clipboard.writeText(message).then(() => {
      alert("تم نسخ النتائج!");
    }).catch((error) => {
      console.error("لم يتم النسخ: ", error);
    });
  }
</script>