# 📌 URL Shortener Microservice

Este proyecto forma parte de la certificación **Back End Development and APIs** de [freeCodeCamp](https://www.freecodecamp.org/).  
El objetivo es construir un microservicio que acorte URLs y redirija al usuario mediante una API REST.

---

## 🌐 Demo Oficial de Referencia

🔗 [https://url-shortener-microservice.freecodecamp.rocks](https://url-shortener-microservice.freecodecamp.rocks)

---

## 🚀 Funcionalidades

- Enviar una URL a `/api/shorturl` para recibir un identificador corto.
- Redirigir automáticamente al visitar `/api/shorturl/:short_url`.
- Validar URLs que cumplan con el formato `http://www.ejemplo.com` o `https://ejemplo.com`.
- Retornar un error JSON si la URL no es válida.

---

## ⚙️ Tecnologías utilizadas

- Node.js
- Express.js
- Body-Parser
- CORS
- DNS (módulo nativo de Node.js)
- dotenv

---

## 📂 Estructura del proyecto

```
fcc-url-shortener-microservice/
├── public/
│   └── styles.css
├── views/
│   └── index.html
├── .env
├── .gitignore
├── package.json
├── README.md
└── server.js
```

---

## 📄 Instalación y uso

### 1️⃣ Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/fcc-url-shortener-microservice.git
cd fcc-url-shortener-microservice
```

### 2️⃣ Eliminar cualquier repositorio anterior y reinicializar

```bash
rm -rf .git
git init
```

### 3️⃣ Crear archivo `.gitignore`

```bash
touch .gitignore
```

**Contenido recomendado para `.gitignore`:**

```
node_modules/
.env
```

### 4️⃣ Instalar dependencias

```bash
npm install
```

### 5️⃣ Configurar archivo `.env`

```bash
touch .env
```

**Contenido del archivo `.env`:**

```
PORT=3000
```

### 6️⃣ Ejecutar el servidor

```bash
npm start
```

Accede a la aplicación en:  
[http://localhost:3000](http://localhost:3000)

---

## 🗂️ Endpoints de la API

### ➤ POST `/api/shorturl`

**Descripción:** Recibe una URL y retorna un identificador corto.

**Body:** (formato `application/x-www-form-urlencoded`)

```
url=https://freecodecamp.org
```

**Respuesta exitosa:**

```json
{
  "original_url": "https://freecodecamp.org",
  "short_url": 1
}
```

**Respuesta en caso de error (URL inválida):**

```json
{ "error": "invalid url" }
```

---

### ➤ GET `/api/shorturl/:short_url`

**Descripción:** Redirige a la URL original según el identificador.

**Ejemplo:**

```
GET /api/shorturl/1
```

**Si existe el identificador:**
Redirige a la URL original.

**Si NO existe:**

```json
{ "error": "No short URL found for the given input" }
```

---

## ✅ Requisitos del Proyecto

✔️ Debes proporcionar tu propia URL, no la de ejemplo.  
✔️ Debes poder enviar una URL a `/api/shorturl` y obtener un JSON con las propiedades `original_url` y `short_url`.  
✔️ Al visitar `/api/shorturl/<short_url>`, serás redirigido a la URL original.  
✔️ Si envías una URL inválida, recibirás `{ "error": "invalid url" }`.

---

## 📝 Comandos útiles para Git

```bash
# Inicializar repositorio desde cero
rm -rf .git
git init

# Crear rama main
git branch -M main

# Agregar todos los archivos
git add .

# Primer commit
git commit -m "Initial commit - URL Shortener Microservice"

# Agregar repositorio remoto
git remote add origin https://github.com/tu-usuario/fcc-url-shortener-microservice.git

# Subir a GitHub
git push -u origin main
```

---

## 🙋‍♂️ Autor

**Gerardo-HG**  
🚀 GitHub: [https://github.com/Gerardo-HG]

---

## 📄 Licencia

Este proyecto es únicamente para fines educativos como parte del currículo de **freeCodeCamp - Back End Development and APIs**.

---

