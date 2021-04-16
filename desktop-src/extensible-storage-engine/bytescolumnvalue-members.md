---
description: 'Дополнительные сведения о: Битесколумнвалуе Members'
title: Элементы Битесколумнвалуе
TOCTitle: BytesColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55100914
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 81a408503b46d98e3140af6aa2aff638f2fb0ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563656"
---
# <a name="bytescolumnvalue-members"></a>Элементы Битесколумнвалуе

Включить защищенные члены  
Включить унаследованные члены  

Значение столбца массива байтов.

Тип [битесколумнвалуе](./bytescolumnvalue-class.md) предоставляет следующие члены.

## <a name="constructors"></a>Конструкторы

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn334168(v=exchg.10).md">битесколумнвалуе</a></td>
<td></td>
</tr>
</tbody>
</table>


Начало

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
<td><a href="dn334126(v=exchg.10).md">Длина</a></td>
<td>Возвращает длину в байтах значения столбца, равного нулю, если столбец имеет значение null, в противном случае соответствует фактической длине массива байтов. (Переопределяет <a href="dn334213(v=exchg.10).md">колумнвалуе. length</a>.)</td>
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
<td><a href="dn334176(v=exchg.10).md">Размер</a></td>
<td>Возвращает размер значения в столбце. Он возвращает 0 для столбцов переменного размера (т. е. двоичного и строкового). (Переопределяет <a href="dn334172(v=exchg.10).md">колумнвалуе. size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334129(v=exchg.10).md">Значение</a></td>
<td>Возвращает или задает значение столбца. Используйте <a href="dn334138(v=exchg.10).md">SetColumns (JET_SESID, JET_TABLEID, [])</a> для обновления записи со значением столбца.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334177(v=exchg.10).md">валуеасобжект</a></td>
<td>Возвращает последнее набор или полученное значение столбца. Значение возвращается в виде универсального объекта. (Переопределяет <a href="dn334214(v=exchg.10).md">колумнвалуе. валуеасобжект</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="methods"></a>Методы

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn334173(v=exchg.10).md">жетвалуефромбитес</a></td>
<td>Данные, полученные из ESENT, декодируются и задают значение в объекте Колумнвалуе. (Переопределяет <a href="dn334208(v=exchg.10).md">колумнвалуе. жетвалуефромбитес ([], Int32, Int32, Int32)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn334124(v=exchg.10).md">ToString</a></td>
<td>Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn334170(v=exchg.10).md">битесколумнвалуе</a>. (Переопределяет <a href="dn334163(v=exchg.10).md">колумнвалуе. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Битесколумнвалуе](./bytescolumnvalue-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
