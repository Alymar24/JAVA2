Тест приложения Credit Card Number Validator

Предусловие:
* Запустить IntelliJ IDEA
* Внести код:


public class Main {
  public static void main(String[] args) {
    // TODO: подставлять номер карты нужно сюда между двойными кавычками, без пробелов
    String number = "5351719427810741";
    System.out.println(String.format("Result is %s", isValidCardNumber(number) ? "OK" : "FAIL"));
  }

  public static boolean isValidCardNumber(String number) {
    if (number == null) {
      return false;
    }

    if (number.length() != 16) {
      return false;
    }

    long result = 0;
    for (int i = 0; i < number.length(); i++) {
      int digit;
      try {
        digit = Integer.parseInt(number.charAt(i) + "");
      } catch (NumberFormatException e) {
        return false;
      }

      if (i % 2 == 0) {
        digit *= 2;
        if (digit > 9) {
          digit -= 9;
        }
      }
      result += digit;
    }

    return (result != 0) && (result % 10 == 0);
  }
}

Шаги теста:

_1. В четвертую строку кода вводим номер карты 5241175304303264_
* Ожидаемый результат Result is OK
* Фактический результат Result is OK

_2. В четвертую строку кода вводим номер карты 4532052399701629850_

* Ожидаемый результат Result is OK
* Фактический результат Result is FAIL

_3. В четвертую строку кода вводим номер карты 374362152947620_

* Ожидаемый результат Result is OK
* Фактический результат Result is FAIL

_4. В четвертую строку кода вводим номер карты 6011797427615062_

* Ожидаемый результат Result is OK
* Фактический результат Result is OK




