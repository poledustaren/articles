# GIGARECOGNIT v2.0

Система распознавания говорящих с транскрипцией и анализом эмоций.

## Структура проекта

```
gigarecognit/
├── src/
│   ├── __init__.py
│   ├── config/
│   │   └── settings.py          # Конфигурация и настройки
│   ├── models/
│   │   └── model_manager.py     # Управление ML моделями
│   ├── database/
│   │   └── speaker_db.py        # База данных говорящих
│   ├── audio/
│   │   ├── audio_processor.py   # Обработка аудио
│   │   ├── diarization.py       # Диаризация говорящих
│   │   ├── speaker_identification.py  # Идентификация
│   │   └── speaker_enrollment.py      # Регистрация говорящих
│   ├── transcription/
│   │   ├── transcriber.py       # Транскрипция
│   │   ├── emotion_analyzer.py  # Анализ эмоций
│   │   └── transcription_manager.py   # Управление транскрипцией
│   ├── utils/
│   │   ├── progress.py          # Прогресс-бары
│   │   ├── file_manager.py      # Управление файлами
│   │   └── statistics.py        # Статистика и отчеты
│   └── core/
│       ├── processor.py         # Основной процессор
│       └── gigarecognit.py      # Главный класс системы
├── main.py                      # Точка входа
├── requirements.txt
├── setup.py
└── README.md
```

## Установка

```bash
pip install -r requirements.txt
```

## Использование

### Полный пайплайн
```bash
python main.py
```

### Обработка директории
```bash
python main.py process_dir /path/to/audio/files
```

### Обработка одного файла
```bash
python main.py process_file /path/to/audio.wav
```

### Статистика
```bash
python main.py stats
```

### Создание отчета
```bash
python main.py report
```

## API

```python
from src.core.gigarecognit import GigaRecognit

# Создание экземпляра
recognizer = GigaRecognit()
recognizer.initialize()

# Обработка файла
recognizer.process_single_file("audio.wav")

# Регистрация говорящего
recognizer.enroll_speaker(["voice1.wav", "voice2.wav"], "John_Doe")
```

## Особенности v2.0

- ✅ Разделение ответственности
- ✅ Легкое тестирование
- ✅ Расширяемость
- ✅ Чистый код
- ✅ Документация
mermaid