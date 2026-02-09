<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Animal Image Study</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f7fa;
      margin: 0;
      padding: 0;
    }
    header {
      background: #2c3e50;
      color: #fff;
      padding: 20px;
      text-align: center;
    }
    main {
      max-width: 900px;
      margin: 30px auto;
      background: #fff;
      padding: 25px;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    }
    h2 {
      margin-top: 0;
    }
    .info {
      background: #eef4ff;
      padding: 15px;
      border-radius: 6px;
      margin-bottom: 20px;
      font-size: 14px;
    }
    label {
      display: block;
      margin-top: 15px;
      font-weight: bold;
    }
    input, select, textarea, button {
      width: 100%;
      padding: 10px;
      margin-top: 6px;
      border-radius: 5px;
      border: 1px solid #ccc;
      font-size: 14px;
    }
    button {
      background: #27ae60;
      color: white;
      border: none;
      cursor: pointer;
      margin-top: 20px;
    }
    button:hover {
      background: #219150;
    }
    .preview {
      margin-top: 20px;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }
    .preview img {
      width: 120px;
      height: 120px;
      object-fit: cover;
      border-radius: 6px;
      border: 1px solid #ddd;
    }
    footer {
      text-align: center;
      font-size: 13px;
      color: #666;
      margin-top: 30px;
    }
  </style>
</head>
<body><header>
  <h1>Animal Image Research Project</h1>
  <p>Help science by contributing animal images</p>
</header><main>
  <h2>Upload Animal Images</h2>  <div class="info">
    <p>
      This project collects animal images to study how humans perceive and emotionally respond to animals.
      Your participation is voluntary. Uploaded images may be used for academic and non-commercial research.
    </p>
  </div>  <form id="uploadForm">
    <label for="animalType">Animal Type</label>
    <select id="animalType" required>
      <option value="">Select an animal</option>
      <option>Dog</option>
      <option>Cat</option>
      <option>Bird</option>
      <option>Wild Animal</option>
      <option>Farm Animal</option>
      <option>Other</option>
    </select><label for="emotion">What emotion does this animal evoke?</label>
<select id="emotion" required>
  <option value="">Select emotion</option>
  <option>Happiness</option>
  <option>Fear</option>
  <option>Calmness</option>
  <option>Curiosity</option>
  <option>Neutral</option>
</select>

<label for="imageUpload">Upload Image(s)</label>
<input type="file" id="imageUpload" accept="image/*" multiple required />

<label for="notes">Optional Notes</label>
<textarea id="notes" rows="3" placeholder="Any thoughts or context about the image"></textarea>

<label>
  <input type="checkbox" id="consent" required />
  I confirm that I own this image or have permission to share it for research purposes.
</label>

<button type="submit">Submit Images</button>

  </form>  <div class="preview" id="preview"></div>
</main><footer>
  <p>© 2026 Animal Image Study | Educational & Research Use Only</p>
</footer><script>
  const imageUpload = document.getElementById('imageUpload');
  const preview = document.getElementById('preview');

  imageUpload.addEventListener('change', () => {
    preview.innerHTML = '';
    const files = imageUpload.files;
    for (const file of files) {
      const reader = new FileReader();
      reader.onload = e => {
        const img = document.createElement('img');
        img.src = e.target.result;
        preview.appendChild(img);
      };
      reader.readAsDataURL(file);
    }
  });

  document.getElementById('uploadForm').addEventListener('submit', e => {
    e.preventDefault();
    alert('Thank you! Your images have been submitted for research.');
    e.target.reset();
    preview.innerHTML = '';
  });
</script></body>
</html># Study--Animal
For those who wanna study animals
