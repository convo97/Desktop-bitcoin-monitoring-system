
# 📈 ESP8266 Bitcoin Price Tracker (INR Conversion)

This project uses an **ESP8266** microcontroller to fetch the **Bitcoin price in USD** from the **CoinGecko API**, converts it into INR, and serves it on a simple web dashboard via a local HTTP server.

## 🔧 Features

- Connects to WiFi and fetches real-time Bitcoin price from CoinGecko.
- Converts USD price to INR using a static exchange rate (modifiable).
- Serves a beautiful, responsive web page with:
  - Bitcoin price in INR
  - A "Refresh" button to reload the data
- Web server runs locally on the ESP8266 (Port 80).
- Auto updates price every 60 seconds or on client request.

## 📦 Tech Stack

- **ESP8266** (NodeMCU, Wemos D1 Mini, etc.)
- **Arduino IDE**
- **CoinGecko API**
- **ArduinoJson**
- **ESP8266WiFi** and **ESP8266HTTPClient** libraries

## 🚀 Getting Started

### 1. 🧰 Requirements

- ESP8266 board (NodeMCU, etc.)
- Arduino IDE with ESP8266 board support
- Libraries:
  - `ESP8266WiFi`
  - `ESP8266HTTPClient`
  - `ArduinoJson` (Install via Library Manager)

### 2. 🔌 Circuit

No external components are needed! Just power your ESP8266.

### 3. ⚙️ Setup

Update the WiFi credentials in the code:

```cpp
const char* ssid = "your_SSID";
const char* password = "your_PASSWORD";
Upload the code to your ESP8266.

Open Serial Monitor at 115200 baud to see connection status and IP address.

4. 🌐 Access the Web Interface
After uploading:

Connect your PC/Phone to the same network.

Open the ESP8266's IP address (shown in Serial Monitor) in a browser.

You’ll see a styled dashboard showing the current Bitcoin price in INR.

💡 Notes
The INR conversion is static (price = price * 81). Update this value for real-time conversion or use an exchange rate API.

CoinGecko API is public and does not require an API key.

🧪 Sample Output
Web Page Screenshot (example):

markdown
Copy
Edit
---------------------
| Bitcoin Price     |
| INR 6,254,321     |
| [Refresh]         |
---------------------
🛠 Customization
Add support for more currencies or crypto coins via CoinGecko URL params.

Use a dynamic exchange rate API for accurate INR conversion.

Display price trends or graphs using JavaScript or external APIs.
