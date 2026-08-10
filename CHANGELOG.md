# Changelog

Todas las modificaciones relevantes del ERS de MundiPets se documentan en este archivo,
con una entrada por cada RFC aprobada por el Comité de Control de Cambios (CCB).

## [1.1] - 2026-08-09

Versión resultante de la sesión del CCB (09/08/2026, 14:00–15:10), que integra las
tres RFC aprobadas junto con la corrección de los 18 defectos críticos y mayores
identificados en la inspección Fagan. Cierra el defecto D-04.

### Añadido
- RF-26 (RFC-01): nuevo requisito para el aviso de extravío con canal de contacto
  mediado entre el publicador y el solicitante; RF-25 deja de exponer los datos de
  contacto directos y muestra en su lugar la zona aproximada y el número de microchip.
- RF-27 (RFC-03): nuevo requisito de revocación del consentimiento informado, con
  despublicación en cascada, notificación a las contrapartes de procesos en curso y
  estado reversible de 30 días antes del borrado definitivo.

### Cambiado
- RF-25 y RNF-16 (RFC-01, defecto D-07): se resuelve el conflicto crítico entre ambos
  requisitos; RNF-16 incorpora la excepción declarada para avisos de extravío activos.
- RF-07 (RFC-01, condición 1 del CCB): repriorizado de *Could have* a *Should have*
  para que RF-26 sea implementable.
- RF-06 (RFC-02, defecto D-18): la salida pasa de "información comparativa" a un
  veredicto de compatibilidad en tres niveles (compatible / con reservas / no
  recomendado), acompañado de la explicación exigida por RNF-13.
- RNF-06 (RFC-02, defecto D-20): criterio de verificación acotado a coincidencia
  mínima del 85 % sobre 40 pares de mascotas evaluados por 3 médicos veterinarios,
  con regla de exclusión para pares sin mayoría.
- RF-02, RF-03, RF-11 y RF-14 (RFC-03, defecto D-21): se incorpora plazo máximo de
  15 días para que el propietario consulte y rectifique la información registrada,
  conforme a RL-02 y RL-03.
- RF-01 (RFC-03, defecto D-22): se añade la aceptación del consentimiento informado
  como entrada obligatoria, con marca temporal y versión de términos aceptados.
- Carátula del ERS (defecto D-04): versión del documento actualizada de 1.0 a 1.1,
  coherente con el historial de revisiones, este CHANGELOG y el tag `baseline-v1.1`.
- §5.5, Tabla 96 y Apéndice D (defecto D-01, p. 97): se corrigió la cantidad de filas
  de la matriz de trazabilidad extendida, de 40 a 50 (TR-01 a TR-50), unificando la
  cifra entre las tres referencias del documento que antes eran inconsistentes entre sí.
- Apéndice H, ítem 14 (defecto D-03, p. 146): se actualizaron las cantidades del
  checklist de aceptación previo al corte a 27 RF, 16 RNF y 50 filas de trazabilidad,
  que correspondían a una versión anterior del ERS, e incorporó la fecha de la última
  verificación.

### Eliminado
- Ninguno.

---

## [1.0] - Versión inicial

Versión base del ERS de MundiPets, entregada en la PE2 (Entrega 2A), previa a la
inspección Fagan y a la gestión de cambios de la PE4.
