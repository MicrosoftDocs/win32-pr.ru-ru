---
description: 'Дополнительные сведения о: JET_ENUMCOLUMNVALUE Members'
title: Элементы JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55103510
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2950caf527af07312f4f27c9464ee4088830fe1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551403"
---
# <a name="jet_enumcolumnvalue-members"></a><span data-ttu-id="97733-103">Элементы JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="97733-103">JET_ENUMCOLUMNVALUE members</span></span>

<span data-ttu-id="97733-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="97733-104">Include protected members</span></span>  
<span data-ttu-id="97733-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="97733-105">Include inherited members</span></span>  

<span data-ttu-id="97733-106">Перечисляет значения столбца записи с помощью функции Жетенумератеколумнс.</span><span class="sxs-lookup"><span data-stu-id="97733-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="97733-107">[Жетенумератеколумнс (JET_SESID, JET_TABLEID, Int32, \[ \] , int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, енумератеколумнсгрбит)](./api.jetenumeratecolumns-method.md) возвращает массив структур JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="97733-107">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="97733-108">Массив возвращается в память, которая была выделена с помощью обратного вызова, предоставленного для этой функции.</span><span class="sxs-lookup"><span data-stu-id="97733-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="97733-109">Тип [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="97733-109">The [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="97733-110">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="97733-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="97733-111">Имя</span><span class="sxs-lookup"><span data-stu-id="97733-111">Name</span></span></th>
<th><span data-ttu-id="97733-112">Описание</span><span class="sxs-lookup"><span data-stu-id="97733-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="97733-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span><span class="sxs-lookup"><span data-stu-id="97733-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97733-115">Начало</span><span class="sxs-lookup"><span data-stu-id="97733-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="97733-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="97733-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="97733-117">Имя</span><span class="sxs-lookup"><span data-stu-id="97733-117">Name</span></span></th>
<th><span data-ttu-id="97733-118">Описание</span><span class="sxs-lookup"><span data-stu-id="97733-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="97733-120"><a href="dn335097(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="97733-120"><a href="dn335097(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="97733-121">Возвращает размер значения столбца для столбца.</span><span class="sxs-lookup"><span data-stu-id="97733-121">Gets the size of the column value for the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="97733-123"><a href="dn335144(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="97733-123"><a href="dn335144(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="97733-124">Возвращает код состояния столбца, полученный в результате перечисления значения столбца.</span><span class="sxs-lookup"><span data-stu-id="97733-124">Gets the column status code resulting from the enumeration of the column value.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="97733-126"><a href="dn335102(v=exchg.10).md">итагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="97733-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="97733-127">Возвращает значение столбца (с использованием одномерного индекса), которое было перечислено.</span><span class="sxs-lookup"><span data-stu-id="97733-127">Gets the column value (by one-based index) that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="97733-129"><a href="dn335149(v=exchg.10).md">пвдата</a></span><span class="sxs-lookup"><span data-stu-id="97733-129"><a href="dn335149(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="97733-130">Возвращает значение, перечисленное для столбца.</span><span class="sxs-lookup"><span data-stu-id="97733-130">Gets the value that was enumerated for the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97733-131">Начало</span><span class="sxs-lookup"><span data-stu-id="97733-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="97733-132">Методы</span><span class="sxs-lookup"><span data-stu-id="97733-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="97733-133">Имя</span><span class="sxs-lookup"><span data-stu-id="97733-133">Name</span></span></th>
<th><span data-ttu-id="97733-134">Описание</span><span class="sxs-lookup"><span data-stu-id="97733-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="97733-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="97733-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="97733-137">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="97733-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="97733-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="97733-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="97733-140">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="97733-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="97733-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="97733-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="97733-143">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="97733-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="97733-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="97733-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="97733-146">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="97733-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="97733-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="97733-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="97733-149">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="97733-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="97733-151"><a href="dn335096(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="97733-151"><a href="dn335096(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="97733-152">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="97733-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="97733-153">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="97733-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97733-154">Начало</span><span class="sxs-lookup"><span data-stu-id="97733-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="97733-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97733-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97733-156">Справочник</span><span class="sxs-lookup"><span data-stu-id="97733-156">Reference</span></span>

[<span data-ttu-id="97733-157">Класс JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="97733-157">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="97733-158">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="97733-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
