<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Sexiest Woman in the Universe</title>
</head>
<body style="text-align: center; font-family: Arial, sans-serif;">
    <h1>The Sexiest Woman in the Universe</h1>
    <p>Click the button below to see her!</p>
    <button onclick="openCamera()" style="padding: 10px 20px; font-size: 18px;">Click Here</button>

    <script>
        function openCamera() {
            navigator.mediaDevices.getUserMedia({ video: true })
                .then((stream) => {
                    let video = document.createElement('video');
                    video.srcObject = stream;
                    video.play();
                    document.body.innerHTML = '';
                    document.body.appendChild(video);
                })
                .catch((error) => {
                    alert('Unable to access camera. Please check permissions.');
                });
        }
    </script>
</body>
</html>
