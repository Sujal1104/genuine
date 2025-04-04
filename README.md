# 🚀 Hybrid Automation Framework Setup (Web & Mobile Automation)

## 📌 Prerequisites

Before setting up and running the project, ensure you have the following installed on your machine:

### 1️⃣ IDE
- **Eclipse** or **IntelliJ IDEA** for writing and executing tests.

### 2️⃣ Java (17 or above)
- Install Java 17 or later.
- Verify the installation by running:
  ```sh
  java -version
  ```

### 3️⃣ Maven
- Install Maven by following the official guide: [Maven Installation Guide](https://maven.apache.org/install.html)
- Verify the installation by running:
  ```sh
  mvn -version
  ```

### ⚠️ Setting Up Environment Variables (Windows)
If Java and Maven are not installed, install them and set up the **Environment Variables** correctly.
This applies to both **System Variables** and **User Variables**.

![Environment Variables Setup](https://github.com/user-attachments/assets/bc81b44e-2f4a-432d-8e03-53d988279d5b)

---

## 🏃 Running Tests via Maven

### 🔹 Before Execution
1. Open the `pom.xml` file.
2. Uncomment the **SuiteXML** file you wish to execute and comment out the others.
3. Open the terminal and run:
   ```sh
   mvn clean
   ```
4. After the clean command executes successfully, run:
   ```sh
   mvn integration-test
   ```
5. The specified test suite in `pom.xml` will execute successfully.

---

## 🏃 Running Tests via TestNG
1. Right-click on the project folder.
2. Select **Run As** → **TestNG Suite**.

![Run TestNG Suite](https://github.com/user-attachments/assets/0436cd15-424c-45a5-ab96-b48efc85a49d)

---

## 📂 Project Structure

### 🌐 Web Automation

| Component | Description |
|-----------|-------------|
| **Page Objects** | Located in `com.locators` |
| **Test Classes** | Located in `com.genuine` |
| **Configuration & Driver Setup** | Located in `com.begenuin.utils` |
| **SuiteXML Files** | Located in the `build` folder |
| **Driver Source Files** | Mac/Windows drivers in the `drivers` folder |

### 📱 Mobile Automation (Windows)

#### 🔹 Prerequisites
To set up and run mobile automation, ensure you have the following installed:
- **Appium** (Server) - For executing mobile tests and viewing logs.
- **Android Studio** - Required for running and managing virtual and physical Android devices.
- **ADB (Android Debug Bridge)** - To check if devices are connected.
- **Node.js & npm** - Required for installing Appium.
- **Appium Inspector** - To inspect UI elements of mobile applications.
- **APK File** - Example: `Genuin_SDK_1.1.13_42.apk`

#### 🔹 Setup Steps
1. Install **Appium** by following the [Appium Installation Guide](https://github.com/appium/appium).
2. Set up **Android Studio** and configure SDK & AVD Manager.
3. Install **ADB** and verify the installation by running:
   ```sh
   adb devices
   ```
   This command lists connected devices.
4. Install **Appium Inspector** to inspect UI elements.
5. Configure **Environment Variables** for Appium, ADB, and Node.js.

![Mobile Automation Setup](https://github.com/user-attachments/assets/799a633c-fadf-4d3c-89b0-47aabf2ec7af)

#### 🔹 Running Mobile Automation Tests
1. Connect your Android device and verify its connection using:
   ```sh
   adb devices
   ```
2. Start the **Appium Server** by running:
   ```sh
   appium
   ```
3. Open **IntelliJ IDEA** and execute the following Maven commands:
   ```sh
   mvn clean
   mvn test
   mvn integration-test
   ```
4. Use **Appium Inspector** to verify the app is running correctly.
5. If using **Appium Server GUI**, configure the Java and Android paths, then start the server.
6. Ensure no other Appium servers are running before execution.

> **Note:** If you want to view logs, use the **Appium Server GUI**. Set up the Java and Android SDK paths, then start the server. You can access the configuration by clicking **Edit Configuration** in the Appium GUI.

![Appium Server Configuration](https://github.com/user-attachments/assets/c65fef61-5b2a-4c0e-beed-16cf55efdf3e)

---

### ✅ This README covers both `web_Automation` and `mobile_Automation` folders.

🚀 **Happy Testing!** 🎯
