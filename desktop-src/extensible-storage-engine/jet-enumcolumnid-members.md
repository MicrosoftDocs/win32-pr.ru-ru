---
description: 'Дополнительные сведения о: JET_ENUMCOLUMNID Members'
title: Элементы JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f852541d8e16a1a9edfd87afe59a0a8a4c4c4af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072616"
---
# <a name="jet_enumcolumnid-members"></a><span data-ttu-id="d7475-103">Элементы JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="d7475-103">JET_ENUMCOLUMNID members</span></span>

<span data-ttu-id="d7475-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="d7475-104">Include protected members</span></span>  
<span data-ttu-id="d7475-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="d7475-105">Include inherited members</span></span>  

<span data-ttu-id="d7475-106">Перечисляет конкретный набор столбцов и, при необходимости, конкретный набор нескольких значений для этих столбцов при использовании функции Жетенумератеколумнс.</span><span class="sxs-lookup"><span data-stu-id="d7475-106">Enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the JetEnumerateColumns function is used.</span></span> <span data-ttu-id="d7475-107">Жетенумератеколумнс при необходимости принимает массив структур JET_ENUMCOLUMNID.</span><span class="sxs-lookup"><span data-stu-id="d7475-107">JetEnumerateColumns optionally takes an array of JET_ENUMCOLUMNID structures.</span></span>

<span data-ttu-id="d7475-108">Тип [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="d7475-108">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="d7475-109">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="d7475-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d7475-110">Имя</span><span class="sxs-lookup"><span data-stu-id="d7475-110">Name</span></span></th>
<th><span data-ttu-id="d7475-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d7475-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d7475-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span><span class="sxs-lookup"><span data-stu-id="d7475-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d7475-114">Начало</span><span class="sxs-lookup"><span data-stu-id="d7475-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="d7475-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="d7475-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d7475-116">Имя</span><span class="sxs-lookup"><span data-stu-id="d7475-116">Name</span></span></th>
<th><span data-ttu-id="d7475-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d7475-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d7475-119"><a href="dn335141(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="d7475-119"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="d7475-120">Возвращает или задает идентификатор columnid для перечисления.</span><span class="sxs-lookup"><span data-stu-id="d7475-120">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d7475-122"><a href="dn335092(v=exchg.10).md">ктагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="d7475-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="d7475-123">Возвращает или задает количество значений столбца (по одному индексу) для перечисления по указанному ИДЕНТИФИКАТОРу столбца.</span><span class="sxs-lookup"><span data-stu-id="d7475-123">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="d7475-124">Если Ктагсекуенце имеет значение 0 (ноль), то Ргтагсекуенце игнорируется и все значения столбцов для указанного идентификатора столбца будут перечислены.</span><span class="sxs-lookup"><span data-stu-id="d7475-124">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="d7475-126"><a href="dn335093(v=exchg.10).md">ргтагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="d7475-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="d7475-127">Возвращает или задает массив индексов, отсчитываемый от единицы, в массиве значений столбцов для данного столбца.</span><span class="sxs-lookup"><span data-stu-id="d7475-127">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="d7475-128">Единственный элемент — это Итагсекуенце, который определен в JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="d7475-128">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="d7475-129">Итагсекуенце 0 (ноль) означает &quot; пропуск &quot; .</span><span class="sxs-lookup"><span data-stu-id="d7475-129">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="d7475-130">Итагсекуенце 1 означает возврат значения первого столбца столбца, 2 — второй и т. д.</span><span class="sxs-lookup"><span data-stu-id="d7475-130">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d7475-131">Начало</span><span class="sxs-lookup"><span data-stu-id="d7475-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="d7475-132">Методы</span><span class="sxs-lookup"><span data-stu-id="d7475-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d7475-133">Имя</span><span class="sxs-lookup"><span data-stu-id="d7475-133">Name</span></span></th>
<th><span data-ttu-id="d7475-134">Описание</span><span class="sxs-lookup"><span data-stu-id="d7475-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d7475-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="d7475-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="d7475-137">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d7475-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="d7475-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="d7475-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="d7475-140">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d7475-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d7475-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="d7475-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="d7475-143">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d7475-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d7475-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="d7475-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="d7475-146">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d7475-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="d7475-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="d7475-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="d7475-149">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d7475-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="d7475-151"><a href="dn335091(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="d7475-151"><a href="dn335091(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="d7475-152">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="d7475-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>.</span></span> <span data-ttu-id="d7475-153">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="d7475-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d7475-154">Начало</span><span class="sxs-lookup"><span data-stu-id="d7475-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="d7475-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7475-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d7475-156">Справочник</span><span class="sxs-lookup"><span data-stu-id="d7475-156">Reference</span></span>

[<span data-ttu-id="d7475-157">Класс JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="d7475-157">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="d7475-158">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d7475-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
