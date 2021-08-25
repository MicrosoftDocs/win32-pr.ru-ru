---
description: 'Дополнительные сведения о: JET_THREADSTATS Members'
title: Элементы JET_THREADSTATS (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_THREADSTATS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats_members(v=EXCHG.10)
ms:contentKeyID: 39514028
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 13713d00431337f5e2190e2f547729e96a7cfb634fe1a95dddba570a9236f1f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890304"
---
# <a name="jet_threadstats-members"></a>Элементы JET_THREADSTATS

Включить защищенные члены  
Включить унаследованные члены  

Содержит совокупную статистику по работе, выполненной ядром СУБД в текущем потоке. Эти сведения возвращаются через Жетжетсреадстатс.

Тип [JET_THREADSTATS](./jet-threadstats-structure2.md) предоставляет следующие члены.

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
<td><a href="hh578305(v=exchg.10).md">кблогрекорд</a></td>
<td>Возвращает общий размер (в байтах) записей журнала транзакций, созданных ядром СУБД в текущем потоке.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh578110(v=exchg.10).md">клогрекорд</a></td>
<td>Возвращает общее число записей журнала транзакций, созданных ядром СУБД в текущем потоке.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh578651(v=exchg.10).md">кпажедиртиед</a></td>
<td>Возвращает общее число страниц базы данных без незаписанных изменений, которые были изменены ядром СУБД в текущем потоке.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh557376(v=exchg.10).md">кпажепререад</a></td>
<td>Возвращает общее число страниц базы данных, выбранных с диска ядром СУБД в текущем потоке.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh163392(v=exchg.10).md">кпажереад</a></td>
<td>Возвращает общее число страниц базы данных, извлекаемых с диска ядром СУБД в текущем потоке.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh596234(v=exchg.10).md">кпажередиртиед</a></td>
<td>Возвращает общее число страниц базы данных с незаписанными изменениями, которые были изменены ядром СУБД в текущем потоке.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="hh557174(v=exchg.10).md">кпажереференцед</a></td>
<td>Возвращает общее число страниц базы данных, посещенных ядром СУБД в текущем потоке.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh565584(v=exchg.10).md">Добавить</a></td>
<td>Добавьте статистику в две структуры JET_THREADSTATS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh538903(v=exchg.10).md">Создание</a></td>
<td>Создать новую <a href="hh578565(v=exchg.10).md">JET_THREADSTATS</a> структуру с указанным значением.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh557146(v=exchg.10).md">Equals (Object)</a></td>
<td>Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру. (Переопределяет <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh596601(v=exchg.10).md">Equals (JET_THREADSTATS)</a></td>
<td>Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh579156(v=exchg.10).md">GetHashCode</a></td>
<td>Возвращает хэш-код данного экземпляра. (Переопределяет <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh579433(v=exchg.10).md">Subtract</a></td>
<td>Вычислите разницу в статистике между двумя JET_THREADSTATSными структурами.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh558249(v=exchg.10).md">ToString</a></td>
<td>Возвращает строковое представление этого объекта. (Переопределяет <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType. ToString ()</a>.)</td>
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
<td><a href="hh163281(v=exchg.10).md">Полняют</a></td>
<td>Добавьте статистику в две структуры JET_THREADSTATS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh558521(v=exchg.10).md">Равенство</a></td>
<td>Определяет, равны ли два указанных экземпляра JET_THREADSTATS.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh577527(v=exchg.10).md">Неравенство</a></td>
<td>Определяет, являются ли два указанных экземпляра JET_THREADSTATS неравными.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh557686(v=exchg.10).md">Вычитания</a></td>
<td>Вычислите разницу в статистике между двумя JET_THREADSTATSными структурами.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Структура JET_THREADSTATS](./jet-threadstats-structure2.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
