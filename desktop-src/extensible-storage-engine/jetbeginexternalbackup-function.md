---
description: Дополнительные сведения о функции Жетбегинекстерналбаккуп
title: Функция Жетбегинекстерналбаккуп
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664453"
---
# <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="bba4c-103">Функция Жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="bba4c-103">JetBeginExternalBackup Function</span></span>


<span data-ttu-id="bba4c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bba4c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="bba4c-105">Функция Жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="bba4c-105">JetBeginExternalBackup Function</span></span>

<span data-ttu-id="bba4c-106">Функция **жетбегинекстерналбаккуп** инициирует внешнюю архивацию, пока ядро и база данных находятся в сети и активны.</span><span class="sxs-lookup"><span data-stu-id="bba4c-106">The **JetBeginExternalBackup** function initiates an external backup while the engine and database is online and active.</span></span> <span data-ttu-id="bba4c-107">**Жетбегинекстерналбаккуп** является первым в серии функций, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).</span><span class="sxs-lookup"><span data-stu-id="bba4c-107">**JetBeginExternalBackup** is the first in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="bba4c-108">Внешнюю резервную копию можно использовать для реализации полных, добавочных или разностных резервных копий.</span><span class="sxs-lookup"><span data-stu-id="bba4c-108">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="bba4c-109">Резервное копирование будет нечетким, в то время как резервная копия будет соответствовать одному моменту времени в журнале транзакций, но контролировать конкретный момент времени невозможно.</span><span class="sxs-lookup"><span data-stu-id="bba4c-109">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="bba4c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba4c-110">Parameters</span></span>

<span data-ttu-id="bba4c-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="bba4c-111">*grbit*</span></span>

<span data-ttu-id="bba4c-112">Группа битов, задающих ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="bba4c-112">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bba4c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bba4c-113">Value</span></span></p></th>
<th><p><span data-ttu-id="bba4c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bba4c-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-115">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="bba4c-115">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="bba4c-116">Этот флаг является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="bba4c-116">This flag is deprecated.</span></span> <span data-ttu-id="bba4c-117">Использование этого бита приведет к возвращению JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="bba4c-117">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-118">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="bba4c-118">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="bba4c-119">Создает добавочное резервное копирование, а не полное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="bba4c-119">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="bba4c-120">Это означает, что резервное копирование выполняется только для файлов журнала с момента последнего полного или добавочного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bba4c-120">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-121">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="bba4c-121">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="bba4c-122">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="bba4c-122">Reserved for future use.</span></span> <span data-ttu-id="bba4c-123">Определено для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bba4c-123">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="bba4c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bba4c-124">Return Value</span></span>

