
# Kafka Installation Guide

Follow these steps to install and use Apache Kafka on your local system:

## **Installation Steps**
1. **Download Kafka:**
   - Visit the official [Kafka Downloads](https://kafka.apache.org/downloads) page.
   - Download the latest Kafka ZIP file.

2. **Extract the ZIP file:**
   - Unzip the file into your desired directory (e.g., `C:\kafka`).

3. **Start Zookeeper:**
   ```bash
   bin\windows\zookeeper-server-start.bat config\zookeeper.properties
   ```

4. **Start Kafka Server:**
   ```bash
   bin\windows\kafka-server-start.bat config\server.properties
   ```

## **Kafka Console Commands**

### **Create a New Topic**
```bash
bin\windows\kafka-topics.bat --create --topic demo-topic --bootstrap-server localhost:9092
```

### **Start Kafka Console Producer**
```bash
bin\windows\kafka-console-producer.bat --topic demo-topic --bootstrap-server localhost:9092
```

### **Start Kafka Console Consumer**
```bash
bin\windows\kafka-console-consumer.bat --topic demo-topic --from-beginning --bootstrap-server localhost:9092
```

## **Additional Notes**
- Ensure `JAVA_HOME` is correctly set in your system's environment variables.
- Start Zookeeper before starting the Kafka server.
- Check the [Kafka Documentation](https://kafka.apache.org/documentation/) for more details.
