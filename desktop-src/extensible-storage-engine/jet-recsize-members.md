---
description: 'Дополнительные сведения о: JET_RECSIZE Members'
title: Элементы JET_RECSIZE (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8a39bc4aee3b033b735d5c4ebe818d189c36b1908ba8364200c4cb94b15459cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063754"
---
# <a name="jet_recsize-members"></a>Элементы JET_RECSIZE

Включить защищенные члены  
Включить унаследованные члены  

Используется [жетжетрекордсизе (JET_SESID, JET_TABLEID, JET_RECSIZE, жетрекордсизегрбит)](./vistaapi.jetgetrecordsize-method.md) для получения сведений о требованиях к использованию записи в пространстве данных пользователя, количестве столбцов набора, количестве значений и служебной нагрузке записи ESENT.

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
<td><a href="hh538879(v=exchg.10).md">Добавить</a></td>
<td>Добавьте размеры в две структуры JET_RECSIZE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh558506(v=exchg.10).md">Equals (Object)</a></td>
<td>Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру. (Переопределяет <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh577992(v=exchg.10).md">Equals (JET_RECSIZE)</a></td>
<td>Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="hh557078(v=exchg.10).md">GetHashCode</a></td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh579561(v=exchg.10).md">Subtract</a></td>
<td>Вычисление разницы между двумя JET_RECSIZEными структурами.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.valuetype">ValueType</a>.)</td>
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
<td><a href="hh578675(v=exchg.10).md">Полняют</a></td>
<td>Добавьте размеры в две структуры JET_RECSIZE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh596362(v=exchg.10).md">Равенство</a></td>
<td>Определяет, равны ли два указанных экземпляра JET_RECSIZE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh578809(v=exchg.10).md">Неравенство</a></td>
<td>Определяет, являются ли два указанных экземпляра JET_RECSIZE неравными.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="hh596696(v=exchg.10).md">Вычитания</a></td>
<td>Вычисление разницы между двумя JET_RECSIZEными структурами.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_RECSIZE](./jet-recsize-structure2.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
