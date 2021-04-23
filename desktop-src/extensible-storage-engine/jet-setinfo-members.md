---
description: 'Дополнительные сведения о: JET_SETINFO Members'
title: Элементы JET_SETINFO
TOCTitle: JET_SETINFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103871
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c782eace916b3871ade67870b08e1766faeafd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809017"
---
# <a name="jet_setinfo-members"></a><span data-ttu-id="6016c-103">Элементы JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6016c-103">JET_SETINFO members</span></span>

<span data-ttu-id="6016c-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="6016c-104">Include protected members</span></span>  
<span data-ttu-id="6016c-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="6016c-105">Include inherited members</span></span>  

<span data-ttu-id="6016c-106">Параметры для Жетсетколумн.</span><span class="sxs-lookup"><span data-stu-id="6016c-106">Settings for JetSetColumn.</span></span>

<span data-ttu-id="6016c-107">Тип [JET_SETINFO](./jet-setinfo-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="6016c-107">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="6016c-108">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="6016c-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6016c-109">Имя</span><span class="sxs-lookup"><span data-stu-id="6016c-109">Name</span></span></th>
<th><span data-ttu-id="6016c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6016c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="6016c-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span><span class="sxs-lookup"><span data-stu-id="6016c-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6016c-113">Начало</span><span class="sxs-lookup"><span data-stu-id="6016c-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="6016c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6016c-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6016c-115">Имя</span><span class="sxs-lookup"><span data-stu-id="6016c-115">Name</span></span></th>
<th><span data-ttu-id="6016c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6016c-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="6016c-118"><a href="dn351064(v=exchg.10).md">иблонгвалуе</a></span><span class="sxs-lookup"><span data-stu-id="6016c-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="6016c-119">Возвращает или задает смещение для первого байта, который необходимо задать в столбце типа <a href="hh577895(v=exchg.10).md">лонгбинари</a> или <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="6016c-119">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="6016c-121"><a href="dn351037(v=exchg.10).md">итагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="6016c-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="6016c-122">Возвращает или задает порядковый номер значения в столбце с несколькими значениями, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="6016c-122">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="6016c-123">Массив значений является исходным.</span><span class="sxs-lookup"><span data-stu-id="6016c-123">The array of values is one-based.</span></span> <span data-ttu-id="6016c-124">Первое значение — Sequence 1, а не 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="6016c-124">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="6016c-125">Если столбец записи имеет только одно значение, то значение 1 должно передаваться как Итагсекуенце при замене этого значения.</span><span class="sxs-lookup"><span data-stu-id="6016c-125">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="6016c-126">Значение 0 (ноль) означает, что новый экземпляр значения столбца добавляется в конец последовательности значений столбцов.</span><span class="sxs-lookup"><span data-stu-id="6016c-126">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6016c-127">Начало</span><span class="sxs-lookup"><span data-stu-id="6016c-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="6016c-128">Методы</span><span class="sxs-lookup"><span data-stu-id="6016c-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6016c-129">Имя</span><span class="sxs-lookup"><span data-stu-id="6016c-129">Name</span></span></th>
<th><span data-ttu-id="6016c-130">Описание</span><span class="sxs-lookup"><span data-stu-id="6016c-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="6016c-132"><a href="dn351060(v=exchg.10).md">контентекуалс</a></span><span class="sxs-lookup"><span data-stu-id="6016c-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="6016c-133">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="6016c-133">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="6016c-135"><a href="dn351032(v=exchg.10).md">дипклоне</a></span><span class="sxs-lookup"><span data-stu-id="6016c-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="6016c-136">Возвращает глубокую копию объекта.</span><span class="sxs-lookup"><span data-stu-id="6016c-136">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="6016c-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="6016c-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="6016c-139">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6016c-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="6016c-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="6016c-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="6016c-142">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6016c-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="6016c-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="6016c-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="6016c-145">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6016c-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="6016c-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="6016c-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="6016c-148">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6016c-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="6016c-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="6016c-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="6016c-151">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6016c-151">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="6016c-153"><a href="dn351062(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="6016c-153"><a href="dn351062(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="6016c-154">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="6016c-154">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>.</span></span> <span data-ttu-id="6016c-155">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="6016c-155">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6016c-156">Начало</span><span class="sxs-lookup"><span data-stu-id="6016c-156">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="6016c-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6016c-157">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6016c-158">Справочник</span><span class="sxs-lookup"><span data-stu-id="6016c-158">Reference</span></span>

[<span data-ttu-id="6016c-159">Класс JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6016c-159">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="6016c-160">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6016c-160">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
