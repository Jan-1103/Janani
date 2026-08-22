Flask Application Setup on Ubuntu EC2

Step 1: Update the System
sudo apt update

Step 2: Install Python and Required Packages
Install `pip`:
sudo apt install python3-pip -y
Install Python virtual environment support:
sudo apt update
sudo apt install python3-venv python3-full -y

Step 3: Create and Activate a Virtual Environment
Create a virtual environment:
python3 -m venv venv
Activate the virtual environment:
source venv/bin/activate


Step 4: Install Python Dependencies
Install the required Python packages:
pip install Flask PyMySQL gunicorn

Step 5: Install MySQL Client
Install the MySQL client to connect to the Amazon RDS database:
sudo apt install default-mysql-client -y
Verify the installation:
mysql --version

Step 6: Create the Flask Application
Create a file named:
text
app.py
Add your Flask application code to this file.

Step 7: Run the Flask Application
Start the application in the background:
python3 app.py &

Step 8: Verify the Application
Test the application locally:
curl localhost:5000


Expected Output

  json
{"status": "Flask is running"}
