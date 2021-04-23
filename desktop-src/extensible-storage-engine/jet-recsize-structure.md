---
description: 'Дополнительные сведения: структура JET_RECSIZE'
title: Структура JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808542"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="c14a7-103">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="c14a7-103">JET_RECSIZE Structure</span></span>


<span data-ttu-id="c14a7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c14a7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize-structure"></a><span data-ttu-id="c14a7-105">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="c14a7-105">JET_RECSIZE Structure</span></span>

<span data-ttu-id="c14a7-106">Структура **JET_RECSIZE** используется [жетжетрекордсизе](./jetgetrecordsize-function.md) для получения сведений о требованиях к использованию записи в пространстве данных пользователя, количестве столбцов набора, количестве значений и служебной нагрузке на структуру записи ESE.</span><span class="sxs-lookup"><span data-stu-id="c14a7-106">The **JET_RECSIZE** structure is used by [JetGetRecordSize](./jetgetrecordsize-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="c14a7-107">**Windows Vista:** Структура **JET_RECSIZE** появилась в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c14a7-107">**Windows Vista:** The **JET_RECSIZE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a><span data-ttu-id="c14a7-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="c14a7-108">Members</span></span>

<span data-ttu-id="c14a7-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="c14a7-109">**cbData**</span></span>

<span data-ttu-id="c14a7-110">Пользовательский набор данных в записи.</span><span class="sxs-lookup"><span data-stu-id="c14a7-110">User data set in the record.</span></span>

<span data-ttu-id="c14a7-111">**Примечание**  .  Размер ключа не включен в этот раздел.</span><span class="sxs-lookup"><span data-stu-id="c14a7-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="c14a7-112">**кблонгвалуедата**</span><span class="sxs-lookup"><span data-stu-id="c14a7-112">**cbLongValueData**</span></span>

<span data-ttu-id="c14a7-113">Данные пользователя, связанные с записью, но хранимые в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="c14a7-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="c14a7-114">**Примечание**  .  Это не учитывает внутренние значения long.</span><span class="sxs-lookup"><span data-stu-id="c14a7-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="c14a7-115">**кбоверхеад**</span><span class="sxs-lookup"><span data-stu-id="c14a7-115">**cbOverhead**</span></span>

<span data-ttu-id="c14a7-116">Издержки структуры записи ESE для этой записи.</span><span class="sxs-lookup"><span data-stu-id="c14a7-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="c14a7-117">Сюда входит размер ключа записи.</span><span class="sxs-lookup"><span data-stu-id="c14a7-117">This includes the record's key size.</span></span>

<span data-ttu-id="c14a7-118">**кблонгвалуеоверхеад**</span><span class="sxs-lookup"><span data-stu-id="c14a7-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="c14a7-119">Затраты на данные длинных значений.</span><span class="sxs-lookup"><span data-stu-id="c14a7-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="c14a7-120">**Примечание**  .  Это не учитывает внутренние значения long.</span><span class="sxs-lookup"><span data-stu-id="c14a7-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="c14a7-121">**кнонтагжедколумнс**</span><span class="sxs-lookup"><span data-stu-id="c14a7-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="c14a7-122">Общее число фиксированных и переменных столбцов, заданных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="c14a7-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="c14a7-123">**ктагжедколумнс**</span><span class="sxs-lookup"><span data-stu-id="c14a7-123">**cTaggedColumns**</span></span>

<span data-ttu-id="c14a7-124">Общее число столбцов с тегами, заданных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="c14a7-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="c14a7-125">**клонгвалуес**</span><span class="sxs-lookup"><span data-stu-id="c14a7-125">**cLongValues**</span></span>

<span data-ttu-id="c14a7-126">Общее число значений long, хранящихся в дереве Long-Value для этой записи.</span><span class="sxs-lookup"><span data-stu-id="c14a7-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="c14a7-127">**Примечание**  .  Это не учитывает внутренние значения long.</span><span class="sxs-lookup"><span data-stu-id="c14a7-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="c14a7-128">**кмултивалуес**</span><span class="sxs-lookup"><span data-stu-id="c14a7-128">**cMultiValues**</span></span>

<span data-ttu-id="c14a7-129">Совокупность общего количества значений, находящихся за первым для всех столбцов в записи.</span><span class="sxs-lookup"><span data-stu-id="c14a7-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

### <a name="remarks"></a><span data-ttu-id="c14a7-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c14a7-130">Remarks</span></span>

<span data-ttu-id="c14a7-131">Общее число значений в записи будет **кмултивалуес**  +  **кнонтагжедколумнс**  +  **ктагжедколумнс**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-131">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

### <a name="requirements"></a><span data-ttu-id="c14a7-132">Требования</span><span class="sxs-lookup"><span data-stu-id="c14a7-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c14a7-133"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c14a7-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c14a7-134">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c14a7-134">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c14a7-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c14a7-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c14a7-136">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c14a7-136">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c14a7-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c14a7-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c14a7-138">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c14a7-138">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c14a7-139">См. также:</span><span class="sxs-lookup"><span data-stu-id="c14a7-139">See Also</span></span>

[<span data-ttu-id="c14a7-140">жетжетрекордсизе</span><span class="sxs-lookup"><span data-stu-id="c14a7-140">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)
