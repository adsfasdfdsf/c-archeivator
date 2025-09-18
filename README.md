# 📘 Учебный проект: Архиватор строк (C# / .NET)

## Задача

Нужно реализовать **простейший архиватор методом RLE** (Run-Length Encoding).  
Архиватор должен уметь работать со строками.

Пример:

```

Исходная строка: "aaabb"
Сжатая строка:  "3a2b"
Разжатая строка: "aaabb"

```

---

## 📝 Что нужно сделать

В файле `Archiver.cs` уже заготовлены методы с комментариями:

* `CompressString(string input) -> string`  
  Сжимает строку методом RLE.  
  ⚠️ Нужно использовать вспомогательный метод `WriteRun` и `StringBuilder`.

* `DecompressString(string compressed) -> string`  
  Разжимает строку, восстановленную из RLE-формата.

* `WriteRun(StringBuilder output, char symbol, int count)`  
  Записывает в выходной буфер пару `(count, symbol)` с учётом экранирования.  
  Например:

```

count=3, symbol='a' → "3a"
count=2, symbol='\' → "2\\"
count=3, symbol='3' → "3\3"
count=1, symbol='b' → "b"

````

Твоя задача — реализовать эти методы вместо:

```csharp
throw new NotImplementedException("implement me");
````

---

## ✅ Автотесты

Для проверки написан файл `ArchiverTests.cs`.
Мы используем библиотеку **NUnit**.

Тесты включают:

* Юнит-тесты для строковых функций (`CompressString`, `DecompressString`)


---

## 🚀 Запуск тестов

Выполни в корне проекта:

```
dotnet test Archiver.csproj
```

