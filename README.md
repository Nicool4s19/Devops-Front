# Devops-Front

Frontend de la aplicación **Tienda de Alimentos para Perritos**, desarrollado en HTML, CSS y JavaScript.

## Descripción

Esta aplicación permite visualizar y gestionar productos almacenados en una base de datos MySQL mediante un backend REST API desplegado en Amazon ECS.

## Tecnologías utilizadas

* HTML5
* CSS3
* JavaScript
* Docker
* Amazon ECR
* Amazon ECS Fargate
* GitHub Actions
* AWS Auto Scaling

## Arquitectura

Frontend → Backend API → MySQL

### Componentes AWS

* Amazon ECS Fargate para ejecutar contenedores.
* Amazon ECR para almacenar imágenes Docker.
* GitHub Actions para CI/CD.
* Auto Scaling para escalamiento automático.

## Construcción de la imagen Docker

```bash
docker build -t tienda-frontend .
```

## Ejecución local

```bash
docker run -d -p 80:80 tienda-frontend
```

## Pipeline CI/CD

Cada vez que se realiza un push a la rama `main`:

1. GitHub Actions construye una nueva imagen Docker.
2. La imagen se publica en Amazon ECR.
3. Amazon ECS realiza automáticamente un nuevo despliegue.
4. La aplicación queda actualizada sin intervención manual.

## Evidencia de funcionamiento

La aplicación muestra un mensaje indicando que el despliegue fue realizado automáticamente mediante CI/CD desde GitHub Actions hacia Amazon ECS.

## Autor

Nicolás Silva Figueroa
Dylan Monroy Sanhueza

Ingeniería en Informática
