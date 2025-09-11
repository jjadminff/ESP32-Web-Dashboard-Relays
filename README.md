# 🌐 ESP32 Web Dashboard con Control de Relés

Este proyecto permite controlar múltiples **ESP32** conectados a relés desde un **Dashboard Web**.  
Cada ESP32 obtiene su propia IP local, la cual se integra en el panel principal para manejar remotamente dispositivos eléctricos.

---

## ⚙️ Requisitos

### Hardware
- 3 × ESP32  
- 2 × Módulos Relay  
- Cables USB tipo C  
- Fuentes de poder de 5V (o puertos USB de PC)

### Software
- [Arduino IDE](https://www.arduino.cc/en/software)  
- Librerías necesarias (añade aquí el listado exacto de librerías utilizadas, por ejemplo `WiFi.h`, `ESPAsyncWebServer.h`, etc.)

---

## 🚀 Instalación y Configuración

1. **Dashboard principal**  
   - Flashea el ESP32 con el código **`ESP32 Web Dashboard Main`**.  
   - Abre el **Serial Monitor** y guarda la **IP asignada** (la usarás en tu navegador).

2. **Relés (ESP32 secundarios)**  
   - Flashea los ESP32 con el código **`ESP32 Relay 1 & 2`**.  
   - Guarda las **dos IPs** generadas.  

3. **Configura el Dashboard**  
   - Abre el código del Dashboard.  
   - Añade las IPs de Relay 1 y Relay 2 en el **array de IPs**.  
   - Ejemplo:

     ```cpp
     const char* relayIPs[] = {
       "192.168.1.101", // Relay 1
       "192.168.1.102"  // Relay 2
     };
     ```

4. **Configura los pines GPIO**  
   - Cambia el pin de control de los relés si lo deseas (por defecto `GPIO 2`).  

---

## 🔌 Cableado

El siguiente diagrama muestra la conexión típica entre ESP32 y relé:

| ESP32 Pin | Relay Pin |
|-----------|-----------|
| GPIO 2    | IN        |
| 5V        | VCC       |
| GND       | GND       |

📎 Archivo adjunto: **`ESP32 & Relay Wiring Diagram`**

---

## 🖥️ Uso

1. Conecta los ESP32 a la PC o a fuentes de poder de 5V mediante USB tipo C.  
2. Abre la IP del **Dashboard** en el navegador.  
3. Controla el encendido y apagado de los relés desde la interfaz web.  

---

## 📸 Ejemplo de Interfaz (opcional)

*(Aquí puedes agregar capturas de pantalla del Dashboard y del montaje físico)*

---

## 📝 Notas
- Todos los ESP32 son alimentados con **USB tipo C** y fuentes de poder de **5V**.  
- Proyecto desarrollado con **Arduino IDE**.  

---

## 📄 Licencia
Este proyecto es de uso libre para fines educativos y experimentales.  

---
