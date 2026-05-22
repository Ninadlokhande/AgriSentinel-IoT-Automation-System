#define BLYNK_PRINT Serial
#define BLYNK_TEMPLATE_ID ""
#define BLYNK_TEMPLATE_NAME ""
#define BLYNK_AUTH_TOKEN ""

#include <WiFi.h>
#include <BlynkSimpleEsp32.h>
#include <DHT.h>

// ================= WIFI =================
char ssid[] = "";
char pass[] = "";

// ================= DHT11 =================
#define DHTPIN 2
#define DHTTYPE DHT11

DHT dht(DHTPIN, DHTTYPE);

// ================= SENSOR PINS =================
#define SOIL_SENSOR 34
#define RAIN_SENSOR 35

// =====================================================
// RELAY GPIO PINS
// =====================================================

#define RELAY1   23
#define RELAY2   25
#define RELAY3   26
#define RELAY4   27
#define RELAY5   32
#define RELAY6   33
#define RELAY7   4
#define RELAY8   13
#define RELAY9   16
#define RELAY10  18
#define RELAY11  19
#define RELAY12  21
#define RELAY13  22
#define RELAY14  5
#define RELAY15  15

// =====================================================

BlynkTimer timer;

// =====================================================
// SENSOR FUNCTION
// =====================================================

void sendSensorData() {

  // ================= DHT11 =================
  float temperature = dht.readTemperature();
  float humidity = dht.readHumidity();

  // ================= SOIL SENSOR =================
  int soilValue = analogRead(SOIL_SENSOR);

  // Convert to percentage
  int soilPercent = map(soilValue, 4095, 0, 0, 100);

  // ================= RAIN SENSOR =================
  int rainValue = analogRead(RAIN_SENSOR);

  // Convert to percentage
  int rainPercent = map(rainValue, 4095, 0, 0, 100);

  // =====================================================
  // SEND VALUES TO BLYNK GAUGES
  // =====================================================

  // V30 = Temperature
  Blynk.virtualWrite(V30, temperature);

  // V31 = Rain
  Blynk.virtualWrite(V31, rainPercent);

  // V32 = Soil Moisture
  Blynk.virtualWrite(V32, soilPercent);

  // V33 = Humidity
  Blynk.virtualWrite(V33, humidity);
}

// =====================================================
// SETUP
// =====================================================

void setup() {

  Serial.begin(115200);

  dht.begin();

  // ================= RELAY OUTPUTS =================

  pinMode(RELAY1, OUTPUT);
  pinMode(RELAY2, OUTPUT);
  pinMode(RELAY3, OUTPUT);
  pinMode(RELAY4, OUTPUT);
  pinMode(RELAY5, OUTPUT);
  pinMode(RELAY6, OUTPUT);
  pinMode(RELAY7, OUTPUT);
  pinMode(RELAY8, OUTPUT);
  pinMode(RELAY9, OUTPUT);
  pinMode(RELAY10, OUTPUT);
  pinMode(RELAY11, OUTPUT);
  pinMode(RELAY12, OUTPUT);
  pinMode(RELAY13, OUTPUT);
  pinMode(RELAY14, OUTPUT);
  pinMode(RELAY15, OUTPUT);

  // ================= ALL RELAYS OFF =================

  digitalWrite(RELAY1, LOW);
  digitalWrite(RELAY2, LOW);
  digitalWrite(RELAY3, LOW);
  digitalWrite(RELAY4, LOW);
  digitalWrite(RELAY5, LOW);
  digitalWrite(RELAY6, LOW);
  digitalWrite(RELAY7, LOW);
  digitalWrite(RELAY8, LOW);
  digitalWrite(RELAY9, LOW);
  digitalWrite(RELAY10, LOW);
  digitalWrite(RELAY11, LOW);
  digitalWrite(RELAY12, LOW);
  digitalWrite(RELAY13, LOW);
  digitalWrite(RELAY14, LOW);
  digitalWrite(RELAY15, LOW);

  // ================= BLYNK =================

  Blynk.begin(BLYNK_AUTH_TOKEN, ssid, pass);

  // ================= SENSOR UPDATE TIMER =================

  timer.setInterval(2000L, sendSensorData);
}

// =====================================================
// RELAY CONTROLS
// EVEN VPIN = BUTTON
// ODD VPIN = LED
// =====================================================

// RELAY1
BLYNK_WRITE(V0) {
  int state = param.asInt();
  digitalWrite(RELAY1, state);
  Blynk.virtualWrite(V1, state ? 255 : 0);
}

// RELAY2
BLYNK_WRITE(V2) {
  int state = param.asInt();
  digitalWrite(RELAY2, state);
  Blynk.virtualWrite(V3, state ? 255 : 0);
}

// RELAY3
BLYNK_WRITE(V4) {
  int state = param.asInt();
  digitalWrite(RELAY3, state);
  Blynk.virtualWrite(V5, state ? 255 : 0);
}

// RELAY4
BLYNK_WRITE(V6) {
  int state = param.asInt();
  digitalWrite(RELAY4, state);
  Blynk.virtualWrite(V7, state ? 255 : 0);
}

// RELAY5
BLYNK_WRITE(V8) {
  int state = param.asInt();
  digitalWrite(RELAY5, state);
  Blynk.virtualWrite(V9, state ? 255 : 0);
}

// RELAY6
BLYNK_WRITE(V10) {
  int state = param.asInt();
  digitalWrite(RELAY6, state);
  Blynk.virtualWrite(V11, state ? 255 : 0);
}

// RELAY7
BLYNK_WRITE(V12) {
  int state = param.asInt();
  digitalWrite(RELAY7, state);
  Blynk.virtualWrite(V13, state ? 255 : 0);
}

// RELAY8
BLYNK_WRITE(V14) {
  int state = param.asInt();
  digitalWrite(RELAY8, state);
  Blynk.virtualWrite(V15, state ? 255 : 0);
}

// RELAY9
BLYNK_WRITE(V16) {
  int state = param.asInt();
  digitalWrite(RELAY9, state);
  Blynk.virtualWrite(V17, state ? 255 : 0);
}

// RELAY10
BLYNK_WRITE(V18) {
  int state = param.asInt();
  digitalWrite(RELAY10, state);
  Blynk.virtualWrite(V19, state ? 255 : 0);
}

// RELAY11
BLYNK_WRITE(V20) {
  int state = param.asInt();
  digitalWrite(RELAY11, state);
  Blynk.virtualWrite(V21, state ? 255 : 0);
}

// RELAY12
BLYNK_WRITE(V22) {
  int state = param.asInt();
  digitalWrite(RELAY12, state);
  Blynk.virtualWrite(V23, state ? 255 : 0);
}

// RELAY13
BLYNK_WRITE(V24) {
  int state = param.asInt();
  digitalWrite(RELAY13, state);
  Blynk.virtualWrite(V25, state ? 255 : 0);
}

// RELAY14
BLYNK_WRITE(V26) {
  int state = param.asInt();
  digitalWrite(RELAY14, state);
  Blynk.virtualWrite(V27, state ? 255 : 0);
}

// RELAY15
BLYNK_WRITE(V28) {
  int state = param.asInt();
  digitalWrite(RELAY15, state);
  Blynk.virtualWrite(V29, state ? 255 : 0);
}

// =====================================================
// LOOP
// =====================================================

void loop() {

  Blynk.run();
  timer.run();
}
