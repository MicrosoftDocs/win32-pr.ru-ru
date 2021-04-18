---
description: Дополнительные сведения о функции Жетжетлс
title: Функция Жетжетлс
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712869"
---
# <a name="jetgetls-function"></a><span data-ttu-id="c69cf-103">Функция Жетжетлс</span><span class="sxs-lookup"><span data-stu-id="c69cf-103">JetGetLS Function</span></span>


<span data-ttu-id="c69cf-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c69cf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetls-function"></a><span data-ttu-id="c69cf-105">Функция Жетжетлс</span><span class="sxs-lookup"><span data-stu-id="c69cf-105">JetGetLS Function</span></span>

<span data-ttu-id="c69cf-106">Функция **жетжетлс** позволяет приложению получить описатель контекста, известный как локальное хранилище, связанное с курсором, или с таблицей, связанной с этим курсором.</span><span class="sxs-lookup"><span data-stu-id="c69cf-106">The **JetGetLS** function enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="c69cf-107">Этот обработчик контекста должен быть ранее задан с помощью [жетсетлс](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="c69cf-107">This context handle must have been previously set using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="c69cf-108">**Жетжетлс** также можно использовать для одновременной выборки текущего контекста для курсора или таблицы и сброса дескриптора контекста.</span><span class="sxs-lookup"><span data-stu-id="c69cf-108">**JetGetLS** can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="c69cf-109">**Windows XP: жетжетлс** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c69cf-109">**Windows XP:  JetGetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c69cf-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c69cf-110">Parameters</span></span>

<span data-ttu-id="c69cf-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="c69cf-111">*sesid*</span></span>

<span data-ttu-id="c69cf-112">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c69cf-112">The session to use for this call.</span></span>

<span data-ttu-id="c69cf-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c69cf-113">*tableid*</span></span>

<span data-ttu-id="c69cf-114">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c69cf-114">The cursor to use for this call.</span></span>

<span data-ttu-id="c69cf-115">*pls*</span><span class="sxs-lookup"><span data-stu-id="c69cf-115">*pls*</span></span>

<span data-ttu-id="c69cf-116">Выходной буфер, который получает обработчик контекста, который в текущий момент связан с курсором или таблицей.</span><span class="sxs-lookup"><span data-stu-id="c69cf-116">The output buffer that receives the context handle currently associated with the cursor or table.</span></span>

<span data-ttu-id="c69cf-117">*грбит*</span><span class="sxs-lookup"><span data-stu-id="c69cf-117">*grbit*</span></span>

<span data-ttu-id="c69cf-118">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="c69cf-118">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c69cf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c69cf-119">Value</span></span></p></th>
<th><p><span data-ttu-id="c69cf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c69cf-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-121">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="c69cf-121">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="c69cf-122">Указывает, что должен быть получен обработчик контекста, связанный с заданным курсором.</span><span class="sxs-lookup"><span data-stu-id="c69cf-122">Indicates that the context handle associated with the given cursor should be retrieved.</span></span></p>
<p><span data-ttu-id="c69cf-123">Если не указано ни JET_bitLSCursor, ни JET_bitLSTable, предполагается JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="c69cf-123">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="c69cf-124">Этот параметр нельзя использовать с JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="c69cf-124">This option cannot be used with JET_bitLSTable.</span></span> <span data-ttu-id="c69cf-125">Операция завершится ошибкой с JET_errInvalidgrbit при попытке.</span><span class="sxs-lookup"><span data-stu-id="c69cf-125">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c69cf-126">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="c69cf-126">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="c69cf-127">Указывает, что должен быть получен обработчик контекста, связанный с таблицей, содержащей данный курсор.</span><span class="sxs-lookup"><span data-stu-id="c69cf-127">Indicates that the context handle associated to the table that contains the given cursor should be retrieved.</span></span> <span data-ttu-id="c69cf-128">Использование этого параметра с JET_bitLSCursor недопустимо.</span><span class="sxs-lookup"><span data-stu-id="c69cf-128">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="c69cf-129">Операция завершится ошибкой с JET_errInvalidgrbit при попытке.</span><span class="sxs-lookup"><span data-stu-id="c69cf-129">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-130">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="c69cf-130">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="c69cf-131">Указывает, что обработчик контекста для выбранного объекта должен быть сброшен в JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="c69cf-131">Indicates that the context handle for the chosen object should be reset to JET_LSNil.</span></span> <span data-ttu-id="c69cf-132">Текущее значение маркера контекста возвращается в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="c69cf-132">The current value of the context handle is returned in the output buffer.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c69cf-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c69cf-133">Return Value</span></span>

<span data-ttu-id="c69cf-134">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="c69cf-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c69cf-135">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c69cf-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c69cf-136">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c69cf-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="c69cf-137">Описание</span><span class="sxs-lookup"><span data-stu-id="c69cf-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c69cf-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c69cf-139">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c69cf-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c69cf-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c69cf-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c69cf-141">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="c69cf-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c69cf-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c69cf-143">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="c69cf-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c69cf-144">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c69cf-144">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c69cf-145">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="c69cf-145">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="c69cf-146">Один из запрошенных параметров недопустим, используется недопустимым образом или не реализован.</span><span class="sxs-lookup"><span data-stu-id="c69cf-146">One of the options requested was invalid, used in an illegal manner, or not implemented.</span></span></p>
<p><span data-ttu-id="c69cf-147">Это может произойти для <strong>жетжетлс</strong> , если заданы оба JET_bitLSCursor и JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="c69cf-147">This can happen for <strong>JetGetLS</strong> when both JET_bitLSCursor and JET_bitLSTable are set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-148">JET_errLSNotSet</span><span class="sxs-lookup"><span data-stu-id="c69cf-148">JET_errLSNotSet</span></span></p></td>
<td><p><span data-ttu-id="c69cf-149">Не удалось вернуть контекстный маркер, так как с запрошенным объектом сейчас не связан ни один обработчик контекста.</span><span class="sxs-lookup"><span data-stu-id="c69cf-149">The context handle could not be returned because no context handle is currently associated with the requested object.</span></span></p>
<p><span data-ttu-id="c69cf-150"><strong>Примечание  </strong> . Эта ошибка не возвращается, если указан JET_bitLSReset, но с запрошенным объектом не связан ни один маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="c69cf-150"><strong>Note  </strong> This error is not returned if JET_bitLSReset is specified yet no context handle was associated with the requested object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c69cf-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c69cf-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c69cf-152">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="c69cf-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c69cf-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c69cf-154">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="c69cf-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c69cf-155">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c69cf-155">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c69cf-156">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="c69cf-156">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c69cf-157">При успешном завершении маркер контекста был успешно получен из запрошенного объекта.</span><span class="sxs-lookup"><span data-stu-id="c69cf-157">On success, the context handle was successfully retrieved from the requested object.</span></span> <span data-ttu-id="c69cf-158">Если указан JET_bitLSReset, то этот маркер контекста также был успешно удален из объекта.</span><span class="sxs-lookup"><span data-stu-id="c69cf-158">If JET_bitLSReset was specified then that context handle was also successfully removed from the object.</span></span> <span data-ttu-id="c69cf-159">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c69cf-159">No change to the database state will occur.</span></span>

<span data-ttu-id="c69cf-160">В случае сбоя не произошло изменение состояния запрошенного объекта.</span><span class="sxs-lookup"><span data-stu-id="c69cf-160">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="c69cf-161">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c69cf-161">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c69cf-162">Требования</span><span class="sxs-lookup"><span data-stu-id="c69cf-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-163"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c69cf-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c69cf-164">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c69cf-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c69cf-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c69cf-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c69cf-166">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c69cf-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c69cf-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c69cf-168">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c69cf-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c69cf-169"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="c69cf-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c69cf-170">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c69cf-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c69cf-171"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="c69cf-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c69cf-172">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c69cf-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c69cf-173">См. также:</span><span class="sxs-lookup"><span data-stu-id="c69cf-173">See Also</span></span>

[<span data-ttu-id="c69cf-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c69cf-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c69cf-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c69cf-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c69cf-176">JET_LS</span><span class="sxs-lookup"><span data-stu-id="c69cf-176">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="c69cf-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c69cf-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c69cf-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c69cf-178">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c69cf-179">жетсетлс</span><span class="sxs-lookup"><span data-stu-id="c69cf-179">JetSetLS</span></span>](./jetsetls-function.md)
