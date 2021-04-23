---
description: Дополнительные сведения о методе API. Ретриевеколумн
title: API. Ретриевеколумн, метод
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 3bcb5effcfc59e155007fbd9e1733d95db058970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816993"
---
# <a name="apiretrievecolumn-method"></a><span data-ttu-id="d5385-103">API. Ретриевеколумн, метод</span><span class="sxs-lookup"><span data-stu-id="d5385-103">Api.RetrieveColumn method</span></span>

<span data-ttu-id="d5385-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="d5385-104">Include protected members</span></span>  
<span data-ttu-id="d5385-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="d5385-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="d5385-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="d5385-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d5385-107">Имя</span><span class="sxs-lookup"><span data-stu-id="d5385-107">Name</span></span></th>
<th><span data-ttu-id="d5385-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d5385-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="d5385-111"><a href="dn334041(v=exchg.10).md">Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span><span class="sxs-lookup"><span data-stu-id="d5385-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="d5385-112">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d5385-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="d5385-113">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="d5385-113">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="d5385-116"><a href="dn334060(v=exchg.10).md">Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="d5385-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="d5385-117">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d5385-117">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="d5385-118">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="d5385-118">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="d5385-119">Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора.</span><span class="sxs-lookup"><span data-stu-id="d5385-119">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="d5385-120">Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="d5385-120">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="d5385-121">Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</span><span class="sxs-lookup"><span data-stu-id="d5385-121">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d5385-122">Начало</span><span class="sxs-lookup"><span data-stu-id="d5385-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="d5385-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5385-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d5385-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="d5385-124">Reference</span></span>

[<span data-ttu-id="d5385-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="d5385-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d5385-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="d5385-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d5385-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d5385-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
