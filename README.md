# TechBlog

# 🌐 Ciclo de vida de una petición web

Este documento describe de manera simplificada cómo funciona el ciclo de vida de una petición web desde que el usuario hace clic en un enlace o envía un formulario, hasta que recibe la respuesta del servidor en su navegador.

---

## 📌 Pasos principales

1. **Usuario realiza una acción** (ejemplo: clic en un enlace o enviar un formulario).  
2. **El navegador construye la petición HTTP** (método, cabeceras, parámetros).  
3. **La petición viaja por Internet** (DNS, protocolo TCP/IP).  
4. **El servidor web recibe la solicitud**.  
5. **El servidor procesa la petición** (por ejemplo, ejecuta un script en Node.js, PHP, Python, etc.).  
6. **El servidor accede a la base de datos** si es necesario.  
7. **El servidor genera una respuesta HTTP** (código de estado, cabeceras, cuerpo).  
8. **La respuesta viaja de regreso al navegador**.  
9. **El navegador interpreta la respuesta** (HTML, CSS, JS) y la muestra al usuario.  

---

## 🖼️ Diagrama del ciclo de vida

```mermaid
sequenceDiagram
    participant U as Usuario (Navegador)
    participant D as DNS
    participant S as Servidor Web
    participant DB as Base de Datos

    U->>D: 1. Solicita dirección del dominio
    D-->>U: 2. Devuelve dirección IP
    U->>S: 3. Envía petición HTTP
    S->>DB: 4. Consulta datos si es necesario
    DB-->>S: 5. Devuelve resultados
    S-->>U: 6. Respuesta HTTP (HTML, CSS, JS)
    U->>U: 7. Renderiza la página
