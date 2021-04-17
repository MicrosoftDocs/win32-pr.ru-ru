---
description: Дополнительные сведения о функции Жетжетсекондариндексбукмарк
title: Функция Жетжетсекондариндексбукмарк
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712069"
---
# <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="bbad2-103">Функция Жетжетсекондариндексбукмарк</span><span class="sxs-lookup"><span data-stu-id="bbad2-103">JetGetSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="bbad2-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bbad2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="bbad2-105">Функция Жетжетсекондариндексбукмарк</span><span class="sxs-lookup"><span data-stu-id="bbad2-105">JetGetSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="bbad2-106">Функция **жетжетсекондариндексбукмарк** извлекает специальную закладку для записи вторичного индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="bbad2-106">The **JetGetSecondaryIndexBookmark** function retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="bbad2-107">Эту закладку можно использовать для эффективного перемещения курсора обратно к той же записи индекса с помощью [жетготосекондариндексбукмарк](./jetgotosecondaryindexbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="bbad2-107">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span></span> <span data-ttu-id="bbad2-108">Это наиболее полезно при изменении расположения вторичного индекса, который содержит дублирующиеся ключи или содержит несколько записей индекса для одной и той же записи.</span><span class="sxs-lookup"><span data-stu-id="bbad2-108">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="bbad2-109">**Windows XP: жетжетсекондариндексбукмарк** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bbad2-109">**Windows XP:  JetGetSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="bbad2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbad2-110">Parameters</span></span>

<span data-ttu-id="bbad2-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="bbad2-111">*sesid*</span></span>

<span data-ttu-id="bbad2-112">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="bbad2-112">The session to use for this call.</span></span>

<span data-ttu-id="bbad2-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="bbad2-113">*tableid*</span></span>

<span data-ttu-id="bbad2-114">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="bbad2-114">The cursor to use for this call.</span></span>

<span data-ttu-id="bbad2-115">*пвсекондарикэй*</span><span class="sxs-lookup"><span data-stu-id="bbad2-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="bbad2-116">Выходной буфер, который получает вторичный ключ.</span><span class="sxs-lookup"><span data-stu-id="bbad2-116">The output buffer that receives the secondary key.</span></span>

<span data-ttu-id="bbad2-117">*кбсекондарикэймакс*</span><span class="sxs-lookup"><span data-stu-id="bbad2-117">*cbSecondaryKeyMax*</span></span>

<span data-ttu-id="bbad2-118">Максимальный размер (в байтах) выходного буфера для вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="bbad2-118">The maximum size, in bytes, of the output buffer for the secondary key.</span></span>

<span data-ttu-id="bbad2-119">*пкбсекондарикэйактуал*</span><span class="sxs-lookup"><span data-stu-id="bbad2-119">*pcbSecondaryKeyActual*</span></span>

<span data-ttu-id="bbad2-120">Получает фактический размер вторичного ключа в байтах.</span><span class="sxs-lookup"><span data-stu-id="bbad2-120">Receives the actual size in bytes of the secondary key.</span></span>

<span data-ttu-id="bbad2-121">Если этот параметр имеет значение NULL, фактический размер вторичного ключа не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="bbad2-121">If this parameter is NULL, the actual size of the secondary key will not be returned.</span></span>

<span data-ttu-id="bbad2-122">Если выходной буфер слишком мал, фактический размер вторичного ключа будет по-прежнему возвращен.</span><span class="sxs-lookup"><span data-stu-id="bbad2-122">If the output buffer is too small, the actual size of the secondary key will still be returned.</span></span> <span data-ttu-id="bbad2-123">Это означает, что это число будет больше, чем размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="bbad2-123">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="bbad2-124">*пвпримарибукмарк*</span><span class="sxs-lookup"><span data-stu-id="bbad2-124">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="bbad2-125">Выходной буфер, получающий закладку первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="bbad2-125">The output buffer that receives the primary key bookmark.</span></span>

<span data-ttu-id="bbad2-126">*кбпримарибукмаркмакс*</span><span class="sxs-lookup"><span data-stu-id="bbad2-126">*cbPrimaryBookmarkMax*</span></span>

<span data-ttu-id="bbad2-127">Максимальный размер (в байтах) выходного буфера для закладки первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="bbad2-127">The maximum size, in bytes, of the output buffer for the primary key bookmark.</span></span>

<span data-ttu-id="bbad2-128">*пкбпримарикэйактуал*</span><span class="sxs-lookup"><span data-stu-id="bbad2-128">*pcbPrimaryKeyActual*</span></span>

<span data-ttu-id="bbad2-129">Получает фактический размер закладки первичного ключа (в байтах).</span><span class="sxs-lookup"><span data-stu-id="bbad2-129">Receives the actual size, in bytes, of the primary key bookmark.</span></span>

