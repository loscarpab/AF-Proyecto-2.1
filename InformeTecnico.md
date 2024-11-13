# Adquisición máquina comprometida

Para realizar esta adquisición he seguido la siguiente [metodología](https://github.com/IES-Rafael-Alberti/AF-proyecto-01-G2/blob/main/InformeTecnico.md) realizada por nuestro grupo.
La maquina se encontró en el siguiente estado:
![estadoInicial](/pictures/estadoinicial.png)

## Preparación

Como la máquina estaba encendida, no se apaga, se deja tal como está. Para poder empezar con la adquisición se necesita estar preparados, para ello tengo un disco duro externo con las herramientas a utilizar en este caso. Las elegidas son:
+ **Ram Capturer**: para adquirir de manera segura el contenido completo de una memoria volátil.
+ **IRTriage**: este proceso sirve para identificar, clasificar y priorizar incidentes.
+ **FTK Imager**: para adquirir una imagen de la memoria no volátil, en este caso de su disco duro.

## Adquisición

### **Adquisición de Memoria RAM**
La captura de la memoria volátil (RAM) es crítica en una investigación forense, especialmente en un sistema encendido, pues almacena información en tiempo real que puede perderse al apagar el sistema. Se utilizó la herramienta **RAM Capturer** de Belkasoft para asegurar la adquisición confiable de la memoria.

#### **Procedimiento:**
1. **Preparación**:
   - Antes de iniciar la captura, se documentaron todos los datos de identificación del sistema y el entorno físico, manteniendo un registro visual del estado inicial (inserte foto del entorno aquí).
   - Se conectó un dispositivo de almacenamiento externo (USB) de confianza para guardar la imagen de la memoria RAM.

2. **Ejecución**:
   - Se inició **RAM Capturer** desde el dispositivo externo.
   - Se configuró la herramienta para capturar la memoria completa del sistema en su estado actual.
   - Se inició el proceso de adquisición, supervisando que la transferencia se completara sin interrupciones.

3. **Preservación y Verificación**:
   - La imagen de memoria fue guardada en el dispositivo externo, generando el hash correspondiente (MD5 y SHA-1) para su verificación.
   - **Hash MD5**: [871EFDCFD16633684E012FBBD1B1DF15]
   - **Hash SHA-1**: [423A1A6DA14D654E84E7F607D53F242C77E2714E]
   - La memoria capturada fue asegurada en el dispositivo externo, y se desconectó este dispositivo de manera segura para evitar alteraciones.

![RAM](/pictures/aduquisiciónRam.png)

---

### **3.2 Triage del Sistema con IRTriage**
Para realizar un análisis preliminar de la configuración y posibles indicios críticos, se utilizó **IRTriage**. Esta herramienta permite recopilar datos básicos del sistema sin alterar la evidencia principal, permitiendo la identificación de artefactos relevantes como procesos, conexiones de red activas, y archivos recientes.

#### **3.2.1 Procedimiento:**
1. **Preparación**:
   - IRTriage fue ejecutado desde un dispositivo externo para evitar modificaciones en el sistema.
   
2. **Ejecución**:
   - Se configuró IRTriage para capturar información de procesos activos, conexiones de red, y servicios en ejecución.
   - Se procedió a ejecutar un análisis rápido, con todos los datos recolectados almacenados en el dispositivo externo.
   
3. **Preservación y Verificación**:
   - Los datos de triage fueron guardados y verificados en el dispositivo externo.

![IRTriage](/pictures/IRTriage.png)

---

### **3.3 Adquisición Forense del Disco Duro con FTK Imager**
La obtención de una copia completa del disco duro es un paso fundamental para preservar todos los archivos y registros del sistema operativo de manera íntegra. Se utilizó **FTK Imager** para realizar esta copia forense del disco duro.

#### **3.3.1 Procedimiento:**
1. **Preparación**:
   - Antes de la adquisición, se conectó un dispositivo de almacenamiento externo con suficiente capacidad para guardar la imagen del disco duro.
   - Se verificaron las conexiones y el estado del dispositivo de destino para evitar fallos durante el proceso.

2. **Ejecución**:
   - FTK Imager fue ejecutado desde un entorno externo, seleccionando la opción de crear una imagen completa del disco en formato **RAW**.
   - La herramienta fue configurada para generar automáticamente los hashes MD5 y SHA-1 de la imagen, asegurando así su autenticidad y permitiendo la futura verificación.

3. **Preservación y Verificación**:
   - Al finalizar la copia, se generaron y verificaron los hashes correspondientes.
   - La imagen forense fue asegurada en el dispositivo externo y desconectada adecuadamente tras la verificación.

![IRTriage](/pictures/FTK.png)

---
## Acta de adquisicón RAM
| Acta de Adquisición Forense |                                                              |
|-----------------------------|--------------------------------------------------------------|
| Fecha y hora                | 13/11/24 18:25          |
| Lugar                       | Cádiz        |
| Perito forense              | Carlos Cordero Moreno                |
| Solicitante                 | Manuel Rivas |
| **Descripción del dispositivo** |                                                          |
| Tipo de dispositivo         | Memoria RAM         |
| Marca y modelo              | HP Pavilion 17                                        |
| Número de serie             | 05248463489                                  |
| Capacidad                   | 1GB                       |
| Estado físico               | Bueno                |
| **Procedimiento de adquisición** |                                                         |
| Método de adquisición       | Extracción lógico                   |
| Herramientas utilizadas     | RAM Capturer desde un disco duro externo                       |
| **Integridad de la evidencia** |                                                           |
| Valor hash original         | 871EFDCFD16633684E012FBBD1B1DF15              |
| Algoritmo utilizado         | MD5                                           |
| Valor hash de la copia      | 871EFDCFD16633684E012FBBD1B1DF15                   |
| **Observaciones**           | ---|

## Acta de adquisicón del disco duro
| Acta de Adquisición Forense |                                                              |
|-----------------------------|--------------------------------------------------------------|
| Fecha y hora                | 13/11/24 20:15          |
| Lugar                       | Cádiz        |
| Perito forense              | Carlos Cordero Moreno                |
| Solicitante                 | Manuel Rivas |
| **Descripción del dispositivo** |                                                          |
| Tipo de dispositivo         | Disco duro         |
| Marca y modelo              | HP Pavilion 17                                        |
| Número de serie             | 6536543544544                                  |
| Capacidad                   | 25GB                       |
| Estado físico               | Bueno                |
| **Procedimiento de adquisición** |                                                         |
| Método de adquisición       | Extracción lógico                   |
| Herramientas utilizadas     | FTK Imager desde un disco duro externo                       |
| **Integridad de la evidencia** |                                                           |
| Valor hash original         | 918169d48905681456c51ae-4a4e55a44              |
| Algoritmo utilizado         | MD5                                           |
| Valor hash de la copia      | 918169d48905681456c51ae-4a4e55a44                   |
| **Observaciones**           | ---|


## Cadena de custodia

| Tipo de evidencia  | Fecha y hora de recolección | Recolectado por     | Hash de la evidencia                       | Método de adquisición | Estado de la evidencia |
|------------------- |----------------------------|---------------------|-------------------------------------------|-----------------------|------------------------|
| Disco duro (C:)    | 2024-11-13 20:15 AM         | Carlos Cordero          |  918169d48905681456c51ae-4a4e55a44    | Imagen forense         | Sellado y etiquetado    |
| Memoria RAM        | 2024-11-13 18:25 AM         | Carlos Cordero          | 871EFDCFD16633684E012FBBD1B1DF15  | Captura de memoria     | Sellado y etiquetado    |
