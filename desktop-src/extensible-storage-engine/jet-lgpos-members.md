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
# <a name="jet_lgpos-members"></a><span data-ttu-id="bab5f-103">Элементы JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="bab5f-103">JET_LGPOS members</span></span>

<span data-ttu-id="bab5f-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="bab5f-104">Include protected members</span></span>  
<span data-ttu-id="bab5f-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="bab5f-105">Include inherited members</span></span>  

<span data-ttu-id="bab5f-106">Описывает смещение в последовательности журнала.</span><span class="sxs-lookup"><span data-stu-id="bab5f-106">Describes an offset in the log sequence.</span></span>

<span data-ttu-id="bab5f-107">Тип [JET_LGPOS](./jet-lgpos-structure2.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="bab5f-107">The [JET_LGPOS](./jet-lgpos-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="bab5f-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="bab5f-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bab5f-109">Имя</span><span class="sxs-lookup"><span data-stu-id="bab5f-109">Name</span></span></th>
<th><span data-ttu-id="bab5f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bab5f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="bab5f-112"><a href="hh579511(v=exchg.10).md">HasValue</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-112"><a href="hh579511(v=exchg.10).md">HasValue</a></span></span></td>
<td><span data-ttu-id="bab5f-113">Возвращает значение, указывающее, имеет ли данная запись журнала значение null.</span><span class="sxs-lookup"><span data-stu-id="bab5f-113">Gets a value indicating whether this log position is null.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="bab5f-115"><a href="hh565113(v=exchg.10).md">IB</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-115"><a href="hh565113(v=exchg.10).md">ib</a></span></span></td>
<td><span data-ttu-id="bab5f-116">Возвращает или задает смещение в байтах, представленное данной позицией журнала.</span><span class="sxs-lookup"><span data-stu-id="bab5f-116">Gets or sets the byte offset represented by this log position.</span></span> <span data-ttu-id="bab5f-117">Это смещение находится внутри сектора.</span><span class="sxs-lookup"><span data-stu-id="bab5f-117">This offset is inside of the sector.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="bab5f-119"><a href="hh566270(v=exchg.10).md">исек</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-119"><a href="hh566270(v=exchg.10).md">isec</a></span></span></td>
<td><span data-ttu-id="bab5f-120">Возвращает или задает номер сектора, представленного этой позицией журнала.</span><span class="sxs-lookup"><span data-stu-id="bab5f-120">Gets or sets the sector number represented by this log position.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="bab5f-122"><a href="hh577855(v=exchg.10).md">lGeneration</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-122"><a href="hh577855(v=exchg.10).md">lGeneration</a></span></span></td>
<td><span data-ttu-id="bab5f-123">Возвращает или задает поколение этого расположения журнала.</span><span class="sxs-lookup"><span data-stu-id="bab5f-123">Gets or sets the generation of this log position.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab5f-124">Начало</span><span class="sxs-lookup"><span data-stu-id="bab5f-124">Top</span></span>

## <a name="methods"></a><span data-ttu-id="bab5f-125">Методы</span><span class="sxs-lookup"><span data-stu-id="bab5f-125">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bab5f-126">Имя</span><span class="sxs-lookup"><span data-stu-id="bab5f-126">Name</span></span></th>
<th><span data-ttu-id="bab5f-127">Описание</span><span class="sxs-lookup"><span data-stu-id="bab5f-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="bab5f-129"><a href="hh579485(v=exchg.10).md">CompareTo</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-129"><a href="hh579485(v=exchg.10).md">CompareTo</a></span></span></td>
<td><span data-ttu-id="bab5f-130">Сравнивает эту точку журнала с другим положением журнала и определяет, является ли этот экземпляр предшествующим, таким же, как и после другого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bab5f-130">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="bab5f-132"><a href="hh565006(v=exchg.10).md">Equals (Object)</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-132"><a href="hh565006(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="bab5f-133">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="bab5f-133">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="bab5f-134">(Переопределяет <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="bab5f-134">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="bab5f-136"><a href="hh558574(v=exchg.10).md">Equals (JET_LGPOS)</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-136"><a href="hh558574(v=exchg.10).md">Equals(JET_LGPOS)</a></span></span></td>
<td><span data-ttu-id="bab5f-137">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="bab5f-137">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="bab5f-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="bab5f-140">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="bab5f-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="bab5f-142"><a href="hh578422(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-142"><a href="hh578422(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="bab5f-143">Возвращает хэш-код данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bab5f-143">Returns the hash code for this instance.</span></span> <span data-ttu-id="bab5f-144">(Переопределяет <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="bab5f-144">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="bab5f-146"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-146"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="bab5f-147">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="bab5f-147">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="bab5f-149"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-149"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="bab5f-150">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="bab5f-150">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="bab5f-152"><a href="hh558225(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-152"><a href="hh558225(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="bab5f-153">Создает строковое представление структуры.</span><span class="sxs-lookup"><span data-stu-id="bab5f-153">Generate a string representation of the structure.</span></span> <span data-ttu-id="bab5f-154">(Переопределяет <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="bab5f-154">(Overrides <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab5f-155">Начало</span><span class="sxs-lookup"><span data-stu-id="bab5f-155">Top</span></span>

## <a name="operators"></a><span data-ttu-id="bab5f-156">Операторы</span><span class="sxs-lookup"><span data-stu-id="bab5f-156">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bab5f-157">Имя</span><span class="sxs-lookup"><span data-stu-id="bab5f-157">Name</span></span></th>
<th><span data-ttu-id="bab5f-158">Описание</span><span class="sxs-lookup"><span data-stu-id="bab5f-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="bab5f-161"><a href="hh557134(v=exchg.10).md">Равенство</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-161"><a href="hh557134(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="bab5f-162">Определяет, равны ли два указанных экземпляра JET_LGPOS.</span><span class="sxs-lookup"><span data-stu-id="bab5f-162">Determines whether two specified instances of JET_LGPOS are equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="bab5f-165"><a href="hh557121(v=exchg.10).md">GreaterThan</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-165"><a href="hh557121(v=exchg.10).md">GreaterThan</a></span></span></td>
<td><span data-ttu-id="bab5f-166">Определить, находится ли один журнал после другой позицией в журнале.</span><span class="sxs-lookup"><span data-stu-id="bab5f-166">Determine whether one log position is after another log position.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="bab5f-169"><a href="hh557469(v=exchg.10).md">GreaterThanOrEqual;</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-169"><a href="hh557469(v=exchg.10).md">GreaterThanOrEqual</a></span></span></td>
<td><span data-ttu-id="bab5f-170">Определить, находится ли одна запись журнала после или равна другому положению в журнале.</span><span class="sxs-lookup"><span data-stu-id="bab5f-170">Determine whether one log position is after or equal to another log position.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="bab5f-173"><a href="hh564795(v=exchg.10).md">Неравенство</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-173"><a href="hh564795(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="bab5f-174">Определяет, являются ли два указанных экземпляра JET_LGPOS неравными.</span><span class="sxs-lookup"><span data-stu-id="bab5f-174">Determines whether two specified instances of JET_LGPOS are not equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="bab5f-177"><a href="hh577466(v=exchg.10).md">LessThan;</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-177"><a href="hh577466(v=exchg.10).md">LessThan</a></span></span></td>
<td><span data-ttu-id="bab5f-178">Определить, находится ли один журнал до другого места в журнале.</span><span class="sxs-lookup"><span data-stu-id="bab5f-178">Determine whether one log position is before another log position.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="bab5f-181"><a href="hh557093(v=exchg.10).md">LessThanOrEqual;</a></span><span class="sxs-lookup"><span data-stu-id="bab5f-181"><a href="hh557093(v=exchg.10).md">LessThanOrEqual</a></span></span></td>
<td><span data-ttu-id="bab5f-182">Определить, находится ли одна запись журнала до или равна другому положению в журнале.</span><span class="sxs-lookup"><span data-stu-id="bab5f-182">Determine whether one log position is before or equal to another log position.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab5f-183">Начало</span><span class="sxs-lookup"><span data-stu-id="bab5f-183">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="bab5f-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bab5f-184">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bab5f-185">Справочник</span><span class="sxs-lookup"><span data-stu-id="bab5f-185">Reference</span></span>

[<span data-ttu-id="bab5f-186">Структура JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="bab5f-186">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="bab5f-187">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bab5f-187">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
