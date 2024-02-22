## Запуск vosk через docker

В этом режиме модель скачается в контейнер автоматически

 ```shell
cd vosk
docker build -t vosk . docker run -p 2700:2700 vosk`
 ```

## Непосредственный запуск скрипта

1. Скачать модель в папку vosk/models по инструкции в vosk/models/readme.md
2. Запустить скрипт python

```shell
cd vosk
python vosk_server.py --model=models/vosk-model-small-ru-0.22 \
                      --host=0.0.0.0 \
                      --port=2700 \
                      --log_file=logs/vosk.log
```

 