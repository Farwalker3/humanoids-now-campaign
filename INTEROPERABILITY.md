# Humanoids Now — Interoperability (the whole list)

**Principle:** interoperable *by design*. It's built on open standards and modular interfaces, not a
walled garden — so it speaks the languages the rest of the robotics, AI, hardware, and web ecosystems
already use. The list below is the **compatibility surface** (what it's designed to plug into), not a
claim that every single item is individually validated yet.

---

## 1. Brains / LLMs & AI models
- **Cloud LLMs:** OpenAI GPT, Anthropic Claude, Google Gemini, Meta Llama, Mistral, Cohere, xAI Grok,
  DeepSeek, Alibaba Qwen, Amazon Nova, Perplexity.
- **Agents:** **Raccoon AI** (agent model — coworker tasks), LangChain, LlamaIndex, AutoGPT-style agents,
  CrewAI, OpenAI Agents/Assistants, Google ADK.
- **Local / open model runtimes:** Ollama, llama.cpp, vLLM, LM Studio, Jan, GPT4All, TensorRT-LLM, MLX.
- **Robotics foundation / VLA models:** NVIDIA GR00T, Google RT-2 / RT-X / Gemini Robotics,
  Physical Intelligence π0, Hugging Face **LeRobot** policies, OpenVLA, Octo.
- **Vision:** YOLO, SAM / SAM 2, Grounding DINO, CLIP, DepthAnything, OpenCV.
- **Speech:** Whisper / faster-whisper (STT); Piper, Coqui, Kokoro, ElevenLabs (TTS); Silero VAD.
- **Any OpenAI-API-compatible endpoint** (swap providers with one base-URL change).

## 2. Protocols & interfaces (the "any web server or MCP" part)
- **MCP (Model Context Protocol)** — connect any MCP server/tool.
- **Web:** REST / HTTP, WebSocket, gRPC, GraphQL, WebRTC, Server-Sent Events, OAuth2, webhooks.
- **Messaging / IoT:** MQTT, AMQP, ZeroMQ, Redis pub/sub, Kafka.
- **Robotics middleware:** **ROS / ROS 2** (DDS), micro-ROS, Zenoh, LCM.
- **Smart home:** Matter, Thread, Home Assistant, Zigbee, Z-Wave, HomeKit, Google Home, Alexa.
- **Industrial:** OPC-UA, Modbus, EtherCAT, PROFINET.
- **Wireless:** Wi-Fi, Bluetooth / BLE, UWB, LoRa, 5G/LTE.

## 3. Hardware buses & wiring (component-level)
- USB / USB-C, UART / serial, I²C, SPI, CAN bus / CANopen, RS-485, PWM, GPIO, PoE, HDMI/DisplayPort, PCIe.

## 4. Robot software, sim & description formats
- **Middleware/stacks:** ROS 2, NVIDIA Isaac ROS / Isaac Sim / Isaac Lab, MoveIt (planning), Nav2
  (navigation), ros2_control.
- **Simulators:** **MuJoCo** (our engine), Gazebo, PyBullet, Genesis, Drake, Isaac Sim, Webots, CoppeliaSim.
- **Description / scene formats:** **URDF**, SDF, **OpenUSD**, MJCF, xacro.
- **Viz / tooling:** RViz, Foxglove, rosbag, Meshcat.

## 5. Onboard compute (brains you can drop in)
- NVIDIA Jetson (Orin Nano / NX / AGX), Raspberry Pi (4/5/CM), Intel NUC & mini-PCs, Google Coral
  (Edge TPU), Qualcomm RB5/RB3, Radxa/Rock, x86 SBCs.
- **Microcontrollers:** Arduino, ESP32, Teensy, STM32, RP2040 (Pico) — MicroPython / CircuitPython / Arduino.

## 6. Actuators / "muscles" (mix and match)
- **Smart servos:** Robotis **Dynamixel**, Feetech **STS/SCS**, HerkuleX.
- **BLDC + field-oriented controllers:** **ODrive**, mjbots **moteus**, MyActuator, CubeMars, T-Motor,
  SimpleFOC, VESC.
- **Quasi-direct-drive actuators** (the prosthetics/legged kind), harmonic-drive joints.
- **Standard hobby servos** (PWM), steppers + drivers (TMC/A4988), linear actuators, pneumatics.

## 7. Sensors (plug-and-play)
- **Cameras / depth:** Intel **RealSense**, Luxonis **OAK**, Stereolabs **ZED**, Orbbec, Arducam,
  Raspberry Pi Cam, USB UVC webcams.
- **LiDAR:** Slamtec **RPLidar**, Livox, Ouster, Hesai, Velodyne, ToF modules.
- **IMU / orientation:** Bosch **BNO085/055**, ICM-20948, MPU-6050, VectorNav.
- **Force / tactile:** load cells + HX711, FSRs, force-torque sensors, sensorized skins, capacitive touch.
- **Audio:** ReSpeaker mic arrays, USB mics, I²S MEMS mics.
- **Position:** magnetic/optical encoders (AS5600, AMT), hall sensors.

## 8. Fabrication & physical parts (3D-printed + aftermarket)
- **3D printers:** Bambu Lab, Prusa, **Voron**, Creality (Ender), **RepRap**, Ultimaker, Anycubic;
  resin: Formlabs, Elegoo, Anycubic.
- **File formats:** STL, STEP, **3MF**, OBJ, IGES, gcode.
- **CAD:** FreeCAD, Fusion 360, Onshape, Blender, SolidWorks, OpenSCAD.
- **Standard mechanical parts (aftermarket):** metric fasteners (M2/M3/M4/M5), ball bearings
  (608/6800 series), **2020 V-slot aluminum extrusion**, GT2 belts & pulleys, MGN linear rails,
  lead screws, threaded inserts, servo brackets/horns, shaft couplers, silicone/TPU.
- **Open-hardware bodies you can borrow from:** InMoov, Poppy Project, Reachy (Pollen), Open-Source Leg.

## 9. Power
- LiPo / Li-ion / 18650 packs, LiFePO4, BMS boards, buck/boost converters, USB-C PD, and standard
  connectors: XT60/XT30, JST-XH/PH, Anderson Powerpole, barrel jacks.

## 10. Prosthetics / neurobionics (the testbed angle)
- **U-M Open-Source Leg** (standardized limb hardware/software), Humotech emulators, OpenBCI / EMG
  (Myoware) inputs, standard prosthetic pyramid adapters & socket interfaces, powered knee/ankle modules.

## 11. Web, cloud & the "coworker" stack
- **MCP servers** (any), Zapier, IFTTT, n8n, Make, webhooks.
- **Work tools:** Google Workspace (Calendar/Docs/Gmail), Microsoft 365/Outlook, **Slack, Discord,
  Teams, Zoom**, Notion, Jira, Linear, Trello, Asana.
- **Cloud:** AWS, GCP, Azure, Cloudflare; databases (Postgres, SQLite) & vector DBs (pgvector, Chroma,
  Qdrant, Pinecone, Weaviate).

## 12. Other robots & platforms (talks to them)
- **Anything ROS 2** (interoperate at the middleware layer).
- **Educational/kits:** **EZ-Robot JD**, LEGO Spike/Mindstorms, VEX, Petoi.
- **Arms:** SO-ARM100 / LeRobot arm, xArm (UFactory), Universal Robots (UR), Franka, Kinova, WidowX.
- **Humanoids / legged:** Unitree (G1/H1/Go2), Booster, Fourier, Boston Dynamics Spot (SDK),
  open humanoids (InMoov, Poppy, Reachy).

## 13. Languages & SDKs
- Python, C++, Rust, JavaScript/TypeScript (Node), Go; ROS 2 (rclpy/rclcpp), Arduino/PlatformIO,
  MicroPython, CircuitPython, MATLAB/Simulink.

---

*Honesty note: this is the interoperability the open + modular + standards-based design enables. On the
public campaign we present it as "compatible by design," not "every item lab-validated."*