<span data-ttu-id="bba4c-125">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="bba4c-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bba4c-126">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bba4c-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bba4c-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bba4c-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="bba4c-128">Описание</span><span class="sxs-lookup"><span data-stu-id="bba4c-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bba4c-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bba4c-130">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bba4c-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="bba4c-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="bba4c-132">Если внешняя резервная копия или резервная копия моментального снимка уже находится в процессе, возвращается эта ошибка, пока не будет вызван <strong>жетбегинекстерналбаккуп</strong> (или один из вариантов).</span><span class="sxs-lookup"><span data-stu-id="bba4c-132">If an external backup or snapshot backup is already in process, this error will be returned, until <strong>JetBeginExternalBackup</strong> (or one of the variants of it) is called.</span></span> <span data-ttu-id="bba4c-133">ESE допускает только одну оперативную архивацию за раз.</span><span class="sxs-lookup"><span data-stu-id="bba4c-133">ESE allows only one online backup at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-134">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="bba4c-134">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="bba4c-135">Экземпляр или ядро СУБД либо находится в состоянии восстановления, либо на этапе завершения работы или прекращения.</span><span class="sxs-lookup"><span data-stu-id="bba4c-135">The instance or database engine is either in recovery or in a shutdown or termination phase.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-136">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="bba4c-136">JET_errCheckpointCorrupt</span></span></p></td>
<td><p><span data-ttu-id="bba4c-137">Не удалось прочитать файл контрольных точек в полной резервной копии, или не удалось проверить файл.</span><span class="sxs-lookup"><span data-stu-id="bba4c-137">On a full backup, the checkpoint file could not be read, or the file could not be verified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-138">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="bba4c-138">JET_errCheckpointFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="bba4c-139">Не удалось найти файл контрольных точек в полной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="bba4c-139">On a full backup, the checkpoint file could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bba4c-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bba4c-141">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="bba4c-141">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bba4c-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bba4c-143">Операция не может быть завершена, поскольку в экземпляре, связанном с сеансом, произошла неустранимая ошибка, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="bba4c-143">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="bba4c-144"><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bba4c-144"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-145">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="bba4c-145">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="bba4c-146">Циклическое ведение журнала включено, а указанный тип резервного копирования — JET_bitBackupIncremental.</span><span class="sxs-lookup"><span data-stu-id="bba4c-146">Circular logging is enabled and the backup type specified is JET_bitBackupIncremental.</span></span> <span data-ttu-id="bba4c-147">Сведения о том, как управлять циклическим или нециклическим ведением журнала, см. в разделе <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> <strong>ошибок в журнале транзакций</strong> .</span><span class="sxs-lookup"><span data-stu-id="bba4c-147">See <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in the <strong>Transaction Log Errors</strong> for information about how to control circular or non-circular logging.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-148">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="bba4c-148">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="bba4c-149">Один или несколько элементов <em>грбит</em> недопустимы.</span><span class="sxs-lookup"><span data-stu-id="bba4c-149">One or more of the <em>grbit</em> members was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-150">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="bba4c-150">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="bba4c-151">Восстановление или ведение журнала отключено.</span><span class="sxs-lookup"><span data-stu-id="bba4c-151">Recovery or logging is disabled.</span></span> <span data-ttu-id="bba4c-152">Невозможно выполнить оперативную архивацию, если ведение журнала отключено.</span><span class="sxs-lookup"><span data-stu-id="bba4c-152">You cannot do an online backup if logging is disabled.</span></span> <span data-ttu-id="bba4c-153">Дополнительные сведения о ведении журналов и восстановлении см. в разделе <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span><span class="sxs-lookup"><span data-stu-id="bba4c-153">For more information about logging and recovery, see <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-154">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="bba4c-154">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="bba4c-155">Модуль остановил запись на диск журнала из-за переполнения журнала или ошибок ввода-вывода на диск.</span><span class="sxs-lookup"><span data-stu-id="bba4c-155">The engine has stopped writing to the log drive, due to log being full or disk IO errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-156">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="bba4c-156">JET_errMissingFullBackup</span></span></p></td>
<td><p><span data-ttu-id="bba4c-157">Было указано добавочное резервное копирование (с JET_bitBackupIncremental) и никогда не было полной резервной копии для одной из присоединенных баз данных для набора журналов.</span><span class="sxs-lookup"><span data-stu-id="bba4c-157">The incremental backup was specified (with JET_bitBackupIncremental), and never was a full backup taken for one of the attached databases for the logging set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bba4c-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bba4c-159">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="bba4c-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="bba4c-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="bba4c-161">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="bba4c-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bba4c-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bba4c-163">Операция не может быть завершена, так как выполняется операция восстановления для экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="bba4c-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-164">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="bba4c-164">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="bba4c-165">Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</span><span class="sxs-lookup"><span data-stu-id="bba4c-165">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bba4c-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bba4c-167">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="bba4c-167">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bba4c-168">Если функция выполнена, инициируется внешнее резервное копирование и инициализируется обработчик состояния резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bba4c-168">If the function succeeds, an external backup is initiated and the backup state engine is initialized.</span></span> <span data-ttu-id="bba4c-169">Последующие API теперь можно вызывать для завершения внешней последовательности и потока резервного копирования или чтения файла базы данных, файла исправления базы данных (если поддерживается) и файла журнала.</span><span class="sxs-lookup"><span data-stu-id="bba4c-169">Subsequent APIs can now be called to complete the external backup sequence and stream or read off the database file, the database patch file (if supported), and the log file.</span></span> <span data-ttu-id="bba4c-170">Событие может регистрироваться в том случае, если внешнее резервное копирование началось.</span><span class="sxs-lookup"><span data-stu-id="bba4c-170">An event can be logged that an external backup has begun.</span></span>

<span data-ttu-id="bba4c-171">Если функция завершается ошибкой, сеанс резервного копирования не запускается.</span><span class="sxs-lookup"><span data-stu-id="bba4c-171">If the function fails, the backup session will not be initiated.</span></span> <span data-ttu-id="bba4c-172">Если выполняется другой сеанс резервного копирования, он не будет отменен.</span><span class="sxs-lookup"><span data-stu-id="bba4c-172">If another backup session is in progress, it will not be cancelled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bba4c-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bba4c-173">Remarks</span></span>

