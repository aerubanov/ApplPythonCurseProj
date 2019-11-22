# Подзадачи проета
для каждой подзадачи своя [директория]

## Предобработка изображений [preprocessing] **(Chermanteev Ramil)**
модуль, который из картинки с формулой выделяет символы и их положение
- [X] черно белое изображение
- [X] нормализация изображения
- [X] выделение символов
- [X] измение размера (привести к тому что будет подоваться на вход классификатора)
стоит посмотреть https://scikit-image.org/docs/dev/auto_examples/segmentation/plot_label.html например

## Классификатор изображений [symbol_classifier] **(Vera)**
получает картинку символа и возвращает имя (номер) символа
- [X] сделать датасет (https://github.com/ThomasLech/CROHME_extractor)
- [X] выбрать архитектуру и обучить классификатор изображений

## Парсер выражений [parser]
собирает из распознанных классификатором символов и информации об их местоположении запрос к api wolfram
- [ ] определиться с форматом представления символов (номера классов которые выдает классификатор)
- [ ] определиться с форматом представления положения символов (получает при предобработке)
- [ ] париснг выражения (на выходе строка запроса к вольфрам)

## Взаимодействие с пользователем и api wolfram [web] **(Anatoly Rubanov)** 
- [X] api нашего приложения  
- [X] взаимодействие с пользователем - получение картинки с выражением, запрос к api нашего приложения, возвращение
полученного результата (думаю телеграмм-бот подойдет хорошо для этого) 
  - [x] сервер для бота
  - [x] запросы к api wolfram
- [X] интеграция предобработки
- [ ] интеграция классификатора
