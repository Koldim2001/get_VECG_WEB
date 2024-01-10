# Веб-версия проекта по ВЭКГ

Векторная электрокардиография (ВЭКГ) - это метод, позволяющий измерять и представлять электрический вектор сердца во время сердечного цикла. Этот вектор представляет собой направление дипольного момента сердца, что дает информацию о сокращении сердечной мышцы. Врачи используют ВЭКГ для анализа движения вектора в трех основных плоскостях и его 3D отображения для диагностики и мониторинга состояния сердца. Такая информация может быть полезной для обнаружения аномалий, нарушений проводимости и оценки эффективности лечения. Векторная электрокардиография является важным инструментом в кардиологии и помогает улучшить диагностику и лечение сердечно-сосудистых заболеваний.

Данное приложение основано на его GUI версии - [get_VECG_GUI](https://github.com/Koldim2001/get_VECG_GUI)

Код позвляет получать проекции и 3D представление ВЭКГ из исходных ЭКГ сигналов формата EDF, реализовывать систему поддержкии принятия решений (болен/здоров) на основе векторных петель, а так же определять информативные параметры данных петель.

PS: ДЛЯ ТЕСТИРОВАНИЯ РВБОТЫ ПРИЛОЖЕНИЯ МОЖНО ИСПОЛЬЗОВАТЬ EDF ФАЙЛЫ В ПАПКЕ - Data_for_testing

### Видео туториалы: 
>  [__Презентация работы веб-приложения__]()


---
<br>

## __УСТАНОВКА:__

### __Используя Python:__
Необходимо иметь установленный python 3.11 или более версии. \
Данные команды требуется запускать последовательно в терминале:
1. Склонируйте к себе этот репозиторий 
```
git clone https://github.com/Koldim2001/get_VECG_web.git
```
2. Перейдите с помощью команды cd в созданную папку get_VECG_web
```
cd get_VECG_web
```
3. Загрузите все необходимые библиотеки:
```
pip install -r requirements.txt
```
4. Запустите streamlit сервер:
```
streamlit run main.py
```
Для запуска веб-приложения надо перейти по адресу http://localhost:8501

---
<br>

### __Используя Docker:__
1. Команда загружает образ Docker с именем koldim2001/get_vecg_web и тегом 1.0_dev из Docker Hub на вашу локальную машину. Этот образ содержит всю необходимую конфигурацию и зависимости для запуска приложения:
```
docker pull koldim2001/get_vecg_web:1.0_dev
```

2. Команда  запускает контейнер из загруженного образа. Флаг -p 8501:8501 связывает порт 8501 контейнера с портом 8501 хоста, что позволяет внешним пользователям обращаться к приложению:
```
docker run -p 8501:8501 koldim2001/get_vecg_web:1.0_dev
```


Для запуска веб-приложения надо перейти по адресу http://localhost:8501
