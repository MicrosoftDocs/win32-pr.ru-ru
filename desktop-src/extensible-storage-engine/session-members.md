---
description: 'Дополнительные сведения: члены сеанса'
title: 'Участники сеанса '
TOCTitle: Session members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Session
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session_members(v=EXCHG.10)
ms:contentKeyID: 55104004
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 77a82e2792b984aebfc72c68c15d8c356a4176d6cd9c228064a102346d70bb29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071777"
---
# <a name="session-members"></a>Участники сеанса 

Включить защищенные члены  
Включить унаследованные члены  

Класс, инкапсулирующий JET_SESID в удаляемом объекте.

Тип [сеанса](./session-class.md) предоставляет следующие члены.

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
<td><a href="dn351126(v=exchg.10).md">Session</a></td>
<td>Инициализирует новый экземпляр класса Session. Новый JET_SESSION выделяется из заданного экземпляра.</td>
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
<td><a href="dn351175(v=exchg.10).md">жетсесид</a></td>
<td>Возвращает JET_SESID, который содержит этот сеанс.</td>
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
<td><a href="dn350553(v=exchg.10).md">Dispose ()</a></td>
<td>Удаляет этот объект, освобождая базовый ресурс ESENT. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (логическое значение)</a></td>
<td>Вызывается методом Dispose и методом завершения. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn351128(v=exchg.10).md">END</a></td>
<td>Завершите сеанс.</td>
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
<td><a href="dn351165(v=exchg.10).md">релеасересаурце</a></td>
<td>Освободите базовую JET_SESID. (Переопределяет <a href="dn350545(v=exchg.10).md">есентресаурце. релеасересаурце ()</a>.)</td>
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
<td><a href="dn351129(v=exchg.10).md">ToString</a></td>
<td>Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn351164(v=exchg.10).md">сеанс</a>. (Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
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
<td><a href="dn351178(v=exchg.10).md">Неявное (сеанс для JET_SESID)</a></td>
<td>Неявный оператор преобразования из сеанса в JET_SESID. Это позволяет использовать сеанс с интерфейсами API, которые предполагают JET_SESID.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Session class](./session-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
