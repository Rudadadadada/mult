**Рудаков Н. А.**
**М8О-401Б-21**

**Для задачи классификации был выбран встроенный датасет:** 
`from sklearn.datasets import load_breast_cancer`. 

Этот набор данных используется для задач классификации и включает информацию о опухолях груди. Задача состоит в определении, является ли опухоль злокачественной или доброкачественной на основе набора характеристик:

- Количество наблюдений: 569 экземпляров.
- Количество признаков: 30 числовых признаков, описывающих различные характеристики ядер клеток, такие как размер, симметрия и текстура.
- Классы: два класса — злокачественные (malignant) и доброкачественные (benign).

Метрика оценки качества классификации: **F1**. Метрика выбрана потому что балансирует метрики **precision** и **recall**. 

**Для задачи регрессии был выбран встроенный датасет:**
 `from sklearn.datasets import fetch_california_housing`.

Этот набор данных используется для задач регрессии. Он содержит информацию о ценах на жилье в Калифорнии по данным переписи населения 1990 года. Задача состоит в прогнозировании медианной стоимости жилья в разных районах.

- Количество наблюдений: 20,640 экземпляров.
- Количество признаков: 8 числовых признаков, включая средний доход в домохозяйстве, средний возраст дома и среднее количество комнат.
- Целевой признак: Медианная стоимость дома в каждой области.

Метрика оценки качества регрессии: **R^2**. Данная метрика выбрана, поскольку хорошо подходит для сравнения моделей с одинаковыми данными.

*Метрики качества на тестовом наборе данных:*
<table>
    <tr>
        <th rowspan="1">Алгоритм</th>
        <th>Задача</th>
        <th>Бейзлайн</th>
        <th>Улучшенный бейзлайн</th>
        <th>Самостоятельная имплементация алгоритма</th>
        <th>Улучшенная самостоятельная имплементация алгоритма</th>
    </tr>
    <tr>
        <td rowspan="2">KNN</td>
        <td>классификация</td>
        <td>0.9444444444444444</td>
        <td>0.9718309859154933</td>
        <td>0.9577464788732394</td>
        <td>0.9577464788732394</td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>0.6438795499720962</td>
        <td>0.7080936452318685</td>
        <td>0.1075958511657286</td>
        <td>0.6438795499720962</td>
    </tr>
    <tr>
        <td rowspan="2">Линейные модели</td>
        <td>классификация</td>
        <td>0.9655172413793104</td>
        <td>0.9930069930069933</td>
        <td>0.9558823529411765</td>
        <td>0.9558823529411765</td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>0.5757877060324512</td>
        <td>0.6456819729261881</td>
        <td>0.5670509282565295</td>
        <td>0.5671692517174186</td>
    </tr>
    <tr>
        <td rowspan="2">Решающее дерево</td>
        <td>классификация</td>
        <td>0.9577464788732394</td>
        <td>0.9577464788732394</td>
        <td>0.9436619718309859</td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>0.6186740579561492</td>
        <td>0.6883380738855668</td>
        <td>0.6763337730343438</td>
    </tr>
    <tr>
        <td rowspan="2">Случайный лес</td>
        <td>классификация</td>
        <td>0.9722222222222222</td>
        <td>0.9722222222222222</td>
        <td>0.9577464788732394</td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>0.8047359842513278</td>
        <td>0.8046162363031335</td>
        <td>0.7694569147407242</td>
    </tr>
    <tr>
        <td rowspan="2">Градиентный бустинг</td>
        <td>классификация</td>
        <td>0.965034965034965</td>
        <td>0.965034965034965</td>
        <td>0.965034965034965</td>
    </tr>
    <tr>
        <td>регрессия</td>
        <td>0.7756446042829697</td>
        <td>0.8291520436187658</td>
        <td>0.7756924075023037</td>
    </tr>
</table>

<br><br>
**Вывод:** 
- лучшая модель для решения задачи классификации - улучшенная **линейная модель** из библиотеки.
- лучшая модель для решения задачи регрессии - улучшенная модель **градиентного бустинга** из библиотеки.
<br>