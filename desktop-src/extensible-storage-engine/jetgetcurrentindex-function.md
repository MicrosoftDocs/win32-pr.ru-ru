---
description: Дополнительные сведения о функции Жетжеткуррентиндекс
title: Функция Жетжеткуррентиндекс
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712417"
---
# <a name="jetgetcurrentindex-function"></a><span data-ttu-id="25e87-103">Функция Жетжеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="25e87-103">JetGetCurrentIndex Function</span></span>


<span data-ttu-id="25e87-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="25e87-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcurrentindex-function"></a><span data-ttu-id="25e87-105">Функция Жетжеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="25e87-105">JetGetCurrentIndex Function</span></span>

<span data-ttu-id="25e87-106">Функция **жетжеткуррентиндекс** определяет имя текущего индекса данного курсора.</span><span class="sxs-lookup"><span data-stu-id="25e87-106">The **JetGetCurrentIndex** function determines the name of the current index of a given cursor.</span></span> <span data-ttu-id="25e87-107">Это имя также используется для повторного выбора этого индекса в качестве текущего индекса с помощью [жетсеткуррентиндекс](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="25e87-107">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="25e87-108">Его также можно использовать для обнаружения свойств этого индекса с помощью [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="25e87-108">It can also be used to discover the properties of that index using [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="25e87-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="25e87-109">Parameters</span></span>

<span data-ttu-id="25e87-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="25e87-110">*sesid*</span></span>

<span data-ttu-id="25e87-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="25e87-111">The session to use for this call.</span></span>

<span data-ttu-id="25e87-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="25e87-112">*tableid*</span></span>

<span data-ttu-id="25e87-113">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="25e87-113">The cursor to use for this call.</span></span>

<span data-ttu-id="25e87-114">*сзиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="25e87-114">*szIndexName*</span></span>

<span data-ttu-id="25e87-115">Выходной буфер, который получает имя текущего индекса курсора.</span><span class="sxs-lookup"><span data-stu-id="25e87-115">The output buffer that receives the name of the current index of the cursor.</span></span>

<span data-ttu-id="25e87-116">*кчиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="25e87-116">*cchIndexName*</span></span>

<span data-ttu-id="25e87-117">Максимальный размер в символах выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="25e87-117">The maximum size in characters of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="25e87-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25e87-118">Return Value</span></span>

<span data-ttu-id="25e87-119">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="25e87-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="25e87-120">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="25e87-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25e87-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="25e87-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="25e87-122">Описание</span><span class="sxs-lookup"><span data-stu-id="25e87-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25e87-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="25e87-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="25e87-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="25e87-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e87-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="25e87-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="25e87-126">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="25e87-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25e87-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="25e87-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="25e87-128">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="25e87-128">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="25e87-129">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="25e87-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e87-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="25e87-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="25e87-131">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="25e87-131">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25e87-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="25e87-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="25e87-133">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="25e87-133">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e87-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="25e87-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="25e87-135">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="25e87-135">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="25e87-136">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="25e87-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25e87-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="25e87-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="25e87-138">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="25e87-138">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e87-139">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="25e87-139">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="25e87-140">Операция успешно завершена, но выходной буфер слишком мал для получения полного имени индекса.</span><span class="sxs-lookup"><span data-stu-id="25e87-140">The operation completed successfully, but the output buffer was too small to receive the entire index name.</span></span></p>
<p><span data-ttu-id="25e87-141">Выходной буфер заполнен как часть имени индекса, которая будет соответствовать.</span><span class="sxs-lookup"><span data-stu-id="25e87-141">The output buffer has been filled with as much of the index name as would fit.</span></span> <span data-ttu-id="25e87-142">Если выходной буфер имеет длину по крайней мере один символ, то строка в этом выходном буфере будет завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="25e87-142">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="25e87-143"><strong>Примечание  </strong> . Эта ошибка не будет возвращена, если Кчиндекснаме равен нулю.</span><span class="sxs-lookup"><span data-stu-id="25e87-143"><strong>Note  </strong>This error will not be returned if cchIndexName is zero.</span></span> <span data-ttu-id="25e87-144">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="25e87-144">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25e87-145">В случае успешного выполнения в выходном буфере будет возвращено имя текущего индекса данного курсора.</span><span class="sxs-lookup"><span data-stu-id="25e87-145">On success, the name of the current index of the given cursor will be returned in the output buffer.</span></span> <span data-ttu-id="25e87-146">Если возвращается значение JET_wrnBufferTruncated, то выходной буфер будет содержать столько имен индексов, сколько будет помещаться в предоставленное пространство.</span><span class="sxs-lookup"><span data-stu-id="25e87-146">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the index name as will fit in the space provided.</span></span> <span data-ttu-id="25e87-147">Если выходной буфер имеет длину по крайней мере один символ, то строка, возвращаемая в этом буфере, будет завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="25e87-147">If the output buffer is at least one character in length then the string returned in that buffer will be null terminated.</span></span> <span data-ttu-id="25e87-148">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25e87-148">No change to the database state will occur.</span></span>

<span data-ttu-id="25e87-149">В случае сбоя состояние выходного буфера будет не определено.</span><span class="sxs-lookup"><span data-stu-id="25e87-149">On failure, the state of the output buffer will be undefined.</span></span> <span data-ttu-id="25e87-150">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25e87-150">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="25e87-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25e87-151">Remarks</span></span>

<span data-ttu-id="25e87-152">Если текущий индекс для курсора отсутствует, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="25e87-152">If there is no current index for the cursor then an empty string will be returned.</span></span> <span data-ttu-id="25e87-153">Это может произойти, если курсор находится на кластеризованном индексе таблицы, а первичный индекс не определен.</span><span class="sxs-lookup"><span data-stu-id="25e87-153">This can happen when the cursor is on the clustered index of the table and no primary index was defined.</span></span> <span data-ttu-id="25e87-154">Этот индекс известен как последовательный индекс таблицы и не имеет определения.</span><span class="sxs-lookup"><span data-stu-id="25e87-154">This index is known as the sequential index of the table and has no definition.</span></span> <span data-ttu-id="25e87-155">В любом случае установка текущего индекса в пустую строку с помощью [жетсеткуррентиндекс](./jetsetcurrentindex-function.md) выберет кластеризованный индекс независимо от наличия первичного определения индекса.</span><span class="sxs-lookup"><span data-stu-id="25e87-155">In any case, setting the current index to an empty string using [JetSetCurrentIndex](./jetsetcurrentindex-function.md) will select the clustered index regardless of the presence of a primary index definition.</span></span>

<span data-ttu-id="25e87-156">В этой функции есть важная ошибка, которая присутствует во всех выпусках.</span><span class="sxs-lookup"><span data-stu-id="25e87-156">There is an important bug in this function that is present in all releases.</span></span> <span data-ttu-id="25e87-157">Если выходной буфер слишком мал для получения всего имени индекса, а выходной буфер является по крайней мере одним символом длиной, то JET_wrnBufferTruncated не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="25e87-157">If the output buffer is too small to receive the entire index name and the output buffer is at least one character in length then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="25e87-158">Вместо этого будет возвращено JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="25e87-158">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="25e87-159">Чтобы избежать этой проблемы, выходной буфер должен всегда иметь длину не менее JET_cbNameMost + 1 (65) символов.</span><span class="sxs-lookup"><span data-stu-id="25e87-159">To avoid this issue, the output buffer should always be at least JET_cbNameMost + 1 (65) characters in length.</span></span>

#### <a name="requirements"></a><span data-ttu-id="25e87-160">Требования</span><span class="sxs-lookup"><span data-stu-id="25e87-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25e87-161"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="25e87-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="25e87-162">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="25e87-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e87-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="25e87-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="25e87-164">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="25e87-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25e87-165"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="25e87-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="25e87-166">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="25e87-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e87-167"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="25e87-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="25e87-168">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="25e87-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25e87-169"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="25e87-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="25e87-170">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="25e87-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e87-171"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="25e87-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="25e87-172">Реализуется как <strong>жетжеткуррентиндексв</strong> (Юникод) и <strong>жетжеткуррентиндекса</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="25e87-172">Implemented as <strong>JetGetCurrentIndexW</strong> (Unicode) and <strong>JetGetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="25e87-173">См. также:</span><span class="sxs-lookup"><span data-stu-id="25e87-173">See Also</span></span>

[<span data-ttu-id="25e87-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="25e87-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="25e87-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="25e87-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="25e87-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="25e87-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="25e87-177">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="25e87-177">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="25e87-178">жетсеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="25e87-178">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
