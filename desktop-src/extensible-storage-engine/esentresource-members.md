---
description: 'Дополнительные сведения о: Есентресаурце Members'
title: Элементы Есентресаурце
TOCTitle: EsentResource members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource_members(v=EXCHG.10)
ms:contentKeyID: 55107302
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af0f0a4baa76cc702c6f4048e42e9ec78463e5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550507"
---
# <a name="esentresource-members"></a>Элементы Есентресаурце

Включить защищенные члены  
Включить унаследованные члены  

Это базовый класс для всех объектов ресурсов ESENT. Подклассы этого класса могут распределять и освобождать неуправляемые ресурсы.

Тип [есентресаурце](./esentresource-class.md) предоставляет следующие члены.

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
<td><a href="dn350551(v=exchg.10).md">есентресаурце</a></td>
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
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Защищенное свойство" alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">хасресаурце</a></td>
<td>Возвращает значение, указывающее, выделен ли базовый ресурс в данный момент.</td>
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
<td>Создать исключение, если этот объект был удален.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose ()</a></td>
<td>Удаляет этот объект, освобождая базовый ресурс ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (логическое значение)</a></td>
<td>Вызывается методом Dispose и методом завершения.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalize</a></td>
<td>Завершает экземпляр класса Есентресаурце. (Переопределяет <a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Object. Finalize ()</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350545(v=exchg.10).md">релеасересаурце</a></td>
<td>Реализуется подклассом для освобождения ресурса.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ресаурцевасаллокатед</a></td>
<td>Вызывается подклассом при выделении ресурса.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ресаурцевасрелеасед</a></td>
<td>Вызывается подклассом при освобождении ресурса.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.tostring#System_Object_ToString">ToString</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Есентресаурце](./esentresource-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
