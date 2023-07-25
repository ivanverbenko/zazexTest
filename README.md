# Техническое задание:
Сделать api где в запросе передается текст, он передается в языковую модель, она достает все существительные и возвращает их в ответе.

### Реализовано
Сервис API на Django с применением rest_framework, который принимает текст в формате текстового сообщения и извлекает из него все существительные на русском языке при помощи предобученной модели Transformers. 
Результат возвращается в формате JSON, содержащем список существительных и время обработки в секундах.

### Результат тестирования
Тестирование времени обработки для различных объемов текста: для "Война и Мир" время обработки было примерно 120 секунд, для большого сборника произведений разных авторов(объем примерно 50мб) время обработки было примерно  650 секунд.

### Формат использования

#### Параметры
```bash
URL: {HOST}/tagger/extract_nouns/
Метод: POST
Формат запроса: text
Формат ответа: json
```

#### Пример запроса
```html
Привел пример извлечения из текста существительных
```

#### Пример ответа:
```json
{
    "result": [
        "пример",
        "извлечение",
        "текст",
        "существительное"
    ],
    "time": 1.192478656768799
}
```
