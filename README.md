🎮 PPG Mod Studio AI
<div align="center">
https://img.shields.io/badge/%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F-1.0.0-blue?style=for-the-badge
https://img.shields.io/badge/%D1%81%D1%82%D0%B0%D1%82%D1%83%D1%81-%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%B5%D0%BD-success?style=for-the-badge
https://img.shields.io/badge/%D0%BB%D0%B8%D1%86%D0%B5%D0%BD%D0%B7%D0%B8%D1%8F-MIT-green?style=for-the-badge
https://img.shields.io/badge/AI-Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white

✨ Интерактивная студия для создания модов к People Playground с ИИ-помощником

</div>
📖 О проекте
PPG Mod Studio AI — это веб-приложение (один HTML-файл) для разработки модов к игре People Playground с интеграцией Google Gemini AI.

Просто опишите механику мода на русском языке, а ИИ сгенерирует C# код и структуру файлов. Всё управление файлами — через удобный интерфейс с боковой панелью.

✨ Возможности
Функция	Описание
🤖 ИИ-помощник	Общайтесь с Gemini на русском, описывайте механику мода
📁 Файловый менеджер	Встроенная файловая система с созданием/удалением файлов
🧠 VFS-команды	ИИ автоматически сохраняет файлы через специальные блоки WRITE/DELETE
📦 Экспорт в ZIP	Скачивайте готовый мод одним кликом
🔌 Гибкие API	Поддержка Google Gemini, OpenRouter, любых OpenAI-совместимых прокси
🖼️ Загрузка изображений	Прикрепляйте референсы и скриншоты к запросам
💾 Локальное сохранение	Все данные (чат, файлы, настройки) сохраняются в браузере
🚀 Быстрый старт
1. Клонируйте репозиторий
bash
git clone https://github.com/iljalepmets12-stack/ppg-mod-studio.git
cd ppg-mod-studio
2. Откройте index.html
bash
# Windows
start index.html

# macOS
open index.html

# Linux
xdg-open index.html
3. Настройте API ключ
Нажмите ⚙ Настройки в правом верхнем углу

Вставьте API ключ:

Для Gemini: AIzaSy... (получить на Google AI Studio)

Для OpenRouter: sk-... (получить на OpenRouter)

Выберите модель в выпадающем списке

4. Начинайте творить!
Напишите в чат, какой мод хотите создать, и ИИ поможет вам!

🧠 Как это работает
Архитектура
text
Вы → Чат → Gemini AI → VFS-команды → Файлы мода → 📦 ZIP
VFS-команды (Virtual File System)
ИИ использует специальные блоки в ответах для управления файлами:

markdown
```vfs
WRITE /mod.json
{
  "Name": "Мой мод",
  "Author": "Ваше имя",
  "Description": "Описание мода",
  "ModVersion": "1.0",
  "GameVersion": "1.26+",
  "EntryPoint": "Mod.Main"
}
```

```vfs
WRITE /Main.cs
using UnityEngine;

namespace Mod
{
    public class Main
    {
        public static void Main()
        {
            // Ваш код
        }
    }
}
```

```vfs
DELETE /OldScript.cs
```
Все созданные файлы появляются в боковой панели "Файлы мода".

🛠️ Поддерживаемые модели
Модель	API	Настройка
gemini-2.5-flash	Google Gemini	По умолчанию
gemini-2.5-pro	Google Gemini	Выбрать в меню
Любая кастомная	OpenRouter / OpenAI	Выбрать "Кастомная модель" + указать ID
Пример для OpenRouter:
text
Base URL: https://openrouter.ai/api/v1
API Key: sk-...
Модель: google/gemini-2.5-flash-exp:free
📂 Структура проекта
text
ppg-mod-studio/
├── 📄 index.html          # Полное приложение (всё в одном файле)
├── 📄 README.md           # Документация
└── 📄 LICENSE             # Лицензия
Проект — это один HTML-файл с встроенными стилями и JavaScript.

🎯 Пример использования
Напишите в чат:

"Создай мод, который добавляет взрывающуюся палку. При клике ПКМ она через 2 секунды взрывается с радиусом 5."

ИИ сгенерирует:

mod.json — манифест мода

Main.cs — C# скрипт с логикой взрыва

Дополнительные файлы при необходимости

Нажмите 📦 "Скачать мод (.zip)" — готовый мод для установки в игру!

⚙️ Настройки
Параметр	Описание
API Key	Ключ от Google Gemini (AIzaSy...) или OpenRouter (sk-...)
Base URL	Для прокси (оставьте пустым для оригинального Gemini)
Кастомная модель	ID модели, если выбрана "Кастомная модель"
🛠️ Разработка и вклад
Хотите улучшить проект?

Форкните репозиторий

Внесите изменения в index.html

Проверьте работу

Отправьте Pull Request

Идеи для улучшения:
□ Поддержка нескольких языков интерфейса
□ Готовые шаблоны модов (оружие, предметы, механики)
□ Визуальный редактор спрайтов
□ История версий файлов
□ Экспорт в готовый .dll
📄 Лицензия
Распространяется под лицензией MIT. Подробности в файле LICENSE.

📬 Контакты
<div align="center">
https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white

</div>
<div align="center"> <sub>Сделано с ❤️ для сообщества People Playground</sub> </div>
