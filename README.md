Q1.Scroll snaps
Q2.Glassomorphic card 
Q3.Tabbed navigation system
Q4.E Commerce Drop-down menu
Q5. Table
Q6.trafic signal
Q7.minmax
Q8.responsive form
Q9.Humburger menu
Q10.multi column form


Q1.Scroll snaps
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Horizontal Scroll Snap</title>

  <style>
    body {
      margin: 0;
      font-family: sans-serif;
    }

    .scroll-container {
      display: flex;
      overflow-x: scroll;
      scroll-snap-type: x mandatory;
      scroll-behavior: smooth;
      -webkit-overflow-scrolling: touch;
      height: 100vh;
    }

    .scroll-item {
      flex: 0 0 100vw;
      scroll-snap-align: start;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2rem;
      background: lightgray;
      border-right: 2px solid white;
    }

    .scroll-item:nth-child(even) {
      background: #87ceeb;
    }

    .scroll-item:nth-child(odd) {
      background: #ffb6c1;
    }
  </style>
</head>
<body>

  <div class="scroll-container">
    <div class="scroll-item">
      <img src="data:image/png;base64,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">
      <h2>product 1</h2><br>
      <p>₹ 365.0p</p><br>
    </div>
    <div class="scroll-item">Item 2</div>
    <div class="scroll-item">Item 3</div>
    <div class="scroll-item">Item 4</div>
  </div>

</body>
</html>


Q2.Glassomorphic card 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Glassmorphic Card</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
    }

    body {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #c3ec52 0%, #0ba29d 100%);
    }

    .card {
      width: 300px;
      height: 400px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 20px;
      backdrop-filter: blur(15px);
      -webkit-backdrop-filter: blur(15px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
      padding: 20px;
      color: white;
      text-align: center;
    }

    .card h2 {
      margin-bottom: 15px;
      font-size: 24px;
    }

    .card p {
      font-size: 16px;
      line-height: 1.5;
    }

    .card img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 20px;
      border: 2px solid rgba(255, 255, 255, 0.5);
    }
  </style>
</head>
<body>
  <div class="card">
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRDSFaLdWdSpAk1Z0s8bB1f4Ml5rcvvlQxfRZXWyf-_6w&s" alt="Profile Image" />
    <h2>Glassmorphic Card</h2>
    <p>This is a modern glassmorphic card using CSS blur and transparency effects. Simple and elegant!</p>
  </div>
</body>
</html>


Q3.Tabbed navigation system
!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Tabbed Navigation</title>
  <style>
    .tabs {
      display: flex;
      flex-direction: column;
      width: 300px;
      margin: auto;
    }

    .tab-labels {
      display: flex;
    }

    .tab-labels label {
      flex: 1;
      padding: 10px;
      background: #eee;
      text-align: center;
      cursor: pointer;
      border: 1px solid #ccc;
      border-bottom: none;
      transition: background 0.3s;
    }

    .tab-labels label:hover {
      background: #ddd;
    }

    input[type="radio"] {
      display: none;
    }

    .tab-content {
      border: 1px solid #ccc;
      padding: 10px;
      display: none;
    }

    #tab1:checked ~ .contents #content1,
    #tab2:checked ~ .contents #content2,
    #tab3:checked ~ .contents #content3 {
      display: block;
    }

    #tab1:checked ~ .tab-labels label[for="tab1"],
    #tab2:checked ~ .tab-labels label[for="tab2"],
    #tab3:checked ~ .tab-labels label[for="tab3"] {
      background: #fff;
      font-weight: bold;
    }
  </style>
</head>
<body>

