---
description: 'Дополнительные сведения: структура JET_ENUMCOLUMN'
title: Структура JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143612"
---
# <a name="jet_enumcolumn-structure"></a><span data-ttu-id="60910-103">Структура JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="60910-103">JET_ENUMCOLUMN Structure</span></span>


<span data-ttu-id="60910-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60910-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumn-structure"></a><span data-ttu-id="60910-105">Структура JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="60910-105">JET_ENUMCOLUMN Structure</span></span>

<span data-ttu-id="60910-106">Структура **JET_ENUMCOLUMN** перечисляет значения столбцов записи a при использовании функции [жетенумератеколумнс](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="60910-106">The **JET_ENUMCOLUMN** structure enumerates the column values of a record when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="60910-107">[Жетенумератеколумнс](./jetenumeratecolumns-function.md) возвращает массив структур **JET_ENUMCOLUMN** .</span><span class="sxs-lookup"><span data-stu-id="60910-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMN** structures.</span></span> <span data-ttu-id="60910-108">Массив возвращается в памяти, выделенной с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено этому API.</span><span class="sxs-lookup"><span data-stu-id="60910-108">The array is returned in memory that is allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that API.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a><span data-ttu-id="60910-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="60910-109">Members</span></span>

<span data-ttu-id="60910-110">**columnid**</span><span class="sxs-lookup"><span data-stu-id="60910-110">**columnid**</span></span>

<span data-ttu-id="60910-111">Идентификатор столбца, который был перечислен.</span><span class="sxs-lookup"><span data-stu-id="60910-111">The column ID that was enumerated.</span></span>

<span data-ttu-id="60910-112">**Err**</span><span class="sxs-lookup"><span data-stu-id="60910-112">**err**</span></span>

<span data-ttu-id="60910-113">Код состояния столбца, полученный в результате перечисления столбца.</span><span class="sxs-lookup"><span data-stu-id="60910-113">The column status code that results from the enumeration of the column.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60910-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="60910-114">Error Codes</span></span></p></th>
<th><p><span data-ttu-id="60910-115">Значение</span><span class="sxs-lookup"><span data-stu-id="60910-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60910-116">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="60910-116">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="60910-117">Идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="60910-117">The column ID is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60910-118">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="60910-118">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="60910-119">Столбец, описываемый ИДЕНТИФИКАТОРом столбца, не существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="60910-119">The column described by the column ID does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60910-120">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="60910-120">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="60910-121">Все значения для этого столбца равны NULL.</span><span class="sxs-lookup"><span data-stu-id="60910-121">All values for this column are NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60910-122">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="60910-122">JET_wrnColumnPresent</span></span></p></td>
<td><p><span data-ttu-id="60910-123">Указан JET_bitEnumeratePresenceOnly, и для этого столбца было возвращено по крайней мере одно значение столбца, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="60910-123">JET_bitEnumeratePresenceOnly was specified and at least one non-NULL column value would have been returned for this column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60910-124">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="60910-124">JET_wrnColumnSingleValue</span></span></p></td>
<td><p><span data-ttu-id="60910-125">Указан JET_bitEnumerateCompressOutput, и для этого столбца возвращено ровно одно значение столбца, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="60910-125">JET_bitEnumerateCompressOutput was specified and exactly one non-NULL column value has been returned for this column.</span></span> <span data-ttu-id="60910-126">В результате возвращается сжатая форма <strong>JET_ENUMCOLUMN</strong> .</span><span class="sxs-lookup"><span data-stu-id="60910-126">As a result, the compressed form of <strong>JET_ENUMCOLUMN</strong> has been returned.</span></span> <span data-ttu-id="60910-127">Дополнительные сведения см. в разделе <strong>JET_ENUMCOLUMN</strong> .</span><span class="sxs-lookup"><span data-stu-id="60910-127">See <strong>JET_ENUMCOLUMN</strong> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60910-128">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="60910-128">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="60910-129">Идентификатор столбца в структуре <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> , соответствующей этой <strong>JET_ENUMCOLUMN</strong> структуре, равен нулю.</span><span class="sxs-lookup"><span data-stu-id="60910-129">The column ID in the <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct corresponding to this <strong>JET_ENUMCOLUMN</strong> struct was zero.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60910-130">**ценумколумнвалуе**</span><span class="sxs-lookup"><span data-stu-id="60910-130">**cEnumColumnValue**</span></span>

<span data-ttu-id="60910-131">Массив значений столбца, перечисленных для столбца.</span><span class="sxs-lookup"><span data-stu-id="60910-131">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="60910-132">Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="60910-132">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="60910-133">Этот выходной буфер используется, когда код состояния столбца не равен JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="60910-133">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="60910-134">Дополнительные сведения см. в разделе [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="60910-134">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="60910-135">Возвращается, если "Err \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="60910-135">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="60910-136">**рженумколумнвалуе**</span><span class="sxs-lookup"><span data-stu-id="60910-136">**rgEnumColumnValue**</span></span>

<span data-ttu-id="60910-137">Массив значений столбца, перечисленных для столбца.</span><span class="sxs-lookup"><span data-stu-id="60910-137">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="60910-138">Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="60910-138">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="60910-139">Этот выходной буфер используется, когда код состояния столбца не равен JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="60910-139">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="60910-140">Дополнительные сведения см. в разделе [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="60910-140">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="60910-141">Возвращается, если "Err \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="60910-141">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="60910-142">**cbData**</span><span class="sxs-lookup"><span data-stu-id="60910-142">**cbData**</span></span>

<span data-ttu-id="60910-143">Значение столбца, перечисленное для столбца.</span><span class="sxs-lookup"><span data-stu-id="60910-143">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="60910-144">Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="60910-144">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="60910-145">Этот выходной буфер используется только в том случае, если код состояния столбца имеет значение JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="60910-145">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="60910-146">Дополнительные сведения см. в разделе [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="60910-146">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="60910-147">Возвращается, если "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="60910-147">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="60910-148">**пвдата**</span><span class="sxs-lookup"><span data-stu-id="60910-148">**pvData**</span></span>

<span data-ttu-id="60910-149">Значение столбца, перечисленное для столбца.</span><span class="sxs-lookup"><span data-stu-id="60910-149">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="60910-150">Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="60910-150">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="60910-151">Этот выходной буфер используется только в том случае, если код состояния столбца имеет значение JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="60910-151">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="60910-152">Дополнительные сведения см. в разделе [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="60910-152">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="60910-153">Возвращается, если "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="60910-153">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

### <a name="requirements"></a><span data-ttu-id="60910-154">Требования</span><span class="sxs-lookup"><span data-stu-id="60910-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60910-155"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="60910-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="60910-156">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="60910-156">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60910-157"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="60910-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="60910-158">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="60910-158">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60910-159"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="60910-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="60910-160">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="60910-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="60910-161">См. также:</span><span class="sxs-lookup"><span data-stu-id="60910-161">See Also</span></span>

[<span data-ttu-id="60910-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="60910-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="60910-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="60910-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="60910-164">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="60910-164">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="60910-165">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="60910-165">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="60910-166">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="60910-166">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="60910-167">realloc</span><span class="sxs-lookup"><span data-stu-id="60910-167">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
