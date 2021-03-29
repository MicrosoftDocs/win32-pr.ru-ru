---
description: 'Дополнительные сведения о: JET_ENUMCOLUMN свойствах'
title: Свойства JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 69d0822e12078a7990615ebd401fb63e474a389e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897301"
---
# <a name="jet_enumcolumn-properties"></a>Свойства JET_ENUMCOLUMN

Включить защищенные члены  
Включить унаследованные члены  

Тип [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) предоставляет следующие члены.

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
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Возвращает размер значения, перечисленного для столбца. Этот элемент используется, только если <a href="dn335086(v=exchg.10).md">Err</a> равен <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">ценумколумнвалуе</a></td>
<td>Возвращает количество значений столбца, перечисленных для столбца. Этот элемент используется только в том случае, если <a href="dn335086(v=exchg.10).md">Err</a> не <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">columnid</a></td>
<td>Возвращает идентификатор columnid, который был перечислен.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">Err</a></td>
<td>Возвращает код состояния столбца, полученный в результате перечисления.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">пвдата</a></td>
<td>Возвращает значение, перечисленное для столбца. Этот элемент используется, только если <a href="dn335086(v=exchg.10).md">Err</a> равен <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a>. Это указывает на память, выделенную с помощью обратного вызова <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> распределителя, переданного в <a href="dn292148(v=exchg.10).md">жетенумератеколумнс (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, енумератеколумнсгрбит)</a>. Не забудьте освободить память по завершении.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">рженумколумнвалуе</a></td>
<td>Возвращает перечисляемые значения столбцов для столбца. Этот элемент используется только в том случае, если <a href="dn335086(v=exchg.10).md">Err</a> не <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a>.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
