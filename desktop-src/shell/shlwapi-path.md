---
description: в этом разделе описываются функции обработки пути оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.
title: Функции обработки пути оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 90937e4aa3c93c14957ec0db7f081c1cb598989e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481970"
---
# <a name="shell-path-handling-functions"></a>Функции обработки пути оболочки

в этом разделе описываются функции обработки пути оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.

## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>пасаддбаккслаш</strong></a><br /> | Добавляет обратную косую черту в конец строки, чтобы создать правильный синтаксис для пути. Если в исходном пути уже есть обратная косая черта, обратная косая черта не добавляется. <br /><blockquote>[!Note]<br />Неправильное использование этой функции может привести к переполнению буфера. На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>паскчаддбаккслаш</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>паскчаддбаккслашекс</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>пасаддекстенсион</strong></a><br /> | Добавляет расширение имени файла в строку пути.<br /><blockquote>[!Note]<br />Неправильное использование этой функции может привести к переполнению буфера. Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>паскчаддекстенсион</strong></a> на своем месте.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>пасаппенд</strong></a><br /> | Добавляет один путь к концу другого. <br /><blockquote>[!Note]<br />Неправильное использование этой функции может привести к переполнению буфера. На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>паскчаппенд</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>паскчаппендекс</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>пасбуилдрут</strong></a><br /> | Создает корневой путь из заданного номера диска.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>пасканоникализе</strong></a><br /> | Упрощает путь путем удаления элементов навигации, таких как "." и "..", для создания прямого, правильно сформированного пути.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>паскомбине</strong></a><br /> | Объединяет две строки, представляющие правильно сформированные пути, в один путь. также сцепляет все элементы относительного пути. <br /><blockquote>[!Note]<br />Неправильное использование этой функции может привести к переполнению буфера. На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>паскчкомбине</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>паскчкомбиникс</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>паскоммонпрефикс</strong></a><br /> | Сравнивает два пути, чтобы определить, имеют ли они общий префикс. Префикс имеет один из следующих типов: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>паскомпактпас</strong></a><br /> | Усекает путь к файлу в соответствии с заданной шириной в пикселях, заменяя компоненты пути многоточием.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>паскомпактпасекс</strong></a><br /> | Усекает путь, чтобы он поместился в определенное число символов, заменяя компоненты пути многоточием.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>паскреатефромурл</strong></a><br /> | Преобразует URL-адрес файла в путь Microsoft MS-DOS.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>паскреатефромурлаллок</strong></a><br /> | Создает путь из URL-адреса файла.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>пасфиликсистс</strong></a><br /> | Определяет, является ли допустимым путь к объекту файловой системы, например файлу или папке.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>пасфиндекстенсион</strong></a><br /> | Поиск расширения в пути.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>пасфиндфиленаме</strong></a><br /> | Поиск имени файла в пути.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>пасфинднексткомпонент</strong></a><br /> | Анализирует путь и возвращает часть этого пути, следующую за первой обратной косой чертой.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>пасфиндонпас</strong></a><br /> | Выполняет поиск файла.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>пасфиндсуффиксаррай</strong></a><br /> | Определяет, имеет ли заданное имя файла один из списков суффиксов.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>пасжетаргс</strong></a><br /> | Находит аргументы командной строки в заданном пути.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>пасжетчартипе</strong></a><br /> | Определяет тип символа относительно пути.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>пасжетдривенумбер</strong></a><br /> | Ищет в пути букву диска в диапазоне от "A" до "Z" и возвращает соответствующий номер диска.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>пасисконтенттипе</strong></a><br /> | Определяет, соответствует ли зарегистрированный тип содержимого файла указанному типу содержимого. Эта функция получает тип содержимого для указанного типа файла и сравнивает эту строку с <em>псзконтенттипе</em>. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>пасисдиректори</strong></a><br /> | Проверяет, является ли путь допустимым каталогом.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>пасисдиректоремпти</strong></a><br /> | Определяет, является ли указанный путь пустым каталогом.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>пасисфилеспек</strong></a><br /> | Выполняет поиск в пути любых символов, разделяющих путь (например, ":" или " \' ). Если нет символов, разделяющих пути, путь считается путем к файлу спецификации файла.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>пасиштмлфиле</strong></a><br /> | Определяет, является ли файл HTML-файлом. Определение устанавливается на основе типа содержимого, зарегистрированного для расширения файла.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>пасислфнфилеспек</strong></a><br /> | Определяет, имеет ли имя файла полный формат.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>пасиснетворкпас</strong></a><br /> | Определяет, представляет ли строка пути сетевой ресурс.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>пасиспрефикс</strong></a><br /> | Выполняет поиск по пути, чтобы определить, содержит ли он допустимый префикс типа, переданного <em>псзпрефикс</em>. Префикс имеет один из следующих типов: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>пасисрелативе</strong></a><br /> | Выполняет поиск по пути и определяет, является ли он относительным.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>пасисрут</strong></a><br /> | Определяет, относится ли строка пути к корню тома.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>пасиссамерут</strong></a><br /> | Сравнивает два пути, чтобы определить, имеют ли они общий корневой компонент.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>пасиссистемфолдер</strong></a><br /> | Определяет, содержит ли существующая папка атрибуты, которые делают ее системной папкой. Кроме того, эта функция указывает, должны ли определенные атрибуты определить папку как системную папку.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>пасисунк</strong></a><br /> | Определяет, является ли строка пути допустимым UNC-путем (в отличие от пути, основанного на букве диска).<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>пасисунксервер</strong></a><br /> | Определяет, является ли строка допустимым UNC-именем только для пути сервера.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>пасисунксервершаре</strong></a><br /> | Определяет, является ли строка допустимым UNC-путем к общему ресурсу на \\ <em>сервере</em> \<em> </em> .<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>пасисурл</strong></a><br /> | Проверяет заданную строку, чтобы определить, соответствует ли она допустимому формату URL-адреса.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>пасмакепретти</strong></a><br /> | Преобразует путь все прописные буквы в символы нижнего регистра, чтобы обеспечить единообразный внешний вид.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>пасмакесистемфолдер</strong></a><br /> | Предоставляет существующей папке правильные атрибуты для того, чтобы стать системной папкой.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>пасматчспек</strong></a><br /> | Выполняет поиск строки, используя тип совпадения с подстановочным знаком MS-DOS.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>пасматчспецекс</strong></a><br /> | Сопоставляет имя файла из пути с одним или несколькими шаблонами имен файлов.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>паспарсеиконлокатион</strong></a><br /> | Анализирует строку расположения файла, содержащую расположение файла и индекс значка, и возвращает отдельные значения.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>паскуотеспацес</strong></a><br /> | Поиск пробелов в пути. Если найдены пробелы, весь путь заключается в кавычки.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>пасрелативепасто</strong></a><br /> | Создает относительный путь от одного файла или папки к другому.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>пасремовеаргс</strong></a><br /> | Удаляет все аргументы из заданного пути.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>пасремовебаккслаш</strong></a><br /> | Удаляет замыкающую обратную косую черту из заданного пути.<br /><blockquote>[!Note]<br />Эта функция является устаревшей. Мы рекомендуем использовать функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>паскчремовебаккслаш</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>паскчремовебаккслашекс</strong></a> на своем месте.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>пасремовебланкс</strong></a><br /> | Удаляет все начальные и конечные пробелы из строки.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>пасремовикстенсион</strong></a><br /> | Удаляет расширение имени файла из пути, если он имеется. <br /><blockquote>[!Note]<br />Эта функция является устаревшей. Мы рекомендуем использовать <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>паскчремовикстенсион</strong></a> на своем месте.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>пасремовефилеспек</strong></a><br /> | Удаляет завершающее имя файла и обратную косую черту из пути, если они есть.<br /><blockquote>[!Note]<br />Эта функция является устаревшей. Мы рекомендуем использовать функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>паскчремовефилеспек</strong></a> на своем месте.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>пасренамикстенсион</strong></a><br /> | Заменяет расширение имени файла новым расширением. Если имя файла не содержит расширение, расширение будет присоединено к концу строки.<br /><blockquote>[!Note]<br />Неправильное использование этой функции может привести к переполнению буфера. Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>паскчренамикстенсион</strong></a> на своем месте.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>пассеарчандкуалифи</strong></a><br /> | Определяет, является ли данный путь правильно отформатированным и полным.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>пассетдлгитемпас</strong></a><br /> | Задает текст дочернего элемента управления в окне или диалоговом окне с помощью <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>паскомпактпас</strong></a> , чтобы гарантировать, что путь умещается в элементе управления.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>пасскипрут</strong></a><br /> | Извлекает указатель на первый символ в пути после буквы диска или UNC-сервера или пути к общей папке.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>пасстриппас</strong></a><br /> | Удаляет часть пути к полному пути и файлу.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>пасстрипторут</strong></a><br /> | Удаляет все элементы File и Directory в пути, за исключением корневой информации.<br /><blockquote>[!Note]<br />Неправильное использование этой функции может привести к переполнению буфера. Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>паскчстрипторут</strong></a> на своем месте.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>пасундекорате</strong></a><br /> | Удаляет Оформление из строки пути.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>пасунекспанденвстрингс</strong></a><br /> | Заменяет определенные имена папок в полном пути на соответствующую строку среды.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>пасунмакесистемфолдер</strong></a><br /> | Удаляет атрибуты из папки, сделав ее системной папкой. На самом деле эта папка должна существовать в файловой системе.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>пасункуотеспацес</strong></a><br /> | Удаляет кавычки с начала и с конца пути.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>шскипжунктион</strong></a><br /> | Проверяет контекст привязки, чтобы проверить, является ли он ненадежным для привязки к конкретному объекту компонента.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>урлапплисчеме</strong></a><br /> | Определяет схему для указанной строки URL-адреса и возвращает строку с соответствующим префиксом.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>урлканоникализе</strong></a><br /> | Преобразует строку URL-адреса в каноническую форму.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>урлкомбине</strong></a><br /> | При указании с относительным URL-адресом и его базой, возвращает URL-адрес в канонической форме.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>урлкомпаре</strong></a><br /> | Выполняет сравнение с учетом регистра двух строк URL-адреса.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>урлкреатефромпас</strong></a><br /> | Преобразует путь MS-DOS в канонический URL-адрес.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>урлескапе</strong></a><br /> | Преобразует символы или суррогатные пары в URL-адресе, который может быть изменен во время передачи через Интернет («ненадежные» символы) в соответствующие управляющие последовательности. Суррогатные пары — это символы между U + 10000 и U + 10FFFF (в UTF-32) или между DC00 и DFFF (в UTF-16). <br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>урлескапеспацес</strong></a><br /> | Макрос, который преобразует символы пробела в соответствующую escape-последовательность.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>урлжетлокатион</strong></a><br /> | Извлекает расположение из URL-адреса.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>урлжетпарт</strong></a><br /> | Принимает строку URL-адреса и возвращает указанную часть этого URL-адреса.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>урлхаш</strong></a><br /> | Хэширует строку URL-адреса.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>урлис</strong></a><br /> | Проверяет, имеет ли URL-адрес указанный тип.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>урлисфилеурл</strong></a><br /> | Проверяет URL-адрес, чтобы определить, является ли он URL-адресом файла.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>урлиснохистори</strong></a><br /> | Возвращает значение, указывающее, является ли URL-адрес URL, который обычно не включается в журнал навигации.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>урлисопакуе</strong></a><br /> | Возвращает значение, указывающее, является ли URL-адрес непрозрачным.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>урлунескапе</strong></a><br /> | Преобразует escape-последовательности обратно в обычные символы.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>урлунескапеинплаце</strong></a><br /> | Преобразует escape-последовательности обратно в обычные символы и перезаписывает исходную строку.<br /> | 




 

 

 




