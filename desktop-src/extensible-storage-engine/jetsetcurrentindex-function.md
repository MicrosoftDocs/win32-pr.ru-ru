---
description: Дополнительные сведения о функции Жетсеткуррентиндекс
title: Функция JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710936"
---
# <a name="jetsetcurrentindex-function"></a><span data-ttu-id="484f5-103">Функция JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="484f5-103">JetSetCurrentIndex Function</span></span>


<span data-ttu-id="484f5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="484f5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex-function"></a><span data-ttu-id="484f5-105">Функция JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="484f5-105">JetSetCurrentIndex Function</span></span>

<span data-ttu-id="484f5-106">Функцию **жетсеткуррентиндекс** можно использовать для задания текущего индекса курсора.</span><span class="sxs-lookup"><span data-stu-id="484f5-106">The **JetSetCurrentIndex** function can be used to set the current index of a cursor.</span></span> <span data-ttu-id="484f5-107">Текущий индекс курсора определяет, какие записи в таблице видимы для этого курсора, и порядок, в котором они отображаются, выбрав набор записей индекса, который будет использоваться для предоставления этих записей.</span><span class="sxs-lookup"><span data-stu-id="484f5-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="484f5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="484f5-108">Parameters</span></span>

<span data-ttu-id="484f5-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="484f5-109">*sesid*</span></span>

<span data-ttu-id="484f5-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="484f5-110">The session to use for this call.</span></span>

<span data-ttu-id="484f5-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="484f5-111">*tableid*</span></span>

<span data-ttu-id="484f5-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="484f5-112">The cursor to use for this call.</span></span>

<span data-ttu-id="484f5-113">*сзиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="484f5-113">*szIndexName*</span></span>

