# Technopark-VK-ML

## Description
Участникам предоставлен набор данных, содержащий url и title веб-страниц, а также метку класса - 1, если страница относится к контенту 18+ и 0 - не относится к контенту 18+.\
\
Задача состоит в том, чтобы на основе предоставленного набора тренировочных данных построить бинарный классификатор веб-страниц.

## Evaluation
Метрика качества в данном соревновании: F1-Score. F1-Score представляет собой среднее гармоническое между точностью - Precision и полнотой - Recall. Precision - отношение числа истинно-положительных предсказаний (true positives, tp) ко всем предсказанным положительным результатам (tp + fp). Recall- отношение истинно-положительных предсказаний ко всем положительным событиям набора данных (tp + fn).\
\
Разбиение тестового набора на Public-/Private- части выполнено в пропорции 30/70%.\
\
Файл ответов должен содержать заголовок и иметь следующий вид: 
```py
ID,label 
135309,0 
135310,0 
135311,0 
135312,1 
...
```
## Dataset Description
### Описание файлов

_train.csv_ - тренировочный набор данных (поля: ID, url, title, label) \
_test.csv_ - тестовый набор данных (поля: ID, url, title) \
_baseline.ipynb_ - Jupyter-notebook с примером подготовки решения

### Поля данных

**ID** - уникальный id страницы \
**url** - доменное имя страницы \
**title** - заголовок страницы \
**label** - целевая переменная (1, если страница относится к контенту 18+, и 0 в противном случае)

# Описание файлов
_GridSearchCV..._ - поиски не увенчались успехом, не хватилдо времени \
_LogisticRegression.ipynb_ - первое применение ColumnTransformer \
_baseline.ipynb_ - baseline \
_bert10k.ipynb_ - попытка обучить bert на 10к строках, качество не обрадаволо, заняло много времени \
_bert_try.ipynb_ - тоже самое, но другие объёмы данных \
_best13.ipynb_ - лучшая архитектура, данные используются после предобработки ссылок с большим количеством фич, закоментированы все классификаторы линейный классификатор опорных векторов показал себя лучше всего \
_first_try.ipynb_ - предобработка данных URL и первая попытка предсказания чисто по URL \
_postproc.ipynb_ - постобработка с помощью ключевых слов на разных языках. **ОСТОРОЖНО МАТ** \
_tfdf.ipynb_ - tfdf \
_translator.ipynb_ - попытка для перевода всего датасета на английский, потом использовалось как переводчик
