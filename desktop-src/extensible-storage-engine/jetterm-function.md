---
description: Дополнительные сведения о функции Жеттерм
title: Функция JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692200"
---
# <a name="jetterm-function"></a><span data-ttu-id="c380d-103">Функция JetTerm</span><span class="sxs-lookup"><span data-stu-id="c380d-103">JetTerm Function</span></span>


<span data-ttu-id="c380d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c380d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm-function"></a><span data-ttu-id="c380d-105">Функция JetTerm</span><span class="sxs-lookup"><span data-stu-id="c380d-105">JetTerm Function</span></span>

<span data-ttu-id="c380d-106">Функция **жеттерм** инициирует завершение работы экземпляра, инициализированного [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="c380d-106">The **JetTerm** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="c380d-107">**Жеттерм** также можно использовать для уничтожения неинициализированного экземпляра, созданного с помощью [жеткреатеинстанце](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="c380d-107">**JetTerm** can also be used to destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="c380d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c380d-108">Parameters</span></span>

<span data-ttu-id="c380d-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="c380d-109">*instance*</span></span>

<span data-ttu-id="c380d-110">Указывает экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c380d-110">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="c380d-111">**Windows 2000:**  Этот параметр пропускается и всегда должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c380d-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="c380d-112">**Windows XP и более поздние версии:**  Этот параметр перегружен.</span><span class="sxs-lookup"><span data-stu-id="c380d-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="c380d-113">Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь **значение NULL** или содержать фактический экземпляр, возвращаемый функцией [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="c380d-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="c380d-114">Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть указателем на экземпляр, созданный с помощью [жеткреатеинстанце](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="c380d-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="c380d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c380d-115">Return Value</span></span>

<span data-ttu-id="c380d-116">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="c380d-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c380d-117">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c380d-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c380d-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c380d-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="c380d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="c380d-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c380d-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c380d-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c380d-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c380d-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c380d-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c380d-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c380d-123">Один из указанных параметров содержал непредвиденное значение, или сочетание нескольких параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="c380d-123">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="c380d-124">Эта ошибка будет возвращена функцией <strong>жеттерм</strong> , когда модуль находится в режиме с несколькими экземплярами и когда <em>пинстанце</em> ссылается на недопустимый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c380d-124">This error will be returned by <strong>JetTerm</strong> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="c380d-125"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c380d-125"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c380d-126">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c380d-126">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c380d-127">Операция не может быть завершена, так как экземпляр еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="c380d-127">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c380d-128">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c380d-128">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c380d-129">Операция не может быть завершена, так как работа экземпляра завершается.</span><span class="sxs-lookup"><span data-stu-id="c380d-129">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c380d-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c380d-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c380d-131">Невозможно выполнить операцию, так как в экземпляре выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="c380d-131">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c380d-132">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="c380d-132">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="c380d-133">Операция не может быть завершена, так как в экземпляре выполняется операция резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="c380d-133">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c380d-134">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="c380d-134">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="c380d-135">Не удается завершить работу экземпляра, так как в настоящий момент имеются сеансы с активными транзакциями для указанного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c380d-135">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="c380d-136">Эта ошибка возникает только в том случае, если используется JET_bitTermComplete.</span><span class="sxs-lookup"><span data-stu-id="c380d-136">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c380d-137">Если эта функция завершается, работа указанного экземпляра будет завершена.</span><span class="sxs-lookup"><span data-stu-id="c380d-137">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="c380d-138">Кроме того, этот экземпляр будет закрыт и сделан недоступным для любого API, который принимает экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c380d-138">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="c380d-139">Все остальные объекты, связанные с экземпляром, например сеансы, также будут закрыты.</span><span class="sxs-lookup"><span data-stu-id="c380d-139">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="c380d-140">Состояние файла контрольных точек, файлов журнала транзакций и файлов базы данных, присоединенных к экземпляру, будет изменено в процессе завершения работы.</span><span class="sxs-lookup"><span data-stu-id="c380d-140">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="c380d-141">Если эта функция завершается ошибкой в результате ошибки использования, экземпляр остается в инициализированном состоянии и ничего не меняется.</span><span class="sxs-lookup"><span data-stu-id="c380d-141">If this function fails as the result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="c380d-142">В противном случае экземпляр по-прежнему завершает работу, как в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="c380d-142">Otherwise, the instance is still shut down as per the success case.</span></span> <span data-ttu-id="c380d-143">Разница заключается в том, что экземпляру потребуется выполнить восстановление после сбоя при следующей инициализации.</span><span class="sxs-lookup"><span data-stu-id="c380d-143">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="c380d-144">Ядро попытается очистить как можно больше данных, чтобы максимально увеличить требуемый объем восстановления.</span><span class="sxs-lookup"><span data-stu-id="c380d-144">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="c380d-145">По сути, такой сбой **жеттерм** не отличается от сбоя процесса.</span><span class="sxs-lookup"><span data-stu-id="c380d-145">Conceptually, such a failure of **JetTerm** is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c380d-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c380d-146">Remarks</span></span>

<span data-ttu-id="c380d-147">Если ведущий процесс экземпляра завершается по какой-либо причине, прежде чем **жеттерм** успешно вызывается для этого экземпляра, считается, что экземпляр находится в состоянии сбоя.</span><span class="sxs-lookup"><span data-stu-id="c380d-147">If the host process of an instance quits for any reason before **JetTerm** is successfully called on that instance then the instance is considered to be in a crashed state.</span></span> <span data-ttu-id="c380d-148">Восстановление после сбоя произойдет при следующей попытке инициализации этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c380d-148">Crash recovery will occur on the next attempt to initialize that instance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c380d-149">Требования</span><span class="sxs-lookup"><span data-stu-id="c380d-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c380d-150"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c380d-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c380d-151">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c380d-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c380d-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c380d-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c380d-153">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c380d-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c380d-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c380d-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c380d-155">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c380d-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c380d-156"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="c380d-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c380d-157">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c380d-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c380d-158"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="c380d-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c380d-159">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c380d-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c380d-160">См. также:</span><span class="sxs-lookup"><span data-stu-id="c380d-160">See Also</span></span>

[<span data-ttu-id="c380d-161">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="c380d-161">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="c380d-162">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="c380d-162">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c380d-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c380d-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c380d-164">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c380d-164">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c380d-165">жетинит</span><span class="sxs-lookup"><span data-stu-id="c380d-165">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="c380d-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c380d-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c380d-167">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="c380d-167">JetTerm2</span></span>](./jetterm2-function.md)
