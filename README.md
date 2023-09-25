<!DOCTYPE html>
<html>
<head>
    <title>Registro de Evolução Médica</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
        }

        h1 {
            text-align: center;
            background-color: #3498db;
            color: white;
            padding: 20px;
        }

        form {
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        label {
            display: block;
            margin-bottom: 10px;
        }

        input[type="text"],
        input[type="date"],
        input[type="tel"],
        textarea,
        select {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        textarea {
            height: 150px;
        }

        button[type="submit"] {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
        }

        button[type="submit"]:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>
    <h1>Registro de Evolução Médica</h1>
    <form id="evolutionForm">
        <label for="patientName">Nome do Paciente:</label>
        <input type="text" id="patientName" name="patientName" required>

        <label for="fatherName">Nome do Pai:</label>
        <input type="text" id="fatherName" name="fatherName" required>

        <label for="motherName">Nome da Mãe:</label>
        <input type="text" id="motherName" name="motherName" required>

        <label for="birthDate">Data de Nascimento:</label>
        <input type="date" id="birthDate" name="birthDate" required>

        <label for="maritalStatus">Estado Civil:</label>
        <select id="maritalStatus" name="maritalStatus" required>
            <option value="solteiro">Solteiro</option>
            <option value="casado">Casado</option>
            <option value="divorciado">Divorciado</option>
            <option value="viuvo">Viúvo</option>
        </select>

        <label for="contactPhone">Telefone de Contato:</label>
        <input type="tel" id="contactPhone" name="contactPhone" required>

        <label for="familyPhone">Telefone Familiar:</label>
        <input type="tel" id="familyPhone" name="familyPhone" required>

        <label for="evolutionText">Evolução Médica:</label>
        <textarea id="evolutionText" name="evolutionText" required></textarea>

        <button type="submit">Registrar Evolução</button>
    </form>

    <script>
        // Exemplo de JavaScript para lidar com o envio do formulário
        document.getElementById("evolutionForm").addEventListener("submit", function (event) {
            event.preventDefault(); // Impede o envio padrão do formulário

            // Coleta os valores dos campos
            var patientName = document.getElementById("patientName").value;
            var fatherName = document.getElementById("fatherName").value;
            var motherName = document.getElementById("motherName").value;
            var birthDate = document.getElementById("birthDate").value;
            var maritalStatus = document.getElementById("maritalStatus").value;
            var contactPhone = document.getElementById("contactPhone").value;
            var familyPhone = document.getElementById("familyPhone").value;
            var evolutionText = document.getElementById("evolutionText").value;

            // Aqui você pode enviar os dados para o servidor ou realizar outras ações necessárias
            // Por exemplo, você pode usar o Fetch API para enviar os dados para o servidor

            // Exemplo de exibição dos dados (substitua com sua lógica real)
            alert("Nome do Paciente: " + patientName + "\nNome do Pai: " + fatherName + "\nNome da Mãe: " + motherName +
                "\nData de Nascimento: " + birthDate + "\nEstado Civil: " + maritalStatus +
                "\nTelefone de Contato: " + contactPhone + "\nTelefone Familiar: " + familyPhone +
                "\nEvolução Médica: " + evolutionText);
        });
    </script>
</body>
</html>
