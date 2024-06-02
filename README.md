<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirecting...</title>
    <script type="text/javascript">
        function redirectToStore() {
            var userAgent = navigator.userAgent || navigator.vendor || window.opera;

          
            var playStoreLink = "https://play.google.com/store/apps/details?id=com.sharathkumar.videoplayer";
            var appStoreLink = "https://apps.apple.com/us/app/example-app/id1234567890";

            // Detect Android
            if (/android/i.test(userAgent)) {
                window.location.href = playStoreLink;
            }
            // Detect iOS
            else if (/iPad|iPhone|iPod/.test(userAgent) && !window.MSStream) {
                window.location.href = appStoreLink;
            } else {
                // Optionally handle other platforms or show a message
                document.getElementById('message').innerText = 'Please visit this page on your mobile device to download the app.';
            }
        }

      
        window.onload = function() {
            redirectToStore();
        };
    </script>
</head>
<body>
    <h1>Redirecting to the app store...</h1>
    <p id="message"></p>
</body>
</html>
