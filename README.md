# PRUEBA-II
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi página - Práctica</title>
  <style>
    /* Tipografía y reset básico */
    :root{
      --bg: #f6f1ff;
      --accent: #7a2be6;
      --accent-dark: #5a1db0;
      --card: #ffffff;
      --muted: #555;
      --success: #2b8a44;
    }
    *{box-sizing: border-box}
    body{
      margin:0;
      padding:0;
      font-family: 'Times New Roman', Times, serif;
      background: linear-gradient(180deg,var(--bg), #ffdff6 120%);
      color: #222;
      -webkit-font-smoothing:antialiased;
    }
    header{background:var(--accent); color:#fff; padding:18px 12px; text-align:center}
    header img{height:48px; vertical-align:middle; margin-right:12px}
    header h1{display:inline-block; font-size:22px; margin:0; vertical-align:middle}

    main{max-width:1000px; margin:22px auto; padding:0 16px}

    .card{background:var(--card); border-radius:12px; padding:18px; margin-bottom:18px; box-shadow:0 6px 18px rgba(0,0,0,0.06)}
    h2{margin:6px 0 12px 0; color:var(--accent-dark); text-align:center}
    p{color:var(--muted); text-align:center}

    /* Lista simple */
    ul, ol{max-width:500px; margin:12px auto; padding-left:24px}

    /* Calculadoras: diseño en grid */
    .calc-grid{display:grid; gap:18px; grid-template-columns:repeat(auto-fit,minmax(260px,1fr))}
    .calc{padding:12px}
    .calc label{display:block; font-weight:bold; margin-top:6px}
    .calc input[type=number]{width:100%; padding:8px; margin-top:6px; border-radius:6px; border:1px solid #ddd}
    .calc button{margin-top:10px; width:100%; padding:10px; border-radius:8px; border:none; cursor:pointer; background:var(--accent); color:#fff; font-weight:600}
    .result{margin-top:10px; font-size:18px; font-weight:bold; text-align:center}

    /* Formulario de contacto */
    .form-container{width:100%; max-width:700px; margin:0 auto}
    form label{font-weight:bold; display:block; margin-top:10px}
    input[type=text], input[type=email], textarea{width:100%; padding:10px; margin-top:6px; border-radius:6px; border:1px solid #ccc}
    .btn-submit{background:#3367d6; color:#fff; padding:12px; border-radius:8px; border:none; margin-top:12px; cursor:pointer}
    .btn-submit:hover{background:#2654a6}

    footer{margin:20px 0 60px 0; text-align:center; color:#666}

    /* Responsive small tweaks */
    @media (max-width:420px){header h1{font-size:18px}}
  </style>
</head>
<body>
  <header>
    <!-- reemplaza src por la imagen real si quieres -->
    <img src="imagen/Universidad_Tecnológica_de_Bolívar.png" alt="Logo Universidad"/>
    <h1>Mi página web — Práctica</h1>
  </header>

  <main>
    <section class="card">
      <h2>Mi primer título</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing. Recusandae hic facere voluptas itaque commodi adipisci quibusdam et earum dolores neque cum quis, eaque veniam molestias id corporis omnis magnam.</p>
    </section>

    <section class="card">
      <h2>Comida favorita</h2>
      <p>La vida es como el cucayo: dura pero sabrosa.</p>
      <ul>
        <li>Pollo</li>
        <li>Pescado</li>
        <li>Pizza</li>
      </ul>
    </section>

    <section class="card">
      <h2>Ranking de perfumes</h2>
      <p>Matar, besar, casar: elige</p>
      <ol type="A">
        <li>Selena Gomez</li>
        <li>Rihanna</li>
        <li>Cardi B</li>
      </ol>
    </section>

    <section class="card">
      <h2>Calculadoras</h2>
      <div class="calc-grid">
        <!-- Suma -->
        <div class="calc card">
          <h3>Suma</h3>
          <label for="num1">Número 1</label>
          <input id="num1" type="number" step="any" placeholder="Número 1">
          <label for="num2">Número 2</label>
          <input id="num2" type="number" step="any" placeholder="Número 2">
          <button id="btnSum">Sumar</button>
          <div class="result" id="resultadoSuma">Resultado: —</div>
        </div>

        <!-- Resta -->
        <div class="calc card">
          <h3>Resta</h3>
          <label for="num3">Número 3</label>
          <input id="num3" type="number" step="any" placeholder="Número 3">
          <label for="num4">Número 4</label>
          <input id="num4" type="number" step="any" placeholder="Número 4">
          <button id="btnRest">Restar</button>
          <div class="result" id="resultadoResta">Resultado: —</div>
        </div>

        <!-- Multiplicación -->
        <div class="calc card">
          <h3>Multiplicación</h3>
          <label for="num5">Número 5</label>
          <input id="num5" type="number" step="any" placeholder="Número 5">
          <label for="num6">Número 6</label>
          <input id="num6" type="number" step="any" placeholder="Número 6">
          <button id="btnMult">Multiplicar</button>
          <div class="result" id="resultadoMultiplicacion">Resultado: —</div>
        </div>
      </div>
    </section>

    <section class="card">
      <h2>Contacto</h2>
      <div class="form-container">
        <form id="contactForm">
          <label for="nombre">Nombre:</label>
          <input id="nombre" name="nombre" type="text" required>

          <label for="email">Correo electrónico:</label>
          <input id="email" name="email" type="email" required>

          <label for="mensaje">Mensaje:</label>
          <textarea id="mensaje" name="mensaje" rows="5" required></textarea>

          <button class="btn-submit" type="submit">Enviar</button>
        </form>
        <div id="formStatus" style="margin-top:12px;text-align:center;color:var(--success);"></div>
      </div>
    </section>

  </main>

  <footer>
    <p>Práctica de HTML / CSS / JavaScript — 04/10/2024</p>
  </footer>

  <script>
    // Funciones de cálculo con manejo de entradas vacías
    function toNumber(v){
      const n = parseFloat(v);
      return Number.isFinite(n) ? n : 0;
    }

    document.getElementById('btnSum').addEventListener('click', ()=>{
      const a = toNumber(document.getElementById('num1').value);
      const b = toNumber(document.getElementById('num2').value);
      document.getElementById('resultadoSuma').innerText = 'Resultado: ' + (a + b);
    });

    document.getElementById('btnRest').addEventListener('click', ()=>{
      const a = toNumber(document.getElementById('num3').value);
      const b = toNumber(document.getElementById('num4').value);
      document.getElementById('resultadoResta').innerText = 'Resultado: ' + (a - b);
    });

    document.getElementById('btnMult').addEventListener('click', ()=>{
      const a = toNumber(document.getElementById('num5').value);
      const b = toNumber(document.getElementById('num6').value);
      document.getElementById('resultadoMultiplicacion').innerText = 'Resultado: ' + (a * b);
    });

    // Manejo del formulario (evita recargar la página)
    document.getElementById('contactForm').addEventListener('submit', function(e){
      e.preventDefault();
      const nombre = document.getElementById('nombre').value.trim();
      const email = document.getElementById('email').value.trim();
      const mensaje = document.getElementById('mensaje').value.trim();

      // Simulación de envío
      document.getElementById('formStatus').innerText = `Gracias ${nombre}. Tu mensaje ha sido recibido.`;
      // limpiar formulario
      this.reset();
    });
  </script>
</body>
</html>
