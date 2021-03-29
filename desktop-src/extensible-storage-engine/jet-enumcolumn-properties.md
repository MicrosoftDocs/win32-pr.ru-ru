---
description: 'Дополнительные сведения о: JET_ENUMCOLUMN свойствах'
title: Свойства JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 69d0822e12078a7990615ebd401fb63e474a389e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897301"
---
# <a name="jet_enumcolumn-properties"></a><span data-ttu-id="50ec9-103">Свойства JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="50ec9-103">JET_ENUMCOLUMN properties</span></span>

<span data-ttu-id="50ec9-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="50ec9-104">Include protected members</span></span>  
<span data-ttu-id="50ec9-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="50ec9-105">Include inherited members</span></span>  

<span data-ttu-id="50ec9-106">Тип [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="50ec9-106">The [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="50ec9-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="50ec9-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="50ec9-108">Имя</span><span class="sxs-lookup"><span data-stu-id="50ec9-108">Name</span></span></th>
<th><span data-ttu-id="50ec9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="50ec9-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="50ec9-111"><a href="dn335137(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="50ec9-111"><a href="dn335137(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="50ec9-112">Возвращает размер значения, перечисленного для столбца.</span><span class="sxs-lookup"><span data-stu-id="50ec9-112">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="50ec9-113">Этот элемент используется, только если <a href="dn335086(v=exchg.10).md">Err</a> равен <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a>.</span><span class="sxs-lookup"><span data-stu-id="50ec9-113">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="50ec9-115"><a href="dn335085(v=exchg.10).md">ценумколумнвалуе</a></span><span class="sxs-lookup"><span data-stu-id="50ec9-115"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="50ec9-116">Возвращает количество значений столбца, перечисленных для столбца.</span><span class="sxs-lookup"><span data-stu-id="50ec9-116">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="50ec9-117">Этот элемент используется только в том случае, если <a href="dn335086(v=exchg.10).md">Err</a> не <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a>.</span><span class="sxs-lookup"><span data-stu-id="50ec9-117">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="50ec9-119"><a href="dn335135(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="50ec9-119"><a href="dn335135(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="50ec9-120">Возвращает идентификатор columnid, который был перечислен.</span><span class="sxs-lookup"><span data-stu-id="50ec9-120">Gets the columnid ID that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="50ec9-122"><a href="dn335086(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="50ec9-122"><a href="dn335086(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="50ec9-123">Возвращает код состояния столбца, полученный в результате перечисления.</span><span class="sxs-lookup"><span data-stu-id="50ec9-123">Gets the column status code that results from the enumeration.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="50ec9-125"><a href="dn335087(v=exchg.10).md">пвдата</a></span><span class="sxs-lookup"><span data-stu-id="50ec9-125"><a href="dn335087(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="50ec9-126">Возвращает значение, перечисленное для столбца.</span><span class="sxs-lookup"><span data-stu-id="50ec9-126">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="50ec9-127">Этот элемент используется, только если <a href="dn335086(v=exchg.10).md">Err</a> равен <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a>.</span><span class="sxs-lookup"><span data-stu-id="50ec9-127">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span> <span data-ttu-id="50ec9-128">Это указывает на память, выделенную с помощью обратного вызова <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> распределителя, переданного в <a href="dn292148(v=exchg.10).md">жетенумератеколумнс (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, енумератеколумнсгрбит)</a>.</span><span class="sxs-lookup"><span data-stu-id="50ec9-128">This points to memory allocated with the <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> allocator callback passed to <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span></span> <span data-ttu-id="50ec9-129">Не забудьте освободить память по завершении.</span><span class="sxs-lookup"><span data-stu-id="50ec9-129">Remember to release the memory when finished.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="50ec9-131"><a href="dn335089(v=exchg.10).md">рженумколумнвалуе</a></span><span class="sxs-lookup"><span data-stu-id="50ec9-131"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="50ec9-132">Возвращает перечисляемые значения столбцов для столбца.</span><span class="sxs-lookup"><span data-stu-id="50ec9-132">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="50ec9-133">Этот элемент используется только в том случае, если <a href="dn335086(v=exchg.10).md">Err</a> не <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a>.</span><span class="sxs-lookup"><span data-stu-id="50ec9-133">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50ec9-134">Начало</span><span class="sxs-lookup"><span data-stu-id="50ec9-134">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="50ec9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50ec9-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50ec9-136">Справочник</span><span class="sxs-lookup"><span data-stu-id="50ec9-136">Reference</span></span>

[<span data-ttu-id="50ec9-137">Класс JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="50ec9-137">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="50ec9-138">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="50ec9-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
