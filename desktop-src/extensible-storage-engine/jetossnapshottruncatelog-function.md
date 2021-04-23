---
description: Дополнительные сведения о функции Жетосснапшоттрункателог
title: Функция Жетосснапшоттрункателог
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647565"
---
# <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="03af1-103">Функция Жетосснапшоттрункателог</span><span class="sxs-lookup"><span data-stu-id="03af1-103">JetOSSnapshotTruncateLog Function</span></span>


<span data-ttu-id="03af1-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="03af1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="03af1-105">Функция Жетосснапшоттрункателог</span><span class="sxs-lookup"><span data-stu-id="03af1-105">JetOSSnapshotTruncateLog Function</span></span>

<span data-ttu-id="03af1-106">Функция **жетосснапшоттрункателог** включает усечение журнала для всех экземпляров, которые являются частью сеанса моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="03af1-106">The **JetOSSnapshotTruncateLog** function enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="03af1-107">**Windows Vista:**  **Жетосснапшоттрункателог** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03af1-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="03af1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="03af1-108">Parameters</span></span>

<span data-ttu-id="03af1-109">*снапид*</span><span class="sxs-lookup"><span data-stu-id="03af1-109">*snapId*</span></span>

<span data-ttu-id="03af1-110">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="03af1-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="03af1-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="03af1-111">*grbit*</span></span>

<span data-ttu-id="03af1-112">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="03af1-112">The options for this call.</span></span> <span data-ttu-id="03af1-113">Этот параметр может иметь сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="03af1-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03af1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="03af1-114">Value</span></span></p></th>
<th><p><span data-ttu-id="03af1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="03af1-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03af1-116">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="03af1-116">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="03af1-117">Все базы данных подключены, поэтому подсистема хранилища может вычислять и выполнять усечение журнала.</span><span class="sxs-lookup"><span data-stu-id="03af1-117">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03af1-118">Ноль (0)</span><span class="sxs-lookup"><span data-stu-id="03af1-118">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="03af1-119">Усечение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03af1-119">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="03af1-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03af1-120">Return Value</span></span>

<span data-ttu-id="03af1-121">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="03af1-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="03af1-122">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="03af1-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03af1-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="03af1-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="03af1-124">Описание</span><span class="sxs-lookup"><span data-stu-id="03af1-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03af1-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="03af1-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="03af1-126">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="03af1-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03af1-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="03af1-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="03af1-128">Недопустимый параметр <em>грбит</em> .</span><span class="sxs-lookup"><span data-stu-id="03af1-128">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03af1-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="03af1-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="03af1-130">Сеанс моментального снимка не находится в состоянии, в котором может произойти усечение.</span><span class="sxs-lookup"><span data-stu-id="03af1-130">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="03af1-131">Возможные причины:</span><span class="sxs-lookup"><span data-stu-id="03af1-131">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="03af1-132">вызов выполняется по истечении времени ожидания сеанса моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="03af1-132">the call is done after the snapshot session timed-out</span></span></p></li>
<li><p><span data-ttu-id="03af1-133">сеанс был указан в качестве моментального снимка копии</span><span class="sxs-lookup"><span data-stu-id="03af1-133">the session was specified as a copy snapshot</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03af1-134">При успешном выполнении файлы журнала для одной или всех экземпляров сеанса моментальных снимков будут обрезаны, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="03af1-134">On success, the log files for one or all the instances part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="03af1-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03af1-135">Remarks</span></span>

<span data-ttu-id="03af1-136">Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="03af1-136">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="03af1-137">В противном случае сеанс моментального снимка был бы завершен после вызова [жетосснапшотсав](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="03af1-137">Otherwise, the snapshot session would have ended after the [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) call.</span></span>

#### <a name="requirements"></a><span data-ttu-id="03af1-138">Требования</span><span class="sxs-lookup"><span data-stu-id="03af1-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03af1-139"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="03af1-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="03af1-140">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03af1-140">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03af1-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="03af1-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="03af1-142">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="03af1-142">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03af1-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="03af1-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="03af1-144">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="03af1-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03af1-145"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="03af1-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="03af1-146">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="03af1-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03af1-147"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="03af1-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="03af1-148">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="03af1-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="03af1-149">См. также:</span><span class="sxs-lookup"><span data-stu-id="03af1-149">See Also</span></span>

[<span data-ttu-id="03af1-150">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="03af1-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="03af1-151">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="03af1-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="03af1-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="03af1-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="03af1-153">жетосснапшотенд</span><span class="sxs-lookup"><span data-stu-id="03af1-153">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="03af1-154">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="03af1-154">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="03af1-155">жетосснапшотпрепаре</span><span class="sxs-lookup"><span data-stu-id="03af1-155">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="03af1-156">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="03af1-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
