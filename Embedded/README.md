# Sensored - Embedded
There are 2 sensors on the Sensored board, these are the ICM20948 and the BME280. The ICM20948 is a compact IMU with 3 axis accelerometer, gyroscope and magnetometer. The BME is a sensitive sensor that measures temperature, pressure and humidity. The I2C lanes are pulled up to 3V3 via 10K resistors. There is also a 1V8 LDO for converting 3V3 to 1V8 as the ICM20948 requires it for its internal VDDIO pin. DO NOT EXCEED 3V3 on the 3V3, SDA and SCL pins, this device also DOES NOT HAVE reverse voltage protection as it doesnt require one. The board is designed to be soldered directly onto other boards and is not ment to be an externally mounted module. You can do this by removing the middle "Island" from the outer ring.

Here are the specifications for the ICM-20948 and BME280 sensors.

## ICM-20948
| Sensor        | Axis     | Full-Scale Range                 | Sensitivity                 
| ------------- | -------- | -------------------------------- | ----------------------------
| Accelerometer | X, Y, Z  | ±2g, ±4g, ±8g, ±16g              | 16384, 8192, 4096, 2048 LSB/g
| Gyroscope     | X, Y, Z  | ±250, ±500, ±1000, ±2000 °/s     | 131, 65.5, 32.8, 16.4 LSB/°/s
| Magnetometer  | X, Y, Z  | ±4900 µT                         | 0.15 µT/LSB

## BME280
| Sensor      | Parameter   | Measurement Range   | Resolution
| ----------- | ----------- | ------------------- | -----------
| Pressure    | Pressure    | 300 to 1100 hPa     | 0.18 Pa
| Temperature | Temperature | -40 to 85 °C        | 0.01 °C
| Humidity    | Humidity    | 0 to 100 %RH        | 0.008 %RH

---

The entire board was routed on one side with a single ground plate to reduce EMI. The inner island is 8mm x 8mm which is a very small footprint and should fit in nearly any project. The fabricated board is using a 0.8mm board thickness rather than the standard 1.6mm as this also reduces the overall 3D footprint. All of the LCSC BOM part numbers are included within the KiCAD file and can be directly converted to Gerber + drill + placement files and sent off to JLCPCB to be manufactured (JLCPCB was used as they are cheap). The cost is roughly $150 AUD for 5 fully assembled boards therefore its ~$30 / Board.

![Embedded_Capabilities](/.assets/Sensored%20Routing%20Image.png)