<span data-ttu-id="bba4c-174">Процесс внешнего резервного копирования (как запущенный **жетбегинекстерналбаккуп**) разрешается в оперативной резервной копии нечеткой транзакции для всего экземпляра на целевое устройство в виде потока.</span><span class="sxs-lookup"><span data-stu-id="bba4c-174">The external backup process (as started by **JetBeginExternalBackup**) is designed to allow a fuzzy transaction online backup of the entire instance to a target device as a stream.</span></span> <span data-ttu-id="bba4c-175">Резервная копия будет содержать все файлы базы данных, присоединенные к экземпляру с помощью [жетаттачдатабасе](./jetattachdatabase-function.md) (для полной резервной копии), а также связанные файлы исправлений базы данных (если они поддерживаются) и, наконец, файлы журнала транзакций, созданные в процессе резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bba4c-175">The backup will contain all the database files that are attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) (for a full backup), followed by their associated database patch files (if supported), and finally by the transaction log files that were generated during the backup process.</span></span> <span data-ttu-id="bba4c-176">Конечным результатом будет набор файлов, которые могут быть восстановлены из потока, возможно, объединены с существующими файлами базы данных и журнала, и, наконец, восстановлены в стабильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="bba4c-176">The end result will be a set of files that can be restored from the stream, possibly combined with existing database and log files, and finally recovered to a consistent state.</span></span>

