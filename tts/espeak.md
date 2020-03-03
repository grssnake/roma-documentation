aplay /usr/share/sounds/alsa/*
sudo apt-get install espeak python-espeak
sudo apt-get install espeak-ng
echo "export PA_ALSA_PLUGHW=1" >> ~/.bashrc
source ~/.bashrc
espeak -ven-us "Hello my name is roma" 2>/dev/null
espeak -vru "Привет меня зовут рома" 2>/dev/null
cat test.txt | espeak -vru 2>/dev/null
