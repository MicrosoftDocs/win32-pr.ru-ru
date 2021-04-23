---
description: 'Дополнительные сведения о: JET_RETRIEVECOLUMN свойствах'
title: Свойства JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816368"
---
# <a name="jet_retrievecolumn-properties"></a><span data-ttu-id="5ad4e-103">Свойства JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="5ad4e-103">JET_RETRIEVECOLUMN properties</span></span>

<span data-ttu-id="5ad4e-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="5ad4e-104">Include protected members</span></span>  
<span data-ttu-id="5ad4e-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="5ad4e-105">Include inherited members</span></span>  

<span data-ttu-id="5ad4e-106">Тип [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-106">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="5ad4e-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="5ad4e-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5ad4e-108">Имя</span><span class="sxs-lookup"><span data-stu-id="5ad4e-108">Name</span></span></th>
<th><span data-ttu-id="5ad4e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5ad4e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-111"><a href="dn335226(v=exchg.10).md">кбактуал</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="5ad4e-112">Возвращает размер данных в байтах, извлекаемый операцией извлечения столбца.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-112">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-114"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-114"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="5ad4e-115">Возвращает или задает размер буфера <a href="dn351040(v=exchg.10).md">пвдата</a> в байтах.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-115">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="5ad4e-116">Операция получения столбца не будет хранить больше данных в Пвдата, чем cbData.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-116">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-118"><a href="dn335230(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-118"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="5ad4e-119">Возвращает или задает идентификатор столбца для извлекаемого столбца.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-119">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-121"><a href="dn335229(v=exchg.10).md">колумниднексттагжед</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="5ad4e-122">Получает значение columnid столбца с тегом, многозначным или разреженным, если все столбцы с тегами извлекаются путем передачи 0 в качестве значения columnid.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-122">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-124"><a href="dn335231(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-124"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="5ad4e-125">Возвращает предупреждение, возвращенное при извлечении столбца.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-125">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-127"><a href="dn335232(v=exchg.10).md">грбит</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-127"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="5ad4e-128">Возвращает или задает параметры для извлечения столбца.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-128">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-130"><a href="dn335233(v=exchg.10).md">ибдата</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-130"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="5ad4e-131">Возвращает или задает смещение в буфере, в котором будут храниться данные.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-131">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-133"><a href="dn335234(v=exchg.10).md">иблонгвалуе</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="5ad4e-134">Возвращает или задает смещение для первого байта, получаемого из столбца типа <a href="hh577895(v=exchg.10).md">лонгбинари</a> или <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-134">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-136"><a href="dn351039(v=exchg.10).md">итагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="5ad4e-137">Возвращает или задает порядковый номер значений, содержащихся в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-137">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="5ad4e-138">Если значение Итагсекуенце равно 0, то вместо данных столбца возвращается число экземпляров многозначного столбца.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-138">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="5ad4e-140"><a href="dn351040(v=exchg.10).md">пвдата</a></span><span class="sxs-lookup"><span data-stu-id="5ad4e-140"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="5ad4e-141">Возвращает или задает буфер, в котором будут храниться данные, извлекаемые из столбца.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-141">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5ad4e-142">Начало</span><span class="sxs-lookup"><span data-stu-id="5ad4e-142">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5ad4e-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ad4e-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ad4e-144">Справочник</span><span class="sxs-lookup"><span data-stu-id="5ad4e-144">Reference</span></span>

[<span data-ttu-id="5ad4e-145">Класс JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="5ad4e-145">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="5ad4e-146">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5ad4e-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
