<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Código</title>
    <style>
        .code-container {
            display: none;
            margin-top: 20px;
            border: 1px solid #ccc;
            padding: 10px;
            background-color: #f9f9f9;
        }
        .code-container pre {
            margin: 0;
        }
        .active {
            display: block;
        }
        .buttons {
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div class="buttons">
        <button onclick="showCode('javascript')">JavaScript</button>
        <button onclick="showCode('php')">PHP</button>
        <button onclick="showCode('html')">HTML</button>
    </div>

    <div id="javascript" class="code-container">
        <pre><code class="language-javascript">
console.log("Esta é uma linha de código em Javascript.");
        </code></pre>
    </div>

    <div id="php" class="code-container">
        <pre><code class="language-php">
echo "Esta é uma linha de código em PHP.";
        </code></pre>
    </div>

    <div id="html" class="code-container">
        <pre><code class="language-html">
&lt;p&gt;Esta é uma linha de código em HTML.&lt;/p&gt;
        </code></pre>
    </div>

    <script>
        function showCode(language) {
            var containers = document.querySelectorAll('.code-container');
            containers.forEach(function(container) {
                container.classList.remove('active');
            });
            document.getElementById(language).classList.add('active');
        }
    </script>
</body>
</html>
