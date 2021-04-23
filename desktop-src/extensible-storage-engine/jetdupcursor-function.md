---
description: Дополнительные сведения о функции Жетдупкурсор
title: Функция JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712727"
---
# <a name="jetdupcursor-function"></a><span data-ttu-id="84140-103">Функция JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="84140-103">JetDupCursor Function</span></span>


<span data-ttu-id="84140-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="84140-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupcursor-function"></a><span data-ttu-id="84140-105">Функция JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="84140-105">JetDupCursor Function</span></span>

<span data-ttu-id="84140-106">Функция **жетдупкурсор** дублирует открытый курсор и возвращает указатель на дублирующийся курсор.</span><span class="sxs-lookup"><span data-stu-id="84140-106">The **JetDupCursor** function duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="84140-107">Если курсор, который был продублирован, был курсором только для чтения, то дубликат курсора также является курсором только для чтения.</span><span class="sxs-lookup"><span data-stu-id="84140-107">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="84140-108">Любое состояние, связанное с построением ключа поиска или обновлением записи, не копируется в дублирующийся курсор.</span><span class="sxs-lookup"><span data-stu-id="84140-108">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="84140-109">Кроме того, положение исходного курсора не дублируется в повторяющемся курсоре.</span><span class="sxs-lookup"><span data-stu-id="84140-109">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="84140-110">Дубликат курсора всегда открывается в кластеризованном индексе, и его расположение всегда находится в первой строке таблицы.</span><span class="sxs-lookup"><span data-stu-id="84140-110">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="84140-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="84140-111">Parameters</span></span>

<span data-ttu-id="84140-112">*сесид*</span><span class="sxs-lookup"><span data-stu-id="84140-112">*sesid*</span></span>

<span data-ttu-id="84140-113">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="84140-113">The session to use for this call.</span></span>

<span data-ttu-id="84140-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="84140-114">*tableid*</span></span>

<span data-ttu-id="84140-115">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="84140-115">The cursor to use for this call.</span></span>

<span data-ttu-id="84140-116">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="84140-116">*ptableid*</span></span>

<span data-ttu-id="84140-117">Указатель на *tableid*.</span><span class="sxs-lookup"><span data-stu-id="84140-117">Pointer to *tableid*.</span></span>

<span data-ttu-id="84140-118">*грбит*</span><span class="sxs-lookup"><span data-stu-id="84140-118">*grbit*</span></span>

<span data-ttu-id="84140-119">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="84140-119">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="84140-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84140-120">Return Value</span></span>

<span data-ttu-id="84140-121">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="84140-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="84140-122">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="84140-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84140-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="84140-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="84140-124">Описание</span><span class="sxs-lookup"><span data-stu-id="84140-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84140-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="84140-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="84140-126">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="84140-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84140-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="84140-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="84140-128">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="84140-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84140-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="84140-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="84140-130">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="84140-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="84140-131">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="84140-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84140-132">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="84140-132">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="84140-133">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="84140-133">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84140-134">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="84140-134">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="84140-135">Нет доступных ресурсов курсора.</span><span class="sxs-lookup"><span data-stu-id="84140-135">No available cursor resources exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84140-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="84140-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="84140-137">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="84140-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84140-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="84140-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="84140-139">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="84140-139">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="84140-140">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="84140-140">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84140-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="84140-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="84140-142">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="84140-142">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84140-143">При успешном выполнении *pTableID* задается дубликат курсора.</span><span class="sxs-lookup"><span data-stu-id="84140-143">On success, *ptableid* is set to a duplicated cursor.</span></span>

<span data-ttu-id="84140-144">В случае сбоя изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="84140-144">On failure, no changes are made.</span></span> <span data-ttu-id="84140-145">Состояние *tableid* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="84140-145">The state of *tableid* is unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="84140-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84140-146">Remarks</span></span>

<span data-ttu-id="84140-147">Для повторяющегося курсора не скопировано полное состояние курсора.</span><span class="sxs-lookup"><span data-stu-id="84140-147">The duplicated cursor does not have the entire cursor state copied.</span></span> <span data-ttu-id="84140-148">Расположение повторяющегося курсора, включая текущий индекс, обычно отличается от указанного курсора.</span><span class="sxs-lookup"><span data-stu-id="84140-148">The location of the duplicated cursor, including the current index, is usually different from the given cursor.</span></span> <span data-ttu-id="84140-149">Дубликат курсора всегда возвращается в кластеризованном индексе и в первой строке таблицы.</span><span class="sxs-lookup"><span data-stu-id="84140-149">The duplicated cursor is always returned on the clustered index and on the first row in the table.</span></span> <span data-ttu-id="84140-150">Если таблица пуста, то дублирующийся курсор не находится ни в одной строке.</span><span class="sxs-lookup"><span data-stu-id="84140-150">If the table is empty, the duplicated cursor is not on any row.</span></span>

<span data-ttu-id="84140-151">Таблицы, открытые с помощью **жетдупкурсор** , обычно должны быть закрыты с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="84140-151">Tables opened with **JetDupCursor** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="84140-152">Исключение из этого правила происходит при вызове **жетдупкурсор** в транзакции и откате транзакции (WITH [жетроллбакк](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="84140-152">The exception to this rule happens when **JetDupCursor** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="84140-153">При откате транзакции курсор автоматически закрывается.</span><span class="sxs-lookup"><span data-stu-id="84140-153">When rolling back a transaction, the cursor is automatically closed.</span></span> <span data-ttu-id="84140-154">В этом случае возникает ошибка при закрытии таблицы с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="84140-154">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="84140-155">Количество таблиц, которые могут быть открыты одновременно, повлияет непосредственно на [JET_paramMaxOpenTables](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="84140-155">The number of tables that can be opened simultaneously is affected directly by [JET_paramMaxOpenTables](./resource-parameters.md).</span></span> <span data-ttu-id="84140-156">Дополнительные сведения см. в разделе [системные параметры](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="84140-156">See [System Parameters](./extensible-storage-engine-system-parameters.md) for details.</span></span>

#### <a name="requirements"></a><span data-ttu-id="84140-157">Требования</span><span class="sxs-lookup"><span data-stu-id="84140-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84140-158"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="84140-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="84140-159">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="84140-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84140-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="84140-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="84140-161">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="84140-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84140-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="84140-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="84140-163">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="84140-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84140-164"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="84140-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="84140-165">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="84140-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84140-166"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="84140-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="84140-167">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="84140-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="84140-168">См. также:</span><span class="sxs-lookup"><span data-stu-id="84140-168">See Also</span></span>

[<span data-ttu-id="84140-169">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="84140-169">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="84140-170">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="84140-170">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="84140-171">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="84140-171">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="84140-172">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="84140-172">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="84140-173">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="84140-173">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="84140-174">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="84140-174">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="84140-175">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="84140-175">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
