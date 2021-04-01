---
description: 'Дополнительные сведения о: Стрингколумнвалуе свойства'
title: Свойства Стрингколумнвалуе
TOCTitle: StringColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.StringColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55104024
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 822e469fae8de69137cbbe7a8e085137c290850a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265114"
---
# <a name="stringcolumnvalue-properties"></a>Свойства Стрингколумнвалуе

Включить защищенные члены  
Включить унаследованные члены  

Тип [стрингколумнвалуе](./stringcolumnvalue-class.md) предоставляет следующие члены.

## <a name="properties"></a>Свойства

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334166(v=exchg.10).md">Columnid</a></td>
<td>Возвращает или задает значение columnid, которое должно быть задано или получено. (Наследуется от <a href="dn334206(v=exchg.10).md">колумнвалуе</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Ошибка</a></td>
<td>Возвращает предупреждение, созданное путем извлечения или установки этого столбца. (Наследуется от <a href="dn334206(v=exchg.10).md">колумнвалуе</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">итагсекуенце</a></td>
<td>Возвращает или задает последовательность столбцов итаг. (Наследуется от <a href="dn334206(v=exchg.10).md">колумнвалуе</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351195(v=exchg.10).md">Длина</a></td>
<td>Возвращает длину в байтах значения столбца, равного нулю, если столбец имеет значение null, в противном случае соответствует длине в байтах строкового значения. Длина байта определяется в соответствии с двумя байтами на символ. (Переопределяет <a href="dn334213(v=exchg.10).md">колумнвалуе. length</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">ретриевегрбит</a></td>
<td>Возвращает или задает параметры извлечения столбца. (Наследуется от <a href="dn334206(v=exchg.10).md">колумнвалуе</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">сетгрбит</a></td>
<td>Возвращает или задает параметры обновления столбца. (Наследуется от <a href="dn334206(v=exchg.10).md">колумнвалуе</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Защищенное свойство" alt="Protected property" /></td>
<td><a href="dn351137(v=exchg.10).md">Размер</a></td>
<td>Возвращает размер значения в столбце. Он возвращает 0 для столбцов переменного размера (т. е. двоичного и строкового). (Переопределяет <a href="dn334172(v=exchg.10).md">колумнвалуе. size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351204(v=exchg.10).md">Значение</a></td>
<td>Возвращает или задает значение столбца. Используйте <a href="dn334138(v=exchg.10).md">SetColumns (JET_SESID, JET_TABLEID, [])</a> для обновления записи со значением столбца.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351202(v=exchg.10).md">валуеасобжект</a></td>
<td>Возвращает последнее набор или полученное значение столбца. Значение возвращается в виде универсального объекта. (Переопределяет <a href="dn334214(v=exchg.10).md">колумнвалуе. валуеасобжект</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Стрингколумнвалуе](./stringcolumnvalue-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
