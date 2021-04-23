---
description: Дополнительные сведения о методе API. Жетретриевеколумн
title: API. Жетретриевеколумн, метод
TOCTitle: 'JetRetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100791
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: e4e43d57f4393d6b0d4ce2f1cdbe4ecd8338ec54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272733"
---
# <a name="apijetretrievecolumn-method"></a><span data-ttu-id="f1ea0-103">API. Жетретриевеколумн, метод</span><span class="sxs-lookup"><span data-stu-id="f1ea0-103">Api.JetRetrieveColumn method</span></span>

<span data-ttu-id="f1ea0-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="f1ea0-104">Include protected members</span></span>  
<span data-ttu-id="f1ea0-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="f1ea0-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="f1ea0-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="f1ea0-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f1ea0-107">Имя</span><span class="sxs-lookup"><span data-stu-id="f1ea0-107">Name</span></span></th>
<th><span data-ttu-id="f1ea0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f1ea0-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="f1ea0-111"><a href="dn332995(v=exchg.10).md">Жетретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Ретриевеколумнгрбит, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="f1ea0-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="f1ea0-112">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="f1ea0-113">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-113">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="f1ea0-114">Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-114">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="f1ea0-115">Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-115">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="f1ea0-116">Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-116">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="f1ea0-119"><a href="dn332997(v=exchg.10).md">Жетретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, Ретриевеколумнгрбит, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="f1ea0-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="f1ea0-120">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-120">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="f1ea0-121">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-121">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="f1ea0-122">Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-122">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="f1ea0-123">Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-123">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="f1ea0-124">Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</span><span class="sxs-lookup"><span data-stu-id="f1ea0-124">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1ea0-125">Начало</span><span class="sxs-lookup"><span data-stu-id="f1ea0-125">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f1ea0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1ea0-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f1ea0-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="f1ea0-127">Reference</span></span>

[<span data-ttu-id="f1ea0-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="f1ea0-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f1ea0-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="f1ea0-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f1ea0-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f1ea0-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
