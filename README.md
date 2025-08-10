<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hotel Mulya Booking Form</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
<style>
    body {
        background-color: #fdf9f0;
        font-family: 'Open Sans', sans-serif;
        color: #444;
        margin: 0;
        padding: 0;
    }
    .container {
        max-width: 800px;
        margin: 40px auto;
        padding: 40px;
        background-color: #fdf9f0;
    }
    h1 {
        font-family: 'Playfair Display', serif;
        font-size: 48px;
        color: #d9b77c;
        text-align: center;
        margin-bottom: 10px;
    }
    p.subtitle {
        text-align: center;
        font-size: 16px;
        line-height: 1.6;
        margin-bottom: 40px;
    }
    form {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
    }
    .full-width {
        grid-column: 1 / 3;
    }
    label {
        font-size: 14px;
        font-weight: 600;
        display: block;
        margin-bottom: 5px;
    }
    input, select, textarea {
        width: 100%;
        border: none;
        border-bottom: 1px solid #ccc;
        padding: 8px 0;
        font-size: 14px;
        background-color: transparent;
        font-family: inherit;
    }
    textarea {
        resize: vertical;
        min-height: 60px;
    }
    button {
        grid-column: 1 / 3;
        padding: 14px;
        background-color: #d9b77c;
        color: white;
        font-size: 16px;
        font-weight: bold;
        border: none;
        cursor: pointer;
        transition: background-color 0.3s ease;
    }
    button:hover {
        background-color: #c6a567;
    }
    img.logo {
        display: block;
        margin: 0 auto 20px;
        max-width: 120px;
    }
</style>
</head>
<body>

<div class="container">
    <img src="hotel-mulya-logo.png" alt="Hotel Mulya Logo" class="logo">
    <h1>Discover the Best of Both Worlds</h1>
    <p class="subtitle">
        Designed with your comfort in mind, all facilities—including ballrooms, meeting rooms, restaurants, and recreational areas—
        are conveniently accessible from one another. Share your vision with us, and we will assist you in creating unforgettable events.
    </p>

    <form action="https://webto.salesforce.com/servlet/servlet.WebToLead?encoding=UTF-8" method="POST">
        <input type="hidden" name="oid" value="YOUR_SALESFORCE_OID">
        
        <!-- Destination -->
        <div>
            <label for="area_sales">Destination*</label>
            <select name="Area_Sales__c" id="area_sales" required>
                <option value="">-- Select Destination --</option>
                <option value="Jakarta">Jakarta</option>
                <option value="Bandung">Bandung</option>
                <option value="Puncak">Puncak</option>
            </select>
        </div>

        <!-- Event Name -->
        <div>
            <label for="event_name">Event Name*</label>
            <input type="text" name="Event_Name__c" id="event_name" required>
        </div>

        <!-- First Name -->
        <div>
            <label for="first_name">First Name*</label>
            <input type="text" name="first_name" id="first_name" required>
        </div>

        <!-- Last Name -->
        <div>
            <label for="last_name">Last Name*</label>
            <input type="text" name="last_name" id="last_name" required>
        </div>

        <!-- Phone -->
        <div>
            <label for="phone">Phone Number*</label>
            <input type="tel" name="phone" id="phone" required>
        </div>

        <!-- Email -->
        <div>
            <label for="email">Email Address*</label>
            <input type="email" name="email" id="email" required>
        </div>

        <!-- Company -->
        <div>
            <label for="company">Company</label>
            <input type="text" name="company" id="company">
        </div>

        <!-- Number of Attendees -->
        <div>
            <label for="attendees">Number of Attendees</label>
            <input type="number" name="Jumlah_Tamu__c" id="attendees" min="1">
        </div>

        <!-- Product Interest -->
        <div class="full-width">
            <label for="product_interest">Product Interest</label>
            <select name="Product_Interest__c" id="product_interest" multiple size="6">
                <option value="Ballroom">Ballroom</option>
                <option value="Resto Buffet">Resto Buffet</option>
                <option value="Meeting Room">Meeting Room</option>
                <option value="Standard Room - No Breakfast">Standard Room - No Breakfast</option>
                <option value="Standard Room - Breakfast">Standard Room - Breakfast</option>
                <option value="Deluxe Room - No Breakfast">Deluxe Room - No Breakfast</option>
                <option value="Deluxe Room - Breakfast">Deluxe Room - Breakfast</option>
                <option value="Deluxe Room - No Breakfast - City View">Deluxe Room - No Breakfast - City View</option>
                <option value="Deluxe Room - Breakfast - City View">Deluxe Room - Breakfast - City View</option>
                <option value="Deluxe Room - No Breakfast - Park View">Deluxe Room - No Breakfast - Park View</option>
                <option value="Deluxe Room - Breakfast - Park View">Deluxe Room - Breakfast - Park View</option>
                <option value="Family Room - Breakfast - Pool View">Family Room - Breakfast - Pool View</option>
                <option value="President Suite">President Suite</option>
                <option value="Private VIP Room">Private VIP Room</option>
            </select>
        </div>

        <!-- Add-on Facility -->
        <div class="full-width">
            <label for="add_on">Add-on Facility</label>
            <select name="Add_On_Facility__c" id="add_on" multiple size="6">
                <option value="Private Spa">Private Spa</option>
                <option value="Gym">Gym</option>
                <option value="Laundry All In">Laundry All In</option>
                <option value="Bandung Open Trip">Bandung Open Trip</option>
                <option value="City Explore Trip">City Explore Trip</option>
                <option value="Jacuzzi">Jacuzzi</option>
            </select>
        </div>

        <!-- Check In Date -->
        <div>
            <label for="check_in">Check In Date</label>
            <input type="date" name="Check_In_Date__c" id="check_in">
        </div>

        <!-- Check Out Date -->
        <div>
            <label for="check_out">Check Out Date</label>
            <input type="date" name="Check_Out_Date__c" id="check_out">
        </div>

        <!-- Any Special Request -->
        <div class="full-width">
            <label for="request">Any Special Request</label>
            <textarea name="Any_Request_Needed__c" id="request" placeholder="Write your request here..."></textarea>
        </div>

        <!-- Submit Button -->
        <button type="submit">Submit Booking</button>
    </form>
</div>

</body>
</html>
