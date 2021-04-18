---
description: 'Дополнительные сведения: элементы таблицы'
title: 'Участники таблицы '
TOCTitle: Table members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_members(v=EXCHG.10)
ms:contentKeyID: 55104054
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4e5bd09cf1c450197978e3126dc63fe96ec6425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562820"
---
# <a name="table-members"></a>Участники таблицы 

Включить защищенные члены  
Включить унаследованные члены  

Класс, инкапсулирующий JET_TABLEID в удаляемом объекте. Откроется существующая таблица. Чтобы создать таблицу, используйте метод Жеткреатетабле.

Тип [таблицы](./table-class.md) предоставляет следующие члены.

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
<td><a href="dn351234(v=exchg.10).md">Таблица</a></td>
<td>Инициализирует новый экземпляр класса Table. Таблица открывается из заданной базы данных.</td>
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
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Защищенное свойство" alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">хасресаурце</a></td>
<td>Возвращает значение, указывающее, выделен ли базовый ресурс в данный момент. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351171(v=exchg.10).md">жеттаблеид</a></td>
<td>Возвращает JET_TABLEID, который содержит эта таблица.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351170(v=exchg.10).md">Name</a></td>
<td>Возвращает имя этой таблицы.</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">чеккобжектиснотдиспосед</a></td>
<td>Создать исключение, если этот объект был удален. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn351235(v=exchg.10).md">Закрыть</a></td>
<td>Закройте таблицу.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose ()</a></td>
<td>Удаляет этот объект, освобождая базовый ресурс ESENT. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (логическое значение)</a></td>
<td>Вызывается методом Dispose и методом завершения. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalize</a></td>
<td>Завершает экземпляр класса Есентресаурце. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
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
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn351168(v=exchg.10).md">релеасересаурце</a></td>
<td>Освободите базовую JET_TABLEID. (Переопределяет <a href="dn350545(v=exchg.10).md">есентресаурце. релеасересаурце ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ресаурцевасаллокатед</a></td>
<td>Вызывается подклассом при выделении ресурса. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ресаурцевасрелеасед</a></td>
<td>Вызывается подклассом при освобождении ресурса. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn351237(v=exchg.10).md">ToString</a></td>
<td>Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущую <a href="dn351163(v=exchg.10).md">таблицу</a>. (Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
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
<td><a href="dn351239(v=exchg.10).md">Неявные (таблица для JET_TABLEID)</a></td>
<td>Неявный оператор преобразования из таблицы в JET_TABLEID. Это позволяет использовать таблицу с API, которые предполагают JET_TABLEID.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Table](./table-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
