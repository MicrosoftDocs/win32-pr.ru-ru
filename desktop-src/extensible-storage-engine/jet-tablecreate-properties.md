---
description: 'Дополнительные сведения о: JET_TABLECREATE свойствах'
title: Свойства JET_TABLECREATE
TOCTitle: JET_TABLECREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_TABLECREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103995
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2c79440fa5e04acefe54ed271460d6bd11bc57fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081595"
---
# <a name="jet_tablecreate-properties"></a>Свойства JET_TABLECREATE

Включить защищенные члены  
Включить унаследованные члены  

Тип [JET_TABLECREATE](./jet-tablecreate-class.md) предоставляет следующие члены.

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
<td><a href="dn351077(v=exchg.10).md">кбсепарателв</a></td>
<td>Возвращает или задает размер эвристики для отделения встроенной функции LV от основной записи.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351078(v=exchg.10).md">кбтип</a></td>
<td>Возвращает или задает тип функции обратного вызова.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351080(v=exchg.10).md">кколумнс</a></td>
<td>Возвращает или задает число создаваемых столбцов.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351079(v=exchg.10).md">ккреатед</a></td>
<td>Возвращает или задает число созданных объектов (столбцы + таблица + индексы + обратные вызовы).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351081(v=exchg.10).md">Циндексес</a></td>
<td>Возвращает или задает количество создаваемых индексов.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351082(v=exchg.10).md">грбит</a></td>
<td>Возвращает или задает параметры таблицы.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351087(v=exchg.10).md">плвспацехинтс</a></td>
<td>Возвращает или задает размещение, Обслуживание и указания по использованию для разделенного дерева LV типа <a href="dn351095(v=exchg.10).md">JET_SPACEHINTS</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351083(v=exchg.10).md">псекспацехинтс</a></td>
<td>Возвращает или задает размещение, Обслуживание и указания по использованию для последовательного индекса по умолчанию.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351086(v=exchg.10).md">ргколумнкреате</a></td>
<td>Возвращает или задает массив сведений о создании столбца типа <a href="dn335028(v=exchg.10).md">JET_COLUMNCREATE</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351089(v=exchg.10).md">ргиндекскреате</a></td>
<td>Возвращает или задает массив создаваемых индексов типа <a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351090(v=exchg.10).md">сзкаллбакк</a></td>
<td>Возвращает или задает функцию обратного вызова, используемую для таблицы. Это в форме &quot; module! FunctionName &quot; , и в нем предполагается неуправляемый код. В качестве альтернативы см. <strong>жетрегистеркаллбакк (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</strong> .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351092(v=exchg.10).md">сзтабленаме</a></td>
<td>Возвращает или задает имя создаваемой таблицы.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351093(v=exchg.10).md">сзтемплатетабленаме</a></td>
<td>Возвращает или задает имя таблицы, из которой наследуется базовый DDL.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351099(v=exchg.10).md">TableID</a></td>
<td>Возвращает или задает возвращенный табледид.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351101(v=exchg.10).md">улденсити</a></td>
<td>Возвращает или задает плотность таблицы.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351102(v=exchg.10).md">улпажес</a></td>
<td>Возвращает или задает начальные страницы, выделяемые для таблицы.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_TABLECREATE](./jet-tablecreate-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
