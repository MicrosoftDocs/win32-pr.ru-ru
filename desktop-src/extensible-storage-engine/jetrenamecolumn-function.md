---
description: Дополнительные сведения о функции Жетренамеколумн
title: Функция Жетренамеколумн
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702926"
---
# <a name="jetrenamecolumn-function"></a><span data-ttu-id="fe0af-103">Функция Жетренамеколумн</span><span class="sxs-lookup"><span data-stu-id="fe0af-103">JetRenameColumn Function</span></span>


<span data-ttu-id="fe0af-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fe0af-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenamecolumn-function"></a><span data-ttu-id="fe0af-105">Функция Жетренамеколумн</span><span class="sxs-lookup"><span data-stu-id="fe0af-105">JetRenameColumn Function</span></span>

<span data-ttu-id="fe0af-106">Функцию **жетренамеколумн** можно использовать для изменения имени существующего столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="fe0af-106">The **JetRenameColumn** function can be used to change the name of an existing column on a table.</span></span>

<span data-ttu-id="fe0af-107">**Windows XP:**  **Жетренамеколумн** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe0af-107">**Windows XP:**  **JetRenameColumn** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="fe0af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe0af-108">Parameters</span></span>

<span data-ttu-id="fe0af-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="fe0af-109">*sesid*</span></span>

<span data-ttu-id="fe0af-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="fe0af-110">The session to use for this call.</span></span>

<span data-ttu-id="fe0af-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="fe0af-111">*tableid*</span></span>

<span data-ttu-id="fe0af-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="fe0af-112">The cursor to use for this call.</span></span>

<span data-ttu-id="fe0af-113">*szName*</span><span class="sxs-lookup"><span data-stu-id="fe0af-113">*szName*</span></span>

<span data-ttu-id="fe0af-114">Текущее имя столбца, который будет переименован.</span><span class="sxs-lookup"><span data-stu-id="fe0af-114">The current name of the column that will be renamed.</span></span>

<span data-ttu-id="fe0af-115">*сзнаменев*</span><span class="sxs-lookup"><span data-stu-id="fe0af-115">*szNameNew*</span></span>

<span data-ttu-id="fe0af-116">Новое имя для столбца, который будет переименован.</span><span class="sxs-lookup"><span data-stu-id="fe0af-116">The new name for the column that will be renamed.</span></span>

<span data-ttu-id="fe0af-117">*грбит*</span><span class="sxs-lookup"><span data-stu-id="fe0af-117">*grbit*</span></span>

<span data-ttu-id="fe0af-118">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="fe0af-118">This parameter must be 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="fe0af-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe0af-119">Return Value</span></span>

