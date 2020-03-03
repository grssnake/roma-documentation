1 aplay /usr/share/sounds/alsa/*
1 sudo apt-get install espeak python-espeak
1 sudo apt-get install espeak-ng
1 echo "export PA_ALSA_PLUGHW=1" >> ~/.bashrc
1 source ~/.bashrc
1 espeak -ven-us "Hello my name is roma" 2>/dev/null
1 espeak -vru "Привет меня зовут рома" 2>/dev/null
1 cat test.txt | espeak -vru 2>/dev/null
