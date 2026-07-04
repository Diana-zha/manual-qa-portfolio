# Requirements

## Feature

DemoQA Student Registration Form

## Test Object

DemoQA Practice Form

## Source

Требования составлены на основе наблюдаемого поведения формы DemoQA Student Registration Form, так как официальное бизнес-требование не предоставлено.

## Description

Форма позволяет пользователю отправить данные регистрации студента и увидеть отправленные данные в модальном окне подтверждения.

## Fields

- First Name
- Last Name
- Email
- Gender
- Mobile
- Date of Birth
- Subjects
- Hobbies
- Picture
- Current Address
- State
- City

## Observed Business Rules

- Поле First Name является обязательным.
- Поле Last Name является обязательным.
- Поле Gender является обязательным.
- Поле Mobile является обязательным.
- Поле Mobile ожидает ввод 10 цифр.
- Поле Email принимает значение в формате email.
- Date of Birth выбирается через календарь.
- Subjects вводится через поле с автодополнением.
- Hobbies выбирается с помощью чекбоксов.
- Picture загружается из локальной файловой системы.
- State и City выбираются из выпадающих списков.
- Список City зависит от выбранного State.
- Кнопка Submit отправляет форму.
- После успешной отправки отображается модальное окно подтверждения.
- В модальном окне отображаются отправленные данные.

## Open Questions

Некоторые правила валидации и ожидаемое поведение формы неочевидны и требуют уточнения у Product Owner или аналитика.