---
description: Дополнительные сведения о функции Жетосснапшотфризе
title: Функция JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265714"
---
# <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="649b0-103">Функция JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="649b0-103">JetOSSnapshotFreeze Function</span></span>


<span data-ttu-id="649b0-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="649b0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="649b0-105">Функция JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="649b0-105">JetOSSnapshotFreeze Function</span></span>

<span data-ttu-id="649b0-106">Функция **жетосснапшотфризе** запускает моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="649b0-106">The **JetOSSnapshotFreeze** function starts a snapshot.</span></span> <span data-ttu-id="649b0-107">Во время выполнения моментального снимка подсистема не может выполнить действия записи на диск.</span><span class="sxs-lookup"><span data-stu-id="649b0-107">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="649b0-108">**Windows XP:**  **Жетосснапшотфризе** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="649b0-108">**Windows XP:**  **JetOSSnapshotFreeze** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="649b0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="649b0-109">Parameters</span></span>

<span data-ttu-id="649b0-110">*снапид*</span><span class="sxs-lookup"><span data-stu-id="649b0-110">*snapId*</span></span>

<span data-ttu-id="649b0-111">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="649b0-111">The identifier of the snapshot session.</span></span>

<span data-ttu-id="649b0-112">*пЦинстанцеинфо*</span><span class="sxs-lookup"><span data-stu-id="649b0-112">*pcInstanceInfo*</span></span>

<span data-ttu-id="649b0-113">Число экземпляров, выполняемых в данный момент в ядре, которые являются частью сеанса моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="649b0-113">The number of instances currently running in the engine that are part of the snapshot session.</span></span>

<span data-ttu-id="649b0-114">*паинстанцеинфо*</span><span class="sxs-lookup"><span data-stu-id="649b0-114">*paInstanceInfo*</span></span>

<span data-ttu-id="649b0-115">Массив структур, по одному для каждого работающего экземпляра, который является частью сеанса моментального снимка, описывающий экземпляр и базы данных, которые являются его частью.</span><span class="sxs-lookup"><span data-stu-id="649b0-115">An array of structures, one for each running instance that is part of the snapshot session, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="649b0-116">*грбит*</span><span class="sxs-lookup"><span data-stu-id="649b0-116">*grbit*</span></span>

<span data-ttu-id="649b0-117">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="649b0-117">The options for this call.</span></span> <span data-ttu-id="649b0-118">Этот параметр зарезервирован для будущего использования, и поддерживается только допустимое значение 0.</span><span class="sxs-lookup"><span data-stu-id="649b0-118">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="649b0-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="649b0-119">Return Value</span></span>

<span data-ttu-id="649b0-120">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="649b0-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="649b0-121">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="649b0-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="649b0-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="649b0-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="649b0-123">Описание</span><span class="sxs-lookup"><span data-stu-id="649b0-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="649b0-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="649b0-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="649b0-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="649b0-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="649b0-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="649b0-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="649b0-127">Указатели, предоставленные для выходных параметров, имеют значение NULL, сеанс моментального снимка недопустим, или параметр <em>грбит</em> является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="649b0-127">The pointers provided for the output parameters are NULL, the snapshot session is invalid, or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="649b0-128">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="649b0-128">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="649b0-129">Сеанс моментального снимка находится в неправильном состоянии, чтобы начать замораживание (например, если предыдущая фиксация не удалась в этом сеансе).</span><span class="sxs-lookup"><span data-stu-id="649b0-129">The snapshot session is not in the appropriate state to start a freeze (for example, a previous freeze failed on this session before).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="649b0-130">JET_errOSSnapshotNotAllowed</span><span class="sxs-lookup"><span data-stu-id="649b0-130">JET_errOSSnapshotNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="649b0-131">Обработчик не находится в состоянии, в котором можно выполнить моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="649b0-131">The engine is not in a state in which a snapshot can be performed.</span></span> <span data-ttu-id="649b0-132">Уже выполняется одно или несколько резервных копий потоковой передачи, либо один или несколько экземпляров проходят через этапы восстановления или завершаются.</span><span class="sxs-lookup"><span data-stu-id="649b0-132">Either one or more streaming backups is already in progress, or one or more instances are going through recovery steps or terminating.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="649b0-133">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="649b0-133">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="649b0-134">Недопустимый идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="649b0-134">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="649b0-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="649b0-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="649b0-136">Ошибка при выполнении функции из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="649b0-136">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="649b0-137">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="649b0-137">JET_errOutOfThreads</span></span></p></td>
<td><p><span data-ttu-id="649b0-138">Не удалось выполнить функцию, так как не удалось запустить новый поток, выполняющий замораживание.</span><span class="sxs-lookup"><span data-stu-id="649b0-138">The function failed because a new thread doing the freeze failed to start.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="649b0-139">Если эта функция завершится с ошибкой, то для файлов базы данных или файлов журнала, которые являются частью замороженных экземпляров, не будет выдана запись IOs.</span><span class="sxs-lookup"><span data-stu-id="649b0-139">If this function succeeds, there will not be any write IOs issued for the database files or for the log files that are part of instances that are frozen.</span></span> <span data-ttu-id="649b0-140">Кроме того, сведения об экземпляре будут заполнены должным образом и должны быть освобождены позже путем вызова [жетфрибуффер](./jetfreebuffer-function.md) с указателем на возвращаемый массив сведений об экземпляре.</span><span class="sxs-lookup"><span data-stu-id="649b0-140">Also, the instance information will be properly filled and it must be freed later on by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="649b0-141">Если эта функция завершается с ошибкой, ядро продолжает работать нормально с IOs, как обычно.</span><span class="sxs-lookup"><span data-stu-id="649b0-141">If this function fails, the engine will keep running normally with the IOs occurring as usual.</span></span> <span data-ttu-id="649b0-142">Нет необходимости вызывать [жетосснапшотсав](./jetossnapshotthaw-function.md) в случае сбоя Freeze.</span><span class="sxs-lookup"><span data-stu-id="649b0-142">There is no need to call [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) if the freeze fails.</span></span> <span data-ttu-id="649b0-143">Кроме того, сведения об экземпляре не будут заполнены, поэтому освободить этот ресурс не нужно.</span><span class="sxs-lookup"><span data-stu-id="649b0-143">Also, the instance information will not be filled so there is no need to free this resource.</span></span>

