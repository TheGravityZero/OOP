# OOP
## oop_exercise_01
Создать класс BitString для работы с 128-битовыми строками. Битовая строка должна быть представлена двумя полями типа unsigned long long. Должны быть реализованы все традиционные операции для работы с битами: and, or, xor, not. Реализовать сдвиг влево shiftLeft и сдвиг вправо shiftRight на заданное количество битов. Реализовать операцию вычисления количества единичных битов, операции сравнения по количеству единичных битов. Реализовать операцию проверки включения.  
## oop_exercise_02
Создать класс Money для работы с денежными суммами. Сумма денег должна быть представлено двумя полями: типа unsigned long long для рублей и типа unsigned char – для копеек. Дробная часть (копейки) при выводе на экран должна быть отделена от целой части запятой. Реализовать сложение сумм, вычитание, деление сумм, деление суммы на дробное число, умножение на дробное число и операции сравнения.
Операции сложения, вычитания, умножения, деления, сравнения (на равенство, больше и меньше) должны быть выполнены в виде перегрузки операторов. 
Необходимо реализовать пользовательский литерал для работы с константами типа Money.  
## oop_exercise_03
Разработать классы согласно варианту задания, классы должны наследоваться от базового класса Figure. Фигуры являются фигурами вращения. Все классы должны поддерживать набор общих методов:
1)Вычисление геометрического центра фигуры;
2)Вывод в стандартный поток вывода std::cout координат вершин фигуры; 
3)Вычисление площади фигуры.  
Создать программу, которая позволяет:
1) Вводить из стандартного ввода std::cin фигуры, согласно варианту задания.
2) Сохранять созданные фигуры в динамический массив std::vector<Figure*>.
3) Вызывать для всего массива общие функции (1-3 см. выше).Т.е. распечатывать для каждой фигуры в массиве геометрический центр, координаты вершин и площадь.
4) Необходимо уметь вычислять общую площадь фигур в массиве.
5) Удалять из массива фигуру по индексу.

## oop_exercise_04
Разработать шаблоны классов согласно варианту задания. Параметром шаблона должен являться скалярный тип данных задающий тип данных для оси координат. Классы должны иметь только публичные поля. В классах не должно быть методов, только поля. Фигуры являются фигурами вращения (равнобедренными), за исключением трапеции и прямоугольника. Для хранения координат фигур необходимо использовать шаблон  std::pair.  
Необходимо реализовать две шаблонных функции:
1) Функция print печати фигур на экран std::cout  (печататься должны координаты вершин фигур). Функция должна принимать на вход std::tuple с фигурами, согласно варианту задания (минимум по одной каждого класса).
2) Функция square вычисления суммарной площади фигур. Функция должна принимать на вход std::tuple с фигурами, согласно варианту задания (минимум по одной каждого класса).  
Создать программу, которая позволяет:
1) Создает набор фигур согласно варианту задания (как минимум по одной фигуре каждого типа с координатами типа int и координатами типа double).
2) Сохраняет фигуры в std::tuple
3) Печатает на экран содержимое std::tuple с помощью шаблонной функции print.
4) Вычисляет суммарную площадь фигур в std::tuple и выводит значение на экран.
 При реализации шаблонных функций допускается использование вспомогательных шаблонов std::enable_if, std::tuple_size, std::is_same.

## oop_exercise_05
Разработать шаблоны классов согласно варианту задания.  Параметром шаблона должен являться скалярный тип данных задающий тип данных для оси координат. Классы должны иметь публичные поля. Фигуры являются фигурами вращения, т.е. равносторонними (кроме трапеции и прямоугольника). Для хранения координат фигур необходимо использовать шаблон  std::pair.
Создать шаблон динамической коллекцию, согласно варианту задания:
1) 	Коллекция должна быть реализована с помощью умных указателей (std::shared_ptr, std::weak_ptr). Опционально использование std::unique_ptr;
2) В качестве параметра шаблона коллекция должна принимать тип данных - фигуры;
3) Реализовать forwarditerator по коллекции;
4) Коллекция должны возвращать итераторы begin() и  end();
5) Коллекция должна содержать метод вставки на позицию итератора insert(iterator);
6) Коллекция должна содержать метод удаления из позиции итератора erase(iterator);
7) При выполнении недопустимых операций (например выход за границы коллекции или удаление несуществующего элемента) необходимо генерировать исключения;
8) Итератор должен быть совместим со стандартными алгоритмами (например, std::count_if)  
Коллекция должна содержать метод доступа:  
Стек – pop, push, top; Очередь – pop, push, top;	Список, Динамический массив – доступ к элементу по оператору [];
10)	Реализовать программу, которая:  
Позволяет вводить с клавиатуры фигуры (с типом int в качестве параметра шаблона фигуры) и добавлять в коллекцию;  
Позволяет удалять элемент из коллекции по номеру элемента;  
Выводит на экран введенные фигуры c помощью std::for_each;  
Выводит на экран количество объектов, у которых площадь меньше заданной (с помощью  std::count_if);
## oop_exercise_06
Разработать шаблоны классов согласно варианту задания.  Параметром шаблона должен являться скалярный тип данных задающий тип данных для оси координат. Классы должны иметь публичные поля. Фигуры являются фигурами вращения, т.е. равносторонними (кроме трапеции и прямоугольника). Для хранения координат фигур необходимо использовать шаблон  std::pair.
Создать шаблон динамической коллекции. Коллекция должна быть реализована с помощью умных указателей (std::shared_ptr, std::weak_ptr). Опционально использование std::unique_ptr;
В качестве параметра шаблона коллекция должна принимать тип данных;
Коллекция должна содержать метод доступа:
1) Стек – pop, push, top;
2) Очередь – pop, push, top;  
3) Список, Динамический массив – доступ к элементу по оператору [];  
Реализовать аллокатор, который выделяет фиксированный размер памяти (количество блоков памяти – является параметром шаблона аллокатора). Внутри аллокатор должен хранить указатель на используемый блок памяти и динамическую коллекцию указателей на свободные блоки. Динамическая коллекция должна соответствовать варианту задания (Динамический массив, Список, Стек, Очередь);
Коллекция должна использовать аллокатор для выделения и освобождения памяти для своих элементов.
Аллокатор должен быть совместим с контейнерами std::map и std::list (опционально – vector).
Реализовать программу, которая:
1) Позволяет вводить с клавиатуры фигуры (с типом int в качестве параметра шаблона фигуры) и добавлять в коллекцию использующую аллокатор;
2) Позволяет удалять элемент из коллекции по номеру элемента;
3) Выводит на экран введенные фигуры c помощью std::for_each;

## oop_exercise_07
Разработать программу на языке C++ согласно варианту задания. Спроектировать простейший «графический» векторный редактор.
Требование к функционалу редактора:
* создание нового документа.
* импорт документа из файла.
* экспорт документа в файл.
* создание графического примитива (согласно варианту задания)
* удаление графического примитива.
* отображение документа на экране (печать перечня графических объектов и их характеристик в std::cout).
* реализовать операцию undo, отменяющую последнее сделанное действие. Должно действовать для операций добавления/удаления фигур.
 
Требования к реализации:
1) Создание графических примитивов необходимо вынести в отдельный класс – Factory.
2) Сделать упор на использовании полиморфизма при работе с фигурами.
3) Взаимодействие с пользователем (ввод команд) реализовать в функции main.

## oop_exercise_08
