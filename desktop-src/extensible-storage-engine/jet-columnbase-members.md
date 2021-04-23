---
description: 'Дополнительные сведения о: JET_COLUMNBASE Members'
title: 'Члены JET_COLUMNBASE '
TOCTitle: JET_COLUMNBASE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase_members(v=EXCHG.10)
ms:contentKeyID: 55103414
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 72f26e02963d1cc0617fb908ce325c0c0099f7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348285"
---
# <a name="jet_columnbase-members"></a><span data-ttu-id="d0d96-103">Члены JET_COLUMNBASE </span><span class="sxs-lookup"><span data-stu-id="d0d96-103">JET_COLUMNBASE members</span></span>

<span data-ttu-id="d0d96-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="d0d96-104">Include protected members</span></span>  
<span data-ttu-id="d0d96-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="d0d96-105">Include inherited members</span></span>  

<span data-ttu-id="d0d96-106">Описывает столбец в таблице базы данных ESENT.</span><span class="sxs-lookup"><span data-stu-id="d0d96-106">Describes a column in a table of an ESENT database.</span></span>

<span data-ttu-id="d0d96-107">Тип [JET_COLUMNBASE](./jet-columnbase-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="d0d96-107">The [JET_COLUMNBASE](./jet-columnbase-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="d0d96-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="d0d96-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d0d96-109">Имя</span><span class="sxs-lookup"><span data-stu-id="d0d96-109">Name</span></span></th>
<th><span data-ttu-id="d0d96-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d0d96-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d0d96-112"><a href="dn335065(v=exchg.10).md">кбмакс</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-112"><a href="dn335065(v=exchg.10).md">cbMax</a></span></span></td>
<td><span data-ttu-id="d0d96-113">Возвращает максимальную длину столбца.</span><span class="sxs-lookup"><span data-stu-id="d0d96-113">Gets the maximum length of the column.</span></span> <span data-ttu-id="d0d96-114">Это имеет смысл только для столбцов типа <a href="hh577895(v=exchg.10).md">Text</a>, <a href="hh577895(v=exchg.10).md">LongText</a>, <a href="hh577895(v=exchg.10).md">binary</a> и <a href="hh577895(v=exchg.10).md">лонгбинари</a>.</span><span class="sxs-lookup"><span data-stu-id="d0d96-114">This is only meaningful for columns of type <a href="hh577895(v=exchg.10).md">Text</a>, <a href="hh577895(v=exchg.10).md">LongText</a>, <a href="hh577895(v=exchg.10).md">Binary</a> and <a href="hh577895(v=exchg.10).md">LongBinary</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d0d96-116"><a href="dn351019(v=exchg.10).md">колтип</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-116"><a href="dn351019(v=exchg.10).md">coltyp</a></span></span></td>
<td><span data-ttu-id="d0d96-117">Возвращает тип столбца.</span><span class="sxs-lookup"><span data-stu-id="d0d96-117">Gets type of the column.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d0d96-119"><a href="dn335024(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-119"><a href="dn335024(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="d0d96-120">Возвращает значение columnid столбца.</span><span class="sxs-lookup"><span data-stu-id="d0d96-120">Gets the columnid of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d0d96-122"><a href="dn335066(v=exchg.10).md">cp</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-122"><a href="dn335066(v=exchg.10).md">cp</a></span></span></td>
<td><span data-ttu-id="d0d96-123">Возвращает кодовую страницу столбца.</span><span class="sxs-lookup"><span data-stu-id="d0d96-123">Gets code page of the column.</span></span> <span data-ttu-id="d0d96-124">Это имеет смысл только для столбцов типа <a href="hh577895(v=exchg.10).md">Text</a> и <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="d0d96-124">This is only meaningful for columns of type <a href="hh577895(v=exchg.10).md">Text</a> and <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d0d96-126"><a href="dn351020(v=exchg.10).md">грбит</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-126"><a href="dn351020(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="d0d96-127">Возвращает параметры столбца.</span><span class="sxs-lookup"><span data-stu-id="d0d96-127">Gets the column options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d0d96-129"><a href="dn335067(v=exchg.10).md">сзбасеколумннаме</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-129"><a href="dn335067(v=exchg.10).md">szBaseColumnName</a></span></span></td>
<td><span data-ttu-id="d0d96-130">Возвращает имя столбца в таблице шаблонов.</span><span class="sxs-lookup"><span data-stu-id="d0d96-130">Gets the name of the column in the template table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d0d96-132"><a href="dn335026(v=exchg.10).md">сзбасетабленаме</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-132"><a href="dn335026(v=exchg.10).md">szBaseTableName</a></span></span></td>
<td><span data-ttu-id="d0d96-133">Возвращает таблицу, из которой текущая таблица наследует свою DDL.</span><span class="sxs-lookup"><span data-stu-id="d0d96-133">Gets the table from which the current table inherits its DDL.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d0d96-134">Начало</span><span class="sxs-lookup"><span data-stu-id="d0d96-134">Top</span></span>

## <a name="methods"></a><span data-ttu-id="d0d96-135">Методы</span><span class="sxs-lookup"><span data-stu-id="d0d96-135">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d0d96-136">Имя</span><span class="sxs-lookup"><span data-stu-id="d0d96-136">Name</span></span></th>
<th><span data-ttu-id="d0d96-137">Описание</span><span class="sxs-lookup"><span data-stu-id="d0d96-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d0d96-139"><a href="dn335062(v=exchg.10).md">Equals (Object)</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-139"><a href="dn335062(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="d0d96-140">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="d0d96-140">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="d0d96-141">(Переопределяет <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. Equals (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="d0d96-141">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d0d96-143"><a href="dn351009(v=exchg.10).md">Equals (JET_COLUMNBASE)</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-143"><a href="dn351009(v=exchg.10).md">Equals(JET_COLUMNBASE)</a></span></span></td>
<td><span data-ttu-id="d0d96-144">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="d0d96-144">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="d0d96-146"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-146"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="d0d96-147">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d0d96-147">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d0d96-149"><a href="dn335023(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-149"><a href="dn335023(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="d0d96-150">Возвращает хэш-код данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d0d96-150">Returns the hash code for this instance.</span></span> <span data-ttu-id="d0d96-151">(Переопределяет <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="d0d96-151">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d0d96-153"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-153"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="d0d96-154">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d0d96-154">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="d0d96-156"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-156"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="d0d96-157">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d0d96-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d0d96-159"><a href="dn335064(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="d0d96-159"><a href="dn335064(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="d0d96-160">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn335045(v=exchg.10).md">JET_COLUMNBASE</a>.</span><span class="sxs-lookup"><span data-stu-id="d0d96-160">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335045(v=exchg.10).md">JET_COLUMNBASE</a>.</span></span> <span data-ttu-id="d0d96-161">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="d0d96-161">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d0d96-162">Начало</span><span class="sxs-lookup"><span data-stu-id="d0d96-162">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="d0d96-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0d96-163">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0d96-164">Справочник</span><span class="sxs-lookup"><span data-stu-id="d0d96-164">Reference</span></span>

[<span data-ttu-id="d0d96-165">Класс JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="d0d96-165">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="d0d96-166">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d0d96-166">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
