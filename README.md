# deepspeech2_new

## How to Run
1. Create a VM instance (on Google Cloud Platform)
2. Clone the project
3. Download the data
4. Setup the enviroment (tensorflow v1.15)
5. Train the model

### Some basic commands are:

1. Connect to VM instance
```
gcloud compute instances start instance-name
gcloud compute ssh instance-name
```

2. Setup the virtual environment 
```
sudo apt update
sudo apt install python3-dev python3-pip
sudo pip3 install -U virtualenv  # system-wide install

virtualenv --system-site-packages -p python3 ./venv
source ./venv/bin/activate

pip install --upgrade pip
pip install --upgrade tensorflow==1.15
pip install -r requirements.txt
```

3. Train the model
```
python3 -W ignore ./train.py ./check_point/ ./json/for_newEngine/train_json.json ./json/for_newEngine/test_json.json ./log.csv
```

4. Using screen for non-stop training
```
Create: screen 
Enter: screen -r
Exit: Ctrl + A D
```
