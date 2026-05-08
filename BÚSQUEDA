<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Consulta de Evaluaciones UDEP</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f2f5;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        .contenedor {
            width: 100%;
            max-width: 600px;
        }

        /* Las dos ventanas pequeñas de arriba */
        .fila-superior {
            display: flex;
            gap: 15px;
            margin-bottom: 15px;
        }

        .ventana-pequena {
            flex: 1;
            background: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            border-top: 5px solid #003057; /* Azul UDEP */
        }

        /* Ventana de resultados grande abajo */
        .ventana-grande {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            min-height: 200px;
        }

        label {
            display: block;
            font-weight: bold;
            font-size: 12px;
            color: #003057;
            margin-bottom: 5px;
        }

        input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
            font-size: 16px;
            text-transform: uppercase;
        }

        button {
            width: 100%;
            padding: 12px;
            background-color: #003057;
            color: white;
            border: none;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            margin-bottom: 15px;
        }

        button:hover {
            background-color: #004a85;
        }

        .resultado-item {
            padding: 12px;
            border-bottom: 1px solid #eee;
            line-height: 1.6;
        }

        .disponible { color: #28a745; font-weight: bold; }
        .no-disponible { color: #dc3545; font-weight: bold; }
    </style>
</head>
<body>

<div class="contenedor">
    <div class="fila-superior">
        <div class="ventana-pequena">
            <label>SIGLA DEL CURSO</label>
            <input type="text" id="curso" placeholder="Ej: A1MT1">
        </div>
        <div class="ventana-pequena">
            <label>SECCIÓN</label>
            <input type="text" id="seccion" placeholder="Ej: C">
        </div>
    </div>

    <button onclick="buscarEnExcel()">CONSULTAR ESTADO</button>

    <div class="ventana-grande" id="pantallaResultados">
        <h3 style="margin-top: 0; color: #003057;">Resultados:</h3>
        <div id="listaResultados">
            <p style="color: #888;">Ingresa los datos arriba para verificar disponibilidad.</p>
        </div>
    </div>
</div>

<script>
    function buscarEnExcel() {
        const sigla = document.getElementById('curso').value.trim().toUpperCase();
        const seccion = document.getElementById('seccion').value.trim().toUpperCase();
        const lista = document.getElementById('listaResultados');

        if (sigla === "" || seccion === "") {
            alert("Por favor, completa la sigla y la sección.");
            return;
        }

        lista.innerHTML = "<p>Buscando en OneDrive...</p>";

        // --- LÓGICA DE SIMULACIÓN (Esto se reemplaza con la conexión real) ---
        setTimeout(() => {
            // Aquí definimos los datos de prueba
            const datos = {
                practica: "RECOJO / VENCE 12.05.2026 / TURNO PM",
                reclamo1: "DISPONIBLE",
                reclamo2: "NO DISPONIBLE"
            };

            lista.innerHTML = `
                <div class="resultado-item">
                    <strong>Práctica 1:</strong> ${datos.practica}
                </div>
                <div class="resultado-item">
                    <strong>Primer reclamo:</strong> 
                    <span class="${datos.reclamo1 === 'DISPONIBLE' ? 'disponible' : 'no-disponible'}">${datos.reclamo1}</span>
                </div>
                <div class="resultado-item">
                    <strong>Segundo reclamo:</strong> 
                    <span class="${datos.reclamo2 === 'DISPONIBLE' ? 'disponible' : 'no-disponible'}">${datos.reclamo2}</span>
                </div>
            `;
        }, 600);
    }
</script>

</body>
</html>
