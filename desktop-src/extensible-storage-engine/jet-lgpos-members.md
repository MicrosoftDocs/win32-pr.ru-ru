---
description: 'Дополнительные сведения о: JET_LGPOS Members'
title: Элементы JET_LGPOS
TOCTitle: JET_LGPOS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_LGPOS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos_members(v=EXCHG.10)
ms:contentKeyID: 39516766
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4031a41fe521f6dceb6bb64b5bc8567afee97e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998963"
---
# <a name="jet_lgpos-members"></a>Элементы JET_LGPOS

Включить защищенные члены  
Включить унаследованные члены  

Описывает смещение в последовательности журнала.

Тип [JET_LGPOS](./jet-lgpos-structure2.md) предоставляет следующие члены.

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
<td><a href="hh579511(v=exchg.10).md">HasValue</a></td>
<td>Возвращает значение, указывающее, имеет ли данная запись журнала значение null.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh565113(v=exchg.10).md">IB</a></td>
<td>Возвращает или задает смещение в байтах, представленное данной позицией журнала. Это смещение находится внутри сектора.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh566270(v=exchg.10).md">исек</a></td>
<td>Возвращает или задает номер сектора, представленного этой позицией журнала.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh577855(v=exchg.10).md">lGeneration</a></td>
<td>Возвращает или задает поколение этого расположения журнала.</td>
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
<td><a href="hh579485(v=exchg.10).md">CompareTo</a></td>
<td>Сравнивает эту точку журнала с другим положением журнала и определяет, является ли этот экземпляр предшествующим, таким же, как и после другого экземпляра.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh565006(v=exchg.10).md">Equals (Object)</a></td>
<td>Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру. (Переопределяет <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh558574(v=exchg.10).md">Equals (JET_LGPOS)</a></td>
<td>Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh578422(v=exchg.10).md">GetHashCode</a></td>
<td>Возвращает хэш-код данного экземпляра. (Переопределяет <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh558225(v=exchg.10).md">ToString</a></td>
<td>Создает строковое представление структуры. (Переопределяет <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="operators"></a>Операторы

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
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh557134(v=exchg.10).md">Равенство</a></td>
<td>Определяет, равны ли два указанных экземпляра JET_LGPOS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh557121(v=exchg.10).md">GreaterThan</a></td>
<td>Определить, находится ли один журнал после другой позицией в журнале.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh557469(v=exchg.10).md">GreaterThanOrEqual;</a></td>
<td>Определить, находится ли одна запись журнала после или равна другому положению в журнале.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh564795(v=exchg.10).md">Неравенство</a></td>
<td>Определяет, являются ли два указанных экземпляра JET_LGPOS неравными.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh577466(v=exchg.10).md">LessThan;</a></td>
<td>Определить, находится ли один журнал до другого места в журнале.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh557093(v=exchg.10).md">LessThanOrEqual;</a></td>
<td>Определить, находится ли одна запись журнала до или равна другому положению в журнале.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_LGPOS](./jet-lgpos-structure2.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
