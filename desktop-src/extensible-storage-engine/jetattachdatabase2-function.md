---
description: Дополнительные сведения о функции JetAttachDatabase2
title: Функция JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712875"
---
# <a name="jetattachdatabase2-function"></a><span data-ttu-id="0070f-103">Функция JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="0070f-103">JetAttachDatabase2 Function</span></span>


<span data-ttu-id="0070f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0070f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase2-function"></a><span data-ttu-id="0070f-105">Функция JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="0070f-105">JetAttachDatabase2 Function</span></span>

<span data-ttu-id="0070f-106">Функция **JetAttachDatabase2** присоединяет файл базы данных для использования с экземпляром базы данных и задает максимальный размер для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="0070f-106">The **JetAttachDatabase2** function attaches a database file for use with a database instance and specifies a maximum size for that database.</span></span> <span data-ttu-id="0070f-107">Чтобы использовать базу данных, ее потребуется впоследствии открыть с помощью [жетопендатабасе](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="0070f-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="0070f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0070f-108">Parameters</span></span>

<span data-ttu-id="0070f-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="0070f-109">*sesid*</span></span>

<span data-ttu-id="0070f-110">Контекст сеанса базы данных, который будет использоваться для вызова API.</span><span class="sxs-lookup"><span data-stu-id="0070f-110">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="0070f-111">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="0070f-111">*szFilename*</span></span>

<span data-ttu-id="0070f-112">Имя присоединяемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="0070f-112">The name of the database to attach.</span></span>

<span data-ttu-id="0070f-113">*кпгдатабасесиземакс*</span><span class="sxs-lookup"><span data-stu-id="0070f-113">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="0070f-114">Максимальный размер (в страницах базы данных) для базы данных.</span><span class="sxs-lookup"><span data-stu-id="0070f-114">The maximum size, in database pages, for database.</span></span> <span data-ttu-id="0070f-115">Размер страницы базы данных по умолчанию — 4 килобайта, который можно изменить с помощью функции [жетсетсистемпараметер](./jetsetsystemparameter-function.md) перед созданием базы данных.</span><span class="sxs-lookup"><span data-stu-id="0070f-115">The default database page size is 4 kilobytes, which can be changed using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function prior to creating a database.</span></span>

<span data-ttu-id="0070f-116">Передача нуля означает отсутствие ограничения, принудительно применяемого ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="0070f-116">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="0070f-117">*грбит*</span><span class="sxs-lookup"><span data-stu-id="0070f-117">*grbit*</span></span>

<span data-ttu-id="0070f-118">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, в том числе ноль или более следующих:</span><span class="sxs-lookup"><span data-stu-id="0070f-118">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0070f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0070f-119">Value</span></span></p></th>
<th><p><span data-ttu-id="0070f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0070f-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0070f-121">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="0070f-121">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="0070f-122">Если параметр <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> установлен, все индексы данных в Юникоде будут удалены.</span><span class="sxs-lookup"><span data-stu-id="0070f-122">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="0070f-123">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="0070f-123">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-124">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="0070f-124">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="0070f-125">Все индексы данных в Юникоде будут удалены независимо от значения параметра <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="0070f-125">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="0070f-126">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="0070f-126">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0070f-127">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="0070f-127">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="0070f-128">Предотвращает изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0070f-128">Prevents modifications to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-129">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="0070f-129">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="0070f-130">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="0070f-130">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0070f-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0070f-131">Return Value</span></span>

<span data-ttu-id="0070f-132">Функция возвращает один из [JET_ERR](./jet-err.md) кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="0070f-132">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="0070f-133">Чаще всего возвращаются следующие.</span><span class="sxs-lookup"><span data-stu-id="0070f-133">The following are the most commonly returned.</span></span> <span data-ttu-id="0070f-134">(Полный список ошибок для этого API см. в разделе [расширенные коды ошибок подсистемы хранилища](./extensible-storage-engine-error-codes.md).)</span><span class="sxs-lookup"><span data-stu-id="0070f-134">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0070f-135">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0070f-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="0070f-136">Описание</span><span class="sxs-lookup"><span data-stu-id="0070f-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0070f-137">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0070f-137">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0070f-138">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0070f-138">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-139">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="0070f-139">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="0070f-140">Присоединение базы данных во время резервного копирования не допускается.</span><span class="sxs-lookup"><span data-stu-id="0070f-140">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0070f-141">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="0070f-141">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="0070f-142">Файл базы данных, указанный параметром <em>сзфиленаме</em> , должен быть доступным для записи.</span><span class="sxs-lookup"><span data-stu-id="0070f-142">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="0070f-143">Атрибут Read-Only не должен быть задан, а выполняющийся процесс должен иметь достаточные привилегии для записи в файл.</span><span class="sxs-lookup"><span data-stu-id="0070f-143">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="0070f-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="0070f-145">Файл базы данных уже открыт другим процессом.</span><span class="sxs-lookup"><span data-stu-id="0070f-145">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0070f-146">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="0070f-146">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="0070f-147">В <em>сзфиленаме</em>указан недопустимый путь.</span><span class="sxs-lookup"><span data-stu-id="0070f-147">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="0070f-148"><em>сзфиленаме</em> не должно иметь значение NULL и ссылаться на допустимый путь.</span><span class="sxs-lookup"><span data-stu-id="0070f-148"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-149">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="0070f-149">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="0070f-150">Файл базы данных уже присоединен к другому сеансу.</span><span class="sxs-lookup"><span data-stu-id="0070f-150">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0070f-151">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="0070f-151">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="0070f-152">Файл, указанный в <em>сзфиленаме</em> , не существует.</span><span class="sxs-lookup"><span data-stu-id="0070f-152">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-153">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="0070f-153">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="0070f-154">Ошибка в первичном индексе.</span><span class="sxs-lookup"><span data-stu-id="0070f-154">There is an error with the primary index.</span></span> <span data-ttu-id="0070f-155">Это может быть из-за физического повреждения (например, повреждения диска или памяти).</span><span class="sxs-lookup"><span data-stu-id="0070f-155">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="0070f-156">Она также может быть возвращена при присоединении базы данных, которая была изменена в более старой операционной системе, а первичный индекс — в столбце с данными в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="0070f-156">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="0070f-157">Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="0070f-157">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0070f-158">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="0070f-158">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="0070f-159">Ошибка в дополнительном индексе.</span><span class="sxs-lookup"><span data-stu-id="0070f-159">There is an error with a secondary index.</span></span> <span data-ttu-id="0070f-160">Это может быть из-за физического повреждения (например, повреждения диска или памяти).</span><span class="sxs-lookup"><span data-stu-id="0070f-160">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="0070f-161">Он также может возвращаться при присоединении базы данных, которая была изменена в более старой версии операционной системы, а вторичный индекс — над столбцом с данными в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="0070f-161">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="0070f-162">Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="0070f-162">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="0070f-163">Вторичные индексы полностью перестраиваются при дефрагментации базы данных с помощью автономной программы, используя следующую команду: <strong>Esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="0070f-163">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-164">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="0070f-164">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="0070f-165">В каждом экземпляре может быть присоединено только конечное число баз данных.</span><span class="sxs-lookup"><span data-stu-id="0070f-165">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="0070f-166">Сейчас ограничение составляет семь баз данных на экземпляр.</span><span class="sxs-lookup"><span data-stu-id="0070f-166">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0070f-167">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="0070f-167">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="0070f-168">Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</span><span class="sxs-lookup"><span data-stu-id="0070f-168">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="0070f-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0070f-169">Remarks</span></span>

<span data-ttu-id="0070f-170">Файл базы данных отсоединяется с помощью [жетдетачдатабасе](./jetdetachdatabase-function.md) или [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="0070f-170">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="0070f-171">См. раздел [жетаттачдатабасе](./jetattachdatabase-function.md) for remarks.</span><span class="sxs-lookup"><span data-stu-id="0070f-171">See [JetAttachDatabase](./jetattachdatabase-function.md) for remarks.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0070f-172">Требования</span><span class="sxs-lookup"><span data-stu-id="0070f-172">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0070f-173"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="0070f-173"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0070f-174">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0070f-174">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-175"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0070f-175"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0070f-176">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0070f-176">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0070f-177"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0070f-177"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0070f-178">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0070f-178">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-179"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="0070f-179"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0070f-180">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0070f-180">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0070f-181"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="0070f-181"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0070f-182">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0070f-182">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0070f-183"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="0070f-183"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0070f-184">Реализуется как <strong>JetAttachDatabase2W</strong> (Юникод) и <strong>JetAttachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0070f-184">Implemented as <strong>JetAttachDatabase2W</strong> (Unicode) and <strong>JetAttachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0070f-185">См. также:</span><span class="sxs-lookup"><span data-stu-id="0070f-185">See Also</span></span>

[<span data-ttu-id="0070f-186">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="0070f-186">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="0070f-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0070f-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0070f-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0070f-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0070f-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0070f-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0070f-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0070f-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0070f-191">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="0070f-191">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="0070f-192">жеткреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="0070f-192">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="0070f-193">жетопендатабасе</span><span class="sxs-lookup"><span data-stu-id="0070f-193">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="0070f-194">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="0070f-194">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
