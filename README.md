<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Discipleship Registration - LB Church</title>
  <style>
    * { box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
    body { background: linear-gradient(135deg, #e8f0fe 0%, #d4e4f7 100%); display: flex; justify-content: center; padding: 2rem 1rem; margin: 0; min-height: 100vh; }
    .form-card { max-width: 700px; width: 100%; background: white; padding: 2.5rem; border-radius: 20px; box-shadow: 0 10px 40px rgba(0,0,0,0.15); }
    h1 { color: #1a3a5c; text-align: center; border-bottom: 4px solid #2e7daf; padding-bottom: 0.7rem; margin-top: 0; }
    .subtitle { text-align: center; color: #4a6a85; margin-bottom: 2rem; font-size: 1.1rem; }
    label { font-weight: 600; display: block; margin-top: 1.2rem; color: #1a3a5c; font-size: 0.95rem; }
    .required { color: #c0392b; margin-left: 3px; }
    input, select, textarea { width: 100%; padding: 12px 14px; margin-top: 5px; border: 2px solid #dce4ec; border-radius: 10px; font-size: 1rem; transition: 0.3s; background: #fafcff; }
    input:focus, select:focus, textarea:focus { border-color: #2e7daf; outline: none; background: white; box-shadow: 0 0 0 3px rgba(46, 125, 175, 0.15); }
    .fee-group { background: #f0f7fe; padding: 1.2rem; border-radius: 12px; margin-top: 1rem; border-left: 4px solid #2e7daf; }
    .fee-group label { margin-top: 0.5rem; }
    .radio-group { display: flex; gap: 2rem; margin-top: 8px; flex-wrap: wrap; }
    .radio-group label { font-weight: 400; display: flex; align-items: center; gap: 8px; margin-top: 0; cursor: pointer; }
    .radio-group input[type="radio"] { width: auto; margin-right: 5px; transform: scale(1.2); }
    button { background: #2e7daf; color: white; border: none; padding: 16px; width: 100%; margin-top: 2rem; border-radius: 12px; font-size: 1.2rem; font-weight: bold; cursor: pointer; transition: 0.3s; letter-spacing: 0.5px; }
    button:hover { background: #1a5a7a; transform: translateY(-2px); box-shadow: 0 6px 20px rgba(46, 125, 175, 0.4); }
    .hidden { display: none; }
    #thankYou { text-align: center; padding: 2.5rem 0; }
    #thankYou h2 { color: #1a3a5c; font-size: 2rem; }
    #thankYou p { color: #4a6a85; font-size: 1.1rem; }
    .whatsapp-btn { display: inline-block; background: #25D366; color: white; padding: 14px 32px; border-radius: 50px; text-decoration: none; font-weight: bold; margin-top: 1.5rem; transition: 0.3s; font-size: 1.1rem; }
    .whatsapp-btn:hover { background: #1da851; transform: scale(1.05); }
    .small-note { color: #888; font-size: 0.85rem; margin-top: 1.5rem; }
    .fee-amount { font-weight: 700; color: #1a5a7a; }
    @media (max-width: 600px) { .form-card { padding: 1.5rem; } .radio-group { gap: 1rem; } }
  </style>
</head>
<body>
  <div class="form-card">
    <h1>✝️ Discipleship Training</h1>
    <p class="subtitle">LB Church — Grow in faith, serve with purpose</p>

    <!-- Form -->
    <form id="discipleForm">
      <!-- 1. Full Name -->
      <label>1. Full Name <span class="required">*</span></label>
      <input type="text" id="fullName" required placeholder="Enter your full name">

      <!-- 2. Father's Name -->
      <label>2. Father's Name <span class="required">*</span></label>
      <input type="text" id="fathersName" required placeholder="Enter your father's name">

      <!-- 3. Date of Birth -->
      <label>3. Date of Birth <span class="required">*</span></label>
      <input type="date" id="dateOfBirth" required>

      <!-- 4. Address -->
      <label>4. Address <span class="required">*</span></label>
      <input type="text" id="address" required placeholder="Enter your complete address">

      <!-- 5. Your Church Name -->
      <label>5. Your Church Name <span class="required">*</span></label>
      <input type="text" id="churchName" required placeholder="Name of your church">

      <!-- 6. Your Role in the Church -->
      <label>6. Your Role in the Church</label>
      <input type="text" id="roleInChurch" placeholder="e.g., Member, Deacon, Worship Leader, etc.">

      <!-- 7. Your Church Address -->
      <label>7. Your Church Address <span class="required">*</span></label>
      <input type="text" id="churchAddress" required placeholder="Full address of your church">

      <!-- 8. Your Pastor's Name -->
      <label>8. Your Pastor's Name <span class="required">*</span></label>
      <input type="text" id="pastorsName" required placeholder="Name of your pastor">

      <!-- 9. Education -->
      <label>9. Education</label>
      <input type="text" id="education" placeholder="e.g., Bachelor's, Master's, etc.">

      <!-- 10. Mobile Number -->
      <label>10. Mobile Number <span class="required">*</span></label>
      <input type="tel" id="mobileNumber" required placeholder="e.g., 923001234567">

      <!-- 11. WhatsApp Number -->
      <label>11. WhatsApp Number <span class="required">*</span></label>
      <input type="tel" id="whatsappNumber" required placeholder="e.g., 923001234567">

      <!-- Fee Section -->
      <div class="fee-group">
        <label>12. Registration Fee (one time) <span class="required">*</span></label>
        <p style="margin: 5px 0 0 0; color: #1a5a7a; font-weight: 600;">PKR 1,000 (one-time admission fee)</p>
        <input type="hidden" id="registrationFee" value="1000">

        <label>13. Monthly Fee Selection <span class="required">*</span></label>
        <div class="radio-group">
          <label><input type="radio" name="monthlyFee" value="500" required> PKR 500/month</label>
          <label><input type="radio" name="monthlyFee" value="1000"> PKR 1,000/month</label>
        </div>

        <label>14. Payment Method <span class="required">*</span></label>
        <div class="radio-group">
          <label><input type="radio" name="paymentMethod" value="Option 1" required> Option 1 (Bank Transfer)</label>
          <label><input type="radio" name="paymentMethod" value="Option 2"> Option 2 (Easypaisa/JazzCash)</label>
        </div>
        <p style="font-size:0.85rem; color:#666; margin-top:8px;">Details for both options will be shared after registration.</p>
      </div>

      <!-- Discipleship Questions (optional but helpful) -->
      <label>Why do you want to be a disciple?</label>
      <textarea id="whyDisciple" rows="2" placeholder="Share your heart behind joining..."></textarea>

      <label>Spiritual gifts or areas of interest</label>
      <input type="text" id="spiritualGifts" placeholder="e.g., teaching, worship, outreach, prayer">

      <label>Availability for training (days/times)</label>
      <input type="text" id="availability" placeholder="e.g., Saturdays 3-5pm">

      <label>Prayer requests or special needs</label>
      <textarea id="prayerRequests" rows="2" placeholder="Any prayer requests..."></textarea>

      <button type="submit">🚀 Submit Registration</button>
    </form>

    <!-- Thank You Message -->
    <div id="thankYou" class="hidden">
      <h2>✅ Thank You, <span id="thankYouName"></span>!</h2>
      <p>Your discipleship registration has been saved.</p>
      <p style="font-weight:600; color:#1a5a7a;">📌 Registration Fee: PKR 1,000 (one-time)</p>
      <p style="font-weight:600; color:#1a5a7a;">📌 Monthly Fee: <span id="displayMonthlyFee"></span></p>
      <p style="font-weight:600; color:#1a5a7a;">📌 Payment Method: <span id="displayPaymentMethod"></span></p>
      <p style="margin-top: 1rem;">Click the button below to receive your thank-you message on WhatsApp:</p>
      <a id="whatsappLink" href="#" target="_blank" class="whatsapp-btn">📱 Get Thank-You on WhatsApp</a>
      <p class="small-note">(If the link doesn't open, copy your WhatsApp number and send us a message)</p>
    </div>
  </div>

  <script>
    const form = document.getElementById('discipleForm');
    const thankYouDiv = document.getElementById('thankYou');
    const thankYouName = document.getElementById('thankYouName');
    const whatsappLink = document.getElementById('whatsappLink');
    const displayMonthlyFee = document.getElementById('displayMonthlyFee');
    const displayPaymentMethod = document.getElementById('displayPaymentMethod');

    // REPLACE THIS WITH YOUR GOOGLE APPS SCRIPT WEB APP URL
    const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbzP-z1EQLe1OMhaZRI51H5RUw54nPxJrhJM8KsISTZNCSMLuDBhNbyCMdjHbqie61AlJA/exec';

    form.addEventListener('submit', async function(e) {
      e.preventDefault();

      // Get selected monthly fee
      const monthlyFeeRadios = document.querySelectorAll('input[name="monthlyFee"]');
      let monthlyFee = '';
      for (const radio of monthlyFeeRadios) {
        if (radio.checked) monthlyFee = radio.value;
      }

      // Get selected payment method
      const paymentRadios = document.querySelectorAll('input[name="paymentMethod"]');
      let paymentMethod = '';
      for (const radio of paymentRadios) {
        if (radio.checked) paymentMethod = radio.value;
      }

      const formData = {
        fullName: document.getElementById('fullName').value.trim(),
        fathersName: document.getElementById('fathersName').value.trim(),
        dateOfBirth: document.getElementById('dateOfBirth').value,
        address: document.getElementById('address').value.trim(),
        churchName: document.getElementById('churchName').value.trim(),
        roleInChurch: document.getElementById('roleInChurch').value.trim(),
        churchAddress: document.getElementById('churchAddress').value.trim(),
        pastorsName: document.getElementById('pastorsName').value.trim(),
        education: document.getElementById('education').value.trim(),
        mobileNumber: document.getElementById('mobileNumber').value.trim(),
        whatsappNumber: document.getElementById('whatsappNumber').value.trim(),
        registrationFee: '1000',
        monthlyFee: monthlyFee,
        paymentMethod: paymentMethod,
        whyDisciple: document.getElementById('whyDisciple').value.trim(),
        spiritualGifts: document.getElementById('spiritualGifts').value.trim(),
        availability: document.getElementById('availability').value.trim(),
        prayerRequests: document.getElementById('prayerRequests').value.trim()
      };

      // Send to Google Sheets
      try {
        const response = await fetch(SCRIPT_URL, {
          method: 'POST',
          mode: 'no-cors',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify(formData)
        });

        // Show thank-you
        thankYouName.textContent = formData.fullName;
        displayMonthlyFee.textContent = `PKR ${formData.monthlyFee}/month`;
        displayPaymentMethod.textContent = formData.paymentMethod;

        // WhatsApp message
        const cleanPhone = formData.whatsappNumber.replace(/\D/g, '');
        const message = `🙏 Thank you ${formData.fullName}! Your discipleship registration has been received. \n\n📌 Registration Fee: PKR 1,000 (one-time)\n📌 Monthly Fee: PKR ${formData.monthlyFee}/month\n📌 Payment Method: ${formData.paymentMethod}\n\nWe'll contact you soon with training details. God bless you! 🌟`;
        const encodedMsg = encodeURIComponent(message);
        whatsappLink.href = `https://wa.me/${cleanPhone}?text=${encodedMsg}`;

        form.classList.add('hidden');
        thankYouDiv.classList.remove('hidden');

      } catch (error) {
        alert('Something went wrong. Please try again or contact the church office.');
        console.error(error);
      }
    });
  </script>
</body>
</html>
