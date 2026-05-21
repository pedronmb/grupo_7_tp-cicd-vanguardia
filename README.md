# grupo_7_tp-cicd-vanguardia

Trabajo práctico del **Grupo 7** para la materia **Programación de Vanguardia** (3.er cuatrimestre). El proyecto es una aplicación web mínima pensada como base para practicar **integración y despliegue continuo (CI/CD)** con GitHub y GitHub Actions.

## Descripción

El repositorio incluye un sitio estático de demostración servido por un servidor **Node.js** con **Express**. La página muestra un mensaje de bienvenida y documenta, a nivel conceptual, el flujo de publicación automática mediante un pipeline en GitHub.

El objetivo del TP es:

- Versionar el código en GitHub.
- Configurar un pipeline de CI/CD que construya y/o despliegue la aplicación en cada cambio relevante (por ejemplo, un `push` a `main`).
- Entender la diferencia entre ejecutar la app en local y publicarla en un entorno accesible desde internet.

## Tecnologías

| Componente | Tecnología |
|------------|------------|
| Frontend   | HTML5, CSS3, JavaScript |
| Backend    | Node.js + Express 5 |
| Gestión de paquetes | npm |

## Estructura del proyecto

```
.
├── index.html      # Página principal
├── style.css       # Estilos
├── script.js       # Lógica del cliente
├── server.js       # Servidor Express (archivos estáticos)
├── package.json    # Dependencias y script de inicio
└── package-lock.json
```

## Requisitos

- [Node.js](https://nodejs.org/) (versión LTS recomendada)
- npm (incluido con Node.js)
- Cuenta de [GitHub](https://github.com/) para el flujo de CI/CD

## Ejecución en local

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/pedronmb/grupo_7_tp-cicd-vanguardia.git
   cd grupo_7_tp-cicd-vanguardia
   ```

2. Instalar dependencias:

   ```bash
   npm install
   ```

3. Iniciar el servidor:

   ```bash
   npm start
   ```

4. Abrir en el navegador: [http://localhost:3000](http://localhost:3000)

El comando `npm start` ejecuta `node server.js`, que expone los archivos estáticos del directorio en el puerto **3000**.

## CI/CD (previsto)

La página indica que el despliegue puede automatizarse con **GitHub Actions**. El pipeline típico incluye:

1. Dispararse ante un `push` o `pull request` en la rama principal.
2. Instalar dependencias y, si aplica, validar el proyecto.
3. Publicar el sitio (por ejemplo, en **GitHub Pages** para contenido estático, o en un servicio que soporte Node.js si se despliega el servidor Express).

Los workflows de Actions se agregan en `.github/workflows/` cuando el equipo los implemente como parte del TP.

## Repositorio

https://github.com/pedronmb/grupo_7_tp-cicd-vanguardia

## Licencia

ISC (según `package.json`).
