---
description: 'Дополнительные сведения: структура JET_ENUMCOLUMNID'
title: Структура JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541471"
---
# <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="2e91e-103">Структура JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="2e91e-103">JET_ENUMCOLUMNID Structure</span></span>


<span data-ttu-id="2e91e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2e91e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="2e91e-105">Структура JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="2e91e-105">JET_ENUMCOLUMNID Structure</span></span>

<span data-ttu-id="2e91e-106">Структура **JET_ENUMCOLUMNID** перечисляет конкретный набор столбцов и, при необходимости, конкретный набор нескольких значений для этих столбцов при использовании функции [жетенумератеколумнс](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="2e91e-106">The **JET_ENUMCOLUMNID** structure enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="2e91e-107">[Жетенумератеколумнс](./jetenumeratecolumns-function.md) возвращает массив структур **JET_ENUMCOLUMNID** .</span><span class="sxs-lookup"><span data-stu-id="2e91e-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNID** structures.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a><span data-ttu-id="2e91e-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="2e91e-108">Members</span></span>

<span data-ttu-id="2e91e-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="2e91e-109">**columnid**</span></span>

<span data-ttu-id="2e91e-110">Идентификатор столбца для перечисления.</span><span class="sxs-lookup"><span data-stu-id="2e91e-110">The column ID to enumerate.</span></span>

<span data-ttu-id="2e91e-111">Если идентификатор столбца равен 0 (нулю), то перечисление этого столбца пропускается, а соответствующая область в выходном массиве [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) структур будет создана с состоянием столбца JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="2e91e-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="2e91e-112">**ктагсекуенце**</span><span class="sxs-lookup"><span data-stu-id="2e91e-112">**ctagSequence**</span></span>

<span data-ttu-id="2e91e-113">При необходимости определяет массив значений столбца (по одному индексу) для перечисления по указанному ИДЕНТИФИКАТОРу столбца.</span><span class="sxs-lookup"><span data-stu-id="2e91e-113">Optionally identifies an array of column values (by one-based index) to enumerate for the specified column ID.</span></span>

<span data-ttu-id="2e91e-114">Если **ктагсекуенце** имеет значение 0 (ноль), то **ргтагсекуенце** игнорируется и все значения столбцов для указанного идентификатора столбца будут перечислены.</span><span class="sxs-lookup"><span data-stu-id="2e91e-114">If **ctagSequence** is 0 (zero) then **rgtagSequence** is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="2e91e-115">Если элемент **ргтагсекуенце** имеет значение 0 (ноль), то перечисление этого значения столбца (с помощью индекса, начинающегося с единицы) будет пропущено.</span><span class="sxs-lookup"><span data-stu-id="2e91e-115">If an element of **rgtagSequence** is 0 (zero), then the enumeration of that column value (by one-based index) will be skipped.</span></span> <span data-ttu-id="2e91e-116">Соответствующий слот в выходном массиве структуры **JET_ENUMCOLUMNID** будет создан со значением состояния столбца JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="2e91e-116">A corresponding slot in the output array of the **JET_ENUMCOLUMNID** structure will be generated with a column status value of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="2e91e-117">**ргтагсекуенце**</span><span class="sxs-lookup"><span data-stu-id="2e91e-117">**rgtagSequence**</span></span>

<span data-ttu-id="2e91e-118">Массив индексов, отсчитываемый от единицы, в массиве значений столбцов для данного столбца.</span><span class="sxs-lookup"><span data-stu-id="2e91e-118">An array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="2e91e-119">Единственный элемент — это **итагсекуенце** , который определен в [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="2e91e-119">A single element is an **itagSequence** which is defined in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="2e91e-120">**Итагсекуенце** 0 (ноль) означает "Skip".</span><span class="sxs-lookup"><span data-stu-id="2e91e-120">An **itagSequence** of 0 (zero) means "skip".</span></span> <span data-ttu-id="2e91e-121">**Итагсекуенце** 1 означает возврат значения первого столбца столбца, 2 — второй и т. д.</span><span class="sxs-lookup"><span data-stu-id="2e91e-121">An **itagSequence** of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

### <a name="requirements"></a><span data-ttu-id="2e91e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2e91e-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e91e-123"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="2e91e-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2e91e-124">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2e91e-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e91e-125"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2e91e-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2e91e-126">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2e91e-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e91e-127"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2e91e-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2e91e-128">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="2e91e-128">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2e91e-129">См. также:</span><span class="sxs-lookup"><span data-stu-id="2e91e-129">See Also</span></span>

[<span data-ttu-id="2e91e-130">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="2e91e-130">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="2e91e-131">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="2e91e-131">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="2e91e-132">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="2e91e-132">JET_ENUMCOLUMNID</span></span>]()  
[<span data-ttu-id="2e91e-133">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="2e91e-133">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="2e91e-134">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="2e91e-134">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
