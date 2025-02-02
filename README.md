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
- **Database URL**: `jdbc:mysql://localhost:3306/test_db?useSSL=false`
- **User**: `jovyan`
- **Password**: `password`
- **Driver**: `com.mysql.jdbc.Driver`

### Step 5: Perform Data Operations
1. List all available tables in the `test_db` database.
2. Create a DataFrame that calculates the total spending per user.

### Step 6: Commit Your Work to GitHub
1. Install Git if it's not already installed.
   ```sh
   sudo apt-get update && sudo apt-get install -y git
   ```
2. Clone the challenge repository:
   ```sh
   git clone https://github.com/paulorangeljr/spark-challenge.git
   ```
3. Create a new branch using your name:
   ```sh
   cd spark-challenge
   git checkout -b your-name
   ```
4. Add your notebook to the repository:
   ```sh
   git add your-notebook.ipynb
   git commit -m "Added my solution"
   git push origin your-name
   ```
5. Open a pull request on GitHub to submit your solution.

Good luck! 🚀

