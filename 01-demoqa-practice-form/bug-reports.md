# Bug report

## Feature

DemoQA Student Registration Form

---

### BUG-01: Модальное окно подтверждения не закрывается по кнопке Close

**Environment:**
- OS: Windows
- Browser: Chrome
- URL: https://demoqa.com/automation-practice-form

**Preconditions:**
- Открыта страница DemoQA Practice Form.
- Форма успешно отправлена.
- Отображается модальное окно подтверждения.

**Steps to Reproduce:**
1. Открыть страницу DemoQA Practice Form.
2. Заполнить обязательные поля First Name, Last Name, Gender и Mobile валидными данными.
3. Нажать кнопку Submit.
4. Дождаться отображения модального окна подтверждения.
5. Нажать кнопку Close в модальном окне подтверждения.

**Actual Result:**
- Модальное окно подтверждения не закрывается после нажатия кнопки Close.
- Модальное окно можно закрыть при клике вне области окна или с помощью клавиши Esc.

**Expected Result:**
- Модальное окно подтверждения закрывается после нажатия кнопки Close.

**Severity:** Medium

**Priority:** Medium

**Attachments:**
- Not attached