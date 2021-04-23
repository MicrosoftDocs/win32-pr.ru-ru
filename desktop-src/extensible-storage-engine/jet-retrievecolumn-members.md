---
description: 'Дополнительные сведения о: JET_RETRIEVECOLUMN Members'
title: Элементы JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9a5eda1d671cfe6225a8419314b2f53558294754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571754"
---
# <a name="jet_retrievecolumn-members"></a><span data-ttu-id="82216-103">Элементы JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="82216-103">JET_RETRIEVECOLUMN members</span></span>

<span data-ttu-id="82216-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="82216-104">Include protected members</span></span>  
<span data-ttu-id="82216-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="82216-105">Include inherited members</span></span>  

<span data-ttu-id="82216-106">Содержит входные и выходные параметры для [жетретриевеколумнс (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetretrievecolumns-method.md).</span><span class="sxs-lookup"><span data-stu-id="82216-106">Contains input and output parameters for [JetRetrieveColumns(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetretrievecolumns-method.md).</span></span> <span data-ttu-id="82216-107">Поля в структуре описывают извлекаемое значение столбца, способ его извлечения и место сохранения результатов.</span><span class="sxs-lookup"><span data-stu-id="82216-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

<span data-ttu-id="82216-108">Тип [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="82216-108">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="82216-109">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="82216-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="82216-110">Имя</span><span class="sxs-lookup"><span data-stu-id="82216-110">Name</span></span></th>
<th><span data-ttu-id="82216-111">Описание</span><span class="sxs-lookup"><span data-stu-id="82216-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="82216-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="82216-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="82216-114">Начало</span><span class="sxs-lookup"><span data-stu-id="82216-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="82216-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="82216-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="82216-116">Имя</span><span class="sxs-lookup"><span data-stu-id="82216-116">Name</span></span></th>
<th><span data-ttu-id="82216-117">Описание</span><span class="sxs-lookup"><span data-stu-id="82216-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-119"><a href="dn335226(v=exchg.10).md">кбактуал</a></span><span class="sxs-lookup"><span data-stu-id="82216-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="82216-120">Возвращает размер данных в байтах, извлекаемый операцией извлечения столбца.</span><span class="sxs-lookup"><span data-stu-id="82216-120">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-122"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="82216-122"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="82216-123">Возвращает или задает размер буфера <a href="dn351040(v=exchg.10).md">пвдата</a> в байтах.</span><span class="sxs-lookup"><span data-stu-id="82216-123">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="82216-124">Операция получения столбца не будет хранить больше данных в Пвдата, чем cbData.</span><span class="sxs-lookup"><span data-stu-id="82216-124">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-126"><a href="dn335230(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="82216-126"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="82216-127">Возвращает или задает идентификатор столбца для извлекаемого столбца.</span><span class="sxs-lookup"><span data-stu-id="82216-127">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-129"><a href="dn335229(v=exchg.10).md">колумниднексттагжед</a></span><span class="sxs-lookup"><span data-stu-id="82216-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="82216-130">Получает значение columnid столбца с тегом, многозначным или разреженным, если все столбцы с тегами извлекаются путем передачи 0 в качестве значения columnid.</span><span class="sxs-lookup"><span data-stu-id="82216-130">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-132"><a href="dn335231(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="82216-132"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="82216-133">Возвращает предупреждение, возвращенное при извлечении столбца.</span><span class="sxs-lookup"><span data-stu-id="82216-133">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-135"><a href="dn335232(v=exchg.10).md">грбит</a></span><span class="sxs-lookup"><span data-stu-id="82216-135"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="82216-136">Возвращает или задает параметры для извлечения столбца.</span><span class="sxs-lookup"><span data-stu-id="82216-136">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-138"><a href="dn335233(v=exchg.10).md">ибдата</a></span><span class="sxs-lookup"><span data-stu-id="82216-138"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="82216-139">Возвращает или задает смещение в буфере, в котором будут храниться данные.</span><span class="sxs-lookup"><span data-stu-id="82216-139">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-141"><a href="dn335234(v=exchg.10).md">иблонгвалуе</a></span><span class="sxs-lookup"><span data-stu-id="82216-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="82216-142">Возвращает или задает смещение для первого байта, получаемого из столбца типа <a href="hh577895(v=exchg.10).md">лонгбинари</a> или <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="82216-142">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-144"><a href="dn351039(v=exchg.10).md">итагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="82216-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="82216-145">Возвращает или задает порядковый номер значений, содержащихся в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="82216-145">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="82216-146">Если значение Итагсекуенце равно 0, то вместо данных столбца возвращается число экземпляров многозначного столбца.</span><span class="sxs-lookup"><span data-stu-id="82216-146">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="82216-148"><a href="dn351040(v=exchg.10).md">пвдата</a></span><span class="sxs-lookup"><span data-stu-id="82216-148"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="82216-149">Возвращает или задает буфер, в котором будут храниться данные, извлекаемые из столбца.</span><span class="sxs-lookup"><span data-stu-id="82216-149">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="82216-150">Начало</span><span class="sxs-lookup"><span data-stu-id="82216-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="82216-151">Методы</span><span class="sxs-lookup"><span data-stu-id="82216-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="82216-152">Имя</span><span class="sxs-lookup"><span data-stu-id="82216-152">Name</span></span></th>
<th><span data-ttu-id="82216-153">Описание</span><span class="sxs-lookup"><span data-stu-id="82216-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="82216-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="82216-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="82216-156">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="82216-156">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="82216-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="82216-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="82216-159">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="82216-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="82216-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="82216-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="82216-162">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="82216-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="82216-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="82216-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="82216-165">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="82216-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="82216-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="82216-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="82216-168">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="82216-168">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="82216-170"><a href="dn335224(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="82216-170"><a href="dn335224(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="82216-171">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="82216-171">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>.</span></span> <span data-ttu-id="82216-172">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="82216-172">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="82216-173">Начало</span><span class="sxs-lookup"><span data-stu-id="82216-173">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="82216-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82216-174">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82216-175">Справочник</span><span class="sxs-lookup"><span data-stu-id="82216-175">Reference</span></span>

[<span data-ttu-id="82216-176">Класс JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="82216-176">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="82216-177">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="82216-177">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
