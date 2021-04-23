---
description: Дополнительные сведения о функции Жеткреатедатабасе
title: Функция JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8fbec76e3b38f9b42c36156b2312a8e77a6b43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712073"
---
# <a name="jetcreatedatabase-function"></a><span data-ttu-id="12caa-103">Функция JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="12caa-103">JetCreateDatabase Function</span></span>


<span data-ttu-id="12caa-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="12caa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase-function"></a><span data-ttu-id="12caa-105">Функция JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="12caa-105">JetCreateDatabase Function</span></span>

<span data-ttu-id="12caa-106">Функция **жеткреатедатабасе** создает и прикрепляет файл базы данных для использования с ЯДРОМ СУБД ESE.</span><span class="sxs-lookup"><span data-stu-id="12caa-106">The **JetCreateDatabase** function creates and attaches a database file to be used with the ESE database engine.</span></span> <span data-ttu-id="12caa-107">Вызов [JetCreateDatabase2](./jetcreatedatabase2-function.md) с *кпгдатабасесиземакс* , установленным в ноль, идентичен вызову **жеткреатедатабасе** с параметром *сзконнект* , имеющим значение null.</span><span class="sxs-lookup"><span data-stu-id="12caa-107">Calling [JetCreateDatabase2](./jetcreatedatabase2-function.md) with *cpgDatabaseSizeMax* set to zero is identical to calling **JetCreateDatabase** with *szConnect* set to NULL.</span></span> <span data-ttu-id="12caa-108">В настоящее время для каждого экземпляра можно создать до семи баз данных.</span><span class="sxs-lookup"><span data-stu-id="12caa-108">Currently, up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="12caa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="12caa-109">Parameters</span></span>

<span data-ttu-id="12caa-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="12caa-110">*sesid*</span></span>

<span data-ttu-id="12caa-111">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="12caa-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="12caa-112">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="12caa-112">*szFilename*</span></span>

<span data-ttu-id="12caa-113">Имя создаваемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="12caa-113">The name of the database to be created.</span></span>

<span data-ttu-id="12caa-114">*сзконнект*</span><span class="sxs-lookup"><span data-stu-id="12caa-114">*szConnect*</span></span>

<span data-ttu-id="12caa-115">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="12caa-115">Reserved for future use.</span></span> <span data-ttu-id="12caa-116">задано значение NULL.</span><span class="sxs-lookup"><span data-stu-id="12caa-116">Set to NULL.</span></span>

<span data-ttu-id="12caa-117">*пдбид*</span><span class="sxs-lookup"><span data-stu-id="12caa-117">*pdbid*</span></span>

<span data-ttu-id="12caa-118">Указатель на буфер, который при успешном вызове содержит идентификатор базы данных.</span><span class="sxs-lookup"><span data-stu-id="12caa-118">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="12caa-119">При сбое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="12caa-119">On failure, the value is undefined.</span></span>

<span data-ttu-id="12caa-120">*грбит*</span><span class="sxs-lookup"><span data-stu-id="12caa-120">*grbit*</span></span>

<span data-ttu-id="12caa-121">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="12caa-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12caa-122">Значение</span><span class="sxs-lookup"><span data-stu-id="12caa-122">Value</span></span></p></th>
<th><p><span data-ttu-id="12caa-123">Значение</span><span class="sxs-lookup"><span data-stu-id="12caa-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12caa-124">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="12caa-124">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="12caa-125">По умолчанию, если вызывается <strong>жеткреатедатабасе</strong> и база данных уже существует, вызов API завершится ошибкой и исходная база данных не будет перезаписана.</span><span class="sxs-lookup"><span data-stu-id="12caa-125">By default, if <strong>JetCreateDatabase</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="12caa-126">JET_bitDbOverwriteExisting изменяет это поведение, а старая база данных будет перезаписана новой.</span><span class="sxs-lookup"><span data-stu-id="12caa-126">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="12caa-127">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="12caa-127">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-128">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="12caa-128">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="12caa-129">JET_bitDbRecoveryOff отключает ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="12caa-129">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="12caa-130">Установка этого бита теряет возможность воспроизведения файлов журнала и восстановления базы данных до стабильного работоспособного состояния после аварийного события.</span><span class="sxs-lookup"><span data-stu-id="12caa-130">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-131">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="12caa-131">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="12caa-132">При установке JET_bitDbShadowingOff будет отключено дублирование некоторых внутренних структур баз данных (теневая).</span><span class="sxs-lookup"><span data-stu-id="12caa-132">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="12caa-133">Дублирование этих структур выполняется для обеспечения устойчивости, поэтому параметр JET_bitDbShadowingOff удалит эту устойчивость.</span><span class="sxs-lookup"><span data-stu-id="12caa-133">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="12caa-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12caa-134">Return Value</span></span>

