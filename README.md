<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TRÁMITES ADMINISTRATIVOS PLANTEL CEYTEM</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }
        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 10px;
        }
        .container {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        .box {
            background-color: white;
            width: 250px;
            margin: 10px;
            padding: 20px;
            text-align: center;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .box h3 {
            margin-bottom: 15px;
        }
        .box button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 5px;
            font-size: 14px;
        }
        .box button:hover {
            background-color: #45a049;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.4);
            padding-top: 60px;
        }
        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            max-width: 600px;
            border-radius: 8px;
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }
        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <header>
        <h1>TRÁMITES ADMINISTRATIVOS PLANTEL CEYTEM</h1>
        <img src="cecyy.jpeg" style="width:400px;height:400px;">
    </header>

    <div class="container">
        <div class="box">
            <h3>Eventos académicos</h3>
            <button id="btnEventos">Ver fechas de eventos</button>
        </div>
        <div class="box">
            <h3>Temporadas de Exámenes</h3>
            <button id="btnExamenes">Ver fechas de exámenes</button>
        </div>
        <div class="box">
            <h3>Horarios</h3>
            <button id="btnHorarios">Ver horarios</button>
        </div>
    </div>

    <p style="text-align: center; padding: 20px;">En esta página se encontrará información sobre el plantel dedicada para los alumnos, cualquier duda de alguna fecha de exámenes, eventos e incluso horarios.</p>

    <!-- Modal para eventos -->
    <div id="modalEventos" class="modal">
        <div class="modal-content">
            <span class="close" id="closeEventos">&times;</span>
            <h2>Fechas de eventos académicos</h2>
            <ul>
                <li>Evento 1: 20 de abril - Conferencia sobre Investigación</li>
                <li>Evento 2: 5 de mayo - Taller de Innovación Educativa</li>
                <li>Evento 3: 15 de junio - Feria de Ciencia y Tecnología</li>
            </ul>
        </div>
    </div>

    <!-- Modal para exámenes -->
    <div id="modalExamenes" class="modal">
        <div class="modal-content">
            <span class="close" id="closeExamenes">&times;</span>
            <h2>Fechas de exámenes</h2>
            <ul>
                <li>Primer parcial: 10 de mayo</li>
                <li>Segundo parcial: 15 de junio</li>
                <li>Tercer parcial: 10 de julio</li>
            </ul>
        </div>
    </div>

    <!-- Modal para horarios -->
    <div id="modalHorarios" class="modal">
        <div class="modal-content">
            <span class="close" id="closeHorarios">&times;</span>
            <h2>Horarios de clases</h2>
            <ul>
                <li>Lunes: 8:00 AM - 12:00 PM</li>
                <li>Martes: 9:00 AM - 1:00 PM</li>
                <li>Miércoles: 10:00 AM - 2:00 PM</li>
                <li>Jueves: 11:00 AM - 3:00 PM</li>
                <li>Viernes: 8:00 AM - 12:00 PM</li>
            </ul>
        </div>
    </div>

    <script>
        // Obtener los botones y los modales
        var modalEventos = document.getElementById('modalEventos');
        var modalExamenes = document.getElementById('modalExamenes');
        var modalHorarios = document.getElementById('modalHorarios');
        
        var btnEventos = document.getElementById('btnEventos');
        var btnExamenes = document.getElementById('btnExamenes');
        var btnHorarios = document.getElementById('btnHorarios');
        
        var closeEventos = document.getElementById('closeEventos');
        var closeExamenes = document.getElementById('closeExamenes');
        var closeHorarios = document.getElementById('closeHorarios');

        // Mostrar el modal para eventos
        btnEventos.onclick = function() {
            modalEventos.style.display = "block";
        }

        // Mostrar el modal para exámenes
        btnExamenes.onclick = function() {
            modalExamenes.style.display = "block";
        }

        // Mostrar el modal para horarios
        btnHorarios.onclick = function() {
            modalHorarios.style.display = "block";
        }

        // Cerrar los modales
        closeEventos.onclick = function() {
            modalEventos.style.display = "none";
        }

        closeExamenes.onclick = function() {
            modalExamenes.style.display = "none";
        }

        closeHorarios.onclick = function() {
            modalHorarios.style.display = "none";
        }

        // Cerrar los modales si se hace clic fuera del contenido
        window.onclick = function(event) {
            if (event.target == modalEventos) {
                modalEventos.style.display = "none";
            }
            if (event.target == modalExamenes) {
                modalExamenes.style.display = "none";
            }
            if (event.target == modalHorarios) {
                modalHorarios.style.display = "none";
            }
        }
    </script>

</body>
</html>
