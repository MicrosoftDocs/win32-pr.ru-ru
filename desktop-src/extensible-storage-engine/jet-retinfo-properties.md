---
description: 'Дополнительные сведения о: JET_RETINFO свойствах'
title: Свойства JET_RETINFO
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556122"
---
# <a name="jet_retinfo-properties"></a><span data-ttu-id="72f6c-103">Свойства JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="72f6c-103">JET_RETINFO properties</span></span>

<span data-ttu-id="72f6c-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="72f6c-104">Include protected members</span></span>  
<span data-ttu-id="72f6c-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="72f6c-105">Include inherited members</span></span>  

<span data-ttu-id="72f6c-106">Тип [JET_RETINFO](./jet-retinfo-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="72f6c-106">The [JET_RETINFO](./jet-retinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="72f6c-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="72f6c-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="72f6c-108">Имя</span><span class="sxs-lookup"><span data-stu-id="72f6c-108">Name</span></span></th>
<th><span data-ttu-id="72f6c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="72f6c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="72f6c-111"><a href="dn335221(v=exchg.10).md">колумниднексттагжед</a></span><span class="sxs-lookup"><span data-stu-id="72f6c-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="72f6c-112">Получает значение columnid полученного помеченного, многозначного или разреженного столбца, когда все отмеченные столбцы извлекаются путем передачи 0 в качестве значения columnid в Жетретриевеколумн.</span><span class="sxs-lookup"><span data-stu-id="72f6c-112">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="72f6c-114"><a href="dn335220(v=exchg.10).md">иблонгвалуе</a></span><span class="sxs-lookup"><span data-stu-id="72f6c-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="72f6c-115">Возвращает или задает смещение для первого байта, получаемого из столбца типа <a href="hh577895(v=exchg.10).md">лонгбинари</a>или <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="72f6c-115">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a>, or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="72f6c-117"><a href="dn351035(v=exchg.10).md">итагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="72f6c-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="72f6c-118">Возвращает или задает порядковый номер значения в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="72f6c-118">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="72f6c-119">Массив значений является исходным.</span><span class="sxs-lookup"><span data-stu-id="72f6c-119">The array of values is one-based.</span></span> <span data-ttu-id="72f6c-120">Первое значение — Sequence 1, а не 0.</span><span class="sxs-lookup"><span data-stu-id="72f6c-120">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="72f6c-121">Если столбец записи имеет только одно значение, то в качестве Итагсекуенце передается 1.</span><span class="sxs-lookup"><span data-stu-id="72f6c-121">If the record column has only one value then 1 should be passed as the itagSequence.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72f6c-122">Начало</span><span class="sxs-lookup"><span data-stu-id="72f6c-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="72f6c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72f6c-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="72f6c-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="72f6c-124">Reference</span></span>

[<span data-ttu-id="72f6c-125">Класс JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="72f6c-125">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="72f6c-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="72f6c-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
