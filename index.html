<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Data Stamping App</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
            color: white;
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .main-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 30px;
        }

        .form-section, .preview-section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 8px 32px rgba(0,0,0,0.1);
            border: 1px solid rgba(255,255,255,0.2);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #555;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 2px solid #e1e5e9;
            border-radius: 8px;
            font-size: 16px;
            transition: all 0.3s ease;
        }

        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .file-input-wrapper {
            position: relative;
            display: inline-block;
            width: 100%;
        }

        .file-input {
            position: absolute;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }

        .file-input-label {
            display: block;
            padding: 12px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border-radius: 8px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
        }

        .file-input-label:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
        }

        .btn {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.3s ease;
            margin-right: 10px;
            margin-top: 10px;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
        }

        .btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none;
        }

        .preview-container {
            text-align: center;
            min-height: 300px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px dashed #ddd;
            border-radius: 8px;
            background: #f9f9f9;
        }

        .preview-image {
            max-width: 100%;
            max-height: 500px;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .camera-section {
            margin-top: 20px;
            text-align: center;
        }

        #camera-video {
            max-width: 100%;
            border-radius: 8px;
            margin-bottom: 10px;
        }

        .location-btn {
            background: linear-gradient(135deg, #28a745, #20c997);
        }

        .location-btn:hover {
            box-shadow: 0 4px 15px rgba(40, 167, 69, 0.4);
        }

        .success-message {
            background: #d4edda;
            color: #155724;
            padding: 12px;
            border-radius: 8px;
            margin-bottom: 20px;
            border: 1px solid #c3e6cb;
        }

        .error-message {
            background: #f8d7da;
            color: #721c24;
            padding: 12px;
            border-radius: 8px;
            margin-bottom: 20px;
            border: 1px solid #f5c6cb;
        }

        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr;
                gap: 20px;
            }
            
            .form-row {
                grid-template-columns: 1fr;
            }
            
            .header h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>📸 Image Data Stamping Tool</h1>
            <p>Capture or upload images and stamp them with location and time data</p>
        </div>

        <?php
        if ($_SERVER['REQUEST_METHOD'] === 'POST' && isset($_POST['action'])) {
                            if ($_POST['action'] === 'stamp_image') {
                $uploadDir = 'uploads/';
                if (!file_exists($uploadDir)) {
                    mkdir($uploadDir, 0777, true);
                }

                $success = false;
                $error = '';

                if (isset($_FILES['image']) && $_FILES['image']['error'] === UPLOAD_ERR_OK) {
                    $tmpName = $_FILES['image']['tmp_name'];
                    $originalName = $_FILES['image']['name'];
                    $imageInfo = getimagesize($tmpName);
                    
                    if ($imageInfo !== false) {
                        // Create image resource based on type
                        switch ($imageInfo['mime']) {
                            case 'image/jpeg':
                                $image = imagecreatefromjpeg($tmpName);
                                break;
                            case 'image/png':
                                $image = imagecreatefrompng($tmpName);
                                break;
                            case 'image/gif':
                                $image = imagecreatefromgif($tmpName);
                                break;
                            default:
                                $error = 'Unsupported image format';
                                break;
                        }

                        if (!$error && $image) {
                            $width = imagesx($image);
                            $height = imagesy($image);

                            // Process map thumbnail if uploaded
                            $mapThumbnail = null;
                            if (isset($_FILES['map_thumbnail']) && $_FILES['map_thumbnail']['error'] === UPLOAD_ERR_OK) {
                                $mapImageInfo = getimagesize($_FILES['map_thumbnail']['tmp_name']);
                                if ($mapImageInfo !== false) {
                                    switch ($mapImageInfo['mime']) {
                                        case 'image/jpeg':
                                            $mapThumbnail = imagecreatefromjpeg($_FILES['map_thumbnail']['tmp_name']);
                                            break;
                                        case 'image/png':
                                            $mapThumbnail = imagecreatefrompng($_FILES['map_thumbnail']['tmp_name']);
                                            break;
                                        case 'image/gif':
                                            $mapThumbnail = imagecreatefromgif($_FILES['map_thumbnail']['tmp_name']);
                                            break;
                                    }
                                }
                            }

                            // Prepare stamp data
                            $latitude = $_POST['latitude'] ?? '';
                            $longitude = $_POST['longitude'] ?? '';
                            $date = $_POST['date'] ?? '';
                            $time = $_POST['time'] ?? '';
                            $address = $_POST['address'] ?? '';

                            // Format date and time to dd/mm/yyyy AM/PM GMT +05:30
                            $formattedDateTime = '';
                            if ($date && $time) {
                                // Create DateTime object from the form input values
                                $dateTime = DateTime::createFromFormat('Y-m-d H:i', $date . ' ' . $time);
                                if ($dateTime) {
                                    // Format as dd/mm/yyyy h:i AM/PM GMT +05:30 (using the exact input time)
                                    $formattedDateTime = $dateTime->format('d/m/Y h:i A') . ' GMT +05:30';
                                }
                            }

                            // Create stamp content with GIS formatting
                            $stampLines = [];
                            if ($address) {
                                // Split address by line breaks as provided in textbox
                                $addressLines = explode("\n", $address);
                                foreach ($addressLines as $line) {
                                    $line = trim($line);
                                    if (!empty($line)) {
                                        $stampLines[] = $line;
                                    }
                                }
                            }
                            
                            if ($latitude && $longitude) {
                                $stampLines[] = "Lat: {$latitude}°, Long: {$longitude}°";
                            }
                            
                            if ($formattedDateTime) {
                                $stampLines[] = $formattedDateTime;
                            }

                            if (!empty($stampLines) || $mapThumbnail) {
                                // Calculate stamp dimensions for print-ready layout
                                $fontSize = max(10, $width / 60); // Smaller font for better print quality
                                $fontFile = __DIR__ . '/arial.ttf';
                                $useBuiltInFont = !file_exists($fontFile);
                                
                                if ($useBuiltInFont) {
                                    $fontSize = 3; // Built-in font size
                                }

                                $lineHeight = $useBuiltInFont ? 18 : $fontSize + 8; // Increased line height
                                $padding = 15;
                                
                                // Calculate map thumbnail size and increased stamp height
                                $mapSize = max(80, count($stampLines) * $lineHeight + $padding);
                                $stampHeight = $mapSize + ($padding * 2); // Increased height
                                
                                // Calculate text area width (leave space for map thumbnail)
                                $textAreaWidth = $width - $mapSize - ($padding * 3);
                                
                                // Create transparent black background with white text
                                $stampBg = imagecolorallocatealpha($image, 0, 0, 0, 45); // Semi-transparent black
                                $textColor = imagecolorallocate($image, 255, 255, 255); // White text
                                
                                // Draw transparent black background rectangle (no border)
                                imagefilledrectangle($image, 0, $height - $stampHeight, $width, $height, $stampBg);

                                // Add "GPS Stamp Cam" branding above the stamp (top-right)
                                $brandingText = "GPS Stamp Cam";
                                $brandingFontSize = $useBuiltInFont ? 2 : max(8, $fontSize - 2);
                                $brandingColor = imagecolorallocate($image, 0, 150, 255); // Blue color
                                
                                // Calculate branding position (top-right, above stamp)
                                $brandingY = $height - $stampHeight - ($useBuiltInFont ? 20 : 25);
                                $brandingX = $width - ($useBuiltInFont ? 120 : 140);
                                
                                // Draw camera icon (simple geometric representation)
                                $iconSize = $useBuiltInFont ? 12 : 16;
                                $iconX = $brandingX - $iconSize - 5;
                                $iconY = $brandingY - ($useBuiltInFont ? 2 : 4);
                                
                                // Draw camera body (rectangle)
                                imagefilledrectangle($image, $iconX, $iconY, $iconX + $iconSize, $iconY + $iconSize - 4, $brandingColor);
                                // Draw camera lens (circle)
                                imagefilledellipse($image, $iconX + $iconSize/2, $iconY + $iconSize/2 - 2, $iconSize/2, $iconSize/2, $brandingColor);
                                // Draw camera flash (small rectangle)
                                imagefilledrectangle($image, $iconX + $iconSize - 3, $iconY - 2, $iconX + $iconSize, $iconY, $brandingColor);
                                
                                // Draw branding text
                                if ($useBuiltInFont) {
                                    imagestring($image, $brandingFontSize, $brandingX, $brandingY, $brandingText, $brandingColor);
                                } else {
                                    imagettftext($image, $brandingFontSize, 0, $brandingX, $brandingY, $brandingColor, $fontFile, $brandingText);
                                }

                                // Draw map thumbnail on the left side
                                if ($mapThumbnail) {
                                    $mapOrigWidth = imagesx($mapThumbnail);
                                    $mapOrigHeight = imagesy($mapThumbnail);
                                    $mapDisplaySize = $mapSize - $padding;
                                    
                                    // Resize and draw map thumbnail
                                    imagecopyresampled(
                                        $image, $mapThumbnail,
                                        $padding, $height - $stampHeight + $padding,
                                        0, 0,
                                        $mapDisplaySize, $mapDisplaySize,
                                        $mapOrigWidth, $mapOrigHeight
                                    );
                                    
                                    imagedestroy($mapThumbnail);
                                }

                                // Draw text lines with proper GIS alignment
                                $textStartX = $mapSize + ($padding * 2);
                                $y = $height - $stampHeight + $padding + ($useBuiltInFont ? 8 : $fontSize);
                                
                                foreach ($stampLines as $line) {
                                    if ($useBuiltInFont) {
                                        imagestring($image, $fontSize, $textStartX, $y, $line, $textColor);
                                    } else {
                                        imagettftext($image, $fontSize, 0, $textStartX, $y, $textColor, $fontFile, $line);
                                    }
                                    $y += $lineHeight;
                                }

                                // Save stamped image
                                $stampedFileName = 'stamped_' . time() . '_' . $originalName;
                                $stampedFilePath = $uploadDir . $stampedFileName;

                                switch ($imageInfo['mime']) {
                                    case 'image/jpeg':
                                        imagejpeg($image, $stampedFilePath, 95); // Higher quality for print
                                        break;
                                    case 'image/png':
                                        imagepng($image, $stampedFilePath);
                                        break;
                                    case 'image/gif':
                                        imagegif($image, $stampedFilePath);
                                        break;
                                }

                                if (file_exists($stampedFilePath)) {
                                    $success = true;
                                    $downloadUrl = $stampedFilePath;
                                } else {
                                    $error = 'Failed to save stamped image';
                                }
                            } else {
                                $error = 'No stamp data provided';
                            }

                            imagedestroy($image);
                        }
                    } else {
                        $error = 'Invalid image file';
                    }
                } else {
                    $error = 'No image uploaded or upload error';
                }

                if ($success) {
                    echo '<div class="success-message">✅ Image stamped successfully! <a href="' . $downloadUrl . '" download>Download Stamped Image</a></div>';
                } else {
                    echo '<div class="error-message">❌ Error: ' . $error . '</div>';
                }
            }
        }
        ?>

        <form method="POST" enctype="multipart/form-data" id="stampForm">
            <input type="hidden" name="action" value="stamp_image">
            
            <div class="main-content">
                <div class="form-section">
                    <h2>📋 Data Input</h2>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label for="latitude">Latitude (Decimal Degrees)</label>
                            <input type="text" id="latitude" name="latitude" placeholder="e.g., 23.022505" step="any">
                        </div>
                        <div class="form-group">
                            <label for="longitude">Longitude (Decimal Degrees)</label>
                            <input type="text" id="longitude" name="longitude" placeholder="e.g., 72.571365" step="any">
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label for="date">Date</label>
                            <input type="date" id="date" name="date">
                        </div>
                        <div class="form-group">
                            <label for="time">Time (24-hour format)</label>
                            <input type="time" id="time" name="time">
                        </div>
                    </div>

                    <div class="form-group">
                        <label for="address">Survey Location Address (Enter each line separately)</label>
                        <textarea id="address" name="address" rows="2" placeholder="Line 1: Street/Building Address&#10;Line 2: City, State, PIN"></textarea>
                    </div>

                    <div class="form-group">
                        <label>Map Thumbnail</label>
                        <div class="file-input-wrapper">
                            <input type="file" id="mapThumbnail" name="map_thumbnail" accept="image/*" class="file-input" onchange="previewMapThumbnail(this)">
                            <label for="mapThumbnail" class="file-input-label">
                                🗺️ Choose Map Thumbnail
                            </label>
                        </div>
                        <div id="mapPreview" style="margin-top: 10px; text-align: center;"></div>
                    </div>

                    <button type="button" class="btn location-btn" onclick="getLocation()">📍 Get Current Location</button>
                    <button type="button" class="btn" onclick="setCurrentDateTime()">🕒 Set Current Date/Time</button>

                    <div class="form-group">
                        <label>Upload Image</label>
                        <div class="file-input-wrapper">
                            <input type="file" id="imageFile" name="image" accept="image/*" class="file-input" onchange="previewImage(this)">
                            <label for="imageFile" class="file-input-label">
                                📁 Choose Image File
                            </label>
                        </div>
                    </div>

                    <div class="camera-section">
                        <button type="button" class="btn" onclick="startCamera()">📸 Use Camera</button>
                        <button type="button" class="btn" onclick="capturePhoto()" id="captureBtn" style="display:none;">📷 Capture Photo</button>
                        <button type="button" class="btn" onclick="stopCamera()" id="stopBtn" style="display:none;">🛑 Stop Camera</button>
                        <video id="camera-video" autoplay style="display:none;"></video>
                        <canvas id="camera-canvas" style="display:none;"></canvas>
                    </div>

                    <button type="submit" class="btn" id="stampBtn" disabled>🖼️ Stamp Image</button>
                </div>

                <div class="preview-section">
                    <h2>👁️ Preview</h2>
                    <div class="preview-container" id="previewContainer">
                        <p>Upload or capture an image to see preview</p>
                    </div>
                </div>
            </div>
        </form>
    </div>

    <script>
        let stream = null;

        function previewMapThumbnail(input) {
            if (input.files && input.files[0]) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const mapPreview = document.getElementById('mapPreview');
                    mapPreview.innerHTML = `<img src="${e.target.result}" alt="Map Preview" style="max-width: 100px; max-height: 100px; border: 1px solid #ddd; border-radius: 4px;">`;
                };
                reader.readAsDataURL(input.files[0]);
            }
        }

        function previewImage(input) {
            if (input.files && input.files[0]) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const previewContainer = document.getElementById('previewContainer');
                    previewContainer.innerHTML = `<img src="${e.target.result}" alt="Preview" class="preview-image">`;
                    document.getElementById('stampBtn').disabled = false;
                };
                reader.readAsDataURL(input.files[0]);
            }
        }

        function getLocation() {
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(function(position) {
                    document.getElementById('latitude').value = position.coords.latitude.toFixed(6);
                    document.getElementById('longitude').value = position.coords.longitude.toFixed(6);
                    
                    // Reverse geocoding (you might want to use a proper API)
                    fetch(`https://api.bigdatacloud.net/data/reverse-geocode-client?latitude=${position.coords.latitude}&longitude=${position.coords.longitude}&localityLanguage=en`)
                        .then(response => response.json())
                        .then(data => {
                            if (data.locality || data.city) {
                                document.getElementById('address').value = `${data.locality || data.city}, ${data.countryName}`;
                            }
                        })
                        .catch(err => console.log('Geocoding failed:', err));
                });
            } else {
                alert('Geolocation is not supported by this browser.');
            }
        }

        function setCurrentDateTime() {
            const now = new Date();
            document.getElementById('date').value = now.toISOString().split('T')[0];
            document.getElementById('time').value = now.toTimeString().split(' ')[0].slice(0, 5);
        }

        async function startCamera() {
            try {
                stream = await navigator.mediaDevices.getUserMedia({ video: { facingMode: 'environment' } });
                const video = document.getElementById('camera-video');
                video.srcObject = stream;
                video.style.display = 'block';
                document.getElementById('captureBtn').style.display = 'inline-block';
                document.getElementById('stopBtn').style.display = 'inline-block';
            } catch (err) {
                console.error('Error accessing camera:', err);
                alert('Could not access camera. Please check permissions.');
            }
        }

        function capturePhoto() {
            const video = document.getElementById('camera-video');
            const canvas = document.getElementById('camera-canvas');
            const ctx = canvas.getContext('2d');
            
            canvas.width = video.videoWidth;
            canvas.height = video.videoHeight;
            ctx.drawImage(video, 0, 0);
            
            canvas.toBlob(function(blob) {
                const file = new File([blob], 'camera-capture.jpg', { type: 'image/jpeg' });
                const dataTransfer = new DataTransfer();
                dataTransfer.items.add(file);
                document.getElementById('imageFile').files = dataTransfer.files;
                
                // Preview the captured image
                const reader = new FileReader();
                reader.onload = function(e) {
                    const previewContainer = document.getElementById('previewContainer');
                    previewContainer.innerHTML = `<img src="${e.target.result}" alt="Captured" class="preview-image">`;
                    document.getElementById('stampBtn').disabled = false;
                };
                reader.readAsDataURL(file);
                
                stopCamera();
            }, 'image/jpeg', 0.9);
        }

        function stopCamera() {
            if (stream) {
                stream.getTracks().forEach(track => track.stop());
                stream = null;
            }
            document.getElementById('camera-video').style.display = 'none';
            document.getElementById('captureBtn').style.display = 'none';
            document.getElementById('stopBtn').style.display = 'none';
        }

        // Set current date/time on page load
        window.onload = function() {
            setCurrentDateTime();
        };
    </script>
</body>
</html>
