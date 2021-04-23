---
description: 'Дополнительные сведения о: JET_SETINFO свойствах'
title: Свойства JET_SETINFO
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144248"
---
# <a name="jet_setinfo-properties"></a><span data-ttu-id="57adf-103">Свойства JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="57adf-103">JET_SETINFO properties</span></span>

<span data-ttu-id="57adf-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="57adf-104">Include protected members</span></span>  
<span data-ttu-id="57adf-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="57adf-105">Include inherited members</span></span>  

<span data-ttu-id="57adf-106">Тип [JET_SETINFO](./jet-setinfo-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="57adf-106">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="57adf-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="57adf-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="57adf-108">Имя</span><span class="sxs-lookup"><span data-stu-id="57adf-108">Name</span></span></th>
<th><span data-ttu-id="57adf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="57adf-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="57adf-111"><a href="dn351064(v=exchg.10).md">иблонгвалуе</a></span><span class="sxs-lookup"><span data-stu-id="57adf-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="57adf-112">Возвращает или задает смещение для первого байта, который необходимо задать в столбце типа <a href="hh577895(v=exchg.10).md">лонгбинари</a> или <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="57adf-112">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="57adf-114"><a href="dn351037(v=exchg.10).md">итагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="57adf-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="57adf-115">Возвращает или задает порядковый номер значения в столбце с несколькими значениями, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="57adf-115">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="57adf-116">Массив значений является исходным.</span><span class="sxs-lookup"><span data-stu-id="57adf-116">The array of values is one-based.</span></span> <span data-ttu-id="57adf-117">Первое значение — Sequence 1, а не 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="57adf-117">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="57adf-118">Если столбец записи имеет только одно значение, то значение 1 должно передаваться как Итагсекуенце при замене этого значения.</span><span class="sxs-lookup"><span data-stu-id="57adf-118">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="57adf-119">Значение 0 (ноль) означает, что новый экземпляр значения столбца добавляется в конец последовательности значений столбцов.</span><span class="sxs-lookup"><span data-stu-id="57adf-119">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57adf-120">Начало</span><span class="sxs-lookup"><span data-stu-id="57adf-120">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="57adf-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57adf-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="57adf-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="57adf-122">Reference</span></span>

[<span data-ttu-id="57adf-123">Класс JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="57adf-123">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="57adf-124">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="57adf-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
