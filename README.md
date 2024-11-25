<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body class="home">
    <div class="home-content">
        <h1>Welcome to Your Audio and Video Editor</h1>
        <p>Fix and edit your files with AI tools to separate audio tracks and make custom adjustments.</p>
        <button onclick="location.href='editor.html'">Get Started</button>
    </div>
</body>
</html>
body.home {
    background-color: black;
    color: white;
    text-align: center;
    background-image: url('music-notes-animation.gif'); /* Använd en bild med musiknoter eller skapa en animerad bakgrund */
    background-size: cover;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

button {
    background-color: #007bff; /* Blå färg */
    color: white;
    padding: 15px 30px;
    border: none;
    cursor: pointer;
    font-size: 18px;
    border-radius: 5px;
}

button:hover {
    background-color: #0056b3;
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>File Editor</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body class="editor">
    <div class="editor-content">
        <h1>Edit Your Files</h1>

        <!-- Browse Button -->
        <button onclick="document.getElementById('file-input').click()">Browse my files</button>
        <input type="file" id="file-input" style="display:none" onchange="handleFileSelect(event)">
        
        <div id="file-info"></div>

        <!-- Save Button -->
        <button id="save-button" onclick="saveFile()">Save</button>
    </div>

    <script src="scripts.js"></script>
</body>
</html>
body.editor {
    background-color: black;
    color: white;
    text-align: center;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

button {
    background-color: #007bff;
    color: white;
    padding: 15px 30px;
    border: none;
    cursor: pointer;
    font-size: 18px;
    margin: 10px;
    border-radius: 5px;
}

button:hover {
    background-color: #0056b3;
}

#file-info {
    margin-top: 20px;
    font-size: 18px;
}
function handleFileSelect(event) {
    const file = event.target.files[0];
    const fileInfoDiv = document.getElementById('file-info');
    
    if (file) {
        fileInfoDiv.textContent = `Selected file: ${file.name}`;
    }
}

function saveFile() {
    alert("Your changes have been saved!"); // Här kan du senare lägga till funktioner för att spara filen.
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Audio Editor</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Audio Editor</h1>
    
    <!-- Browse files button -->
    <button onclick="document.getElementById('file-input').click()">Browse my files</button>
    <input type="file" id="file-input" style="display:none" onchange="handleFileSelect(event)">
    
    <div id="file-info"></div>

    <!-- Save button -->
    <button id="save-button" onclick="saveFile()">Save</button>

    <script>
        function handleFileSelect(event) {
            const file = event.target.files[0];
            const fileInfoDiv = document.getElementById('file-info');
            
            if (file) {
                fileInfoDiv.textContent = `Selected file: ${file.name}`;
                // Here you can add code to visualize the audio file, such as with Wavesurfer.js
            }
        }

        function saveFile() {
            alert("Changes have been saved!");
        }
    </script>
</body>
</html>
