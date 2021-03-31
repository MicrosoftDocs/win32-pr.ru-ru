---
description: 'Дополнительные сведения о: JET_RECSIZE свойствах'
title: Свойства JET_RECSIZE (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913563"
---
# <a name="jet_recsize-properties"></a>Свойства JET_RECSIZE

Включить защищенные члены  
Включить унаследованные члены  

Тип [JET_RECSIZE](./jet-recsize-structure2.md) предоставляет следующие члены.

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
<td><a href="hh557581(v=exchg.10).md">cbData</a></td>
<td>Возвращает пользовательский набор данных в записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh596280(v=exchg.10).md">кбдатакомпрессед</a></td>
<td>Возвращает сжатый размер данных пользователя в записи. Это то же самое, что <a href="hh557581(v=exchg.10).md">cbData</a> , если никакие внутренние значения long не сжимаются).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh557913(v=exchg.10).md">кблонгвалуедата</a></td>
<td>Возвращает пользовательский набор данных в записи, но хранится в дереве длинных значений.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh566144(v=exchg.10).md">кблонгвалуедатакомпрессед</a></td>
<td>Возвращает сжатый размер пользовательских данных в дереве длинных значений. Это то же самое, что и <a href="hh557913(v=exchg.10).md">кблонгвалуедата</a> , если не сжаты отдельные длинные значения.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh558003(v=exchg.10).md">кблонгвалуеоверхеад</a></td>
<td>Возвращает дополнительную нагрузку на данные с длинными значениями.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh565836(v=exchg.10).md">кбоверхеад</a></td>
<td>Возвращает дополнительную нагрузку на структуру записи ESENT для этой записи. Сюда входит размер ключа записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh566154(v=exchg.10).md">ккомпресседколумнс</a></td>
<td>Возвращает общее число сжатых столбцов в записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh596288(v=exchg.10).md">клонгвалуес</a></td>
<td>Возвращает общее количество значений long, хранящихся в дереве Long-Value для этой записи. Это не относится к внутренним длинным значениям.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh577486(v=exchg.10).md">кмултивалуес</a></td>
<td>Возвращает совокупное число значений, находящихся за первым для всех столбцов в записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh578172(v=exchg.10).md">кнонтагжедколумнс</a></td>
<td>Возвращает общее число фиксированных и переменных столбцов, заданных в этой записи.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh566034(v=exchg.10).md">ктагжедколумнс</a></td>
<td>Возвращает общее число столбцов с тегами, заданных в этой записи.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_RECSIZE](./jet-recsize-structure2.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
