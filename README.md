# 🎬 Blockbuster Clone (Ruby on Rails 7)

Mini–catálogo tipo **Blockbuster** para gestionar **películas** y **clientes**, desarrollado con **Ruby on Rails 7** (Importmap + Turbo + Stimulus) y **PostgreSQL**.  
Incluye un CRUD completo para `movies` y `clients`, con vistas básicas y `root` en `movies#index`.

> Proyecto académico orientado a practicar rutas RESTful, controladores, modelos y vistas con renderizado server-side.

---

## ✨ Funcionalidades principales

- 🎞️ **Películas:** listar, crear, ver, editar y eliminar.  
- 👥 **Clientes:** listar, crear, ver, editar y eliminar.  
- 🔁 Navegación simple entre módulos.  
- 🧩 Vistas con layouts ERB personalizables.  
- 🌐 Rutas RESTful generadas automáticamente con `resources`.

---

## 🧱 Stack tecnológico

| Componente | Descripción |
|-------------|-------------|
| **Lenguaje** | Ruby 3.1.3 |
| **Framework** | Ruby on Rails 7.0.6 |
| **Base de datos** | PostgreSQL |
| **Frontend** | Importmap, Turbo, Stimulus |
| **Servidor web** | Puma |
| **Renderizado** | ERB + Jbuilder |
| **Testing** | Minitest / Capybara / Selenium |

---

## 📂 Estructura del proyecto
app/
├── controllers/
│ ├── application_controller.rb
│ ├── clients_controller.rb
│ └── movies_controller.rb
├── models/
│ ├── application_record.rb
│ ├── client.rb
│ └── movie.rb
├── views/
│ ├── layouts/
│ ├── clients/
│ └── movies/
config/
└── routes.rb
Gemfile

---

## 🗺️ Rutas

**Archivo:** `config/routes.rb`

```rb
Rails.application.routes.draw do
  resources :movies
  resources :clients
  root "movies#index"
end
```
--- 
# 🌐 Endpoints principales
| **Endpoint**        | **Método HTTP** | **Descripción**                                           |
| ------------------- | --------------- | --------------------------------------------------------- |
| `/movies`           | GET             | Muestra el listado de películas disponibles.              |
| `/movies/:id`       | GET             | Muestra el detalle de una película específica.            |
| `/movies/new`       | GET             | Muestra el formulario para agregar una nueva película.    |
| `/movies`           | POST            | Crea una nueva película en la base de datos.              |
| `/movies/:id/edit`  | GET             | Muestra el formulario para editar una película existente. |
| `/movies/:id`       | PATCH / PUT     | Actualiza la información de una película.                 |
| `/movies/:id`       | DELETE          | Elimina una película del sistema.                         |
| `/clients`          | GET             | Muestra el listado de clientes registrados.               |
| `/clients/:id`      | GET             | Muestra el detalle de un cliente específico.              |
| `/clients/new`      | GET             | Muestra el formulario para agregar un nuevo cliente.      |
| `/clients`          | POST            | Crea un nuevo cliente en la base de datos.                |
| `/clients/:id/edit` | GET             | Muestra el formulario para editar un cliente.             |
| `/clients/:id`      | PATCH / PUT     | Actualiza la información de un cliente.                   |
| `/clients/:id`      | DELETE          | Elimina un cliente del sistema.                           |
| `/`                 | GET             | Página principal del sitio (`movies#index`).              |

# 🚀 Puesta en marcha
## 1️⃣ Requisitos previos

- Ruby 3.1.3
- Bundler instalado
- PostgreSQL configurado localmente

## 2️⃣ Instalación del proyecto
git clone https://github.com/FranOlivec/BlockbusterCloneFOV.git
cd BlockbusterCloneFOV
bundle install

## 3️⃣ Configuración de la base de datos

Edita config/database.yml con tus credenciales de PostgreSQL o utiliza variables de entorno.

bin/rails db:create
bin/rails db:migrate
bin/rails db:seed   # opcional: si agregas datos demo

## 4️⃣ Iniciar el servidor
bin/rails s

Luego abre http://localhost:3000
→ se cargará la vista principal movies#index.

# 🧪 Pruebas
bin/rails test
## o, si usas RSpec:
bundle exec rspec

📝 Roadmap

- Validaciones de modelos (presencia, longitud)
- Paginación y búsqueda de películas
- Relación cliente–películas (historial de arriendos)
- Estilos con Bootstrap / Tailwind
- Datos semilla (seeds.rb) con ejemplos

# 📄 Licencia

MIT © Francisca Olivares — 2025

