<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VERGAS DATA HUB | Home</title>
    <style>
        :root { --primary: #001f3f; --accent: #007bff; --white: #ffffff; }
        body { font-family: 'Arial', sans-serif; margin: 0; background: radial-gradient(circle, #001f3f, #000); color: white; }
        header { text-align: center; padding: 50px 20px; background: rgba(0,0,0,0.5); }
        .profile-img { width: 140px; height: 140px; border-radius: 50%; border: 3px solid var(--accent); object-fit: cover; box-shadow: 0 0 20px var(--accent); }
        .container { max-width: 800px; margin: auto; padding: 20px; }
        .pricing { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 30px; }
        .card { background: rgba(255,255,255,0.1); padding: 20px; border-radius: 15px; text-align: center; border: 1px solid var(--accent); backdrop-filter: blur(5px); }
        .card h3 { margin: 0; color: var(--accent); }
        .form-box { background: white; color: #333; padding: 30px; border-radius: 20px; }
        label { display: block; margin: 10px 0 5px; font-weight: bold; }
        input, select { width: 100%; padding: 12px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 8px; box-sizing: border-box; }
        button { width: 100%; padding: 15px; background: var(--accent); color: white; border: none; border-radius: 8px; font-size: 1.1rem; cursor: pointer; font-weight: bold; }
        footer { text-align: center; padding: 30px; font-size: 0.8rem; opacity: 0.7; }
    </style>
</head>
<body>

<header>
    <img src="WhatsApp Image 2026-01-18 at 2.09.35 PM.jpeg" alt="Nana" class="profile-img">
    <h1>VERGAS DATA HUB</h1>
    <p>WELCOME! value customer I'am	<b>ADU BOAHENG MINTA (Nana)</b>. Get your affordable data here instantly!</p>
</header>

<div class="container">
    <div class="pricing">
        <div class="card"><h3>1GB</h3><p>GHS 5</p></div>
        <div class="card"><h3>2GB</h3><p>GHS 10</p></div>
        <div class="card"><h3>10GB</h3><p>GHS 50</p></div>
        <div class="card"><h3>100GB</h3><p>GHS 200</p></div>
    </div>

    <div class="form-box">
        <form id="dataForm">
            <label>Full Name</label>
            <input type="text" id="name" placeholder="Your Name" required>
            
            <label>Phone Number (Data Recipient)</label>
            <input type="tel" id="number" placeholder="05XXXXXXXX" required>
            
            <label>Network</label>
            <select id="network" required>
                <option value="MTN">MTN</option>
                <option value="Telecel">Telecel</option>
                <option value="AT">AT</option>
            </select>
            
            <label>Select Data Plan</label>
            <select id="plan" required>
                <option value="1GB (GHS 5)">1GB - GHS 5</option>
                <option value="2GB (GHS 10)">2GB - GHS 10</option>
                <option value="10GB (GHS 50)">10GB - GHS 50</option>
                <option value="100GB (GHS 200)">100GB - GHS 200</option>
            </select>

            <label>Payment Method</label>
            <select id="payment" required>
                <option value="MoMo">Mobile Money (MoMo)</option>
                <option value="Bank">Bank Transfer</option>
            </select>
            
            <button type="submit">BUY NOW</button>
        </form>
    </div>
</div>

<footer>
    <p>Website created by <b>ADU BOAHENG MINTA (Nana)</b></p>
</footer>

<script>
    document.getElementById('dataForm').addEventListener('submit', function(e) {
        e.preventDefault();
        
        // ENTER YOUR PHONE NUMBER HERE
        const myWhatsAppNumber = "233XXXXXXXXX"; 

        const name = document.getElementById('name').value;
        const num = document.getElementById('number').value;
        const net = document.getElementById('network').value;
        const plan = document.getElementById('plan').value;
        const pay = document.getElementById('payment').value;

        const message = `*VERGAS DATA HUB ORDER*%0A%0A` +
                        `*Customer:* ${name}%0A` +
                        `*Data Number:* ${num}%0A` +
                        `*Network:* ${net}%0A` +
                        `*Plan:* ${plan}%0A` +
                        `*Payment:* ${pay}`;

        window.open(`https://wa.me/${myWhatsAppNumber}?text=${message}`, '_blank');
    });
</script>

</body>
</html>
