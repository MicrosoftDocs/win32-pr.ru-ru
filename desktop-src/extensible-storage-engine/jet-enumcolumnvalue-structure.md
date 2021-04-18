---
description: 'Дополнительные сведения: структура JET_ENUMCOLUMNVALUE'
title: Структура JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693436"
---
# <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="f420d-103">Структура JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="f420d-103">JET_ENUMCOLUMNVALUE Structure</span></span>


<span data-ttu-id="f420d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f420d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="f420d-105">Структура JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="f420d-105">JET_ENUMCOLUMNVALUE Structure</span></span>

<span data-ttu-id="f420d-106">Структура **JET_ENUMCOLUMNVALUE** перечисляет значения столбцов записи с помощью функции [жетенумератеколумнс](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f420d-106">The **JET_ENUMCOLUMNVALUE** structure enumerates the column values of a record using the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function.</span></span> <span data-ttu-id="f420d-107">[Жетенумератеколумнс](./jetenumeratecolumns-function.md) возвращает массив структур **JET_ENUMCOLUMNVALUE** .</span><span class="sxs-lookup"><span data-stu-id="f420d-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNVALUE** structures.</span></span> <span data-ttu-id="f420d-108">Массив возвращается в памяти, выделенной с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено этой функции.</span><span class="sxs-lookup"><span data-stu-id="f420d-108">The array is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that function.</span></span>

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a><span data-ttu-id="f420d-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="f420d-109">Members</span></span>

<span data-ttu-id="f420d-110">**итагсекуенце**</span><span class="sxs-lookup"><span data-stu-id="f420d-110">**itagSequence**</span></span>

<span data-ttu-id="f420d-111">Значение столбца (по основанному на единицу индексу), которое было перечислено.</span><span class="sxs-lookup"><span data-stu-id="f420d-111">The column value (by one-based index) that was enumerated.</span></span>

<span data-ttu-id="f420d-112">**Err**</span><span class="sxs-lookup"><span data-stu-id="f420d-112">**err**</span></span>

<span data-ttu-id="f420d-113">Код состояния столбца, полученный в результате перечисления значения столбца.</span><span class="sxs-lookup"><span data-stu-id="f420d-113">The column status code resulting from the enumeration of the column value.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f420d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f420d-114">Value</span></span></p></th>
<th><p><span data-ttu-id="f420d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f420d-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f420d-116">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="f420d-116">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="f420d-117">Запрошенное значение столбца равно NULL.</span><span class="sxs-lookup"><span data-stu-id="f420d-117">The requested column value is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f420d-118">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="f420d-118">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="f420d-119"><em>Итагсекуенце</em> , указанный в элементе массива <em>ргтагсекуенце</em> в структуре <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> , соответствующей этой <strong>JET_ENUMCOLUMNVALUE</strong> структуре, была нулевой.</span><span class="sxs-lookup"><span data-stu-id="f420d-119">The <em>itagSequence</em> that is specified in the element of the <em>rgtagSequence</em> array in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct corresponding to this <strong>JET_ENUMCOLUMNVALUE</strong> struct was zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f420d-120">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="f420d-120">JET_wrnColumnTruncated</span></span></p></td>
<td><p><span data-ttu-id="f420d-121">Значение запрошенного столбца было усечено до указанного размера перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="f420d-121">The requested column value was truncated to the specified size before being returned.</span></span></p>
<p><span data-ttu-id="f420d-122">Это усечение происходит только для длинных текстовых и длинных двоичных столбцов, содержащих большие объемы данных.</span><span class="sxs-lookup"><span data-stu-id="f420d-122">This truncation occurs only for long text and long binary columns that contain large amounts of data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f420d-123">**cbData**</span><span class="sxs-lookup"><span data-stu-id="f420d-123">**cbData**</span></span>

<span data-ttu-id="f420d-124">Значение столбца, перечисленное для столбца.</span><span class="sxs-lookup"><span data-stu-id="f420d-124">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="f420d-125">Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="f420d-125">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="f420d-126">**пвдата**</span><span class="sxs-lookup"><span data-stu-id="f420d-126">**pvData**</span></span>

<span data-ttu-id="f420d-127">Значение столбца, перечисленное для столбца.</span><span class="sxs-lookup"><span data-stu-id="f420d-127">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="f420d-128">Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="f420d-128">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="f420d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f420d-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f420d-130"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f420d-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f420d-131">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f420d-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f420d-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f420d-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f420d-133">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f420d-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f420d-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f420d-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f420d-135">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f420d-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f420d-136">См. также:</span><span class="sxs-lookup"><span data-stu-id="f420d-136">See Also</span></span>

[<span data-ttu-id="f420d-137">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="f420d-137">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="f420d-138">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="f420d-138">JET_ENUMCOLUMNVALUE</span></span>]()  
[<span data-ttu-id="f420d-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f420d-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f420d-140">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="f420d-140">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="f420d-141">realloc</span><span class="sxs-lookup"><span data-stu-id="f420d-141">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
