* [https://www.dexterindustries.com/howto/make-your-raspberry-pi-speak/]
* [http://espeak.sourceforge.net/commands.html]

* aplay /usr/share/sounds/alsa/*
* sudo apt-get install espeak python-espeak
* sudo apt-get install espeak-ng
* echo "export PA_ALSA_PLUGHW=1" >> ~/.bashrc
* source ~/.bashrc
* espeak -ven-us "Hello my name is roma" 2>/dev/null
* espeak -v mb-en1 "Hello my name is roma" 2>/dev/null
* espeak -vru "Привет меня зовут рома" 2>/dev/null
* cat test.txt | espeak -vru 2>/dev/null

cat test.txt | espeak -vru 2>/dev/null
cat test.txt | espeak -vru+m1 2>/dev/null
cat test.txt | espeak -vru+m2 2>/dev/null
cat test.txt | espeak -vru+m3 2>/dev/null
cat test.txt | espeak -vru+m4 2>/dev/null
cat test.txt | espeak -vru+m5 2>/dev/null
cat test.txt | espeak -vru+m6 2>/dev/null
cat test.txt | espeak -vru+m7 2>/dev/null

cat test.txt | espeak -vru+whisper 2>/dev/null
cat test.txt | espeak -vru+m7 -s120 2>/dev/null

find /usr/lib/ -name "espeak-data"
wget http://espeak.sourceforge.net/data/ru_dict-48.zip
unzip ru_dict-48.zip
sudo mv ru_dict-48 /usr/lib/arm-linux-gnueabihf/espeak-data/ru_dict


pi@RobotRoma:~/Documents/roma-documentation/tts $ sudo mkdir /usr/share/espeak-data
pi@RobotRoma:~/Documents/roma-documentation/tts $ cd /usr/share/espeak-data


