# Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-
Laboratorio de ciberseguridad con Snort y Mininet para detectar tráfico malicioso y analizar alertas IDS en tiempo real. Incluye descarga del malware Nimda, captura de paquetes y monitoreo de reglas de firewall en un entorno simulado de red.

Cybersecurity lab using Snort and Mininet to detect malicious traffic and analyze IDS alerts in real time. Includes Nimda malware download, packet capture, and firewall rule monitoring in a simulated network environment.

## 🔧 Tecnologías usadas / Technologies used
- Snort IDS
- Mininet
- Linux / Ubuntu
- tcpdump
- VirtualBox (mode Brigde)
- Malware (W32.Nimda)

**Nota:** No incluyo muestras de malware ni enlaces de descarga. En los pasos uso archivos locales o simulaciones para análisis seguro.

**Note:** I do not include malware samples or download links. In the steps, I use local files or simulations for safe analysis..



<p>This is something I'm doing in the labs where I study, and I want to share what I'm doing. I'll explain step by step what I achieve so I have something to show when I'm looking for a job.</p>

<p>Esto es algo que estoy realizando en los laboratorios de donde estudio y quiero compartir lo que estoy haciendo explicare paso a paso de lo que logro para tener algo que mostrar cuando busque un trabajo.</p>

## <p>In the lab, it requires me to have the cyberops virtual machine and the network in bridge mode.</p>
## <p>En el laboratorio me pide tener la maquina virtual Cyberops la red en modo puente.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/ConfigVirtualBox.png)

## <p>As a next step, it asked me to run the script for the network configuration of the mininet and it was located in this folder.</p>
## <p>Como siguiente paso me pedia el ejecutar el script para la configuración de red del mininet y se encontraba en esta carpeta.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/CyberopsScripts.png)

## <p>Ejecute el script para poder configurar las IPs necesarias en el laboratorio y luego ejecute el script para poder levantar la Mininet</p>
## <p>Run the script to configure the necessary IPs in the lab, and then run the script to start the Mininet.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/Configuraci%C3%B3n%20estatica.png)
![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/TopoCyberopsMininet.png)

## <p>Después abrir el R1 mediante la consola de xterm como lo pedia el laboratorio.</p>
## <p>then open R1 using the xterm console as requested by the lab.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/EjecutandoR1.png)

## <p> Inicie el IDS basado en Linux: Snort.</p>
## <p> Start the Linux-based IDS: Snort.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/SnortR1.png)

## <p>Abrí shells para los hosts H5 y H10 y en el laboratorio pedia que en H10 ejecute el servidor</p>
## <p>Open shells for the H5 and H10 hosts and in the lab it asked that the server run in H10 </p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/ShellH5-H10.png)
![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/ServerH10.png)

## <p>Como no sabia si el servidor estaba activo ejecute para ver si estaba activo en el puerto 80 pero no resulto asi que busque la manera de encontrar el puerto y logre dar con el y vi que estaba activo</p>
## <p>Since I didn't know if the server was active, I ran a command to check if it was active on port 80, but it didn't work. So I looked for a way to find the port and managed to locate it, and I saw that it was active.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/ErrorPort.png)
![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/ServidorGOD.png)

## <p>En el laboratorio para iniciar otro R1 para poder monitorear el archivo con el comando que se vera</p>
## <p>In the lab, to start another R1 in order to monitor the file with the command that will be shown</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/R1Logs.png)

## <p>Para seguir con el laboratorio descargue el malware desde el H1 usando la ip del servidor y el puerto</p>
## <p>To continue with the lab, download the malware from H1 using the server's IP address and port.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/ScriptV1Malware.png)
![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/MalwareDescargado.png)

## <p>Imagen del IDS mostrando que genero alerta de descarga en la IP del servidor y el puerto utilizado para descargar el malware</p>
## <p>Image from the IDS showing that it generated a download alert on the server's IP address and the port used to download the malware.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/IDSalert.png)

## <p> En H5, utilice el comando para capturar el evento y volver a descargar el  archivo malicioso y así poder capturar la transacción. Volvi a descargar el malware en H5</p>
## <p>In H5, use the command to capture the event and re-download the malicious file so you can capture the transaction. I re-downloaded the malware in H5.</p>

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/DownloadH5.png)

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/captureDone.png)

## WIRESHARK

![image](https://github.com/ChecheMC/Network-IDS-Firewall-Rules-Analysis-Lab-Snort-Mininet-/blob/main/ImgCyberops/captureWireshrak.png)



🚀 Conclusiones Profesionales / Professional Conclusion

Esta sección resume los hallazgos técnicos clave del laboratorio, demostrando las habilidades de Detección, Respuesta a Incidentes (IR) y Análisis Forense de Redes.
This section summarizes the key technical findings of the lab, demonstrating Detection, Incident Response (IR), and Network Forensics Analysis skills.

## 1. Resumen de Habilidades Técnicas / Technical Skills Summary
   
Habilidad (Skill) |	Evidencia Demostrada (Evidence Demonstrated)

Monitoreo IDS/NIDS (SOC) | Se implementó y monitoreó Snort en tiempo real en el router R1 (punto de inspección), logrando la detección inmediata de una amenaza conocida (Nimda).

Respuesta a Incidentes (IR) | Se realizó un Diagnóstico de Servicios (netstat) y se ejecutó una Captura Forense de tráfico (tcpdump) como acciones primarias de contención y recolección de evidencia.

Troubleshooting (Soporte Técnico) | Se diagnosticó y resolvió el conflicto de Address already in use en el puerto 6666/TCP, un problema crítico que impedía la simulación del ataque.

Análisis Forense | Se utilizó Wireshark para validar la traza de red capturada (nimda_h5_capture.pcap), confirmando la solicitud GET y la transferencia del archivo malicioso.

## 2. Hallazgos Específicos del Ataque / Specific Attack Findings

## Español

Punto de Detección: El IDS detectó la descarga del archivo W32.Nimda.Amm.exe al correlacionar el tráfico contra su base de firmas, incluso cuando el tráfico se realizaba sobre un puerto no estándar (6666/TCP).

Protocolo y Puerto: La comunicación con el servidor de malware (H10) se realizó sobre el Puerto 6666/TCP, utilizando el protocolo HTTP. Este desvío del puerto estándar (80) es una táctica común del adversario.

Análisis de Evidencia: La captura de tráfico confirmó el payload de la amenaza. El cliente H5 (209.165.200.235) realizó una solicitud GET, y el servidor H10 (209.165.202.133) respondió con un estado 200 OK, entregando el archivo binario a la red.

## English

Detection Point: The IDS successfully detected the download of the W32.Nimda.Amm.exe file by correlating traffic against its signature base, even though the communication used a non-standard port (6666/TCP).

Protocol and Port: Communication with the malware server (H10) occurred over Port 6666/TCP, utilizing the HTTP protocol. This deviation from the standard port (80) is a common adversary tactic.

Evidence Analysis: The traffic capture confirmed the threat payload. Client H5 (209.165.200.235) made a GET request, and server H10 (209.165.202.133) responded with a 200 OK status, delivering the binary file onto the network.

## 🌟 Declaración Final / Final Statement

[Mininet Laboratory] demostró la implementación práctica de controles de seguridad de red y las habilidades de un analista para diagnosticar problemas operativos, detectar amenazas en tiempo real y obtener evidencia forense para la post-explotación.

This project demonstrated the practical implementation of network security controls and the analyst's ability to diagnose operational issues, detect threats in real-time, and collect forensic evidence for post-exploitation analysis.