<span data-ttu-id="484f5-114">Имя индекса, выбранного для курсора.</span><span class="sxs-lookup"><span data-stu-id="484f5-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="484f5-115">Если этот параметр имеет значение NULL или является пустой строкой, выбирается кластеризованный индекс.</span><span class="sxs-lookup"><span data-stu-id="484f5-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="484f5-116">Если для таблицы определен первичный индекс, то этот индекс будет выбран, так как он совпадает с кластеризованным индексом.</span><span class="sxs-lookup"><span data-stu-id="484f5-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="484f5-117">Если для таблицы не определен первичный индекс, будет выбран последовательный индекс.</span><span class="sxs-lookup"><span data-stu-id="484f5-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="484f5-118">Последовательный индекс не имеет определения индекса.</span><span class="sxs-lookup"><span data-stu-id="484f5-118">The sequential index has no index definition.</span></span> <span data-ttu-id="484f5-119">Дополнительные сведения см. в разделе [жеткреатеиндекс](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="484f5-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="484f5-120">Если *pIndexID* не равно null, имя индекса будет игнорироваться, а индекс будет выбран по идентификатору индекса.</span><span class="sxs-lookup"><span data-stu-id="484f5-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

### <a name="return-value"></a><span data-ttu-id="484f5-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="484f5-121">Return Value</span></span>

<span data-ttu-id="484f5-122">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="484f5-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="484f5-123">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="484f5-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="484f5-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="484f5-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="484f5-125">Описание</span><span class="sxs-lookup"><span data-stu-id="484f5-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="484f5-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="484f5-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="484f5-127">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="484f5-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-128">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="484f5-128">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="484f5-129">Вторичный индекс выбирается с параметром JET_bitNoMove и для первого многозначного ключевого столбца в определении нового индекса, который соответствует указанному порядковому номеру, отсутствует значение.</span><span class="sxs-lookup"><span data-stu-id="484f5-129">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="484f5-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="484f5-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="484f5-131">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="484f5-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-132">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="484f5-132">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="484f5-133">Содержимое идентификатора индекса недопустимо или устарело, и его необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="484f5-133">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="484f5-134">Это может произойти для <strong>жетсеткуррентиндекс</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="484f5-134">This can happen for <strong>JetSetCurrentIndex</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="484f5-135">pIndexID- &gt; кбструкт не имеет ожидаемого размера (Windows Server 2003 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="484f5-135">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="484f5-136">Работа обработчика была завершена, так как был получен идентификатор индекса.</span><span class="sxs-lookup"><span data-stu-id="484f5-136">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="484f5-137">Все курсоры, ссылающиеся на таблицу, содержащую индекс, соответствующий ИДЕНТИФИКАТОРу индекса, были закрыты и обработчик удалил определение индекса из кэша схемы.</span><span class="sxs-lookup"><span data-stu-id="484f5-137">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="484f5-138">Идентификатор индекса используется с курсором, открытым в неверной таблице.</span><span class="sxs-lookup"><span data-stu-id="484f5-138">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="484f5-139">Индекс был удален или еще не виден в сеансе.</span><span class="sxs-lookup"><span data-stu-id="484f5-139">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="484f5-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="484f5-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="484f5-141">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="484f5-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="484f5-142">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="484f5-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-143">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="484f5-143">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="484f5-144">Одно из указанных имен объектов недопустимо.</span><span class="sxs-lookup"><span data-stu-id="484f5-144">One of the specified object names was invalid.</span></span> <span data-ttu-id="484f5-145">Все имена объектов должны соответствовать одному и тому же набору правил.</span><span class="sxs-lookup"><span data-stu-id="484f5-145">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="484f5-146">Ниже приведены эти правила.</span><span class="sxs-lookup"><span data-stu-id="484f5-146">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="484f5-147">Имена объектов должны состоять из символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="484f5-147">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="484f5-148">Имена объектов должны иметь длину по крайней мере один символ.</span><span class="sxs-lookup"><span data-stu-id="484f5-148">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="484f5-149">Длина имен объектов не может превышать JET_cbNameMost (64) символов.</span><span class="sxs-lookup"><span data-stu-id="484f5-149">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="484f5-150">Имена объектов не могут начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="484f5-150">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="484f5-151">Имена объектов не могут содержать управляющие символы ASCII (0x00 – 0x1F).</span><span class="sxs-lookup"><span data-stu-id="484f5-151">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="484f5-152">Имена объектов не могут содержать восклицательный знак (!), точку (.), открывающую квадратную скобку ([) или правую квадратную скобку (]).</span><span class="sxs-lookup"><span data-stu-id="484f5-152">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="484f5-153">После проверки для имени объекта будет использоваться только часть строки вплоть до первого пробела (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="484f5-153">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="484f5-154">Это фактически означает, что имена объектов не могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="484f5-154">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="484f5-155">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="484f5-155">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="484f5-156">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="484f5-156">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="484f5-157">Это может произойти для <strong>жетсеткуррентиндекс</strong> , если <em>PINDEXID</em> не равен null, а pIndexID- &gt; кбструкт не имеет ожидаемого размера (Windows XP и более ранние выпуски).</span><span class="sxs-lookup"><span data-stu-id="484f5-157">This can happen for <strong>JetSetCurrentIndex</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-158">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="484f5-158">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="484f5-159">Вторичный индекс выбирается с параметром JET_bitNoMove и в новом индексе отсутствует запись индекса, соответствующая записи, связанной с записью индекса, в текущей позиции курсора по старому индексу.</span><span class="sxs-lookup"><span data-stu-id="484f5-159">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="484f5-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="484f5-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="484f5-161">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="484f5-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-162">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="484f5-162">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="484f5-163">Подсистема исчерпала пул ресурсов, используемых для открытия курсоров.</span><span class="sxs-lookup"><span data-stu-id="484f5-163">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="484f5-164">С помощью <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>можно управлять максимальным количеством курсоров, которые могут быть открыты в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="484f5-164">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="484f5-165">Дополнительные сведения см. в разделе <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> .</span><span class="sxs-lookup"><span data-stu-id="484f5-165">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="484f5-166">Это может произойти для <strong>жетсеткуррентиндекс</strong> , когда был выбран вторичный индекс, и обработчик не может открыть внутренний курсор для использования этого индекса.</span><span class="sxs-lookup"><span data-stu-id="484f5-166">This can happen for <strong>JetSetCurrentIndex</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="484f5-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="484f5-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="484f5-168">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="484f5-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="484f5-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="484f5-170">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="484f5-170">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="484f5-171">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="484f5-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="484f5-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="484f5-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="484f5-173">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="484f5-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="484f5-174">При успешном выполнении текущий индекс курсора задается равным запрошенному индексу.</span><span class="sxs-lookup"><span data-stu-id="484f5-174">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="484f5-175">Теперь элементы индекса можно искать с помощью [жетсик](./jetseek-function.md) в соответствии с определением индекса запрошенного индекса.</span><span class="sxs-lookup"><span data-stu-id="484f5-175">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="484f5-176">Элементы индекса можно также перечислить с помощью [жетмове](./jetmove-function.md) в порядке, указанном в определении индекса.</span><span class="sxs-lookup"><span data-stu-id="484f5-176">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="484f5-177">Текущая позиция курсора либо установлена на первый элемент индекса (JET_bitMoveFirst), либо на конкретную запись индекса, связанную с текущей позицией курсора по старому индексу (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="484f5-177">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="484f5-178">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="484f5-178">No change to the database state will occur.</span></span>

<span data-ttu-id="484f5-179">В случае сбоя текущий индекс и текущая позиция курсора находятся в неопределенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="484f5-179">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="484f5-180">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="484f5-180">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="484f5-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="484f5-181">Remarks</span></span>

<span data-ttu-id="484f5-182">Если указание идентификатора индекса устарело, то API просто завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="484f5-182">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="484f5-183">В данном случае откат к текстовому имени индекса отсутствует, как можно было бы ожидать.</span><span class="sxs-lookup"><span data-stu-id="484f5-183">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="484f5-184">Эта резервная копия должна выполняться вручную вызывающим объектом API.</span><span class="sxs-lookup"><span data-stu-id="484f5-184">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="484f5-185">Требования</span><span class="sxs-lookup"><span data-stu-id="484f5-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="484f5-186"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="484f5-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="484f5-187">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="484f5-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="484f5-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="484f5-189">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="484f5-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="484f5-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="484f5-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="484f5-191">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="484f5-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-192"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="484f5-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="484f5-193">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="484f5-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="484f5-194"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="484f5-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="484f5-195">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="484f5-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="484f5-196"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="484f5-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="484f5-197">Реализуется как <strong>жетсеткуррентиндексв</strong> (Юникод) и <strong>жетсеткуррентиндекса</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="484f5-197">Implemented as <strong>JetSetCurrentIndexW</strong> (Unicode) and <strong>JetSetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="484f5-198">См. также:</span><span class="sxs-lookup"><span data-stu-id="484f5-198">See Also</span></span>

[<span data-ttu-id="484f5-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="484f5-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="484f5-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="484f5-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="484f5-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="484f5-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="484f5-202">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="484f5-202">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="484f5-203">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="484f5-203">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="484f5-204">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="484f5-204">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="484f5-205">жетжеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="484f5-205">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="484f5-206">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="484f5-206">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="484f5-207">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="484f5-207">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="484f5-208">жетмове</span><span class="sxs-lookup"><span data-stu-id="484f5-208">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="484f5-209">жетсик</span><span class="sxs-lookup"><span data-stu-id="484f5-209">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="484f5-210">жетсеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="484f5-210">JetSetCurrentIndex</span></span>]()  
[<span data-ttu-id="484f5-211">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="484f5-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="484f5-212">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="484f5-212">JetStopService</span></span>](./jetstopservice-function.md)
