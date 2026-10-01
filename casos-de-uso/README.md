# Módulo de Casos de Uso - Sistema Hospitalario

Este directorio contiene la especificación de casos de uso para la propuesta de arquitectura del Sistema Hospitalario de Huamanga.

## Diagrama General de Casos de Uso

```mermaid
graph TD
    P[Paciente] --> CU01(CU-01: Agendar Cita)
    P --> CU03(CU-03: Consultar HCE)
    M[Médico] --> CU04(CU-04: Registrar Triaje)
    M --> CU05(CU-05: Consultar HCE)
    A[Admisión] --> CU07(CU-07: Admisión y Check-in)
    TI[Administrador TI] --> CU09(CU-09: Control RBAC)