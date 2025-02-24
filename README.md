<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bienvenido</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
        h1 { color: #ffffff; }
        .btn { display: block; margin: 10px auto; padding: 15px; width: 200px; text-decoration: none; color: white; border-radius: 10px; }
        .btn.fotos { background-color: #000000; }
        .btn.videos { background-color: #000000; }
    </style>
</head>
<body>
    <h1 id="welcome"></h1>
    <a id="fotosLink" class="btn fotos" href="#">Ver Fotos</a>
    <a id="videosLink" class="btn videos" href="#">Ver Videos</a>

    <script>
        // Obtener el nombre desde la URL
        const params = new URLSearchParams(window.location.search);
        const nombre = params.get("name") || "Visitante";

        // Mostrar el nombre en la bienvenida
        document.getElementById("welcome").innerText = `¡Hola, ${nombre}!`;
        

        // Configurar enlaces con el nombre
        document.getElementById("fotosLink").href = `fotos.html?name=${nombre}`;
        document.getElementById("videosLink").href = `videos.html?name=${nombre}`;
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fotos</title>
</head>
<body>
    <h1 id="welcome"></h1>

    <script>
        const params = new URLSearchParams(window.location.search);
        const nombre = params.get("name") || "Visitante";
        document.getElementById("welcome").innerText = `Fotos de ${nombre}`;
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Videos</title>
</head>
<body>
    <h1 id="welcome"></h1>

    <script>
        const params = new URLSearchParams(window.location.search);
        const nombre = params.get("name") || "Visitante";
        document.getElementById("welcome").innerText = `Videos de ${nombre}`;
    </script>
</body>
</html>
# Recuerdame
