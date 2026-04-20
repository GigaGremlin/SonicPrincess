# 🐾 SonicPrincess
### Mobile Ultraschall-Hundeklingel auf ESP8266-Basis

<div align="center">
  <img width="400" alt="SonicPrincess Logo" src="https://github.com/user-attachments/assets/ca15e9b7-ed4c-41c0-8a40-d04486d67c78" />
  <p><em>Damit Princess nicht mehr bellen muss, wenn sie ins Haus möchte.</em></p>
</div>

---

## 📖 Über dieses Projekt

Da unser Hund am liebsten draußen in der Sonne liegt oder im Vorgarten spielt, brauchten wir eine Lösung, <br>die es unserer **Princess** ermöglicht zu "klingeln", wenn sie wieder rein möchte. 

Früher hat sie sich einfach vor die Tür gesetzt und gebellt, bis jemand kam. <br>Heute gibt es dafür im Haus eine elegante Durchsage über **Home Assistant**. 🔊

### Warum Ultraschall?
Wir haben viel experimentiert, aber Standardlösungen waren unzuverlässig:
* ❌ **PIR-Sensoren:** Zu viele Fehlalarme durch Lichtwechsel.
* ❌ **Präsenzmelder (Tuya/Zigbee):** Hohe Latenz und zu große Reichweite (Reflektionen).
* ✅ **Ultraschall (HC-SR04):** Präzise Distanzmessung. Keine Fehlalarme mehr, und der Hund wird nicht gestört.

---

## 🛠 Hardware & Komponenten

Das Herzstück ist ein günstiges ESP8266-Board mit integriertem Akkuhalter für maximale Mobilität.

| Komponente | Beschreibung | Bild |
| :--- | :--- | :--- |
| **Controller** | ESP8266 D1 Mini WiFi + 18650 Akku-Halter | <img width="150" src="https://github.com/user-attachments/assets/d05f15a1-95be-44bf-ba53-09ab3dbc2600" /> |
| **Sensor** | HC-SR04 Ultraschall Modul | <img width="150" src="https://github.com/user-attachments/assets/411c1335-ff7d-49be-a0e3-f806a84872cc" /> |
| **Energie** | 18650 Li-Ion Akku | |

> [!TIP]
> Selbstverständlich funktioniert das auch mit einem normalen ESP8266 ohne Akku per USB-Netzteil, <br>wenn die Klingel fest an einem Ort montiert wird.

---

## 🚀 Funktionsweise

1. Der **HC-SR04** misst kontinuierlich die Distanz vor der Tür.
2. Sobald Princess einen definierten Schwellenwert (Abstand zur Tür) unterschreitet, <br>erkennt der **ESP8266** dies als "Anwesenheit".
3. Ein Signal wird per WiFi an **Home Assistant** gesendet.
4. Home Assistant löst eine Benachrichtigung oder Sprachausgabe im Haus aus.

---

## 💻 Installation & Code

Du findest die aktuelle Konfigurationsdatei direkt hier im Repository:

📂 **[Firmware / YAML (v2.5)](./firmware/SonicPrincess%20FW-Ver%202.5.yaml)**

Die Einbindung in Home Assistant erfolgt am einfachsten über **ESPHome**. Einfach die YAML anpassen <br>(WLAN-Daten & Distanz-Schwellenwert) und auf den ESP flashen.

---

## 👑 Die Namensgeberin im Einsatz (auf Strandwache)

<div align="center">
  <img width="800" alt="Princess Urlaub am Meer" src="https://github.com/user-attachments/assets/c35ac6f1-62fd-4b38-a2c6-8c0f8ea8c9fd" />
</div>

---

<div align="center">
  <p>Erstellt mit ❤️ für Princess von</p>
  <a href="https://gigagremlin.de">
    <img src="https://img.shields.io/badge/Made%20by-GigaGremlin-blue?style=for-the-badge" alt="GigaGremlin Website" />
  </a>
</div>
