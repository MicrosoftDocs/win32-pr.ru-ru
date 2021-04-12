---
description: Дополнительные сведения о функции Жетретриевеколумнс
title: Функция JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272393"
---
# <a name="jetretrievecolumns-function"></a><span data-ttu-id="77fc1-103">Функция JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="77fc1-103">JetRetrieveColumns Function</span></span>


<span data-ttu-id="77fc1-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77fc1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumns-function"></a><span data-ttu-id="77fc1-105">Функция JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="77fc1-105">JetRetrieveColumns Function</span></span>

<span data-ttu-id="77fc1-106">Функция **жетретриевеколумнс** получает несколько значений столбцов из текущей записи в одной операции.</span><span class="sxs-lookup"><span data-stu-id="77fc1-106">The **JetRetrieveColumns** function retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="77fc1-107">Массив структур [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) используется для описания набора значений столбцов для извлечения, а также для описания выходных буферов для каждого извлекаемого значения столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-107">An array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="77fc1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="77fc1-108">Parameters</span></span>

<span data-ttu-id="77fc1-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="77fc1-109">*sesid*</span></span>

<span data-ttu-id="77fc1-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="77fc1-110">The session to use for this call.</span></span>

<span data-ttu-id="77fc1-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="77fc1-111">*tableid*</span></span>

<span data-ttu-id="77fc1-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="77fc1-112">The cursor to use for this call.</span></span>

<span data-ttu-id="77fc1-113">*претриевеколумн*</span><span class="sxs-lookup"><span data-stu-id="77fc1-113">*pretrievecolumn*</span></span>

