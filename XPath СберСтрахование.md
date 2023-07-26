# XPath'ы кнопок:

1. Кнопка "Квартира":
//button[@id='mat-button-toggle-1-button']

2. Кнопка "Дом":
//button[@id='mat-button-toggle-2-button']

3. Кнопка Сдается в аренду "Да":
//*[text()='Сдается в аренду']/following::button[1]

4. Кнопка Сдается в аренду "Нет"
//*[text()='Сдается в аренду']/following::button[2]

5. Кнопка Расположена на первом или последнем этаже "Да"
//*[text()='Расположена на первом или последнем этаже']/following::button[1]

6. Кнопка Расположена на первом или последнем этаже "Нет"
//*[text()='Расположена на первом или последнем этаже']/following::button[2]

7. Кнопка Установлена охранная сигнализация "Да"
//*[text()='Установлена охранная сигнализация']/following::button[1]

8. Установлена охранная сигнализация "Нет"
//*[text()='Установлена охранная сигнализация']/following::button[2]

9. Кнопка Промокод "Применить"
//button[@class='mat-focus-indicator action-back mat-stroked-button mat-button-base']

10. Кнопка "Оформить"
//button[@class='mat-focus-indicator mat-stroked-button mat-button-base mat-accent mat-button-disabled']

11. Кнопка "заполнить по Сбер ID"
//button[@class='mat-focus-indicator sber-id-button mat-flat-button mat-button-base mat-primary']

12. Кнопка "Мужской"
//*[text()='Мужской']

13. Кнопка "Женский"
//*[text()='Женский']

14. Кнопка "Вернуться"
//button[@class='mat-focus-indicator action-back mat-stroked-button mat-button-base']

15. Кнопка "Оформить"
//button[@class='mat-focus-indicator mat-flat-button mat-button-base mat-accent']

# XPath'ы полей для ввода текста:

1. Регион проживания:
//div[@class='mat-form-field-outline mat-form-field-outline-thick ng-tns-c61-0 ng-star-inserted']

2. Промокод:
//div[@class='mat-form-field-wrapper ng-tns-c61-22']

3. Фамилия: 
//div[@class='mat-form-field-infix ng-tns-c61-3']

4. Имя: 
//div[@class='mat-form-field-infix ng-tns-c61-4']

5. Отчество: 
//div[@class='mat-form-field-infix ng-tns-c61-5']

6. Серия:
//div[@class='mat-form-field-infix ng-tns-c61-7']

7. Номер: 
//div[@class='mat-form-field-flex ng-tns-c61-8']

8. Кем выдан: 
//div[@class='mat-form-field-infix ng-tns-c61-10']

9. Код подразделения: 
//div[@class='mat-form-field-infix ng-tns-c61-11']

10. Регион: 
//div[@class='mat-form-field-infix ng-tns-c61-12']

11. Город или населенный пункт: 
//div[@class='mat-form-field-infix ng-tns-c61-13']

12. Улица: 
//div[@class='mat-form-field-infix ng-tns-c61-14']

14. Дом, литера, корпус, строение: 
//div[@class='mat-form-field-infix ng-tns-c61-15']

15. Квартира: 
//div[@class='mat-form-field-infix ng-tns-c61-16']

16. Телефон: 
//div[@class='mat-form-field-infix ng-tns-c61-17']

17. Электронная почта: 
//div[@class='mat-form-field-infix ng-tns-c61-18']

18. Повтор электронной почты: 
//div[@class='mat-form-field-infix ng-tns-c61-19']


# Чек-боксы:
1. Отчество отсутсвует:
//*[@id="mat-checkbox-1"]

2. Улица отсутствует: 
//*[@id="mat-checkbox-2"]

# Датапикеры:

1. Срок действия страхования:
//button[@class='mat-focus-indicator mat-icon-button mat-button-base']

2. Дата рождения:
//*[text()='Дата рождения']/following::button[1]

3. Дата выдачи:
//*[text()='Дата выдачи']/following::button[1]

# Логотип СберСтрахования:
1. //*[@class='sber-logo']
2. //div[@class='sber-logo']

# Слайдера в блоке выбора суммы:
1. //div[@class='mat-slider-wrapper']

# Хедер "Что будет застраховано?":
//*[text()='Что будет застраховано?']

# Текстовые блоки:
1. "Мебель, техника и ваши вещи":
//div[@class='sbi-form__col-2'][contains(., 'Мебель')]
2. "Падение летательных аппаратов и их частей":
//*[text()='Падение летательных аппаратов и их частей']

#  Колонки в списке, который находится под хедером "Страховая защита включенная в программу".
1. Чрезвычайная ситуация колонка:
//div[text()='Чрезвычайная ситуация']/ancestor::ul
2. Стихийные бедствия:
//div[text()='Стихийные бедствия']/ancestor::ul
