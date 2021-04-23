---
description: Дополнительные сведения о функции Жетосснапшотпрепаре
title: Функция JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647513"
---
# <a name="jetossnapshotprepare-function"></a><span data-ttu-id="64daf-103">Функция JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="64daf-103">JetOSSnapshotPrepare Function</span></span>


<span data-ttu-id="64daf-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="64daf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepare-function"></a><span data-ttu-id="64daf-105">Функция JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="64daf-105">JetOSSnapshotPrepare Function</span></span>

<span data-ttu-id="64daf-106">Функция **жетосснапшотпрепаре** начинает подготовку сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="64daf-106">The **JetOSSnapshotPrepare** function begins the preparations for a snapshot session.</span></span> <span data-ttu-id="64daf-107">Сеанс моментальных снимков — это короткий интервал времени, в течение которого модуль не выполняет никаких операций записи с диска IOs на диск, чтобы подсистема могла участвовать в сеансе моментальных снимков тома (при использовании модуля записи моментальных снимков).</span><span class="sxs-lookup"><span data-stu-id="64daf-107">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="64daf-108">**Windows XP:**  **Жетосснапшотпрепаре** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="64daf-108">**Windows XP:**  **JetOSSnapshotPrepare** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="64daf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64daf-109">Parameters</span></span>

<span data-ttu-id="64daf-110">*пснапид*</span><span class="sxs-lookup"><span data-stu-id="64daf-110">*psnapId*</span></span>

<span data-ttu-id="64daf-111">Идентификатор сеанса моментального снимка, который необходимо запустить.</span><span class="sxs-lookup"><span data-stu-id="64daf-111">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="64daf-112">*грбит*</span><span class="sxs-lookup"><span data-stu-id="64daf-112">*grbit*</span></span>

<span data-ttu-id="64daf-113">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="64daf-113">The options for this call.</span></span> <span data-ttu-id="64daf-114">Этот параметр может иметь сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="64daf-114">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64daf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="64daf-115">Value</span></span></p></th>
<th><p><span data-ttu-id="64daf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="64daf-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64daf-117">0</span><span class="sxs-lookup"><span data-stu-id="64daf-117">0</span></span></p></td>
<td><p><span data-ttu-id="64daf-118">Стандартный моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="64daf-118">Normal snapshot.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64daf-119">JET_bitIncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="64daf-119">JET_bitIncrementalSnapshot</span></span></p></td>
<td><p><span data-ttu-id="64daf-120">Будут предприняты только файлы журналов.</span><span class="sxs-lookup"><span data-stu-id="64daf-120">Only log files will be taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64daf-121">JET_bitCopySnapshot</span><span class="sxs-lookup"><span data-stu-id="64daf-121">JET_bitCopySnapshot</span></span></p></td>
<td><p><span data-ttu-id="64daf-122">Моментальный снимок копии (обычная или добавочная) без усечения журнала.</span><span class="sxs-lookup"><span data-stu-id="64daf-122">A copy snapshot (normal or incremental) with no log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64daf-123">JET_bitContinueAfterThaw</span><span class="sxs-lookup"><span data-stu-id="64daf-123">JET_bitContinueAfterThaw</span></span></p></td>
<td><p><span data-ttu-id="64daf-124">Сеанс моментального снимка происходит после <a href="gg269229(v=exchg.10).md">жетосснапшотсав</a> и требует вызова функции <a href="gg294136(v=exchg.10).md">жетосснапшотенд</a> .</span><span class="sxs-lookup"><span data-stu-id="64daf-124">The snapshot session occurs after <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> and will require a <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> function call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64daf-125">JET_bitExplicitPrepare</span><span class="sxs-lookup"><span data-stu-id="64daf-125">JET_bitExplicitPrepare</span></span></p></td>
<td><p><span data-ttu-id="64daf-126">Ни один экземпляр не будет подготовлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64daf-126">No instances will be prepared by default.</span></span></p>
<p><span data-ttu-id="64daf-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64daf-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="64daf-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64daf-128">Return Value</span></span>

