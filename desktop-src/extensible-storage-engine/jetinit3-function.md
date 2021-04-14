---
description: Дополнительные сведения о функции JetInit3
title: Функция JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350422"
---
# <a name="jetinit3-function"></a><span data-ttu-id="695a8-103">Функция JetInit3</span><span class="sxs-lookup"><span data-stu-id="695a8-103">JetInit3 Function</span></span>


<span data-ttu-id="695a8-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="695a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit3-function"></a><span data-ttu-id="695a8-105">Функция JetInit3</span><span class="sxs-lookup"><span data-stu-id="695a8-105">JetInit3 Function</span></span>

<span data-ttu-id="695a8-106">Функция **JetInit3** помещает ядро СУБД в состояние, в котором оно может поддерживать использование файлов базы данных приложением.</span><span class="sxs-lookup"><span data-stu-id="695a8-106">The **JetInit3** function puts the database engine into a state in which it can support application use of database files.</span></span> <span data-ttu-id="695a8-107">Подсистема уже должна быть правильно настроена для инициализации, которую можно выполнить с помощью функции [жетсетсистемпараметер](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="695a8-107">The engine must already be properly configured for initialization, which you accomplish by using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span> <span data-ttu-id="695a8-108">Обратите внимание, что восстановление после сбоя базы данных происходит автоматически в рамках процесса инициализации.</span><span class="sxs-lookup"><span data-stu-id="695a8-108">Note that database crash recovery occurs automatically as a part of the initialization process.</span></span>

<span data-ttu-id="695a8-109">**Windows Vista:**  **JetInit3** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="695a8-109">**Windows Vista:**  **JetInit3** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="695a8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="695a8-110">Parameters</span></span>

<span data-ttu-id="695a8-111">*пинстанце*</span><span class="sxs-lookup"><span data-stu-id="695a8-111">*pinstance*</span></span>

<span data-ttu-id="695a8-112">Экземпляр, используемый для конкретного вызова.</span><span class="sxs-lookup"><span data-stu-id="695a8-112">The instance that you use for a particular call.</span></span> <span data-ttu-id="695a8-113">Использование этого параметра зависит от режима работы ядра.</span><span class="sxs-lookup"><span data-stu-id="695a8-113">The use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="695a8-114">Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), в котором поддерживается только один экземпляр, можно установить этот параметр в **значение NULL** или в допустимый выходной буфер, содержащий **null** или JET_instanceNil, который возвращает глобальный экземпляр, созданный в качестве побочного результата инициализации.</span><span class="sxs-lookup"><span data-stu-id="695a8-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode), in which only one instance is supported, you can set this parameter either to **NULL** or to a valid output buffer containing either **NULL** or JET_instanceNil, which returns the global instance handle created as a side-effect of the initialization.</span></span> <span data-ttu-id="695a8-115">Этот экземпляр можно передать в любой другой API, который принимает экземпляр.</span><span class="sxs-lookup"><span data-stu-id="695a8-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="695a8-116">Если ядро работает в режиме с несколькими экземплярами, необходимо присвоить этому параметру Допустимый входной буфер, содержащий экземпляр, возвращаемый функцией [жеткреатеинстанце](./jetcreateinstance-function.md) , которая инициализируется.</span><span class="sxs-lookup"><span data-stu-id="695a8-116">If the engine is operating in multi-instance mode, you must set this parameter to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function that is being initialized.</span></span>

<span data-ttu-id="695a8-117">*прстинфо*</span><span class="sxs-lookup"><span data-stu-id="695a8-117">*prstInfo*</span></span>

<span data-ttu-id="695a8-118">Дополнительные параметры восстановления, используемые для повторного сопоставления баз данных во время восстановления, для задания расположения, в котором будет прерываться восстановление, или для определения текущего состояния восстановления.</span><span class="sxs-lookup"><span data-stu-id="695a8-118">Additional recovery parameters used for remapping databases during recovery, for setting the position where recovery will stop, or for determining the current recovery status.</span></span>

<span data-ttu-id="695a8-119">*грбит*</span><span class="sxs-lookup"><span data-stu-id="695a8-119">*grbit*</span></span>

