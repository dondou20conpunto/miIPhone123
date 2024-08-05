# miIPhone123
pagina para ver como son de buenos el modelo que te quieres comprar ( modelos x y xr no disponibles)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modelos de iPhone</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 1em;
            text-align: center;
        }

        main {
            padding: 20px;
        }

        .search-container {
            margin-bottom: 20px;
        }

        #search-bar {
            width: 100%;
            padding: 10px;
            font-size: 16px;
        }

        .model-selector {
            margin-bottom: 20px;
        }

        #iphone-models {
            width: 100%;
            padding: 10px;
            font-size: 16px;
        }

        #model-info {
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        #model-info img {
            max-width: 100%;
            height: auto;
            border-radius: 5px;
        }

        .rating {
            margin-top: 10px;
        }

        .rating input {
            display: none;
        }

        .rating label {
            color: #ddd;
            font-size: 24px;
            cursor: pointer;
        }

        .rating input:checked ~ label {
            color: gold;
        }

        .rating input:checked ~ label ~ label {
            color: gold;
        }

        .rating label:hover,
        .rating label:hover ~ label {
            color: gold;
        }
    </style>
</head>
<body>
    <header>
        <h1>Modelos de iPhone</h1>
    </header>
    
    <main>
        <div class="search-container">
            <label for="search-bar">Buscar modelo de iPhone:</label>
            <input type="text" id="search-bar" placeholder="Buscar...">
        </div>

        <div class="model-selector">
            <label for="iphone-models">Selecciona un modelo de iPhone:</label>
            <select id="iphone-models">
                <option value="">--Selecciona--</option>
                <!-- Aquí van todos los modelos -->
                <option value="iphone-1">iPhone 1</option>
                <option value="iphone-3g">iPhone 3G</option>
                <option value="iphone-3gs">iPhone 3GS</option>
                <option value="iphone-4">iPhone 4</option>
                <option value="iphone-4s">iPhone 4S</option>
                <option value="iphone-5">iPhone 5</option>
                <option value="iphone-5c">iPhone 5C</option>
                <option value="iphone-5s">iPhone 5S</option>
                <option value="iphone-6">iPhone 6</option>
                <option value="iphone-6-plus">iPhone 6 Plus</option>
                <option value="iphone-6s">iPhone 6S</option>
                <option value="iphone-6s-plus">iPhone 6S Plus</option>
                <option value="iphone-se">iPhone SE (1ra Gen)</option>
                <option value="iphone-7">iPhone 7</option>
                <option value="iphone-7-plus">iPhone 7 Plus</option>
                <option value="iphone-8">iPhone 8</option>
                <option value="iphone-8-plus">iPhone 8 Plus</option>
                <option value="iphone-x">iPhone X</option>
                <option value="iphone-xs">iPhone XS</option>
                <option value="iphone-xs-max">iPhone XS Max</option>
                <option value="iphone-xr">iPhone XR</option>
                <option value="iphone-11">iPhone 11</option>
                <option value="iphone-11-pro">iPhone 11 Pro</option>
                <option value="iphone-11-pro-max">iPhone 11 Pro Max</option>
                <option value="iphone-se-2">iPhone SE (2da Gen)</option>
                <option value="iphone-12">iPhone 12</option>
                <option value="iphone-12-mini">iPhone 12 Mini</option>
                <option value="iphone-12-pro">iPhone 12 Pro</option>
                <option value="iphone-12-pro-max">iPhone 12 Pro Max</option>
                <option value="iphone-13">iPhone 13</option>
                <option value="iphone-13-mini">iPhone 13 Mini</option>
                <option value="iphone-13-pro">iPhone 13 Pro</option>
                <option value="iphone-13-pro-max">iPhone 13 Pro Max</option>
                <option value="iphone-se-3">iPhone SE (3ra Gen)</option>
                <option value="iphone-14">iPhone 14</option>
                <option value="iphone-14-plus">iPhone 14 Plus</option>
                <option value="iphone-14-pro">iPhone 14 Pro</option>
                <option value="iphone-14-pro-max">iPhone 14 Pro Max</option>
                <option value="iphone-15">iPhone 15</option>
                <option value="iphone-15-pro-max">iPhone 15 Pro Max</option>
            </select>
        </div>
        
        <div id="model-info">
            <!-- Información del modelo seleccionado -->
        </div>
    </main>

    <script>
        const models = [
            { name: "iPhone 1", price: "1,000,000 COP", features: "Pantalla de 3.5 pulgadas, cámara de 2 MP.", differences: "Primer modelo de iPhone, sin 3G ni GPS.", image: "images/iphone-1.jpg" },
            { name: "iPhone 3G", price: "1,200,000 COP", features: "Pantalla de 3.5 pulgadas, cámara de 2 MP, soporte 3G.", differences: "Mejora en la conectividad con 3G, diseño similar al original.", image: "images/iphone-3g.jpg" },
            { name: "iPhone 3GS", price: "1,500,000 COP", features: "Pantalla de 3.5 pulgadas, cámara de 3 MP, procesador más rápido.", differences: "Mejora en la velocidad y la cámara.", image: "images/iphone-3gs.jpg" },
            { name: "iPhone 4", price: "1,800,000 COP", features: "Pantalla Retina de 3.5 pulgadas, cámara de 5 MP, diseño de vidrio.", differences: "Introducción de la pantalla Retina, diseño más delgado.", image: "images/iphone-4.jpg" },
            { name: "iPhone 4S", price: "2,000,000 COP", features: "Pantalla Retina de 3.5 pulgadas, cámara de 8 MP, Siri.", differences: "Mejora en la cámara y la introducción de Siri.", image: "images/iphone-4s.jpg" },
            { name: "iPhone 5", price: "2,200,000 COP", features: "Pantalla de 4 pulgadas, cámara de 8 MP, procesador A6.", differences: "Pantalla más grande, diseño más ligero y delgado.", image: "images/iphone-5.jpg" },
            { name: "iPhone 5C", price: "2,500,000 COP", features: "Pantalla de 4 pulgadas, cámara de 8 MP, diseño de plástico.", differences: "Versión más económica del iPhone 5 con diseño de plástico.", image: "images/iphone-5c.jpg" },
            { name: "iPhone 5S", price: "2,800,000 COP", features: "Pantalla de 4 pulgadas, cámara de 8 MP, sensor de huellas Touch ID.", differences: "Introducción del sensor de huellas dactilares.", image: "images/iphone-5s.jpg" },
            { name: "iPhone 6", price: "3,000,000 COP", features: "Pantalla de 4.7 pulgadas, cámara de 8 MP, diseño delgado.", differences: "Pantalla más grande y diseño más delgado.", image: "images/iphone-6.jpg" },
            { name: "iPhone 6 Plus", price: "3,300,000 COP", features: "Pantalla de 5.5 pulgadas, cámara de 8 MP, estabilización óptica.", differences: "Pantalla más grande y estabilización óptica de imagen.", image: "images/iphone-6-plus.jpg" },
            { name: "iPhone 6S", price: "3,500,000 COP", features: "Pantalla de 4.7 pulgadas, cámara de 12 MP, 3D Touch.", differences: "Mejora en la cámara y la introducción de 3D Touch.", image: "images/iphone-6s.jpg" },
            { name: "iPhone 6S Plus", price: "3,800,000 COP", features: "Pantalla de 5.5 pulgadas, cámara de 12 MP, 3D Touch.", differences: "Pantalla más grande y mejoras en la cámara.", image: "images/iphone-6s-plus.jpg" },
            { name: "iPhone SE (1ra Gen)", price: "3,800,000 COP", features: "Pantalla de 4 pulgadas, cámara de 12 MP, procesador A9.", differences: "Diseño compacto con el procesador del iPhone 6S.", image: "images/iphone-se.jpg" },
            { name: "iPhone 7", price: "4,000,000 COP", features: "Pantalla de 4.7 pulgadas, cámara de 12 MP, resistencia al agua.", differences: "Mejora en la resistencia al agua y eliminación del conector para auriculares.", image: "images/iphone-7.jpg" },
            { name: "iPhone 7 Plus", price: "4,300,000 COP", features: "Pantalla de 5.5 pulgadas, cámaras duales de 12 MP, resistencia al agua.", differences: "Cámara dual y mayor tamaño en comparación con el iPhone 7.", image: "images/iphone-7-plus.jpg" },
            { name: "iPhone 8", price: "4,500,000 COP", features: "Pantalla de 4.7 pulgadas, cámara de 12 MP, carga inalámbrica.", differences: "Introducción de carga inalámbrica y vidrio en la parte posterior.", image: "images/iphone-8.jpg" },
            { name: "iPhone 8 Plus", price: "4,800,000 COP", features: "Pantalla de 5.5 pulgadas, cámaras duales de 12 MP, carga inalámbrica.", differences: "Mayor tamaño y cámaras duales.", image: "images/iphone-8-plus.jpg" },
            { name: "iPhone X", price: "5,000,000 COP", features: "Pantalla OLED de 5.8 pulgadas, cámara dual de 12 MP, Face ID.", differences: "Introducción de Face ID y diseño sin botones.", image: "images/iphone-x.jpg" },
            { name: "iPhone XS", price: "5,500,000 COP", features: "Pantalla OLED de 5.8 pulgadas, cámara dual de 12 MP, Face ID.", differences: "Mejora en la resistencia al agua y el rendimiento.", image: "images/iphone-xs.jpg" },
            { name: "iPhone XS Max", price: "5,800,000 COP", features: "Pantalla OLED de 6.5 pulgadas, cámara dual de 12 MP, Face ID.", differences: "Mayor tamaño de pantalla y batería más grande.", image: "images/iphone-xs-max.jpg" },
            { name: "iPhone XR", price: "5,500,000 COP", features: "Pantalla LCD de 6.1 pulgadas, cámara de 12 MP, Face ID.", differences: "Pantalla LCD y variedad de colores.", image: "images/iphone-xr.jpg" },
            { name: "iPhone 11", price: "6,000,000 COP", features: "Pantalla de 6.1 pulgadas, cámara dual de 12 MP, procesador A13 Bionic.", differences: "Mejora en la cámara y el rendimiento.", image: "images/iphone-11.jpg" },
            { name: "iPhone 11 Pro", price: "7,000,000 COP", features: "Pantalla OLED de 5.8 pulgadas, cámaras triples de 12 MP, procesador A13 Bionic.", differences: "Cámara triple y pantalla OLED.", image: "images/iphone-11-pro.jpg" },
            { name: "iPhone 11 Pro Max", price: "7,500,000 COP", features: "Pantalla OLED de 6.5 pulgadas, cámaras triples de 12 MP, procesador A13 Bionic.", differences: "Mayor tamaño y batería más grande.", image: "images/iphone-11-pro-max.jpg" },
            { name: "iPhone SE (2da Gen)", price: "6,500,000 COP", features: "Pantalla de 4.7 pulgadas, cámara de 12 MP, procesador A13 Bionic.", differences: "Diseño compacto con el rendimiento del iPhone 11.", image: "images/iphone-se-2.jpg" },
            { name: "iPhone 12", price: "7,000,000 COP", features: "Pantalla OLED de 6.1 pulgadas, cámara dual de 12 MP, procesador A14 Bionic.", differences: "Introducción de 5G y pantalla OLED.", image: "images/iphone-12.jpg" },
            { name: "iPhone 12 Mini", price: "6,800,000 COP", features: "Pantalla OLED de 5.4 pulgadas, cámara dual de 12 MP, procesador A14 Bionic.", differences: "Diseño compacto con las mismas características que el iPhone 12.", image: "images/iphone-12-mini.jpg" },
            { name: "iPhone 12 Pro", price: "8,000,000 COP", features: "Pantalla OLED de 6.1 pulgadas, cámaras triples de 12 MP, LiDAR.", differences: "Cámara triple y sensor LiDAR para AR.", image: "images/iphone-12-pro.jpg" },
            { name: "iPhone 12 Pro Max", price: "8,500,000 COP", features: "Pantalla OLED de 6.7 pulgadas, cámaras triples de 12 MP, LiDAR.", differences: "Mayor tamaño y capacidad de la cámara.", image: "images/iphone-12-pro-max.jpg" },
            { name: "iPhone 13", price: "8,500,000 COP", features: "Pantalla OLED de 6.1 pulgadas, cámara dual de 12 MP, procesador A15 Bionic.", differences: "Mejora en el rendimiento y la duración de la batería.", image: "images/iphone-13.jpg" },
            { name: "iPhone 13 Mini", price: "8,200,000 COP", features: "Pantalla OLED de 5.4 pulgadas, cámara dual de 12 MP, procesador A15 Bionic.", differences: "Diseño compacto con rendimiento mejorado.", image: "images/iphone-13-mini.jpg" },
            { name: "iPhone 13 Pro", price: "9,000,000 COP", features: "Pantalla ProMotion de 6.1 pulgadas, cámaras triples de 12 MP, LiDAR.", differences: "Pantalla ProMotion y mejoras en la cámara.", image: "images/iphone-13-pro.jpg" },
            { name: "iPhone 13 Pro Max", price: "9,500,000 COP", features: "Pantalla ProMotion de 6.7 pulgadas, cámaras triples de 12 MP, LiDAR.", differences: "Mayor tamaño y mejoras en la cámara.", image: "images/iphone-13-pro-max.jpg" },
            { name: "iPhone SE (3ra Gen)", price: "8,700,000 COP", features: "Pantalla de 4.7 pulgadas, cámara de 12 MP, procesador A15 Bionic.", differences: "Diseño compacto con el rendimiento del iPhone 13.", image: "images/iphone-se-3.jpg" },
            { name: "iPhone 14", price: "9,000,000 COP", features: "Pantalla OLED de 6.1 pulgadas, cámara dual de 12 MP, procesador A15 Bionic.", differences: "Mejora en la cámara y la duración de la batería.", image: "images/iphone-14.jpg" },
            { name: "iPhone 14 Plus", price: "9,500,000 COP", features: "Pantalla OLED de 6.7 pulgadas, cámara dual de 12 MP, procesador A15 Bionic.", differences: "Mayor tamaño de pantalla y batería.", image: "images/iphone-14-plus.jpg" },
            { name: "iPhone 14 Pro", price: "10,000,000 COP", features: "Pantalla ProMotion de 6.1 pulgadas, cámaras triples de 48 MP, LiDAR.", differences: "Cámara principal de 48 MP y pantalla ProMotion.", image: "images/iphone-14-pro.jpg" },
            { name: "iPhone 14 Pro Max", price: "10,500,000 COP", features: "Pantalla ProMotion de 6.7 pulgadas, cámaras triples de 48 MP, LiDAR.", differences: "Mayor tamaño y mejoras en la cámara.", image: "images/iphone-14-pro-max.jpg" },
            { name: "iPhone 15", price: "10,800,000 COP", features: "Pantalla OLED de 6.1 pulgadas, cámara dual de 48 MP, procesador A17 Bionic.", differences: "Mejora en el rendimiento y la cámara.", image: "images/iphone-15.jpg" },
            { name: "iPhone 15 Pro Max", price: "11,500,000 COP", features: "Pantalla OLED de 6.7 pulgadas, cámaras triples de 48 MP, LiDAR, procesador A17 Bionic.", differences: "Mayor tamaño y capacidades de cámara mejoradas.", image: "images/iphone-15-pro-max.jpg" }
        ];

        const select = document.getElementById('iphone-models');
        const modelInfoDiv = document.getElementById('model-info');

        select.addEventListener('change', (event) => {
            const model = event.target.value;
            const selectedModel = models.find(m => m.name.toLowerCase().replace(/ /g, '-') === model);

            if (selectedModel) {
                modelInfoDiv.innerHTML = `
                    <h2>${selectedModel.name}</h2>
                    <img src="${selectedModel.image}" alt="${selectedModel.name}">
                    <p><strong>Precio:</strong> ${selectedModel.price}</p>
                    <p><strong>Características:</strong> ${selectedModel.features}</p>
                    <p><strong>Diferencias:</strong> ${selectedModel.differences}</p>
                    <div class="rating" data-model="${selectedModel.name}">
                        <input type="radio" id="star5-${selectedModel.name}" name="rating-${selectedModel.name}" value="5">
                        <label for="star5-${selectedModel.name}">★</label>
                        <input type="radio" id="star4-${selectedModel.name}" name="rating-${selectedModel.name}" value="4">
                        <label for="star4-${selectedModel.name}">★</label>
                        <input type="radio" id="star3-${selectedModel.name}" name="rating-${selectedModel.name}" value="3">
                        <label for="star3-${selectedModel.name}">★</label>
                        <input type="radio" id="star2-${selectedModel.name}" name="rating-${selectedModel.name}" value="2">
                        <label for="star2-${selectedModel.name}">★</label>
                        <input type="radio" id="star1-${selectedModel.name}" name="rating-${selectedModel.name}" value="1">
                        <label for="star1-${selectedModel.name}">★</label>
                        <p><strong>Calificación:</strong> <span id="rating-display-${selectedModel.name}">No calificado</span></p>
                    </div>
                `;

                const ratingInputs = document.querySelectorAll(`input[name="rating-${selectedModel.name}"]`);
                const ratingDisplay = document.getElementById(`rating-display-${selectedModel.name}`);

                // Cargar calificación desde localStorage
                const storedRating = localStorage.getItem(selectedModel.name);
                if (storedRating) {
                    const storedValue = parseInt(storedRating, 10);
                    document.getElementById(`star${storedValue}-${selectedModel.name}`).checked = true;
                    ratingDisplay.textContent = `${storedValue} estrellas`;
                }

                // Guardar calificación en localStorage
                ratingInputs.forEach(input => {
                    input.addEventListener('change', (event) => {
                        const rating = event.target.value;
                        localStorage.setItem(selectedModel.name, rating);
                        ratingDisplay.textContent = `${rating} estrellas`;
                    });
                });
            } else {
                modelInfoDiv.innerHTML = '';
            }
        });

        // Función de conversión de moneda
        function convertToCOP(amountUSD) {
            const exchangeRate = 4500; // Tipo de cambio aproximado de USD a COP
            return amountUSD * exchangeRate;
        }

        // Muestra el precio en COP en el select
        const pricesInUSD = {
            "iphone-15": 2500, // Precio en USD para ejemplo
            "iphone-15-pro-max": 3000 // Precio en USD para ejemplo
        };

        function updatePrices() {
            const select = document.getElementById('iphone-models');
            for (let option of select.options) {
                if (pricesInUSD[option.value]) {
                    const priceInUSD = pricesInUSD[option.value];
                    const priceInCOP = convertToCOP(priceInUSD);
                    option.text = option.text.replace(/COP$/, `${priceInCOP.toLocaleString()} COP`);
                }
            }
        }

        updatePrices();
    </script>
</body>
</html>
