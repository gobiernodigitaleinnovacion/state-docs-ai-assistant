# State Documents AI Assistant

Sistema de gestión documental con IA para gobiernos estatales y municipales.

## Características
- Indexación automática de PDFs
- Búsqueda semántica
- Consultas en lenguaje natural usando Azure OpenAI
- Soporte multi-estado/municipio

## Arquitectura
- Azure Blob Storage: Almacenamiento de documentos
- Azure Cognitive Search: Motor de búsqueda
- Azure OpenAI Service: Procesamiento lenguaje natural
- Azure App Service: Alojamiento de la aplicación

## Requisitos Previos
- Cuenta Azure
- Suscripción Azure OpenAI
- Node.js y Python 3.9+
- Terraform

## Instalación

1. Clonar repositorio:
```bash
git clone https://github.com/gobiernodigitaleinnovacion/state-docs-ai-assistant.git
cd state-docs-ai-assistant
```

2. Configurar variables de entorno:
```bash
cp .env.example .env
# Editar .env con tus credenciales
```

3. Infraestructura Azure:
```bash
cd infrastructure/terraform
terraform init
terraform apply
```

4. Instalar dependencias:
```bash
pip install -r requirements.txt
cd src/frontend
npm install
```

5. Ejecutar aplicación:
```bash
# Backend
cd src/api
uvicorn main:app --reload

# Frontend
cd src/frontend
npm start
```

## Estructura del Proyecto
```
/
├── src/
│   ├── indexer/     # Procesamiento PDFs
│   ├── api/         # API Backend
│   └── frontend/    # UI React
├── infrastructure/  # Terraform IaC
└── docs/           # Documentación
```

## Licencia
MIT
