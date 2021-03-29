---
description: В этом разделе описываются функции обработки пути оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.
title: Функции обработки пути оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997903"
---
# <a name="shell-path-handling-functions"></a>Функции обработки пути оболочки

В этом разделе описываются функции обработки пути оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>пасаддбаккслаш</strong></a><br/></td>
<td>Добавляет обратную косую черту в конец строки, чтобы создать правильный синтаксис для пути. Если в исходном пути уже есть обратная косая черта, обратная косая черта не добавляется. <br/>
<blockquote>
[!Note]<br />
Неправильное использование этой функции может привести к переполнению буфера. На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>паскчаддбаккслаш</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>паскчаддбаккслашекс</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>пасаддекстенсион</strong></a><br/></td>
<td>Добавляет расширение имени файла в строку пути.<br/>
<blockquote>
[!Note]<br />
Неправильное использование этой функции может привести к переполнению буфера. Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>паскчаддекстенсион</strong></a> на своем месте.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>пасаппенд</strong></a><br/></td>
<td>Добавляет один путь к концу другого. <br/>
<blockquote>
[!Note]<br />
Неправильное использование этой функции может привести к переполнению буфера. На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>паскчаппенд</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>паскчаппендекс</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>пасбуилдрут</strong></a><br/></td>
<td>Создает корневой путь из заданного номера диска.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>пасканоникализе</strong></a><br/></td>
<td>Упрощает путь путем удаления элементов навигации, таких как &quot; . &quot; и &quot; .. &quot; , для создания прямого, правильно сформированного пути.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>паскомбине</strong></a><br/></td>
<td>Объединяет две строки, представляющие правильно сформированные пути, в один путь. также сцепляет все элементы относительного пути. <br/>
<blockquote>
[!Note]<br />
Неправильное использование этой функции может привести к переполнению буфера. На своем месте рекомендуется использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>паскчкомбине</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>паскчкомбиникс</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>паскоммонпрефикс</strong></a><br/></td>
<td>Сравнивает два пути, чтобы определить, имеют ли они общий префикс. Префикс имеет один из следующих типов: &quot; C: \\ &quot; , &quot; ., &quot; . &quot; . &quot; , &quot; .. \\ &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>паскомпактпас</strong></a><br/></td>
<td>Усекает путь к файлу в соответствии с заданной шириной в пикселях, заменяя компоненты пути многоточием.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>паскомпактпасекс</strong></a><br/></td>
<td>Усекает путь, чтобы он поместился в определенное число символов, заменяя компоненты пути многоточием.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>паскреатефромурл</strong></a><br/></td>
<td>Преобразует URL-адрес файла в путь Microsoft MS-DOS.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>паскреатефромурлаллок</strong></a><br/></td>
<td>Создает путь из URL-адреса файла.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>пасфиликсистс</strong></a><br/></td>
<td>Определяет, является ли допустимым путь к объекту файловой системы, например файлу или папке.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>пасфиндекстенсион</strong></a><br/></td>
<td>Поиск расширения в пути.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>пасфиндфиленаме</strong></a><br/></td>
<td>Поиск имени файла в пути.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>пасфинднексткомпонент</strong></a><br/></td>
<td>Анализирует путь и возвращает часть этого пути, следующую за первой обратной косой чертой.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>пасфиндонпас</strong></a><br/></td>
<td>Выполняет поиск файла.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>пасфиндсуффиксаррай</strong></a><br/></td>
<td>Определяет, имеет ли заданное имя файла один из списков суффиксов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>пасжетаргс</strong></a><br/></td>
<td>Находит аргументы командной строки в заданном пути.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>пасжетчартипе</strong></a><br/></td>
<td>Определяет тип символа относительно пути.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>пасжетдривенумбер</strong></a><br/></td>
<td>Ищет в пути букву диска в диапазоне от "A" до "Z" и возвращает соответствующий номер диска.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>пасисконтенттипе</strong></a><br/></td>
<td>Определяет, соответствует ли зарегистрированный тип содержимого файла указанному типу содержимого. Эта функция получает тип содержимого для указанного типа файла и сравнивает эту строку с <em>псзконтенттипе</em>. Сравнение выполняется без учета регистра.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>пасисдиректори</strong></a><br/></td>
<td>Проверяет, является ли путь допустимым каталогом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>пасисдиректоремпти</strong></a><br/></td>
<td>Определяет, является ли указанный путь пустым каталогом.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>пасисфилеспек</strong></a><br/></td>
<td>Выполняет поиск в пути любых символов, разделяющих путь (например, ":" или " \' ). Если нет символов, разделяющих пути, путь считается путем к файлу спецификации файла.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>пасиштмлфиле</strong></a><br/></td>
<td>Определяет, является ли файл HTML-файлом. Определение устанавливается на основе типа содержимого, зарегистрированного для расширения файла.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>пасислфнфилеспек</strong></a><br/></td>
<td>Определяет, имеет ли имя файла полный формат.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>пасиснетворкпас</strong></a><br/></td>
<td>Определяет, представляет ли строка пути сетевой ресурс.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>пасиспрефикс</strong></a><br/></td>
<td>Выполняет поиск по пути, чтобы определить, содержит ли он допустимый префикс типа, переданного <em>псзпрефикс</em>. Префикс имеет один из следующих типов: &quot; C: \\ &quot; , &quot; ., &quot; . &quot; . &quot; , &quot; .. \\ &quot; .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>пасисрелативе</strong></a><br/></td>
<td>Выполняет поиск по пути и определяет, является ли он относительным.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>пасисрут</strong></a><br/></td>
<td>Определяет, относится ли строка пути к корню тома.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>пасиссамерут</strong></a><br/></td>
<td>Сравнивает два пути, чтобы определить, имеют ли они общий корневой компонент.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>пасиссистемфолдер</strong></a><br/></td>
<td>Определяет, содержит ли существующая папка атрибуты, которые делают ее системной папкой. Кроме того, эта функция указывает, должны ли определенные атрибуты определить папку как системную папку.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>пасисунк</strong></a><br/></td>
<td>Определяет, является ли строка пути допустимым UNC-путем (в отличие от пути, основанного на букве диска).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>пасисунксервер</strong></a><br/></td>
<td>Определяет, является ли строка допустимым UNC-именем только для пути сервера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>пасисунксервершаре</strong></a><br/></td>
<td>Определяет, является ли строка допустимым UNC-путем к общему ресурсу на \\ <em>сервере</em> \ <em></em>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>пасисурл</strong></a><br/></td>
<td>Проверяет заданную строку, чтобы определить, соответствует ли она допустимому формату URL-адреса.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>пасмакепретти</strong></a><br/></td>
<td>Преобразует путь все прописные буквы в символы нижнего регистра, чтобы обеспечить единообразный внешний вид.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>пасмакесистемфолдер</strong></a><br/></td>
<td>Предоставляет существующей папке правильные атрибуты для того, чтобы стать системной папкой.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>пасматчспек</strong></a><br/></td>
<td>Выполняет поиск строки, используя тип совпадения с подстановочным знаком MS-DOS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>пасматчспецекс</strong></a><br/></td>
<td>Сопоставляет имя файла из пути с одним или несколькими шаблонами имен файлов.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>паспарсеиконлокатион</strong></a><br/></td>
<td>Анализирует строку расположения файла, содержащую расположение файла и индекс значка, и возвращает отдельные значения.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>паскуотеспацес</strong></a><br/></td>
<td>Поиск пробелов в пути. Если найдены пробелы, весь путь заключается в кавычки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>пасрелативепасто</strong></a><br/></td>
<td>Создает относительный путь от одного файла или папки к другому.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>пасремовеаргс</strong></a><br/></td>
<td>Удаляет все аргументы из заданного пути.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>пасремовебаккслаш</strong></a><br/></td>
<td>Удаляет замыкающую обратную косую черту из заданного пути.<br/>
<blockquote>
[!Note]<br />
Эта функция является устаревшей. Мы рекомендуем использовать функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>паскчремовебаккслаш</strong></a> или <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>паскчремовебаккслашекс</strong></a> на своем месте.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>пасремовебланкс</strong></a><br/></td>
<td>Удаляет все начальные и конечные пробелы из строки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>пасремовикстенсион</strong></a><br/></td>
<td>Удаляет расширение имени файла из пути, если он имеется. <br/>
<blockquote>
[!Note]<br />
Эта функция является устаревшей. Мы рекомендуем использовать <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>паскчремовикстенсион</strong></a> на своем месте.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>пасремовефилеспек</strong></a><br/></td>
<td>Удаляет завершающее имя файла и обратную косую черту из пути, если они есть.<br/>
<blockquote>
[!Note]<br />
Эта функция является устаревшей. Мы рекомендуем использовать функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>паскчремовефилеспек</strong></a> на своем месте.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>пасренамикстенсион</strong></a><br/></td>
<td>Заменяет расширение имени файла новым расширением. Если имя файла не содержит расширение, расширение будет присоединено к концу строки.<br/>
<blockquote>
[!Note]<br />
Неправильное использование этой функции может привести к переполнению буфера. Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>паскчренамикстенсион</strong></a> на своем месте.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>пассеарчандкуалифи</strong></a><br/></td>
<td>Определяет, является ли данный путь правильно отформатированным и полным.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>пассетдлгитемпас</strong></a><br/></td>
<td>Задает текст дочернего элемента управления в окне или диалоговом окне с помощью <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>паскомпактпас</strong></a> , чтобы гарантировать, что путь умещается в элементе управления.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>пасскипрут</strong></a><br/></td>
<td>Извлекает указатель на первый символ в пути после буквы диска или UNC-сервера или пути к общей папке.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>пасстриппас</strong></a><br/></td>
<td>Удаляет часть пути к полному пути и файлу.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>пасстрипторут</strong></a><br/></td>
<td>Удаляет все элементы File и Directory в пути, за исключением корневой информации.<br/>
<blockquote>
[!Note]<br />
Неправильное использование этой функции может привести к переполнению буфера. Мы рекомендуем использовать более безопасную функцию <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>паскчстрипторут</strong></a> на своем месте.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>пасундекорате</strong></a><br/></td>
<td>Удаляет Оформление из строки пути.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>пасунекспанденвстрингс</strong></a><br/></td>
<td>Заменяет определенные имена папок в полном пути на соответствующую строку среды.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>пасунмакесистемфолдер</strong></a><br/></td>
<td>Удаляет атрибуты из папки, сделав ее системной папкой. На самом деле эта папка должна существовать в файловой системе.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>пасункуотеспацес</strong></a><br/></td>
<td>Удаляет кавычки с начала и с конца пути.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>шскипжунктион</strong></a><br/></td>
<td>Проверяет контекст привязки, чтобы проверить, является ли он ненадежным для привязки к конкретному объекту компонента.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>урлапплисчеме</strong></a><br/></td>
<td>Определяет схему для указанной строки URL-адреса и возвращает строку с соответствующим префиксом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>урлканоникализе</strong></a><br/></td>
<td>Преобразует строку URL-адреса в каноническую форму.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>урлкомбине</strong></a><br/></td>
<td>При указании с относительным URL-адресом и его базой, возвращает URL-адрес в канонической форме.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>урлкомпаре</strong></a><br/></td>
<td>Выполняет сравнение с учетом регистра двух строк URL-адреса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>урлкреатефромпас</strong></a><br/></td>
<td>Преобразует путь MS-DOS в канонический URL-адрес.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>урлескапе</strong></a><br/></td>
<td>Преобразует символы или суррогатные пары в URL-адресе, который может быть изменен во время передачи через Интернет ( &quot; ненадежные &quot; символы) в соответствующие управляющие последовательности. Суррогатные пары — это символы между U + 10000 и U + 10FFFF (в UTF-32) или между DC00 и DFFF (в UTF-16). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>урлескапеспацес</strong></a><br/></td>
<td>Макрос, который преобразует символы пробела в соответствующую escape-последовательность.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>урлжетлокатион</strong></a><br/></td>
<td>Извлекает расположение из URL-адреса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>урлжетпарт</strong></a><br/></td>
<td>Принимает строку URL-адреса и возвращает указанную часть этого URL-адреса.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>урлхаш</strong></a><br/></td>
<td>Хэширует строку URL-адреса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>урлис</strong></a><br/></td>
<td>Проверяет, имеет ли URL-адрес указанный тип.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>урлисфилеурл</strong></a><br/></td>
<td>Проверяет URL-адрес, чтобы определить, является ли он URL-адресом файла.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>урлиснохистори</strong></a><br/></td>
<td>Возвращает значение, указывающее, является ли URL-адрес URL, который обычно не включается в журнал навигации.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>урлисопакуе</strong></a><br/></td>
<td>Возвращает значение, указывающее, является ли URL-адрес непрозрачным.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>урлунескапе</strong></a><br/></td>
<td>Преобразует escape-последовательности обратно в обычные символы.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>урлунескапеинплаце</strong></a><br/></td>
<td>Преобразует escape-последовательности обратно в обычные символы и перезаписывает исходную строку.<br/></td>
</tr>
</tbody>
</table>



 

 

 




