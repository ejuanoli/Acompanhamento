<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Conferência</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }
        .container h2 {
            text-align: center;
            margin-bottom: 20px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .form-group select {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .submit-btn {
            width: 100%;
            padding: 10px;
            background-color: #007BFF;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .submit-btn:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Formulário de Conferência</h2>
        <form id="conferenceForm">
            <div class="form-group">
                <label for="pv">PV (Valor numérico):</label>
                <input type="number" id="pv" name="pv" required>
            </div>
            <div class="form-group">
                <label for="conferente">Conferente:</label>
                <input type="text" id="conferente" name="conferente" required>
            </div>
            <div class="form-group">
                <label for="temConferencia">Tem Conferência?</label>
                <select id="temConferencia" name="temConferencia" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                </select>
            </div>
            <button type="submit" class="submit-btn">Enviar</button>
        </form>
        <div id="result"></div>
    </div>

    <script>
        document.getElementById('conferenceForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            const pv = document.getElementById('pv').value;
            const conferente = document.getElementById('conferente').value;
            const temConferencia = document.getElementById('temConferencia').value;
            
            document.getElementById('result').innerHTML = `
                <p><strong>PV:</strong> ${pv}</p>
                <p><strong>Conferente:</strong> ${conferente}</p>
                <p><strong>Tem Conferência:</strong> ${temConferencia}</p>
            `;
        });
    </script>
</body>
</html>
