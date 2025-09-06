<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      padding: 0;
      background: transparent;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .button-container {
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      background: none;
      border: none;
    }
    svg {
      fill: black; /* Cambia "black" por cualquier color */
      width: 60px;
      height: 60px;
    }
  </style>
</head>
<body>

<div id="playPauseButton" class="button-container">
  <!-- Ícono Play -->
  <svg id="playIcon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 36 36" style="transform: translateX(2px);">
    <path d="m12.233 7.68 15.75 10.124c.69.443.69 1.45 0 1.892L12.233 29.82a1.125 1.125 0 0 1-1.733-.947V8.627c0-.89.985-1.428 1.733-.947z"></path>
  </svg>
  <!-- Ícono Pausa -->
  <svg id="pauseIcon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 36 36" style="display: none;">
    <path d="M12 12h-4v12h4v-12zM24 12h-4v12h4v-12z"></path>
  </svg>
</div>

<script>
  const playPauseButton = document.getElementById('playPauseButton');
  const playIcon = document.getElementById('playIcon');
  const pauseIcon = document.getElementById('pauseIcon');
  let isPlaying = false;

  playPauseButton.addEventListener('click', () => {
    if (isPlaying) {
      playIcon.style.display = 'block';
      pauseIcon.style.display = 'none';
    } else {
      playIcon.style.display = 'none';
      pauseIcon.style.display = 'block';
    }
    isPlaying = !isPlaying;
  });
</script>

</body>
</html>
