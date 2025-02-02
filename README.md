# Jupyter + Spark + MySQL Challenge

## Overview
This challenge requires you to run a Docker container with Jupyter, Spark, and MySQL, then interact with the MySQL database using PySpark.

## Steps to Complete the Challenge

### Step 1: Run the Docker Container
Execute the following command to start the container:
```sh
docker run -e NB_UID=1000 -e NB_GID=100 -p 8888:8888 pjunior1/jupyter-spark-data-enginerring
```
This will start Jupyter Notebook, Spark, and MySQL inside the container.

### Step 2: Access Jupyter Notebook
Once the container is running, open Jupyter Notebook in your browser by navigating to:
```
http://localhost:8888
```
Use the token provided in the terminal to log in.

### Step 3: Start a Spark Session
Inside Jupyter Notebook, create a new notebook and start a Spark session that allows connecting to MySQL.

### Step 4: Connect to MySQL
Use PySpark to establish a connection to the MySQL database using the following details:
- **Database URL**: `jdbc:mysql://localhost:3306/test_db?useSSL=false&allowPublicKeyRetrieval=true`
- **User**: `jovyan`
- **Password**: `password`
- **Driver**: `com.mysql.jdbc.Driver`

### Step 5: Perform Data Operations
1. List all available tables in the `test_db` database.
2. Create a DataFrame that calculates the total spending per user.
3. You should write the DataFrame to the MysqlDB creating a new table called Results. Please output the results on the notebook
4. You should write the DataFrame to the local disk creating a Delta Table. (HINT: Delta is not present on the docker image, you should install it first)


### Step 6: Commit Your Work to GitHub
1. Install Git if it's not already installed.

2. Fork this repo and add your notebook and the folder files from delta writing.

