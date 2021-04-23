---
description: Дополнительные сведения о функции Жетосснапшоттрункателогинстанце
title: Функция Жетосснапшоттрункателогинстанце
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808428"
---
# <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="8d52c-103">Функция Жетосснапшоттрункателогинстанце</span><span class="sxs-lookup"><span data-stu-id="8d52c-103">JetOSSnapshotTruncateLogInstance Function</span></span>


<span data-ttu-id="8d52c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8d52c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="8d52c-105">Функция Жетосснапшоттрункателогинстанце</span><span class="sxs-lookup"><span data-stu-id="8d52c-105">JetOSSnapshotTruncateLogInstance Function</span></span>

<span data-ttu-id="8d52c-106">Функция **жетосснапшоттрункателогинстанце** усекает журнал для указанного экземпляра во время сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8d52c-106">The **JetOSSnapshotTruncateLogInstance** function truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="8d52c-107">**Windows Vista:**  **Жетосснапшоттрункателогинстанце** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8d52c-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8d52c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d52c-108">Parameters</span></span>

<span data-ttu-id="8d52c-109">*снапид*</span><span class="sxs-lookup"><span data-stu-id="8d52c-109">*snapId*</span></span>

<span data-ttu-id="8d52c-110">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8d52c-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="8d52c-111">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="8d52c-111">*instance*</span></span>

<span data-ttu-id="8d52c-112">Экземпляр, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="8d52c-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="8d52c-113">*грбит*</span><span class="sxs-lookup"><span data-stu-id="8d52c-113">*grbit*</span></span>

<span data-ttu-id="8d52c-114">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="8d52c-114">The options for this call.</span></span> <span data-ttu-id="8d52c-115">Этот параметр может иметь сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8d52c-115">This parameter can have a combination of the following values.</span></span>

<span data-ttu-id="8d52c-116">*грбит* может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8d52c-116">*grbit* can be one of the following values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d52c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8d52c-117">Value</span></span></p></th>
<th><p><span data-ttu-id="8d52c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8d52c-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d52c-119">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d52c-119">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="8d52c-120">Все базы данных подключены, поэтому подсистема хранилища может вычислять и выполнять усечение журнала.</span><span class="sxs-lookup"><span data-stu-id="8d52c-120">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d52c-121">Ноль (0)</span><span class="sxs-lookup"><span data-stu-id="8d52c-121">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="8d52c-122">Усечение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d52c-122">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8d52c-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d52c-123">Return Value</span></span>

<span data-ttu-id="8d52c-124">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="8d52c-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8d52c-125">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8d52c-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d52c-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8d52c-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="8d52c-127">Описание</span><span class="sxs-lookup"><span data-stu-id="8d52c-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d52c-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8d52c-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8d52c-129">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8d52c-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d52c-130">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="8d52c-130">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="8d52c-131">Недопустимый параметр <em>грбит</em> .</span><span class="sxs-lookup"><span data-stu-id="8d52c-131">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d52c-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="8d52c-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="8d52c-133">Сеанс моментального снимка не находится в состоянии, в котором может произойти усечение.</span><span class="sxs-lookup"><span data-stu-id="8d52c-133">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="8d52c-134">Возможные причины:</span><span class="sxs-lookup"><span data-stu-id="8d52c-134">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="8d52c-135">Вызов завершается после истечения времени ожидания сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8d52c-135">The call completes after the snapshot session timed out.</span></span></p></li>
<li><p><span data-ttu-id="8d52c-136">Сеанс был указан в качестве моментального снимка копии.</span><span class="sxs-lookup"><span data-stu-id="8d52c-136">The session was specified as a copy snapshot.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d52c-137">Если эта функция выполнена, файлы журнала для одного или всех экземпляров, которые являются частью сеанса моментального снимка, будут обрезаны, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="8d52c-137">If this function succeeds, the log files for one or all of the instances that are part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8d52c-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d52c-138">Remarks</span></span>

<span data-ttu-id="8d52c-139">Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="8d52c-139">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="8d52c-140">В противном случае сеанс моментального снимка завершается после вызова [жетосснапшотсав](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="8d52c-140">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="8d52c-141">Требования</span><span class="sxs-lookup"><span data-stu-id="8d52c-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d52c-142"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="8d52c-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8d52c-143">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8d52c-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d52c-144"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8d52c-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8d52c-145">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8d52c-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d52c-146"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8d52c-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8d52c-147">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8d52c-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d52c-148"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="8d52c-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8d52c-149">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8d52c-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d52c-150"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="8d52c-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8d52c-151">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8d52c-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8d52c-152">См. также:</span><span class="sxs-lookup"><span data-stu-id="8d52c-152">See Also</span></span>

[<span data-ttu-id="8d52c-153">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="8d52c-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="8d52c-154">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="8d52c-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="8d52c-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8d52c-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8d52c-156">жетосснапшотенд</span><span class="sxs-lookup"><span data-stu-id="8d52c-156">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="8d52c-157">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="8d52c-157">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="8d52c-158">жетосснапшотпрепаре</span><span class="sxs-lookup"><span data-stu-id="8d52c-158">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="8d52c-159">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="8d52c-159">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
