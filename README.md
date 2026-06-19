<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>تطبيق إداره النادي الرياضي</title>
  <style>
    /* 1. Reset: مسح التنسيقات الافتراضية للمتصفح */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body { 
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex; 
      height: 100vh; 
      background-color: #f4f7f6; 
    }

    /* 2. تصميم الشريط الجانبي (Sidebar) */
    .sidebar { 
      width: 260px; 
      background-color: #2c3e50; 
      color: white; 
      padding: 20px;
    }
    .sidebar h2 { text-align: center; margin-bottom: 30px; font-size: 1.2rem; }
    .nav-item { 
      padding: 15px; 
      display: block; 
      color: #bdc3c7; 
      text-decoration: none; 
      transition: 0.3s;
    }
    .nav-item:hover { background-color: #34495e; color: white; border-right: 4px solid #3498db; }

    /* 3. تصميم المحتوى الرئيسي */
    .main-content { flex: 1; padding: 40px; }
    .btn-action {
      background-color: #27ae60;
      color: white;
      padding: 12px 25px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1rem;
    }
    .btn-action:hover { background-color: #219150; }
    
    #display-area { margin-top: 30px; padding: 20px; background: white; border-radius: 8px; }
    img { max-width: 100%; height: auto; border-radius: 8px; margin-top: 15px; }
  </style>
</head>
<body>

  <div class="sidebar">
    <h2>لوحة التحكم</h2>
    <a href="#" class="nav-item">🏠 الرئيسية</a>
    <a href="#" class="nav-item">👤 اللاعبين</a>
    <a href="#" class="nav-item">⚙️ الإعدادات</a>
  </div>

  <main class="main-content">
    <h1>منظومة التشريح التفاعلية</h1>
    <br>
    <button class="btn-action" onclick="showAnatomy()">عرض الهيكل التشريحي</button>
    
    <div id="display-area">
      <p>اضغط على الزر لعرض المحتوى.</p>
    </div>
  </main>

  <script>
    function showAnatomy() 
      const area = document.getElementById('display-area');
      
      // ملاحظة: قم بتغيير الاسم هنا ليتطابق مع اسم الملف الفعلي في مجلد مشروعك
      const imagePath = "anatomy.jpg"; 
      
      area.innerHTML = `
        <h3>الهيكل العظمي البشري</h3>
        <img src="${imagePath}" alt="صورة تشريحية" onerror="this.src='placeholder.jpg'; this.style.display='none'; alert('لم يتم العثور على ملف الصورة!');">
      `;
    }
  </script>
</body>
</html>
قمت بإعادة انشاء صفة جديد بهذا الكود
