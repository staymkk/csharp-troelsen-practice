# Chapter 04: Главные конструкции программирования на C# (часть II)

## 📘 Темы главы
- Работа со строками (`string`)
- Перечисления (`enum`)
- Структуры (`struct`)
- Дополнительные элементы управления потоком

---

## ✅ Задания

### 1. 📍 Структура Point2D
Создайте структуру `Point2D` с полями `X`, `Y` и методом `DistanceTo(Point2D other)`, который возвращает расстояние между двумя точками по формуле:

sqrt((x2 - x1)^2 + (y2 - y1)^2)

yaml
Копировать
Редактировать

Реализуйте метод и протестируйте его в `Main`.

---

### 2. 🗓️ Перечисление и расписание
Создайте перечисление `WeekDay` с днями недели. Напишите программу, которая:
- принимает значение дня недели от пользователя
- выводит расписание на этот день

Используйте `enum.Parse` для преобразования строки в `enum`.

*Пример:*
Введите день недели: Monday
Расписание: 9:00 — совещание, 11:00 — код-ревью

yaml
Копировать
Редактировать

---

### 3. ✂️ Подсчёт слов в строке
Напишите программу, которая:
- принимает строку от пользователя
- выводит количество слов в строке

Слова считаются разделёнными пробелами. Используйте `string.Split()` и `Trim()`.

---

## 💡 Советы
- Для структур обязательно используйте `public` модификаторы
- Попробуйте перегрузить `ToString()` в структуре `Point2D`
- Используйте `Enum.TryParse()` для безопасного разбора строки

---

## 📁 Папки

- `Examples/` — демонстрации синтаксиса и особенностей `string`, `enum`, `struct`
- `Tasks/` — реализации заданий с тестами
- `Notes.md` — заметки по ключевым моментам

---

## 📌 Цель
Научиться создавать собственные типы данных (`struct`, `enum`), уверенно работать со строками, закрепить управление потоком выполнения.