<span data-ttu-id="bbad2-130">Если этот параметр имеет значение NULL, фактический размер закладки первичного ключа не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="bbad2-130">If this parameter is NULL then the actual size of the primary key bookmark will not be returned.</span></span>

<span data-ttu-id="bbad2-131">Если выходной буфер слишком мал, то фактический размер закладки первичного ключа будет по-прежнему возвращен.</span><span class="sxs-lookup"><span data-stu-id="bbad2-131">If the output buffer is too small, the actual size of the primary key bookmark will still be returned.</span></span> <span data-ttu-id="bbad2-132">Это означает, что это число будет больше, чем размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="bbad2-132">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="bbad2-133">*грбит*</span><span class="sxs-lookup"><span data-stu-id="bbad2-133">*grbit*</span></span>

<span data-ttu-id="bbad2-134">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="bbad2-134">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="bbad2-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbad2-135">Return Value</span></span>

<span data-ttu-id="bbad2-136">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="bbad2-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bbad2-137">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bbad2-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbad2-138">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bbad2-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="bbad2-139">Описание</span><span class="sxs-lookup"><span data-stu-id="bbad2-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbad2-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bbad2-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bbad2-141">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bbad2-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbad2-142">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="bbad2-142">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="bbad2-143">Операция успешно завершена, но один из буферов вывода слишком мал для получения запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="bbad2-143">The operation completed successfully, but one of the output buffers was too small to receive the requested data.</span></span></p>
<p><span data-ttu-id="bbad2-144">Выходной буфер заполнен объемом заданной закладки.</span><span class="sxs-lookup"><span data-stu-id="bbad2-144">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="bbad2-145">При запросе также возвращается фактический размер закладки.</span><span class="sxs-lookup"><span data-stu-id="bbad2-145">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbad2-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bbad2-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bbad2-147">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="bbad2-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbad2-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bbad2-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bbad2-149">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="bbad2-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="bbad2-150">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="bbad2-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbad2-151">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="bbad2-151">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="bbad2-152">Курсор в данный момент не находится во вторичном индексе.</span><span class="sxs-lookup"><span data-stu-id="bbad2-152">The cursor is not currently on a secondary index.</span></span></p>
<p><span data-ttu-id="bbad2-153">Получение закладки вторичного индекса не имеет смысла, когда курсор в данный момент не использует вторичный индекс.</span><span class="sxs-lookup"><span data-stu-id="bbad2-153">It is not meaningful to retrieve a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="bbad2-154"><a href="gg269221(v=exchg.10).md">Жетжетбукмарк</a> следует использовать, если курсор не находится на вторичном индексе.</span><span class="sxs-lookup"><span data-stu-id="bbad2-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbad2-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="bbad2-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="bbad2-156">Курсор не располагается на записи.</span><span class="sxs-lookup"><span data-stu-id="bbad2-156">The cursor is not positioned on a record.</span></span></p>
<p><span data-ttu-id="bbad2-157">Это может произойти по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="bbad2-157">This can happen for many different reasons.</span></span> <span data-ttu-id="bbad2-158">Например, это произойдет, если курсор находится в данный момент после последней записи в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="bbad2-158">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbad2-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bbad2-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bbad2-160">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="bbad2-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbad2-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bbad2-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bbad2-162">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="bbad2-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbad2-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bbad2-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bbad2-164">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="bbad2-164">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="bbad2-165">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="bbad2-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbad2-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bbad2-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bbad2-167">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="bbad2-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bbad2-168">При успешном выполнении закладка вторичного индекса для записи индекса в текущей позиции курсора будет возвращена в выходных буферах.</span><span class="sxs-lookup"><span data-stu-id="bbad2-168">On success, the secondary index bookmark for the index entry at the current position of a cursor will be returned in the output buffers.</span></span> <span data-ttu-id="bbad2-169">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbad2-169">No change to the database state will occur.</span></span>

<span data-ttu-id="bbad2-170">В случае сбоя состояние буферов вывода и фактический размер закладки вторичного индекса будут неопределенными, если не была возвращена JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="bbad2-170">On failure, the state of the output buffers and the actual size of the secondary index bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="bbad2-171">В случае, если возвращается JET_errBufferTooSmall, выходные буферы будут содержать столько закладок вторичного индекса, сколько будет помещаться в предоставленное пространство, и фактический размер закладки вторичного индекса будет неточным.</span><span class="sxs-lookup"><span data-stu-id="bbad2-171">In the event that JET_errBufferTooSmall is returned, the output buffers will contain as much of the secondary index bookmark as will fit in the space provided and the actual size of the secondary index bookmark will be accurate.</span></span> <span data-ttu-id="bbad2-172">В любом случае изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbad2-172">In any case, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bbad2-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbad2-173">Remarks</span></span>

