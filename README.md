# Инструмент для анализа клиентских отзывов

## Описание
*Проектная работа по программе "Сириус.ИИ" от Тинькофф.*

![](https://cdn.discordapp.com/attachments/1191641717733085225/1223596656243511396/-1_2.png?ex=661a6e30&is=6607f930&hm=ffd5fc67bd1259e9404dd9c61b6483481625b676f0b91330af14722202a0abd8&)

Этот инструмент предназначен для анализа отзывов клиентов из открытых источников. Он использует различные методы обработки естественного языка и машинного обучения для классификации отзывов по их эмоциональной окраске и выявления ключевых тем.

Сотрудники Тинькофф могут использовать этот инструмент для получения ценной обратной связи от клиентов и выявления областей для улучшения. Это может помочь улучшить клиентский опыт и увеличить уровень удовлетворенности клиентов.
## Функциональность
- Сбор отзывов с открытых источников.
- Предварительная обработка текста отзывов, включая удаление стоп-слов, приведение текста к нижнему регистру, удаление пунктуации.
- Применение модели машинного обучения для определения эмоциональной окраски отзывов.
- Выявление ключевых тем в отзывах.

## Библиотеки
В коде используются библиотеки:
- pandas
- requests
- BeautifulSoup из bs4
- json
- html
- re
- time
- random
- csv
- nltk
- stopwords из nltk.corpus
- WordNetLemmatizer из nltk.stem
- string
- TfidfVectorizer из sklearn.feature_extraction.text
- numpy
- matplotlib.pyplot
- LatentDirichletAllocation из sklearn.decomposition
- Counter из collections
- IsolationForest из sklearn.ensemble
- LogisticRegression из sklearn.linear_model
- train_test_split из sklearn.model_selection
- classification_report из sklearn.metrics
- drive из google.colab
- pymorphy2
- sys
- re
- vstack из scipy.sparse
## Установка
Для установки всех необходимых библиотек выполните следующую команду:
```python
pip install pandas requests bs4 json html re time random csv nltk string sklearn numpy matplotlib google.colab pymorphy2 sys scipy
```
Также вам потребуется датасет [ru_sentiment_dataset](https://huggingface.co/datasets/MonoHime/ru_sentiment_dataset/blob/main/datasets.csv) для работы модели. Вы можете скачать его здесь.
## Описание файлов 
*Customer_Review_Analysis_Tool.ipynb* - это сам jupyter-ноутбук, который содержит код. Для его открытия вы можете скачать и установить [*Jupiter*](https://jupyter.org/) на ваш компьютер или загрузить его в [*Google Colab*](https://colab.google/), который позволяет работать с Jupyter-ноутбуками прямо в вашем браузере<br>
*reviews.csv* - это файл, который содержит отзывы с сайта [*banki.ru*](https://www.banki.ru/services/responses/bank/tcs/?type=al).<br>
*processed_reviews.csv* - это обработанный *reviews.csv*. У него удалины стоп-слова, весь текст преобразованн в нижний регистр, удалена пунктуация, и пропущены все заголовки.<br>
*processed_reviews_with_sentiments.csv* — это файл, прошедший через модель, которая определеяет эмоциональную окраску отзыва. Ему добавился 1 столбец "*sentiments*", в котором цифры от 0 до 2. Где:<br>
0 - Нейтральный отзыв. <br>
1 - Положительный отзыв. <br>
2 - Негативный отзыв.

