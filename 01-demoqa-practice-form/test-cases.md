# Test-cases

## Feature

DemoQA Student Registration Form

## Test-cases

### TC-01: Успешная отправка формы с заполнением обязательных полей

**Priority:** High  
**Status:** Passed

**Preconditions:**
- Открыта страница DemoQA Practice Form.

**Test Data:**
- First Name: Anna
- Last Name: Ivanova
- Gender: Female
- Mobile: 1234567890

**Steps:**
1. Ввести значение в поле First Name.
2. Ввести значение в поле Last Name.
3. Выбрать значение Gender.
4. Ввести значение в поле Mobile.
5. Нажать кнопку Submit.

**Expected Result:**
- Форма успешно отправляется.
- Отображается модальное окно подтверждения.
- В модальном окне отображаются введённые данные: First Name, Last Name, Gender и Mobile.

---

### TC-02: Успешная отправка формы с заполнением всех полей

**Priority:** High  
**Status:** Passed

**Preconditions:**
- Открыта страница DemoQA Practice Form.

**Test Data:**
- First Name: Anna
- Last Name: Ivanova
- Email: anna.ivanova@example.com
- Gender: Female
- Mobile: 1234567890
- Date of Birth: 10 May 2000
- Subjects: Maths
- Hobbies: Sports, Reading
- Picture: test-image.png
- Current Address: Test address 123
- State: NCR
- City: Delhi

**Steps:**
1. Ввести значение в поле First Name.
2. Ввести значение в поле Last Name.
3. Ввести значение в поле Email.
4. Выбрать значение Gender.
5. Ввести значение в поле Mobile.
6. Выбрать Date of Birth через date picker.
7. Выбрать значение в поле Subjects из списка автодополнения.
8. Выбрать значения Hobbies.
9. Загрузить файл в поле Picture.
10. Ввести значение в поле Current Address.
11. Выбрать значение State.
12. Выбрать значение City.
13. Нажать кнопку Submit.

**Expected Result:**
- Форма успешно отправляется.
- Отображается модальное окно подтверждения.
- В модальном окне отображаются все введённые и выбранные пользователем данные.

---

### TC-03: Проверка обязательных полей при отправке пустой формы

**Priority:** High  
**Status:** Passed

**Preconditions:**
- Открыта страница DemoQA Practice Form.

**Test Data:**
- Не используется.

**Steps:**
1. Не заполнять поля формы.
2. Нажать кнопку Submit.

**Expected Result:**
- Форма не отправляется.
- Модальное окно подтверждения не отображается.
- Обязательные поля First Name, Last Name, Gender и Mobile визуально подсвечиваются как невалидные.

---

### TC-04: Валидация Mobile — менее 10 цифр

**Priority:** High  
**Status:** Passed

**Preconditions:**
- Открыта страница DemoQA Practice Form.

**Test Data:**
- First Name: Anna
- Last Name: Ivanova
- Gender: Female
- Mobile: 123456789

**Steps:**
1. Ввести значение в поле First Name.
2. Ввести значение в поле Last Name.
3. Выбрать значение Gender.
4. Ввести невалидное значение в поле Mobile: `123456789`.
5. Нажать кнопку Submit.

**Expected Result:**
- Форма не отправляется.
- Модальное окно подтверждения не отображается.
- Поле Mobile визуально подсвечивается как невалидное.

---

### TC-05: Ограничение длины поля Mobile при вводе более 10 цифр

**Priority:** High  
**Status:** Passed

**Preconditions:**
- Открыта страница DemoQA Practice Form.

**Test Data:**
- Mobile: 12345678901

**Steps:**
1. Ввести значение в поле Mobile: `12345678901`.

**Expected Result:**
- Поле Mobile не позволяет ввести более 10 цифр.
- В поле Mobile отображается только значение `1234567890`.
- Одиннадцатая цифра не добавляется в поле.

---

### TC-06: Валидация Email — невалидный формат

**Priority:** High  
**Status:** Passed

**Preconditions:**
- Открыта страница DemoQA Practice Form.

**Test Data:**
- First Name: Anna
- Last Name: Ivanova
- Gender: Female
- Mobile: 1234567890
- Email: anna.ivanovaexample.com

**Steps:**
1. Ввести значение в поле First Name.
2. Ввести значение в поле Last Name.
3. Выбрать значение Gender.
4. Ввести значение в поле Mobile.
5. Ввести невалидное значение в поле Email: `anna.ivanovaexample.com`.
6. Нажать кнопку Submit.

**Expected Result:**
- Форма не отправляется.
- Модальное окно подтверждения не отображается.
- Поле Email визуально подсвечивается как невалидное.

---

### TC-07: Проверка зависимости State и City

**Priority:** Medium  
**Status:** Passed

**Preconditions:**
- Открыта страница DemoQA Practice Form.

**Test Data:**
- State: NCR
- City: Delhi

**Steps:**
1. Открыть выпадающий список State.  
   **Expected Result:** Отображается список доступных State.

2. Выбрать значение State: NCR.  
   **Expected Result:** Значение NCR отображается в поле State.

3. Открыть выпадающий список City.  
   **Expected Result:** В списке City отображаются города, доступные для выбранного State NCR.

4. Выбрать значение City: Delhi.  
   **Expected Result:** Значение Delhi отображается в поле City.

---

### TC-08: Закрытие модального окна подтверждения по кнопке Close

**Priority:** Medium  
**Status:** Failed

**Preconditions:**
- Открыта страница DemoQA Practice Form.
- Форма успешно отправлена.
- Отображается модальное окно подтверждения.

**Test Data:**
- First Name: Anna
- Last Name: Ivanova
- Gender: Female
- Mobile: 1234567890

**Steps:**
1. Заполнить обязательные поля First Name, Last Name, Gender и Mobile валидными данными.
2. Нажать кнопку Submit.
3. Убедиться, что отображается модальное окно подтверждения.
4. Нажать кнопку Close в модальном окне подтверждения.

**Expected Result:**
- Модальное окно подтверждения закрывается после нажатия кнопки Close.

**Actual Result:**
- Модальное окно подтверждения не закрывается после нажатия кнопки Close.
- Модальное окно можно закрыть только при клике вне области окна или с помощью клавиши Esc.
