# Commands to install Java (Latest Version) on Ubuntu

```bash
# Update the package index
sudo apt-get update

# Install Java
sudo apt install default-jdk -y

# Verify the installation
java -version
```

# Commands to Install Java 17 on Ubuntu

```bash
# Update the package index
sudo apt-get update

# Install Java 17
sudo apt install openjdk-17-jdk -y

# Verify the installation
java -version
```

# Basic Java Commands

## Compiling and Running Java Programs

```bash
# Compile a Java file
javac <filename>.java

# Run a Java program
java <filename>

# Run a Java program with classpath
java -cp <path_to_classes> <classname>
```
