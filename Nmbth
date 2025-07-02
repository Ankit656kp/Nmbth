<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>MAA BHAWANI TENT HOUSE</title>

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet"/>

  <!-- Bootstrap Icons CDN for Footer -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css" rel="stylesheet">

  <!-- Google Font for Stylish Heading -->
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&display=swap" rel="stylesheet">

  <style>
    body {
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
      color: #fff;
      font-family: 'Segoe UI', sans-serif;
      padding-bottom: 80px;
    }

    header {
      background: linear-gradient(90deg, #00c6ff, #0072ff);
      color: white;
      padding: 1.2rem 1rem;
      text-align: center;
      border-bottom: 3px solid #00ffcc;
      font-family: 'Orbitron', sans-serif;
      font-size: 1.2rem;
    }

    nav {
      background: rgba(0, 0, 0, 0.7);
      padding: 10px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 1000;
      backdrop-filter: blur(5px);
      box-shadow: 0 2px 5px #00ffcc;
    }

    nav button {
      margin: 5px;
      padding: 10px 20px;
      background: #00ffcc;
      border: none;
      border-radius: 30px;
      color: #000;
      font-weight: bold;
      transition: all 0.3s ease;
      box-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffcc inset;
    }

    nav button:hover {
      background: #00d4aa;
      transform: scale(1.05);
      box-shadow: 0 0 20px #00ffcc;
    }

    section {
      padding: 20px;
      background: rgba(255, 255, 255, 0.05);
      margin: 20px 0;
      border-radius: 15px;
      box-shadow: 0 0 10px rgba(0, 255, 204, 0.2);
      backdrop-filter: blur(4px);
    }

    input, select, textarea {
      background: rgba(255, 255, 255, 0.1);
      border: 1px solid #00ffcc;
      color: #fff;
      border-radius: 10px;
      padding: 10px;
      width: 100%;
      margin-bottom: 10px;
    }

    input::placeholder {
      color: #ccc;
    }

    button {
      background-color: #00ffcc;
      border: none;
      color: black;
      font-weight: bold;
      padding: 10px 20px;
      border-radius: 25px;
      cursor: pointer;
      transition: 0.3s;
      box-shadow: 0 0 10px #00ffcc;
    }

    button:hover {
      background-color: #00d4aa;
      transform: scale(1.03);
      box-shadow: 0 0 20px #00ffcc;
    }

    footer {
      position: fixed;
      bottom: 0;
      width: 100%;
      background: #000;
      color: #00ffcc;
      text-align: center;
      padding: 10px 0;
      border-top: 1px solid #00ffcc;
      box-shadow: 0 -2px 10px #00ffcc;
    }

    .social-icons a {
      margin: 0 10px;
      font-size: 1.4rem;
    }

    .img-thumb {
      height: 80px;
      border: 1px solid #00ffcc;
      border-radius: 10px;
      margin: 5px;
    }

    .testimonial-scroll {
      display: flex;
      overflow-x: auto;
      gap: 1rem;
      padding: 1rem 0;
    }

    .testimonial-scroll img {
      max-height: 150px;
      border-radius: 10px;
      border: 2px solid #00ffcc;
    }
  </style>
</head>

<body>

  <!-- Header -->
  <header>
    <h1>MAA BHAWANI TENT HOUSE</h1>
    <small>📍 Parshurampur, Turkauliya, East Champaran, Bihar – 845437</small>
  </header>

  <!-- Menu Buttons -->
  <nav>
    <button onclick="showSection('home')">Home</button>
    <button onclick="showSection('book')">Book</button>
    <button onclick="showSection('admin')">Admin</button>
    <button onclick="showSection('search')">Search</button>
  </nav>

  <!-- Sections -->
  <main class="container py-3">
    <section id="home">
      <h3>Welcome to MAA BHAWANI TENT HOUSE</h3>
      <p>We provide tent services for all your events. Book now!</p>
      <h4 class="mt-4">Customer Testimonials</h4>
      <div class="testimonial-scroll" id="testimonialList"></div>
    </section>

    <section id="book" style="display:none">
      <h3>Customer Booking</h3>
      <input type="text" id="cname" placeholder="Name" />
      <input type="text" id="cfunc" placeholder="Function" />
      <input type="date" id="cdate" />
      <input type="tel" id="ccontact" placeholder="Contact" />
      <button onclick="sendToWhatsApp()">Send to WhatsApp</button>
    </section>

    <section id="admin" style="display:none">
      <h3>Admin Panel</h3>
      <div id="adminLogin">
        <input type="password" id="adminkey" placeholder="Enter Admin Key" />
        <button onclick="checkAdmin()">Enter</button>
      </div>
      <div id="adminPanel" style="display:none">
        <h5>Add or Update Booking</h5>
        <input type="text" id="bcode" placeholder="Booking Code (or leave blank)" />
        <input type="text" id="bname" placeholder="Customer Name" />
        <input type="tel" id="bphone" placeholder="Phone Number" />
        <input type="number" id="btotal" placeholder="Total Amount" />
        <input type="number" id="bpaid" placeholder="Paid Amount" />
        <input type="file" id="bestimate" accept="image/*" />
        <input type="file" id="bfbill" accept="image/*" />
        <button onclick="searchBooking()">Search by Code</button>
        <button onclick="saveBooking()">Save Booking</button>

        <hr />
        <h5>Bookings</h5>
        <div class="d-flex flex-wrap mb-3">
          <button onclick="loadTodayBookings()">Today's</button>
          <button onclick="loadYesterdayBookings()">Yesterday's</button>
          <button onclick="loadAllBookings()">All Bookings</button>
          <button onclick="downloadPDF()">Download PDF</button>
        </div>
        <input type="text" oninput="searchByName(this.value)" placeholder="Search by name..." />
        <div id="bookingList" class="table-responsive"></div>
        <div id="totals" class="fw-bold mt-2"></div>

        <hr />
        <h5>Manage Testimonials</h5>
        <input type="file" id="testiUpload" accept="image/*">
        <button onclick="uploadTestimonial()">Upload</button>
        <div id="testimonialGallery" class="d-flex flex-wrap mt-3"></div>
      </div>
    </section>

    <section id="search" style="display:none">
      <h3>Check Booking</h3>
      <input type="text" id="scode" placeholder="Enter Booking Code" />
      <button onclick="searchBooking()">Search</button>
      <div id="sresult" class="mt-3"></div>
    </section>
  </main>

  <!-- Footer -->
  <footer>
    <div class="social-icons mb-2">
      <a href="https://www.youtube.com/" target="_blank" class="text-danger"><i class="bi bi-youtube"></i></a>
      <a href="https://wa.me/919430820346" target="_blank" class="text-success"><i class="bi bi-whatsapp"></i></a>
      <a href="https://facebook.com/" target="_blank" class="text-primary"><i class="bi bi-facebook"></i></a>
      <a href="https://instagram.com/" target="_blank" class="text-warning"><i class="bi bi-instagram"></i></a>
    </div>
    <small>&copy; <span id="year"></span> MAA BHAWANI TENT HOUSE — All Rights Reserved</small>
  </footer>

  <!-- Script placeholder -->
  <script>
document.getElementById('year').innerText = new Date().getFullYear();

function showSection(id) {
  document.querySelectorAll('section').forEach(sec => sec.style.display = 'none');
  document.getElementById(id).style.display = 'block';
}

function sendToWhatsApp() {
  const name = document.getElementById('cname').value;
  const func = document.getElementById('cfunc').value;
  const date = document.getElementById('cdate').value;
  const contact = document.getElementById('ccontact').value;
  const code = 'BKG' + Date.now();
  const msg = `*New Booking Request*%0ACode: ${code}%0AName: ${name}%0AFunction: ${func}%0ADate: ${date}%0AContact: ${contact}`;
  window.open(`https://wa.me/919430820346?text=${msg}`);
  alert(`Booking Code: ${code} — please save it for reference.`);
}

function checkAdmin() {
  const key = document.getElementById('adminkey').value;
  if (key === 'Nmbth656') {
    document.getElementById('adminLogin').style.display = 'none';
    document.getElementById('adminPanel').style.display = 'block';
  } else {
    alert('Invalid Key');
  }
}

function generateCode() {
  return 'NMBTH' + Math.floor(Math.random() * 1e6).toString().padStart(6, '0');
}

function saveBooking() {
  const name = document.getElementById("bname").value.trim();
  const phone = document.getElementById("bphone").value.trim();
  const total = parseFloat(document.getElementById("btotal").value || 0);
  const paid = parseFloat(document.getElementById("bpaid").value || 0);
  const estimateFile = document.getElementById("bestimate").files[0];
  const billFile = document.getElementById("bfbill").files[0];

  if (!name || !phone || total <= 0) {
    return alert("Please fill all required fields correctly.");
  }

  const code = document.getElementById("bcode").value || generateCode();
  const reader1 = new FileReader();
  const reader2 = new FileReader();

  reader1.onloadend = () => {
    const estimate = reader1.result || "";
    reader2.onloadend = () => {
      const bill = reader2.result || "";
      const data = {
        name, phone, total, paid,
        estimate, bill,
        date: new Date().toISOString().slice(0, 10)
      };
      localStorage.setItem(code, JSON.stringify(data));
      alert(`Saved! Booking code: ${code}`);
      if (confirm("Send booking to customer on WhatsApp?")) {
        const msg = `Hi ${data.name},\nYour booking is confirmed.\nCode: ${code}\nTotal: ₹${data.total}\nPaid: ₹${data.paid}`;
        window.open(`https://wa.me/91${data.phone}?text=${encodeURIComponent(msg)}`);
      }
      resetForm();
      loadAllBookings();
    };
    if (billFile) reader2.readAsDataURL(billFile);
    else reader2.onloadend();
  };

  if (estimateFile) reader1.readAsDataURL(estimateFile);
  else reader1.onloadend();
}

function searchBooking() {
  const code = document.getElementById("bcode")?.value.trim() || document.getElementById("scode")?.value.trim();
  if (!code) return alert("Enter code to search");
  const data = JSON.parse(localStorage.getItem(code));
  if (!data) return alert("No booking found");

  if (document.getElementById("bname")) {
    document.getElementById("bcode").value = code;
    document.getElementById("bname").value = data.name;
    document.getElementById("bphone").value = data.phone;
    document.getElementById("btotal").value = data.total;
    document.getElementById("bpaid").value = data.paid;
  }

  if (document.getElementById("sresult")) {
    let imgHtml = "";
    if (data.bill) {
      imgHtml += `<div><strong>Bill Image:</strong><br><img src="${data.bill}" style="max-width:100%;height:auto;border:1px solid #ccc;margin-top:10px;border-radius:8px;"></div>`;
    } else {
      imgHtml += `<p style="color:red;">No bill image uploaded.</p>`;
    }

    document.getElementById("sresult").innerHTML = `
      <h5>${data.name}</h5>
      <p>${data.phone}</p>
      <p>Total: ₹${data.total}, Paid: ₹${data.paid}</p>
      ${imgHtml}`;
  }
}

function resetForm() {
  ["bcode", "bname", "bphone", "btotal", "bpaid", "bestimate", "bfbill"].forEach(id => {
    const el = document.getElementById(id);
    if (el) el.value = "";
  });
}

function displayBookings(filterFn = () => true) {
  const bookings = [];
  let total = 0, paid = 0;
  for (let i = 0; i < localStorage.length; i++) {
    const key = localStorage.key(i);
    if (!key.startsWith("NMBTH")) continue;
    const data = JSON.parse(localStorage.getItem(key));
    if (!filterFn(data)) continue;
    bookings.push({ code: key, ...data });
    total += data.total;
    paid += data.paid;
  }

  let html = `<table class="table table-bordered table-sm"><thead><tr><th>Code</th><th>Name</th><th>Phone</th><th>Total</th><th>Paid</th><th>Date</th><th>Actions</th></tr></thead><tbody>`;
  for (const b of bookings) {
    html += `<tr><td>${b.code}</td><td>${b.name}</td><td>${b.phone}</td><td>₹${b.total}</td><td>₹${b.paid}</td><td>${b.date}</td>
      <td><button class='btn btn-sm btn-danger' onclick='deleteBooking("${b.code}")'>🗑️</button>
      <button class='btn btn-sm btn-secondary' onclick='printBooking("${b.code}")'>🖨️</button></td></tr>`;
  }
  html += `</tbody></table>`;
  document.getElementById("bookingList").innerHTML = html;
  document.getElementById("totals").innerText = `Total: ₹${total} | Paid: ₹${paid} | Due: ₹${total - paid}`;
}

function loadAllBookings() { displayBookings(); }
function loadTodayBookings() {
  const today = new Date().toISOString().slice(0, 10);
  displayBookings(b => b.date === today);
}
function loadYesterdayBookings() {
  const yest = new Date(Date.now() - 86400000).toISOString().slice(0, 10);
  displayBookings(b => b.date === yest);
}
function searchByName(name) {
  name = name.toLowerCase();
  displayBookings(b => b.name.toLowerCase().includes(name));
}
function deleteBooking(code) {
  if (confirm("Delete this booking?")) {
    localStorage.removeItem(code);
    loadAllBookings();
  }
}
function printBooking(code) {
  const data = JSON.parse(localStorage.getItem(code));
  const { jsPDF } = window.jspdf;
  const doc = new jsPDF();
  doc.setFontSize(14);
  doc.text("Booking Receipt", 20, 20);
  doc.text(`Code: ${code}`, 20, 40);
  doc.text(`Name: ${data.name}`, 20, 50);
  doc.text(`Phone: ${data.phone}`, 20, 60);
  doc.text(`Total: ₹${data.total}`, 20, 70);
  doc.text(`Paid: ₹${data.paid}`, 20, 80);
  doc.text(`Date: ${data.date}`, 20, 90);
  doc.save(`Booking_${code}.pdf`);
}
function downloadPDF() {
  alert("Use the 🖨️ Print button for each booking to download individual PDF.");
}

function uploadTestimonial() {
  const file = document.getElementById("testiUpload").files[0];
  if (!file) return alert("Choose an image");
  const reader = new FileReader();
  reader.onload = () => {
    const arr = JSON.parse(localStorage.getItem("testimonials") || "[]");
    arr.push(reader.result);
    localStorage.setItem("testimonials", JSON.stringify(arr));
    loadTestimonials();
  };
  reader.readAsDataURL(file);
}

function loadTestimonials() {
  const list = JSON.parse(localStorage.getItem('testimonials') || '[]');
  const box = document.getElementById('testimonialList');
  if (box) {
    box.innerHTML = '';
    list.forEach(src => {
      const img = document.createElement('img');
      img.src = src;
      box.appendChild(img);
    });
  }
  const gallery = document.getElementById("testimonialGallery");
  if (gallery) {
    gallery.innerHTML = '';
    list.forEach((src, i) => {
      gallery.innerHTML += `<div><img src='${src}' class='img-thumb' /><button onclick='deleteTestimonial(${i})' class='btn btn-sm btn-danger'>🗑️</button></div>`;
    });
  }
}

function deleteTestimonial(i) {
  const arr = JSON.parse(localStorage.getItem("testimonials") || "[]");
  arr.splice(i, 1);
  localStorage.setItem("testimonials", JSON.stringify(arr));
  loadTestimonials();
}

loadTestimonials();
</script>
</body>
</html>