<span data-ttu-id="12caa-135">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="12caa-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="12caa-136">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="12caa-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12caa-137">Код возврата</span><span class="sxs-lookup"><span data-stu-id="12caa-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="12caa-138">Описание</span><span class="sxs-lookup"><span data-stu-id="12caa-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12caa-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="12caa-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="12caa-140">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="12caa-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-141">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="12caa-141">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="12caa-142">База данных с именем в <em>сзфиленаме</em> уже существует.</span><span class="sxs-lookup"><span data-stu-id="12caa-142">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="12caa-143">При возвращении этой ошибки база данных не прикрепляется.</span><span class="sxs-lookup"><span data-stu-id="12caa-143">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="12caa-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="12caa-145">Может возвращаться, если был запрошен монопольный доступ, но его не удалось предоставить, или если другой сеанс уже открыл базу данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="12caa-145">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-146">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="12caa-146">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="12caa-147">Возвращается, если <em>кпгдатабасесиземакс</em> больше максимального числа страниц, разрешенного в базе данных.</span><span class="sxs-lookup"><span data-stu-id="12caa-147">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="12caa-148">Текущее максимальное значение — 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="12caa-148">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-149">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="12caa-149">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="12caa-150">В <em>сзфиленаме</em>указан недопустимый путь.</span><span class="sxs-lookup"><span data-stu-id="12caa-150">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="12caa-151"><em>сзфиленаме</em> должен иметь значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="12caa-151"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="12caa-152">По умолчанию <em>сзфиленаме</em> должен указывать на существующий каталог.</span><span class="sxs-lookup"><span data-stu-id="12caa-152">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="12caa-153">Путь будет создан, если задан параметр <em>JET_paramCreatePathIfNotExist</em> (см. <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a>).</span><span class="sxs-lookup"><span data-stu-id="12caa-153">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-154">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="12caa-154">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="12caa-155">Указывает, что другой сеанс уже открыл базу данных в монопольном режиме (с помощью JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="12caa-155">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-156">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="12caa-156">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="12caa-157">База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a>).</span><span class="sxs-lookup"><span data-stu-id="12caa-157">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-158">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="12caa-158">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="12caa-159">Файл базы данных уже присоединен к другому сеансу.</span><span class="sxs-lookup"><span data-stu-id="12caa-159">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-160">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="12caa-160">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="12caa-161">Предпринята попытка создать базу данных во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="12caa-161">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-162">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="12caa-162">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="12caa-163">Предпринята попытка открыть файл, который не является допустимым файлом базы данных.</span><span class="sxs-lookup"><span data-stu-id="12caa-163">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-164">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="12caa-164">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="12caa-165">Была предпринята попытка открыть несколько баз данных, а JET_paramOneDatabasePerSession были заданы.</span><span class="sxs-lookup"><span data-stu-id="12caa-165">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="12caa-166">См. раздел <a href="gg269337(v=exchg.10).md">Параметры базы данных</a>.</span><span class="sxs-lookup"><span data-stu-id="12caa-166">See <a href="gg269337(v=exchg.10).md">Database Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-167">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="12caa-167">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="12caa-168">Не удалось выполнить операцию, так как не удалось выделить память.</span><span class="sxs-lookup"><span data-stu-id="12caa-168">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-169">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="12caa-169">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="12caa-170">В каждом экземпляре может быть присоединено только конечное количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="12caa-170">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="12caa-171">Сейчас ограничение составляет семь баз данных на экземпляр.</span><span class="sxs-lookup"><span data-stu-id="12caa-171">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-172">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="12caa-172">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="12caa-173">Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</span><span class="sxs-lookup"><span data-stu-id="12caa-173">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-174">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="12caa-174">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="12caa-175">JET_wrnFileOpenReadOnly указывает, что файл был присоединен только для чтения, но <strong>жеткреатедатабасе</strong> не прошел JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="12caa-175">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <strong>JetCreateDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="12caa-176">База данных по-прежнему открыта с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="12caa-176">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="12caa-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12caa-177">Remarks</span></span>

<span data-ttu-id="12caa-178">Если база данных, указанная в *сзфиленаме* , существует и JET_bitDbOverwriteExisting не была передана, вызов API завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="12caa-178">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="12caa-179">Если JET_bitDbOverwriteExisting был передан, старый файл базы данных будет удален первым.</span><span class="sxs-lookup"><span data-stu-id="12caa-179">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="12caa-180">Если API создает файл базы данных, а затем вызывает другую ошибку, он очищает и удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="12caa-180">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="12caa-181">**Жеткреатедатабасе** будет неявно открывать базу данных.</span><span class="sxs-lookup"><span data-stu-id="12caa-181">**JetCreateDatabase** will implicitly open the database.</span></span> <span data-ttu-id="12caa-182">В дальнейшем не обязательно вызывать [жетопендатабасе](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="12caa-182">It is not necessarily to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="12caa-183">Требования</span><span class="sxs-lookup"><span data-stu-id="12caa-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12caa-184"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="12caa-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="12caa-185">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="12caa-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="12caa-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="12caa-187">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="12caa-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="12caa-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="12caa-189">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="12caa-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-190"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="12caa-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="12caa-191">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="12caa-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12caa-192"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="12caa-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="12caa-193">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="12caa-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12caa-194"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="12caa-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="12caa-195">Реализуется как <strong>жеткреатедатабасев</strong> (Юникод) и <strong>жеткреатедатабасеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="12caa-195">Implemented as <strong>JetCreateDatabaseW</strong> (Unicode) and <strong>JetCreateDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="12caa-196">См. также:</span><span class="sxs-lookup"><span data-stu-id="12caa-196">See Also</span></span>

[<span data-ttu-id="12caa-197">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="12caa-197">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="12caa-198">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="12caa-198">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="12caa-199">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="12caa-199">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="12caa-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="12caa-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="12caa-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="12caa-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="12caa-202">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="12caa-202">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="12caa-203">жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="12caa-203">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="12caa-204">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="12caa-204">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="12caa-205">жетопендатабасе</span><span class="sxs-lookup"><span data-stu-id="12caa-205">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="12caa-206">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="12caa-206">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="12caa-207">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="12caa-207">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