<div class="tabs">
  <input type="radio" name="tab" id="tab1" checked>
  <input type="radio" name="tab" id="tab2">
  <input type="radio" name="tab" id="tab3">

  <div class="tab-labels">
    <label for="tab1">Tab 1</label>
    <label for="tab2">Tab 2</label>
    <label for="tab3">Tab 3</label>
  </div>

  <div class="contents">
    <div class="tab-content" id="content1">
      <img src="https://newprofilepic.photo-cdn.net//assets/images/article/profile.jpg?90af0c8" width="200px">
      <p> Tab 1.</p>
    </div>
    <div class="tab-content" id="content2">
      <img src="https://newprofilepic.photo-cdn.net//assets/images/article/profile.jpg?90af0c8" width="200px">
      <p>This is content for Tab 2.</p>
    </div>
    <div class="tab-content" id="content3">
      <img src="https://newprofilepic.photo-cdn.net//assets/images/article/profile.jpg?90af0c8" width="200px">
      <p>This is content for Tab 3.</p>
    </div>
  </div>
</div>

</body>
</html>



Q4.E Commerce Drop-down menu
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>E-commerce Dropdown Menu</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }

    .navbar {
      background-color: #333;
      overflow: hidden;
    }

    .navbar a, .dropdown-btn {
      float: left;
      font-size: 16px;
      color: white;
      text-align: center;
      padding: 14px 20px;
      text-decoration: none;
      cursor: pointer;
    }

    .navbar a:hover, .dropdown:hover .dropdown-btn {
      background-color: #555;
    }

    .dropdown {
      float: left;
      overflow: hidden;
    }

    .dropdown-content {
      display: none;
      position: absolute;
      background-color: white;
      min-width: 160px;
      box-shadow: 0px 8px 16px rgba(0,0,0,0.2);
      z-index: 1;
    }

    .dropdown-content a {
      float: none;
      color: black;
      padding: 12px 16px;
      text-decoration: none;
      display: block;
      text-align: left;
    }

    .dropdown-content a:hover {
      background-color: #ddd;
    }

    .dropdown:hover .dropdown-content {
      display: block;
    }
  </style>
</head>
<body>

<div class="navbar">
  <a href="#">Home</a>
  <div class="dropdown">
    <button class="dropdown-btn">Men</button>
    <div class="dropdown-content">
      <a href="#">Shirts</a>
      <a href="#">Jeans</a>
      <a href="#">Shoes</a>
    </div>
  </div>

  <div class="dropdown">
    <button class="dropdown-btn">Women</button>
    <div class="dropdown-content">
      <a href="#">Tops</a>
      <a href="#">Dresses</a>
      <a href="#">Sandals</a>
    </div>
  </div>

  <div class="dropdown">
    <button class="dropdown-btn">Electronics</button>
    <div class="dropdown-content">
      <a href="#">Mobiles</a>
      <a href="#">Laptops</a>
      <a href="#">Accessories</a>
    </div>
  </div>
</div>

</body>
</html>


Q5.Table 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Table</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }

    .table-container {
      overflow-x: auto;
    }

    table {
      border-collapse: collapse;
      width: 100%;
      min-width: 800px;
    }

    thead th {
      position: sticky;
      top: 0;
      background-color: #333;
      color: white;
      padding: 10px;
      text-align: left;
      z-index: 1;
    }

    tbody td {
      padding: 10px;
      border-bottom: 1px solid #ccc;
    }

    tbody tr:nth-child(even) {
      background-color: #f9f9f9;
    }

    tbody tr:nth-child(odd) {
      background-color: #fff;
    }

    @media (max-width: 600px) {
      table {
        font-size: 14px;
      }
    }
  </style>
</head>
<body>

  <h2>Responsive Table with Sticky Header</h2>
  <div class="table-container">
    <table>
      <thead>
        <tr>
          <th>#</th>
          <th>Name</th>
          <th>Email</th>
          <th>Department</th>
          <th>Role</th>
          <th>Joining Date</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>Aniket </td><td>aniket@gmail.com</td><td>Aiml</td><td>student</td><td>2025-5-21</td></tr>
        <tr><td>2</td><td>Gayan sir</td><td>sir@gmail.com</td><td>Aiml</td><td>teacher</td><td>2024-1-1</td></tr>
        <tr><td>3</td><td>Akshada mam</td><td>Mam@gmail.com</td><td>Aiml</td><td>Lab assistant</td><td>2024-5-22</td></tr>
      </tbody>
    </table>
  </div>

