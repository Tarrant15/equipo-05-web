# Guía de Contribución

¡Gracias por contribuir al proyecto! Para mantener un flujo de trabajo ágil, predecible y un historial de Git limpio, asegúrate de seguir estas directrices antes de enviar tus cambios.

---

## 1. Convención de Nombres de Rama

Todas las ramas deben crearse a partir de `main` (o `develop`, según corresponda) y utilizar minúsculas con palabras separadas por guiones (`kebab-case`).

### Formato general:

```text
<tipo>/<identificador-o-ticket>-<descripcion-corta>

```

### Prefijos admitidos:

* **`feature/`**: Nueva funcionalidad o característica.
* **`fix/`**: Corrección de un fallo o bug.
* **`hotfix/`**: Corrección crítica directa para producción.
* **`docs/`**: Modificaciones exclusivas en documentación.
* **`refactor/`**: Reestructuración de código sin alterar su comportamiento externo ni añadir funcionalidad.
* **`test/`**: Adición o modificación de pruebas unitarias o de integración.
* **`chore/`**: Tareas de mantenimiento, dependencias, scripts o configuración de CI/CD.

### Ejemplos:

* `feature/PROJ-102-autenticacion-oauth`
* `fix/issue-45-error-redondeo-total`
* `docs/actualizar-endpoints-api`

---

## 2. Convención de Mensajes de Commit

Seguimos la especificación de **Conventional Commits**. Los mensajes deben redactarse preferentemente en modo imperativo o presente, ser descriptivos y concisos.

### Formato:

```text
<tipo>(<ámbito opcional>): <descripción>

[cuerpo opcional detallando el motivo o contexto del cambio]

[pie opcional con referencias a issues, ej. Closes #123]

```

### Tipos de commit:

* **`feat`**: Incorpora una nueva funcionalidad.
* **`fix`**: Corrige un fallo.
* **`docs`**: Cambios en la documentación.
* **`style`**: Ajustes de formato, espaciado o linting sin impacto en la lógica.
* **`refactor`**: Refactorización que no añade características ni soluciona bugs.
* **`perf`**: Mejoras de rendimiento.
* **`test`**: Inclusión o corrección de tests.
* **`chore`**: Tareas de compilación, herramientas o actualización de paquetes.

### Ejemplos:

```text
feat(auth): implementar refresco de token JWT

fix(checkout): resolver cálculo de impuestos en moneda local
Closes #128

```

---

## 3. Requisitos para una Pull Request (PR)

Debes completar correctamente la plantilla de la pull request que facilitamos con el repositorio.

### Título de la PR

El título debe mantener la misma convención que los commits:

> *Ejemplo:* `feat(auth): implementar soporte para inicio de sesión con Google`

### Secciones a completar

* **Qué cambia**: Resume en una o dos frases las modificaciones exactas introducidas en el código.


* **Por qué**: Explica el problema que se resuelve, la necesidad técnica o la tarea que se completa con este cambio.


* **Cómo comprobarlo**: Detalla los pasos secuenciales para que el revisor pueda ejecutar, reproducir y verificar las modificaciones en su entorno local.


* **Closes #**: Indica el número de la incidencia o issue asociada (por ejemplo, `Closes #42`) para que se cierre de forma automática al mergear la rama.


### Verificaciones previas

* Todas las pruebas automáticas existentes deben ejecutarse y superarse localmente antes de enviar el cambio.