<span data-ttu-id="77fc1-114">Указатель на массив из одной или нескольких структур [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="77fc1-114">A pointer to an array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="77fc1-115">Каждая структура включает описание того, какое значение столбца необходимо извлечь и где хранить возвращенные данные.</span><span class="sxs-lookup"><span data-stu-id="77fc1-115">Each structure includes descriptions of which column value to retrieve and where to store returned data.</span></span>

<span data-ttu-id="77fc1-116">*кретриевеколумн*</span><span class="sxs-lookup"><span data-stu-id="77fc1-116">*cretrievecolumn*</span></span>

<span data-ttu-id="77fc1-117">Число структур [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) в массиве, заданном параметром *претриевеколумн*.</span><span class="sxs-lookup"><span data-stu-id="77fc1-117">The number of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures in the array given by *pretrievecolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="77fc1-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77fc1-118">Return Value</span></span>

<span data-ttu-id="77fc1-119">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="77fc1-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="77fc1-120">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="77fc1-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77fc1-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="77fc1-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="77fc1-122">Описание</span><span class="sxs-lookup"><span data-stu-id="77fc1-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="77fc1-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="77fc1-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="77fc1-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-125">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="77fc1-125">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="77fc1-126">Недопустимое значение порядкового номера столбца с несколькими значениями было передано в претинфо- &gt; итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="77fc1-126">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="77fc1-127">Допустимые значения для порядковых номеров значений столбца с несколькими значениями: 1 или более.</span><span class="sxs-lookup"><span data-stu-id="77fc1-127">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="77fc1-128">Значение 0 (ноль) допустимо для этой функции, но недопустимо для <a href="gg269198(v=exchg.10).md">жетретриевеколумн</a>.</span><span class="sxs-lookup"><span data-stu-id="77fc1-128">A value of 0 (zero) is valid for this function but is invalid for <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-129">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="77fc1-129">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="77fc1-130">Указанный идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-130">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="77fc1-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="77fc1-132">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="77fc1-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="77fc1-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="77fc1-134">Столбец, описываемый данным <em>columnid</em> , не существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="77fc1-134">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-135">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="77fc1-135">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="77fc1-136">Столбцы, индексируемые как подстроки, не могут быть извлечены из индекса, так как в каждой записи индекса обычно содержится только небольшая часть столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-136">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-137">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="77fc1-137">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="77fc1-138">В некоторых случаях буфер, заданный для столбца получения, должен иметь достаточный размер, чтобы вернуть любой объем значения столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-138">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="77fc1-139">Например, депонированные обновляемые столбцы настраиваются таким образом, чтобы они были согласованы в транзакционном контексте вызывающего сеанса, и эта корректировка требует наличия буфера, предоставленного вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="77fc1-139">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="77fc1-140">Если предоставлено недостаточное место в буфере, возвращается JET_errInvalidBufferSize и данные столбца не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="77fc1-140">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-141">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="77fc1-141">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="77fc1-142">Указанные параметры неизвестны или являются недопустимым сочетанием известных битовых параметров.</span><span class="sxs-lookup"><span data-stu-id="77fc1-142">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="77fc1-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="77fc1-144">Один или несколько указанных параметров неверны.</span><span class="sxs-lookup"><span data-stu-id="77fc1-144">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="77fc1-145">Это может произойти, если размер ретинфо. Кбструкт меньше, чем <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="77fc1-145">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="77fc1-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="77fc1-147">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="77fc1-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="77fc1-148"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="77fc1-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-149">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="77fc1-149">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="77fc1-150">Курсор не располагается на записи.</span><span class="sxs-lookup"><span data-stu-id="77fc1-150">The cursor is not positioned on a record.</span></span> <span data-ttu-id="77fc1-151">Это может произойти по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="77fc1-151">This can happen for many different reasons.</span></span> <span data-ttu-id="77fc1-152">Например, это произойдет, если курсор находится в данный момент после последней записи в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="77fc1-152">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="77fc1-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="77fc1-154">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="77fc1-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="77fc1-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="77fc1-156">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="77fc1-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-157">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="77fc1-157">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="77fc1-158">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="77fc1-158">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="77fc1-159"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="77fc1-159"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="77fc1-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="77fc1-161">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="77fc1-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-162">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="77fc1-162">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="77fc1-163">Не удалось получить значение полного столбца, так как размер данного буфера меньше размера столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-163">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77fc1-164">В случае успеха данные столбцов и размер столбца возвращаются в предоставленных буферах, описанных в разделе массив структур [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="77fc1-164">On success, columns data and column size are returned in provided buffers described in array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="77fc1-165">Если для *итагсекуенце* было задано значение 0 (ноль), чтобы указать, что вместо данных столбца требуется количество экземпляров многозначного поля, то число экземпляров многозначного столбца возвращается в самом поле *итагсекуенце* .</span><span class="sxs-lookup"><span data-stu-id="77fc1-165">If an *itagSequence* was set to 0 (zero) to indicate that the number of instances of a multi-valued field was desired instead of column data, then the number of instances of a multi-valued column is returned in the *itagSequence* field itself.</span></span> <span data-ttu-id="77fc1-166">Каждая структура [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) содержит поле ошибки, которое содержит предупреждения для извлекаемого столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-166">Each [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure has an error field that contains warnings for the column retrieved.</span></span> <span data-ttu-id="77fc1-167">Если столбец имеет **значение NULL** , то код ошибки будет установлен в JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="77fc1-167">If the column was **NULL** valued, then the error code will be set to JET_wrnColumnNull.</span></span>

<span data-ttu-id="77fc1-168">В случае сбоя положение курсора остается неизменным и данные не копируются в предоставленный буфер.</span><span class="sxs-lookup"><span data-stu-id="77fc1-168">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="77fc1-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77fc1-169">Remarks</span></span>

<span data-ttu-id="77fc1-170">**Жетретриевеколумнс** поддерживает одну функцию, которая не является [жетретриевеколумн](./jetretrievecolumn-function.md) .</span><span class="sxs-lookup"><span data-stu-id="77fc1-170">**JetRetrieveColumns** supports one feature that [JetRetrieveColumn](./jetretrievecolumn-function.md) does not.</span></span> <span data-ttu-id="77fc1-171">Это возможность получения количества экземпляров столбца с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="77fc1-171">This is the ability to retrieve the number of instances of a multi-valued column.</span></span> <span data-ttu-id="77fc1-172">Эта функция предназначена для того, чтобы приложение получало все значения столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-172">The purpose of this feature is to allow an application to retrieve all values of a column.</span></span> <span data-ttu-id="77fc1-173">Это можно сделать, сначала определив количество значений в столбце.</span><span class="sxs-lookup"><span data-stu-id="77fc1-173">This can be done by first determining the number of values that a column has.</span></span> <span data-ttu-id="77fc1-174">Затем их длину можно определить, вызвав **жетретриевеколумнс** еще раз с одной структурой [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) , выделенной для каждого значения, чтобы определить длину данных столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-174">Next, their lengths can be determined by calling **JetRetrieveColumns** again with one [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure allocated for each value to determine the length of column data.</span></span> <span data-ttu-id="77fc1-175">Это можно сделать, передав указатели **null**_пвдата_ с *кбмакс* 0 (нулем) и извлекая длину столбца в *кбактуал*.</span><span class="sxs-lookup"><span data-stu-id="77fc1-175">This can be done by passing **NULL**_pvData_ pointers with *cbMax* of 0 (zero) and retrieving the column length in *cbActual*.</span></span> <span data-ttu-id="77fc1-176">Третий и последний вызовы можно выполнить с выделенной памятью для данных значения столбца.</span><span class="sxs-lookup"><span data-stu-id="77fc1-176">The third and last call can be made with allocated memory for the column value data.</span></span>

<span data-ttu-id="77fc1-177">Если любой полученный столбец усекается из-за недостаточного размера буфера, API возвратит JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="77fc1-177">If any column retrieved is truncated due to an insufficient length buffer, then the API will return JET_wrnBufferTruncated.</span></span> <span data-ttu-id="77fc1-178">Однако другие ошибки, JET_wrnColumnNull возвращаются только в поле ошибки в [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="77fc1-178">However, other errors, JET_wrnColumnNull are returned only in the error field in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="77fc1-179">Это связано с тем, что приложения часто хотят убедиться, что все данные получены и возвращать эту ошибку из **жетретриевеколумнс** , что упрощает это понимание.</span><span class="sxs-lookup"><span data-stu-id="77fc1-179">The reason for this is that applications often want to ensure that all data has been retrieved and returning this error from **JetRetrieveColumns** facilitates this understanding.</span></span>

#### <a name="requirements"></a><span data-ttu-id="77fc1-180">Требования</span><span class="sxs-lookup"><span data-stu-id="77fc1-180">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-181"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="77fc1-181"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77fc1-182">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="77fc1-182">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-183"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="77fc1-183"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77fc1-184">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="77fc1-184">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-185"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="77fc1-185"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77fc1-186">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="77fc1-186">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77fc1-187"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="77fc1-187"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="77fc1-188">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="77fc1-188">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77fc1-189"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="77fc1-189"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="77fc1-190">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="77fc1-190">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="77fc1-191">См. также:</span><span class="sxs-lookup"><span data-stu-id="77fc1-191">See Also</span></span>

[<span data-ttu-id="77fc1-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="77fc1-192">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="77fc1-193">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="77fc1-193">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="77fc1-194">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="77fc1-194">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="77fc1-195">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="77fc1-195">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="77fc1-196">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="77fc1-196">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="77fc1-197">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="77fc1-197">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="77fc1-198">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="77fc1-198">JetSetColumns</span></span>](./jetsetcolumns-function.md)