<span data-ttu-id="695a8-120">Группа битов, указывающая ноль или более параметров, указанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="695a8-120">A group of bits that specifies zero or more of the options listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="695a8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="695a8-121">Value</span></span></p></th>
<th><p><span data-ttu-id="695a8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="695a8-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="695a8-123">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="695a8-123">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="695a8-124">Это значение зарезервировано для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="695a8-124">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="695a8-125">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="695a8-125">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="695a8-126">Это значение зарезервировано для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="695a8-126">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="695a8-127">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="695a8-127">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="695a8-128">Это значение позволяет пользователю запускать восстановление на наборе файлов журнала даже в случае отсутствия баз данных, которые были присоединены к набору файлов журнала в некоторый момент.</span><span class="sxs-lookup"><span data-stu-id="695a8-128">This value enables the user to run recovery on a set of log files, even in the absence of the databases that were attached to the log file set at some point.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="695a8-129">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="695a8-129">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="695a8-130">Это значение позволяет пользователю выполнять восстановление, но только до (и не включая) этапа отката.</span><span class="sxs-lookup"><span data-stu-id="695a8-130">This value enables the user to perform recovery, but only up to (and not including) the Undo phase.</span></span> <span data-ttu-id="695a8-131">С помощью этого значения можно копировать и применять дополнительные журналы транзакций.</span><span class="sxs-lookup"><span data-stu-id="695a8-131">Using this value, additional transaction logs can be copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="695a8-132">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="695a8-132">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="695a8-133">Это значение приводит к усечению файлов журнала при успешном мягком восстановлении.</span><span class="sxs-lookup"><span data-stu-id="695a8-133">This value causes log files to be truncated during a successful soft recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="695a8-134">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="695a8-134">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="695a8-135">Это значение приводит к тому, что в отсутствующей записи схемы базы данных по умолчанию устанавливается одно и то же расположение.</span><span class="sxs-lookup"><span data-stu-id="695a8-135">This value causes a missing database map entry to default to the same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="695a8-136">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="695a8-136">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="695a8-137">Это значение приводит к тому, что журналы, потерянные от конца потока журнала, будут игнорироваться во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="695a8-137">This value causes logs lost from the end of the log stream to be ignored during a recovery.</span></span></p>
<p><span data-ttu-id="695a8-138"><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="695a8-138"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="695a8-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="695a8-139">Return Value</span></span>

<span data-ttu-id="695a8-140">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="695a8-140">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="695a8-141">Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="695a8-141">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="695a8-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="695a8-142">Remarks</span></span>

