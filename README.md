# Zuzu.Git.Hub.io

<html>
<head>
    <title>Richiesta di eliminazione dati Instagram</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 40px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            color: #333;
            font-size: 36px;
            margin-bottom: 20px;
        }

        .description {
            color: #666;
            font-size: 18px;
            margin-bottom: 40px;
        }

        #ping-data {
            border: 1px solid #ccc;
            background-color: #f7f7f7;
            padding: 20px;
            border-radius: 4px;
        }

        pre {
            white-space: pre-wrap;
            font-size: 14px;
            line-height: 1.6;
            margin: 0;
        }

        /* Stili per i bottoni */
        .custom-btn {
            border: none;
            padding: 10px 20px;
            color: #fff;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            margin-right: 10px;
        }

        .primary-btn {
            background-color: #007bff;
        }

        .secondary-btn {
            background-color: #6c757d;
        }

        .success-btn {
            background-color: #28a745;
        }

        .warning-btn {
            background-color: #ffc107;
        }

        .error-btn {
            background-color: #dc3545;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Richiesta di eliminazione dati Instagram</h1>
        <p class="description">Questa pagina visualizza i ping inviati da Instagram quando qualcuno richiede la rimozione dei propri dati.</p>
        <div id="ping-data"></div>
    </div>

    <script>
        function displayPingData(ping) {
            var pingDataDiv = document.getElementById('ping-data');
            pingDataDiv.innerHTML = '<pre>' + JSON.stringify(ping, null, 2) + '</pre>';
        }

        function handlePing(event) {
            var ping = JSON.parse(event.data);
            displayPingData(ping);
        }

        window.addEventListener('message', handlePing);
    </script>
</body>
</html>
