---
description: Дополнительные сведения о функции Жетсетиндексранже
title: Функция JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263234"
---
# <a name="jetsetindexrange-function"></a><span data-ttu-id="545d3-103">Функция JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="545d3-103">JetSetIndexRange Function</span></span>


<span data-ttu-id="545d3-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="545d3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetindexrange-function"></a><span data-ttu-id="545d3-105">Функция JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="545d3-105">JetSetIndexRange Function</span></span>

<span data-ttu-id="545d3-106">Функция **жетсетиндексранже** временно ограничивает набор записей индекса, которые курсор может проанализировать с помощью [жетмове](./jetmove-function.md) , начиная с текущего элемента индекса и заканчивая записью индекса, которая соответствует критериям поиска, заданным в ключе поиска в этом курсоре, и указанным критериям привязки.</span><span class="sxs-lookup"><span data-stu-id="545d3-106">The **JetSetIndexRange** function temporarily limits the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="545d3-107">Ключ поиска должен быть ранее создан с помощью [жетмакекэй](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="545d3-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="545d3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="545d3-108">Parameters</span></span>

<span data-ttu-id="545d3-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="545d3-109">*sesid*</span></span>

<span data-ttu-id="545d3-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="545d3-110">The session to use for this call.</span></span>

<span data-ttu-id="545d3-111">*таблеидсрк*</span><span class="sxs-lookup"><span data-stu-id="545d3-111">*tableidSrc*</span></span>

<span data-ttu-id="545d3-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="545d3-112">The cursor to use for this call.</span></span>

<span data-ttu-id="545d3-113">*грбит*</span><span class="sxs-lookup"><span data-stu-id="545d3-113">*grbit*</span></span>

<span data-ttu-id="545d3-114">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, в том числе ноль или более следующих:</span><span class="sxs-lookup"><span data-stu-id="545d3-114">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="545d3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="545d3-115">Value</span></span></p></th>
<th><p><span data-ttu-id="545d3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="545d3-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="545d3-117">JET_bitRangeInclusive</span><span class="sxs-lookup"><span data-stu-id="545d3-117">JET_bitRangeInclusive</span></span></p></td>
<td><p><span data-ttu-id="545d3-118">Это присутствие или отсутствие этого параметра указывает критерии границ диапазона индекса.</span><span class="sxs-lookup"><span data-stu-id="545d3-118">This presence or absence of this option indicates the boundary criteria of the index range.</span></span> <span data-ttu-id="545d3-119">При наличии этот параметр указывает, что предел диапазона индекса является инклюзивным.</span><span class="sxs-lookup"><span data-stu-id="545d3-119">When present, this option indicates that the limit of the index range is inclusive.</span></span> <span data-ttu-id="545d3-120">Если этот параметр отсутствует, это означает, что ограничение диапазона индекса является эксклюзивным.</span><span class="sxs-lookup"><span data-stu-id="545d3-120">When absent, this option indicates that the limit of the index range is exclusive.</span></span> <span data-ttu-id="545d3-121">Если ограничение диапазона индекса является инклюзивным, то все записи индекса, соответствующие условиям поиска, включаются в диапазон.</span><span class="sxs-lookup"><span data-stu-id="545d3-121">When the limit of the index range is inclusive then any index entries exactly matching the search criteria are included in the range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-122">JET_bitRangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="545d3-122">JET_bitRangeInstantDuration</span></span></p></td>
<td><p><span data-ttu-id="545d3-123">Этот параметр запрашивает удаление диапазона индекса сразу после его установки.</span><span class="sxs-lookup"><span data-stu-id="545d3-123">This option requests that the index range be removed as soon as it has been established.</span></span> <span data-ttu-id="545d3-124">Все остальные аспекты операции остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="545d3-124">All other aspects of the operation remain unchanged.</span></span> <span data-ttu-id="545d3-125">Это полезно для проверки существования записей индекса, соответствующих условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="545d3-125">This is useful for testing for the existence of index entries that match the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="545d3-126">JET_bitRangeRemove</span><span class="sxs-lookup"><span data-stu-id="545d3-126">JET_bitRangeRemove</span></span></p></td>
<td><p><span data-ttu-id="545d3-127">Этот параметр запрашивает отмену существующего диапазона индекса в курсоре.</span><span class="sxs-lookup"><span data-stu-id="545d3-127">This option requests that an existing index range on the cursor be canceled.</span></span> <span data-ttu-id="545d3-128">После отмены диапазона индексов можно будет перемещаться за пределы диапазона индекса с помощью <a href="gg294117(v=exchg.10).md">жетмове</a>.</span><span class="sxs-lookup"><span data-stu-id="545d3-128">Once the index range is canceled, it will be possible to move beyond the end of the index range using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span> <span data-ttu-id="545d3-129">Если диапазон индексов еще не действует, <strong>жетсетиндексранже</strong> завершится с JET_errInvalidOperation.</span><span class="sxs-lookup"><span data-stu-id="545d3-129">If an index range is not already in effect, then <strong>JetSetIndexRange</strong> will fail with JET_errInvalidOperation.</span></span></p>
<p><span data-ttu-id="545d3-130">Если указан этот параметр, все остальные параметры игнорируются.</span><span class="sxs-lookup"><span data-stu-id="545d3-130">When this option is specified, all other options are ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-131">JET_bitRangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="545d3-131">JET_bitRangeUpperLimit</span></span></p></td>
<td><p><span data-ttu-id="545d3-132">Если используется этот параметр, то ключ поиска в курсоре представляет критерий поиска для элемента индекса, ближайшего к концу индекса, который будет соответствовать диапазону индексов.</span><span class="sxs-lookup"><span data-stu-id="545d3-132">If this option is used, then the search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span> <span data-ttu-id="545d3-133">Диапазон индекса будет установлен между текущей позицией курсора и этой записью индекса, чтобы можно было найти все совпадения путем прохода по индексу с помощью <a href="gg294117(v=exchg.10).md">жетмове</a> с JET_MoveNext или положительным смещением.</span><span class="sxs-lookup"><span data-stu-id="545d3-133">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking forward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MoveNext or a positive offset.</span></span></p>
<p><span data-ttu-id="545d3-134">Этот параметр не имеет смысла использовать с ключом поиска, созданным с помощью <a href="gg269329(v=exchg.10).md">жетмакекэй</a> , с помощью параметра подстановочного знака, предназначенного для поиска записей индекса, ближайших к началу индекса.</span><span class="sxs-lookup"><span data-stu-id="545d3-134">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p>
<p><span data-ttu-id="545d3-135">Если этот параметр не указан, то поисковый ключ в курсоре представляет критерий поиска, ближайший к началу индекса, который будет соответствовать диапазону индексов.</span><span class="sxs-lookup"><span data-stu-id="545d3-135">If this option is omitted, then the search key in the cursor represents the search criteria for the index entry closest to the start of the index that will match the index range.</span></span> <span data-ttu-id="545d3-136">Диапазон индекса будет установлен между текущей позицией курсора и этой записью индекса, чтобы можно было найти все совпадения путем прохода назад по индексу с помощью <a href="gg294117(v=exchg.10).md">жетмове</a> с JET_MovePrevious или отрицательным смещением.</span><span class="sxs-lookup"><span data-stu-id="545d3-136">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking backward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MovePrevious or a negative offset.</span></span></p>
<p><span data-ttu-id="545d3-137">Не имеет смысла опускать этот параметр с помощью ключа поиска, созданного с помощью <a href="gg269329(v=exchg.10).md">жетмакекэй</a> , с помощью подстановочного знака, предназначенного для поиска записей индекса, ближайших к концу индекса.</span><span class="sxs-lookup"><span data-stu-id="545d3-137">It is not meaningful to omit this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="545d3-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="545d3-138">Return Value</span></span>

<span data-ttu-id="545d3-139">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="545d3-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="545d3-140">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="545d3-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="545d3-141">Код возврата</span><span class="sxs-lookup"><span data-stu-id="545d3-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="545d3-142">Описание</span><span class="sxs-lookup"><span data-stu-id="545d3-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="545d3-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="545d3-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="545d3-144">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="545d3-144">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="545d3-145">Для <strong>жетсетиндексранже</strong>это означает, что либо существующий диапазон индексов был отменен, либо в диапазоне индекса есть хотя бы одна запись индекса.</span><span class="sxs-lookup"><span data-stu-id="545d3-145">For <strong>JetSetIndexRange</strong>, this means that either an existing index range was canceled or that there is at least one index entry inside of the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="545d3-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="545d3-147">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="545d3-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="545d3-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="545d3-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="545d3-149">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="545d3-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="545d3-150">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="545d3-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="545d3-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="545d3-152">Эта ошибка будет возвращена функцией <strong>жетсетиндексранже</strong> при указании JET_bitRangeRemove и отсутствии диапазона индексов.</span><span class="sxs-lookup"><span data-stu-id="545d3-152">This error will be returned by <strong>JetSetIndexRange</strong> when JET_bitRangeRemove was specified and no index range was in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="545d3-153">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="545d3-153">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="545d3-154">Для курсора отсутствует текущий ключ поиска.</span><span class="sxs-lookup"><span data-stu-id="545d3-154">There is no current search key for the cursor.</span></span> <span data-ttu-id="545d3-155"><strong>Жетсетиндексранже</strong> требует, чтобы курсор имел допустимый ключ поиска, так как он будет использовать его для условий поиска, используемых для поиска записей индекса.</span><span class="sxs-lookup"><span data-stu-id="545d3-155"><strong>JetSetIndexRange</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-156">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="545d3-156">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="545d3-157">Для курсора отсутствует текущий индекс.</span><span class="sxs-lookup"><span data-stu-id="545d3-157">There is no current index for the cursor.</span></span> <span data-ttu-id="545d3-158">Это произойдет для <strong>жетсетиндексранже</strong> , если курсор находится на кластеризованном индексе таблицы, первичный индекс не определен.</span><span class="sxs-lookup"><span data-stu-id="545d3-158">This will happen for <strong>JetSetIndexRange</strong> if the cursor is on the clustered index of a table, a primary index has not been defined.</span></span> <span data-ttu-id="545d3-159">Установка диапазона индекса по такому индексу не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="545d3-159">Setting an index range over such an index is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="545d3-160">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="545d3-160">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="545d3-161">Эта ошибка будет возвращена функцией <strong>жетсетиндексранже</strong> , чтобы указать, что в диапазоне индекса нет записей индекса.</span><span class="sxs-lookup"><span data-stu-id="545d3-161">This error will be returned by <strong>JetSetIndexRange</strong> to indicate that there are no index entries inside the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-162">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="545d3-162">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="545d3-163">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="545d3-163">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="545d3-164">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="545d3-164">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="545d3-165">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="545d3-165">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-166">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="545d3-166">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="545d3-167">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="545d3-167">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="545d3-168">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="545d3-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="545d3-169">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="545d3-169">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="545d3-170">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="545d3-170">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="545d3-171">При успешном выполнении, если указан JET_bitRangeRemove, то диапазон индексов, действующий в данный момент, отменяется.</span><span class="sxs-lookup"><span data-stu-id="545d3-171">On success, if JET_bitRangeRemove is specified, then the index range that is currently in effect is canceled.</span></span> <span data-ttu-id="545d3-172">Если JET_bitRangeRemove не указан и указан JET_bitRangeInstantDuration, диапазон индексов не действует.</span><span class="sxs-lookup"><span data-stu-id="545d3-172">If JET_bitRangeRemove is not specified and JET_bitRangeInstantDuration is specified, then no index range is in effect.</span></span> <span data-ttu-id="545d3-173">Если не указаны ни JET_bitRangeRemove, ни JET_bitRangeInstantDuration, то действует новый диапазон индекса.</span><span class="sxs-lookup"><span data-stu-id="545d3-173">If neither JET_bitRangeRemove nor JET_bitRangeInstantDuration is specified, then a new index range is in effect.</span></span> <span data-ttu-id="545d3-174">Этот диапазон индексов временно ограничивает набор записей индекса, которые курсор может проанализировать с помощью [жетмове](./jetmove-function.md) , начиная с текущей записи индекса и заканчивая записью индекса, которая соответствует критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="545d3-174">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="545d3-175">Позиции курсора останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="545d3-175">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="545d3-176">Если для курсора был создан ключ поиска, то этот ключ поиска будет удален.</span><span class="sxs-lookup"><span data-stu-id="545d3-176">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="545d3-177">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="545d3-177">No change to the database state will occur.</span></span>

<span data-ttu-id="545d3-178">В случае сбоя, если JET_errNoCurrentRecord не возвращается, диапазон индексов не действует.</span><span class="sxs-lookup"><span data-stu-id="545d3-178">On failure, if JET_errNoCurrentRecord is not returned, then no index range is in effect.</span></span> <span data-ttu-id="545d3-179">Если возвращается значение JET_errNoCurrentRecord, действует новый диапазон индекса.</span><span class="sxs-lookup"><span data-stu-id="545d3-179">If JET_errNoCurrentRecord is returned, then a new index range is in effect.</span></span> <span data-ttu-id="545d3-180">Этот диапазон индексов временно ограничивает набор записей индекса, которые курсор может проанализировать с помощью [жетмове](./jetmove-function.md) , начиная с текущей записи индекса и заканчивая записью индекса, которая соответствует критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="545d3-180">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="545d3-181">Позиции курсора останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="545d3-181">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="545d3-182">Если был возвращен JET_errNoCurrentRecord и для курсора был создан ключ поиска, то этот ключ поиска будет удален.</span><span class="sxs-lookup"><span data-stu-id="545d3-182">If JET_errNoCurrentRecord was returned and a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="545d3-183">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="545d3-183">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="545d3-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="545d3-184">Remarks</span></span>

<span data-ttu-id="545d3-185">Диапазон индексов является временным и автоматически отменяется, если в курсоре выполняется любая Навигация, отличная от [жетмове](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="545d3-185">An index range is volatile and will automatically be canceled if any navigation other than [JetMove](./jetmove-function.md) is performed on the cursor.</span></span>

<span data-ttu-id="545d3-186">Индексные диапазоны работают только в одном направлении.</span><span class="sxs-lookup"><span data-stu-id="545d3-186">Index ranges only work in one direction.</span></span> <span data-ttu-id="545d3-187">Если установлен верхний предел, то после достижения конца диапазона индекса будет предотвращено только перенаправление движения с использованием [жетмове](./jetmove-function.md) с JET_MoveNext или положительным смещением.</span><span class="sxs-lookup"><span data-stu-id="545d3-187">If an upper limit is established then only forward motion using [JetMove](./jetmove-function.md) with JET_MoveNext or a positive offset will be prevented once the end of the index range has been reached.</span></span> <span data-ttu-id="545d3-188">В этом случае можно оставить диапазон индекса в этом случае, используя [жетмове](./jetmove-function.md) с JET_MovePrevious или отрицательным смещением.</span><span class="sxs-lookup"><span data-stu-id="545d3-188">It is still possible to leave the index range in this case using [JetMove](./jetmove-function.md) with JET_MovePrevious or a negative offset.</span></span> <span data-ttu-id="545d3-189">Аналогичная ситуация возникает для нижнего предела.</span><span class="sxs-lookup"><span data-stu-id="545d3-189">An analogous situation occurs for a lower limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="545d3-190">Требования</span><span class="sxs-lookup"><span data-stu-id="545d3-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="545d3-191"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="545d3-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="545d3-192">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="545d3-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-193"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="545d3-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="545d3-194">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="545d3-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="545d3-195"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="545d3-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="545d3-196">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="545d3-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="545d3-197"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="545d3-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="545d3-198">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="545d3-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="545d3-199"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="545d3-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="545d3-200">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="545d3-200">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="545d3-201">См. также:</span><span class="sxs-lookup"><span data-stu-id="545d3-201">See Also</span></span>

[<span data-ttu-id="545d3-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="545d3-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="545d3-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="545d3-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="545d3-204">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="545d3-204">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="545d3-205">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="545d3-205">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="545d3-206">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="545d3-206">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="545d3-207">жетмове</span><span class="sxs-lookup"><span data-stu-id="545d3-207">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="545d3-208">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="545d3-208">JetSetIndexRange</span></span>]()  
[<span data-ttu-id="545d3-209">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="545d3-209">JetStopService</span></span>](./jetstopservice-function.md)
