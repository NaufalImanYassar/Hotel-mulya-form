<!--  Hotel Mulya Web-to-Lead Form tanpa reCAPTCHA  -->

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Hotel Mulya Booking Form</title>
<style>
    body {
        background-color: #000;
        color: #d4af37; /* warna emas */
        font-family: Arial, sans-serif;
        padding: 20px;
    }
    form {
        background-color: rgba(0,0,0,0.8);
        padding: 20px;
        border: 1px solid #d4af37;
        border-radius: 10px;
        max-width: 500px;
        margin: auto;
    }
    label {
        display: block;
        margin-top: 10px;
    }
    input, select {
        width: 100%;
        padding: 8px;
        margin-top: 5px;
        border-radius: 5px;
        border: 1px solid #d4af37;
        background-color: #111;
        color: #fff;
    }
    input[type="submit"] {
        background-color: #ad8505;
        color: #000000;
        font-weight: bold;
        cursor: pointer;
    }
    input[type="submit"]:hover {
        background-color: #b8860b;
    }
    .logo {
        text-align: center;
        margin-bottom: 20px;
    }
</style>
</head>
<body>

<div class="logo">
    <img src="hotel-mulya-logo.png" alt="Hotel Mulya" width="120">
</div>

<form action="https://webto.salesforce.com/servlet/servlet.WebToLead?encoding=UTF-8&orgId=00DNS00000IaWdK" method="POST">
    <input type="hidden" name="oid" value="00DNS00000IaWdK">
    <input type="hidden" name="retURL" value="http://hotelmulya.com/thank-you">

    <label for="first_name">First Name</label>
    <input id="first_name" maxlength="40" name="first_name" type="text">

    <label for="last_name">Last Name</label>
    <input id="last_name" maxlength="80" name="last_name" type="text">

    <label for="email">Email</label>
    <input id="email" maxlength="80" name="email" type="email">

    <label for="phone">Phone</label>
    <input id="phone" maxlength="40" name="phone" type="text">

    <label for="company">Company</label>
    <input id="company" maxlength="40" name="company" type="text">

    <label for="state">State/Province</label>
    <input id="state" maxlength="20" name="state" type="text">

    <label>Check in Date</label>
    <input id="00NNS00001imwfl" name="00NNS00001imwfl" type="date">

    <label>Check out Date</label>
    <input id="00NNS00001imPSL" name="00NNS00001imPSL" type="date">

    <label for="00NNS00001imrBR">Product Interest</label>
    <select id="00NNS00001imrBR" multiple name="00NNS00001imrBR" title="Product Interest">
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
        <option value="Ballroom">Ballroom</option>
        <option value="Resto Buffet">Resto Buffet</option>
    </select>

    <label for="00NNS00001kJADZ">Add On Facility</label>
    <select id="00NNS00001kJADZ" multiple name="00NNS00001kJADZ" title="Add On Facility">
        <option value="Private Spa">Private Spa</option>
        <option value="Gym">Gym</option>
        <option value="Laundry All In">Laundry All In</option>
        <option value="Bandung_Open_Trip">Bandung Open Trip</option>
        <option value="City Explore Trip">City Explore Trip</option>
        <option value="Jacuzzi">Jacuzzi</option>
    </select>

    <label for="00NNS00001ip1pp">Jumlah Tamu</label>
    <input id="00NNS00001ip1pp" name="00NNS00001ip1pp" type="number" min="1">

    <br><br>
    <input type="submit" value="Submit">
</form>

</body>
</html>
