proyecto-mei-infrastructure
proyecto M.E.I.A. Macro-Infraestructura Empresarial Inmutable y Automatizada

Este repositorio contiene la documentación, planos lógicos, manifiestos de Infraestructura como Código (IaC) y scripts de automatización para el despliegue del entorno corporativo avanzado M.E.I.A., diseñado como preparación para el segundo bloque del ciclo superior de ASIR.

Bloque 1: Inicialización del Hierro y Virtualización Base (Completado)

En este primer bloque se ha preparado el nodo de cómputo físico base y se ha estabilizado el entorno del hipervisor para los despliegues posteriores.

Ficha Técnica del Hardware (Nodo 'uno')
Hardware:Lenovo ThinkCentre M920q Tiny (USFF)
Procesador: Intel Core i5-8500T (6 núcleos reales)
Memoria RAM: 8 GB DDR4 (Base)
Almacenamiento: 240 GB NVMe M.2
Hipervisor: Proxmox VE 9.2.3 (Bare-Metal Tipo 1)

Desafíos Técnicos y Soluciones Aplicadas

1 Topología de Red Temporal (Puente de Red):Debido a restricciones físicas temporales de espacio, el nodo `uno` se configuró inicialmente mediante un puente de red Ethernet Cat 6e conectado a una laptop auxiliar para heredar conectividad y permitir el aprovisionamiento inicial por DHCP.
2.Estabilización de Repositorios APT (Licenciamiento):Se solventó el error de suscripción corporativa (`pve-enterprise`) que provocaba fallos de autenticación (código 401 Unauthorized). Se desactivaron los repositorios de pago y se inyectaron las listas comunitarias de producción gratuita `No-Subscription`. El sistema se encuentra 100% actualizado y libre de alertas de dependencias.

Las evidencias gráficas del panel de control de Proxmox totalmente actualizado y estabilizado se encuentran alojadas en la carpeta `/docs`.
