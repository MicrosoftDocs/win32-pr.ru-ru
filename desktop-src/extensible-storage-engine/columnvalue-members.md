---
description: 'Дополнительные сведения о: Колумнвалуе Members'
title: Элементы Колумнвалуе
TOCTitle: ColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55100951
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f197a18f1ef0f024a51f8d51f00cb269705edcf65ffac713ce91ef416cd9d7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066984"
---
# <a name="columnvalue-members"></a>Элементы Колумнвалуе

Включить защищенные члены  
Включить унаследованные члены  

Базовый класс для объектов, представляющих значение столбца, которое необходимо задать.

Тип [колумнвалуе](./columnvalue-class.md) предоставляет следующие члены.

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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn334207(v=exchg.10).md">колумнвалуе</a></td>
<td>Инициализирует новый экземпляр класса Колумнвалуе.</td>
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
<td>Возвращает или задает значение columnid, которое должно быть задано или получено.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Ошибка</a></td>
<td>Возвращает предупреждение, созданное путем извлечения или установки этого столбца.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">итагсекуенце</a></td>
<td>Возвращает или задает последовательность столбцов итаг.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334213(v=exchg.10).md">Длина</a></td>
<td>Возвращает длину в байтах значения столбца, равного нулю, если столбец имеет значение null, в противном случае он соответствует размеру для столбцов фиксированного размера и представляет фактическую длину байт для столбцов переменного размера (т. е. двоичного и строкового). Для строк длина определяется в предположении 2 байта на символ.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">ретриевегрбит</a></td>
<td>Возвращает или задает параметры извлечения столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">сетгрбит</a></td>
<td>Возвращает или задает параметры обновления столбца.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Защищенное свойство" alt="Protected property" /></td>
<td><a href="dn334172(v=exchg.10).md">Размер</a></td>
<td>Возвращает размер значения в столбце. Он возвращает 0 для столбцов переменного размера (т. е. двоичного и строкового).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn334214(v=exchg.10).md">валуеасобжект</a></td>
<td>Возвращает последнее набор или полученное значение столбца. Значение возвращается в виде универсального объекта.</td>
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
<td><a href="dn334208(v=exchg.10).md">жетвалуефромбитес</a></td>
<td>Данные, полученные из ESENT, декодируются и задают значение в объекте Колумнвалуе.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn334163(v=exchg.10).md">ToString</a></td>
<td>Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn334206(v=exchg.10).md">колумнвалуе</a>. (Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс Колумнвалуе](./columnvalue-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
