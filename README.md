
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>BCA Question Paper</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: #fff8f3;
      color: #333;
      scroll-behavior: smooth;
    }
    header {
      background-color: #cc5500;
      color: white;
      padding: 1.5rem 1rem;
      text-align: center;
    }
    .hero {
      padding: 4rem 2rem;
      background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.6)),
        url('https://source.unsplash.com/1600x700/?education,college') center/cover no-repeat;
      color: white;
      text-align: center;
    }
    .hero h1 {
      font-size: 3rem;
      margin: 0.5rem 0;
    }
    .hero p {
      font-size: 1.2rem;
      margin-bottom: 2rem;
    }
    .hero button {
      background: #ff8c42;
      border: none;
      padding: 1rem 2rem;
      font-size: 1rem;
      color: white;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    .hero button:hover {
      background: #e67300;
    }
    .section {
      padding: 3rem 1rem;
      max-width: 1000px;
      margin: auto;
      text-align: center;
    }
    .section h2 {
      color: #cc5500;
      margin-bottom: 1rem;
    }
    .filters {
      margin-bottom: 2rem;
    }
    .filters button {
      margin: 0.3rem;
      padding: 0.7rem 1.5rem;
      border: 1px solid #cc5500;
      background: white;
      color: #cc5500;
      border-radius: 4px;
      cursor: pointer;
    }
    .filters button.active,
    .filters button:hover {
      background: #cc5500;
      color: white;
    }
    .papers {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
    }
    .paper {
      background: #fff;
      border: 1px solid #eee;
      border-left: 5px solid #cc5500;
      padding: 1rem;
      width: 280px;
      border-radius: 5px;
      text-align: left;
      text-decoration: none;
      color: inherit;
      box-shadow: 0 2px 5px rgba(0,0,0,0.05);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .paper:hover {
      transform: translateY(-5px);
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .paper h4 { margin: 0.5rem 0; }
    .paper p { font-size: 0.9rem; }

    .contact {
      background-color: #fef1e7;
      padding: 2rem 1rem;
    }
    .contact h2 { color: #cc5500; }
    .contact p { margin: 0.3rem 0; }

    footer {
      background-color: #cc5500;
      color: white;
      text-align: center;
      padding: 1rem;
    }
    .social-icons a {
      color: white;
      margin: 0 0.5rem;
      text-decoration: none;
    }

    #toTopBtn {
      position: fixed;
      bottom: 30px;
      right: 30px;
      display: none;
      background-color: #cc5500;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 50%;
      font-size: 1.2rem;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <header>
    <h1>BCA Question Paper</h1>
  </header>

  <section class="hero">
    <h1>Prepare with Confidence</h1>
    <p>All BCA question papers in one place. Download. Practice. Succeed.</p>
    <button onclick="document.getElementById('papers').scrollIntoView()">View Papers</button>
  </section>

  <section id="papers" class="section">
    <h2>Browse Question Papers</h2>
    <div class="filters">
      <button class="active" onclick="filterPapers('all')">All</button>
      <button onclick="filterPapers('year1')">1st Year</button>
      <button onclick="filterPapers('year2')">2nd Year</button>
      <button onclick="filterPapers('year3')">3rd Year</button>
    </div>
    <div class="papers">
      <a class="paper year1" href="https://drive.google.com/file/d/1UScOeIvwA1v74KIk1CPpbnw-0MiJq8Wk/view?usp=drivesdk" target="_blank">
        <h4>C program</h4>
        <p>1st Year -1st sem</p>
      </a>
      <a class="paper year1" href="https://drive.google.com/file/d/1HqLSjk3zFv5FTRJBpKK3xclDcOdBDGoZ/view?usp=drivesdk" target="_blank">
        <h4>Mathematics I</h4>
        <p>1st Year - 1st sem</p>
      </a>
      <a class="paper year2" href="pdfs/data-structures.pdf" target="_blank">
        <h4>Data Structures</h4>
        <p>2nd Year - 2024</p>
      </a>
      <a class="paper year2" href="pdfs/operating-systems.pdf" target="_blank">
        <h4>Operating Systems</h4>
        <p>2nd Year - 2023</p>
      </a>
      <a class="paper year3" href="pdfs/web-technologies.pdf" target="_blank">
        <h4>Web Technologies</h4>
        <p>3rd Year - 2024</p>
      </a>
      <a class="paper year3" href="pdfs/machine-learning.pdf" target="_blank">
        <h4>Machine Learning</h4>
        <p>3rd Year - 2023</p>
      </a>
    </div>
  </section>

  <section class="contact">
    <h2>Contact Us</h2>
    <p>Email: vishwa@bcapapers.com</p>
    <p>Phone: +91 12345 67890</p>
    <p>Address: davanagere</p>
  </section>

  <footer>
    <p>Connect with us:</p>
    <div class="social-icons">
      <a href="#">Facebook</a> |
      <a href="#">Instagram</a> |
      <a href="#">LinkedIn</a>
    </div>
    <p>&copy; 2025 BCA Question Paper. All rights reserved.</p>
  </footer>

  <button id="toTopBtn" onclick="scrollToTop()">↑</button>

  <script>
    const filterButtons = document.querySelectorAll('.filters button');
    const papers = document.querySelectorAll('.paper');

    function filterPapers(category) {
      filterButtons.forEach(btn => btn.classList.remove('active'));
      event.target.classList.add('active');
      papers.forEach(paper => {
        if (category === 'all') {
          paper.style.display = 'block';
        } else {
          paper.style.display = paper.classList.contains(category) ? 'block' : 'none';
        }
      });
    }

    window.onscroll = function() {
      document.getElementById("toTopBtn").style.display = (window.scrollY > 400) ? "block" : "none";
    };

    function scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  </script>

</body>
</html>