<span data-ttu-id="64daf-129">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="64daf-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="64daf-130">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="64daf-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64daf-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="64daf-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="64daf-132">Описание</span><span class="sxs-lookup"><span data-stu-id="64daf-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64daf-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="64daf-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="64daf-134">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="64daf-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64daf-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="64daf-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="64daf-136">Указатель идентификатора моментального снимка имеет значение NULL, или параметр <em>грбит</em> является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="64daf-136">The snapshot ID pointer is NULL or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64daf-137">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="64daf-137">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="64daf-138">Сеанс моментальных снимков уже выполняется, и в данный момент операция не может иметь более одного сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="64daf-138">A snapshot session is already in progress and the operation is not allowed to have more then one snapshot session at any given time.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64daf-139">Если эта функция завершится с ошибкой, сеанс моментального снимка можно будет запустить в любое время с фазы замораживания ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="64daf-139">If this function succeeds, a snapshot session will be able to start at any time with the IO freeze phase.</span></span> <span data-ttu-id="64daf-140">Идентификатор сеанса будет возвращен и должен использоваться в последующих вызовах для сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="64daf-140">The identifier for the session will be returned and must be used in the subsequent calls for the snapshot session.</span></span>

<span data-ttu-id="64daf-141">Выполняющиеся экземпляры подсистемы теперь будут рассматриваться как часть сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="64daf-141">The running instances of the engine will now be considered part of the snapshot session.</span></span>

<span data-ttu-id="64daf-142">**Windows Vista:**  Чтобы указать другое подмножество экземпляров, можно вызвать [жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="64daf-142">**Windows Vista:**  To specify a different subset of instances, the [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) can be called.</span></span>

<span data-ttu-id="64daf-143">Стандартный вызов последовательности API: **жетосснапшотпрепаре**, при необходимости за одним или несколькими вызовами [жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md), после которого следует [жетосснапшотфризе](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="64daf-143">The normal API sequence call is: **JetOSSnapshotPrepare**, optionally followed by one or more calls to [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="64daf-144">После запуска замораживания его можно завершить с помощью [жетосснапшотсав](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="64daf-144">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="64daf-145">В любое время после подготовки сеанс моментального снимка может внезапно завершиться с помощью [жетосснапшотаборт](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="64daf-145">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span>

<span data-ttu-id="64daf-146">Если после [жетосснапшотсав](./jetossnapshotthaw-function.md)указан JET_bitContinueAfterThaw, то сеанс моментального снимка останется (хотя операция ввода-вывода будет возобновлена).</span><span class="sxs-lookup"><span data-stu-id="64daf-146">If JET_bitContinueAfterThaw is specified after [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), the snapshot session will remain (although the I/O will resume).</span></span> <span data-ttu-id="64daf-147">При этом будет включена проверка моментального снимка и, при необходимости, будет включено усечение журнала с помощью [жетосснапшоттрункателог](./jetossnapshottruncatelog-function.md) и потребуется вызов [жетосснапшотенд](./jetossnapshotend-function.md).</span><span class="sxs-lookup"><span data-stu-id="64daf-147">This will enable a verification of the snapshot, and if needed, will enable log truncation using [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) and will require a call to [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span></span>

<span data-ttu-id="64daf-148">Если эта функция завершается неудачно, изменение состояния модуля не происходит.</span><span class="sxs-lookup"><span data-stu-id="64daf-148">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="64daf-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64daf-149">Remarks</span></span>

<span data-ttu-id="64daf-150">Записи журнала событий будут созданы для различных этапов создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="64daf-150">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="64daf-151">Требования</span><span class="sxs-lookup"><span data-stu-id="64daf-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64daf-152"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="64daf-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="64daf-153">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="64daf-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64daf-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="64daf-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="64daf-155">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="64daf-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64daf-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="64daf-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="64daf-157">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="64daf-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64daf-158"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="64daf-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="64daf-159">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="64daf-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64daf-160"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="64daf-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="64daf-161">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="64daf-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="64daf-162">См. также:</span><span class="sxs-lookup"><span data-stu-id="64daf-162">See Also</span></span>

[<span data-ttu-id="64daf-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="64daf-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="64daf-164">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="64daf-164">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="64daf-165">жетосснапшотаборт</span><span class="sxs-lookup"><span data-stu-id="64daf-165">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="64daf-166">жетосснапшотенд</span><span class="sxs-lookup"><span data-stu-id="64daf-166">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="64daf-167">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="64daf-167">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="64daf-168">жетосснапшотпрепареинстанце</span><span class="sxs-lookup"><span data-stu-id="64daf-168">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="64daf-169">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="64daf-169">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)  
[<span data-ttu-id="64daf-170">жетосснапшоттрункателог</span><span class="sxs-lookup"><span data-stu-id="64daf-170">JetOSSnapshotTruncateLog</span></span>](./jetossnapshottruncatelog-function.md)
