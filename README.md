<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <main class="card">
        <form class="display">
            <input id="layar" placeholder="0">
        </form>
        <section class="button">
            <div class="tombol-kiri">
                <button class="tombol" onclick="display('AC')">AC</button>
                <button class="tombol" onclick="display('Del')">Del</button>
                <button class="tombol" onclick="display('%')">%</button>
                <script>
                    for (let i = 9; i >= 1; i--) {
                        document.write(
                            `<button class=tombol onclick=display(${i})>`+i+`</button>`
                        )
                        
                    }
                </script>
                <button class="tombol" onclick="display"></button>
                <button class="tombol" onclick="display('0')">0</button>
                <button class="tombol" onclick="display"></button>
            </div>
            <div class="tombol-kanan">
                <button class="tombol" onclick="display('/')">/</button>
                <button class="tombol" onclick="display('*')">X</button>
                <button class="tombol" onclick="display('-')">-</button>
                <button class="tombol" onclick="display('+')">+</button>
                <button class="tombol" onclick="display('action')">=</button>
            </div>
        </section>
    </main>
    <script>
        let result = document.getElementById('layar')
        const display = (a) => {
            if(a == 'clear'){
                result.value = ''
            } else if(a == 'Del'){
                result.value = result.value.slice(0,-1)
            }
            else if(a == 'action'){
                try {
                    result.value = eval(result.value)
                } catch (error) {
                    alert('error')
                }                   
            }else{
                result.value += a
            }
        }
    </script>
    

</body>
</html>
