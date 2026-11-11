[informe_de_avance.md](https://github.com/user-attachments/files/34702563/informe_de_avance.md)
# **SmartGrow (Cuidador de Planta Automático) - Informe de Avance**

**Autores:** Lucas Santiago Pozo, Nicolás Uriel Koo, Andrés Maturano
**Padrones:** 113786, 113609, 113884
**Fecha:** 2do cuatrimestre 2026

A continuación se detalla el informe de avance del Trabajo Final basándose en los requisitos planteados en la Propuesta, utilizando un esquema de colores para definir el estado de cada punto:

| Estado | Descripción |
| :---: | :--- |
| 🟢 | Ya implementado / Completado |
| 🟡 | En proceso de implementación |
| 🔴 | No se implementará / Descartado o con retraso crítico |

### **1. Actuadores de Riego**
| Req ID | Descripción | Estado |
| :--- | :--- | :---: |
| 1.1 | El sistema contará con una micro-bomba de agua para regar la planta. | 🟢 |
| 1.2 | El sistema accionará la bomba únicamente cuando la lectura de humedad del suelo caiga por debajo del umbral configurado. | 🟡 |

### **2. Climatización**
| Req ID | Descripción | Estado |
| :--- | :--- | :---: |
| 2.1 | El sistema contará con un ventilador para renovar el aire y reducir la temperatura/humedad. | 🟢 |
| 2.2 | El ventilador se activará automáticamente si la temperatura o humedad ambiente supera el umbral máximo. | 🟡 |

### **3. Iluminación**
| Req ID | Descripción | Estado |
| :--- | :--- | :---: |
| 3.1 | El sistema contará con tiras de luz LED orientadas a la planta. | 🟢 |
| 3.2 | El encendido de las luces seguirá un ciclo diario programable. | 🟡 |

### **4. Sensores**
| Req ID | Descripción | Estado |
| :--- | :--- | :---: |
| 4.1 | El sistema contará con un sensor de humedad de suelo. | 🟢 |
| 4.2 | El sistema contará con un sensor de temperatura y humedad ambiente (DHT11/DHT22). | 🟢 |

### **5. Indicadores y Hardware de Interfaz**
| Req ID | Descripción | Estado |
| :--- | :--- | :---: |
| 5.1 | El sistema contará con un indicador visual (LED) para alertar cuando el depósito de agua general esté vacío o bajo. | 🟢 |
| 5.2 | El sistema contará con indicadores de estado de conexión Bluetooth (conectando, conectado, error). | 🟡 |
| 5.3 | Uso de Dip Switches, botones, buzzer y Flash interna del microcontrolador. | 🟡 |

### **6. Comunicación Bluetooth (Módulo HM-10)**
| Req ID | Descripción | Estado |
| :--- | :--- | :---: |
| 6.1 | El sistema se conectará mediante Bluetooth para interactuar con la aplicación. | 🟡 |
| 6.2 | El sistema enviará periódicamente los datos de temperatura, humedad ambiente y humedad del suelo a la base de datos. | 🟡 |
| 6.3 | El sistema deberá recibir comandos manuales (forzar riego, encender luces, modificar umbrales) desde la aplicación. | 🔴 |

### **7. Aplicación**
| Req ID | Descripción | Estado |
| :--- | :--- | :---: |
| 7.1 | La aplicación mostrará un panel de control con los valores actuales de los sensores. | 🟡 |
| 7.2 | La aplicación deberá permitirle al usuario ajustar los umbrales de humedad de suelo que disparan el riego. | 🔴 |

### **8. Requisitos de Software**
| Req ID | Descripción | Estado |
| :--- | :--- | :---: |
| 8.1 | Arquitectura Bare Metal, modular (Escrutar / Procesar / Actuar) y patrón Super-Loop. | 🟢 |
| 8.2 | Máquina de Estados Finos (FSM) y temporización por SysTick no bloqueante. | 🟡 |
| 8.3 | Gestión de modos de operación (NORMAL, SET_UP, FALLA) e implementación de bajo consumo. | 🟡 |
| 8.4 | Control de potencia por PWM y protocolo UART para Bluetooth. | 🟡 |
