<!DOCTYPE html>
<html>
<head>
    <title>Calculadora de Idade Gestacional</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
        }
        .container {
            display: flex;
            justify-content: space-between;
            max-width: 800px;
            margin: 0 auto;
        }
        .calculator {
            width: 48%;
        }
        input, button {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
        }
        label {
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Calculadora de Idade Gestacional pela Ultrassonografia -->
        <div class="calculator">
            <h2>Cálculo da IG pela Ultrassonografia</h2>
            <label for="ultrasoundDate">Data do Ultrassom:</label>
            <input type="date" id="ultrasoundDate" required>
            
            <label for="gestationalWeeks">Semanas Gestacionais:</label>
            <input type="number" id="gestationalWeeks" required>
            
            <label for="gestationalDays">Dias Gestacionais:</label>
            <input type="number" id="gestationalDays" required>
            
            <button onclick="calculateGestationalAgeByUltrasound()">Calcular Idade Gestacional Atual</button>
            
            <h3 id="resultUltrasound"></h3>
        </div>
        
        <!-- Calculadora de Idade Gestacional pela DUM -->
        <div class="calculator">
            <h2>Cálculo da IG pela DUM</h2>
            <label for="dumDate">Data da Última Menstruação (DUM):</label>
            <input type="date" id="dumDate" required>
            
            <button onclick="calculateGestationalAgeByDUM()">Calcular Idade Gestacional Atual</button>
            
            <h3 id="resultDUM"></h3>
        </div>
    </div>

    <script>
        function calculateGestationalAgeByUltrasound() {
            // Obtém os valores inseridos pelo usuário
            const ultrasoundDate = new Date(document.getElementById('ultrasoundDate').value);
            const gestationalWeeks = parseInt(document.getElementById('gestationalWeeks').value);
            const gestationalDays = parseInt(document.getElementById('gestationalDays').value);

            // Calcula a idade gestacional na data atual
            const currentDate = new Date();
            const timeDiff = currentDate - ultrasoundDate;
            const diffDays = Math.floor(timeDiff / (1000 * 60 * 60 * 24));
            
            let totalDays = gestationalWeeks * 7 + gestationalDays + diffDays;
            const currentWeeks = Math.floor(totalDays / 7);
            const currentDays = totalDays % 7;

            // Exibe o resultado
            document.getElementById('resultUltrasound').innerHTML = `<b>A idade gestacional hoje é ${currentWeeks} semanas e ${currentDays} dias.</b>`;
        }

        function calculateGestationalAgeByDUM() {
            // Obtém a data da última menstruação
            const dumDate = new Date(document.getElementById('dumDate').value);

            // Calcula a idade gestacional na data atual
            const currentDate = new Date();
            const timeDiff = currentDate - dumDate;
            const totalDays = Math.floor(timeDiff / (1000 * 60 * 60 * 24));
            const currentWeeks = Math.floor(totalDays / 7);
            const currentDays = totalDays % 7;

            // Exibe o resultado
            document.getElementById('resultDUM').innerHTML = `<b>A idade gestacional hoje é ${currentWeeks} semanas e ${currentDays} dias.</b>`;
        }
    </script>
</body>
</html>
