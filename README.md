<!DOCTYPE html>
<html>
<head>
    <script src="https://aframe.io/releases/1.6.0/aframe.min.js"></script>
</head>
<body>
    <a-scene background="color:#0a0a0a">
        <a-camera>
            <a-cursor color="yellow" fuse="false"></a-cursor>
        </a-camera>

        <!-- Sun -->
        <a-sphere color="red" radius="5" position="-4 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Sun"></a-sphere>
        
        <!-- Mercury -->
        <a-sphere color="gray" radius="0.2" position="3 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Mercury_(planet)"></a-sphere>
        
        <!-- Venus -->
        <a-sphere color="orange" radius="0.5" position="5 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Venus"></a-sphere>

        <!-- Earth -->
        <a-sphere color="#0f77b6" radius="0.6" position="7 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Earth">
            <a-sphere color="#1e7b34" radius="0.6" position="0 0 0" rotation="0 0 90" opacity="0.5"></a-sphere>
        </a-sphere>
        
        <!-- Mars -->
        <a-sphere color="#d94a02" radius="0.45" position="9 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Mars"></a-sphere>
        
        <!-- Jupiter -->
        <a-sphere color="#c45b04" radius="1.8" position="12.1 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Jupiter"></a-sphere>
        <a-ring color="white" radius-outer="2.2" radius-inner="2" position="12.1 3 3" rotation="90 0 0"></a-ring>
        
        <!-- Saturn -->
        <a-sphere color="#d19258" radius="2" position="16.8 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Saturn"></a-sphere>
        <a-ring color="white" radius-outer="2.5" position="16.8 3 3" rotation="90 0 0"></a-ring>

        <!-- Uranus -->
        <a-sphere color="#bdc8f0" radius="1" position="21.75 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Uranus"></a-sphere>
        <a-ring color="white" radius-outer="2" radius-inner="1.95" position="21.75 3 3" rotation="90 0 0"></a-ring>
             
        <!-- Neptune -->
        <a-sphere color="#001075" radius="1" position="25.75 3 3" class="planet" data-link="https://en.wikipedia.org/wiki/Neptune"></a-sphere>
        <a-ring color="white" radius-outer="2" radius-inner="1.98" position="25.75 3 3" rotation="90 0 0"></a-ring>
                <a-text value="Welcome to The Milkyway!" color="white" width="40" position="0 10 0"></a-text>
                <a-text value="By Leon" color="white" width="20" position="0 -4 0"></a-text>
    </a-scene>

    <script>
        const planets = document.querySelectorAll('.planet');

        planets.forEach(planet => {
            planet.addEventListener('click', function () {
                const url = planet.getAttribute('data-link');
                window.open(url, '_blank');
            });
        });
    </script>
</body>
</html>
