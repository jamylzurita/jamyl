<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Realidad Aumentada - EGO Barber Show</title>

    <!-- Importar A-Frame y AR.js -->
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://cdn.rawgit.com/jeromeetienne/ar.js/master/aframe/build/aframe-ar.min.js"></script>
    
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            overflow: hidden;
        }
        .ar-info {
            position: absolute;
            top: 20px;
            left: 20px;
            color: white;
            background: rgba(0, 0, 0, 0.5);
            padding: 10px;
            border-radius: 10px;
            z-index: 10;
        }
        .ar-info h1 {
            margin: 0;
            font-size: 24px;
        }
    </style>
</head>
<body>

    <div class="ar-info">
        <h1>Escanea el marcador Hiro</h1>
        <p>Usa tu cámara para visualizar el modelo en AR.</p>
        <p>Descarga el marcador Hiro: <a href="https://jeromeetienne.github.io/AR.js/data/images/hiro.png" target="_blank">aquí</a></p>
    </div>

    <!-- Escena AR -->
    <a-scene embedded arjs="sourceType: webcam;">
        <!-- Marcador Hiro -->
        <a-marker preset="hiro">
            <!-- Modelo 3D de un mono -->
            <a-entity
                gltf-model="url(https://cdn.aframe.io/test-models/models/monkey/monkey.gltf)"
                scale="0.5 0.5 0.5"
                position="0 0 0">
            </a-entity>
        </a-marker>
        <a-entity camera></a-entity>
    </a-scene>

</body>
</html>