<span data-ttu-id="bba4c-177">Общий порядок операций с полной резервной копией состоит из следующих вызовов.</span><span class="sxs-lookup"><span data-stu-id="bba4c-177">The general order of operations for a full backup consists of the following calls.</span></span> <span data-ttu-id="bba4c-178">Во-первых, для запуска процесса резервного копирования вызывается **жетбегинекстерналбаккуп** .</span><span class="sxs-lookup"><span data-stu-id="bba4c-178">First, **JetBeginExternalBackup** is called to start the backup process.</span></span> <span data-ttu-id="bba4c-179">Затем вызывается [жетжетаттачинфо](./jetgetattachinfo-function.md) для получения списка баз данных, присоединенных к экземпляру, для которого необходимо создать резервную копию.</span><span class="sxs-lookup"><span data-stu-id="bba4c-179">Then, [JetGetAttachInfo](./jetgetattachinfo-function.md) is called to get the list of databases that are attached to the instance that needs to be backed up.</span></span> <span data-ttu-id="bba4c-180">Для каждой из этих баз данных вызывается [жетопенфиле](./jetopenfile-function.md) , за которым следует ряд вызовов [жетреадфиле](./jetreadfile-function.md) , а затем вызов [жетклосефиле](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="bba4c-180">For each of these databases, [JetOpenFile](./jetopenfile-function.md) is called, followed by a number of [JetReadFile](./jetreadfile-function.md) calls, and then by a call to [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="bba4c-181">Затем вызывается [жетжетлогинфо](./jetgetloginfo-function.md) для получения списка обновлений базы данных и файлов журналов для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bba4c-181">Then, [JetGetLogInfo](./jetgetloginfo-function.md) is called to get a list of database patch and log files to be backed up.</span></span> <span data-ttu-id="bba4c-182">Для каждого из этих файлов выполняется другая последовательность вызовов [жетопенфиле](./jetopenfile-function.md), [жетреадфиле](./jetreadfile-function.md)и [жетклосефиле](./jetclosefile-function.md) .</span><span class="sxs-lookup"><span data-stu-id="bba4c-182">For each of these files, another sequence of [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md), and [JetCloseFile](./jetclosefile-function.md) calls are made.</span></span> <span data-ttu-id="bba4c-183">Затем все нежелательные файлы журнала транзакций удаляются с помощью [жеттрункателог](./jettruncatelog-function.md).</span><span class="sxs-lookup"><span data-stu-id="bba4c-183">Then, any undesired transaction log files are deleted using [JetTruncateLog](./jettruncatelog-function.md).</span></span> <span data-ttu-id="bba4c-184">Наконец, резервное копирование завершается вызовом [жетендекстерналбаккуп](./jetendexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="bba4c-184">Finally, the backup is ended by a call to [JetEndExternalBackup](./jetendexternalbackup-function.md).</span></span>

<span data-ttu-id="bba4c-185">Также можно изменить этот набор шагов, чтобы выполнить добавочное резервное копирование экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bba4c-185">It is also possible to modify this set of steps to perform an incremental backup of the instance.</span></span> <span data-ttu-id="bba4c-186">Добавочное резервное копирование перечисляет и выполняет резервное копирование файлов журналов.</span><span class="sxs-lookup"><span data-stu-id="bba4c-186">An incremental backup enumerates and backs up log files.</span></span> <span data-ttu-id="bba4c-187">Добавочное резервное копирование возможно только в том случае, если циклическое ведение журнала не включено.</span><span class="sxs-lookup"><span data-stu-id="bba4c-187">Incremental backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="bba4c-188">Также можно изменить этот набор шагов, чтобы разрешить выполнение последующих разностных резервных копий экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bba4c-188">It is also possible to modify this set of steps to allow subsequent differential backups of the instance to be performed.</span></span> <span data-ttu-id="bba4c-189">Чтобы выполнить разностное резервное копирование, не вызывайте [жеттрункателог](./jettruncatelog-function.md) в предыдущей полной или добавочной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="bba4c-189">To perform a differential backup, do not call [JetTruncateLog](./jettruncatelog-function.md) in the previous full or incremental backup.</span></span> <span data-ttu-id="bba4c-190">Не вызывая [жеттрункателог](./jettruncatelog-function.md), вы включаете последующие резервные копии в соответствии с последним полным или добавочным резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="bba4c-190">By not calling [JetTruncateLog](./jettruncatelog-function.md), you enable subsequent backups to be differential with respect to the last full or incremental backup.</span></span> <span data-ttu-id="bba4c-191">Разностное резервное копирование возможно только в том случае, если циклическое ведение журнала не включено.</span><span class="sxs-lookup"><span data-stu-id="bba4c-191">Differential backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="bba4c-192">Файл исправления базы данных — это специальный вспомогательный файл, который используется для хранения образов страниц базы данных при определенных обстоятельствах во время резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bba4c-192">The database patch file is a special auxiliary file that is used to store database page images under certain circumstances during the backup.</span></span> <span data-ttu-id="bba4c-193">Этот файл должен находиться в том же расположении, что и связанная с ним база данных во время операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="bba4c-193">This file must be present in the same location as its associated database during a restore operation.</span></span> <span data-ttu-id="bba4c-194">Этот файл используется только в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="bba4c-194">This file is only used in Windows 2000.</span></span> <span data-ttu-id="bba4c-195">В результате все приложения, написанные для работы с Windows 2000 и другими выпусками, должны поддерживать файлы исправления базы данных, если они существуют, но также не должны завершаться ошибкой, если они отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="bba4c-195">As a result, any application that is written to work against Windows 2000 and other releases must support database patch files, if they are present, but also must not fail if they are not present.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bba4c-196">Требования</span><span class="sxs-lookup"><span data-stu-id="bba4c-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-197"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="bba4c-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bba4c-198">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bba4c-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-199"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bba4c-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bba4c-200">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bba4c-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-201"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bba4c-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bba4c-202">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bba4c-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba4c-203"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="bba4c-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bba4c-204">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bba4c-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bba4c-205"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="bba4c-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bba4c-206">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bba4c-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bba4c-207">См. также:</span><span class="sxs-lookup"><span data-stu-id="bba4c-207">See Also</span></span>

[<span data-ttu-id="bba4c-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bba4c-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bba4c-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bba4c-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bba4c-210">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bba4c-210">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="bba4c-211">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="bba4c-211">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="bba4c-212">жетбегинекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="bba4c-212">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="bba4c-213">жетклосефиле</span><span class="sxs-lookup"><span data-stu-id="bba4c-213">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="bba4c-214">жетендекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="bba4c-214">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="bba4c-215">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="bba4c-215">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="bba4c-216">жетжетаттачинфо</span><span class="sxs-lookup"><span data-stu-id="bba4c-216">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="bba4c-217">жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="bba4c-217">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="bba4c-218">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="bba4c-218">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="bba4c-219">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="bba4c-219">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="bba4c-220">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="bba4c-220">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="bba4c-221">жеттрункателог</span><span class="sxs-lookup"><span data-stu-id="bba4c-221">JetTruncateLog</span></span>](./jettruncatelog-function.md)
