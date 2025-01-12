<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to Our Home</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Bodoni+Moda:wght@400;600&display=swap');
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Open Sans', sans-serif; line-height: 1.6; color: #333; background-color: #FAF9F6; padding: 20px; }
        header { text-align: center; margin-bottom: 30px; }
        header h1 {
            font-family: 'Bodoni Moda', serif;
            font-size: 9rem;
            color: #A88C7D;
        }
        header p { font-size: 1.2rem; color: #555; }
        .smart-home-link {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #A88C7D;
            color: #FFF;
            font-weight: bold;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        .smart-home-link:hover { background-color: #946b5d; }
        .weather-widget {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: linear-gradient(135deg, #FFF, #F7F2EE);
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 15px;
            margin-bottom: 20px;
        }
        .weather-widget i {
            font-size: 3rem;
            color: #A88C7D;
        }
        .weather-widget div {
            font-size: 1.2rem;
            color: #555;
        }
        .weather-widget div strong {
            color: #A88C7D;
        }
        .section {
            background: linear-gradient(135deg, #FFF, #F7F2EE);
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
            padding: 20px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        .section h2 {
            font-family: 'Bodoni Moda', serif;
            font-size: 2rem;
            color: #A88C7D;
            margin-bottom: 10px;
            text-align: center;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .section-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-out, padding 0.3s ease-out;
        }
        .section-content.active {
            max-height: 1000px;
            padding: 10px 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Home</h1>
        <p>We’re so glad to have you here. Click on the icons for quick navigation.</p>
        <a href="https://jmoney737.github.io/Routine-Activator/" target="_blank" class="smart-home-link">Smart Home Control</a>
    </header>

    <!-- Weather Widget -->
    <div class="weather-widget" id="weather-widget">
        <i class="fas fa-cloud-sun"></i>
        <div id="weather-data">
            <p>Loading weather data...</p>
        </div>
    </div>
    <div class="search-bar"> 
        <input type="text" id="search-input" placeholder="Search for a section..." aria-label="Search for a section"> 
        <button onclick="searchSections()">Search</button> 
    </div>
    
    <div class="divider"></div>

    <!-- Appliances & Devices -->
    <div class="section">
        <h2>
            <i class="fas fa-tv"></i> Appliances & Devices
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li><strong>Thermostat:</strong> Don’t Touch.</li>
                <li><strong>Smart TV:</strong> YouTube TV, Hulu, Netflix, Disney, Prime Video.</li>
                <li>
                    <strong>Washer/Dryer:</strong> Use the AI Opti Wash & Dry Setting. Detergent is automatically dispensed. Clean filter before use.
                    <a href="#lint-filter-cleaning" style="margin-left: 5px;">See Lint Filter Cleaning Instructions</a>
                </li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Nespresso Coffee Preparation Guide -->
    <div class="section">
        <h2>
            <i class="fas fa-coffee"></i> Nespresso Coffee Preparation Guide
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ol>
                <p><strong>Note:</strong> Capsules are to the left in the jar. The automatic motor raises and lowers the machine's head when the lever is pushed up or down.</p>
                <li>Fill the water tank with fresh drinking water.</li>
                <img src="https://github.com/user-attachments/assets/b2e02e7d-1c8a-4cee-84ad-52ac8514c588" alt="Fill Water Tank">
                <li>Turn on the machine by pressing the button.</li>
                <img src="https://github.com/user-attachments/assets/797a5710-f9b1-4916-a2c6-cb403407c967" alt="Machine Button">
                <li>GREEN lights will blink while the machine is heating up.</li>
                <img src="https://github.com/user-attachments/assets/4472e73a-19de-4921-9d1b-0a32f4deea4a" alt="Heating Indicator">
                <li>Steady GREEN light indicates the machine is ready.</li>
                <img src="https://github.com/user-attachments/assets/f9577087-ca37-42a7-9068-29e00fcad0f8" alt="Ready Light">
                <li>Place a cup under the coffee outlet.</li>
                <img src="https://github.com/user-attachments/assets/1abf0322-36b9-47ab-8629-199779d02c84" alt="Place Cup">
                <li>Open the machine head by pushing the lever up.</li>
                <img src="https://github.com/user-attachments/assets/03cb69aa-3172-47e4-9511-84bfad7a0fc4" alt="Open Machine Head">
                <li>Insert a capsule, dome side down.</li>
                <li>Close the lid by pressing the lever down, then press the button to start brewing.</li>
            </ol>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Lint Filter Cleaning Instructions -->
    <div class="section" id="lint-filter-cleaning">
        <h2>
            <i class="fas fa-filter"></i> Lint Filter Cleaning Instructions
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ol>
                <li>Open the lint filter cover and pull out the lint filter.</li>
                <img src="https://github.com/user-attachments/assets/26512380-ef32-44d5-ae12-3c88316588c6" alt="Lint Filter Cover">
                <li>Avoid removing the rubber seal on the filter.</li>
                <img src="https://github.com/user-attachments/assets/18dacdf1-a21b-4aef-8b52-3ed60f90d134" alt="Rubber Seal">
                <li>Separate the outer and inner filters.</li>
                <img src="https://github.com/user-attachments/assets/2c1c4ce0-a6c2-4c5a-9e40-c09a6d7b2394" alt="Separate Filters">
                <li>Remove lint from both filters.</li>
                <li>Reassemble the filters and insert them back in place.</li>
            </ol>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Guide to Local Bars and Restaurants -->
    <div class="section">
        <h2>
            <i class="fas fa-utensils"></i> Guide to Local Bars and Restaurants
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li>
                    <strong>GreenHouse Restaurant and Bar</strong><br>
                    Enjoy New American cuisine and an award-winning bar. 
                    <a href="https://greenhouserestaurantdenton.com/" target="_blank">Visit Website</a>
                </li>
                <li>
                    <strong>Rooster's Roadhouse</strong><br>
                    Casual BBQ and burgers in a relaxed atmosphere. 
                    <a href="https://roosters-roadhouse.com/" target="_blank">Visit Website</a>
                </li>
                <li>
                    <strong>Barley & Board</strong><br>
                    A gastropub with craft beers and elevated comfort food. 
                    <a href="https://www.barleyandboard.com/" target="_blank">Visit Website</a>
                </li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Local Attractions -->
    <div class="section">
        <h2>
            <i class="fas fa-map-marker-alt"></i> Local Attractions
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li>
                    <strong>Denton Courthouse-on-the-Square Museum</strong><br>
                    Learn about local history in this iconic courthouse. 
                    <a href="https://dentoncounty.gov/Departments/Courthouse-on-the-Square" target="_blank">Visit Website</a>
                </li>
                <li>
                    <strong>Ray Roberts Lake State Park</strong><br>
                    A haven for nature enthusiasts with hiking, biking, and fishing. 
                    <a href="https://tpwd.texas.gov/state-parks/ray-roberts-lake" target="_blank">Visit Website</a>
                </li>
                <li>
                    <strong>Arts & Jazz Festival</strong><br>
                    An annual festival featuring live music, art, and local food. 
                    <a href="https://dentonjazzfest.com/" target="_blank">Visit Website</a>
                </li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Left Office Drawer -->
    <div class="section">
        <h2>
            <i class="fas fa-drawer"></i> Left Office Drawer (Image 1)
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <h3>Writing and Drawing Supplies:</h3>
            <ul>
                <li>Sharpie markers (various colors)</li>
                <li>Ballpoint pens (blue and black)</li>
                <li>Highlighters (multiple colors)</li>
            </ul>
            <h3>Office Supplies:</h3>
            <ul>
                <li>Stapler</li>
                <li>Staples</li>
                <li>Tape dispenser</li>
                <li>Scissors</li>
                <li>Push pins</li>
                <li>Gold paper clips</li>
                <li>Binder clips</li>
            </ul>
            <h3>Small Electronics:</h3>
            <ul>
                <li>Remote control</li>
                <li>SD card</li>
            </ul>
            <h3>Batteries:</h3>
            <ul>
                <li>Assorted batteries (AA, AAA, etc.)</li>
                <li>Small battery storage cases</li>
            </ul>
            <h3>Adhesives and Tools:</h3>
            <ul>
                <li>Glue bottle</li>
                <li>Roll of masking tape</li>
                <li>Knife in a leather sheath</li>
            </ul>
            <h3>Miscellaneous:</h3>
            <ul>
                <li>Small plastic containers for organization</li>
                <li>Packaged hooks or hanging supplies</li>
                <li>Notepad or sketchpad</li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Right Office Drawer -->
    <div class="section">
        <h2>
            <i class="fas fa-drawer"></i> Right Office Drawer (Image 2)
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <h3>Cables and Chargers:</h3>
            <ul>
                <li>USB, USB-C, and Lightning cables</li>
                <li>HDMI or auxiliary cables</li>
                <li>Power cords</li>
                <li>White power adapters/plugs</li>
                <li>Coiled extension cords</li>
            </ul>
            <h3>Electronic Accessories:</h3>
            <ul>
                <li>USB wall adapters</li>
                <li>Smart plugs or sockets</li>
                <li>Circular wireless charging pad</li>
                <li>Small black hub or adapter</li>
            </ul>
            <h3>Writing Supplies:</h3>
            <ul>
                <li>Markers (e.g., Sharpie)</li>
                <li>Dry-erase markers</li>
            </ul>
            <h3>Portable Electronics:</h3>
            <ul>
                <li>JBL portable speaker</li>
                <li>Earbuds or headphones</li>
                <li>Small black pouch (likely for accessories)</li>
            </ul>
            <h3>Miscellaneous:</h3>
            <ul>
                <li>Bicycle playing cards (two decks)</li>
                <li>Tape measure (yellow and black)</li>
                <li>Roll of electrical or duct tape</li>
                <li>Cylindrical containers (likely for spare parts)</li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Left Office Cabinet -->
    <div class="section">
        <h2>
            <i class="fas fa-cabinet"></i> Left Office Cabinet (Image 3)
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <h3>Top Shelf:</h3>
            <ul>
                <li>Woven basket (contains small items)</li>
                <li>Aerosol can (possibly compressed air or cleaner)</li>
                <li>Stacked black trays or storage cases</li>
                <li>White boxes (likely empty or containing small items)</li>
            </ul>
            <h3>Bottom Shelf:</h3>
            <ul>
                <li><strong>Electronics:</strong> Microprocessor tuner/amplifier, Charging station (with multiple cables)</li>
                <li><strong>Cables and Chargers:</strong> Tangled/organized cables (USB, power cords), Wall adapters</li>
                <li><strong>Accessories:</strong> LIFX smart bulb packaging, Wicker basket with small items (possibly lenses or tools), Soft pouch</li>
                <li><strong>Miscellaneous:</strong> Folded black fabric (with yellow text), Paperwork</li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Right Office Cabinet -->
    <div class="section">
        <h2>
            <i class="fas fa-cabinet"></i> Right Office Cabinet (Image 4)
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
