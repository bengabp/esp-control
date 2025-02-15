# esp-control

So sometimes I want to leave my pc at home and travel with my laptop. I might want to run ai models locally on my pc and use them anywhere from my laptop. 
I need a way to turn on my pc from my phone, because you see in my country there isnt constant electricity. Also want to do other cool things like monitor 
how frequent my pc looses power or possibly gather metrics about how much power my pc uses.

## Running this project
Make sure you have atleast python3.11 and poetry setup (as this project uses poetry for dependency management) - I recommend using python3.11

### Install dependencies
```bash
poetry update
```

### Upload the code to your esp32
Make sure your esp32 is connected to your pc and you have the necessary micropython firmware installed on it, as this project uses micropython.
From the folder having the README.md file , run this command to upload the code to your esp32. 
Your program entrypoint must be named `main.py` as esp32 runs this program after it boots up.

```bash
# Activate poetry shell
poetry shell
ampy --port <ESP_COM_PORT> put esp_control/main.py
```