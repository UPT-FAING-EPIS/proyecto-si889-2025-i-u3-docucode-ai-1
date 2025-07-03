<center>

[comment]: <img src="./media/media/image1.png" style="width:1.088in;height:1.46256in" alt="escudo.png" />

![./media/logo-upt.png](./media/logo-upt.png)

**UNIVERSIDAD PRIVADA DE TACNA**  
**FACULTAD DE INGENIERIA**  
**Escuela Profesional de Ingeniería de Sistemas**  

**Proyecto DocuCode-AI**  
Curso: *PATRONES DE SOFTWARE*  
Docente: *PATRICK JOSE CUADROS QUIROGA*  

**Integrantes:**  
Farley Rodrigo Eduardo Viveros Blanco - 2020066896  
Ronal Daniel Lupaca Mamani - 202006146  

**Tacna – Perú**  
**2025**

</center>

---

# CONTROL DE VERSIONES

| Versión | Hecha por | Revisada por | Aprobada por | Fecha       | Motivo              |
|---------|-----------|--------------|--------------|-------------|---------------------|
| 1.0     | MPV       | ELV          | ARV          | 3/04/2025   | Versión Original    |
| 2.0     | MPV       | ELV          | ARV          | 30/05/2020  | Mejora              |

---

# Sistema DocuCode-AI  
## DICCIONARIO DE DATOS
**Versión 2.0**

---

# Índice General

1. Modelo Entidad / Relación  
  1.1 Diseño Lógico  
  1.2 Diseño Físico  
2. Diccionario de Datos  
  2.1 Tablas  
  2.2 Lenguaje de Definición de Datos (DDL)  
  2.3 Lenguaje de Manipulación de Datos (DML)  

---

# 1. Modelo Entidad / Relación  
## 1.1 Diseño Lógico (PlantUML)

![alt text](<diseño logico.png>)

---

## 1.2 Diseño Físico

![alt text](<diseño fisico.png>)
---

# 2. Diccionario de Datos  
## 2.1 Tablas

### Tabla: `usuarios_github`  
**Descripción:** Registro de usuarios que usan el sistema DocuCodeAI.  
**Relaciones:** PK, clave foránea para `historial_analisis`.

| Nro | Campo        | Tipo         | Nulo | PK | FK | Descripción                         |
|-----|--------------|--------------|------|----|----|-------------------------------------|
| 1   | id           | int          | No   | Sí | No | Identificador único del usuario     |
| 2   | github_id    | varchar(50)  | Sí   | No | Sí | ID externo de GitHub                |
| 3   | nombre       | varchar(100) | Sí   | No | No | Nombre del usuario                  |
| 4   | usuario      | varchar(50)  | Sí   | No | No | Nombre de usuario GitHub            |
| 5   | email        | varchar(100) | Sí   | No | No | Correo electrónico                  |
| 6   | avatar_url   | text         | Sí   | No | No | URL del avatar                      |

---

### Tabla: `historial_analisis`  
**Descripción:** Historial de análisis realizados por los usuarios.  
**Relaciones:** FK hacia `usuarios_github`.

| Nro | Campo                 | Tipo         | Nulo | PK | FK | Descripción                                  |
|-----|-----------------------|--------------|------|----|----|----------------------------------------------|
| 1   | id                    | int          | No   | Sí | No | ID único del análisis                        |
| 2   | usuario_github_id     | int          | No   | No | Sí | Usuario que realizó el análisis              |
| 3   | archivo               | varchar(255) | Sí   | No | No | Nombre del archivo analizado                 |
| 4   | resumen               | text         | Sí   | No | No | Resumen generado                             |
| 5   | calidad               | text         | Sí   | No | No | Evaluación de calidad                        |
| 6   | duplicados            | text         | Sí   | No | No | Código duplicado                             |
| 7   | diagramas_clase       | text         | Sí   | No | No | Diagrama de clases                           |
| 8   | diagramas_uso         | text         | Sí   | No | No | Diagrama de casos de uso                     |
| 9   | diagramas_componentes | text         | Sí   | No | No | Diagrama de componentes                      |
| 10  | diagramas_paquetes    | text         | Sí   | No | No | Diagrama de paquetes                         |
| 11  | diagramas_actividad   | text         | Sí   | No | No | Diagrama de actividad                        |
| 12  | diagramas_secuencia   | text         | Sí   | No | No | Diagrama de secuencia                        |
| 13  | fecha                 | datetime     | Sí   | No | No | Fecha del análisis                           |
| 14  | github_user_id        | varchar(50)  | No   | No | No | ID GitHub textual                            |

---

## 2.2 Lenguaje de Definición de Datos (DDL)

### 2.2.1 `CREATE DATABASE` y `DROP DATABASE`

```sql
CREATE DATABASE IF NOT EXISTS docucodeai
  DEFAULT CHARACTER SET latin1
  COLLATE latin1_swedish_ci;

DROP DATABASE IF EXISTS docucodeai;
```

---

### 2.2.2 `CREATE TABLE` y `DROP TABLE`

```sql
-- Tabla: usuarios_github
CREATE TABLE IF NOT EXISTS usuarios_github (
  id INT AUTO_INCREMENT PRIMARY KEY,
  github_id VARCHAR(50),
  nombre VARCHAR(100),
  usuario VARCHAR(50),
  email VARCHAR(100),
  avatar_url TEXT,
  UNIQUE (github_id)
);

-- Tabla: historial_analisis
CREATE TABLE IF NOT EXISTS historial_analisis (
  id INT AUTO_INCREMENT PRIMARY KEY,
  usuario_github_id INT NOT NULL,
  archivo VARCHAR(255),
  resumen TEXT,
  calidad TEXT,
  duplicados TEXT,
  diagramas_clase TEXT,
  diagramas_uso TEXT,
  diagramas_componentes TEXT,
  diagramas_paquetes TEXT,
  diagramas_actividad TEXT,
  diagramas_secuencia TEXT,
  fecha DATETIME DEFAULT current_timestamp(),
  github_user_id VARCHAR(50),
  FOREIGN KEY (usuario_github_id) REFERENCES usuarios_github(id)
);
```

---


---

