# Arquitectura de Software: Sistema de Control Remoto para DVAs

Este repositorio documenta el diseño arquitectónico de un sistema de control remoto para dispositivos DVA (Detector de Víctimas de Avalanchas), utilizado en prácticas de rescate en nieve. El proyecto fue desarrollado para la materia **Arquitectura de Software** (Optativa) en la UNRN (2025).

## Contexto del Sistema
El sistema permite gestionar de forma remota múltiples dispositivos DVA enterrados en la nieve, facilitando la simulación de rescates sin necesidad de activación manual en el sitio. 

## Atributos de Calidad y Requerimientos
El diseño se centró en cumplir con atributos de calidad críticos para entornos de emergencia:
- **Disponibilidad:** Garantizar que el sistema responda durante la ventana de tiempo de la práctica.
- **Interoperabilidad:** Comunicación fluida entre la aplicación de escritorio (Qt) y el hardware embebido mediante LoRa.
- **Rendimiento:** Latencia mínima en la transmisión de comandos para una activación casi instantánea.

## Diseño Arquitectónico (Modelo 4+1 Vistas)
Se aplicó el modelo de Kruchten para describir el sistema desde múltiples perspectivas:

- **Vista Lógica (MVC):** Implementación del patrón Modelo-Vista-Controlador para desacoplar la lógica de negocio de la interfaz de usuario en Qt.
- **Vista de Procesos:** Modelado del comportamiento dinámico mediante diagramas de secuencia para los casos de uso.
- **Vista de Despliegue:** Arquitectura de red distribuida que incluye una Aplicación, un nodo Maestro (Control) y múltiples nodos Esclavos (DVAs) comunicados por LoRa P2P.

## Tecnologías Utilizadas
- **Lenguajes:** C++.
- **Framework:** Qt Creator (Interfaz de Usuario).
- **Comunicación:** Protocolo LoRa P2P.
- **Modelado:** PlantUML / Diagramas de arquitectura.

## Contenido del Repositorio
- `/documentacion`: Informe técnico final con el detalle de las vistas y decisiones de diseño.
- `/diagramas`: Diagramas presentados en el Informe.
