<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smartphone-Friendly Routine Dashboard</title>
    <style>
        /* General Styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 1rem 0;
        }
        .dashboard-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            padding: 1rem;
        }
        .group-header {
            grid-column: 1 / -1;
            text-align: center;
            font-size: 1.8rem;
            font-weight: bold;
            margin-bottom: 10px;
        }
        .card {
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            padding: 1rem;
            text-align: center;
        }
        .card h3 {
            margin: 0.5rem 0;
            font-size: 1.5rem;
        }

        /* Button Styling */
        .button-group {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 1rem;
        }
        .button-group button {
            border: none;
            border-radius: 5px;
            padding: 15px 20px;
            font-size: 1.2rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        .button-on {
            background-color: #4CAF50; /* Green */
            color: white;
        }
        .button-off {
            background-color: #f44336; /* Red */
            color: white;
        }
        .button-group button:hover {
            opacity: 0.9;
        }

        /* Dark Mode Styling */
        .dark-mode {
            background-color: #121212;
            color: white;
        }
        .dark-mode .card {
            background-color: #1e1e1e;
            border-color: #333;
        }
        .dark-mode .button-on {
            background-color: #66BB6A;
        }
        .dark-mode .button-off {
            background-color: #EF5350;
        }

        footer {
            text-align: center;
            padding: 1rem;
            background-color: #4CAF50;
            color: white;
            margin-top: 2rem;
        }
    </style>
</head>
<body>
    <header>
        <h1>Routine Dashboard</h1>
        <button onclick="toggleDarkMode()" style="position: absolute; top: 10px; right: 10px; background: none; color: white; border: none; font-size: 1.2rem; cursor: pointer;">
            Toggle Dark Mode
        </button>
    </header>

    <div class="dashboard-container">
        <!-- Group Headers -->
        <h2 class="group-header">Kitchen</h2>
        <div class="card">
            <h3>Kitchen Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5846a7ff-8452-4c2f-81c7-65792b5cfbcb&token=57d238c9-34e8-4bdd-9bd8-76f34bbeb544&response=html', this)">
                    <i class="fas fa-power-off"></i> On
                </button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=f909cd87-e74a-4c94-bf0a-91d88c567111&token=5405bd16-657c-487b-a635-5422deae8015&response=html', this)">
                    <i class="fas fa-power-off"></i> Off
                </button>
            </div>
        </div>

        <h2 class="group-header">Living Room</h2>
        <div class="card">
            <h3>Living Room Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=39168a11-14c6-4bfb-8504-a73578a37555&token=a2b9357b-2a6a-4277-b2ac-3fe59fc0a80e&response=html', this)">
                    <i class="fas fa-power-off"></i> On
                </button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=1f805a37-03bd-404d-b781-0d7c4f8a051c&token=f34fc986-2182-4d80-816e-4cb08e3f7578&response=html', this)">
                    <i class="fas fa-power-off"></i> Off
                </button>
            </div>
        </div>

        <h2 class="group-header">NFC</h2>
        <div class="card">
            <h3>NFC 1 - Living Room</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=43a345bd-7137-4efb-bcf3-d1138b11652f&token=48d2e3a7-60af-4973-b63e-3a183df4b9e8&response=html', this)">
                    <i class="fas fa-power-off"></i> On
                </button>
            </div>
        </div>

        <h2 class="group-header">Office</h2>
        <div class="card">
            <h3>Office Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=747403c7-9a9f-4a47-9a80-0f6923b5c4d0&token=50f5e41a-50c5-4802-9d4f-a673d38c2491&response=html', this)">
                    <i class="fas fa-power-off"></i> On
                </button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=e458094d-4c7a-42b8-8d7c-61b0bcaca741&token=1549d5d9-19ef-4a9c-bb1f-9a2f055e6a82&response=html', this)">
                    <i class="fas fa-power-off"></i> Off
                </button>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2025 Routine Dashboard</p>
    </footer>

    <script>
        function triggerRoutine(url, button) {
            button.dataset.originalText = button.innerHTML;
            button.innerHTML = "Processing...";
            fetch(url)
                .then(response => {
                    if (response.ok) {
                        alert("Routine triggered successfully!");
                    }
                })
                .finally(() => {
                    button.innerHTML = button.dataset.originalText;
                });
        }

        function toggleDarkMode() {
            document.body.classList.toggle("dark-mode");
        }
    </script>
</body>
</html>
