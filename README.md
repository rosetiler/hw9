# 1. Общие сведения
Работу выполняла в Notepad++, проверяла на [regexr.com](https://regexr.com/)
# 2. Замена пустых строк
Сначала я написала такое регулярное выражение: ^\s+$ чтобы найти все строки, начинающиеся с пробела. Оказалось, что в тексте есть не только строки с пробелами, но и отступы между абзацами, поэтому формулу изменила на такую: ^\s|\d+$. Чтобы убрать строки, я их заменила на пустоту, как на скриншоте:

![](https://github.com/rosetiler/hw9/blob/master/%D0%B7%D0%B0%D0%BC%D0%B5%D0%BD%D0%B0%20%D0%BF%D1%83%D1%81%D1%82%D1%8B%D1%85%20%D1%81%D1%82%D1%80%D0%BE%D0%BA.png)
# 3. Поиск имен и городов
Для поиска всех имен на "слав" я придумала такое регулярное выражение: [А-Я]\w+слав(\w+)?
Поскольку regexr вообще отказался искать по такой формуле, я попробовала сразу в Notepad++. Итого - **592 вхождения**, среди них правильно выбраны имена и города, но есть проблема. Ноутпад выдает странные артефакты, которые не убираются изменениями формулы (становится только хуже). Пример на скриншоте:
![](https://github.com/rosetiler/hw9/blob/master/%D0%BF%D1%80%D0%BE%D0%B1%D0%BB%D0%B5%D0%BC%D0%B0%20%D1%81%20%D0%B0%D1%80%D1%82%D0%B5%D1%84%D0%B0%D0%BA%D1%82%D0%B0%D0%BC%D0%B8.png)

К тому же на скриншоте можно заметить, что некоторые имена не подсвечиваются, хотя они явно подходят по формуле... Эту проблему не удалось решить даже после консультации с преподавателем.
# 4. Поиск всех случаев использования Новгорода
Для поиска всех случаев употребления слова Новгород я использовала такую формулу: Нов.?город(а|у|е|ом|ъ)? 
Как видно из формулы я оставила неизменные корни "нов" и "город", между ними оставила возможность появления любого знака и прибавила окончания всех падежей плюс твердый знак. На regexr все выглядело так:
![](https://github.com/rosetiler/hw9/blob/master/%D0%BD%D0%BE%D0%B2%D0%B3%D0%BE%D1%80%D0%BE%D0%B4%20%D1%80%D0%B5%D0%B3%D0%B5%D0%BA%D1%81.png)
Всего **59 вхождений** - все соответствуют нужному запросу.
В Ноутпад++ результат тот же:
![](https://github.com/rosetiler/hw9/blob/master/%D0%BD%D0%BE%D0%B2%D0%B3%D0%BE%D1%80%D0%BE%D0%B4%20%D0%BD%D0%BE%D1%83%D1%82%D0%BF%D0%B0%D0%B4.png)
Бонусные задания я не делала. Файл с текстом прилагается.
