---
description: Дополнительные сведения о функции Жетаттачдатабасе
title: Функция JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262864"
---
# <a name="jetattachdatabase-function"></a><span data-ttu-id="e3ca2-103">Функция JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="e3ca2-103">JetAttachDatabase Function</span></span>


<span data-ttu-id="e3ca2-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e3ca2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase-function"></a><span data-ttu-id="e3ca2-105">Функция JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="e3ca2-105">JetAttachDatabase Function</span></span>

<span data-ttu-id="e3ca2-106">Функция **жетаттачдатабасе** присоединяет файл базы данных для использования с экземпляром базы данных.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-106">The **JetAttachDatabase** function attaches a database file for use with a database instance.</span></span> <span data-ttu-id="e3ca2-107">Чтобы использовать базу данных, ее потребуется впоследствии открыть с помощью [жетопендатабасе](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="e3ca2-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e3ca2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3ca2-108">Parameters</span></span>

<span data-ttu-id="e3ca2-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="e3ca2-109">*sesid*</span></span>

<span data-ttu-id="e3ca2-110">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="e3ca2-111">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="e3ca2-111">*szFilename*</span></span>

<span data-ttu-id="e3ca2-112">Имя присоединяемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-112">The name of the database to attach.</span></span>

<span data-ttu-id="e3ca2-113">*грбит*</span><span class="sxs-lookup"><span data-stu-id="e3ca2-113">*grbit*</span></span>

<span data-ttu-id="e3ca2-114">Группа битов, задающих ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-114">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3ca2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e3ca2-115">Value</span></span></p></th>
<th><p><span data-ttu-id="e3ca2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e3ca2-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-117">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="e3ca2-117">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-118">Если параметр <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> установлен, все индексы данных в Юникоде будут удалены.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-118">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="e3ca2-119">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e3ca2-119">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-120">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="e3ca2-120">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-121">Все индексы данных в Юникоде будут удалены независимо от значения параметра <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-121">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="e3ca2-122">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e3ca2-122">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-123">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="e3ca2-123">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-124">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-124">Obsolete.</span></span> <span data-ttu-id="e3ca2-125">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-125">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="e3ca2-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-127">Предотвращает изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e3ca2-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3ca2-128">Return Value</span></span>

<span data-ttu-id="e3ca2-129">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e3ca2-130">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e3ca2-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3ca2-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e3ca2-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="e3ca2-132">Описание</span><span class="sxs-lookup"><span data-stu-id="e3ca2-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e3ca2-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-134">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-135">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="e3ca2-135">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-136">Присоединение базы данных во время резервного копирования не допускается.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-136">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-137">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="e3ca2-137">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-138">Файл базы данных, указанный параметром <em>сзфиленаме</em> , должен быть доступным для записи.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-138">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="e3ca2-139">Атрибут Read-Only не должен быть задан, а выполняющийся процесс должен иметь достаточные привилегии для записи в файл.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-139">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-140">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="e3ca2-140">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-141">Файл базы данных уже открыт другим процессом.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-141">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-142">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="e3ca2-142">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-143">В <em>сзфиленаме</em>указан недопустимый путь.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-143">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="e3ca2-144"><em>сзфиленаме</em> не должно иметь значение NULL и ссылаться на допустимый путь.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-144"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-145">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e3ca2-145">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-146">Файл базы данных уже присоединен к другому сеансу.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-146">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-147">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="e3ca2-147">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-148">Ядру СУБД не удается открыть файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-148">The database engine cannot open the database file.</span></span> <span data-ttu-id="e3ca2-149">Возможно, файл используется другим процессом, или у вызывающего объекта недостаточно прав для открытия файла.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-149">The file may be in use by another process or the caller may not have sufficient privileges to open the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="e3ca2-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-151">Файл, указанный в <em>сзфиленаме</em> , не существует.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-151">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-152">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="e3ca2-152">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-153">Ошибка в первичном индексе.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-153">There is an error with the primary index.</span></span> <span data-ttu-id="e3ca2-154">Это может быть из-за физического повреждения (например, повреждения диска или памяти).</span><span class="sxs-lookup"><span data-stu-id="e3ca2-154">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="e3ca2-155">Она также может быть возвращена при присоединении базы данных, которая была изменена в более старой операционной системе, а первичный индекс — в столбце с данными в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-155">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="e3ca2-156">Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-156">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-157">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="e3ca2-157">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-158">Ошибка в дополнительном индексе.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-158">There is an error with a secondary index.</span></span> <span data-ttu-id="e3ca2-159">Это может быть из-за физического повреждения (например, повреждения диска или памяти).</span><span class="sxs-lookup"><span data-stu-id="e3ca2-159">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="e3ca2-160">Он также может возвращаться при присоединении базы данных, которая была изменена в более старой версии операционной системы, а вторичный индекс — над столбцом с данными в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-160">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="e3ca2-161">Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-161">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="e3ca2-162">Вторичные индексы полностью перестраиваются при дефрагментации базы данных с помощью автономной программы, используя следующую команду: <strong>Esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-162">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-163">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="e3ca2-163">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-164">В каждом экземпляре может быть присоединено только конечное число баз данных.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-164">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="e3ca2-165">Сейчас ограничение составляет семь баз данных на экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-165">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-166">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="e3ca2-166">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="e3ca2-167">Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-167">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e3ca2-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3ca2-168">Remarks</span></span>

