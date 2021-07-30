# Lesson_1-Helper-Classes-and-Lambda-Functions
Домашнее задание

Имеется база сотрудников и номеров их телефонов. Требуется написать соответствующие структуры для хранения данных, и заполнить контейнер записями из базы. Затем необходимо реализовать методы обработки данных, а также вывести на экран всю необходимую информацию.

Важно! Имена переменным, классам и функциям давайте осознанные, состоящие из слов на английском языке.

Создайте структуру Person с 3 полями: фамилия, имя, отчество. Поле отчество должно быть опционального типа, т.к. не у всех людей есть отчество. 
Перегрузите оператор вывода данных для этой структуры. Также перегрузите операторы < и == (используйте tie).
Создайте структуру PhoneNumber с 4 полями:

·         код страны (целое число)

·         код города (целое число)

·         номер (строка)

·         добавочный номер (целое число, опциональный тип)

Для этой структуры перегрузите оператор вывода. Необходимо, чтобы номер телефона выводился в формате: +7(911)1234567 12, где 7 – это номер страны, 911 – номер города, 1234567 – номер, 12 – добавочный номер. Если добавочного номера нет, то его выводить не надо.

Создайте класс PhoneBook, который будет в контейнере хранить пары: Человек – Номер телефона. Конструктор этого класса должен принимать параметр типа ifstream – поток данных, полученных из файла. В теле конструктора происходит считывание данных из файла и заполнение контейнера. Класс PhoneBook должен содержать перегруженный оператор вывода, для вывода всех данных из контейнера в консоль.

В классе PhoneBook реализуйте метод SortByName, который должен сортировать элементы контейнера по фамилии людей в алфавитном порядке. Если фамилии будут одинаковыми, то сортировка должна выполняться по именам, если имена будут одинаковы, то сортировка производится по отчествам. Используйте алгоритмическую функцию sort.

Реализуйте метод SortByPhone, который должен сортировать элементы контейнера по номерам телефонов. Используйте алгоритмическую функцию sort.

Реализуйте метод GetPhoneNumber, который принимает фамилию человека, а возвращает кортеж из строки и PhoneNumber. Строка должна быть пустой, если найден ровно один человек с заданном фамилией в списке. Если не найден ни один человек с заданной фамилией, то в строке должна быть запись «not found», если было найдено больше одного человека, то в строке должно быть «found more than 1».  Для прохода по элементам контейнера используйте алгоритмическую функцию for_each.

Реализуйте метод ChangePhoneNumber, который принимает человека и новый номер телефона и, если находит заданного человека в контейнере, то меняет его номер телефона на новый, иначе ничего не делает. Используйте алгоритмическую функцию find_if.
