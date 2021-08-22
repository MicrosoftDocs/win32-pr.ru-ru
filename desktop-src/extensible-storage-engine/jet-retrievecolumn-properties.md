---
description: 'Дополнительные сведения о: JET_RETRIEVECOLUMN свойствах'
title: Свойства JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c1e902b7e79111f3e9d9bf0160880d95c3957804de981fd56bbc36db5a9c3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107348"
---
# <a name="jet_retrievecolumn-properties"></a>Свойства JET_RETRIEVECOLUMN

Включить защищенные члены  
Включить унаследованные члены  

Тип [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) предоставляет следующие члены.

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
<td><a href="dn335226(v=exchg.10).md">кбактуал</a></td>
<td>Возвращает размер данных в байтах, извлекаемый операцией извлечения столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>Возвращает или задает размер буфера <a href="dn351040(v=exchg.10).md">пвдата</a> в байтах. Операция получения столбца не будет хранить больше данных в Пвдата, чем cbData.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">columnid</a></td>
<td>Возвращает или задает идентификатор столбца для извлекаемого столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">колумниднексттагжед</a></td>
<td>Получает значение columnid столбца с тегом, многозначным или разреженным, если все столбцы с тегами извлекаются путем передачи 0 в качестве значения columnid.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">Err</a></td>
<td>Возвращает предупреждение, возвращенное при извлечении столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">грбит</a></td>
<td>Возвращает или задает параметры для извлечения столбца.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ибдата</a></td>
<td>Возвращает или задает смещение в буфере, в котором будут храниться данные.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">иблонгвалуе</a></td>
<td>Возвращает или задает смещение для первого байта, получаемого из столбца типа <a href="hh577895(v=exchg.10).md">лонгбинари</a> или <a href="hh577895(v=exchg.10).md">LongText</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">итагсекуенце</a></td>
<td>Возвращает или задает порядковый номер значений, содержащихся в столбце с несколькими значениями. Если значение Итагсекуенце равно 0, то вместо данных столбца возвращается число экземпляров многозначного столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">пвдата</a></td>
<td>Возвращает или задает буфер, в котором будут храниться данные, извлекаемые из столбца.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
