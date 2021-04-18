---
description: 'Дополнительные сведения о: JET_RECSIZE Members'
title: Элементы JET_RECSIZE (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 224d22b5dea0447297163fb6b5e1a70fe62a6396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561766"
---
# <a name="jet_recsize-members"></a><span data-ttu-id="47a90-103">Элементы JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="47a90-103">JET_RECSIZE members</span></span>

<span data-ttu-id="47a90-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="47a90-104">Include protected members</span></span>  
<span data-ttu-id="47a90-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="47a90-105">Include inherited members</span></span>  

<span data-ttu-id="47a90-106">Используется [жетжетрекордсизе (JET_SESID, JET_TABLEID, JET_RECSIZE, жетрекордсизегрбит)](./vistaapi.jetgetrecordsize-method.md) для получения сведений о требованиях к использованию записи в пространстве данных пользователя, количестве столбцов набора, количестве значений и служебной нагрузке записи ESENT.</span><span class="sxs-lookup"><span data-stu-id="47a90-106">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="47a90-107">Тип [JET_RECSIZE](./jet-recsize-structure2.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="47a90-107">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="47a90-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="47a90-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="47a90-109">Имя</span><span class="sxs-lookup"><span data-stu-id="47a90-109">Name</span></span></th>
<th><span data-ttu-id="47a90-110">Описание</span><span class="sxs-lookup"><span data-stu-id="47a90-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-112"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="47a90-112"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="47a90-113">Возвращает пользовательский набор данных в записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-113">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-115"><a href="hh596280(v=exchg.10).md">кбдатакомпрессед</a></span><span class="sxs-lookup"><span data-stu-id="47a90-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="47a90-116">Возвращает сжатый размер данных пользователя в записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-116">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="47a90-117">Это то же самое, что <a href="hh557581(v=exchg.10).md">cbData</a> , если никакие внутренние значения long не сжимаются).</span><span class="sxs-lookup"><span data-stu-id="47a90-117">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-119"><a href="hh557913(v=exchg.10).md">кблонгвалуедата</a></span><span class="sxs-lookup"><span data-stu-id="47a90-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="47a90-120">Возвращает пользовательский набор данных в записи, но хранится в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="47a90-120">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-122"><a href="hh566144(v=exchg.10).md">кблонгвалуедатакомпрессед</a></span><span class="sxs-lookup"><span data-stu-id="47a90-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="47a90-123">Возвращает сжатый размер пользовательских данных в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="47a90-123">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="47a90-124">Это то же самое, что и <a href="hh557913(v=exchg.10).md">кблонгвалуедата</a> , если не сжаты отдельные длинные значения.</span><span class="sxs-lookup"><span data-stu-id="47a90-124">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-126"><a href="hh558003(v=exchg.10).md">кблонгвалуеоверхеад</a></span><span class="sxs-lookup"><span data-stu-id="47a90-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="47a90-127">Возвращает дополнительную нагрузку на данные с длинными значениями.</span><span class="sxs-lookup"><span data-stu-id="47a90-127">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-129"><a href="hh565836(v=exchg.10).md">кбоверхеад</a></span><span class="sxs-lookup"><span data-stu-id="47a90-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="47a90-130">Возвращает дополнительную нагрузку на структуру записи ESENT для этой записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-130">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="47a90-131">Сюда входит размер ключа записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-131">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-133"><a href="hh566154(v=exchg.10).md">ккомпресседколумнс</a></span><span class="sxs-lookup"><span data-stu-id="47a90-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="47a90-134">Возвращает общее число сжатых столбцов в записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-134">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-136"><a href="hh596288(v=exchg.10).md">клонгвалуес</a></span><span class="sxs-lookup"><span data-stu-id="47a90-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="47a90-137">Возвращает общее количество значений long, хранящихся в дереве Long-Value для этой записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-137">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="47a90-138">Это не относится к внутренним длинным значениям.</span><span class="sxs-lookup"><span data-stu-id="47a90-138">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-140"><a href="hh577486(v=exchg.10).md">кмултивалуес</a></span><span class="sxs-lookup"><span data-stu-id="47a90-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="47a90-141">Возвращает совокупное число значений, находящихся за первым для всех столбцов в записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-141">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-143"><a href="hh578172(v=exchg.10).md">кнонтагжедколумнс</a></span><span class="sxs-lookup"><span data-stu-id="47a90-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="47a90-144">Возвращает общее число фиксированных и переменных столбцов, заданных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-144">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="47a90-146"><a href="hh566034(v=exchg.10).md">ктагжедколумнс</a></span><span class="sxs-lookup"><span data-stu-id="47a90-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="47a90-147">Возвращает общее число столбцов с тегами, заданных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="47a90-147">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47a90-148">Начало</span><span class="sxs-lookup"><span data-stu-id="47a90-148">Top</span></span>

## <a name="methods"></a><span data-ttu-id="47a90-149">Методы</span><span class="sxs-lookup"><span data-stu-id="47a90-149">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="47a90-150">Имя</span><span class="sxs-lookup"><span data-stu-id="47a90-150">Name</span></span></th>
<th><span data-ttu-id="47a90-151">Описание</span><span class="sxs-lookup"><span data-stu-id="47a90-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="47a90-154"><a href="hh538879(v=exchg.10).md">Добавление</a></span><span class="sxs-lookup"><span data-stu-id="47a90-154"><a href="hh538879(v=exchg.10).md">Add</a></span></span></td>
<td><span data-ttu-id="47a90-155">Добавьте размеры в две структуры JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="47a90-155">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="47a90-157"><a href="hh558506(v=exchg.10).md">Equals (Object)</a></span><span class="sxs-lookup"><span data-stu-id="47a90-157"><a href="hh558506(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="47a90-158">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="47a90-158">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="47a90-159">(Переопределяет <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="47a90-159">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="47a90-161"><a href="hh577992(v=exchg.10).md">Equals (JET_RECSIZE)</a></span><span class="sxs-lookup"><span data-stu-id="47a90-161"><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></span></span></td>
<td><span data-ttu-id="47a90-162">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="47a90-162">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="47a90-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="47a90-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="47a90-165">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="47a90-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="47a90-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="47a90-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="47a90-168">Возвращает хэш-код данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="47a90-168">Returns the hash code for this instance.</span></span> <span data-ttu-id="47a90-169">(Переопределяет <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="47a90-169">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="47a90-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="47a90-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="47a90-172">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="47a90-172">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="47a90-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="47a90-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="47a90-175">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="47a90-175">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="47a90-178"><a href="hh579561(v=exchg.10).md">Subtract</a></span><span class="sxs-lookup"><span data-stu-id="47a90-178"><a href="hh579561(v=exchg.10).md">Subtract</a></span></span></td>
<td><span data-ttu-id="47a90-179">Вычисление разницы между двумя JET_RECSIZEными структурами.</span><span class="sxs-lookup"><span data-stu-id="47a90-179">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="47a90-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="47a90-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="47a90-182">(Наследуется от <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span><span class="sxs-lookup"><span data-stu-id="47a90-182">(Inherited from <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47a90-183">Начало</span><span class="sxs-lookup"><span data-stu-id="47a90-183">Top</span></span>

## <a name="operators"></a><span data-ttu-id="47a90-184">Операторы</span><span class="sxs-lookup"><span data-stu-id="47a90-184">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="47a90-185">Имя</span><span class="sxs-lookup"><span data-stu-id="47a90-185">Name</span></span></th>
<th><span data-ttu-id="47a90-186">Описание</span><span class="sxs-lookup"><span data-stu-id="47a90-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="47a90-189"><a href="hh578675(v=exchg.10).md">Полняют</a></span><span class="sxs-lookup"><span data-stu-id="47a90-189"><a href="hh578675(v=exchg.10).md">Addition</a></span></span></td>
<td><span data-ttu-id="47a90-190">Добавьте размеры в две структуры JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="47a90-190">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="47a90-193"><a href="hh596362(v=exchg.10).md">Равенство</a></span><span class="sxs-lookup"><span data-stu-id="47a90-193"><a href="hh596362(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="47a90-194">Определяет, равны ли два указанных экземпляра JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="47a90-194">Determines whether two specified instances of JET_RECSIZE are equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="47a90-197"><a href="hh578809(v=exchg.10).md">Неравенство</a></span><span class="sxs-lookup"><span data-stu-id="47a90-197"><a href="hh578809(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="47a90-198">Определяет, являются ли два указанных экземпляра JET_RECSIZE неравными.</span><span class="sxs-lookup"><span data-stu-id="47a90-198">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="47a90-201"><a href="hh596696(v=exchg.10).md">Вычитания</a></span><span class="sxs-lookup"><span data-stu-id="47a90-201"><a href="hh596696(v=exchg.10).md">Subtraction</a></span></span></td>
<td><span data-ttu-id="47a90-202">Вычисление разницы между двумя JET_RECSIZEными структурами.</span><span class="sxs-lookup"><span data-stu-id="47a90-202">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47a90-203">Начало</span><span class="sxs-lookup"><span data-stu-id="47a90-203">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="47a90-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47a90-204">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="47a90-205">Справочник</span><span class="sxs-lookup"><span data-stu-id="47a90-205">Reference</span></span>

[<span data-ttu-id="47a90-206">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="47a90-206">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="47a90-207">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="47a90-207">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
