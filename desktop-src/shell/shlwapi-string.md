---
description: в этом разделе описываются функции обработки строк оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.
title: Функции обработки строк оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d11ad956b6eab11212243232dfaf8ef341d05544
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473320"
---
# <a name="shell-string-handling-functions"></a>Функции обработки строк оболочки

в этом разделе описываются функции обработки строк оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.

## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>чркмпи</strong></a><br /> | Выполняет сравнение двух символов. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>жетакцептлангуажес</strong></a><br /> | Извлекает строку, используемую с веб-сайтами при указании параметров языка.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>интлстрекн</strong></a><br /> | Выполняет сравнение указанного числа символов с начала двух локализованных строк с учетом регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>интлстрекни</strong></a><br /> | Выполняет сравнение указанного числа символов с начала двух локализованных строк без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>интлстрекворкер</strong></a><br /> | Сравнивает указанное число символов от начала двух локализованных строк.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>исчарспаце</strong></a><br /> | Определяет, представляет ли символ пробел.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>шлоадиндиректстринг</strong></a><br /> | Извлекает указанный текстовый ресурс, когда этот ресурс задается в виде непрямой строки (строка, которая начинается с символа "@").<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>шстрдуп</strong></a><br /> | Создает копию строки в только что выделенной памяти.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br /> | Добавляет одну строку в другую. <br /><blockquote>[!Note]<br />Не используйте. Дополнительные функции см. в разделе Примечания.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>стркатбуфф</strong></a><br /> | Копирует символы из одной строки в другую, а затем добавляет их в конец. <br /><blockquote>[!Note]<br />Не используйте. Дополнительные функции см. в разделе Примечания.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>стркатчаинв</strong></a><br /> | Сцепляет две строки в Юникоде. Используется, если требуются повторные объединения в один и тот же буфер.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br /> | Ищет в строке первое вхождение символа, совпадающего с указанным символом. При сравнении учитывается регистр.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>стрчри</strong></a><br /> | Ищет в строке первое вхождение символа, совпадающего с указанным символом. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>стрчрнив</strong></a><br /> | Ищет в строке первое вхождение указанного символа. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>стрчрнв</strong></a><br /> | Ищет в строке первое вхождение указанного символа. При сравнении учитывается регистр.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br /> | Сравнивает две строки, чтобы определить, совпадают ли они. При сравнении учитывается регистр.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>стркмпк</strong></a><br /> | Сравнивает строки с использованием правил сортировки времени выполнения языка C (ASCII). При сравнении учитывается регистр.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>стркмпи</strong></a><br /> | Сравнивает две строки, чтобы определить, совпадают ли они. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>стркмпик</strong></a><br /> | Сравнивает две строки с помощью правил сортировки времени выполнения языка C (ASCII). Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>стркмплогикалв</strong></a><br /> | Сравнивает две строки в Юникоде. Цифры в строках рассматриваются как числовое содержимое, а не как текст. В этом тесте регистр не учитывается.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>стркмпн</strong></a><br /> | Сравнивает указанное число символов от начала двух строк, чтобы определить, совпадают ли они. При сравнении учитывается регистр. Макрос <strong>StrNCmp</strong> отличается от этой функции только именем.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>стркмпнк</strong></a><br /> | Сравнивает указанное число символов от начала двух строк с помощью правил сортировки времени выполнения языка C (ASCII). При сравнении учитывается регистр.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>стркмпни</strong></a><br /> | Сравнивает указанное число символов от начала двух строк, чтобы определить, совпадают ли они. Сравнение выполняется без учета регистра. Макрос <strong>стрнкмпи</strong> отличается от этой функции только именем.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>стркмпник</strong></a><br /> | Сравнивает указанное число символов от начала двух строк с помощью правил сортировки времени выполнения языка C (ASCII). Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a><br /> | Копирует одну строку в другую. <br /><blockquote>[!Note]<br />Не используйте. Дополнительные функции см. в разделе Примечания.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>стркпин</strong></a><br /> | Копирует указанное число символов с начала одной строки в другую.<br /><blockquote>[!Note]<br />Не используйте эту функцию или макрос <strong>StrNCpy</strong> . Дополнительные функции см. в разделе Примечания.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>стркспн</strong></a><br /> | Ищет в строке первое вхождение любой из групп символов. В методе поиска учитывается регистр, а завершающий <strong>нуль</strong> -символ включается в соответствие шаблону поиска.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>стркспни</strong></a><br /> | Ищет в строке первое вхождение любой из групп символов. В методе поиска регистр не учитывается, а завершающий <strong>нуль</strong> -символ включается в соответствие шаблону поиска.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br /> | Дублирует строку.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br /> | Преобразует числовое значение в строку, представляющую число, выраженное в байтах, килобайтах, мегабайтах или гигабайтах, в зависимости от размера.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>стрформатбитесизеа</strong></a><br /> | Преобразует числовое значение в строку, представляющую число, выраженное в байтах, килобайтах, мегабайтах или гигабайтах, в зависимости от размера. Отличается от <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>стрформатбитесизев</strong></a> в одном типе параметра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>стрформатбитесизикс</strong></a><br /> | Преобразует числовое значение в строку, представляющую число в байтах, килобайтах, мегабайтах или гигабайтах в зависимости от размера. Расширяет <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>стрформатбитесизев</strong></a> , предлагая параметр для округления до ближайшей отображаемой цифры или для удаления неотображаемых цифр.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>стрформатбитесизев</strong></a><br /> | Преобразует числовое значение в строку, представляющую число, выраженное в байтах, килобайтах, мегабайтах или гигабайтах, в зависимости от размера. Отличается от <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>стрформатбитесизеа</strong></a> в одном типе параметра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>стрформаткбсизе</strong></a><br /> | Преобразует числовое значение в строку, представляющую число, выраженное в виде значения размера в килобайтах.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>стрфромтимеинтервал</strong></a><br /> | Преобразует интервал времени, указанный в миллисекундах, в строку.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>стрисинтлекуал</strong></a><br /> | Сравнивает указанное число символов от начала двух строк, чтобы определить, равны ли они.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br /> | Добавляет указанное число символов от начала одной строки к концу другой. <br /><blockquote>[!Note]<br />Не используйте эту функцию или макрос <strong>стркатн</strong> . Дополнительные функции см. в разделе Примечания.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>стрпбрк</strong></a><br /> | Ищет в строке первое вхождение символа, содержащегося в указанном буфере. Этот поиск не включает завершающий нуль символ.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br /> | Выполняет поиск в строке последнего вхождения указанного символа. При сравнении учитывается регистр.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>стррчри</strong></a><br /> | Выполняет поиск в строке последнего вхождения указанного символа. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>стрреттобстр</strong></a><br /> | Принимает структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>стррет</strong></a> , возвращенную <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>Ишеллфолдер:: жетдисплайнамеоф</strong></a> , которая содержит или указывает на строку, и возвращает эту строку в виде <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>стрреттобуф</strong></a><br /> | Преобразует структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>стррет</strong></a> , возвращенную <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>Ишеллфолдер:: жетдисплайнамеоф</strong></a> , в строку и помещает результат в буфер.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>стрреттостр</strong></a><br /> | Принимает структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>стррет</strong></a> , возвращенную <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>Ишеллфолдер:: жетдисплайнамеоф</strong></a> , и возвращает указатель на выделенную строку, содержащую отображаемое имя.<br /> | 
| <a href="strrettostrn.md"><strong>стрреттострн</strong></a><br /> | Принимает структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>стррет</strong></a> , возвращенную <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>Ишеллфолдер:: жетдисплайнамеоф</strong></a>, преобразует ее в строку и помещает результат в буфер.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>стррстри</strong></a><br /> | Выполняет поиск последнего вхождения указанной подстроки в строку. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br /> | Получает длину подстроки в строке, которая состоит исключительно из символов, содержащихся в указанном буфере.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>стрстр</strong></a><br /> | Находит первое вхождение подстроки в строке. При сравнении учитывается регистр.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>стрстри</strong></a><br /> | Находит первое вхождение подстроки в строке. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>стртоинт</strong></a><br /> | Преобразует строку, представляющую десятичное значение, в целое число. Макрос <strong>стртолонг</strong> идентичен этой функции.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br /> | Преобразует строку, представляющую десятичное или шестнадцатеричное значение, в 64-разрядное целое число.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>стртоинтекс</strong></a><br /> | Преобразует строку, представляющую десятичное или шестнадцатеричное число, в целое число.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>стртрим</strong></a><br /> | Удаляет указанные начальные и конечные символы из строки.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>внспринтф</strong></a><br /> | Принимает список аргументов переменной длины и возвращает значения аргументов как отформатированную строку в стиле <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br /><blockquote>[!Note]<br />Не используйте эту функцию. Дополнительные функции см. в разделе Примечания.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>ввнспринтф</strong></a><br /> | Принимает список аргументов и возвращает значения аргументов как отформатированную строку в стиле <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br /><blockquote>[!Note]<br />Не используйте эту функцию. Дополнительные функции см. в разделе Примечания.</blockquote><br /> | 




 

 

 
