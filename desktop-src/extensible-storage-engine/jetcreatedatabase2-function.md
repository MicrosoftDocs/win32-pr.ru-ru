---
description: Дополнительные сведения о функции JetCreateDatabase2
title: Функция JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712581"
---
# <a name="jetcreatedatabase2-function"></a><span data-ttu-id="7ef00-103">Функция JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="7ef00-103">JetCreateDatabase2 Function</span></span>


<span data-ttu-id="7ef00-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7ef00-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase2-function"></a><span data-ttu-id="7ef00-105">Функция JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="7ef00-105">JetCreateDatabase2 Function</span></span>

<span data-ttu-id="7ef00-106">Функция **JetCreateDatabase2** создает и прикрепляет файл базы данных для использования с ядром базы данных ESE с заданным максимальным размером базы данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-106">The **JetCreateDatabase2** function creates and attaches a database file to be used with the ESE database engine with a maximum database size specified.</span></span> <span data-ttu-id="7ef00-107">Вызов **JetCreateDatabase2** с *кпгдатабасесиземакс* , установленным в ноль, идентичен вызову [жеткреатедатабасе](./jetcreatedatabase-function.md) с параметром *сзконнект* , имеющим значение null.</span><span class="sxs-lookup"><span data-stu-id="7ef00-107">Calling **JetCreateDatabase2** with *cpgDatabaseSizeMax* set to zero is identical to calling [JetCreateDatabase](./jetcreatedatabase-function.md) with *szConnect* set to NULL.</span></span> <span data-ttu-id="7ef00-108">В настоящее время для каждого экземпляра можно создать до семи баз данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-108">Currently up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7ef00-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ef00-109">Parameters</span></span>

<span data-ttu-id="7ef00-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="7ef00-110">*sesid*</span></span>

<span data-ttu-id="7ef00-111">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="7ef00-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="7ef00-112">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="7ef00-112">*szFilename*</span></span>

<span data-ttu-id="7ef00-113">Имя создаваемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-113">The name of the database to be created.</span></span>

<span data-ttu-id="7ef00-114">*кпгдатабасесиземакс*</span><span class="sxs-lookup"><span data-stu-id="7ef00-114">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="7ef00-115">Максимальный размер базы данных на страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-115">The maximum size, in database pages, for the database.</span></span> <span data-ttu-id="7ef00-116">Размер страницы базы данных по умолчанию составляет 4 килобайта и может быть изменен с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) перед созданием базы данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-116">The default database page size is 4 kilobytes, and can be changed with [JetSetSystemParameter](./jetsetsystemparameter-function.md) prior to creating a database.</span></span>

<span data-ttu-id="7ef00-117">Передача нуля означает отсутствие ограничения, принудительно применяемого ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="7ef00-117">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="7ef00-118">*пдбид*</span><span class="sxs-lookup"><span data-stu-id="7ef00-118">*pdbid*</span></span>

<span data-ttu-id="7ef00-119">Указатель на буфер, который при успешном вызове содержит идентификатор базы данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-119">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="7ef00-120">При сбое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="7ef00-120">On failure, the value is undefined.</span></span>

<span data-ttu-id="7ef00-121">*грбит*</span><span class="sxs-lookup"><span data-stu-id="7ef00-121">*grbit*</span></span>

<span data-ttu-id="7ef00-122">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="7ef00-122">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ef00-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7ef00-123">Value</span></span></p></th>
<th><p><span data-ttu-id="7ef00-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7ef00-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-125">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="7ef00-125">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="7ef00-126">По умолчанию, если вызывается <a href="gg269212(v=exchg.10).md">жеткреатедатабасе</a> или <strong>JetCreateDatabase2</strong> и база данных уже существует, вызов API завершится ошибкой и исходная база данных не будет перезаписана.</span><span class="sxs-lookup"><span data-stu-id="7ef00-126">By default, if <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> or <strong>JetCreateDatabase2</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="7ef00-127">JET_bitDbOverwriteExisting изменяет это поведение, а старая база данных будет перезаписана новой.</span><span class="sxs-lookup"><span data-stu-id="7ef00-127">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="7ef00-128">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="7ef00-128">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-129">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="7ef00-129">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="7ef00-130">JET_bitDbRecoveryOff отключает ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="7ef00-130">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="7ef00-131">Установка этого бита теряет возможность воспроизведения файлов журнала и восстановления базы данных до стабильного работоспособного состояния после аварийного события.</span><span class="sxs-lookup"><span data-stu-id="7ef00-131">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-132">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="7ef00-132">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="7ef00-133">При установке JET_bitDbShadowingOff будет отключено дублирование некоторых внутренних структур баз данных (теневая).</span><span class="sxs-lookup"><span data-stu-id="7ef00-133">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="7ef00-134">Дублирование этих структур выполняется для обеспечения устойчивости, поэтому параметр JET_bitDbShadowingOff удалит эту устойчивость.</span><span class="sxs-lookup"><span data-stu-id="7ef00-134">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7ef00-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ef00-135">Return Value</span></span>