</body>
</html>


Q6.Traffic light
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Traffic Light Toggle</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #111;
    }

    .traffic-light {
      width: 100px;
      background: #333;
      padding: 20px;
      border-radius: 20px;
      box-shadow: 0 0 10px #000;
    }

    .light {
      width: 60px;
      height: 60px;
      margin: 15px auto;
      border-radius: 50%;
      background: #555;
      transition: background 0.3s;
    }

    #toggle {
      display: none;
    }

    .traffic-light label {
      display: block;
      cursor: pointer;
    }

    #toggle:checked ~ .traffic-light .red {
      background: red;
    }

    #toggle:checked ~ .traffic-light .yellow {
      background: #555;
    }

    #toggle:checked ~ .traffic-light .green {
      background: #555;
    }

  
    .traffic-light:has(#toggle:checked) .yellow {
      background: yellow;
    }

    .traffic-light:has(#toggle:checked):hover .green {
      background: lime;
      background: limegreen;
    }
  </style>
</head>
<body>

  <input type="checkbox" id="toggle">
  <label for="toggle">
    <div class="traffic-light">
      <div class="light red"></div>
      <div class="light yellow"></div>
      <div class="light green"></div>
    </div>
  </label>

</body>
</html>


Q7.minmax
<!DOCTYPE html>
<html>
<head>
  <title>Input Restrictions Form</title>
</head>
<body>
  <h2>User Input Form with Restrictions</h2>
  <form>
  
    <label for="before1980">Enter a date before January 1, 1980:</label>
    <input type="date" id="before1980" name="before1980" max="1979-12-31" required>
    <br><br>

  
    <label for="after2000">Enter a date after January 1, 2000:</label>
    <input type="date" id="after2000" name="after2000" min="2000-01-02" required>
    <br><br>

  
    <label for="quantity">Enter quantity (between 1 and 5):</label>
    <input type="number" id="quantity" name="quantity" min="1" max="5" required>
    <br><br>

    <input type="submit" value="Submit">
  </form>
</body>
</html>


Q8. Responsive form 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Accessible Responsive Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      max-width: 600px;
      margin: auto;
    }

    label {
      display: block;
      margin-top: 15px;
      font-weight: bold;
    }

    select, input[type="checkbox"], input[type="radio"] {
      margin-top: 5px;
    }

    .checkbox-group, .radio-group {
      display: flex;
      flex-direction: column;
      margin-top: 5px;
    }

    @media (max-width: 600px) {
      body {
        padding: 10px;
      }
    }
  </style>
</head>
<body>
  <h2>User Information Form</h2>
  <form>

    <!-- Dropdown: Country List -->
    <label for="country">Select Your Country:</label>
    <select id="country" name="country" required>
      <option value="">--Select Country--</option>
      <option value="India">India</option>
      <option value="United States">United States</option>
      <option value="United Kingdom">United Kingdom</option>
      <option value="Canada">Canada</option>
      <option value="Australia">Australia</option>
    </select>

    <!-- Checkbox: Skills -->
    <label>Choose Your Skills:</label>
    <div class="checkbox-group" role="group" aria-labelledby="skills">
      <label><input type="checkbox" name="skills" value="HTML"> HTML</label>
      <label><input type="checkbox" name="skills" value="CSS"> CSS</label>
      <label><input type="checkbox" name="skills" value="JavaScript"> JavaScript</label>
      <label><input type="checkbox" name="skills" value="Python"> Python</label>
    </div>

    <!-- Radio: Gender -->
    <label>Gender:</label>
    <div class="radio-group" role="radiogroup" aria-labelledby="gender">
      <label><input type="radio" name="gender" value="Male" required> Male</label>
      <label><input type="radio" name="gender" value="Female"> Female</label>
      <label><input type="radio" name="gender" value="Other"> Other</label>
    </div>

    <br>
    <input type="submit" value="Submit">

  </form>
</body>
</html>


