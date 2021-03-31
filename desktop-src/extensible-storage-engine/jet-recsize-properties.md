---
description: 'Дополнительные сведения о: JET_RECSIZE свойствах'
title: Свойства JET_RECSIZE (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913563"
---
# <a name="jet_recsize-properties"></a><span data-ttu-id="407fa-103">Свойства JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="407fa-103">JET_RECSIZE properties</span></span>

<span data-ttu-id="407fa-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="407fa-104">Include protected members</span></span>  
<span data-ttu-id="407fa-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="407fa-105">Include inherited members</span></span>  

<span data-ttu-id="407fa-106">Тип [JET_RECSIZE](./jet-recsize-structure2.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="407fa-106">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="407fa-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="407fa-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="407fa-108">Имя</span><span class="sxs-lookup"><span data-stu-id="407fa-108">Name</span></span></th>
<th><span data-ttu-id="407fa-109">Описание</span><span class="sxs-lookup"><span data-stu-id="407fa-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-111"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="407fa-111"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="407fa-112">Возвращает пользовательский набор данных в записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-112">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-114"><a href="hh596280(v=exchg.10).md">кбдатакомпрессед</a></span><span class="sxs-lookup"><span data-stu-id="407fa-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="407fa-115">Возвращает сжатый размер данных пользователя в записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-115">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="407fa-116">Это то же самое, что <a href="hh557581(v=exchg.10).md">cbData</a> , если никакие внутренние значения long не сжимаются).</span><span class="sxs-lookup"><span data-stu-id="407fa-116">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-118"><a href="hh557913(v=exchg.10).md">кблонгвалуедата</a></span><span class="sxs-lookup"><span data-stu-id="407fa-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="407fa-119">Возвращает пользовательский набор данных в записи, но хранится в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="407fa-119">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-121"><a href="hh566144(v=exchg.10).md">кблонгвалуедатакомпрессед</a></span><span class="sxs-lookup"><span data-stu-id="407fa-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="407fa-122">Возвращает сжатый размер пользовательских данных в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="407fa-122">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="407fa-123">Это то же самое, что и <a href="hh557913(v=exchg.10).md">кблонгвалуедата</a> , если не сжаты отдельные длинные значения.</span><span class="sxs-lookup"><span data-stu-id="407fa-123">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-125"><a href="hh558003(v=exchg.10).md">кблонгвалуеоверхеад</a></span><span class="sxs-lookup"><span data-stu-id="407fa-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="407fa-126">Возвращает дополнительную нагрузку на данные с длинными значениями.</span><span class="sxs-lookup"><span data-stu-id="407fa-126">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-128"><a href="hh565836(v=exchg.10).md">кбоверхеад</a></span><span class="sxs-lookup"><span data-stu-id="407fa-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="407fa-129">Возвращает дополнительную нагрузку на структуру записи ESENT для этой записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-129">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="407fa-130">Сюда входит размер ключа записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-130">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-132"><a href="hh566154(v=exchg.10).md">ккомпресседколумнс</a></span><span class="sxs-lookup"><span data-stu-id="407fa-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="407fa-133">Возвращает общее число сжатых столбцов в записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-133">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-135"><a href="hh596288(v=exchg.10).md">клонгвалуес</a></span><span class="sxs-lookup"><span data-stu-id="407fa-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="407fa-136">Возвращает общее количество значений long, хранящихся в дереве Long-Value для этой записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-136">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="407fa-137">Это не относится к внутренним длинным значениям.</span><span class="sxs-lookup"><span data-stu-id="407fa-137">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-139"><a href="hh577486(v=exchg.10).md">кмултивалуес</a></span><span class="sxs-lookup"><span data-stu-id="407fa-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="407fa-140">Возвращает совокупное число значений, находящихся за первым для всех столбцов в записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-140">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-142"><a href="hh578172(v=exchg.10).md">кнонтагжедколумнс</a></span><span class="sxs-lookup"><span data-stu-id="407fa-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="407fa-143">Возвращает общее число фиксированных и переменных столбцов, заданных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-143">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="407fa-145"><a href="hh566034(v=exchg.10).md">ктагжедколумнс</a></span><span class="sxs-lookup"><span data-stu-id="407fa-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="407fa-146">Возвращает общее число столбцов с тегами, заданных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="407fa-146">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="407fa-147">Начало</span><span class="sxs-lookup"><span data-stu-id="407fa-147">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="407fa-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="407fa-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="407fa-149">Справочник</span><span class="sxs-lookup"><span data-stu-id="407fa-149">Reference</span></span>

[<span data-ttu-id="407fa-150">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="407fa-150">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="407fa-151">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="407fa-151">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