<span data-ttu-id="bbad2-174">Закладки обычно должны рассматриваться как непрозрачные фрагменты данных.</span><span class="sxs-lookup"><span data-stu-id="bbad2-174">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="bbad2-175">Для использования внутренней структуры этих данных не нужно предпринимать никаких попыток.</span><span class="sxs-lookup"><span data-stu-id="bbad2-175">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="bbad2-176">Однако следующие свойства могут быть известны всем закладкам ESENT:</span><span class="sxs-lookup"><span data-stu-id="bbad2-176">However, the following properties can be known about all ESENT bookmarks:</span></span>

  - <span data-ttu-id="bbad2-177">Закладка однозначно определяет запись в заданной таблице.</span><span class="sxs-lookup"><span data-stu-id="bbad2-177">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="bbad2-178">Закладка записи не изменится в течение времени существования этой записи.</span><span class="sxs-lookup"><span data-stu-id="bbad2-178">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="bbad2-179">Закладка записи совпадает с ключом записи на первичном индексе таблицы, содержащей эту запись.</span><span class="sxs-lookup"><span data-stu-id="bbad2-179">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="bbad2-180">Если для этой таблицы не определен первичный индекс, ядро СУБД создаст собственную закладку для записи.</span><span class="sxs-lookup"><span data-stu-id="bbad2-180">If no primary index is defined over that table, the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="bbad2-181">Закладки можно сравнить друг с другом с помощью [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) , чтобы установить их относительное упорядочение в первичном индексе по таблице исходных записей.</span><span class="sxs-lookup"><span data-stu-id="bbad2-181">Bookmarks may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="bbad2-182">Если для этой таблицы не определен первичный индекс, то относительный порядок закладок от этой таблицы не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="bbad2-182">If no primary index is defined over that table, the relative ordering of bookmarks from that table is not meaningful.</span></span>

  - <span data-ttu-id="bbad2-183">Нет смысла сравнивать закладки записей из разных таблиц друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bbad2-183">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="bbad2-184">Длина закладки всегда меньше или равна JET_cbBookmarkMost (256) байт до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbad2-184">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="bbad2-185">В Windows Vista и более поздних выпусках закладки могут быть более крупными.</span><span class="sxs-lookup"><span data-stu-id="bbad2-185">On Windows Vista and later releases, bookmarks can be larger.</span></span> <span data-ttu-id="bbad2-186">Максимальный размер закладки равен текущему значению JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="bbad2-186">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

<span data-ttu-id="bbad2-187">Обычно ключи обрабатываются как непрозрачные фрагменты данных.</span><span class="sxs-lookup"><span data-stu-id="bbad2-187">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="bbad2-188">Для использования внутренней структуры этих данных не нужно предпринимать никаких попыток.</span><span class="sxs-lookup"><span data-stu-id="bbad2-188">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="bbad2-189">Однако следующие свойства могут быть известны всем ключам ESENT:</span><span class="sxs-lookup"><span data-stu-id="bbad2-189">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="bbad2-190">Ключи можно сравнить друг с другом с помощью [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) , чтобы установить их относительное упорядочение в исходном индексе по таблице записей исходного индекса.</span><span class="sxs-lookup"><span data-stu-id="bbad2-190">Keys may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="bbad2-191">Нет смысла сравнивать ключи индексов из разных индексов друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bbad2-191">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="bbad2-192">Длина ключа всегда меньше или равна JET_cbKeyMost (255) байт до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbad2-192">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="bbad2-193">В Windows Vista и более поздних выпусках ключи могут быть больше.</span><span class="sxs-lookup"><span data-stu-id="bbad2-193">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="bbad2-194">Максимальный размер ключа равен текущему значению JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="bbad2-194">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bbad2-195">Требования</span><span class="sxs-lookup"><span data-stu-id="bbad2-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbad2-196"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="bbad2-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bbad2-197">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bbad2-197">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbad2-198"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bbad2-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bbad2-199">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bbad2-199">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbad2-200"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bbad2-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bbad2-201">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bbad2-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbad2-202"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="bbad2-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bbad2-203">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bbad2-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbad2-204"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="bbad2-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bbad2-205">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bbad2-205">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bbad2-206">См. также:</span><span class="sxs-lookup"><span data-stu-id="bbad2-206">See Also</span></span>

[<span data-ttu-id="bbad2-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bbad2-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bbad2-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bbad2-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bbad2-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bbad2-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bbad2-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bbad2-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bbad2-211">жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="bbad2-211">JetGetBookmark</span></span>](./jetgetbookmark-function.md)  
[<span data-ttu-id="bbad2-212">жетготосекондариндексбукмарк</span><span class="sxs-lookup"><span data-stu-id="bbad2-212">JetGotoSecondaryIndexBookmark</span></span>](./jetgotosecondaryindexbookmark-function.md)  
[<span data-ttu-id="bbad2-213">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="bbad2-213">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
<span data-ttu-id="bbad2-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="bbad2-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
