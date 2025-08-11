<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Hotel Mulya Booking Form</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
<style>
  :root{
    --gold: #d9b77c;
    --gold-dark: #c6a567;
    --bg: #fdf9f0;
    --text: #333;
    --muted: #6b6b6b;
  }
  html,body{height:100%;margin:0;font-family:'Open Sans',sans-serif;background:var(--bg);color:var(--text)}
  .wrap{max-width:820px;margin:40px auto;padding:36px}
  .card{background:var(--bg);border-radius:12px;padding:36px;box-shadow:0 6px 30px rgba(0,0,0,0.06)}
  .logo{display:block;margin:0 auto 18px;max-width:140px}
  h1{font-family:'Playfair Display',serif;font-size:40px;color:var(--gold);text-align:center;margin:6px 0 8px}
  p.lead{text-align:center;color:var(--muted);margin:0 0 26px}
  form{display:grid;grid-template-columns:1fr 1fr;gap:20px}
  label{display:block;font-weight:600;font-size:13px;margin-bottom:6px}
  input, select, textarea{
    width:100%;padding:10px;border:none;border-bottom:1px solid #e6e6e6;background:transparent;font-size:14px;color:var(--text);
    box-sizing:border-box;
  }
  select[multiple]{min-height:110px}
  textarea{min-height:90px;resize:vertical;padding-top:10px}
  .full{grid-column:1 / 3}
  .btn{grid-column:1 / 3;margin-top:6px;padding:14px;background:var(--gold);border:none;border-radius:8px;color:#fff;font-weight:700;font-size:16px;cursor:pointer}
  .btn:hover{background:var(--gold-dark)}
  @media(max-width:720px){
    form{grid-template-columns:1fr}
    .full{grid-column:1}
  }
</style>
</head>
<body>
  <div class="wrap">
    <div class="card">
      <img src="hotel-mulya-logo.png" alt="Hotel Mulya" class="logo">

      <h1>Discover the Best of Both Worlds</h1>
      <p class="lead">Share your vision with us — from elegant events to comfortable stays. Fill the form below and our team will contact you.</p>

      <form id="bookingForm" action="https://webto.salesforce.com/servlet/servlet.WebToLead?encoding=UTF-8&orgId=00DNS00000IaWdK" method="POST">
        <input type="hidden" name="oid" value="00DNS00000IaWdK">
        <input type="hidden" name="retURL" value="http://hotelmulya.com/thank-you">

        <div>
          <label for="destination">Destination *</label>
          <select id="destination" name="Area_Sales__c" required>
            <option value="">-- Select Destination --</option>
            <option value="Jakarta">Jakarta</option>
            <option value="Bandung">Bandung</option>
            <option value="Puncak">Puncak</option>
          </select>
        </div>

        <div>
          <label for="event_name">Event Name *</label>
          <input id="event_name" name="Event_Name__c" type="text" required>
        </div>

        <div>
          <label for="first_name">First Name *</label>
          <input id="first_name" name="first_name" type="text" required>
        </div>

        <div>
          <label for="last_name">Last Name *</label>
          <input id="last_name" name="last_name" type="text" required>
        </div>

        <div>
          <label for="phone">Phone Number *</label>
          <input id="phone" name="phone" type="tel" required>
        </div>

        <div>
          <label for="email">Email Address *</label>
          <input id="email" name="email" type="email" required>
        </div>

        <div>
          <label for="company">Company</label>
          <input id="company" name="company" type="text">
        </div>

        <div>
          <label for="attendees">Number of Attendees</label>
          <input id="attendees" name="Jumlah_Tamu__c" type="number" min="1">
        </div>

        <div class="full">
          <label for="product_interest">Product Interest</label>
          <select id="product_interest" name="Product_Interest__c" multiple>
            <option value="Ballroom">Ballroom</option>
            <option value="Resto Buffet">Resto Buffet</option>
            <option value="Meeting Room">Meeting Room</option>
            <option value="Standard Room - No Breakfast">Standard Room - No Breakfast</option>
            <option value="Standard Room - Breakfast">Standard Room - Breakfast</option>
            <option value="Deluxe Room - No Breakfast">Deluxe Room - No Breakfast</option>
            <option value="Deluxe Room - Breakfast">Deluxe Room - Breakfast</option>
            <option value="Deluxe Room - No Breakfast - City View">Deluxe Room - No Breakfast - City View</option>
            <option value="Deluxe Room - Breakfast City View">Deluxe Room - Breakfast City View</option>
            <option value="Deluxe Room - No Breakfast - Park View">Deluxe Room - No Breakfast - Park View</option>
            <option value="Deluxe Room - Breakfast - Park View">Deluxe Room - Breakfast - Park View</option>
            <option value="Family Room - Breakfast - Pool View">Family Room - Breakfast - Pool View</option>
            <option value="President Suite">President Suite</option>
            <option value="Private VIP Room">Private VIP Room</option>
          </select>
        </div>

        <div class="full">
          <label for="add_on">Add-On Facility</label>
          <select id="add_on" name="Add_On_Facility__c" multiple>
            <option value="Private Spa">Private Spa</option>
            <option value="Gym">Gym</option>
            <option value="Laundry All In">Laundry All In</option>
            <option value="Bandung Open Trip">Bandung Open Trip</option>
            <option value="City Explore Trip">City Explore Trip</option>
            <option value="Jacuzzi">Jacuzzi</option>
          </select>
        </div>

        <div>
          <label for="check_in">Check In Date (dd/mm/yyyy)</label>
          <input id="check_in" name="00NNS00001imwfl" type="text" placeholder="dd/mm/yyyy" pattern="\d{2}/\d{2}/\d{4}">
        </div>
        <div>
          <label for="check_out">Check Out Date (dd/mm/yyyy)</label>
          <input id="check_out" name="00NNS00001imPSL" type="text" placeholder="dd/mm/yyyy" pattern="\d{2}/\d{2}/\d{4}">
        </div>

        <!-- Address Fields -->
        <div class="full">
          <label for="street">Street Address</label>
          <input id="street" name="street" type="text">
        </div>
        <div>
          <label for="city">City</label>
          <input id="city" name="city" type="text">
        </div>
        <div>
          <label for="state">State/Province</label>
          <input id="state" name="state" type="text">
        </div>
        <div>
          <label for="zip">Postal Code</label>
          <input id="zip" name="zip" type="text">
        </div>
        <div>
          <label for="country">Country</label>
          <input id="country" name="country" type="text">
        </div>

        <div class="full">
          <label for="request">Any Special Request</label>
          <textarea id="request" name="Any_Request_Needed__c" placeholder="Write your request here..."></textarea>
        </div>

        <button class="btn" type="submit">Submit Booking</button>
      </form>
    </div>
  </div>
</body>
</html>
