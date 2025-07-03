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
## Documento de Informe Proyecto Final  
**Versión 2.0**

---

# ÍNDICE GENERAL

1. [Antecedentes](#1-antecedentes)  
2. [Planteamiento del Problema](#2-planteamiento-del-problema)  
   2.1. Problema  
   2.2. Justificación  
   2.3. Alcance  
3. [Objetivos](#3-objetivos)  
4. [Marco Teórico](#4-marco-teórico)  
5. [Desarrollo de la Solución](#5-desarrollo-de-la-solución)  
   5.1. Análisis de Factibilidad  
   5.2. Tecnología de Desarrollo  
   5.3. Metodología de Implementación  
6. [Cronograma](#6-cronograma)  
7. [Presupuesto](#7-presupuesto)  
8. [Conclusiones](#8-conclusiones)  
9. [Recomendaciones](#9-recomendaciones)  
10. [Bibliografía](#10-bibliografía)  
11. [Anexos](#11-anexos)  
   - Anexo 01: Informe de Factibilidad  
   - Anexo 02: Documento de Visión  
   - Anexo 03: Documento SRS  
   - Anexo 04: Documento SAD  
   - Anexo 05: Manuales y Otros Documentos  

---
# 1. Antecedentes

En el contexto académico actual, los estudiantes y docentes de ingeniería de sistemas enfrentan dificultades crecientes para comprender, documentar y evaluar grandes volúmenes de código fuente. La ausencia de herramientas automatizadas que apoyen la interpretación estructurada del código afecta la calidad del aprendizaje, la eficiencia del desarrollo y la comprensión de buenas prácticas en programación. Las revisiones manuales de código suelen ser lentas, subjetivas y poco escalables, especialmente en cursos con numerosos participantes.

En respuesta a estas necesidades, surge el proyecto DocuCode-AI, una plataforma web que utiliza Inteligencia Artificial para analizar código fuente, generar automáticamente documentación técnica, diagramas UML y evaluaciones de calidad. Este sistema busca apoyar tanto a docentes en sus procesos de revisión como a estudiantes en el entendimiento del diseño y arquitectura del software.

---

# 2. Planteamiento del Problema

## a. Problema

Actualmente, los procesos de revisión y documentación del código fuente en entornos académicos son mayormente manuales, lo que genera demoras, errores de interpretación y dificultades para validar la calidad del software desarrollado por los estudiantes. No existen herramientas integradas que automaticen el análisis estructural del código ni que generen documentación técnica útil para el aprendizaje.

## b. Justificación

Este proyecto es importante porque responde a una necesidad concreta del entorno educativo: facilitar la comprensión del código fuente mediante el uso de tecnologías emergentes. Al integrar algoritmos de IA y generación de UML, se proporciona una solución moderna y efectiva que optimiza el proceso de enseñanza-aprendizaje, fomenta buenas prácticas de codificación, y reduce el tiempo de evaluación. Su implementación permitirá a los docentes centrarse más en el contenido y menos en tareas repetitivas, mejorando así la calidad educativa.

## c. Alcance

El sistema DocuCode-AI se implementará como una plataforma web accesible desde navegadores modernos. Permitirá la carga de archivos individuales o comprimidos (RAR/ZIP), su análisis automático, y la generación de reportes con comentarios de código, diagramas UML (clases, casos de uso, secuencia, actividad, componentes, paquetes, etc.), evaluación de calidad y detección de duplicados. El sistema está orientado al uso académico y no contempla funcionalidades de despliegue en producción empresarial.

---

# 3. Objetivos

## Objetivo General

Diseñar e implementar un sistema web basado en inteligencia artificial que permita analizar código fuente, generar documentación técnica automática y evaluar su calidad, con fines educativos en el contexto universitario.

## Objetivos Específicos

- Desarrollar un sistema web con arquitectura Facade que permita subir y procesar archivos de código fuente.
- Implementar una integración con la API de OpenAI para generar comentarios y descripciones automáticas del código.
- Generar diagramas UML automáticos a partir del análisis del código.
- Evaluar la calidad del código fuente utilizando criterios estructurales y sintácticos.
- Detectar posibles duplicaciones o similitudes entre bloques de código.
- Diseñar una interfaz amigable y accesible para usuarios docentes y estudiantes.
- Documentar el sistema, sus funcionalidades y arquitectura, integrando estándares académicos.

---

# 4. Marco Teórico

## 4.1 Sistemas Web y su Rol Académico

Sommerville (2020) indica que los sistemas web son ideales para entornos educativos, ya que centralizan el acceso, permiten escalabilidad y fomentan la colaboración. DocuCode-AI brinda una herramienta en línea para analizar, interpretar y documentar proyectos de software de forma estructurada.

## 4.2 Patrón Arquitectónico MVC

El patrón Modelo-Vista-Controlador (MVC), propuesto por Krasner y Pope (1988), facilita la separación de responsabilidades. DocuCode-AI adopta este patrón para organizar sus funcionalidades, especialmente en la gestión modular del análisis y generación de diagramas.

## 4.3 Diagramas UML como Herramienta de Documentación

UML es el estándar de modelado más usado para representar sistemas de software. Pressman y Maxim (2020) afirman que permite entender, validar y documentar sistemas. DocuCode-AI genera automáticamente diagramas UML (clases, casos de uso, secuencia, actividad, etc.) usados en informes técnicos.

## 4.4 Inteligencia Artificial Aplicada a la Ingeniería de Software

Leiva Suero et al. (2020) señalan que la IA permite representar estructuras de código mediante técnicas automáticas. DocuCode-AI interpreta archivos y genera representaciones gráficas basadas en patrones del sistema.

## 4.5 Evaluación de Calidad y Código Duplicado

Martin (2009) indica que un código limpio mejora la productividad y reduce errores. DocuCode-AI incluye análisis de calidad (legibilidad, modularidad, estilo) y detección de código duplicado para reforzar buenas prácticas.

---

# 5. Desarrollo de la Solución

## a. Análisis de Factibilidad

**Técnica:** Tecnologías: PHP, JS, PlantUML, OpenAI, MySQL. Arquitectura MVC.  
**Económica:** Software libre. Solo gastos opcionales por hosting y tokens OpenAI.  
**Operativa:** Intuitivo, de fácil uso, útil para docentes y estudiantes.  
**Social:** Mejora la calidad de documentación, promueve autonomía.  
**Legal:** Cumple normativas de protección de datos. Herramientas con licencias abiertas.  
**Ambiental:** Digitalización total, elimina impresión.

## b. Tecnología de Desarrollo

- Backend: PHP 8.x MVC  
- Frontend: HTML5, CSS3, Bootstrap 5, JS  
- DB: MySQL/MariaDB  
- Diagramas: PlantUML (.puml)  
- IA: OpenAI API  
- DevOps: GitHub Actions, GitHub Pages, Composer, XAMPP

## c. Metodología de Implementación

SCRUM con 5 sprints:

1. Requisitos y prototipo  
2. Carga y lectura de archivos  
3. Generación UML con PlantUML  
4. Evaluación de calidad con IA  
5. Documentación y despliegue

## d. Documentos Clave

- **FD02:** Documento de Visión  
- **FD03:** Documento de Especificación de Requisitos (SRS)  
- **FD04:** Documento de Arquitectura de Software (SAD)

---

# 6. Cronograma

| Fase | Actividades | Inicio | Fin | Responsable |
|------|-------------|--------|-----|-------------|
| 1 | Requisitos, prototipo, modelo E-R | 01/04/2025 | 07/04/2025 | Todo el equipo |
| 2 | Carga de archivos y análisis | 08/04/2025 | 15/04/2025 | Todo el equipo |
| 3 | Diagramas UML | 16/04/2025 | 23/04/2025 | Todo el equipo |
| 4 | Integración con IA | 24/04/2025 | 30/04/2025 | Todo el equipo |
| 5 | Documentación, despliegue | 01/05/2025 | 06/07/2025 | Líder del proyecto |

---

# 7. Presupuesto

| Concepto | Detalle | Costo Estimado |
|----------|---------|----------------|
| VPS | Elastika (2 vCPU, 4GB RAM, 50GB SSD) anual | S/ 100.00 |
| Dominio + SSL | Hostinger | S/ 12.00 |
| OpenAI | Tokens uso mensual estimado | S/ 20.00 |
| Herramientas Dev | VS Code, GitHub, Composer | S/ 0.00 |
| **Total anual estimado** |  | **S/ 132.00** |

---

# 8. Conclusiones

- Se cumplió el objetivo de generar documentación técnica automatizada.
- Se logró generar diagramas, evaluar calidad, y detectar duplicados.
- Arquitectura modular facilitó mantenibilidad.
- Herramientas modernas permitieron exploración tecnológica real.
- Proyecto completado en tiempo y forma, con roles bien definidos.

---

# 9. Recomendaciones

- Incluir soporte para C++, C#.
- Optimizar análisis con colas de tareas.
- Integración con LMS como Moodle.
- Métricas avanzadas de calidad.
- Generación de reportes Word/PDF.
- Mantener metodología ágil para evolución continua.

---

# 10. Bibliografía

- Pressman, R. & Maxim, B. (2020). *Ingeniería de Software*. McGraw-Hill.  
- Sommerville, I. (2020). *Software Engineering*. Pearson.  
- Martin, R. C. (2009). *Clean Code*. Prentice Hall.  
- Krasner & Pope (1988). *MVC en Smalltalk-80*.  
- Leiva Suero et al. (2020). *Aplicación de IA en código fuente*.  
- Fowler, M. (2002). *Enterprise Architecture*.  
- Documentación oficial: [OpenAI](https://platform.openai.com/docs), [PlantUML](https://plantuml.com), [Terraform](https://www.terraform.io), [Marp](https://marp.app)

---

# 11. Anexos

Repositorio:  
🔗 https://github.com/UPT-FAING-EPIS/proyecto-si889-2025-i-u3-docucodeai-1

- **Anexo 01**: Informe de Factibilidad (FD01)  
- **Anexo 02**: Documento de Visión (FD02)  
- **Anexo 03**: Documento SRS (FD03)  
- **Anexo 04**: Documento SAD (FD04)  
- **Anexo 05**: Manuales y otros documentos  
---