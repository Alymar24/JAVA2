# Отчет о тестировании приложения Credit Card Number Validator

## Краткое описание

24.11.2020-24.11.2020 было проведено функциональное ткстирование приложения Credit Card Number Validator

На тестирование затрачено 0,5 часа

В результате тестирования выявлены следующие дефекты: 
Валидные номера карт некоторых банков не признаются таковыми, так как содержат

* больше 16 цифр,https://github.com/Alymar24/JAVA2/issues/1#issue-749689255
* или
* меньше 16 цифр, https://github.com/Alymar24/JAVA2/issues/2#issue-749691855

## Описание процесса тестирования 

В процессе тестирования использовались следующие артефакты

TestCase_Java2.md 

 

В качестве тестовых данных использовались данные карт, сгенерированные сайтом 
https://www.freeformatter.com/credit-card-number-generator-validator.html, а именно:

* карта MasterCard № 5241175304303264 с ожидаемым результатом валидная (ОК)
* карта Visa № 4532052399701629850 с ожидаемым результатом валидная (ОК)
* карта American Express (AMEX) № 374362152947620 с ожидаемым результатом валидная (ОК)
* карта Discover № 6011797427615062 с ожидаемым результатом валидная (ОК)

Тестирование проводилось в следующем окружении:
* Windows 10 x64
* "IntelliJ IDEA Community" 2020.2.3
* Visual Studio Code 1.50.1