#### <a name="remarks"></a><span data-ttu-id="649b0-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="649b0-144">Remarks</span></span>

<span data-ttu-id="649b0-145">В течение периода закрепления не будет никаких операций записи IOs, выданных подключенным базам данных или журналам транзакций, несмотря на то, что для временных баз данных или потоковых файлов может быть выдана операция ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="649b0-145">During the freeze period, there will not be any write IOs issued to the attached databases or the transaction logs, although there might be write IOs issued to the temporary databases or streaming files.</span></span>

<span data-ttu-id="649b0-146">Состояние, в котором базы данных и файлы журналов будут находиться во время замораживания (состояние, в котором файлы будут находиться в образе моментального снимка тома), будет иметь возможность нормального восстановления, если эти файлы будут восстановлены позже.</span><span class="sxs-lookup"><span data-stu-id="649b0-146">The state in which the databases and the log files will be during the freeze (the state in which the files would be in a Volume Snapshot image) will be such that a normal recovery will be possible if those files are restored later.</span></span>

<span data-ttu-id="649b0-147">Так как в течение периода замораживания нет операций записи, обычно вызовы API в механизме могут быть остановлены для этого интервала.</span><span class="sxs-lookup"><span data-stu-id="649b0-147">Because there are no write operations during the freeze period, normal API calls into the engine might be stalled for that interval.</span></span> <span data-ttu-id="649b0-148">Клиентское приложение должно иметь возможность обрабатывать вызовы API, которые могут занимать больше времени, если происходит зависание.</span><span class="sxs-lookup"><span data-stu-id="649b0-148">The client application must be able to handle API calls that might take longer then normal if a freeze occurs.</span></span>

<span data-ttu-id="649b0-149">Из-за возможных эффектов, описанных выше, существует внутреннее время ожидания, по истечении которого сеанс моментальных снимков останавливает фазу замораживания даже в том случае, если не были вызваны API, выполняющие разморозку или прерывание.</span><span class="sxs-lookup"><span data-stu-id="649b0-149">Due to the possible effects described above, there is an internal timeout after which the snapshot session will stop the freeze phase even if the APIs doing the thaw or abort were not called.</span></span> <span data-ttu-id="649b0-150">Значение времени ожидания можно изменить с помощью параметра системы [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="649b0-150">The value of the timeout can be changed using the [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) system parameter.</span></span> <span data-ttu-id="649b0-151">Обратите внимание, что стандартный интервал замораживания находится в диапазоне 10 секунд, а время ожидания по умолчанию — около 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="649b0-151">Note that the typical freeze interval is in the range of 10 seconds with the default timeout somewhere around 60 seconds.</span></span>

#### <a name="requirements"></a><span data-ttu-id="649b0-152">Требования</span><span class="sxs-lookup"><span data-stu-id="649b0-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="649b0-153"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="649b0-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="649b0-154">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="649b0-154">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="649b0-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="649b0-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="649b0-156">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="649b0-156">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="649b0-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="649b0-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="649b0-158">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="649b0-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="649b0-159"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="649b0-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="649b0-160">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="649b0-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="649b0-161"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="649b0-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="649b0-162">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="649b0-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="649b0-163"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="649b0-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="649b0-164">Реализуется как <strong>жетосснапшотфризев</strong> (Юникод) и <strong>жетосснапшотфризеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="649b0-164">Implemented as <strong>JetOSSnapshotFreezeW</strong> (Unicode) and <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="649b0-165">См. также:</span><span class="sxs-lookup"><span data-stu-id="649b0-165">See Also</span></span>

[<span data-ttu-id="649b0-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="649b0-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="649b0-167">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="649b0-167">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="649b0-168">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="649b0-168">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="649b0-169">жетосснапшотаборт</span><span class="sxs-lookup"><span data-stu-id="649b0-169">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="649b0-170">жетосснапшотпрепаре</span><span class="sxs-lookup"><span data-stu-id="649b0-170">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="649b0-171">жетосснапшотпрепареинстанце</span><span class="sxs-lookup"><span data-stu-id="649b0-171">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="649b0-172">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="649b0-172">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
