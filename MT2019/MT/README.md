Лабораторий №2 по  Методы Трансляции 

вариант: 5 

Язык программы: Java
###Ручное построение нисходящих синтаксических анализаторов


#### Условия Задачи 
Блок описания переменных в Паскале. Блок начинается ключевым
словом “var”, далее идет несколько описаний переменных. Описание переменных содержит имена переменных через запятую, затем двоеточие,
затем имя типа. Достаточно рассматривать только примитивные типы
(массивы, записи и т. п. не требуется).
Используйте один терминал для всех имен переменных и имен типов.
Используйте один терминал для ключевого слова var (не три ‘v’, ‘a’, ‘r’).
Пример: var a, b: integer; c: integer;

#### ше 1)Разработка грамматики
Разработайте контестно-свободную грамматику для языка, описанного в условии вашего варианта. Сначала разработайте грамматику, исходя из структуры языка, чтобы она максимально близко соответствовала интуитивным представлениям о построении слов из языка. Затем,
при необходимости, устраните левую рекурсию и/или правое ветвление.
В отчете приведите исходную и преобразованную грамматику, опишите смысл всех нетерминалов

В файле 2_laba  находиться  кс грамамтика для моей задачи 


#### 2)Построение лексического анализатора
Лексический анализатор должен получать на вход строку и выдавать
последовательность терминалов (токенов). Пробелы и переводы строк
должны игнорироваться.

лексический анализ  находится в файле LexicalAnalyzer
список использованных токенов находится в файле Token

#### 3)Построение синтаксического анализатора
Постройте множества FIRST и FOLLOW для нетерминалов вашей
грамматики. Затем напишите синтаксический анализатор с использованием рекурсивного спуска.

Синтаксический анализатор: Parser
Дерево который я использую для сохранение:Tree

#### 4)Визуализация дерева разбора
Для изучения результата разработайте систему визуализации дерева
разбора.

чтобы нормально вывести результат я использую сайт http://mxwell.github.io/draw-graph/   
который выводить результат  красиво. Как я  заметил чтобы задать какой нибудь граф достаточно 
просто записать все ребра подряд в ссылке 

* example 
  1) a -> b
  2) b -> c 
  3) b -> d
  
  click: http://mxwell.github.io/draw-graph/?q=graph{a--b;b--c;b--d}#
  
  
 теперь остается только создать эту ссылку это я делаю внутри buildClick  
 
 comment: вы можете использовать graphViz
 
 ####  5) Подготовка набора тестов
 все мои тесты находиться внутри checker

