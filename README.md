# Решение транспортной задачи 

### Теоретические основы

Транспортная задача (задача Монжа — Канторовича) — математическая задача линейного
программирования специального вида. Её можно рассматривать как задачу об оптимальном
плане перевозок грузов из пунктов отправления в пункты потребления, с минимальными
затратами на перевозки.
Транспортная задача по теории сложности вычислений входит в класс сложности P. Когда
суммарный объём предложений (грузов, имеющихся в пунктах отправления) не равен
общему объёму спроса на товары (грузы), запрашиваемые пунктами потребления,
транспортная задача называется несбалансированной (открытой).
Для классической транспортной задачи выделяют два типа задач: критерий стоимости
(достижение минимума затрат на перевозку) или расстояний и критерий времени
(затрачивается минимум времени на перевозку). Под названием транспортная задача,
определяется широкий круг задач с единой математической моделью, эти задачи относятся
к задачам линейного программирования и могут быть решены оптимальным методом.
Однако, спец.метод решения транспортной задачи позволяет существенно упростить её
решение, поскольку транспортная задача разрабатывалась для минимизации стоимости
перевозок.

**Цель работы**: ознакомиться с методами решения транспортной задачи с использованием
библиотеки pot.

**Задание**: разработать приложение позволяющее решить транспортную задачу с
использованием исходного набора данных в виде csv файлов. Последовательность
выполнения действий:
1) Осуществить чтение данных из двух csv файлов:
a. New_york_hotels.csv – данные о местоположениях отелей (рассматривать как
пункт назначения)
b. US_accidents_dec20.csv – данные о местоположении аварий (рассматривать
как местоположения автомобилей такси)
2) Сформировать выборки:
a. Из датафрейма местоположений отелей сформировать датафрейм,
содержащий широту и долготу
b. Из датафрейма местоположений автомобилей сформировать датафрейм,
состоящий из значения широты и долготы в городе Нью-Йорк
c. Сбалансировать размерности выборок
3) Вывести график местоположений пунктов назначения и расположений машин такси
(разными цветами в одной координатной плоскости).
4) Рассчитайте расстояние между точками из двух сформированных ранее
датафреймов (функция dist из библиотеки POT: Python Optimal Transport),
отобразите матрицу расстояний на графике.
5) Найдите матрицу оптимальных перемещений (функция emd из библиотеки POT:
Python Optimal Transport), отобразите ее на графике.
6) Исходя из полученных данных местоположений отелей и машин отобразите
оптимальные расстояния (исходные данные: данные местоположений, матрица
оптимальных перемещений).
7) Сформируйте датафрейм, содержащий данные по оптимальным местоположениям
отелей и такси (id отеля, id такси). Создайте два csv файла, которые содержат данные
о местоположениях в соответствии с оптимальными маршрутами.
(В файле с отелями Id отеля, широта долгота, в файле с такси id записи, широта,
долгота)
8) Проведите визуализацию с использованием Tableau — программного обеспечения
для интерактивной бизнес-аналитики и визуализации данных. Платформа платная,
есть триал на 14 дней.
