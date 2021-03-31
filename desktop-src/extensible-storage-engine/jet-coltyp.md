---
description: 'Дополнительные сведения: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912683"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Применимо к:** Windows | Windows Server_

## <a name="jet_coltyp"></a>JET_COLTYP

**JET_COLTYP** группа констант описывает все возможные типы столбцов, которые можно найти в таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа/значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_coltypNil<br />
0</p></td>
<td><p>Недопустимый тип столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBit<br />
1</p></td>
<td><p>Тип столбца, допускающий три значения: <strong>true</strong>, <strong>false</strong>или <strong>null</strong>. Этот тип столбца имеет длину один байт и имеет фиксированный размер. <strong>Значение false</strong> сортирует до <strong>true</strong>. Обратите внимание, что размер этого типа не соответствует размеру логического типа Variant.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedByte<br />
2</p></td>
<td><p>1-байтовое целое число без знака, которое может принимать значения от 0 (ноль) до 255.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypShort<br />
3</p></td>
<td><p>2-байтовое целое число со знаком, которое может принимать значения от-32768 до 32767. Отрицательные значения сортируются перед положительными значениями.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLong<br />
4</p></td>
<td><p>4-байтовое целое число со знаком, которое может принимать значения от-2147483648 до 2147483647. Отрицательные значения сортируются перед положительными значениями.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypCurrency<br />
5</p></td>
<td><p>8-байтовое целое число со знаком, которое может принимать значения от-9223372036854775808 до 9223372036854775807. Отрицательные значения сортируются перед положительными значениями. Этот тип столбца идентичен типу денежной единицы типа Variant. Этот тип столбца также может использоваться в качестве собственного 8-байтового целого числа со знаком.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypIEEESingle<br />
6</p></td>
<td><p>Число с плавающей запятой одиночной точности (4 байта).</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypIEEEDouble<br />
7</p></td>
<td><p>Число с плавающей запятой двойной точности (8 байт).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypDateTime<br />
8</p></td>
<td><p>Число с плавающей запятой двойной точности (8 байт), представляющее дату в дробных днях, начиная с 1900 года. Этот тип столбца идентичен типу Variant типа Date.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBinary<br />
9</p></td>
<td><p>Двоичный столбец фиксированной или переменной длины, который может иметь длину до 255 байт.</p>
<p>Этот тип столбца можно использовать для реализации GUID, если он настроен в виде двоичного столбца фиксированной длины (16 байт). Единственное предостережение заключается в том, что относительный порядок значений в индексе по такому столбцу не будет совпадать с относительным порядком стандартного отображения строки реестра (т &quot; . е. {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypText<br />
10</p></td>
<td><p>Фиксированный или переменный текстовый столбец длиной до 255 символов ASCII длиной или 127 символов Юникода в длину.</p>
<p>Все строки хранятся в виде подсчитанного количества символов. Строки не должны завершаться нулем. Кроме того, для счетчика не нужно включать терминатор null. Наконец, можно хранить внедренные символы NULL.</p>
<p>Строки ASCII всегда обрабатываются как нечувствительные к регистру в целях сортировки и поиска. Кроме того, для сортировки и поиска учитываются только символы, предшествующие первому символу null (если таковые имеются).</p>
<p>Строки в Юникоде используют API Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString завершилось ошибкой</a> для создания ключей сортировки, которые впоследствии используются для сортировки и поиска этих данных. По умолчанию строки Юникода считаются в языковом стандарте «Английский (США)» и сортируются и ищутся с помощью следующих флагов нормализации: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH. В Windows 2000 можно настроить эти флаги для каждого индекса, чтобы также включить NORM_IGNORENONSPACE. В Windows XP и более поздних версиях можно запросить любое сочетание следующих флагов нормализации на индекс: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH и SORT_STRINGSORT.</p>
<p>Во всех выпусках можно настроить языковой стандарт для каждого индекса. Любой языковой стандарт может использоваться при условии, что на компьютере установлен соответствующий языковой пакет. Наконец, любые символы NULL, обнаруженные в строке Юникода, полностью игнорируются.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongBinary<br />
11</p></td>
<td><p>Двоичный столбец фиксированной или переменной длины, который может иметь длину до 2147483647 байт. Этот тип считается длинным значением. Значение типа long является специальным, так как оно может быть большим и доступно в виде потока. В противном случае этот тип идентичен JET_coltypBinary.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLongText<br />
12</p></td>
<td><p>Столбец с фиксированной или переменной длиной, который может содержать до 2147483647 символов ASCII длиной или 1073741823 символов Юникода в длину. Этот тип считается длинным значением. Значение типа long является специальным, так как оно может быть большим и доступно в виде потока. В противном случае этот тип идентичен JET_coltypText.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypSLV<br />
13</p></td>
<td><p>Этот тип столбца устарел.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedLong<br />
14</p></td>
<td><p>4-байтовое целое число без знака, которое может принимать значения от 0 (ноль) до 4294967295.</p>
<p><strong>Windows Vista и Windows Server 2008:</strong>  Этот тип столбца поддерживается в Windows Vista, Windows Server 2008 и более поздних выпусках.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongLong<br />
15</p></td>
<td><p>8-байтовое целое число со знаком, которое может принимать значения от-9223372036854775808 до 9223372036854775807. Отрицательные значения сортируются перед положительными значениями.</p>
<p><strong>Windows Vista и Windows Server 2008:</strong>  Этот тип столбца поддерживается в Windows Vista, Windows Server 2008 и более поздних выпусках.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypGUID<br />
16</p></td>
<td><p>Двоичный столбец фиксированной длины длиной 16 байт, который изначально представляет тип данных GUID. Значения столбца GUID сортируются так же, как строки в стандартной форме (например, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</p>
<p><strong>Windows Vista и Windows Server 2008:</strong>  Этот тип столбца поддерживается в Windows Vista, Windows Server 2008 и более поздних выпусках.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypUnsignedShort<br />
17</p></td>
<td><p>2-байтовое целое число без знака, которое может принимать значения от 0 до 65535.</p>
<p><strong>Windows Vista и Windows Server 2008:</strong>  Этот тип столбца поддерживается в Windows Vista, Windows Server 2008 и более поздних выпусках.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypMax<br />
18</p></td>
<td><p>Константа, описывающая максимальное значение (то есть одно из более наибольшего допустимого) типа столбца, поддерживаемого ядром.</p>
<p>Это значение следует использовать с осторожностью, так как оно меняется по мере поддержки новых типов столбцов. Например, он имеет другое литеральное значение в Windows 2000, чем в Windows XP и более поздних версиях.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жетаддколумн](./jetaddcolumn-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)
