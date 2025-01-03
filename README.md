## Cодержание

1. [Отчет по лабораторной работе № 3](#отчет-по-лабораторной-работе--n)
2. [Критерии оценивания](#критерии-оценивания)

## Отчет по лабораторной работе № 3

#### № группы: `ПМ-2402`

#### Выполнила: `Гуськова Анастасия Павловна`

#### Вариант: `8`

### Cодержание:

- [Постановка задачи](#1-постановка-задачи)
- [Математическая модель](#25-математическая-модель)
- [Алгоритм](#4-алгоритм)
- [Программа](#5-программа)
- [Анализ правильности решения](#6-анализ-правильности-решения)

### 1. Постановка задачи

- Условия задачи

> Разработать программу для работы с числовыми рядами, включая их создание, сортировку и анализ. Реализовать функции вычисления статистических показателей, таких
как средние значения, мода, медиана, дисперсия и другие метрики:
1. Создание списка чисел
   Создание пустого списка чисел, предназначенного для анализа.
2. Вывод отсортированного списка (по возрастанию)
   Отображение списка чисел в порядке неубывания.
3. Добавление числа в список
   Вставка нового числа в список с автоматическим сохранением порядка (по возрастанию).

4. Вывод отсортированного списка (по убыванию)
   Отображение списка чисел в порядке невозрастания.
5. Вывод частотного ряда
   Отображение списка чисел в формате: «число - количество раз, которое оно встречается».
6. Размах числового ряда
   Вычисление размаха как разности между максимальным и минимальным элементами
7. Среднее арифметическое
   Вычисление среднего арифметического всех чисел в списке.
8. Среднее геометрическое
   Вычисление среднего геометрического чисел, используя соответствующую формулу
9. Среднее гармоническое
   Вычисление среднего гармонического чисел в списке.
10. Нахождение моды
    Определение самого часто встречающегося числа. Если все числа встречаются
    одинаковое количество раз, моды нет. Если несколько чисел имеют одинаковую
    максимальную частоту, они образуют набор мод
11. Нахождение медианы
    Определение медианы:
    • Если количество чисел нечётное, медиана — это число посередине.
    • Если количество чисел чётное, медиана равна среднему арифметическому
    двух центральных чисел.
12. Вычисление дисперсии
    Расчёт дисперсии d, равной среднему квадрату отклонений чисел от их среднего
    арифметического.
13. Среднеквадратичное отклонение
    Вычисление среднеквадратичного отклонения σ как квадратного корня из дисперсии d.
14. Дисперсия альтернативного признака
    Расчёт дисперсии альтернативного признака, например, по чётности чисел (чётное
    или нечётное).
15. Вывод всех характеристик ряда
    Отображение всех вычисленных характеристик (размах, средние, мода, медиана,
    дисперсия, среднеквадратичное отклонение и др.) в удобном и читаемом формат


### 2,5. Математическая модель

Для решении данных задач я использовала формулы для вычисления среднего арифметического, геометрического, гармонического, среднеквадратического отклонения, размах строки, частотный ряд массива, вычисления моды, медианы, дисперсии, дисперсии альтернативного признака
Описание формул:

1. Ср. арифметическое: сумму всех чисел в наборе делят на количество всех чисел в наборе
2. Cр. геометрическое: GM = (x1 × x2 × ... × xn)^(1/n), где x1 — первое число, x2 — второе число и так далее, n — общее количество чисел.
3. Гармоническое: H = n/(1/x1 + 1/x2 + ⋯ + 1/xn).
В этой формуле n — количество чисел набора, а x1, x2… — положительный ряд набора.
4. Дисперсия: Формула нахождения дисперсии: S= x¯− x, где. S — дисперсия; x¯ — средний квадрат значений чисел ряда; x — квадрат среднего арифметического ряда.
5. Cреднеквадратичное отклонение: Чтобы вычислить среднеквадратическое отклонение, нужно: 

 Найти среднее арифметическое.
 Для каждого элемента найти квадрат его расстояния до среднего арифметического. 
 Суммировать все результаты, полученные на втором шаге. 
 Делить полученное число на количество элементов. 
 Извлечь квадратный корень
6. Дисперсия альтернативного признака: дисперсия = (доля единиц, обладающих признаком) × (доля единиц, не обладающих данным признаком)

### 3. Алгоритм

1. Класс Statistica обрабатывает массив чисел. В нем описаны следующие методы:
- addChislo(int chislo) - метод для добавления числа в массив с сохранением порядка возрастания
- Vosrastanie() - Метод для вывода отсортированного списка по возрастанию
- Ubvanie() - Метод для вывода отсортированного списка по убыванию
- ChastotniRiad() - Метод для вычисления частоты встречаемости чисел
- Razmach() - Метод для вычисления размаха
- SrArif() - Метод для вычисления среднего арифметического чисел
- SrGeom() - Метод для вычисления среднего геометрического чисел
- Garmonia() - Метод для вычисление гармонического чисел
- moda() - Метод для вычисления моды
- median() - Метод для вычисления медианы
- Dispersia() - Метод для вычисления дисперсии
- Оtklonenie() - Метод для вычисления среднеквадратичного отклонения
- AltDispersia() - метод для вычисления дисперсии альтернативного признака
 Данный метод будет вычислять альтернативную дисперсию по признаку четности числа
- printStatistics() - Вывод всех характеристик ряда
Также в программе есть класс main для тестирования верности работы класса Statistica.

### 4. Программа

```java
public class Statistica {
    private int[] numbers; // Массив для хранения  чисел
    private int size; // Переменная для текущего размера массива (количество чисел)

    // Инициализируем массив numbers
    public Statistica() {
        numbers = new int[100]; // Создаем в массиве 100 ячеек
        size = 0; // стартовое количество чисел 0
    }

    // 1+2. Метод для добавления числа в массив, сразу с сортировкой по возрастанию
    public void addChislo(int chislo) {
        // Проверка, если массив заполнен
        if (size >= numbers.length) {
            System.out.println("Массив заполнен!"); // Проверка!: если это выводится, надо увеличить количество ячеек массива numbers
            return; // Выход из метода, так как некуда добавлять элемент
        }

        // Вставка числа в нужную позицию массива с сохранением прошлого порядка
        int i; //номер в который нужно вставить новый элемент
        // Поиск номера для вставки числа
        for(i=0;i<size;i++){
            if(numbers[i]>chislo){
                break;// цикл находит элемент перед которым вставит число и выходит
            }
        }
        //цикл для освобождения места для нового числа
        for(int j=size;j>i;j--){
            numbers[j]=numbers[j-1];//сдвиг элементов на одну позицию вправо
        }
        numbers[i]=chislo; // вставка числа на найденную позицию
        size++;// увеличиваем размер массива
    }

    // 2. Метод для вывода отсортированного списка по возрастанию
    public void Vosrastanie() {
        System.out.println("Список по возрастанию:");
        for (int i = 0; i < size; i++) {
            System.out.print(numbers[i] + " "); // Просто ыводим каждое число
        }
        System.out.println(); // Переход на новую строку
    }

    // 3. Метод для вывода отсортированного списка по убыванию
    public void Ubvanie() {
        System.out.println("Список по убыванию:");
        for (int i = size - 1; i >= 0; i--) {
            System.out.print(numbers[i] + " "); // Выводим каждое число в обратном порядке
        }
        System.out.println(); // Переход на новую строку
    }
    // 4. Метод для вычисления частоты чисел
    public void ChastotniRiad(){
        for(int i=0;i<size;i++){
            int k=0;
            for(int j=0;j<size;j++){
                if(numbers[i]==numbers[j]){
                    k++;
                }
            }
            System.out.println(numbers[i] +"-"+k);
        }
    }

    // 5. Метод для вычисления размаха
    public int Razmach() {
        if (size == 0) return 0; // Если массив пуст, возвращаем 0
        int min = numbers[0]; // Минимальное значение
        int max = numbers[size - 1]; // Максимальное значение
        return max - min; // Возвращаем разницу
    }

    // 6. Метод для вычисления среднего арифметического чисел
    public double SrArif() {
        if (size == 0) return 0; // Если массив пуст, возвращаем 0
        double sum = 0; // Переменная для хранения суммы
        for (int i = 0; i < size; i++) {
            sum += numbers[i]; // Суммируем все числа
        }
        return sum / size; // Возвращаем среднее
    }

    // 7. Метод для вычисления среднего геометрического чисел
    public double SrGeom(){
        double proizv=1; // начальное произведение берем за 1
        for(int i=0;i<size;i++){ //перемножаем все числа массива
            proizv*=numbers[i];
        }
        double itog=Math.pow(proizv,1.0/size);//из итогового произведения извлекаем корень показатель которго равен size
        return itog;
    }

    // 8. Метод для вычисление гармонического чисел
    public double Garmonia(){
        double sum=0;//создаем переменную для суммирования чисел вида - 1/xn
        for(int i=0;i<size;i++){//циклом обрабатываем все числа в массиве
            if(numbers[i]==0){//проверка: если число 0, то деление на него невозможно
                sum+=0;//если да - прибавляем ноль к сумме
            }
            else{//если нет - прибавляем обратное число
                sum+=(1.0/numbers[i]);
            }
        }
        double garmonia=size/sum;//делим число чисел на сумму
        return garmonia;
    }

    // 9. Метод для вычисления моды
    public void moda() {
        if (size == 0) {
            System.out.println("Мода: нет данных"); // проверка: Если массив пуст, то и моды нет
            return;
        }
        System.out.print("Мода: ");
        int[] counts=new int[size];
        int maxCount = 0; // Максимальное количество вхождений
        int modeValue = numbers[0]; // Значение моды
        for (int i = 0; i < size; i++) {
            int count = 0; //  Переменная для счета количества повторений числа в массиве
            for (int j = 0; j < size; j++) {
                if (numbers[j] == numbers[i]){
                    count++; // Считаем вхождения
                }

            }
            counts[i]=count;//вставляем в доп массив количество повторений
        }
        for(int i=0;i<size;i++){
            if(counts[i]>maxCount){
                maxCount=counts[i];//нашли максимум повторений числа
                modeValue=numbers[i];
            }
        }
        for(int i=0;i<size;i++){
            if(counts[i]==maxCount && numbers[i]!=modeValue){
                System.out.print(numbers[i]+" ");
                break;
            }
        }
        System.out.print(modeValue);
        System.out.println();
    }

    // 10. Метод для вычисления медианы
    public double median() {
        if (size == 0) return 0; // Если массив пуст, возвращаем 0
        if (size % 2 == 1) {
            return numbers[size / 2]; // Если нечетное количество чисел, то возвращаем средний элемент
        } else {
            return (numbers[size / 2 - 1] + numbers[size / 2]) / 2.0; // Если четное, возвращаем среднее арифметическое двух центральных
        }
    }

    // 11. Метод для вычисления дисперсии
    public double Dispersia(){
        double sum=0;//переменная для суммирования чисел массива
        double otkl=0;//переменная для вычисления суммы квадратов разницы числа и средним арифметическим массива
        for(int i=0;i<size;i++){//цикл для суммирования чисел
            sum+=numbers[i];
        }
        double srzn=sum/size;//само среднеее арифметическое массива
        for(int i=0;i<size;i++){//цикл для вычисления суммы квадратов разниц
            otkl+=Math.pow(Math.abs(numbers[i]-srzn),2);
        }
        double dispersia = otkl/size;//делим сумму квадратов отклонений чисел от ср арифметического массива на количество чисел, получаем дисперсию
        return dispersia;
    }

    // 12. Метод для вычисления среднеквадратичного отклонения
    public double Otklonenie(){
        double sum=0;
        double otkl=0;//квадрат расстояния числа до ср арифметического строки
        for(int i=0;i<size;i++){//цикл для суммирования чисел
            sum+=numbers[i];
        }
        double srzn=sum/size;//среднеее арифметическое массива
        for(int i=0;i<size;i++){//цикл для вычисления суммы квадратов разниц
            otkl+=Math.pow(Math.abs(numbers[i]-srzn),2);
        }
        double u=otkl/size;//полученное число деленное на количество элементов
        double otklonenie=Math.sqrt(u);//Извлекаем квадратный корень
        return otklonenie;
    }

    // 13. Метод для вычисления дисперсии альтернативного признака
    //Данный метод будет вычислять альтернативную дисперсию по признаку четности числа
    public double AltDispersia(){
        double chet=0;//переменная для вычисления доли чисел с признаком
        double nechet=0;//переменная для вычисления доли чисел без признака
        for(int i=0;i<size;i++){//цикл для вычисления количества чисел удволетворяющих признаку
            if (numbers[i]%2==0){
                chet++;
            }
        }
        chet=chet/size;//вычисление доли чисел с признаком
        nechet=(size-chet)/size;//вычисление доли чисел без признака
        double altdispersia=chet*nechet;//Вычисление альтернативной дисперсии
        return altdispersia;
    }

    // 14. Вывод всех характеристик ряда
    public void printStatistics() {
        System.out.println("Размах: " + Razmach());
        System.out.println("Среднее арифметическое: " + SrArif());
        System.out.println("Среднее геометрическое: " + SrGeom());
        System.out.println("Гармоническое ряда: " + Garmonia());
        moda(); // Вызываем метод для нахождения моды
        System.out.println("Медиана: " + median());
        System.out.println("Дисперсия: " + Dispersia());
        System.out.println("Среднеквадратическое отклонение: " + Otklonenie());
        System.out.println("Альтернативная дисперсия: " + AltDispersia());
    }

    // Тестируем работу методов
    public static void main(String[] args) {
        Statistica Data = new Statistica(); // для теста обратимся к массиву из класса, с помощью метода addChislo() добавим в него числа
        Data.addChislo(1);
        Data.addChislo(2);
        Data.addChislo(5);
        Data.addChislo(3);
        Data.addChislo(8); // Добавляем число 5 (для проверки правильности вычисления моды строки)
        Data.addChislo(6);
        Data.addChislo(9);

        Data.Vosrastanie(); // Выводим числа по возрастанию
        Data.Ubvanie(); // по убыванию
        Data.ChastotniRiad();// частотный ряд
        Data.printStatistics(); // Выводим статистику по этим числам: размах, ср. арифм, геом, гармон, дисперсию,частотный ряд, альт дисперсию, моду, медиану
    }
}
```

### 5. Анализ правильности решения
Программа работает верно на всем диапазоне чисел.

1. Повторяющиеся числа

- Input:
    ```
    Statistica Data = new Statistica(); 
        Data.addChislo(5);
        Data.addChislo(3);
        Data.addChislo(8);
        Data.addChislo(1);
        Data.addChislo(5); // Добавляем число 5 (для проверки правильности вычисления моды строки)

        Data.Vosrastanie(); 
        Data.Ubvanie(); 
        Data.ChastotniRiad();
        Data.printStatistics();
    ```

- Output:
    ```
    Список по возрастанию:
    1 3 5 5 8
    Список по убыванию:
    8 5 5 3 1
    1-1
    3-1
    5-2
    5-2
    8-1
    Размах: 7
    Среднее арифметическое: 4.4
    Среднее геометрическое: 3.5944318187380233
    Гармоническое ряда: 2.690582959641256
    Мода: 5
    Медиана: 5.0
    Дисперсия: 5.4399999999999995
    Среднеквадратическое отклонение: 2.33238075793812
    Альтернативная дисперсия: 0.192
    ```

2. Все разные числа
- Input:
    ```
    Data.addChislo(1);
        Data.addChislo(2);
        Data.addChislo(5);
        Data.addChislo(3);
        Data.addChislo(8); // Добавляем число 5 (для проверки правильности вычисления моды строки)
        Data.addChislo(6);
        Data.addChislo(9);

        Data.Vosrastanie(); // Выводим числа по возрастанию
        Data.Ubvanie(); // по убыванию
        Data.ChastotniRiad();// частотный ряд
        Data.printStatistics();
    ```

- Output:
    ```
    Список по возрастанию:
   1 2 3 5 6 8 9
   Список по убыванию:
   9 8 6 5 3 2 1
   1-1
   2-1
   3-1
   5-1
   6-1
   8-1
   9-1
   Размах: 8
   Среднее арифметическое: 4.857142857142857
   Среднее геометрическое: 3.868254150740992
   Гармоническое ряда: 2.8734321550741164
   Мода: 2 1
   Медиана: 5.0
   Дисперсия: 7.836734693877552
   Среднеквадратическое отклонение: 2.799416848895061
   Альтернативная дисперсия: 0.4023323615160349
    ```
3. две одинаковые моды
- Input:
    ```
    Data.addChislo(1);
        Data.addChislo(1);
        Data.addChislo(5);
        Data.addChislo(3);
        Data.addChislo(8); 
        Data.addChislo(8);
        Data.addChislo(9);

        Data.Vosrastanie(); 
        Data.Ubvanie(); 
        Data.ChastotniRiad();
        Data.printStatistics();
    ```

- Output:
    ```
   Список по возрастанию:
   1 1 3 5 8 8 9
   Список по убыванию:
   9 8 8 5 3 1 1
   1-2
   1-2
   3-1
   5-1
   8-2
   8-2
   9-1
   Размах: 8
   Среднее арифметическое: 5.0
   Среднее геометрическое: 3.6505567658206943
   Гармоническое ряда: 2.4184261036468326
   Мода: 8 1
   Медиана: 5.0
   Дисперсия: 10.0
   Среднеквадратическое отклонение: 3.1622776601683795
   Альтернативная дисперсия: 0.27405247813411077
    ```
# Критерии оценивания

Обратите внимание на то, что лабораторная работа должна быть выложена в отдельный репозиторий с названием LabN (N -
Номер лабы). В репозитории должно быть минимум 2 файла (README.md - отчет, Main.java - код лабы)

| **Критерий**                                                                                                                                                                           | **Баллы**       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| **Корректность программы**                                                                                                                                                             | **0** - **40**  |
| - Программа полностью выполняет задачу                                                                                                                                                 | 15              |
| - Нет ошибок выполнения                                                                                                                                                                | 10              |
| - Учтены все ограничения                                                                                                                                                               | 5               |
| - Правильное поведение в "крайних" случаях                                                                                                                                             | 10              |
|                                                                                                                                                                                        |                 |
| **Оптимизация кода**                                                                                                                                                                   | **0** - **20**  |
| - Эффективные алгоритмы                                                                                                                                                                | 10              |
| - Избежание избыточности и повторов                                                                                                                                                    | 5               |
| - Разумность использования структур данных                                                                                                                                             | 5               |
|                                                                                                                                                                                        |                 |
| **Читабельность и стиль кода**                                                                                                                                                         | **0** - **20**  |
| - Соблюдение стандартов форматирования                                                                                                                                                 | 5               |
| - Наличие комментариев, в полном объеме поясняющих написанный код                                                                                                                      | 10              |
| - Понятные имена переменных и функций                                                                                                                                                  | 5               |
|                                                                                                                                                                                        |                 |
| **Оформление отчета**                                                                                                                                                                  | **0** - **20**  |
| - Соблюдение структуры отчета                                                                                                                                                          | 5               |
| - Отчет загружен на GitHub в репозиторий с названием LabN (N - номер лабораторной работы), отчет в формате Markdown с названием README.md, также есть файл Main.java с кодом программы | Обязательно     |
| - Четкое описание алгоритма (блок-схема если нужна)                                                                                                                                    | 5               |
| - Полнота покрытия тестами всех случаев                                                                                                                                                | 5               |
| - Обоснования использования алгоритма, структур данных                                                                                                                                 | 5               |
|                                                                                                                                                                                        |                 |
| **Общая сумма**                                                                                                                                                                        | **0** - **100** |

