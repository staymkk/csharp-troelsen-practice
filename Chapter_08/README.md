# Chapter 08: Время жизни объектов и управление памятью

## 📘 Темы главы

- Сборка мусора (Garbage Collector)
- Метод `Finalize()` и деструкторы
- Интерфейс `IDisposable` и метод `Dispose()`
- Использование `using`
- Управление неуправляемыми ресурсами

---

## ✅ Задания

### 1. 🗑️ `TempFile` с деструктором
Создайте класс `TempFile`, в котором:
- Конструктор выводит `Файл создан`
- Деструктор (`~TempFile`) — `Файл удалён`

В `Main()` создайте объект и вызовите `GC.Collect()` + `GC.WaitForPendingFinalizers()`.

---

### 2. 💾 Класс `LogWriter` с `IDisposable`
Создайте класс `LogWriter`, который:
- В конструкторе открывает файл для записи
- В методе `Log(string msg)` записывает сообщение
- В `Dispose()` закрывает файл и выводит `Лог закрыт`

Используйте `using` для автоматического вызова `Dispose()`.

---

### 3. ❌ Ошибка без `Dispose`
Создайте два примера:
- `FileStream` используется **без** `Dispose()`, что приводит к ресурсоутечке
- Тот же код внутри `using`-блока — корректная работа

Сравните поведение и добавьте комментарии.

---

## 📁 Папки

- `Examples/` — демонстрации работы GC, деструкторов и `Dispose`
- `Tasks/` — практические задания по теме
- `Notes.md` — заметки по управлению памятью
- `README.md` — описание главы и заданий

---

## 📌 Цель

Научиться понимать, как .NET управляет памятью, когда нужно вручную освобождать ресурсы, как применять `Dispose()` и `using`, и чем управляемые ресурсы отличаются от неуправляемых.