<span data-ttu-id="e3ca2-169">Вызов **жетаттачдатабасе** эквивалентен вызову [JetAttachDatabase2](./jetattachdatabase2-function.md) и передаче нулевого значения, что означает отсутствие ограничения для параметра *кпгдатабасесиземакс* .</span><span class="sxs-lookup"><span data-stu-id="e3ca2-169">Calling **JetAttachDatabase** is equivalent to calling [JetAttachDatabase2](./jetattachdatabase2-function.md) and passing a value of zero, meaning there is no limit, for the *cpgDatabaseSizeMax* parameter.</span></span>

<span data-ttu-id="e3ca2-170">Присоединение базы данных, доступной для записи (то есть если JET_bitDbReadOnly не было указано в параметре *грбит* ), открывает файл исключительно на уровне операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-170">Attaching a writable database (that is, if JET_bitDbReadOnly was not specified in the *grbit* parameter) will open the file exclusively at the operating system level.</span></span> <span data-ttu-id="e3ca2-171">Ни один другой процесс не сможет открыть файл.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-171">No other process will be able open the file.</span></span> <span data-ttu-id="e3ca2-172">Несколько процессов могут присоединить одну базу данных, открыв их в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-172">It is possible for multiple processes to attach a single database by opening them in read-only mode.</span></span>

