# ISR401-PFC-ERS-[NombreEquipo]

Repositorio de la Práctica Experimental 4 (PE4), Unidad IV, de la asignatura
Ingeniería de Requerimientos (ISR-401), Carrera de Software, Universidad Técnica
Estatal de Quevedo. Período 2026–2027 PPA.

**Docente:** Ing. Gleiston Cicerón Guerrero Ulloa, PhD

**URL del repositorio:** https://github.com/USUARIO/ISR401-PFC-ERS-NOMBREEQUIPO

---

## Sistema

**[Nombre del sistema del PFC]** — [una o dos líneas describiendo qué hace el sistema,
a qué dominio pertenece y quiénes son sus usuarios principales].

---

## Integrantes y roles

| Integrante | Rol en la inspección Fagan | Rol en el CCB |
|---|---|---|
| [Apellidos Nombres] | Moderador | Presidente |
| [Apellidos Nombres] | Lector | Analista |
| [Apellidos Nombres] | Inspector 1 | Representante del cliente |
| [Apellidos Nombres] | Inspector 2 | Desarrollador |

---

## Estructura del repositorio

```
01_ERS/           ERS_v1.0.pdf, ERS_v1.1.pdf y fuentes .tex
02_Inspeccion/    AnexoA_checklists/, AnexoB_registro_defectos.xlsx, metricas.xlsx
03_CCB/           RFC-01.pdf, RFC-02.pdf, RFC-03.pdf, Acta_CCB.pdf
04_Trazabilidad/  matriz_trazabilidad.xlsx, backlog_export.csv, capturas/
05_Informe/       PE4_U4_APELLIDO1_APELLIDO2.tex, referencias.bib, figuras/
06_Evidencias/    capturas_git/, fotos_sesion/, declaracion_IA.pdf
CHANGELOG.md      Historial de versiones del ERS por RFC aprobada
```

---

## Compilación del informe

**Archivo principal:** `05_Informe/PE4_U4_APELLIDO1_APELLIDO2.tex`

### Dependencias

- Distribución LaTeX completa: TeX Live 2023 o superior, o MiKTeX
- Motor de compilación: `pdflatex`
- Procesador bibliográfico: `biber` (backend de biblatex, estilo IEEE)
- Clase: `IEEEtran`
- Paquetes: `babel` (spanish), `csquotes`, `biblatex`, `booktabs`, `tabularx`,
  `array`, `multirow`, `longtable`, `graphicx`, `float`, `xcolor`, `geometry`,
  `fancyhdr`, `parskip`, `enumitem`, `caption`, `titlesec`, `amssymb`,
  `mdframed`, `hyperref`
- Archivos requeridos en `05_Informe/`: `referencias.bib` y la carpeta `figuras/`

### Orden de comandos

```bash
cd 05_Informe
pdflatex PE4_U4_APELLIDO1_APELLIDO2.tex
biber    PE4_U4_APELLIDO1_APELLIDO2
pdflatex PE4_U4_APELLIDO1_APELLIDO2.tex
pdflatex PE4_U4_APELLIDO1_APELLIDO2.tex
```

**Salida:** `05_Informe/PE4_U4_APELLIDO1_APELLIDO2.pdf`

> `biber` recibe el nombre del archivo **sin extensión**. Las dos pasadas finales
> de `pdflatex` son necesarias para resolver las referencias cruzadas y la
> numeración de tablas y figuras.

### Compilación del ERS

El mismo procedimiento aplica a `01_ERS/ERS_v1.1.tex`, que tiene su propio
`referencias.bib` y su propia carpeta `figuras/`.

---

## Línea base

| Elemento | Valor |
|---|---|
| Versión vigente del ERS | v1.1 |
| Tag de línea base | `baseline-v1.1` |
| Aprobada por | CCB, sesión del [fecha] |

Verificación del tag publicado:

```bash
git tag -n
git ls-remote --tags origin
```

---

## Convención de commits

Se usan mensajes semánticos con los prefijos `docs`, `chore`, `feat` y `fix`,
seguidos del ámbito entre paréntesis. Ejemplos:

```
docs(ers): v1.1 - aplicar cambios aprobados por el CCB
docs(inspeccion): checklist Anexo A del Inspector 1
chore(repo): estructura de carpetas y exclusiones LaTeX
```