Q9.Humberger menu
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Hamburger Menu</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
    }

    nav {
      background-color: #333;
      color: white;
      padding: 10px 20px;
    }

    .menu {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .menu ul {
      list-style: none;
      display: flex;
    }

    .menu ul li {
      margin-left: 20px;
    }

    .menu ul li a {
      text-decoration: none;
      color: white;
      padding: 8px 12px;
      transition: background 0.3s;
    }

    .menu ul li a:hover {
      background-color: #575757;
      border-radius: 4px;
    }

    .hamburger {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }

    .hamburger div {
      width: 25px;
      height: 3px;
      background-color: white;
      margin: 4px 0;
    }

    @media (max-width: 768px) {
      .menu ul {
        display: none;
        flex-direction: column;
        background-color: #333;
        width: 100%;
      }

      .menu ul.show {
        display: flex;
      }

      .hamburger {
        display: flex;
      }
    }
  </style>
</head>
<body>

  <nav>
    <div class="menu">
      <h2>Logo</h2>
      <div class="hamburger" onclick="toggleMenu()">
        <div></div>
        <div></div>
        <div></div>
      </div>
      <ul id="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
  </nav>

  <script>
    function toggleMenu() {
      const links = document.getElementById('nav-links');
      links.classList.toggle('show');
    }
  </script>

</body>
</html>


Q10.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Flexbox Form</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background: #f0f4f8;
    }

    .form-container {
      max-width: 800px;
      margin: 0 auto;
      background: #fff;
      padding: 20px 30px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    h2 {
      text-align: center;
      margin-bottom: 20px;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .form-row {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
    }

    .form-group {
      flex: 1;
      min-width: 200px;
      display: flex;
      flex-direction: column;
    }

    .full-width {
      flex: 1 1 100%;
    }

    label {
      margin-bottom: 5px;
      font-weight: bold;
    }

    input,
    textarea {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      padding: 10px 20px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      align-self: flex-start;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    button:hover {
      background: #0056b3;
    }

    @media (max-width: 600px) {
      .form-row {
        flex-direction: column;
      }
    }
  </style>
</head>
<body>

  <div class="form-container">
    <h2>Contact Form</h2>
    <form>
      <div class="form-row">
        <div class="form-group">
          <label for="fname">First Name</label>
          <input type="text" id="fname" name="fname">
    
Q11.Amazon
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Amazon Clone</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header class="navbar">
    <div class="logo">Amazon</div>
    <input type="text" class="search-bar" placeholder="Search Amazon" />
    <div class="nav-links">
      <span>Sign In</span>
      <span>Orders</span>
      <span>Cart</span>
    </div>
  </header>

  <section class="banner">
    <h2>Welcome to Amazon</h2>
  </section>

  <main class="products">
    <div class="product">
      <img src="https://via.placeholder.com/150" alt="Product 1" />
      <h3>Product 1</h3>
      <p>$19.99</p>
      <button>Add to Cart</button>
    </div>
    <div class="product">
      <img src="https://via.placeholder.com/150" alt="Product 2" />
      <h3>Product 2</h3>
      <p>$29.99</p>
      <button>Add to Cart</button>
    </div>
    <div class="product">
      <img src="https://via.placeholder.com/150" alt="Product 3" />
      <h3>Product 3</h3>
      <p>$39.99</p>
      <button>Add to Cart</button>
    </div>
  </main>
</body>
</html>

CSS
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  background-color: #e3e6e6;
}

.navbar {
  background-color: #131921;
  color: white;
  padding: 10px 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

.search-bar {
  width: 50%;
  padding: 8px;
  border: none;
  border-radius: 4px;
}

.nav-links span {
  margin-left: 20px;
  cursor: pointer;
}

.banner {
  background-color: #f3a847;
  padding: 20px;
  text-align: center;
}

.products {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  padding: 20px;
}

.product {
  background-color: white;
  border-radius: 8px;
  padding: 15px;
  margin: 10px;
  width: 200px;
  text-align: center;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

.product img {
  width: 100%;
  height: auto;
}

.product button {
  margin-top: 10px;
  padding: 8px 12px;
  background-color: #ffd814;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