<span data-ttu-id="e3ca2-173">Файл базы данных отсоединяется с помощью [жетдетачдатабасе](./jetdetachdatabase-function.md) или [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="e3ca2-173">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="e3ca2-174">Параметры проверки индексов</span><span class="sxs-lookup"><span data-stu-id="e3ca2-174">Index-checking parameters</span></span>

<span data-ttu-id="e3ca2-175">Разные версии Windows вынормализуются текст в Юникоде различными способами.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-175">Different versions of Windows normalize Unicode text in different ways.</span></span> <span data-ttu-id="e3ca2-176">Это означает, что индексы, созданные в одной версии Windows, могут не работать в других версиях.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-176">That means indexes built under one version of Windows may not work on other versions.</span></span>

<span data-ttu-id="e3ca2-177">До Windows Server 2003 при изменении версии операционной системы (включая установку пакета обновления) каждый индекс данных в Юникоде находился в потенциально поврежденном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-177">Prior to Windows Server 2003, when the operating system version changed (including installation of a Service Pack), every index over Unicode data was in a potentially corrupt state.</span></span>

<span data-ttu-id="e3ca2-178">Индексы, созданные в Windows Server 2003 и более поздних версий, помечаются версией нормализации Юникода, с которой они были построены.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-178">Indexes created in Windows Server 2003 and later are flagged with the version of Unicode normalization with which they were built.</span></span> <span data-ttu-id="e3ca2-179">Более старые индексы не содержат сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-179">Older indexes contain no version information.</span></span> <span data-ttu-id="e3ca2-180">Большинство изменений нормализации Юникода состоит из добавления новых символов, а кодовые точки, которые ранее не были определены, теперь определяются и нормализуются по-разному.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-180">Most Unicode normalization changes consist of adding new characters, code points which were previously undefined are now defined and normalize differently.</span></span> <span data-ttu-id="e3ca2-181">Таким образом, если двоичные данные хранятся в столбце в Юникоде, они будут по-разному нормализованы по мере определения новых кодовых точек.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-181">Thus, if binary data is stored in a Unicode column, it will normalize differently as new code points are defined.</span></span>

<span data-ttu-id="e3ca2-182">Начиная с Windows Server 2003, ядро базы данных ESE отслеживает записи индекса в Юникоде, содержащие неопределенные кодовые точки.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-182">As of Windows Server 2003, the ESE database engine tracks Unicode index entries that contain undefined code points.</span></span> <span data-ttu-id="e3ca2-183">Их можно использовать для исправления индекса при изменении набора определенных символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-183">These can be used to fix an index when the set of defined Unicode characters changes.</span></span>

<span data-ttu-id="e3ca2-184">Эти параметры управляют тем, что происходит, когда ядро базы данных ESE подключается к базе данных, которая была в последний раз использована в другой сборке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-184">These parameters control what happens when the ESE database engine attaches to a database that was last used under a different build of the operating system.</span></span> <span data-ttu-id="e3ca2-185">Версия операционной системы отмечается в заголовке базы данных.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-185">The operating system version is stamped in the database header.</span></span>

<span data-ttu-id="e3ca2-186">Если [JET_paramEnableIndexChecking](./database-parameters.md) имеет значение **true**, а база данных содержит потенциально поврежденные индексы:</span><span class="sxs-lookup"><span data-stu-id="e3ca2-186">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **TRUE**, and the database contains potentially corrupt indexes:</span></span>

  - <span data-ttu-id="e3ca2-187">**Жетаттачдатабасе** удалит потенциально поврежденные индексы, если *грбит* содержит JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="e3ca2-187">**JetAttachDatabase** will delete the potentially corrupt indexes if *grbit* contains JET_bitDbDeleteCorruptIndexes</span></span>

  - <span data-ttu-id="e3ca2-188">**Жетаттачдатабасе** возвращает ошибку, если *грбит* не содержит JET_bitDbDeleteCorruptIndexes и есть индексы, которые требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-188">**JetAttachDatabase** will return an error if *grbit* does not contain JET_bitDbDeleteCorruptIndexes and there are indexes which need deletion.</span></span>

<span data-ttu-id="e3ca2-189">Если [JET_paramEnableIndexChecking](./database-parameters.md) имеет значение **false**:</span><span class="sxs-lookup"><span data-stu-id="e3ca2-189">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **FALSE**:</span></span>

  - <span data-ttu-id="e3ca2-190">**Жетаттачдатабасе** пропускает потенциально поврежденные индексы и возвращает JET_errSuccess (при условии, что нет других ошибок).</span><span class="sxs-lookup"><span data-stu-id="e3ca2-190">**JetAttachDatabase** will ignore potentially corrupt indexes, and return JET_errSuccess (assuming there were no other errors).</span></span>

<span data-ttu-id="e3ca2-191">Windows Server 2003 и более поздние версии: Если [JET_paramEnableIndexChecking](./database-parameters.md) не была сброшена, то для исправления записей индекса будет использоваться внутренняя таблица адресной привязки.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-191">Windows Server 2003 and later: If [JET_paramEnableIndexChecking](./database-parameters.md) has not been reset, the internal fixup table will be used to fixup index entries.</span></span> <span data-ttu-id="e3ca2-192">Это может не исправить все повреждения индекса, но будет прозрачным для приложения.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-192">This may not fix all index corruptions but will be transparent to the application.</span></span>

<span data-ttu-id="e3ca2-193">Если база данных была подключена только для чтения, индекс не может быть исправлен или удален.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-193">If the database was attached as read-only the index cannot be fixed or deleted.</span></span> <span data-ttu-id="e3ca2-194">В этом случае API возвратит ошибку, например JET_errSecondaryIndexCorrupted или JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-194">In this case, the API will instead return an error, such as JET_errSecondaryIndexCorrupted or JET_errPrimaryIndexCorrupted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e3ca2-195">Требования</span><span class="sxs-lookup"><span data-stu-id="e3ca2-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-196"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca2-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e3ca2-197">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-197">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-198"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca2-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e3ca2-199">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-199">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-200"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca2-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e3ca2-201">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-202"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca2-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e3ca2-203">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ca2-204"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca2-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e3ca2-205">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e3ca2-205">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ca2-206"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca2-206"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e3ca2-207">Реализуется как <strong>жетаддколумнв</strong> (Юникод) и <strong>жетаддколумна</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e3ca2-207">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e3ca2-208">См. также:</span><span class="sxs-lookup"><span data-stu-id="e3ca2-208">See Also</span></span>

[<span data-ttu-id="e3ca2-209">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="e3ca2-209">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="e3ca2-210">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e3ca2-210">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e3ca2-211">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e3ca2-211">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e3ca2-212">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e3ca2-212">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e3ca2-213">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e3ca2-213">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e3ca2-214">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="e3ca2-214">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="e3ca2-215">жеткреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="e3ca2-215">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="e3ca2-216">жетдетачдатабасе</span><span class="sxs-lookup"><span data-stu-id="e3ca2-216">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="e3ca2-217">JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="e3ca2-217">JetDetachDatabase2</span></span>](./jetdetachdatabase2-function.md)  
[<span data-ttu-id="e3ca2-218">жетопендатабасе</span><span class="sxs-lookup"><span data-stu-id="e3ca2-218">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="e3ca2-219">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="e3ca2-219">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
