---
description: 'Дополнительные сведения: структура JET_RECSIZE2'
title: Структура JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702626"
---
# <a name="jet_recsize2-structure"></a><span data-ttu-id="32338-103">Структура JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="32338-103">JET_RECSIZE2 Structure</span></span>


<span data-ttu-id="32338-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="32338-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize2-structure"></a><span data-ttu-id="32338-105">Структура JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="32338-105">JET_RECSIZE2 Structure</span></span>

<span data-ttu-id="32338-106">Структура **JET_RECSIZE2** используется [JetGetRecordSize2](./jetgetrecordsize2-function.md) для получения сведений о требованиях к использованию записи в пространстве данных пользователя, количестве столбцов набора, количестве значений и служебной нагрузке на структуру записи ESE.</span><span class="sxs-lookup"><span data-stu-id="32338-106">The **JET_RECSIZE2** structure is used by [JetGetRecordSize2](./jetgetrecordsize2-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="32338-107">**Windows 7:** Структура **JET_RECSIZE2** введена в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32338-107">**Windows 7:** The **JET_RECSIZE2** structure is introduced in the Windows 7 operating system.</span></span>

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
```

### <a name="members"></a><span data-ttu-id="32338-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="32338-108">Members</span></span>

<span data-ttu-id="32338-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="32338-109">**cbData**</span></span>

<span data-ttu-id="32338-110">Пользовательский набор данных в записи.</span><span class="sxs-lookup"><span data-stu-id="32338-110">User data set in the record.</span></span>

<span data-ttu-id="32338-111">**Примечание**  .  Размер ключа не включен в этот раздел.</span><span class="sxs-lookup"><span data-stu-id="32338-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="32338-112">**кблонгвалуедата**</span><span class="sxs-lookup"><span data-stu-id="32338-112">**cbLongValueData**</span></span>

<span data-ttu-id="32338-113">Данные пользователя, связанные с записью, но хранимые в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="32338-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="32338-114">**Примечание**  .  Это не учитывает внутренние значения long.</span><span class="sxs-lookup"><span data-stu-id="32338-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="32338-115">**кбоверхеад**</span><span class="sxs-lookup"><span data-stu-id="32338-115">**cbOverhead**</span></span>

<span data-ttu-id="32338-116">Издержки структуры записи ESE для этой записи.</span><span class="sxs-lookup"><span data-stu-id="32338-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="32338-117">Сюда входит размер ключа записи.</span><span class="sxs-lookup"><span data-stu-id="32338-117">This includes the record's key size.</span></span>

<span data-ttu-id="32338-118">**кблонгвалуеоверхеад**</span><span class="sxs-lookup"><span data-stu-id="32338-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="32338-119">Затраты на данные длинных значений.</span><span class="sxs-lookup"><span data-stu-id="32338-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="32338-120">**Примечание**  .  Это не учитывает внутренние значения long.</span><span class="sxs-lookup"><span data-stu-id="32338-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="32338-121">**кнонтагжедколумнс**</span><span class="sxs-lookup"><span data-stu-id="32338-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="32338-122">Общее число фиксированных и переменных столбцов, заданных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="32338-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="32338-123">**ктагжедколумнс**</span><span class="sxs-lookup"><span data-stu-id="32338-123">**cTaggedColumns**</span></span>

<span data-ttu-id="32338-124">Общее число столбцов с тегами, заданных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="32338-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="32338-125">**клонгвалуес**</span><span class="sxs-lookup"><span data-stu-id="32338-125">**cLongValues**</span></span>

<span data-ttu-id="32338-126">Общее число значений long, хранящихся в дереве Long-Value для этой записи.</span><span class="sxs-lookup"><span data-stu-id="32338-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="32338-127">**Примечание**  .  Это не учитывает внутренние значения long.</span><span class="sxs-lookup"><span data-stu-id="32338-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="32338-128">**кмултивалуес**</span><span class="sxs-lookup"><span data-stu-id="32338-128">**cMultiValues**</span></span>

<span data-ttu-id="32338-129">Совокупность общего количества значений, находящихся за первым для всех столбцов в записи.</span><span class="sxs-lookup"><span data-stu-id="32338-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

<span data-ttu-id="32338-130">**ккомпресседколумнс**</span><span class="sxs-lookup"><span data-stu-id="32338-130">**cCompressedColumns**</span></span>

<span data-ttu-id="32338-131">Общее число сжатых столбцов.</span><span class="sxs-lookup"><span data-stu-id="32338-131">The total number of compressed columns.</span></span>

<span data-ttu-id="32338-132">**кбдатакомпрессед**</span><span class="sxs-lookup"><span data-stu-id="32338-132">**cbDataCompressed**</span></span>

<span data-ttu-id="32338-133">Сжатый размер данных пользователя в этой записи.</span><span class="sxs-lookup"><span data-stu-id="32338-133">The compressed size of user data in this record.</span></span> <span data-ttu-id="32338-134">Это то же самое, что и cbData, если никакие внутренние значения long не сжимаются.</span><span class="sxs-lookup"><span data-stu-id="32338-134">This is the same as cbData if no intrinsic long-values are compressed.</span></span>

<span data-ttu-id="32338-135">**кблонгвалуедатакомпрессед**</span><span class="sxs-lookup"><span data-stu-id="32338-135">**cbLongValueDataCompressed**</span></span>

<span data-ttu-id="32338-136">Сжатый размер данных пользователя в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="32338-136">The compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="32338-137">Это то же самое, что и данные Кблонгвалуе, если не сжаты отдельные длинные значения.</span><span class="sxs-lookup"><span data-stu-id="32338-137">This is the same as cbLongValue data if no separated long values are compressed.</span></span>

### <a name="remarks"></a><span data-ttu-id="32338-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32338-138">Remarks</span></span>

<span data-ttu-id="32338-139">Общее число значений в записи будет **кмултивалуес**  +  **кнонтагжедколумнс**  +  **ктагжедколумнс**.</span><span class="sxs-lookup"><span data-stu-id="32338-139">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

<span data-ttu-id="32338-140">Логическими данными в записи является (cbData + Кблонгвалуедата), а физическим размером данных является (Кбдатакомпрессед + Кблонгвалуедатакомпрессед).</span><span class="sxs-lookup"><span data-stu-id="32338-140">The logical data in the record is (cbData+cbLongValueData) and the physical size of the data is (cbDataCompressed+cbLongValueDataCompressed).</span></span> <span data-ttu-id="32338-141">Это можно использовать для вычисления коэффициента сжатия сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="32338-141">This can be used to calculate the compression ratio of stored data.</span></span>

### <a name="requirements"></a><span data-ttu-id="32338-142">Требования</span><span class="sxs-lookup"><span data-stu-id="32338-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32338-143"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="32338-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="32338-144">Требуется операционная система Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32338-144">Requires Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32338-145"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="32338-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="32338-146">Требуется операционная система Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="32338-146">Requires Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32338-147"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="32338-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="32338-148">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="32338-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="32338-149">См. также:</span><span class="sxs-lookup"><span data-stu-id="32338-149">See Also</span></span>

[<span data-ttu-id="32338-150">жетжетрекордсизе</span><span class="sxs-lookup"><span data-stu-id="32338-150">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)  
[<span data-ttu-id="32338-151">JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="32338-151">JetGetRecordSize2</span></span>](./jetgetrecordsize2-function.md)
