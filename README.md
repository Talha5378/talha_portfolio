# talha_portfolio
from pathlib import Path
from zipfile import ZipFile

# Define the updated HTML content
html_content = """
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Talha | Video Editor & Graphic Designer Portfolio" />
  <title>Talha | Video Editor & Designer</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }
    body {
      background-color: #0d0d0d;
      color: #fff;
      line-height: 1.6;
    }
    header {
      background: #1a1a1a;
      padding: 2rem;
      text-align: center;
    }
    header img {
      height: 80px;
      margin-bottom: 1rem;
    }
    header h1 {
      font-size: 2.5rem;
      color: #00ffe1;
    }
    header p {
      font-size: 1.1rem;
      margin-top: 0.5rem;
      color: #ccc;
    }
    section {
      padding: 2rem;
      max-width: 1000px;
      margin: auto;
    }
    .services, .portfolio {
      margin-top: 3rem;
    }
    h2 {
      color: #00ffe1;
      margin-bottom: 1rem;
      border-bottom: 2px solid #00ffe1;
      display: inline-block;
      padding-bottom: 5px;
    }
    .service-list li, .portfolio-list li {
      margin-bottom: 1rem;
    }
    .portfolio-list img, .portfolio-list video {
      max-width: 100%;
      height: auto;
      border: 2px solid #00ffe1;
      border-radius: 8px;
    }
    footer {
      background: #1a1a1a;
      padding: 1rem;
      text-align: center;
      font-size: 0.9rem;
      color: #999;
      margin-top: 3rem;
    }
    .contact {
      margin-top: 3rem;
    }
    a {
      color: #00ffe1;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <header>
    <img src="https://via.placeholder.com/150x80.png?text=Talha+Logo" alt="Talha Logo" />
    <h1>Talha</h1>
    <p>Video Editor & Graphic Designer</p>
  </header>

  <section class="about">
    <h2>About Me</h2>
    <p>I’m Talha, a creative video editor and graphic designer. I provide high-quality, eye-catching video edits and graphic visuals for brands, creators, and businesses to help them grow online.</p>
  </section>

  <section class="services">
    <h2>Services</h2>
    <ul class="service-list">
      <li>🎬 Professional Video Editing (Reels, Shorts, YouTube)</li>
      <li>🎨 Graphic Designing (Logos, Thumbnails, Posters, Social Media Posts)</li>
    </ul>
  </section>

  <section class="portfolio">
    <h2>Portfolio</h2>
    <ul class="portfolio-list">
      <li><video controls>
        <source src="https://samplelib.com/lib/preview/mp4/sample-5s.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video></li>
      <li><img src="https://via.placeholder.com/600x300.png?text=Graphic+Design+Sample" alt="Graphic Design Sample"></li>
    </ul>
  </section>

  <section class="contact">
    <h2>Contact Me</h2>
    <p>📧 Email: <a href="mailto:talhainam537@gmail.com">talhainam537@gmail.com</a></p>
    <p>📞 Phone: <a href="tel:+923223990393">0322 3990393</a></p>
  </section>

  <footer>
    <p>&copy; 2025 Talha | All rights reserved.</p>
  </footer>
</body>
</html>
"""

# Create a temporary directory and write the HTML file
output_dir = Path("/mnt/data/talha_full_portfolio")
output_dir.mkdir(parents=True, exist_ok=True)
html_file = output_dir / "index.html"
html_file.write_text(html_content)

# Create a ZIP file
zip_path = "/mnt/data/talha_full_portfolio.zip"
with ZipFile(zip_path, "w") as zipf:
    zipf.write(html_file, arcname="index.html")

zip_path
Result
'/mnt/data/talha_full_portfolio.zip'