<span data-ttu-id="695a8-143">Экземпляр должен быть инициализирован вызовом функции **JetInit3** до того, как он может использоваться любым другим, кроме функции [жетсетсистемпараметер](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="695a8-143">An instance must be initialized with a call to the **JetInit3** function before it can be used by anything other than the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span>

<span data-ttu-id="695a8-144">Экземпляр уничтожается вызовом функции [жеттерм](./jetterm-function.md) , даже если этот экземпляр никогда не был инициализирован с помощью функции [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="695a8-144">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized by using the [JetInit](./jetinit-function.md) function.</span></span> <span data-ttu-id="695a8-145">Экземпляр — это единица восстановления для ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="695a8-145">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="695a8-146">Он управляет жизненным циклом всех файлов, используемых для защиты целостности данных в наборе файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="695a8-146">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="695a8-147">Эти файлы включают файл контрольных точек и файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="695a8-147">These files include the checkpoint file and the transaction log files.</span></span> <span data-ttu-id="695a8-148">Обратите внимание, что [жеттерм](./jetterm-function.md) не следует вызывать, если происходит сбой функции **JetInit3** .</span><span class="sxs-lookup"><span data-stu-id="695a8-148">Note that [JetTerm](./jetterm-function.md) should not be called if the **JetInit3** function fails.</span></span> <span data-ttu-id="695a8-149">Однако [жеттерм](./jetterm-function.md) должен вызываться для всех экземпляров, созданных с помощью **JetCreateInstance2** , если **JetInit3** никогда не вызывался, или если **JetInit3** успешно.</span><span class="sxs-lookup"><span data-stu-id="695a8-149">However, [JetTerm](./jetterm-function.md) should still be called for all instances created by **JetCreateInstance2** if **JetInit3** was never called or if **JetInit3** succeeds.</span></span>

<span data-ttu-id="695a8-150">Если восстановление выполняется на наборе журналов, для которых имеются не все связанные базы данных (возвращающие ошибку JET_errAttachedDatabaseMismatch в нормальных обстоятельствах), и клиент хочет, чтобы восстановление продолжалось, несмотря на отсутствующие базы данных, то JET_bitReplayIgnoreMissingDB ошибка используется для продолжения восстановления доступных баз данных.</span><span class="sxs-lookup"><span data-stu-id="695a8-150">If recovery is running on a set of logs for which not all of the related databases are present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wants recovery to continue despite the missing databases, the JET_bitReplayIgnoreMissingDB error is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="695a8-151">Так как восстановление после сбоя обычно происходит не на том же компьютере (и с той же конфигурацией), что и во время сбоя, база данных обычно не меняет расположение.</span><span class="sxs-lookup"><span data-stu-id="695a8-151">Because crash recovery doesn't usually happen on the same machine (and with the same configuration) as at the time of the crash, a database typically doesn't change location.</span></span> <span data-ttu-id="695a8-152">В некоторых сценариях, таких как перемещение файлов на другой компьютер или восстановление резервной копии моментальных снимков в разные места, это не так.</span><span class="sxs-lookup"><span data-stu-id="695a8-152">In certain scenarios, such as moving files to a different machine or restoring snapshot backup to different locations, this is no longer true.</span></span> <span data-ttu-id="695a8-153">Функция **JetInit3** позволяет указать сопоставление (с использованием структур [JET_RSTINFO](./jet-rstinfo-structure.md) и [JET_RSTMAP](./jet-rstmap-structure.md) ) между старым расположением базы данных и ее новым расположением.</span><span class="sxs-lookup"><span data-stu-id="695a8-153">The **JetInit3** function enables you to specify a mapping (using the [JET_RSTINFO](./jet-rstinfo-structure.md) and [JET_RSTMAP](./jet-rstmap-structure.md) structures) between the old database location and its new location.</span></span> <span data-ttu-id="695a8-154">На самом деле требуется только новое расположение, если файлы базы данных находятся в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="695a8-154">In fact, you need only the new location as long as the database files are present at that location.</span></span> <span data-ttu-id="695a8-155">Как только вы узнаете о расположении восстановленных баз данных, подпись базы данных будет использоваться для обнаружения базы данных в процессе восстановления.</span><span class="sxs-lookup"><span data-stu-id="695a8-155">As soon as you know the locations of the restored databases, the database signature will be used to identify the database through the restore process.</span></span> <span data-ttu-id="695a8-156">Исходное расположение базы данных потребуется только в том случае, если необходимо повторно создать базу данных, в этом случае подпись будет известна.</span><span class="sxs-lookup"><span data-stu-id="695a8-156">You'll need the original database location only if you need to re-create a database, in which case the signature is known.</span></span>

<span data-ttu-id="695a8-157">Кроме того, если необходимо отменить восстановление после операции отмены, можно указать конкретную точку, в которой будет прерываться восстановление.</span><span class="sxs-lookup"><span data-stu-id="695a8-157">In addition, if you need to stop a recovery after an Undo operation, you can specify a particular log position at which recovery will stop.</span></span> <span data-ttu-id="695a8-158">Обратите внимание, что сюда входит возможность отмены в конце конкретного создания журнала, если указанная позиция является частью поколения, но находится за концом фактического журнала.</span><span class="sxs-lookup"><span data-stu-id="695a8-158">Note that this includes the ability to stop at the end of a particular log generation if the specified position is part of the generation but past the end of the actual log.</span></span>

<span data-ttu-id="695a8-159">Дополнительные сведения см. в подразделе "Примечания" раздела [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="695a8-159">For more information, see the "Remarks" section in the [JetInit](./jetinit-function.md) topic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="695a8-160">Требования</span><span class="sxs-lookup"><span data-stu-id="695a8-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="695a8-161">Клиент</span><span class="sxs-lookup"><span data-stu-id="695a8-161">Client</span></span></p></td>
<td><p><span data-ttu-id="695a8-162">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="695a8-162">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="695a8-163">Сервер</span><span class="sxs-lookup"><span data-stu-id="695a8-163">Server</span></span></p></td>
<td><p><span data-ttu-id="695a8-164">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="695a8-164">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="695a8-165">Header</span><span class="sxs-lookup"><span data-stu-id="695a8-165">Header</span></span></p></td>
<td><p><span data-ttu-id="695a8-166">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="695a8-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="695a8-167">Библиотека</span><span class="sxs-lookup"><span data-stu-id="695a8-167">Library</span></span></p></td>
<td><p><span data-ttu-id="695a8-168">Использует ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="695a8-168">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="695a8-169">DLL</span><span class="sxs-lookup"><span data-stu-id="695a8-169">DLL</span></span></p></td>
<td><p><span data-ttu-id="695a8-170">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="695a8-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="695a8-171">Юникод</span><span class="sxs-lookup"><span data-stu-id="695a8-171">Unicode</span></span></p></td>
<td><p><span data-ttu-id="695a8-172">Реализуется как <strong>JetInit3W</strong> (Юникод) и <strong>JetInit3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="695a8-172">Implemented as <strong>JetInit3W</strong> (Unicode) and <strong>JetInit3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="695a8-173">См. также:</span><span class="sxs-lookup"><span data-stu-id="695a8-173">See Also</span></span>

[<span data-ttu-id="695a8-174">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="695a8-174">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="695a8-175">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="695a8-175">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="695a8-176">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="695a8-176">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="695a8-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="695a8-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="695a8-178">JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="695a8-178">JET_RSTINFO</span></span>](./jet-rstinfo-structure.md)  
[<span data-ttu-id="695a8-179">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="695a8-179">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="695a8-180">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="695a8-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="695a8-181">жетинит</span><span class="sxs-lookup"><span data-stu-id="695a8-181">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="695a8-182">JetInit2</span><span class="sxs-lookup"><span data-stu-id="695a8-182">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="695a8-183">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="695a8-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="695a8-184">Параметры ресурсов</span><span class="sxs-lookup"><span data-stu-id="695a8-184">Resource Parameters</span></span>](./resource-parameters.md)
