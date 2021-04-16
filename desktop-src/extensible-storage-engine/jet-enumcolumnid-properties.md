---
description: 'Дополнительные сведения о: JET_ENUMCOLUMNID свойствах'
title: Свойства JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540063"
---
# <a name="jet_enumcolumnid-properties"></a><span data-ttu-id="ef4c4-103">Свойства JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="ef4c4-103">JET_ENUMCOLUMNID properties</span></span>

<span data-ttu-id="ef4c4-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="ef4c4-104">Include protected members</span></span>  
<span data-ttu-id="ef4c4-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="ef4c4-105">Include inherited members</span></span>  

<span data-ttu-id="ef4c4-106">Тип [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-106">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="ef4c4-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef4c4-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ef4c4-108">Имя</span><span class="sxs-lookup"><span data-stu-id="ef4c4-108">Name</span></span></th>
<th><span data-ttu-id="ef4c4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ef4c4-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ef4c4-111"><a href="dn335141(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="ef4c4-111"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="ef4c4-112">Возвращает или задает идентификатор columnid для перечисления.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-112">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ef4c4-114"><a href="dn335092(v=exchg.10).md">ктагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="ef4c4-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="ef4c4-115">Возвращает или задает количество значений столбца (по одному индексу) для перечисления по указанному ИДЕНТИФИКАТОРу столбца.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-115">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="ef4c4-116">Если Ктагсекуенце имеет значение 0 (ноль), то Ргтагсекуенце игнорируется и все значения столбцов для указанного идентификатора столбца будут перечислены.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-116">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ef4c4-118"><a href="dn335093(v=exchg.10).md">ргтагсекуенце</a></span><span class="sxs-lookup"><span data-stu-id="ef4c4-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="ef4c4-119">Возвращает или задает массив индексов, отсчитываемый от единицы, в массиве значений столбцов для данного столбца.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-119">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="ef4c4-120">Единственный элемент — это Итагсекуенце, который определен в JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-120">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="ef4c4-121">Итагсекуенце 0 (ноль) означает &quot; пропуск &quot; .</span><span class="sxs-lookup"><span data-stu-id="ef4c4-121">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="ef4c4-122">Итагсекуенце 1 означает возврат значения первого столбца столбца, 2 — второй и т. д.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-122">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef4c4-123">Начало</span><span class="sxs-lookup"><span data-stu-id="ef4c4-123">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ef4c4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef4c4-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef4c4-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="ef4c4-125">Reference</span></span>

[<span data-ttu-id="ef4c4-126">Класс JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="ef4c4-126">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="ef4c4-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ef4c4-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
