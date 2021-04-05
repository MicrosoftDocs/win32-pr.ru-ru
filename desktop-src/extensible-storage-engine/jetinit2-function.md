---
description: Дополнительные сведения о функции JetInit2
title: Функция JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104000548"
---
# <a name="jetinit2-function"></a><span data-ttu-id="0e1d8-103">Функция JetInit2</span><span class="sxs-lookup"><span data-stu-id="0e1d8-103">JetInit2 Function</span></span>


<span data-ttu-id="0e1d8-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0e1d8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit2-function"></a><span data-ttu-id="0e1d8-105">Функция JetInit2</span><span class="sxs-lookup"><span data-stu-id="0e1d8-105">JetInit2 Function</span></span>

<span data-ttu-id="0e1d8-106">Функция **JetInit2** помещает ядро СУБД в состояние, где оно может поддерживать использование файлов базы данных приложением.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-106">The **JetInit2** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="0e1d8-107">Подсистема уже должна быть правильно настроена для инициализации с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0e1d8-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="0e1d8-108">Восстановление после сбоя базы данных выполняется автоматически в рамках процесса инициализации.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

<span data-ttu-id="0e1d8-109">**Windows XP:**  **JetInit2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-109">**Windows XP:**  **JetInit2** is introduced in Windows XP.</span></span>

<span data-ttu-id="0e1d8-110">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-110">This function is obsolete.</span></span> <span data-ttu-id="0e1d8-111">Вместо этого используйте [JetInit3](./jetinit3-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0e1d8-111">Use [JetInit3](./jetinit3-function.md) instead.</span></span>

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="0e1d8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e1d8-112">Parameters</span></span>

<span data-ttu-id="0e1d8-113">*пинстанце*</span><span class="sxs-lookup"><span data-stu-id="0e1d8-113">*pinstance*</span></span>

<span data-ttu-id="0e1d8-114">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-114">The instance to use for this call.</span></span>

<span data-ttu-id="0e1d8-115">Для Windows 2000 этот параметр игнорируется и всегда должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-115">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="0e1d8-116">Для Windows XP и более поздних версий использование этого параметра зависит от режима работы ядра.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-116">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="0e1d8-117">Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь значение NULL или быть установлен в допустимый выходной буфер, содержащий NULL или JET_instanceNil, который возвращает глобальный экземпляр, созданный в качестве побочного результата инициализации.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-117">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil which returns the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="0e1d8-118">Этот экземпляр можно передать в любой другой API, который принимает экземпляр.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-118">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="0e1d8-119">Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть установлен в допустимый входной буфер, содержащий экземпляр, возвращенный [жеткреатеинстанце](./jetcreateinstance-function.md) , который инициализируется.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-119">If the engine is operating in multi-instance mode, this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="0e1d8-120">*грбит*</span><span class="sxs-lookup"><span data-stu-id="0e1d8-120">*grbit*</span></span>

<span data-ttu-id="0e1d8-121">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e1d8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0e1d8-122">Value</span></span></p></th>
<th><p><span data-ttu-id="0e1d8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0e1d8-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e1d8-124">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="0e1d8-124">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="0e1d8-125">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-125">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e1d8-126">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="0e1d8-126">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="0e1d8-127">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-127">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e1d8-128">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="0e1d8-128">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="0e1d8-129">Этот параметр позволяет пользователю выполнять восстановление на наборе файлов журнала без всех существующих баз данных, подключенных к одной точке набора журналов.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-129">This option allows the user to run recovery on a set of log files, without all of the databases being present, that were attached at one point of the log set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e1d8-130">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="0e1d8-130">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="0e1d8-131">Выполните восстановление, но остановите на этапе отката.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-131">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="0e1d8-132">Это позволяет копировать и применять дополнительные журналы транзакций.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-132">This allows additional transaction logs to copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e1d8-133">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="0e1d8-133">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="0e1d8-134">При успешном обратимом восстановлении усечение файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-134">On successful soft recovery, truncate log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e1d8-135">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="0e1d8-135">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="0e1d8-136">Отсутствует запись схемы базы данных по умолчанию в то же расположение.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-136">Missing database map entry default to same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e1d8-137">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="0e1d8-137">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="0e1d8-138">Игнорировать журналы, потерянные с конца потока журнала.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-138">Ignore logs lost from the end of the log stream.</span></span></p>
<p><span data-ttu-id="0e1d8-139"><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-139"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0e1d8-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e1d8-140">Return Value</span></span>

<span data-ttu-id="0e1d8-141">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-141">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0e1d8-142">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e1d8-142">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="0e1d8-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e1d8-143">Remarks</span></span>

<span data-ttu-id="0e1d8-144">Экземпляр должен быть инициализирован с помощью вызова **JetInit2** , прежде чем он сможет использоваться любым другим, кроме [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0e1d8-144">An instance must be initialized with a call to **JetInit2** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="0e1d8-145">Экземпляр уничтожается вызовом функции [жеттерм](./jetterm-function.md) , даже если этот экземпляр никогда не был инициализирован с помощью [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="0e1d8-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="0e1d8-146">Экземпляр — это единица восстановления для ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-146">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="0e1d8-147">Он управляет жизненным циклом всех файлов, используемых для защиты целостности данных в наборе файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-147">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="0e1d8-148">Эти файлы включают файл контрольных точек и файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-148">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="0e1d8-149">Если восстановление выполняется на наборе журналов, для которых не все базы данных (возвращающие ошибку JET_errAttachedDatabaseMismatch при нормальных обстоятельствах), и клиент хочет, чтобы продолжение восстановления, несмотря на отсутствие баз данных, JET_ Битреплайигноремиссингдб используется для продолжения восстановления доступных баз данных.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-149">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="0e1d8-150">Дополнительные сведения см. в разделе "Примечания" в [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0e1d8-150">See the Remarks section in [JetInit](./jetinit-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0e1d8-151">Требования</span><span class="sxs-lookup"><span data-stu-id="0e1d8-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e1d8-152"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="0e1d8-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1d8-153">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e1d8-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0e1d8-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1d8-155">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e1d8-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0e1d8-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1d8-157">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e1d8-158"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="0e1d8-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1d8-159">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e1d8-160"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="0e1d8-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1d8-161">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0e1d8-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0e1d8-162">См. также:</span><span class="sxs-lookup"><span data-stu-id="0e1d8-162">See Also</span></span>

[<span data-ttu-id="0e1d8-163">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="0e1d8-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="0e1d8-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0e1d8-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0e1d8-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0e1d8-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0e1d8-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0e1d8-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0e1d8-167">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="0e1d8-167">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="0e1d8-168">жетинит</span><span class="sxs-lookup"><span data-stu-id="0e1d8-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="0e1d8-169">JetInit3</span><span class="sxs-lookup"><span data-stu-id="0e1d8-169">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="0e1d8-170">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="0e1d8-170">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="0e1d8-171">Параметры ресурсов</span><span class="sxs-lookup"><span data-stu-id="0e1d8-171">Resource Parameters</span></span>](./resource-parameters.md)
