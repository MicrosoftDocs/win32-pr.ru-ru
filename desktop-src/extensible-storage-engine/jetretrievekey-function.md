---
description: Дополнительные сведения о функции Жетретриевекэй
title: Функция JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081471"
---
# <a name="jetretrievekey-function"></a><span data-ttu-id="90a68-103">Функция JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="90a68-103">JetRetrieveKey Function</span></span>


<span data-ttu-id="90a68-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="90a68-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievekey-function"></a><span data-ttu-id="90a68-105">Функция JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="90a68-105">JetRetrieveKey Function</span></span>

<span data-ttu-id="90a68-106">Функция **жетретриевекэй** извлекает ключ для записи индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="90a68-106">The **JetRetrieveKey** function retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="90a68-107">Такие ключи создаются с помощью вызовов [жетмакекэй](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="90a68-107">Such keys are constructed by calls to [JetMakeKey](./jetmakekey-function.md).</span></span> <span data-ttu-id="90a68-108">Полученный ключ можно использовать для эффективного возврата курсора к той же записи индекса с помощью вызова [жетсик](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="90a68-108">The retrieved key can then be used to efficiently return that cursor to the same index entry by a call to [JetSeek](./jetseek-function.md).</span></span>

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="90a68-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90a68-109">Parameters</span></span>

<span data-ttu-id="90a68-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="90a68-110">*sesid*</span></span>

<span data-ttu-id="90a68-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="90a68-111">The session to use for this call.</span></span>

<span data-ttu-id="90a68-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="90a68-112">*tableid*</span></span>

<span data-ttu-id="90a68-113">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="90a68-113">The cursor to use for this call.</span></span>

<span data-ttu-id="90a68-114">*пвдата*</span><span class="sxs-lookup"><span data-stu-id="90a68-114">*pvData*</span></span>

<span data-ttu-id="90a68-115">Выходной буфер, который получит ключ.</span><span class="sxs-lookup"><span data-stu-id="90a68-115">The output buffer that will receive the key.</span></span>

<span data-ttu-id="90a68-116">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="90a68-116">*cbMax*</span></span>

<span data-ttu-id="90a68-117">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="90a68-117">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="90a68-118">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="90a68-118">*pcbActual*</span></span>

<span data-ttu-id="90a68-119">Получает фактический размер ключа в байтах.</span><span class="sxs-lookup"><span data-stu-id="90a68-119">Receives the actual size in bytes of the key.</span></span>

<span data-ttu-id="90a68-120">Если этот параметр имеет значение NULL, фактический размер ключа не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="90a68-120">If this parameter is NULL then the actual size of the key will not be returned.</span></span>

<span data-ttu-id="90a68-121">Если выходной буфер слишком мал, то фактический размер ключа все равно будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="90a68-121">If the output buffer is too small, then the actual size of the key will still be returned.</span></span> <span data-ttu-id="90a68-122">Это означает, что это число будет больше, чем размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="90a68-122">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="90a68-123">*грбит*</span><span class="sxs-lookup"><span data-stu-id="90a68-123">*grbit*</span></span>

<span data-ttu-id="90a68-124">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="90a68-124">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90a68-125">Значение</span><span class="sxs-lookup"><span data-stu-id="90a68-125">Value</span></span></p></th>
<th><p><span data-ttu-id="90a68-126">Значение</span><span class="sxs-lookup"><span data-stu-id="90a68-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90a68-127">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="90a68-127">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="90a68-128">Если этот параметр указан, обработчик вернет ключ поиска курсора.</span><span class="sxs-lookup"><span data-stu-id="90a68-128">When specified, the engine will return the search key for the cursor.</span></span> <span data-ttu-id="90a68-129">Ключ поиска создается с использованием одного или нескольких предыдущих вызовов <a href="gg269329(v=exchg.10).md">жетмакекэй</a> для поиска в этом ключе с помощью <a href="gg294103(v=exchg.10).md">жетсик</a> или задания диапазона индекса с помощью <a href="gg294112(v=exchg.10).md">жетсетиндексранже</a>.</span><span class="sxs-lookup"><span data-stu-id="90a68-129">The search key is built up using one or more prior calls to <a href="gg269329(v=exchg.10).md">JetMakeKey</a> for the purposes of seeking to that key using <a href="gg294103(v=exchg.10).md">JetSeek</a> or setting an index range using <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="90a68-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90a68-130">Return Value</span></span>

<span data-ttu-id="90a68-131">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="90a68-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="90a68-132">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="90a68-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90a68-133">Код возврата</span><span class="sxs-lookup"><span data-stu-id="90a68-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="90a68-134">Описание</span><span class="sxs-lookup"><span data-stu-id="90a68-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90a68-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="90a68-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="90a68-136">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="90a68-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a68-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="90a68-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="90a68-138">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="90a68-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a68-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="90a68-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="90a68-140">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="90a68-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="90a68-141">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="90a68-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a68-142">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="90a68-142">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="90a68-143">Для курсора отсутствует текущий ключ поиска.</span><span class="sxs-lookup"><span data-stu-id="90a68-143">There is no current search key for the cursor.</span></span> <span data-ttu-id="90a68-144">Это произойдет для <strong>жетретриевекэй</strong> , если указан параметр JET_bitRetrieveCopy и для этого курсора не был создан ключ поиска, используя перед ним вызов <a href="gg269329(v=exchg.10).md">жетмакекэй</a>.</span><span class="sxs-lookup"><span data-stu-id="90a68-144">This will happen for <strong>JetRetrieveKey</strong> if JET_bitRetrieveCopy is specified and a search key has not been constructed for this cursor using a prior call to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span> <span data-ttu-id="90a68-145">Ключ поиска будет удален при предыдущем вызове любого API навигации в курсоре, отличном от <a href="gg294117(v=exchg.10).md">жетмове</a>.</span><span class="sxs-lookup"><span data-stu-id="90a68-145">The search key will be deleted by a prior call to any navigational API on the cursor other than <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a68-146">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="90a68-146">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="90a68-147">Курсор не располагается на записи.</span><span class="sxs-lookup"><span data-stu-id="90a68-147">The cursor is not positioned on a record.</span></span> <span data-ttu-id="90a68-148">Это может произойти по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="90a68-148">This can happen for many different reasons.</span></span> <span data-ttu-id="90a68-149">Например, это произойдет, если курсор находится в данный момент после последней записи в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="90a68-149">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a68-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="90a68-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="90a68-151">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="90a68-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a68-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="90a68-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="90a68-153">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="90a68-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a68-154">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="90a68-154">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="90a68-155">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="90a68-155">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="90a68-156">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="90a68-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a68-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="90a68-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="90a68-158">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="90a68-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a68-159">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="90a68-159">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="90a68-160">Операция успешно завершена, но выходной буфер слишком мал для получения всего ключа.</span><span class="sxs-lookup"><span data-stu-id="90a68-160">The operation completed successfully, but the output buffer was too small to receive the entire key.</span></span> <span data-ttu-id="90a68-161">Выходной буфер заполнен объемом ключа, который будет соответствовать.</span><span class="sxs-lookup"><span data-stu-id="90a68-161">The output buffer has been filled with as much of the key as would fit.</span></span> <span data-ttu-id="90a68-162">При запросе также возвращается фактический размер ключа.</span><span class="sxs-lookup"><span data-stu-id="90a68-162">The actual size of the key has also been returned, if requested.</span></span></p>
<p><span data-ttu-id="90a68-163"><strong>Примечание</strong>   .   Эта ошибка не будет возвращена, если указано JET_bitRetrieveCopy.</span><span class="sxs-lookup"><span data-stu-id="90a68-163"><strong>Note</strong>   This error will not be returned if JET_bitRetrieveCopy is specified.</span></span> <span data-ttu-id="90a68-164">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="90a68-164">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="90a68-165">При успешном выполнении ключ для записи индекса в текущей позиции курсора будет возвращен в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="90a68-165">On success, the key for the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="90a68-166">Если возвращается значение JET_wrnBufferTruncated, выходной буфер будет содержать столько ключей, сколько будет помещаться в предоставленное пространство, а фактический размер ключа будет неточным.</span><span class="sxs-lookup"><span data-stu-id="90a68-166">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the key as will fit in the space provided and the actual size of the key will be accurate.</span></span> <span data-ttu-id="90a68-167">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90a68-167">No change to the database state will occur.</span></span>

<span data-ttu-id="90a68-168">В случае сбоя состояние выходного буфера и фактический размер ключа будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="90a68-168">On failure, the state of the output buffer and the actual size of the key will be undefined.</span></span> <span data-ttu-id="90a68-169">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90a68-169">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="90a68-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90a68-170">Remarks</span></span>

<span data-ttu-id="90a68-171">Обычно ключи обрабатываются как непрозрачные фрагменты данных.</span><span class="sxs-lookup"><span data-stu-id="90a68-171">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="90a68-172">Для использования внутренней структуры этих данных не нужно предпринимать никаких попыток.</span><span class="sxs-lookup"><span data-stu-id="90a68-172">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="90a68-173">Однако следующие свойства могут быть известны всем ключам ESENT:</span><span class="sxs-lookup"><span data-stu-id="90a68-173">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="90a68-174">Ключи можно сравнить друг с другом с помощью функции [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) , чтобы установить их относительное упорядочение в исходном индексе по таблице записей исходного индекса.</span><span class="sxs-lookup"><span data-stu-id="90a68-174">Keys may be compared against each other using [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) function to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="90a68-175">Нет смысла сравнивать ключи индексов из разных индексов друг с другом.</span><span class="sxs-lookup"><span data-stu-id="90a68-175">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="90a68-176">Длина ключа всегда меньше или равна JET_cbKeyMost (255) байт до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90a68-176">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="90a68-177">В Windows Vista и более поздних выпусках ключи могут быть больше.</span><span class="sxs-lookup"><span data-stu-id="90a68-177">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="90a68-178">Максимальный размер ключа равен текущему значению JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="90a68-178">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

<span data-ttu-id="90a68-179">Помимо указанных выше свойств ключей ESENT в целом, важно отметить, что ключ поиска отличается от ключа для записи индекса.</span><span class="sxs-lookup"><span data-stu-id="90a68-179">In addition to the above properties of ESENT keys in general, it is important to note that a search key is different from the key for an index entry.</span></span> <span data-ttu-id="90a68-180">В частности, ключ поиска может быть длиннее, чем обычный ключ.</span><span class="sxs-lookup"><span data-stu-id="90a68-180">Specifically, a search key may be longer than an ordinary key.</span></span> <span data-ttu-id="90a68-181">Эта лишние длина возникает, когда при построении ключа поиска используется подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="90a68-181">This extra length occurs when a wildcard option is used while constructing the search key.</span></span> <span data-ttu-id="90a68-182">Дополнительные сведения см. в разделе [жетмакекэй](./jetmakekey-function.md) .</span><span class="sxs-lookup"><span data-stu-id="90a68-182">See [JetMakeKey](./jetmakekey-function.md) for more information.</span></span>

<span data-ttu-id="90a68-183">В этом API есть важная ошибка, которая присутствует во всех выпусках.</span><span class="sxs-lookup"><span data-stu-id="90a68-183">There is an important bug in this API that is present in all releases.</span></span> <span data-ttu-id="90a68-184">Если поисковый ключ запрашивается с помощью JET_bitRetrieveCopy и выходной буфер слишком мал для получения всего ключа, то JET_wrnBufferTruncated не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="90a68-184">If the search key is requested using the use of JET_bitRetrieveCopy and the output buffer is too small to receive the entire key then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="90a68-185">Вместо этого будет возвращено JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="90a68-185">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="90a68-186">Важно убедиться, что фактический размер ключа, возвращаемый с помощью *пкбактуал* , меньше или равен размеру выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="90a68-186">It is important to verify that the actual size of the key as returned using *pcbActual* is less than or equal to the size of the output buffer.</span></span> <span data-ttu-id="90a68-187">Если фактический размер превышает размер выходного буфера, вызывающий объект **жетретриевекэй** должен реагировать так, как будто вместо этого возвращались JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="90a68-187">If the actual size is larger than the size of the output buffer, then the caller of **JetRetrieveKey** should react as if JET_wrnBufferTruncated were returned instead.</span></span>

#### <a name="requirements"></a><span data-ttu-id="90a68-188">Требования</span><span class="sxs-lookup"><span data-stu-id="90a68-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90a68-189"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="90a68-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="90a68-190">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="90a68-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a68-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="90a68-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="90a68-192">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="90a68-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a68-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="90a68-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="90a68-194">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="90a68-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a68-195"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="90a68-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="90a68-196">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="90a68-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a68-197"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="90a68-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="90a68-198">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="90a68-198">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="90a68-199">См. также:</span><span class="sxs-lookup"><span data-stu-id="90a68-199">See Also</span></span>

[<span data-ttu-id="90a68-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="90a68-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="90a68-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="90a68-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="90a68-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="90a68-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="90a68-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="90a68-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="90a68-204">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="90a68-204">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="90a68-205">жетсик</span><span class="sxs-lookup"><span data-stu-id="90a68-205">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="90a68-206">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="90a68-206">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
