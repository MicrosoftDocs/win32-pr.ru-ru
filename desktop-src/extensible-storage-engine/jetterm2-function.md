---
description: Дополнительные сведения о функции JetTerm2
title: Функция JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154563"
---
# <a name="jetterm2-function"></a><span data-ttu-id="8f72f-103">Функция JetTerm2</span><span class="sxs-lookup"><span data-stu-id="8f72f-103">JetTerm2 Function</span></span>


<span data-ttu-id="8f72f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8f72f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm2-function"></a><span data-ttu-id="8f72f-105">Функция JetTerm2</span><span class="sxs-lookup"><span data-stu-id="8f72f-105">JetTerm2 Function</span></span>

<span data-ttu-id="8f72f-106">Функция **JetTerm2** инициирует завершение работы экземпляра, инициализированного [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f72f-106">The **JetTerm2** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="8f72f-107">**JetTerm2** также может уничтожить неинициализированный экземпляр, созданный [жеткреатеинстанце](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f72f-107">**JetTerm2** can also destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8f72f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f72f-108">Parameters</span></span>

<span data-ttu-id="8f72f-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="8f72f-109">*instance*</span></span>

<span data-ttu-id="8f72f-110">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="8f72f-110">The instance to use for this call.</span></span>

<span data-ttu-id="8f72f-111">**Windows 2000:**  Этот параметр пропускается и всегда должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8f72f-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="8f72f-112">**Windows XP и более поздние версии:**  Этот параметр перегружен.</span><span class="sxs-lookup"><span data-stu-id="8f72f-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="8f72f-113">Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь **значение NULL** или содержать фактический экземпляр, возвращаемый функцией [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f72f-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="8f72f-114">Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть указателем на экземпляр, созданный с помощью [жеткреатеинстанце](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f72f-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="8f72f-115">*грбит*</span><span class="sxs-lookup"><span data-stu-id="8f72f-115">*grbit*</span></span>

<span data-ttu-id="8f72f-116">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8f72f-116">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f72f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8f72f-117">Value</span></span></p></th>
<th><p><span data-ttu-id="8f72f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8f72f-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-119">JET_bitTermComplete</span><span class="sxs-lookup"><span data-stu-id="8f72f-119">JET_bitTermComplete</span></span></p></td>
<td><p><span data-ttu-id="8f72f-120">Запрашивает корректное завершение работы экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8f72f-120">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="8f72f-121">Все необязательные операции по очистке, обычно выполняемые в фоновом режиме во время выполнения, выполняются немедленно.</span><span class="sxs-lookup"><span data-stu-id="8f72f-121">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f72f-122">JET_bitTermAbrupt</span><span class="sxs-lookup"><span data-stu-id="8f72f-122">JET_bitTermAbrupt</span></span></p></td>
<td><p><span data-ttu-id="8f72f-123">Запрашивает как можно быстрее завершить работу экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8f72f-123">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="8f72f-124">Все необязательные операции, которые обычно выполняются в фоновом режиме во время выполнения, прекращаются.</span><span class="sxs-lookup"><span data-stu-id="8f72f-124">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></p>
<p><span data-ttu-id="8f72f-125"><strong>Примечание</strong>  .  Этот параметр может вызвать временную или постоянную потери пространства в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8f72f-125"><strong>Note</strong>  This option can cause temporary or permanent space loss in the database.</span></span> <span data-ttu-id="8f72f-126">Это потерянное пространство всегда может быть восстановлено с помощью автономной дефрагментации базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f72f-126">This lost space can always be recovered through an offline defragmentation of the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-127">JET_bitTermStopBackup</span><span class="sxs-lookup"><span data-stu-id="8f72f-127">JET_bitTermStopBackup</span></span></p></td>
<td><p><span data-ttu-id="8f72f-128">Запрашивает завершение работы экземпляра, даже если в данный момент выполняется резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="8f72f-128">Requests that the instance be shut down even if there is currently a backup in progress.</span></span> <span data-ttu-id="8f72f-129">Как правило, отложенная Архивация приведет к сбою <a href="gg269298(v=exchg.10).md">жеттерм</a> с JET_errBackupInProgress.</span><span class="sxs-lookup"><span data-stu-id="8f72f-129">Ordinarily, a pending backup would cause <a href="gg269298(v=exchg.10).md">JetTerm</a> to fail with JET_errBackupInProgress.</span></span> <span data-ttu-id="8f72f-130">Если этот параметр отсутствует, предполагается, что его значение JET_bitTermAbrupt.</span><span class="sxs-lookup"><span data-stu-id="8f72f-130">When this parameter is not present, its value is presumed to be JET_bitTermAbrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f72f-131">JET_bitTermDirty</span><span class="sxs-lookup"><span data-stu-id="8f72f-131">JET_bitTermDirty</span></span></p></td>
<td><p><span data-ttu-id="8f72f-132">Запрашивает завершение работы экземпляра со всеми присоединенными базами данных, оставленными в состоянии «грязных».</span><span class="sxs-lookup"><span data-stu-id="8f72f-132">Requests that the instance be shut down with all the attached databases left in a dirty state.</span></span></p>
<p><span data-ttu-id="8f72f-133">Windows 7: JET_bitTermDirty введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f72f-133">Windows 7: JET_bitTermDirty is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8f72f-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f72f-134">Return Value</span></span>

<span data-ttu-id="8f72f-135">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="8f72f-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8f72f-136">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8f72f-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f72f-137">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8f72f-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="8f72f-138">Описание</span><span class="sxs-lookup"><span data-stu-id="8f72f-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8f72f-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8f72f-140">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8f72f-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f72f-141">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="8f72f-141">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="8f72f-142">Операция не может быть завершена, так как в экземпляре выполняется операция резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8f72f-142">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8f72f-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8f72f-144">Один из указанных параметров содержал непредвиденное значение, или сочетание нескольких параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="8f72f-144">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="8f72f-145">Эта ошибка будет возвращена функцией <a href="gg269298(v=exchg.10).md">жеттерм</a> , когда модуль находится в режиме с несколькими экземплярами и когда <em>пинстанце</em> ссылается на недопустимый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8f72f-145">This error will be returned by <a href="gg269298(v=exchg.10).md">JetTerm</a> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="8f72f-146"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f72f-146"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f72f-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8f72f-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8f72f-148">Операция не может быть завершена, так как экземпляр еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="8f72f-148">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8f72f-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8f72f-150">Операция не может быть завершена, так как работа экземпляра завершается.</span><span class="sxs-lookup"><span data-stu-id="8f72f-150">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f72f-151">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8f72f-151">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8f72f-152">Невозможно выполнить операцию, так как в экземпляре выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="8f72f-152">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-153">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="8f72f-153">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="8f72f-154">Не удается завершить работу экземпляра, так как в настоящий момент имеются сеансы с активными транзакциями для указанного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8f72f-154">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="8f72f-155">Эта ошибка возникает только в том случае, если используется JET_bitTermComplete.</span><span class="sxs-lookup"><span data-stu-id="8f72f-155">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f72f-156">Если эта функция завершается, работа указанного экземпляра будет завершена.</span><span class="sxs-lookup"><span data-stu-id="8f72f-156">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="8f72f-157">Кроме того, этот экземпляр будет закрыт и сделан недоступным для любого API, который принимает экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8f72f-157">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="8f72f-158">Все остальные объекты, связанные с экземпляром, например сеансы, также будут закрыты.</span><span class="sxs-lookup"><span data-stu-id="8f72f-158">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="8f72f-159">Состояние файла контрольных точек, файлов журнала транзакций и файлов базы данных, присоединенных к экземпляру, будет изменено в процессе завершения работы.</span><span class="sxs-lookup"><span data-stu-id="8f72f-159">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="8f72f-160">Если эта функция завершается сбоем в результате ошибки использования, экземпляр остается в инициализированном состоянии и ничего не меняется.</span><span class="sxs-lookup"><span data-stu-id="8f72f-160">If this function fails as a result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="8f72f-161">В противном случае экземпляр по-прежнему завершает работу, как указано в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="8f72f-161">Otherwise, the instance is still shut down as stated for the success case.</span></span> <span data-ttu-id="8f72f-162">Разница заключается в том, что экземпляру потребуется выполнить восстановление после сбоя при следующей инициализации.</span><span class="sxs-lookup"><span data-stu-id="8f72f-162">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="8f72f-163">Ядро попытается очистить как можно больше данных, чтобы максимально увеличить требуемый объем восстановления.</span><span class="sxs-lookup"><span data-stu-id="8f72f-163">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="8f72f-164">По сути, такой сбой [жеттерм](./jetterm-function.md) не отличается от сбоя процесса.</span><span class="sxs-lookup"><span data-stu-id="8f72f-164">Conceptually, such a failure of [JetTerm](./jetterm-function.md) is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8f72f-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f72f-165">Remarks</span></span>

<span data-ttu-id="8f72f-166">См. [жеттерм](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f72f-166">See [JetTerm](./jetterm-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="8f72f-167">Требования</span><span class="sxs-lookup"><span data-stu-id="8f72f-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-168"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="8f72f-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8f72f-169">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8f72f-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f72f-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8f72f-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8f72f-171">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8f72f-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-172"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8f72f-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8f72f-173">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8f72f-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f72f-174"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="8f72f-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8f72f-175">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8f72f-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f72f-176"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="8f72f-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8f72f-177">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8f72f-177">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8f72f-178">См. также:</span><span class="sxs-lookup"><span data-stu-id="8f72f-178">See Also</span></span>

[<span data-ttu-id="8f72f-179">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="8f72f-179">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="8f72f-180">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="8f72f-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="8f72f-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8f72f-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8f72f-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8f72f-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8f72f-183">жетинит</span><span class="sxs-lookup"><span data-stu-id="8f72f-183">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="8f72f-184">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="8f72f-184">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="8f72f-185">жеттерм</span><span class="sxs-lookup"><span data-stu-id="8f72f-185">JetTerm</span></span>](./jetterm-function.md)