<span data-ttu-id="fe0af-120">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="fe0af-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fe0af-121">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fe0af-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe0af-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fe0af-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="fe0af-123">Описание</span><span class="sxs-lookup"><span data-stu-id="fe0af-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fe0af-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fe0af-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fe0af-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fe0af-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fe0af-127">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="fe0af-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-128">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="fe0af-128">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="fe0af-129">Указанный столбец не существует для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="fe0af-129">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-130">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="fe0af-130">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="fe0af-131">Одно из указанных имен объектов недопустимо.</span><span class="sxs-lookup"><span data-stu-id="fe0af-131">One of the specified object names was invalid.</span></span> <span data-ttu-id="fe0af-132">Все имена объектов должны соответствовать одному и тому же набору правил.</span><span class="sxs-lookup"><span data-stu-id="fe0af-132">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="fe0af-133">Ниже приведены эти правила.</span><span class="sxs-lookup"><span data-stu-id="fe0af-133">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="fe0af-134">Имена объектов должны состоять из символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="fe0af-134">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="fe0af-135">Имена объектов должны иметь длину по крайней мере один символ.</span><span class="sxs-lookup"><span data-stu-id="fe0af-135">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="fe0af-136">Длина имен объектов не может превышать JET_cbNameMost (64) символов.</span><span class="sxs-lookup"><span data-stu-id="fe0af-136">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="fe0af-137">Имена объектов не могут начинаться с имен объектов пробела, не могут содержать управляющие символы ASCII (0x00 – 0x1F).</span><span class="sxs-lookup"><span data-stu-id="fe0af-137">Object names may not begin with a space - object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="fe0af-138">Имена объектов не могут содержать восклицательный знак (!), точку (.), открывающую квадратную скобку ([) или правую квадратную скобку (]).</span><span class="sxs-lookup"><span data-stu-id="fe0af-138">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="fe0af-139">После проверки для имени объекта будет использоваться только часть строки вплоть до первого пробела (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="fe0af-139">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="fe0af-140">Это фактически означает, что имена объектов не могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="fe0af-140">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fe0af-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fe0af-142">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="fe0af-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="fe0af-143">Это может произойти для <strong>жетренамеколумн</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="fe0af-143">This can happen for <strong>JetRenameColumn</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="fe0af-144"><em>szName</em> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="fe0af-144"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="fe0af-145"><em>сзнаменев</em> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="fe0af-145"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fe0af-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fe0af-147">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="fe0af-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="fe0af-148">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="fe0af-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-149">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="fe0af-149">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="fe0af-150">Эта операция может быть выполнена только в том случае, если сеанс не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="fe0af-150">This operation may only be performed when the session is not currently inside a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fe0af-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fe0af-152">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="fe0af-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fe0af-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fe0af-154">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="fe0af-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-155">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="fe0af-155">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="fe0af-156">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="fe0af-156">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="fe0af-157">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="fe0af-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fe0af-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fe0af-159">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="fe0af-159">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-160">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe0af-160">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="fe0af-161">Обновление невозможно выполнить в рамках транзакции, доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fe0af-161">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="fe0af-162">Транзакция только для чтения — это транзакция, которая была запущена с помощью вызова <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> с JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="fe0af-162">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="fe0af-163">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="fe0af-163">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe0af-164">При успешном выполнении имя указанного столбца в таблице, связанной с курсором, будет безвозвратно изменено на новое имя.</span><span class="sxs-lookup"><span data-stu-id="fe0af-164">On success, the name of the specified column in the table associated with the cursor is permanently changed to the new name.</span></span> <span data-ttu-id="fe0af-165">Все индексы, ссылающиеся на этот столбец, также будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="fe0af-165">Any indexes that reference that column will also be updated.</span></span>

<span data-ttu-id="fe0af-166">В случае сбоя не произойдет никаких изменений в состоянии базы данных.</span><span class="sxs-lookup"><span data-stu-id="fe0af-166">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fe0af-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe0af-167">Remarks</span></span>

<span data-ttu-id="fe0af-168">Операция переименования столбца нетипична, поскольку, в отличие от других операций с схемами, она не выполняется как транзакция.</span><span class="sxs-lookup"><span data-stu-id="fe0af-168">The column rename operation is unusual because, unlike other schema operations, it is not carried out as a transaction.</span></span> <span data-ttu-id="fe0af-169">Когда столбец в заданной таблице переименовывается в одном сеансе, любой другой сеанс, использующий эту таблицу, сразу же увидит изменение, даже если они находятся в транзакции, препятствующей тому, что сеанс не сможет увидеть другие изменения, внесенные сеансом, выполняющим операцию переименования.</span><span class="sxs-lookup"><span data-stu-id="fe0af-169">When a column in a given table is renamed in one session then any other session using that table will see the change immediately, even if they are in a transaction that would prevent that session from seeing any other change made by the session doing the rename operation.</span></span>

<span data-ttu-id="fe0af-170">Операция переименования не затрагивает идентификатор столбца столбца.</span><span class="sxs-lookup"><span data-stu-id="fe0af-170">The column ID of a column is not affected by the rename operation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fe0af-171">Требования</span><span class="sxs-lookup"><span data-stu-id="fe0af-171">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-172"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="fe0af-172"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fe0af-173">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe0af-173">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-174"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fe0af-174"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fe0af-175">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fe0af-175">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-176"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fe0af-176"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fe0af-177">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fe0af-177">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-178"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="fe0af-178"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fe0af-179">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fe0af-179">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0af-180"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="fe0af-180"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fe0af-181">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fe0af-181">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0af-182"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="fe0af-182"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fe0af-183">Реализуется как <strong>жетренамеколумнв</strong> (Юникод) и <strong>жетренамеколумна</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fe0af-183">Implemented as <strong>JetRenameColumnW</strong> (Unicode) and <strong>JetRenameColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fe0af-184">См. также:</span><span class="sxs-lookup"><span data-stu-id="fe0af-184">See Also</span></span>

[<span data-ttu-id="fe0af-185">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fe0af-185">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fe0af-186">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fe0af-186">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fe0af-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fe0af-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fe0af-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fe0af-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fe0af-189">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="fe0af-189">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
