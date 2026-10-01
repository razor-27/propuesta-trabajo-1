```mermaid
graph TD
    %% Definición de Actores
    subgraph Actores["👤 Actores del Sistema"]
        P["👨‍💼 Paciente"]
        M["👨‍⚕️ Personal Médico / Enfermería"]
        A["👩‍💼 Personal de Admisión"]
        TI["💻 Administrador de TI / Sistema"]
    end

    %% Módulo Citas y Admisión
    subgraph Modulo_Citas["📅 Módulo de Citas y Admisión"]
        CU01(("CU-01: Consultar y Agendar Cita"))
        CU02(("CU-02: Confirmar / Reprogramar Cita"))
        CU07(("CU-07: Admisión y Check-in"))
        CU08(("CU-08: Gestión de Alta"))
    end

    %% Módulo Historia Clínica Electronica y Triaje
    subgraph Modulo_HCE["🏥 Módulo de HCE y Emergencias"]
        CU03(("CU-03: Consultar HCE y Resultados"))
        CU04(("CU-04: Registrar Triaje"))
        CU05(("CU-05: Consultar / Registrar en HCE"))
        CU06(("CU-06: Emitir Órdenes Clínicas"))
    end

    %% Módulo de Gestión y Seguridad
    subgraph Modulo_TI["🔐 Seguridad e Interoperabilidad"]
        CU09(("CU-09: Monitoreo y Control RBAC/MFA"))
        CU10(("CU-10: Sincronización HL7/FHIR"))
    end

    %% Relaciones Paciente
    P --> CU01
    P --> CU02
    P --> CU03

    %% Relaciones Médico / Enfermería
    M --> CU04
    M --> CU05
    M --> CU06

    %% Relaciones Admisión
    A --> CU07
    A --> CU08

    %% Relaciones TI / Sistema
    TI --> CU09
    TI --> CU10

    %% Estilos de Nodos
    style P fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style M fill:#e8f5e9,stroke:#388e3c,stroke-width:2px
    style A fill:#fff3e0,stroke:#f57c00,stroke-width:2px
    style TI fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px