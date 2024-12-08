В проекті має бути реалізовано функціонал модифікації чисел за допомогою об’єкта блокування. Виведення має бути таким:

Initial value is 7
New value is 21
Initial value is 4
New value is 12
Initial value is 5
New value is 15
Initial value is 2
New value is 6

1) Cтворіть проект Locker-App на локальній машині через IntelliJ IDEA (IDE).

(2) Структура проекту має бути такою:

3) Функціонал класу Main

package app;

public class Main {

  public static void main(String[] args) {
    int[] numbers = new DataRepository().getData();
    DataHandler dataHandler = new DataHandler();
    for (int num : numbers) {
      System.out.println("Initial value is " + num);
      int newNum = dataHandler.modify(num);
      System.out.println("New value is " + newNum);
    }
  }
}

4) Функціонал класу DataRepository

package app;

public class DataRepository {

  public int[] getData() {
    return new int[] {7, 4, 5, 2};
  }
}

(5) Доопрацюйте функціонал класу DataHandler

package app;


public class DataHandler {

  private final Locker lock = new

  public synchronized int modify(int num) {
    lock.();
    try {
      num = num * 3;
      return num;
    } finally {
      lock.unlock();
    }
  }
}

Повернутися до домашок
ДЗ 13.1. Locker App.
Створено: 19.10.2024 13:23
не здано
Здати до: 9 грудня 19:15
Складність:
Завдання виконали
5/10
Середній бал групи
99

В проекті має бути реалізовано функціонал модифікації чисел за допомогою об’єкта блокування. Виведення має бути таким:

Initial value is 7
New value is 21
Initial value is 4
New value is 12
Initial value is 5
New value is 15
Initial value is 2
New value is 6

(1) Cтворіть проект Locker-App на локальній машині через IntelliJ IDEA (IDE).

(2) Структура проекту має бути такою:

(3) Функціонал класу Main

package app;

public class Main {

  public static void main(String[] args) {
    int[] numbers = new DataRepository().getData();
    DataHandler dataHandler = new DataHandler();
    for (int num : numbers) {
      System.out.println("Initial value is " + num);
      int newNum = dataHandler.modify(num);
      System.out.println("New value is " + newNum);
    }
  }
}


(4) Функціонал класу DataRepository

package app;

public class DataRepository {

  public int[] getData() {
    return new int[] {7, 4, 5, 2};
  }
}


(5) Доопрацюйте функціонал класу DataHandler

package app;


public class DataHandler {

  private final Locker lock = new

  public synchronized int modify(int num) {
    lock.();
    try {
      num = num * 3;
      return num;
    } finally {
      lock.unlock();
    }
  }
}


(6) Залийте виконаний проект на свій GitHub репозиторій, посилання на який зазначте в LMS.