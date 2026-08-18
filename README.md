
Proyecto M.E.I.A. (Macro-Infraestructura Empresarial Inmutable y Automatizada)

🚀 Visión General

Este es mi espacio personal de experimentación y aprendizaje. He montado el Proyecto M.E.I.A. desde cero con mis propios recursos para experimentar de primera mano cómo funciona una infraestructura de sistemas real y prepararme a fondo para el segundo curso de ASIR.


🖥️ El "Hierro" (Laboratorio Físico)
    Me gusta trabajar con hardware real. Actualmente, mi clúster en escritorio se compone de:
    
  Mila: 16 GB RAM / 250 GB NVMe (Nodo principal).
  
  Randun: 8 GB RAM / 250 GB SSD + 480 GB (WD externo) para Proxmox Backup Server.
    
  Gumball: 16 GB RAM / 480 GB SSD.
    
  Red: Tráfico gestionado por un switch Aruba 1930 y enrutamiento MikroTik AX3 (Router ISP solo como pasarela).


🏗️ Arquitectura Técnica y Segmentación
Implemento una arquitectura de red segmentada (VLANs IEEE 802.1Q) para simular entornos corporativos reales:

VLAN              Nombre                Propósito
10              Gestion interna         Management y acceso remoto seguro
20              DMZ Publica             exposicion controlada de servios web
30              Backed DB               Aislamiento de datos criticos 
40              Corporativo             Enterno Microsoft (Active Directoy)

🌐 Plataforma Web y Base de Datos (Proyecto NAC 31)
Front-End: Desarrollo y despliegue del proyecto NAC 31, una plataforma web alojada en la VLAN 20 (DMZ Pública), expuesta de forma segura mediante un proxy inverso con certificados SSL.

Back-End: Integración con base de datos relacional alojada en la VLAN 30 (Backend DB), garantizando el aislamiento total de los datos mediante políticas estrictas de firewall entre segmentos.

Orquestación: Gestión mediante contenedores Docker y volúmenes persistentes para asegurar la integridad de la información.


🛠️ Stack Tecnológico

  Virtualización: Proxmox VE (Bare-Metal).
    
  Redes/Firewall: pfSense (con WireGuard VPN).
    
  Identidad: Windows Server 2022 (Active Directory).
    
   Orquestación: Docker + Docker Compose + Traefik (Proxy Inverso).
    
   Automatización: Terraform (IaC) + Ansible (Gestión de configuración).
    
  Seguridad: Wazuh SIEM (Detección de incidentes en tiempo real).
    
   Resiliencia: Proxmox Backup Server (PBS).


   🧭 Mi Filosofía: "Aprender, Montar, Romper, Solucionar"
 Mi objetivo no es la perfección teórica, sino enfrentarme a los problemas reales. Este no es un proyecto acabado; es un entorno   vivo donde vivo en un bucle constante de mejora. Cada día aprendo, me equivoco, soluciono y vuelvo a empezar.

Desarrollado por: Christian Reinoso Mondragon
#SysAdmin #DevOps #ASIR #Proxmox #HomeLab #BuildInPublic
