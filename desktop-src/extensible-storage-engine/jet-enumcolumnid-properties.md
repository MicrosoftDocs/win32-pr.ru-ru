---
description: 'Дополнительные сведения о: JET_ENUMCOLUMNID свойствах'
title: Свойства JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540063"
---
# <a name="jet_enumcolumnid-properties"></a>Свойства JET_ENUMCOLUMNID

Включить защищенные члены  
Включить унаследованные члены  

Тип [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) предоставляет следующие члены.

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
<td><a href="dn335141(v=exchg.10).md">columnid</a></td>
<td>Возвращает или задает идентификатор columnid для перечисления.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ктагсекуенце</a></td>
<td>Возвращает или задает количество значений столбца (по одному индексу) для перечисления по указанному ИДЕНТИФИКАТОРу столбца. Если Ктагсекуенце имеет значение 0 (ноль), то Ргтагсекуенце игнорируется и все значения столбцов для указанного идентификатора столбца будут перечислены.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">ргтагсекуенце</a></td>
<td>Возвращает или задает массив индексов, отсчитываемый от единицы, в массиве значений столбцов для данного столбца. Единственный элемент — это Итагсекуенце, который определен в JET_RETRIEVECOLUMN. Итагсекуенце 0 (ноль) означает &quot; пропуск &quot; . Итагсекуенце 1 означает возврат значения первого столбца столбца, 2 — второй и т. д.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
