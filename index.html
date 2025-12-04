
<!DOCTYPE html>
<html>
<head>
    <title>Capture Image & Location</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; }
        video, canvas { margin: 10px auto; display: block; }
        button { margin: 10px; padding: 10px 20px; }
        #location { margin-top: 15px; font-weight: bold; }
    </style>
</head>
<body>
    <h1>Capture Image and Location</h1>
    <video id="video" width="400" height="300" autoplay></video>
    <button id="capture">Capture Image & Location</button>
    <canvas id="canvas" width="400" height="300"></canvas>
    <p id="location">Location: Not captured yet</p>
    <a id="downloadLink" style="display:none;">Download Image & Location</a>

    <script>
        const video = document.getElementById('video');
        const canvas = document.getElementById('canvas');
        const captureBtn = document.getElementById('capture');
        const context = canvas.getContext('2d');
        const locationEl = document.getElementById('location');
        const downloadLink = document.getElementById('downloadLink');

        // Access camera
        navigator.mediaDevices.getUserMedia({ video: true })
            .then(stream => { video.srcObject = stream; })
            .catch(err => { console.error("Camera error:", err); });

        // Capture image and location
        captureBtn.addEventListener('click', () => {
            // Draw video frame on canvas
            context.drawImage(video, 0, 0, canvas.width, canvas.height);

            // Get location
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(pos => {
                    const { latitude, longitude } = pos.coords;
                    locationEl.textContent = `Location: ${latitude}, ${longitude}`;

                    // Prepare download
                    const imageData = canvas.toDataURL("image/png");
                    const textData = `Location: ${latitude}, ${longitude}`;
                    const blob = new Blob([textData], { type: 'text/plain' });

                    // Create a combined download (image + location)
                    const zipContent = `
                        Image: ${imageData}
                        ${textData}
                    `;
                    const zipBlob = new Blob([zipContent], { type: 'text/plain' });
                    const url = URL.createObjectURL(zipBlob);

                    downloadLink.href = url;
                    downloadLink.download = "capture.txt";
                    downloadLink.textContent = "Download Image & Location";
                    downloadLink.style.display = "block";
                }, err => {
                                       locationEl.textContent = "Location access denied.";
                });
            } else {
                locationEl.textContent = "Geolocation not supported.";
            }
        });
    </script>
</body>
