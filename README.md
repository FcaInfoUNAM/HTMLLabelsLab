# Ejercicio: Formulario de Préstamo de Computadoras (HTML + CSS + JS)

Este ejercicio te guía paso a paso para practicar etiquetas **HTML**: `label`, `a`, `input`, `option`, `form`, `table`, `tr`, `th`, `td`, `button`, `script` y `style`; y atributos `class`, `href`, `type` e `id`, en el contexto de **préstamos de computadoras en un aula de cómputo**.

---

## 1) Requisitos previos

- Un navegador web moderno (Chrome, Edge, Firefox, Safari).
- Un editor de código (VS Code, Sublime, etc.).

## 2) Archivos del proyecto

- `index.html` → Página web con el formulario y la tabla. Contiene `<style>` y `<script>` incrustados para mantener todo en un solo archivo.
- `README.md` → Este documento con el tutorial paso a paso.

Para ver el resultado, **abre `index.html` en tu navegador**.

---

## 3) Objetivo de aprendizaje

- Comprender y practicar el uso de etiquetas de formulario y tabla.
- Relacionar `label` con `input` mediante `for`/`id`.
- Emplear atributos `class`, `id`, `type` y `href`.
- Usar `<style>` para dar estilos básicos y `<script>` para agregar interactividad mínima.

---

## 4) Paso a paso (con soluciones)

### Paso 1 — Encabezado con navegación y `<a href>`
Agrega un encabezado con navegación. Incluye un enlace interno que lleve al formulario y otro externo al reglamento.

<details>
    <summary>Solución</summary>
    
      <header>
        <nav class="nav">
          <a href="#formulario" class="nav-link" id="link-form">Ir al formulario</a>
          <a href="https://www.example.com/reglamento-prestamos" class="nav-link" id="link-reglamento" target="_blank" rel="noopener">Reglamento</a>
        </nav>
      </header>
    
</details>

- Aquí usas **`href`** para definir destinos (interno con `#formulario` y externo con URL).
- Se usan **`class`** e **`id`** para aplicar estilos o scripts a elementos específicos.

---

### Paso 2 — Formulario `<form>` con `label` + `input` y `select` + `option`
Crea una sección con un formulario para solicitar el préstamo. Relaciona cada `label` con su `input` mediante `for`/`id` y usa distintos `type` en los campos.
<details>
    <summary>Solución</summary>

    <section id="formulario">
      <h2>Solicitud de préstamo</h2>
      <form id="form-prestamo" class="tarjeta" action="#" method="post">
        <div class="grid">
          <div class="fila">
            <label for="nombre">Nombre completo</label>
            <input type="text" id="nombre" class="campo" placeholder="Tu nombre" required />
          </div>
          <div class="fila">
            <label for="correo">Correo institucional</label>
            <input type="email" id="correo" class="campo" placeholder="tu@escuela.edu" required />
          </div>
          <div class="fila">
            <label for="aula">Aula de cómputo</label>
            <select id="aula" class="campo" required>
              <option value="">— Selecciona un aula —</option>
              <option value="A1">A1</option>
              <option value="A2">A2</option>
              <option value="B1">B1</option>
              <option value="B2">B2</option>
            </select>
          </div>
          <div class="fila">
            <label for="equipo">Número de equipo</label>
            <input type="number" id="equipo" class="campo" min="1" max="60" placeholder="Ej. 12" required />
          </div>
          <div class="fila">
            <label for="fecha">Fecha del préstamo</label>
            <input type="date" id="fecha" class="campo" required />
          </div>
        </div>
        <div class="acciones">
          <button type="submit" id="btn-enviar" class="btn btn-primary">Registrar préstamo</button>
          <button type="button" id="btn-limpiar" class="btn">Limpiar</button>
        </div>
      </form>
    </section>
    
</details>

- Practicas **`type`** (`text`, `email`, `number`, `date`) y el uso de `required`.
- `label` y `input` se relacionan por `for="idDelInput"`.
- `select` ofrece opciones con varias etiquetas **`option`**.

---

### Paso 3 — Tabla `<table>` con `<tr>`, `<th>`, `<td>`
Crea una tabla para listar los préstamos registrados. Empieza con un mensaje de "sin datos".

<details>
    <summary>Solución</summary>

    <section id="reservas">
      <h2>Préstamos registrados</h2>
      <table id="tabla-prestamos" class="tabla-prestamos">
        <thead>
          <tr>
            <th>Folio</th>
            <th>Nombre</th>
            <th>Correo</th>
            <th>Aula</th>
            <th>Equipo</th>
            <th>Fecha</th>
            <th>Duración</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td colspan="7">No hay préstamos aún.</td>
          </tr>
        </tbody>
      </table>
    </section>
    
</details>


- Observa el uso de **`<th>`** para encabezados y **`<td>`** para celdas de datos.
- `colspan` une celdas para el mensaje inicial.

---
### Paso 4 - Sube los cambios al repositorio
<details>
    <summary>Solución</summary>

    git add index.html
    git commit -m  "mensaje"
    git push origin main

</details>

¡Listo! Ya practicaste las etiquetas y atributos solicitados en un caso realista de aula de cómputo.
