---
description: В этом разделе описывается информация о типе календаря (тип данных КАЛТИПЕ), используемая в функциях Енумкалендаринфо, Енумкалендаринфоекс, Енумкалендаринфоексекс, Жеткалендаринфо и GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Сведения о типе календаря
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d59229517143444aa00be9907b7419e0656147ad2fdaacf4aa5cec6e872caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147707"
---
# <a name="calendar-type-information"></a>Сведения о типе календаря

В этом разделе описывается информация о типе календаря (тип данных КАЛТИПЕ), используемая в функциях [**енумкалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**енумкалендаринфоекс**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**енумкалендаринфоексекс**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**жеткалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)и [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) . Некоторые из этих значений также используются функцией [**сеткалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .

Следующие константы КАЛТИПЕ можно использовать в сочетании с любыми другими константами КАЛТИПЕ.



| Константа                     | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAL \_ наусероверриде          | **Windows Me/98, Windows 2000:** Используйте систему по умолчанию вместо выбора пользователя.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| клиентские лицензии \_ возвращают \_ \_ имена женитиве | **Windows 7 и более поздних версий:** Получение результата из [**жеткалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) в виде женитиве названий месяцев, которые являются именами, используемыми при объединении названий месяцев с другими элементами. Например, в украинский эквивалент в январе записывается как «січень», когда месяц называется «только один». Однако если название месяца используется в сочетании, например, в дате, например 5 января 2003, используется женитиве форма имени. Для примера "Украинский" название месяца женитиве отображается как "5 січня 2003". Дополнительные сведения см. в [статье \_ return \_ женитиве \_ names](locale-return-constants.md). |
| \_номер возврата \_ CAL          | **Windows Me/98, Windows 2000:** Получение результата из [**жеткалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) в виде числа, а не строки. Это допустимо только для значений, начинающихся с лицензии CAL \_ I.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CAL \_ использование \_ CP \_ ACP            | **Windows Me/98, Windows 2000:** Используйте системную кодовую страницу ANSI (ACP) вместо кодовой страницы языкового стандарта для перевода строк. Это относится только к версиям функций ANSI, например **енумкалендаринфоа**.                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Следующие константы КАЛТИПЕ являются взаимоисключающими и не могут использоваться в сочетании друг с другом в вызове функции.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAL_ICALINTVALUE</td>
<td>Целочисленное значение, указывающее тип календаря для альтернативного календаря.</td>
</tr>
<tr class="even">
<td>CAL_ITWODIGITYEARMAX</td>
<td><strong>Windows Me/98, Windows 2000:</strong> Целочисленное значение, указывающее верхнюю границу диапазона из двух цифр года.</td>
</tr>
<tr class="odd">
<td>CAL_IYEAROFFSETRANGE</td>
<td>Одна или несколько строк, заканчивающихся нулем, которые задают смещения года для каждого диапазона эры. Последняя строка содержит дополнительный завершающий нуль символ. Это значение зависит от типа необязательного календаря.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME1</td>
<td>Сокращенное собственное имя первого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME2</td>
<td>Сокращенное собственное имя второго дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME3</td>
<td>Сокращенное собственное название третьего дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME4</td>
<td>Сокращенное собственное имя четвертого дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME5</td>
<td>Сокращенное машинное имя пятого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME6</td>
<td>Сокращенное собственное название шестого дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME7</td>
<td>Сокращенное собственное имя седьмого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVERASTRING</td>
<td><strong>Windows 7 и более поздних версий:</strong> Сокращенное машинное имя эры. Полная эра представляется константой CAL_SERASTRING.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME1</td>
<td>Сокращенное собственное имя первого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME2</td>
<td>Сокращенное собственное имя второго месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME3</td>
<td>Сокращенное собственное название третьего месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME4</td>
<td>Сокращенное собственное название четвертого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME5</td>
<td>Сокращенное машинное имя пятого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME6</td>
<td>Сокращенное собственное название шестого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME7</td>
<td>Сокращенное собственное имя седьмого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME8</td>
<td>Сокращенное собственное название восьмого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME9</td>
<td>Сокращенное машинное имя девятого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME10</td>
<td>Сокращенное собственное название десятого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME11</td>
<td>Сокращенное имя в машинном номере одиннадцатого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME12</td>
<td>Сокращенное собственное название двенадцатого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME13</td>
<td>Сокращенное машинное имя тринадцатого месяца года, если оно существует.</td>
</tr>
<tr class="odd">
<td>CAL_SCALNAME</td>
<td>Собственное имя альтернативного календаря.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME1</td>
<td>Собственное имя первого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME2</td>
<td>Собственное имя второго дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME3</td>
<td>Собственное название третьего дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME4</td>
<td>Собственное название четвертого дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME5</td>
<td>Собственное имя пятого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME6</td>
<td>Собственное название шестого дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME7</td>
<td>Собственное название седьмого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SERASTRING</td>
<td>Одна или несколько строк, заканчивающихся нулем, которые задают каждую из кодовых позиций Юникода, указывающих эру, связанную с CAL_IYEAROFFSETRANGE. Последняя строка содержит дополнительный завершающий нуль символ. Это значение зависит от типа необязательного календаря.</td>
</tr>
<tr class="even">
<td>CAL_SLONGDATE</td>
<td>Длинные форматы даты для типа календаря.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHDAY</td>
<td><strong>Windows 7 и более поздних версий:</strong> Формат месяца и дня для типа календаря. Форматирование аналогично форматированию для CAL_SLONGDATE. Например, если шаблон "месяц/день" представляет собой полное название месяца, за которым следует номер дня с начальными нулями, например, &quot; 03 сентября, &quot; то используется формат &quot; мммм дд &quot; . Одинарные кавычки можно использовать для вставки неформатированных символов, например de в испанском.
<blockquote>
[!Note]<br />
Этот тип календаря поддерживает только один формат.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME1</td>
<td>Собственное имя первого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME2</td>
<td>Собственное имя второго месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME3</td>
<td>Собственное название третьего месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME4</td>
<td>Собственное название четвертого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME5</td>
<td>Собственное название пятого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME6</td>
<td>Собственное название шестого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME7</td>
<td>Собственное название седьмого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME8</td>
<td>Собственное название восьмого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME9</td>
<td>Собственное название девятого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME10</td>
<td>Собственное название десятого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME11</td>
<td>Собственное название одиннадцатого месяца года.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME12</td>
<td>Собственное название двенадцатого месяца года.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME13</td>
<td>Собственное имя тринадцатого месяца года, если оно существует.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTDATE</td>
<td>Краткие форматы даты для типа календаря.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME1</td>
<td><strong>Windows Vista и более поздних версий:</strong> Короткое собственное имя первого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME2</td>
<td><strong>Windows Vista и более поздних версий:</strong> Короткое собственное имя второго дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME3</td>
<td><strong>Windows Vista и более поздних версий:</strong> Короткое машинное имя третьего дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME4</td>
<td><strong>Windows Vista и более поздних версий:</strong> Короткое собственное имя четвертого дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME5</td>
<td><strong>Windows Vista и более поздних версий:</strong> Короткое машинное имя пятого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME6</td>
<td><strong>Windows Vista и более поздних версий:</strong> Короткое машинное имя шестого дня недели.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME7</td>
<td><strong>Windows Vista и более поздних версий:</strong> Короткое машинное имя седьмого дня недели.</td>
</tr>
<tr class="odd">
<td>CAL_SYEARMONTH</td>
<td><strong>Windows Me/98, Windows 2000:</strong> Форматы "год/месяц" для указанных календарей.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Если собственное имя дня недели или месяца является пустой строкой, это имя идентично имени, указанному в соответствующей информации о языковых стандартах, и, следовательно, не дублируется здесь.

 

 

 




