# ☕ Java Installation and "Hello, World!" Program

This guide covers installing the necessary Java Development Kit (JDK) and creating, compiling, and running your first basic Java program.

---

## 1. Installing the Java Development Kit (JDK)

The **JDK** is required to write, compile, and run Java applications. We will focus on installing a common version from a major vendor.

### A. Download the JDK

1.  **Visit the official download page:** Go to the Oracle Java SE Downloads page or an alternative vendor like OpenJDK.
2.  **Select the latest LTS (Long-Term Support) version:** For beginners, an LTS version (e.g., Java 17 or Java 21) is recommended for stability.
3.  **Choose your operating system:** Select the installer appropriate for **Windows**, **macOS**, or **Linux**.
4.  **Download the installer:** Download the appropriate installer file (e.g., `.exe` for Windows, `.dmg` for macOS, or `.deb`/`.rpm` for Linux).

### B. Run the Installation

1.  **Windows/macOS:** Double-click the downloaded file and follow the on-screen instructions. The installation typically places the JDK in a default location.
2.  **Linux:** Use the appropriate package manager commands (e.g., `sudo apt install openjdk-17-jdk` for Debian/Ubuntu) or run the downloaded installer.

### C. Verify the Installation and Path

After installation, you need to ensure the `java` and `javac` commands are accessible from your terminal/command prompt.

1.  **Open your terminal/command prompt.**
2.  **Check the Java Runtime Environment (JRE) version:**
    ```bash
    java -version
    ```
3.  **Check the Java Compiler (Javac) version:**
    ```bash
    javac -version
    ```
    If both commands return a version number (e.g., `javac 17.0.9`), the installation is successful. If you get an error like "command not found," you may need to **set the JAVA\_HOME environment variable** and add the JDK's `bin` directory to your system's **PATH** variable. (The installer often handles this, but manual setup is sometimes required).

---

## 2. Writing Your First "Hello, World!" Program

We will use a simple text editor (like VS Code, Sublime Text, Notepad++, or even Notepad) and the command line to create, compile, and run the program.

### A. Create the Java Source File

1.  **Choose a directory** for your Java files (e.g., `C:\JavaProjects` or `~/JavaProjects`).
2.  **Open your text editor** and type the following code **exactly**:

    ```java
    public class HelloWorld {
        public static void main(String[] args) {
            // Print the string "Hello, World!" to the console
            System.out.println("Hello, World!");
        }
    }
    ```

3.  **Save the file** in your chosen directory with the name **`HelloWorld.java`**.
    * **Crucial Rule:** In Java, the filename **must** exactly match the class name (`HelloWorld`), and the extension **must** be `.java`.

### B. Compile the Source Code

Compilation translates the human-readable `.java` source code into machine-executable bytecode stored in a `.class` file.

1.  **Open your terminal/command prompt.**
2.  **Navigate to the directory** where you saved `HelloWorld.java` using the `cd` (change directory) command:
    ```bash
    cd <path/to/your/JavaProjects>
    ```
3.  **Compile the file** using the `javac` compiler:
    ```bash
    javac HelloWorld.java
    ```
    * If successful, this command will generate a new file named **`HelloWorld.class`** in the same directory. If there are errors, `javac` will display them.

### C. Run the Program

The **Java Virtual Machine (JVM)** executes the compiled bytecode (`.class` file).

1.  **Run the compiled program** using the `java` command:
    ```bash
    java HelloWorld
    ```
    * **Note:** You run the class name (`HelloWorld`), **not** the file name (`HelloWorld.class`).

2.  **Output:** You should see the following text displayed in your console:

    ```
    Hello, World!
    ```

Congratulations! You have successfully installed Java and executed your first program.

---

## 💡 Summary of Steps

| Step | Command/Action | Purpose | Output |
| :--- | :--- | :--- | :--- |
| **1. Install** | Download and Run JDK Installer | Provides the compiler (`javac`) and runtime (`java`) | Access to Java tools |
| **2. Create** | Save the code as `HelloWorld.java` | Creates the source code file | `HelloWorld.java` file |
| **3. Compile** | `javac HelloWorld.java` | Translates source code to bytecode | `HelloWorld.class` file |
| **4. Run** | `java HelloWorld` | Executes the bytecode on the JVM | The text "Hello, World!" |
