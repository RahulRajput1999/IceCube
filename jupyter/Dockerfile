# Use an official Python runtime as a parent image
FROM python:3.8


RUN apt update

RUN apt install default-jdk scala git -y

RUN wget https://dlcdn.apache.org/spark/spark-3.5.3/spark-3.5.3-bin-hadoop3.tgz

RUN tar xvf spark-*.tgz

RUN mv spark-3.5.3-bin-hadoop3 /opt/spark

ENV SPARK_HOME=/opt/spark

RUN echo "export PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin" >> ~/.bashrc

ENV PYSPARK_PYTHON=/usr/bin/python3
# Set the working directory to /app
WORKDIR /app

# Install Jupyter Notebook
RUN pip install jupyter

# Make port 8888 available to the world outside this container
EXPOSE 8888

# Define environment variable
ENV NAME World

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Run Jupyter Notebook when the container launches
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]