<span data-ttu-id="7ef00-136">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="7ef00-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7ef00-137">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7ef00-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ef00-138">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7ef00-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="7ef00-139">Описание</span><span class="sxs-lookup"><span data-stu-id="7ef00-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7ef00-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7ef00-141">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7ef00-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-142">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="7ef00-142">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="7ef00-143">База данных с именем в <em>сзфиленаме</em> уже существует.</span><span class="sxs-lookup"><span data-stu-id="7ef00-143">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="7ef00-144">При возвращении этой ошибки база данных не прикрепляется.</span><span class="sxs-lookup"><span data-stu-id="7ef00-144">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-145">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="7ef00-145">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="7ef00-146">Может возвращаться, если был запрошен монопольный доступ, но его не удалось предоставить, или если другой сеанс уже открыл базу данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="7ef00-146">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-147">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="7ef00-147">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="7ef00-148">Возвращается, если <em>кпгдатабасесиземакс</em> больше максимального числа страниц, разрешенного в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-148">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="7ef00-149">Текущее максимальное значение — 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="7ef00-149">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-150">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="7ef00-150">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="7ef00-151">В <em>сзфиленаме</em>указан недопустимый путь.</span><span class="sxs-lookup"><span data-stu-id="7ef00-151">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="7ef00-152"><em>сзфиленаме</em> должен иметь значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="7ef00-152"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="7ef00-153">По умолчанию <em>сзфиленаме</em> должен указывать на существующий каталог.</span><span class="sxs-lookup"><span data-stu-id="7ef00-153">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="7ef00-154">Путь будет создан, если задан параметр <em>JET_paramCreatePathIfNotExist</em> (см. <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a>).</span><span class="sxs-lookup"><span data-stu-id="7ef00-154">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-155">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="7ef00-155">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="7ef00-156">Указывает, что другой сеанс уже открыл базу данных в монопольном режиме (с помощью JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="7ef00-156">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-157">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="7ef00-157">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="7ef00-158">База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a>).</span><span class="sxs-lookup"><span data-stu-id="7ef00-158">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-159">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7ef00-159">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7ef00-160">Файл базы данных уже присоединен к другому сеансу.</span><span class="sxs-lookup"><span data-stu-id="7ef00-160">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-161">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="7ef00-161">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="7ef00-162">Предпринята попытка создать базу данных во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="7ef00-162">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-163">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="7ef00-163">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="7ef00-164">Предпринята попытка открыть файл, который не является допустимым файлом базы данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-164">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-165">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="7ef00-165">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="7ef00-166">Была предпринята попытка открыть несколько баз данных, а JET_paramOneDatabasePerSession были заданы.</span><span class="sxs-lookup"><span data-stu-id="7ef00-166">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="7ef00-167">См. раздел <a href="gg294139(v=exchg.10).md">системные параметры</a>.</span><span class="sxs-lookup"><span data-stu-id="7ef00-167">See <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-168">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="7ef00-168">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="7ef00-169">В системе недостаточно ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7ef00-169">The system ran low on resources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-170">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="7ef00-170">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="7ef00-171">В каждом экземпляре может быть присоединено только конечное количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-171">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="7ef00-172">Сейчас ограничение составляет семь баз данных на экземпляр.</span><span class="sxs-lookup"><span data-stu-id="7ef00-172">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-173">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="7ef00-173">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="7ef00-174">Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</span><span class="sxs-lookup"><span data-stu-id="7ef00-174">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-175">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="7ef00-175">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="7ef00-176">JET_wrnFileOpenReadOnly указывает, что файл был присоединен только для чтения, но <a href="gg269212(v=exchg.10).md">жеткреатедатабасе</a> не прошел JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="7ef00-176">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="7ef00-177">База данных по-прежнему открыта с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7ef00-177">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="7ef00-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ef00-178">Remarks</span></span>

<span data-ttu-id="7ef00-179">Если база данных, указанная в *сзфиленаме* , существует и JET_bitDbOverwriteExisting не была передана, вызов API завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7ef00-179">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="7ef00-180">Если JET_bitDbOverwriteExisting был передан, старый файл базы данных будет удален первым.</span><span class="sxs-lookup"><span data-stu-id="7ef00-180">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="7ef00-181">Если API создает файл базы данных, а затем вызывает другую ошибку, он очищает и удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="7ef00-181">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="7ef00-182">**JetCreateDatabase2** будет неявно открывать базу данных.</span><span class="sxs-lookup"><span data-stu-id="7ef00-182">**JetCreateDatabase2** will implicitly open the database.</span></span> <span data-ttu-id="7ef00-183">В дальнейшем вызов [жетопендатабасе](./jetopendatabase-function.md)не требуется.</span><span class="sxs-lookup"><span data-stu-id="7ef00-183">It is not necessary to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="7ef00-184">Требования</span><span class="sxs-lookup"><span data-stu-id="7ef00-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-185"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="7ef00-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7ef00-186">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7ef00-186">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-187"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7ef00-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7ef00-188">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7ef00-188">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-189"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7ef00-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7ef00-190">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7ef00-190">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-191"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="7ef00-191"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7ef00-192">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7ef00-192">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ef00-193"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="7ef00-193"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7ef00-194">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7ef00-194">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ef00-195"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="7ef00-195"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7ef00-196">Реализуется как <strong>JetCreateDatabase2W</strong> (Юникод) и <strong>JetCreateDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7ef00-196">Implemented as <strong>JetCreateDatabase2W</strong> (Unicode) and <strong>JetCreateDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7ef00-197">См. также:</span><span class="sxs-lookup"><span data-stu-id="7ef00-197">See Also</span></span>

[<span data-ttu-id="7ef00-198">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="7ef00-198">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="7ef00-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7ef00-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7ef00-200">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="7ef00-200">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="7ef00-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7ef00-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7ef00-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7ef00-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7ef00-203">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="7ef00-203">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="7ef00-204">жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="7ef00-204">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="7ef00-205">жеткреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="7ef00-205">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="7ef00-206">жетопендатабасе</span><span class="sxs-lookup"><span data-stu-id="7ef00-206">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="7ef00-207">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="7ef00-207">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="7ef00-208">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="7ef00-208">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
