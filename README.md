<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Routine Dashboard</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #121212;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            transition: background-color 0.3s, color 0.3s;
        }
        .dashboard-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            width: 90%;
            max-width: 600px;
        }
        .tile {
            background-color: #1E1E1E;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 30px;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            min-height: 200px;
        }
        .tile:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
        }
        .tile i {
            font-size: 3rem;
            margin-bottom: 10px;
            color: #4CAF50;
        }
        .tile h3 {
            font-size: 1.5rem;
            margin: 10px 0;
            text-align: center;
        }
        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        .button-group button {
            border: none;
            border-radius: 10px;
            padding: 15px 20px;
            cursor: pointer;
            font-size: 1.2rem;
        }
        .button-on {
            background-color: #4CAF50;
            color: white;
        }
        .button-off {
            background-color: #f44336;
            color: white;
        }
        .tooltip {
            position: relative;
            display: inline-block;
            cursor: pointer;
        }
        .tooltip .tooltiptext {
            visibility: hidden;
            width: 200px;
            background-color: #555;
            color: #fff;
            text-align: center;
            border-radius: 6px;
            padding: 5px;
            position: absolute;
            z-index: 1;
            bottom: 125%; /* Position above the button */
            left: 50%;
            margin-left: -100px;
            opacity: 0;
            transition: opacity 0.3s;
        }
        .tooltip:hover .tooltiptext {
            visibility: visible;
            opacity: 1;
        }
    </style>
</head>
<body>
    <div class="dashboard-container">
        <!-- Kitchen Group Tile -->
        <div class="tile">
            <i class="fas fa-blender"></i>
            <h3>Kitchen Group</h3>
            <div class="button-group">
                <div class="tooltip">
                    <button class="button-on" onclick="triggerRoutine('https://example.com/kitchen-on')">On</button>
                    <span class="tooltiptext">Turns on all kitchen lights, including AMFL Kitchen, Bar 1, Cabinet L, and more.</span>
                </div>
                <div class="tooltip">
                    <button class="button-off" onclick="triggerRoutine('https://example.com/kitchen-off')">Off</button>
                    <span class="tooltiptext">Turns off all kitchen lights, including AMFL Kitchen, Bar 1, Cabinet L, and more.</span>
                </div>
            </div>
        </div>

        <!-- Living Room Group Tile -->
        <div class="tile">
            <i class="fas fa-couch"></i>
            <h3>Living Room</h3>
            <div class="button-group">
                <div class="tooltip">
                    <button class="button-on" onclick="triggerRoutine('https://example.com/living-room-on')">On</button>
                    <span class="tooltiptext">Turns on all living room devices, including FL Living Room, FR Living Room, and more.</span>
                </div>
                <div class="tooltip">
                    <button class="button-off" onclick="triggerRoutine('https://example.com/living-room-off')">Off</button>
                    <span class="tooltiptext">Turns off all living room devices, including FL Living Room, FR Living Room, and more.</span>
                </div>
            </div>
        </div>

        <!-- Office Group Tile -->
        <div class="tile">
            <i class="fas fa-chair"></i>
            <h3>Office Group</h3>
            <div class="button-group">
                <div class="tooltip">
                    <button class="button-on" onclick="triggerRoutine('https://example.com/office-on')">On</button>
                    <span class="tooltiptext">Turns on all office devices, including desk lamp, shelf lights, and fireplace.</span>
                </div>
                <div class="tooltip">
                    <button class="button-off" onclick="triggerRoutine('https://example.com/office-off')">Off</button>
                    <span class="tooltiptext">Turns off all office devices, including desk lamp, shelf lights, and fireplace.</span>
                </div>
            </div>
        </div>
    </div>

    <script>
        function triggerRoutine(url) {
            alert("Triggering routine...");
            fetch(url)
                .then(response => {
                    if (response.ok) {
                        alert("Routine triggered successfully!");
                    } else {
                        alert("Failed to trigger routine.");
                    }
                })
                .catch(() => {
                    alert("Error connecting to the routine.");
                });
        }
    </script>
</body>
</html>
