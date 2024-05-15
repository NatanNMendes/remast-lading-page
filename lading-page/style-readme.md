Clique nos botões abaixo para visualizar diferentes trechos de código.

<div class="buttons">
    <button onclick="showCode('javascript')">JavaScript</button>
    <button onclick="showCode('php')">PHP</button>
    <button onclick="showCode('html')">HTML</button>
</div>

<div id="javascript" class="code-container">
    ```javascript
    console.log("Esta é uma linha de código em Javascript.");
    ```
</div>

<div id="php" class="code-container" style="display:none;">
    ```php
    echo "Esta é uma linha de código em PHP.";
    ```
</div>

<div id="html" class="code-container" style="display:none;">
    ```html
    <p>Esta é uma linha de código em HTML.</p>
    ```
</div>

<script>
    function showCode(language) {
        var containers = document.querySelectorAll('.code-container');
        containers.forEach(function(container) {
            container.style.display = 'none';
        });
        document.getElementById(language).style.display = 'block';
    }
</script>

<style>
    .buttons {
        margin-bottom: 20px;
    }
    .code-container {
        margin-top: 20px;
        border: 1px solid #ccc;
        padding: 10px;
        background-color: #f9f9f9;
    }
</style>