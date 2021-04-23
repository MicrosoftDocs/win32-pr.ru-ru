---
description: Дополнительные сведения о функции Жеткомпутестатс
title: Функция Жеткомпутестатс
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272854"
---
# <a name="jetcomputestats-function"></a><span data-ttu-id="87c81-103">Функция Жеткомпутестатс</span><span class="sxs-lookup"><span data-stu-id="87c81-103">JetComputeStats Function</span></span>


<span data-ttu-id="87c81-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="87c81-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcomputestats-function"></a><span data-ttu-id="87c81-105">Функция Жеткомпутестатс</span><span class="sxs-lookup"><span data-stu-id="87c81-105">JetComputeStats Function</span></span>

<span data-ttu-id="87c81-106">Функция **жеткомпутестатс** просматривает каждый индекс таблицы, чтобы точно вычислить количество записей в индексе и количество различных ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="87c81-106">The **JetComputeStats** function walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="87c81-107">Эти сведения вместе с количеством страниц базы данных, выделенных для индекса, и текущим временем вычислений хранятся в метаданных индекса в базе данных.</span><span class="sxs-lookup"><span data-stu-id="87c81-107">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="87c81-108">Эти данные можно впоследствии извлечь с помощью информационных операций.</span><span class="sxs-lookup"><span data-stu-id="87c81-108">This data can be subsequently retrieved with information operations.</span></span>

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="87c81-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="87c81-109">Parameters</span></span>

<span data-ttu-id="87c81-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="87c81-110">*sesid*</span></span>

<span data-ttu-id="87c81-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="87c81-111">The session to use for this call.</span></span>

<span data-ttu-id="87c81-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="87c81-112">*tableid*</span></span>

<span data-ttu-id="87c81-113">Курсор, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="87c81-113">The cursor that will be used for this call.</span></span> <span data-ttu-id="87c81-114">Описывает таблицу для расчета статистики.</span><span class="sxs-lookup"><span data-stu-id="87c81-114">Describes the table to compute statistics on.</span></span>

### <a name="return-value"></a><span data-ttu-id="87c81-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87c81-115">Return Value</span></span>

<span data-ttu-id="87c81-116">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="87c81-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="87c81-117">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="87c81-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87c81-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="87c81-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="87c81-119">Описание</span><span class="sxs-lookup"><span data-stu-id="87c81-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87c81-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="87c81-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="87c81-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="87c81-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87c81-122">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="87c81-122">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="87c81-123">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="87c81-123">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87c81-124">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="87c81-124">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="87c81-125">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="87c81-125">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="87c81-126">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="87c81-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87c81-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="87c81-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="87c81-128">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="87c81-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87c81-129">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="87c81-129">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="87c81-130">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="87c81-130">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87c81-131">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="87c81-131">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="87c81-132">При выполнении этой операции откат всех изменений произошла ошибка, но произошел сбой отката транзакции.</span><span class="sxs-lookup"><span data-stu-id="87c81-132">An error occurred requiring this operation to rollback all changes, but the transaction rollback itself failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87c81-133">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="87c81-133">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="87c81-134">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="87c81-134">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="87c81-135">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="87c81-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87c81-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="87c81-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="87c81-137">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="87c81-137">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87c81-138">При успешном выполнении статистика сохраняется в каталогах базы данных для таблицы, описанной в данном курсоре.</span><span class="sxs-lookup"><span data-stu-id="87c81-138">On success, up-to-date statistics are stored in the database catalogs for the table described with the given cursor.</span></span>

<span data-ttu-id="87c81-139">В случае сбоя никакие изменения не вносятся в базу данных.</span><span class="sxs-lookup"><span data-stu-id="87c81-139">On failure, no updates of any kind are made to the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="87c81-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87c81-140">Remarks</span></span>

<span data-ttu-id="87c81-141">Эта операция может быть расходом ресурсов, так как каждый индекс в таблице должен быть полностью изменяться.</span><span class="sxs-lookup"><span data-stu-id="87c81-141">This operation can be resource consuming since each index in a table must be walked in its entirety.</span></span> <span data-ttu-id="87c81-142">[Жетжетрекордпоситион](./jetgetrecordposition-function.md) можно использовать для грубой оценки количества записей в индексе, но сам по себе не может оценить количество уникальных значений в индексе.</span><span class="sxs-lookup"><span data-stu-id="87c81-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) can be used to get a rough estimate of the number of entries in an index, but it cannot by itself estimate the number of distinct values in an index.</span></span>

<span data-ttu-id="87c81-143">Данные, вычисленные этой операцией, начинают устареть, а таблица впоследствии обновляется.</span><span class="sxs-lookup"><span data-stu-id="87c81-143">The data computed by this operation begins to become out of date and the table is subsequently updated.</span></span>

<span data-ttu-id="87c81-144">Обновления базы данных, внесенные **жеткомпутестатс** , выполняются отложенно.</span><span class="sxs-lookup"><span data-stu-id="87c81-144">Updates to the database made by **JetComputeStats** are made in a lazy fashion.</span></span> <span data-ttu-id="87c81-145">Это означает, что эта операция не приведет к сбросу журнала, а после возврата JET_errSuccess **жеткомпутестатс** по-прежнему может привести к потере этих обновлений.</span><span class="sxs-lookup"><span data-stu-id="87c81-145">This means that no log flush will be accompanied by this operation and a system crash subsequent to a return of JET_errSuccess by **JetComputeStats** can still cause these updates to be lost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="87c81-146">Требования</span><span class="sxs-lookup"><span data-stu-id="87c81-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87c81-147"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="87c81-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="87c81-148">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="87c81-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87c81-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="87c81-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="87c81-150">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="87c81-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87c81-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="87c81-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="87c81-152">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="87c81-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87c81-153"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="87c81-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="87c81-154">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="87c81-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87c81-155"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="87c81-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="87c81-156">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="87c81-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="87c81-157">См. также:</span><span class="sxs-lookup"><span data-stu-id="87c81-157">See Also</span></span>

[<span data-ttu-id="87c81-158">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="87c81-158">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="87c81-159">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="87c81-159">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="87c81-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="87c81-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="87c81-161">жетжетрекордпоситион</span><span class="sxs-lookup"><span data-stu-id="87c81-161">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="87c81-162">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="87c81-162">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="87c81-163">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="87c81-163">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="87c81-164">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="87c81-164">JetStopService</span></span>](./jetstopservice-function.md)
