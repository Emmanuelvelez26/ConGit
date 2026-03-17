
-----------------------------------------------
📆 PLAN DE IMPLEMENTACIÓN CSS (6 días)
🟢 Día 1 – Base global + Sistema de diseño
🎯 Objetivo: Crear la base que usarán TODAS las páginas
1️⃣ Crear estructura CSS
/proyecto
  /css
    styles.css

En todas las páginas:

<link rel="stylesheet" href="css/styles.css">
2️⃣ Reset + modelo de caja
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
3️⃣ Variables globales
:root {
  --color-primario: #2563eb;
  --color-secundario: #1e293b;
  --color-fondo: #f8fafc;
  --color-texto: #0f172a;
  --color-acento: #38bdf8;

  --fuente-principal: 'Poppins', sans-serif;
}
4️⃣ Estilos base
body {
  font-family: var(--fuente-principal);
  background-color: var(--color-fondo);
  color: var(--color-texto);
  line-height: 1.6;
}
5️⃣ Navbar con Flexbox

Practica:

Selectores

Herencia

Flexbox

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: var(--color-secundario);
}

nav a {
  color: white;
  text-decoration: none;
  margin-left: 1rem;
}

nav a:hover {
  color: var(--color-acento);
}

✅ Al final del día: todo el sitio ya tiene identidad visual.

🟡 Día 2 – Inicio + Sobre mí
🎯 Objetivo: Practicar modelo de caja y tipografía
1️⃣ Hero (Inicio)

Fondo con gradiente

Texto centrado

Botón con hover

Practica:

background

padding grande

text-align

border-radius

2️⃣ Sección “Sobre mí”

Usa:

max-width

margin: auto

box-shadow

border-radius

Ejemplo:

.sobre-mi {
  max-width: 800px;
  margin: 3rem auto;
  padding: 2rem;
  background: white;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}
🟠 Día 3 – Proyectos (Grid)
🎯 Objetivo: Dominar CSS Grid

Esta será tu sección más importante.

.proyectos {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

Tarjetas:

.card {
  background: white;
  padding: 1rem;
  border-radius: 10px;
  transition: 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
}
🔥 IMPORTANTE – Imágenes bien hechas

En vez de:

<img width="250" height="250">

Haz:

.card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 8px;
}

✔ Responsive
✔ Profesional
✔ Limpio

🔵 Día 4 – Blog + Tablas
🎯 Objetivo: Trabajar detalles y menos usados
Blog

article con borde inferior

hover suave

mejor lectura

article {
  margin-bottom: 2rem;
  padding-bottom: 1rem;
  border-bottom: 1px solid #ddd;
}
Tabla

Practica:

border-collapse

nth-child

hover en filas

table {
  width: 100%;
  border-collapse: collapse;
}

th, td {
  padding: 10px;
  border: 1px solid #ddd;
}

tr:nth-child(even) {
  background-color: #f2f2f2;
}
🟣 Día 5 – Formulario + UI
🎯 Objetivo: Interfaz de usuario real
form {
  max-width: 600px;
  margin: auto;
}

input, textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 1rem;
  border-radius: 6px;
  border: 1px solid #ccc;
}

Estados:

input:focus, textarea:focus {
  outline: none;
  border-color: var(--color-primario);
}

Botón:

button {
  background: var(--color-primario);
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}

button:hover {
  background: var(--color-acento);
}
🔴 Día 6 – Responsive + Animaciones
🎯 Objetivo: Nivel junior real
1️⃣ Media Query
@media (max-width: 768px) {

  nav {
    flex-direction: column;
  }

  .proyectos {
    grid-template-columns: 1fr;
  }

}
2️⃣ Animación simple
@keyframes aparecer {
  from { opacity: 0; }
  to { opacity: 1; }
}

.hero {
  animation: aparecer 1s ease-in;
}
🧠 Cómo saber que lo hiciste bien

Tu sitio debe:

✅ Verse bien en móvil
✅ No tener scroll horizontal
✅ No romper layout
✅ Tener hover suaves
✅ No tener colores al azar
✅ Usar variables

🚀 Si quieres subir de nivel

Después de los 6 días:

Agrega modo oscuro

Agrega menú hamburguesa

Agrega animación en scroll

Usa clamp() para tipografía fluida

Usa :root para escalas de espaciado
