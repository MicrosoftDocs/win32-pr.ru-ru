---
description: Дополнительные сведения о функции Жетопендатабасе
title: Функция JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819073"
---
# <a name="jetopendatabase-function"></a><span data-ttu-id="de3d9-103">Функция JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="de3d9-103">JetOpenDatabase Function</span></span>


<span data-ttu-id="de3d9-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="de3d9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopendatabase-function"></a><span data-ttu-id="de3d9-105">Функция JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="de3d9-105">JetOpenDatabase Function</span></span>

<span data-ttu-id="de3d9-106">Функция **жетопендатабасе** открывает ранее присоединенную базу данных с помощью функций [жетаттачдатабасе](./jetattachdatabase-function.md) или [JetAttachDatabase2](./jetattachdatabase2-function.md) для использования с сеансом базы данных.</span><span class="sxs-lookup"><span data-stu-id="de3d9-106">The **JetOpenDatabase** function opens a previously attached database, using the [JetAttachDatabase](./jetattachdatabase-function.md) or [JetAttachDatabase2](./jetattachdatabase2-function.md) functions, for use with a database session.</span></span> <span data-ttu-id="de3d9-107">Эту функцию можно вызывать несколько раз для одной и той же базы данных.</span><span class="sxs-lookup"><span data-stu-id="de3d9-107">This function can be called multiple times for the same database.</span></span>

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="de3d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="de3d9-108">Parameters</span></span>

<span data-ttu-id="de3d9-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="de3d9-109">*sesid*</span></span>

<span data-ttu-id="de3d9-110">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="de3d9-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="de3d9-111">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="de3d9-111">*szFilename*</span></span>

<span data-ttu-id="de3d9-112">Имя открываемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="de3d9-112">The name of the database to open.</span></span>

<span data-ttu-id="de3d9-113">*сзконнект*</span><span class="sxs-lookup"><span data-stu-id="de3d9-113">*szConnect*</span></span>

<span data-ttu-id="de3d9-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="de3d9-114">Reserved.</span></span> <span data-ttu-id="de3d9-115">задано значение NULL.</span><span class="sxs-lookup"><span data-stu-id="de3d9-115">Set to NULL.</span></span>

<span data-ttu-id="de3d9-116">*пдбид*</span><span class="sxs-lookup"><span data-stu-id="de3d9-116">*pdbid*</span></span>

<span data-ttu-id="de3d9-117">Указатель на буфер, который при успешном вызове содержит идентификатор базы данных.</span><span class="sxs-lookup"><span data-stu-id="de3d9-117">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="de3d9-118">Если вызов завершается неудачно, значение не определено.</span><span class="sxs-lookup"><span data-stu-id="de3d9-118">If the call fails, the value is undefined.</span></span>

<span data-ttu-id="de3d9-119">*грбит*</span><span class="sxs-lookup"><span data-stu-id="de3d9-119">*grbit*</span></span>

<span data-ttu-id="de3d9-120">Группа битов, задающих ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="de3d9-120">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de3d9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="de3d9-121">Value</span></span></p></th>
<th><p><span data-ttu-id="de3d9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="de3d9-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de3d9-123">JET_bitDbExclusive</span><span class="sxs-lookup"><span data-stu-id="de3d9-123">JET_bitDbExclusive</span></span></p></td>
<td><p><span data-ttu-id="de3d9-124">Разрешает присоединение базы данных только одному сеансу.</span><span class="sxs-lookup"><span data-stu-id="de3d9-124">Allows only a single session to attach a database.</span></span> <span data-ttu-id="de3d9-125">Как правило, база данных может быть открыта несколькими сеансами.</span><span class="sxs-lookup"><span data-stu-id="de3d9-125">Normally, several sessions can open a database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3d9-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="de3d9-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="de3d9-127">Предотвращает изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="de3d9-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="de3d9-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de3d9-128">Return Value</span></span>

<span data-ttu-id="de3d9-129">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="de3d9-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="de3d9-130">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="de3d9-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de3d9-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="de3d9-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="de3d9-132">Описание</span><span class="sxs-lookup"><span data-stu-id="de3d9-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de3d9-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="de3d9-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="de3d9-134">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="de3d9-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3d9-135">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="de3d9-135">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="de3d9-136">Был запрошен монопольный доступ, но его не удалось предоставить.</span><span class="sxs-lookup"><span data-stu-id="de3d9-136">Exclusive access was requested, but could not be granted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3d9-137">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="de3d9-137">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="de3d9-138">В <em>сзфиленаме</em>указан недопустимый путь.</span><span class="sxs-lookup"><span data-stu-id="de3d9-138">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="de3d9-139"><em>сзфиленаме</em> не должно иметь значение NULL и ссылаться на допустимый файл.</span><span class="sxs-lookup"><span data-stu-id="de3d9-139"><em>szFilename</em> must be non-NULL and refer to a valid file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3d9-140">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="de3d9-140">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="de3d9-141">Другой сеанс уже открыл базу данных в монопольном режиме (с помощью JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="de3d9-141">Another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3d9-142">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="de3d9-142">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="de3d9-143">База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a>).</span><span class="sxs-lookup"><span data-stu-id="de3d9-143">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3d9-144">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="de3d9-144">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="de3d9-145">Предпринята попытка открыть файл, который не является допустимым файлом базы данных.</span><span class="sxs-lookup"><span data-stu-id="de3d9-145">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3d9-146">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="de3d9-146">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="de3d9-147">Была предпринята попытка открыть несколько баз данных, а <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> были заданы.</span><span class="sxs-lookup"><span data-stu-id="de3d9-147">An attempt was made to open more than one database, and <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> was set.</span></span> <span data-ttu-id="de3d9-148">Дополнительные сведения см. в разделе <a href="gg294139(v=exchg.10).md">системные параметры</a>.</span><span class="sxs-lookup"><span data-stu-id="de3d9-148">For more information, see <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3d9-149">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="de3d9-149">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="de3d9-150">Файл был присоединен только для чтения, но <strong>жетопендатабасе</strong> не прошел JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="de3d9-150">The file was attached as read-only, but <strong>JetOpenDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="de3d9-151">База данных по-прежнему открыта с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="de3d9-151">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="de3d9-152">Требования</span><span class="sxs-lookup"><span data-stu-id="de3d9-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de3d9-153"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="de3d9-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="de3d9-154">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="de3d9-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3d9-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="de3d9-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="de3d9-156">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="de3d9-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3d9-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="de3d9-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="de3d9-158">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="de3d9-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3d9-159"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="de3d9-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="de3d9-160">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="de3d9-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3d9-161"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="de3d9-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="de3d9-162">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="de3d9-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3d9-163"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="de3d9-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="de3d9-164">Реализуется как <strong>жетопендатабасев</strong> (Юникод) и <strong>жетопендатабасеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="de3d9-164">Implemented as <strong>JetOpenDatabaseW</strong> (Unicode) and <strong>JetOpenDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="de3d9-165">См. также:</span><span class="sxs-lookup"><span data-stu-id="de3d9-165">See Also</span></span>

[<span data-ttu-id="de3d9-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="de3d9-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="de3d9-167">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="de3d9-167">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="de3d9-168">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="de3d9-168">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="de3d9-169">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="de3d9-169">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="de3d9-170">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="de3d9-170">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="de3d9-171">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="de3d9-171">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="de3d9-172">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="de3d9-172">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="de3d9-173">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="de3d9-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
