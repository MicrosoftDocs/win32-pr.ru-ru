---
description: Дополнительные сведения о функции Жетмове
title: Функция JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262862"
---
# <a name="jetmove-function"></a><span data-ttu-id="d58ae-103">Функция JetMove</span><span class="sxs-lookup"><span data-stu-id="d58ae-103">JetMove Function</span></span>


<span data-ttu-id="d58ae-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d58ae-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetmove-function"></a><span data-ttu-id="d58ae-105">Функция JetMove</span><span class="sxs-lookup"><span data-stu-id="d58ae-105">JetMove Function</span></span>

<span data-ttu-id="d58ae-106">Функция **жетмове** размещает курсор в начале или в конце индекса и перебирает записи в этом индексе вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="d58ae-106">The **JetMove** function positions a cursor at the start or end of an index and traverses the entries in that index either forward or backward.</span></span> <span data-ttu-id="d58ae-107">Можно также переместить курсор вперед или назад по текущему индексу на указанное число записей индекса.</span><span class="sxs-lookup"><span data-stu-id="d58ae-107">It is also possible to move the cursor forward or backward on the current index by a specified number of index entries.</span></span> <span data-ttu-id="d58ae-108">Другой подход заключается в искусственном ограничении записей индекса, которые можно перечислить с помощью **жетмове** , настроив диапазон индексов в курсоре с помощью [жетсетиндексранже](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="d58ae-108">Another approach is to artificially limit the index entries that can be enumerated using **JetMove** by setting up an index range on the cursor using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d58ae-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d58ae-109">Parameters</span></span>

<span data-ttu-id="d58ae-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="d58ae-110">*sesid*</span></span>

<span data-ttu-id="d58ae-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="d58ae-111">The session to use for this call.</span></span>

<span data-ttu-id="d58ae-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d58ae-112">*tableid*</span></span>

<span data-ttu-id="d58ae-113">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="d58ae-113">The cursor to use for this call.</span></span>

<span data-ttu-id="d58ae-114">*CRowset*</span><span class="sxs-lookup"><span data-stu-id="d58ae-114">*cRow*</span></span>

<span data-ttu-id="d58ae-115">Произвольное смещение, которое указывает нужное перемещение курсора в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="d58ae-115">An arbitrary offset that indicates the desired movement of the cursor on the current index.</span></span>

<span data-ttu-id="d58ae-116">Помимо стандартных смещений этот параметр также можно задать с помощью одного из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="d58ae-116">In addition to standard offsets, this parameter can also be set with one of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d58ae-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d58ae-117">Value</span></span></p></th>
<th><p><span data-ttu-id="d58ae-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d58ae-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-119">JET_MoveFirst</span><span class="sxs-lookup"><span data-stu-id="d58ae-119">JET_MoveFirst</span></span></p></td>
<td><p><span data-ttu-id="d58ae-120">Перемещает курсор к первой записи индекса в индексе (если она существует).</span><span class="sxs-lookup"><span data-stu-id="d58ae-120">Moves the cursor to the first index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="d58ae-121"><strong>Примечание</strong>   .   Для обозначения этого параметра используется литеральное значение-2147483648.</span><span class="sxs-lookup"><span data-stu-id="d58ae-121"><strong>Note</strong>   The literal value of -2147483648 is used to denote this option.</span></span> <span data-ttu-id="d58ae-122">Не используйте это значение в качестве обычного смещения или непредвиденного поведения.</span><span class="sxs-lookup"><span data-stu-id="d58ae-122">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d58ae-123">JET_MoveLast</span><span class="sxs-lookup"><span data-stu-id="d58ae-123">JET_MoveLast</span></span></p></td>
<td><p><span data-ttu-id="d58ae-124">Перемещает курсор к последнему элементу индекса в индексе (если он существует).</span><span class="sxs-lookup"><span data-stu-id="d58ae-124">Moves the cursor to the last index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="d58ae-125"><strong>Примечание</strong>   .   Для обозначения этого параметра используется литеральное значение 2147483647.</span><span class="sxs-lookup"><span data-stu-id="d58ae-125"><strong>Note</strong>   The literal value of 2147483647 is used to denote this option.</span></span> <span data-ttu-id="d58ae-126">Не используйте это значение в качестве обычного смещения или непредвиденного поведения.</span><span class="sxs-lookup"><span data-stu-id="d58ae-126">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-127">JET_MoveNext</span><span class="sxs-lookup"><span data-stu-id="d58ae-127">JET_MoveNext</span></span></p></td>
<td><p><span data-ttu-id="d58ae-128">Перемещает курсор к следующей записи индекса в индексе (если она существует).</span><span class="sxs-lookup"><span data-stu-id="d58ae-128">Moves the cursor to the next index entry in the index (if one exists).</span></span> <span data-ttu-id="d58ae-129">Это значение точно равно обычному смещению + 1.</span><span class="sxs-lookup"><span data-stu-id="d58ae-129">This value is exactly equal to an ordinary offset of +1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d58ae-130">JET_MovePrevious</span><span class="sxs-lookup"><span data-stu-id="d58ae-130">JET_MovePrevious</span></span></p></td>
<td><p><span data-ttu-id="d58ae-131">Перемещает курсор к предыдущему элементу индекса в индексе (если он существует).</span><span class="sxs-lookup"><span data-stu-id="d58ae-131">Moves the cursor to the previous index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="d58ae-132">Это значение точно равно обычному смещению-1, или 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="d58ae-132">This value is exactly equal to an ordinary offset of -1, or 0 (Zero).</span></span></p>
<p><span data-ttu-id="d58ae-133">Курсор остается в текущей логической позиции, и существует запись индекса, соответствующая логической позиции, которая будет протестирована.</span><span class="sxs-lookup"><span data-stu-id="d58ae-133">The cursor remains at the current logical position and the existence of the index entry that corresponds to that logical position will be tested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d58ae-134">*грбит*</span><span class="sxs-lookup"><span data-stu-id="d58ae-134">*grbit*</span></span>

<span data-ttu-id="d58ae-135">Группа битов, задающих ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="d58ae-135">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d58ae-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d58ae-136">Value</span></span></p></th>
<th><p><span data-ttu-id="d58ae-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d58ae-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-138">JET_bitMoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="d58ae-138">JET_bitMoveKeyNE</span></span></p></td>
<td><p><span data-ttu-id="d58ae-139">Перемещает курсор вперед или назад по количеству записей индекса, необходимых для пропуска запрошенного количества значений ключа индекса, обнаруженных в индексе.</span><span class="sxs-lookup"><span data-stu-id="d58ae-139">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="d58ae-140">Это влияет на свертывание записей индекса с повторяющимися значениями ключа в одну запись индекса.</span><span class="sxs-lookup"><span data-stu-id="d58ae-140">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span> <span data-ttu-id="d58ae-141">Как правило, смещение перемещает курсор на указанное число записей индекса независимо от их значений ключей.</span><span class="sxs-lookup"><span data-stu-id="d58ae-141">Ordinarily, an offset will move the cursor by the specified number of index entries regardless of their key values.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d58ae-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d58ae-142">Return Value</span></span>

<span data-ttu-id="d58ae-143">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="d58ae-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d58ae-144">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d58ae-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d58ae-145">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d58ae-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="d58ae-146">Описание</span><span class="sxs-lookup"><span data-stu-id="d58ae-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d58ae-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d58ae-148">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d58ae-148">The operation completed successfully.</span></span> <span data-ttu-id="d58ae-149">Для <strong>жетмове</strong>это означает, что запись индекса найдена в запрошенном расположении или смещении по текущему индексу.</span><span class="sxs-lookup"><span data-stu-id="d58ae-149">For <strong>JetMove</strong>, this means that an index entry was found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d58ae-150">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d58ae-150">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d58ae-151">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="d58ae-151">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-152">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d58ae-152">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d58ae-153">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="d58ae-153">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d58ae-154"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d58ae-154"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d58ae-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d58ae-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d58ae-156">Курсор не находится на элементе индекса в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d58ae-156">The cursor is not currently positioned on an index entry.</span></span> <span data-ttu-id="d58ae-157">Для <strong>жетмове</strong>это означает, что запись индекса не была найдена в запрошенном месте или смещении по текущему индексу.</span><span class="sxs-lookup"><span data-stu-id="d58ae-157">For <strong>JetMove</strong>, this means that an index entry was not found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d58ae-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d58ae-159">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="d58ae-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d58ae-160">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="d58ae-160">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="d58ae-161">Курсор в настоящее время логически позиционирован на записи индекса, соответствующей записи, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="d58ae-161">The cursor is currently logically positioned on an index entry that corresponds to a record that has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d58ae-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d58ae-163">Операция не может быть завершена, так как выполняется операция восстановления для экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="d58ae-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d58ae-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d58ae-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d58ae-165">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="d58ae-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d58ae-166"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d58ae-166"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d58ae-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d58ae-168">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="d58ae-168">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d58ae-169">Если эта функция завершится с ошибкой, курсор будет размещен в записи индекса, соответствующей запрошенному расположению или смещению.</span><span class="sxs-lookup"><span data-stu-id="d58ae-169">If this function succeeds, the cursor will be positioned at an index entry that matches the requested location or offset.</span></span> <span data-ttu-id="d58ae-170">Если запись подготовлена к обновлению, это обновление будет отменено.</span><span class="sxs-lookup"><span data-stu-id="d58ae-170">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="d58ae-171">Если диапазон индекса действует, а JET_MoveFirst или JET_MoveLast был указан, то этот диапазон индексов будет отменен.</span><span class="sxs-lookup"><span data-stu-id="d58ae-171">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="d58ae-172">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d58ae-172">No change to the database state will occur.</span></span>

<span data-ttu-id="d58ae-173">Если эта функция завершается ошибкой, то позицию курсора остается неизменной, если не было возвращено JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="d58ae-173">If this function fails, the position of the cursor will remain unchanged unless JET_errNoCurrentRecord was returned.</span></span> <span data-ttu-id="d58ae-174">В этом случае курсор будет размещен в том месте, где находится запись индекса, соответствующая запрошенному расположению или смещению.</span><span class="sxs-lookup"><span data-stu-id="d58ae-174">In that case, the cursor will be positioned where the index entry that matches the requested location or offset would have been.</span></span> <span data-ttu-id="d58ae-175">Курсор может быть перемещен относительно этой позиции, но по-прежнему не находится в допустимой записи индекса.</span><span class="sxs-lookup"><span data-stu-id="d58ae-175">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="d58ae-176">Если запись подготовлена к обновлению, это обновление будет отменено.</span><span class="sxs-lookup"><span data-stu-id="d58ae-176">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="d58ae-177">Если диапазон индекса действует, а JET_MoveFirst или JET_MoveLast был указан, то этот диапазон индексов будет отменен.</span><span class="sxs-lookup"><span data-stu-id="d58ae-177">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="d58ae-178">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d58ae-178">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d58ae-179">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d58ae-179">Remarks</span></span>

<span data-ttu-id="d58ae-180">Курсор можно переместить в две специальные позиции с помощью **жетмове**, до первого и после последнего.</span><span class="sxs-lookup"><span data-stu-id="d58ae-180">A cursor can be moved to two special positions using **JetMove**, Before First and After Last.</span></span> <span data-ttu-id="d58ae-181">Если курсор находится на первой записи индекса в таблице, а **жетмове** вызывается с JET_MovePrevious, вызов завершится с JET_errNoCurrentRecord и курсор будет логически размещается перед первой записью в индексе.</span><span class="sxs-lookup"><span data-stu-id="d58ae-181">If the cursor is on the first index entry in the table and **JetMove** is called with JET_MovePrevious, the call will fail with JET_errNoCurrentRecord and the cursor will be logically positioned before the first entry in the index.</span></span> <span data-ttu-id="d58ae-182">Эта логическая позиция сохраняется, даже если другая запись индекса вставляется до первой записи в индексе.</span><span class="sxs-lookup"><span data-stu-id="d58ae-182">This logical position is maintained even if another index entry is inserted prior to the first entry in the index.</span></span> <span data-ttu-id="d58ae-183">Аналогичная ситуация возникает в конце индекса после последней относительных событий.</span><span class="sxs-lookup"><span data-stu-id="d58ae-183">An analogous situation occurs for After Last relative to the end of the index.</span></span> <span data-ttu-id="d58ae-184">До первого и после последнего наиболее удобного использования при настройке диапазона элементов индекса для итерации с помощью **жетмове**, используя модель итератора, которая должна всегда перемещаться к следующему (или предыдущему) элементу перед использованием этого элемента.</span><span class="sxs-lookup"><span data-stu-id="d58ae-184">Before First and After Last are most useful when setting up a range of index entries to be iterated using **JetMove**, using an iterator model that expects to always move to the next (or previous) element prior to using that element.</span></span>

<span data-ttu-id="d58ae-185">Набор записей индекса, которые могут быть просмотрены **жетмове** , можно ограничить, настроив диапазон индексов в курсоре.</span><span class="sxs-lookup"><span data-stu-id="d58ae-185">The set of index entries that can be visited by **JetMove** can be limited by setting up an index range on the cursor.</span></span> <span data-ttu-id="d58ae-186">Это полезно для приложений, которые перечисляют набор записей индекса, соответствующих простым критериям, которые могут быть выражены с помощью пары ключей поиска, созданных для этого индекса.</span><span class="sxs-lookup"><span data-stu-id="d58ae-186">This is useful for applications that enumerate a set of index entries that match simple criteria that can be expressed through a pair of search keys built for that index.</span></span> <span data-ttu-id="d58ae-187">Дополнительные сведения см. в разделе [жетсетиндексранже](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="d58ae-187">For more information, see [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="d58ae-188">В выпусках до Windows Server 2003 с пакетом обновления 1 (SP1) существует проблема **жетмове** , которая возникает в некоторых специфических случаях, что влияет на правильное применение диапазона индексов, установленного функцией [жетсетиндексранже](./jetsetindexrange-function.md) .</span><span class="sxs-lookup"><span data-stu-id="d58ae-188">On releases prior to Windows Server 2003 SP1, there is a problem in **JetMove** that occurs in some specific cases, that affects the correct enforcement of an index range as set up by the [JetSetIndexRange](./jetsetindexrange-function.md) function.</span></span> <span data-ttu-id="d58ae-189">Если курсор находится перед первой записью индекса, а диапазон индексов задан с верхним пределом, которое меньше, чем первая запись индекса, следующий вызов **жетмове** будет ошибочно переходить к этой записи индекса вместо сбоя с JET_errNoCurrentRecord, как и ожидалось.</span><span class="sxs-lookup"><span data-stu-id="d58ae-189">If the cursor is currently before the first index entry and an index range is set with an upper limit that is less than the first index entry, the next call to **JetMove** will erroneously go to that index entry instead of failing with JET_errNoCurrentRecord, as expected.</span></span> <span data-ttu-id="d58ae-190">Такая же ошибка произойдет в случае аналогичной ситуации, начиная с конца индекса.</span><span class="sxs-lookup"><span data-stu-id="d58ae-190">The same error will happen for the analogous situation starting from the end of the index.</span></span> <span data-ttu-id="d58ae-191">Такая ситуация может возникнуть в приложении, которое настраивает диапазон индексов и осуществляет переход к нему с помощью итератора, который должен запускаться перед первой записью индекса, которая является членом набора записей для перечисления, а не начиная с первой записи индекса этого набора.</span><span class="sxs-lookup"><span data-stu-id="d58ae-191">This situation can occur in an application that sets up an index range and navigates it using an iterator that expects to start before the first index entry that is a member of the set of entries to enumerate, rather than starting on the first index entry of that set.</span></span> <span data-ttu-id="d58ae-192">Эта ситуация также возникает в аналогичном случае, начиная с конца индекса.</span><span class="sxs-lookup"><span data-stu-id="d58ae-192">This situation also occurs on the analogous case starting from the end of the index.</span></span> <span data-ttu-id="d58ae-193">Решение заключается в том, чтобы приложение вручную проверяло, что полученная запись индекса находится внутри диапазона индексов, сравнивая ключ текущей записи индекса (полученный с помощью [жетретриевекэй](./jetretrievekey-function.md)) с ключом, представляющим конец текущего диапазона индекса (полученный с помощью [жетретриевекэй](./jetretrievekey-function.md) с помощью JET_bitRetrieveCopy).</span><span class="sxs-lookup"><span data-stu-id="d58ae-193">The workaround is for the application to manually verify that the index entry acquired is inside the index range by comparing the key for the current index entry (retrieved using [JetRetrieveKey](./jetretrievekey-function.md)) with the key representing the end of the current index range (retrieved using [JetRetrieveKey](./jetretrievekey-function.md) using JET_bitRetrieveCopy).</span></span>

<span data-ttu-id="d58ae-194">Важно соблюдать осторожность при передаче вычисленных смещений в **жетмове**.</span><span class="sxs-lookup"><span data-stu-id="d58ae-194">It is important to be careful when passing computed offsets to **JetMove**.</span></span> <span data-ttu-id="d58ae-195">Если вычисленное смещение меньше или равно JET_MoveFirst, то это смещение должно разбиваться на несколько частей, каждый из которых передается в **жетмове** отдельно, но в рамках одной транзакции, чтобы получить нужный результат.</span><span class="sxs-lookup"><span data-stu-id="d58ae-195">If the computed offset is less than or equal to JET_MoveFirst, that offset must be broken up into multiple pieces, each of which is passed to **JetMove** separately but within a single transaction to get the desired effect.</span></span> <span data-ttu-id="d58ae-196">То же самое справедливо и для смещений, которые больше или равны JET_MoveNext.</span><span class="sxs-lookup"><span data-stu-id="d58ae-196">The same is true for offsets greater than or equal to JET_MoveNext.</span></span> <span data-ttu-id="d58ae-197">Маловероятно, что приложение будет передано в реальном мире, но при этом полезно иметь защиту от этого случая, учитывая очень другую семантику JET_MoveFirst и JET_MoveLast из обычного смещения.</span><span class="sxs-lookup"><span data-stu-id="d58ae-197">It is unlikely that an application would undergo this in the real world, but it is good to have a defense against this case given the very different semantics of JET_MoveFirst and JET_MoveLast from an ordinary offset.</span></span>

<span data-ttu-id="d58ae-198">Когда **жетмове** вызывается с очень большим смещением, например если для параметра CRowset задано значение 1000, **жетмове** проходит все 1000 записей индекса для достижения конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="d58ae-198">When **JetMove** is called with a very large offset, such as when the cRow parameter is set to 1000, **JetMove** traverses all 1000 index entries to reach the final position.</span></span> <span data-ttu-id="d58ae-199">В настоящее время API-интерфейс ESE не предоставляет эффективный способ перемещения непосредственно к заданной записи индекса по смещению, не продвигаясь по каждой записи индекса.</span><span class="sxs-lookup"><span data-stu-id="d58ae-199">Currently, the ESE API does not provide an efficient way to move directly to a given index entry by offset without traversing each index entry.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d58ae-200">Требования</span><span class="sxs-lookup"><span data-stu-id="d58ae-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-201"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d58ae-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d58ae-202">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d58ae-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d58ae-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d58ae-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d58ae-204">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d58ae-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d58ae-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d58ae-206">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d58ae-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d58ae-207"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="d58ae-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d58ae-208">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d58ae-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d58ae-209"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="d58ae-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d58ae-210">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d58ae-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d58ae-211">См. также:</span><span class="sxs-lookup"><span data-stu-id="d58ae-211">See Also</span></span>

[<span data-ttu-id="d58ae-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d58ae-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d58ae-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d58ae-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d58ae-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d58ae-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d58ae-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d58ae-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d58ae-216">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="d58ae-216">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="d58ae-217">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="d58ae-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
