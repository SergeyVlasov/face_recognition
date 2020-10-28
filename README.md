# face_recognition



# Face-Mask-Detection
Detecting face masks using Python, Keras, OpenCV on real video streams

RU version

1) создаем виртуальное кружение

- python3 -m virtualenv /path/MyEnv

2) активируем виртуальное окружение

- source /path/MyEnv/bin/activate


3) устанавливаем все необходимые библиотеки

- pip3 install dlib
- pip3 install face_recognition
- pip3 install imutils


4) моздаем директорию для проекта

- mkdir face_recognition
- cd face_recognition

5) создаем папку для обучающей выборки а в ней подпапки с соответствующей персоной, и наполняем их соответствующими фото

- mkdir dataset
- cd dataset
- mkdir person1
- mkdir person2
....

6) копируем github

- git clone https://github.com/SergeyVlasov/face_recognition

7) загружаем файл 
- wget https://raw.githubusercontent.com/opencv/opencv/master/data/haarcascades/haarcascade_frontalface_default.xml


8) подготавливаем датасет

- python3 data_encoding.py --dataset dataset --encodings encodings.pickle --detection-method hog


9) запускаем распознавание лиц

- python3 video_recognition.py --cascade haarcascade_frontalface_default.xml --encodings encodings.pickle


