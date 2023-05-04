# **Final_Control_Work**

1. Создать репозиторий на GitHub.
2. Нарисовать блок-схему алгоритма (можно обойтись блок-схемой основной содержательной части, если вы выделяете её в отдельный метод).
3. Снабдить репозиторий оформленным текстовым описанием решения (файл README.md).
4. Написать программу, решающую поставленную задачу.
5. Использовать контроль версий в работе над этим небольшим проектом (не должно быть так, что всё залито одним коммитом, как минимум этапы 2, 3, и 4 должны быть расположены в разных коммитах).

# **Описание решения**
Запрашиваем у пользователя количество элементов массива, эта переменная будет использоваться как длина нового массива *"stringArray"*, который мы объявляем следом.

Далее запускаем метод, который запрашивает у пользователя ввести элементы массива и помещаем их в массив *"stringArray"*.

Следующим шагом запускаем метод вывода на печать готового массива, который выводит массив полученный методом выборки из введённых данных <=3 значений и их записи в искомый массив.
___
## **Описание методов:**
___
### **1. Метод запроса ввода данных у пользователя и составления массива *"stringArray"*:**

- для условия что *"i"* не превышает длины массива указанной самим пользователем в начале, выполняем следующее действие:
```
    Console.Write($"Введите {i + 1}й элемент массива: ");
```
  т.е. просим ввести пользователя каждый элемент массива (буквы, цифры, символы), начиная с самого первого.

 -  после чего строкой кода:
```
    stringArray[i] = Console.ReadLine();
```
  присваиваем массиву *"stringArray"* поочерёдно каждый элемент введённый пользователем.

### **2. Метод выборки из введённых данных <=3 значений и их записи в новый массив:**

- объявляем новую переменную *"n"* определяющую длину будущего массива и заводим цикл для определения длины будущего массива с условием:
```
  for (int i = 0; i < stringArray.Length; i++)
```
- далее с помощью оператора ***if*** выбираем элементы, значения длины которых менее или равны трём. Т.о. определяем длину *"n"* будущего массива.

- после выхода из вышеописанного цикла мы получаем длину массива *"n"* и объявляем новый массив "result" с этой длиной:
```
  string[] result = new string[n];
```
  попутно объявляя переменную *"j"*, которая будет выполнять роль индекса элементов нового массива и помогать в переборе элементов.

- заводим цикл для выборки будущих элементов массива с условием:
```
  for (int i = 0; i < stringArray.Length; i++)
```
- далее с помощью оператора ***if*** выбираем элементы, значения длин которых менее или равны трём, после чего записываем отсеянные элементы в новый массив *"result"*.

- возвращаем полученный массив *"result"* с отсеянными элементами.

## **3. Метод вывода на печать:**

- Выводим на печать первую скобку *"["* (чтобы было как в задании), но добавляем перед скобкой *"\n"*, чтобы начать с новой строки.

- далее при выполнении цикла for выводим по одному элементу на печать.

- строчкой кода:
```
    if (i != stringArray.Length - 1) Console.Write(",");
```
  "избавляемся от лишней запятой" которые разделяют элементы массива. Т.е. пока *"i"* не равна длине массива минус один "," будет выводиться, а после завершающего элемента - нет.

- Выводим на печать закрывающую скобку *"]".*
