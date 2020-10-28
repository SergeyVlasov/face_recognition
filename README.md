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

проект должен иметь следующую структуру:
.
├── dataset
│   ├── Ferdy
│   │   ├── 001.jpg
│   │   ├── 002.jpg
│   │   ├── 003.jpg
│   │   ├── 004.jpg
│   │   ├── 005.jpg
│   │   ├── 006.jpg
│   │   ├── 007.jpg
│   │   └── 008.jpeg
│   ├── Nunut
│   │   ├── 001.jpg
│   │   ├── 002.jpg
│   │   ├── 003.jpg
│   │   ├── 004.jpg
│   │   └── 005.jpg
│   └── Yanwar
│       ├── 001.jpg
│       ├── 002.jpg
│       ├── 003.jpg
│       ├── 004.jpg
│       ├── 005.jpg
│       ├── 006.jpg
│       └── 007.jpg
├── encodings.pickle
├── face-encoding.py
├── face-recognition-video.py
└── haarcascade_frontalface_default.xml


6) копируем github

- git clone https://github.com/SergeyVlasov/face_recognition

7) загружаем файл 
- wget https://raw.githubusercontent.com/opencv/opencv/master/data/haarcascades/haarcascade_frontalface_default.xml


8) подготавливаем датасет

- python3 data_encoding.py --dataset dataset --encodings encodings.pickle --detection-method hog




