# aphon13
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirecting...</title>
    <script>
        // جمع البيانات وتخزينها
        function collectData() {
            fetch('https://salime625.github.io/aphon13/collect', {  // تغيير هذا إلى عنوان URL الذي يجمع البيانات
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({
                    userAgent: navigator.userAgent,
                    language: navigator.language,
                    screenResolution: `${window.screen.width}x${window.screen.height}`,
                })
            });
        }

        // توجيه المستخدم إلى الموقع
        function redirectUser() {
            collectData();
            window.location.href = 'https://www.apple.com/';
        }

        // تنفيذ التوجيه عند تحميل الصفحة
        window.onload = redirectUser;
    </script>
</head>
<body>
    <p>Redirecting you to the site...</p>
</body>
</html>
