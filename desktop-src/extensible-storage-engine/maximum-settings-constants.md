---
description: Дополнительные сведения о параметрах максимальной константы параметров
title: Максимальные константы параметров
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897658"
---
# <a name="maximum-settings-constants"></a>Максимальные константы параметров


_**Применимо к:** Windows | Windows Server_

## <a name="maximum-settings-constants"></a>Максимальные константы параметров

Эти константы предоставляют максимальные параметры, разрешенные для элементов в базе данных ESE.

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
<td><p>JET_BASE_NAME_LENGTH<br />
3</p></td>
<td><p>Задает длину префикса, используемого для имен файлов, используемых ядром СУБД. Эта длина применима к имени, заданному для параметра системы <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_MAX_COMPUTERNAME_LENGTH<br />
15</p></td>
<td><p>Задает максимальную длину для <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbBookmarkMost<br />
256</p></td>
<td><p>Максимальный размер закладки по умолчанию. Это допустимо, если размер ключа остался равным значению по умолчанию.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbBookmarkMostMost<br />
2000</p></td>
<td><p>Максимальный размер закладки, если для ESENT настроено максимально возможное количество ключей.</p>
<p><strong>Windows 7:</strong> JET_cbBookmarkMostMost введен в Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbNameMost<br />
64</p></td>
<td><p>Максимальная длина имени объекта, столбца, индекса или свойства.</p>
<p><strong>Примечание</strong>  .  Если Unicode, значение равно 128.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbFullNameMost<br />
255</p></td>
<td><p>Максимальная длина &quot; конструкции Name.Name.Name... &quot;</p>
<p><strong>Примечание</strong>  .  Если Unicode, значение равно 510.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbColumnLVPageOverhead<br />
82</p></td>
<td><p>Этот номер можно использовать для расчета максимального объема большого двоичного объекта, который может храниться ядром СУБД на одной странице базы данных. Формула имеет максимальный размер = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</p>
<p>Теперь это значение устарело. Размер фрагмента данных с длинным значением должен быть получен с помощью параметра JET_paramLVChunkSizeMost.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbColumnMost<br />
255</p></td>
<td><p>Максимальный размер данных в столбцах, не являющихся значениями типа long.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbLVDefaultValueMost<br />
255</p></td>
<td><p>Максимальный размер значения по умолчанию для столбца длинных значений (Лонгбинари или LongText).</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost<br />
255</p></td>
<td><p>Максимальный размер ключа сортировки или индекса по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMost<br />
2000</p></td>
<td><p>Максимальный настраиваемый размер ключа сортировки или индекса для любого размера страницы. (См. JET_INDEXCREATE2. Кбкэймост)</p>
<p><strong>Windows 7:</strong> JET_cbKeyMostMost введены в операционной системе Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost2KBytePage<br />
500</p></td>
<td><p>Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 2048 байт. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage представлен в операционной системе Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMost4KBytePage<br />
1000</p></td>
<td><p>Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 4096 байт. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage введен в Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost8KBytePage<br />
2000</p></td>
<td><p>Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 8192 байт. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage появился в Windows Vista</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMin<br />
255</p></td>
<td><p>Минимальный допустимый максимальный размер ключа индекса. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMostMin введен в Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbLimitKeyMost<br />
256</p></td>
<td><p>Максимальный размер ключа при формировании ключа с помощью ограничения <em>грбит</em>, например JET_bitStrLimit, которое используется в функции <a href="gg269329(v=exchg.10).md">жетмакекэй</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbPrimaryKeyMost<br />
255</p></td>
<td><p>Максимальный размер первичного индекса. Эта возможность устарела.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbSecondaryKeyMost<br />
255</p></td>
<td><p>Максимальный размер вторичного индекса. Эта возможность устарела.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolKeyMost<br />
12</p></td>
<td><p>Максимальное число компонентов в ключе сортировки или индекса.</p>
<p><strong>Windows Vista:  </strong> В Windows Vista и более поздних версиях Windows значение равно 16.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolMost<br />
0x0000fee0</p></td>
<td><p>Максимально допустимое число столбцов в таблице.</p>
<p><strong>Windows XP:  </strong> Значение 0x0000fee0 используется в Windows XP и более поздних версий и более поздних версиях Windows.</p>
<p><strong>Windows 2000:  </strong> Значение 0x00007ffe используется в Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolFixedMost<br />
0x0000007F</p></td>
<td><p>Максимальное число фиксированных столбцов, разрешенное в таблице, в настоящее время 127.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolVarMost<br />
0x00000080</p></td>
<td><p>Максимальное число столбцов переменной длины, которые могут содержаться в таблице, в настоящее время 128.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolTaggedMost<br />
(JET_ccolMost-0x000000ff)</p></td>
<td><p>Максимальное число столбцов с тегами, которые могут содержаться в таблице, в настоящее время 64993.</p></td>
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

