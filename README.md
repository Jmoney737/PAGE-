<!DOCTYPE html>
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
            flex-direction: column;
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
        @media (max-width: 600px) {
            .dashboard-container {
                grid-template-columns: 1fr;
            }
            .tile {
                padding: 20px;
                min-height: 150px;
            }
            .button-group button {
                font-size: 1rem;
                padding: 10px 15px;
            }
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
    </style>
</head>
<body>
    <h1>Routine Dashboard</h1>

    <!-- Dashboard Tiles -->
    <div class="dashboard-container">
        <!-- NFC 1 - Living Room On -->
        <div class="tile">
            <i class="fas fa-tv"></i>
            <h3>NFC 1 - Living Room On</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=43a345bd-7137-4efb-bcf3-d1138b11652f')">Activate</button>
            </div>
        </div>

        <!-- NFC 2 - His closest On -->
        <div class="tile">
            <i class="fas fa-door-open"></i>
            <h3>NFC 2 - His Closet On</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=d05db4c2-a1c4-4bfa-a989-fc26dd0de7be')">Activate</button>
            </div>
        </div>

        <!-- Arrive Home Night -->
        <div class="tile">
            <i class="fas fa-home"></i>
            <h3>Arrive Home Night</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=0f437d3f-f6bb-45f4-8713-1807151995a2')">Activate</button>
            </div>
        </div>

        <!-- NFC 4 - Master Bedroom Lamps -->
        <div class="tile">
            <i class="fas fa-bed"></i>
            <h3>NFC 4 - Master Bedroom Lamps</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=62dcc403-75b7-4a9c-8d7d-544c4ac0a6ea')">Activate</button>
            </div>
        </div>

        <!-- NFC 5 - Living Room Off -->
        <div class="tile">
            <i class="fas fa-power-off"></i>
            <h3>NFC 5 - Living Room Off</h3>
            <div class="button-group">
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=63d016f8-0113-482d-967b-25bc5c79865d')">Deactivate</button>
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
                        alert("Failed to trigger routine. Status: " + response.status);
                    }
                })
                .catch(() => {
                    alert("Error connecting to the routine.");
                });
        }
    </script>
</body>
</html>
