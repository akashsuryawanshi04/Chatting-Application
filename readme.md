# Chatting Application (Java Swing)

&#x20;

> A lightweight client-server chat application built with **Java Swing** and **sockets**. Clean, polished UI with rounded chat bubbles, Enter-to-send support, empty-message protection, grouping/spacing for messages, and a scrollable chat area.

---

## 🎯 Overview

This project demonstrates a simple 1:1 real-time chat using plain Java sockets and a Swing-based UI. It’s a great learning project for socket programming, Swing layouts, and simple UI polish (rounded chat bubbles, grouped messages, scrollable message area).

---

## ✨ Features

- Java Swing GUI for Server and Client
- Real-time messaging over TCP sockets
- Prevents sending empty messages


---

## 🛠️ Tech Stack

- Java (JDK 8+)
- Java Swing (javax.swing)
- Sockets: `ServerSocket`, `Socket`, `DataInputStream`, `DataOutputStream`

---

## 📁 Project structure (suggested)

```
chatting-application/
├── src/
│   └── chatting/
│       └── application/
│           ├── Server.java
│           └── Client.java
├── icons/                # images loaded via ClassLoader.getSystemResource("icons/3.jpg")
│   └── 3.jpg             # All required icons
├── README.md
└── .gitignore
```

> If your `Server.java`/`Client.java` file is not under `src/chatting/application/` but has the same package declaration, adjust paths accordingly.

---

## 🚀 Run locally — command line (quick)

1. Unzip the project and open a terminal in the project root.

2. Compile Java sources (example assumes sources are under `src/` and package `chatting.application`):

```bash
javac -d out src/chatting/application/*.java
```

3. Make sure your `icons/` folder is available on the classpath. A quick way is to copy `icons/` into the `out/` directory after compilation:

```bash
cp -r icons out/
```

4. Run the **Server** in one terminal window:

```bash
java -cp out chatting.application.Server
```

5. Run the **Client** in another terminal window:

```bash
java -cp out chatting.application.Client
```

---

## 🧰 Run in IDE (recommended for development)

- Import the folder as a Java project (IntelliJ IDEA / Eclipse / NetBeans).
- Make sure JDK is configured for the project/module.
- Mark `src/` as source root if needed.
- Ensure `icons/` is set as a resources folder (or copied to the output folder by the IDE).
- Run `Server.main()` and `Client.main()` from run configurations.

---

## ✅ Best-practice `.gitignore` (copy to a `.gitignore` file)

```gitignore
# Java
*.class
*.jar
*.war
*.ear

# Packages
target/
build/
out/

# IDEs
.idea/
*.iml
.vscode/

# Logs
*.log

# Others
.DS_Store
Thumbs.db

# Optional: exclude local config files
local.properties
```

---

## 📦 How to create a distributable JAR (optional)

1. After compiling to `out/` you can create a jar (simple, without manifest main-class):

```bash
cd out
jar cvf chatting-app.jar .
```

2. To run (you need to specify the main class manually):

```bash
java -cp chatting-app.jar chatting.application.Server
```

(For a proper executable jar with `Main-Class` in `MANIFEST.MF`, create the manifest file and build with `jar cfm ...`.)

---

## 📸 Screenshots

Add screenshot files into an `assets/` or `docs/` folder and reference them in this README like:

```md
![Server UI](assets/server-ui.png)
![Client UI](assets/client-ui.png)
```

---

## 🧩 Troubleshooting

- **Port already in use**: If `java.net.BindException: Address already in use: JVM_Bind` appears, change the port number (currently `6060`) in `Server.java` and `Client.java` or kill the process using the port.
- **icons not found**: Ensure the `icons/` folder is on the runtime classpath (copy to `out/` or configure your IDE to include it as resources).
- **Cannot connect client to server**: Confirm server is running and using the correct IP (127.0.0.1 for local machine) and port (6060).

---

## 📋 Contributing

1. Fork the repo
2. Create a feature branch: `git checkout -b feature/awesome-feature`
3. Commit your changes: `git commit -m "Add some feature"`
4. Push: `git push origin feature/awesome-feature`
5. Open a pull request


---

## 📜 License

This project is open-source. Choose a license that fits you — I recommend the MIT license for simple projects. Example (place in `LICENSE` file):

```
MIT License

Copyright (c) YEAR Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
... (standard MIT text)
```

---

## 👨‍💻 Author

**Akash Suryawanshi**  
📧 [akashsuryawanshi1344@gmail.com](mailto:akashsuryawanshi1344@gmail.com)  
💼 [LinkedIn Profile](https://linkedin.com/in/akashsuryawanshi04)  
🌐 [GitHub Profile](https://github.com/akashsuryawanshi04)

---

⭐ If you like this project, don't forget to **star the repo** on GitHub!


