**Question :**

```Design a call-to-action button with a background color, white text, and smooth hover scaling animation using transitions.```

**Code :**
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CTA Button with Popup Image</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #f4f4f4;
      font-family: sans-serif;
    }

    .cta-button {
      background-color: #007BFF;
      color: #fff;
      padding: 12px 24px;
      font-size: 16px;
      font-weight: bold;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: transform 0.3s ease, background-color 0.3s ease;
    }

    .cta-button:hover {
      transform: scale(1.05);
      background-color: #0056b3;
    }

    
    .popup-image {
      display: none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      max-width: 80%;
      max-height: 80%;
      border: 4px solid #fff;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
      z-index: 1000;
      background-color: #fff;
    }

    .overlay {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.6);
      z-index: 999;
    }
  </style>
</head>
<body>

  <button class="cta-button" onclick="showImage()">Get Started</button>

  
  <div class="overlay" onclick="hideImage()"></div>
  <img src="profile.jpg" alt="Popup" class="popup-image" id="popupImage">

  <script>
    function showImage() {
      document.querySelector('.overlay').style.display = 'block';
      document.getElementById('popupImage').style.display = 'block';
    }

    function hideImage() {
      document.querySelector('.overlay').style.display = 'none';
      document.getElementById('popupImage').style.display = 'none';
    }
  </script>

</body>
</html>
```

**Output :**

![Screenshot 2025-07-02 124635](https://github.com/user-attachments/assets/e2d1ef3d-cfb9-45db-bb80-f59939f68759)
