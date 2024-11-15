# 🚀 Big Data Ecosystem: Hadoop, Hive, and Spark on Docker  

![Big Data Ecosystem](https://via.placeholder.com/800x200?text=Big+Data+Ecosystem+on+Docker)  
*A scalable, modular Big Data ecosystem deployed using Docker, featuring Hadoop, Hive, and Spark.*

## 📖 Overview  

This project provides a fully containerized environment for experimenting with Hadoop, Hive, and Spark. It's designed to help developers and data enthusiasts build, test, and deploy Big Data workflows quickly and efficiently.

## 🎯 Features  

- **Hadoop**: Distributed storage and processing.  
- **Hive**: Data warehousing and SQL-like querying.  
- **Spark**: Fast in-memory processing for real-time and batch tasks.  
- **Dockerized Deployment**: Easily set up and tear down environments.  
- **Scalable Architecture**: Supports multiple nodes and services.  

## 🛠️ Architecture  

![Architecture Diagram](https://via.placeholder.com/800x400?text=Architecture+Diagram)  
*Example architecture showing how Hadoop, Hive, and Spark interact. (Yet to be created)*

## 📦 Setup and Installation  

### Prerequisites  
- **Docker**: [Install Docker](https://www.docker.com/get-started)

### Steps  

1. **Clone the Repository**:  
   ```bash
   git clone https://github.com/RahulRajput1999/IceCube.git
   cd your-repo-name
   ```

3. **Building local images of containers (You will need make installed)**:
  ```bash
  make
  ```
2. **Start the Environment**:  
   ```bash
   docker-compose up -d
   ```

3. **Verify the Setup**:  
   - Hadoop Web UI: `http://localhost:9870`  
   - Spark UI: `http://localhost:8080`  
   - Hive Interface: `http://localhost:10000`  

4. **Access the Containers**:  
   ```bash
   docker exec -it namenode bash
   docker exec -it spark-master bash
   docker exec -it hive-server bash
   ```

## 📝 Usage  

### Running a Hive Query  
1. Access the Hive server:  
   ```bash
   docker exec -it hive-server bash
   ```
2. Launch the Hiveserver2:  
   ```bash
   hiveserver2
   ```
3. Launch the beeline interface
  ```bash
  beeline
  ```
3. Execute your query:  
   ```sql
   SELECT * FROM your_table LIMIT 10;
   ```

### Running a Spark Job  
1. Access the Spark master:  
   ```bash
   docker exec -it spark-master bash
   ```
2. Submit your Spark job:  
   ```bash
   spark-submit --class <main_class> <your_application>.jar
   ```

## 🌟 Key Benefits  

- **Simplified Development**: No need for manual setup of Hadoop, Hive, or Spark.  
- **Modular Design**: Replace or upgrade individual components easily.  
- **Quick Prototyping**: Focus on your workflows instead of managing infrastructure.  

## 🐛 Troubleshooting  

| Issue                         | Solution                                                                 |
|-------------------------------|--------------------------------------------------------------------------|
| Containers not starting       | Ensure Docker and Docker Compose are installed and running.             |
| Unable to access Web UIs      | Check port bindings in the `docker-compose.yml` file.                   |
| Hive queries failing          | Verify that Hive Metastore is properly configured and accessible.       |

## 🙌 Contributions  

Contributions are welcome! Please fork the repository and submit a pull request.  


## 💬 Contact  

For questions or support, reach out to:    
- **GitHub**: [Rahul Sindhav](https://github.com/RahulRajput1999)  