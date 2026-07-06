## Proyecto Clientes — API REST ##  

**Aprendiz:** María Paula Aguilera Reina  
**Ficha:** 3407184

---

## Descripción

API REST desarrollada con FastAPI para administrar clientes, facturas y transacciones. El proyecto utiliza SQLModel como ORM y SQLite como base de datos, permitiendo realizar operaciones CRUD y calcular el valor total de las facturas.

## Características ## 
 
* Gestión de clientes, facturas y transacciones.
* Cálculo automático del valor total de una factura.
* Base de datos SQLite.
* Documentación automática con Swagger UI.
* Arquitectura modular utilizando FastAPI.

## Tecnologías Utilizadas ##

* Python 3
* FastAPI
* SQLModel
* SQLite
* Uvicorn

##  Estructura del Proyecto ##

```text
📦 p.y.t.h.o.n/
├── 📁 app/
│   ├── 📁 models/
│   │   ├── clientes.py              # Modelo de clientes
│   │   └── facturas.py              # Modelo de facturas
│   │
│   ├── 📁 routers/
│   │   ├── clientes.py              # CRUD de clientes
│   │   ├── facturas.py              # CRUD de facturas
│   │   └── transacciones.py         # CRUD de transacciones
│   │
│   ├── 📄 conexion_bd.py            # Configuración de la base de datos
│   └── 📄 main.py                   # Punto de entrada de la API
│
├── 📄 requirements.txt              # Dependencias del proyecto
├── 📄 .gitignore                    # Archivos ignorados por Git
└── 📄 README.md                     # Documentación del proyecto
```

##  Instalación 

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/tu-repositorio.git
cd p.y.t.h.o.n
```

### 2. Crear entorno virtual

```bash
python -m venv venv
```

### 3. Activar entorno virtual

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

Sabrás que está activo porque verás `(venv)` al inicio de tu terminal.

### 4. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 5. Ejecutar el servidor

```bash
<<<<<<< HEAD
uvicorn app.main:app --reload
=======
uvicorn main:app --reload
>>>>>>> 5645ec320f9bd808b91db7f48fc989a6fd4c72df
```

La API estará disponible en: `http://127.0.0.1:8000`  
Documentación interactiva en: `http://127.0.0.1:8000/docs`

---

##  Documentación de la API ##

Swagger UI:

```text
http://127.0.0.1:8000/docs
```

ReDoc:

```text
http://127.0.0.1:8000/redoc
```

##  Base de Datos ##

La aplicación utiliza SQLite como sistema de almacenamiento.

Archivo generado automáticamente:

```text
base_datos.db
```

Las tablas se crean automáticamente al iniciar la aplicación mediante el evento startup.

##  Endpoints Disponibles ##

### Clientes

| Método | Endpoint       | Descripción            |
| ------ | -------------- | ---------------------- |
| GET    | /clientes      | Listar clientes        |
| GET    | /clientes/{id} | Obtener cliente por ID |
| POST   | /clientes      | Crear cliente          |
| PUT    | /clientes/{id} | Actualizar cliente     |
| DELETE | /clientes/{id} | Eliminar cliente       |

### Facturas

| Método | Endpoint                   | Descripción                     |
| ------ | -------------------------- | ------------------------------- |
| GET    | /facturas                  | Listar facturas                 |
| GET    | /facturas/{id}             | Obtener factura por ID          |
| GET    | /facturas/{id}/valor_total | Calcular valor total de factura |
| POST   | /facturas                  | Crear factura                   |
| PUT    | /facturas/{id}             | Actualizar factura              |
| DELETE | /facturas/{id}             | Eliminar factura                |

### Transacciones

| Método | Endpoint            | Descripción                |
| ------ | ------------------- | -------------------------- |
| GET    | /transacciones      | Listar transacciones       |
| GET    | /transacciones/{id} | Obtener transacción por ID |
| POST   | /transacciones      | Crear transacción          |
| PUT    | /transacciones/{id} | Actualizar transacción     |
| DELETE | /transacciones/{id} | Eliminar transacción       |

##  Endpoint de Prueba ##

```http
GET /
```

Respuesta:

```json
{
  "mensaje": "API funcionando"
}
```

## Desactivar el entorno virtual

```bash
deactivate
```

---

*Aprendiz SENA — Ficha 3407184*
