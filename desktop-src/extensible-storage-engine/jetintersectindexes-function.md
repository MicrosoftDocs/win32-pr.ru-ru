---
description: Дополнительные сведения о функции Жетинтерсектиндексес
title: Функция JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692125"
---
# <a name="jetintersectindexes-function"></a><span data-ttu-id="c7123-103">Функция JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="c7123-103">JetIntersectIndexes Function</span></span>


<span data-ttu-id="c7123-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c7123-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetintersectindexes-function"></a><span data-ttu-id="c7123-105">Функция JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="c7123-105">JetIntersectIndexes Function</span></span>

<span data-ttu-id="c7123-106">Функция **жетинтерсектиндексес** вычислит пересечение между несколькими наборами записей индекса из разных вторичных индексов в одной таблице.</span><span class="sxs-lookup"><span data-stu-id="c7123-106">The **JetIntersectIndexes** function computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="c7123-107">Эта операция полезна для поиска набора записей в таблице, соответствующих двум или более критериям, которые могут быть выражены с помощью диапазонов индексов.</span><span class="sxs-lookup"><span data-stu-id="c7123-107">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span>

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c7123-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7123-108">Parameters</span></span>

<span data-ttu-id="c7123-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="c7123-109">*sesid*</span></span>

<span data-ttu-id="c7123-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c7123-110">The session to use for this call.</span></span>

<span data-ttu-id="c7123-111">*ргиндексранже*</span><span class="sxs-lookup"><span data-stu-id="c7123-111">*rgindexrange*</span></span>

<span data-ttu-id="c7123-112">Указатель на массив структур [JET_IndexRange](./jet-indexrange-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c7123-112">A pointer to an array of [JET_IndexRange](./jet-indexrange-structure.md) structures.</span></span> <span data-ttu-id="c7123-113">Каждая структура включает [JET_TABLEID](./jet-tableid.md) , для которой настроено удержание одного из диапазонов индексов для пересечение.</span><span class="sxs-lookup"><span data-stu-id="c7123-113">Each structure includes a [JET_TABLEID](./jet-tableid.md) that has been set up to hold one of the index ranges to be intersected.</span></span> <span data-ttu-id="c7123-114">Дополнительные сведения см. в разделе [JET_IndexRange](./jet-indexrange-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c7123-114">For more information, see [JET_IndexRange](./jet-indexrange-structure.md).</span></span>

<span data-ttu-id="c7123-115">*Циндексранже*</span><span class="sxs-lookup"><span data-stu-id="c7123-115">*cindexrange*</span></span>

<span data-ttu-id="c7123-116">Число структур [JET_IndexRange](./jet-indexrange-structure.md) в массиве, которое содержится в параметре *ргиндексранже* .</span><span class="sxs-lookup"><span data-stu-id="c7123-116">The number of [JET_IndexRange](./jet-indexrange-structure.md) structures in the array that is contained in the *rgindexrange* parameter.</span></span>

<span data-ttu-id="c7123-117">*прекордлист*</span><span class="sxs-lookup"><span data-stu-id="c7123-117">*precordlist*</span></span>

<span data-ttu-id="c7123-118">Указатель на структуру [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c7123-118">Pointer to a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="c7123-119">Эта структура будет заполнена достаточной информацией для обхода временной таблицы с результатами **жетинтерсектиндексес**.</span><span class="sxs-lookup"><span data-stu-id="c7123-119">This structure will be populated with enough information to traverse the temporary table with the results from **JetIntersectIndexes**.</span></span>

<span data-ttu-id="c7123-120">Выходной буфер, который получает структуру [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c7123-120">The output buffer that receives a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="c7123-121">Структура содержит описание результирующего набора пересечения.</span><span class="sxs-lookup"><span data-stu-id="c7123-121">The structure contains a description of the result set of the intersection.</span></span>

<span data-ttu-id="c7123-122">*грбит*</span><span class="sxs-lookup"><span data-stu-id="c7123-122">*grbit*</span></span>

<span data-ttu-id="c7123-123">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="c7123-123">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="c7123-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7123-124">Return Value</span></span>

<span data-ttu-id="c7123-125">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="c7123-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c7123-126">Дополнительные сведения об ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c7123-126">For more information about ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7123-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c7123-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="c7123-128">Описание</span><span class="sxs-lookup"><span data-stu-id="c7123-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7123-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c7123-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c7123-130">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c7123-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c7123-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c7123-132">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="c7123-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c7123-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c7123-134">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="c7123-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c7123-135"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7123-135"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-136">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="c7123-136">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="c7123-137">Один из запрошенных параметров недопустим, используется неправильно или не реализован.</span><span class="sxs-lookup"><span data-stu-id="c7123-137">One of the options requested was invalid, used incorrectly, or not implemented.</span></span></p>
<p><span data-ttu-id="c7123-138">Эта ошибка возвращается функцией <strong>жетинтерсектиндексес</strong> , когда:</span><span class="sxs-lookup"><span data-stu-id="c7123-138">This error is returned by <strong>JetIntersectIndexes</strong> when:</span></span></p>
<p><span data-ttu-id="c7123-139"><em>Грбит</em> , содержащийся в структуре <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> , на которую указывает любой элемент в массиве <em>ргиндексранже</em> , не равно JET_bitRecordInIndex.</span><span class="sxs-lookup"><span data-stu-id="c7123-139">The <em>grbit</em> contained in the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure pointed to by any element in the <em>rgindexrange</em> array is not equal to JET_bitRecordInIndex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-140">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c7123-140">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c7123-141">Один из указанных параметров содержит непредвиденное значение или значение, которое не согласуется при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="c7123-141">One of the parameters provided contains an unexpected value or a value that is inconsistent when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="c7123-142">Эта ошибка возвращается <strong>жетинтерсектиндексес</strong> по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="c7123-142">This error is returned by <strong>JetIntersectIndexes</strong> for of the following reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="c7123-143">Параметр <em>прекордлист</em> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="c7123-143">The <em>precordlist</em> parameter is NULL.</span></span></p></li>
<li><p><span data-ttu-id="c7123-144">Элемент <strong>кбструкт</strong> структуры <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> , указанный в параметре <em>прекордлист</em> , не равен размеру структуры <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="c7123-144">The <strong>cbStruct</strong> member of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure specified in the <em>precordlist</em> parameter is not equal to size of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="c7123-145">Параметр <em>Циндексранже</em> равен нулю.</span><span class="sxs-lookup"><span data-stu-id="c7123-145">The <em>cindexrange</em> parameter is zero.</span></span></p></li>
<li><p><span data-ttu-id="c7123-146">Значение параметра <em>Циндексранже</em> больше 64.</span><span class="sxs-lookup"><span data-stu-id="c7123-146">The <em>cindexrange</em> parameter is greater than 64.</span></span></p></li>
<li><p><span data-ttu-id="c7123-147">Элемент <strong>кбструкт</strong> для любого элемента в массиве, заданном параметром <em>ргиндексранже</em> , не равен размеру структуры <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</span><span class="sxs-lookup"><span data-stu-id="c7123-147">The <strong>cbStruct</strong> member for any element in the array specified by the <em>rgindexrange</em> parameter is not equal to the size of the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="c7123-148">Элементы в массиве <em>ргиндексранже</em> содержат <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s из разных таблиц.</span><span class="sxs-lookup"><span data-stu-id="c7123-148">The elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s from different tables.</span></span></p></li>
<li><p><span data-ttu-id="c7123-149">Элемент в массиве <em>ргиндексранже</em> содержит <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> , который не позиционирован на вторичном индексе.</span><span class="sxs-lookup"><span data-stu-id="c7123-149">An element in the <em>rgindexrange</em> array contains a <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> that is not positioned on a secondary index.</span></span></p></li>
<li><p><span data-ttu-id="c7123-150">Один или несколько элементов в массиве <em>ргиндексранже</em> содержат <a href="gg269182(v=exchg.10).md">JET_TABLEIDы</a>, расположенные на одном и том же вторичном индексе.</span><span class="sxs-lookup"><span data-stu-id="c7123-150">One or more of the elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s positioned on the same secondary index.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-151">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="c7123-151">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="c7123-152">Недопустимый обработчик сеанса или ссылается на закрытый сеанс.</span><span class="sxs-lookup"><span data-stu-id="c7123-152">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="c7123-153">Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="c7123-153">This error is not returned under all circumstances.</span></span> <span data-ttu-id="c7123-154">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="c7123-154">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-155">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c7123-155">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c7123-156">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="c7123-156">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-157">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="c7123-157">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="c7123-158">Не удалось выполнить операцию, так как подсистеме не удалось выделить ресурсы, необходимые для открытия нового курсора.</span><span class="sxs-lookup"><span data-stu-id="c7123-158">The operation failed because the engine could not allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="c7123-159">Ресурсы курсора настраиваются путем вызова <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <em>JET_paramMaxCursors</em> , указанными в параметре <em>парамид</em> .</span><span class="sxs-lookup"><span data-stu-id="c7123-159">Cursor resources are configured by calling <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxCursors</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c7123-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="c7123-161">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="c7123-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="c7123-162"><strong>Жетинтерсектиндексес</strong> может возвращать JET_errOutOfMemory, если адресное пространство хост-процесса оказывается слишком фрагментированным.</span><span class="sxs-lookup"><span data-stu-id="c7123-162"><strong>JetIntersectIndexes</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="c7123-163">Временный диспетчер таблиц всегда выделяет 1 МБ адресного пространства для каждой временной таблицы, созданной независимо от объема сохраняемых данных.</span><span class="sxs-lookup"><span data-stu-id="c7123-163">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span> <span data-ttu-id="c7123-164"><strong>Жетинтерсектиндексес</strong> создаст одну временную таблицу для каждого <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> , указанного в параметре <em>ргиндексранже</em> , и одну временную таблицу для выходных данных в <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="c7123-164"><strong>JetIntersectIndexes</strong> will create one temporary table for each <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specified in the <em>rgindexrange</em> parameter, and one temporary table for the output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c7123-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c7123-166">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="c7123-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c7123-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c7123-168">Нельзя одновременно использовать один сеанс из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="c7123-168">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c7123-169"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7123-169"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c7123-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c7123-171">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="c7123-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-172">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="c7123-172">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="c7123-173">Не удалось выполнить операцию, так как подсистеме не удалось выделить ресурсы, необходимые для кэширования индексов таблицы.</span><span class="sxs-lookup"><span data-stu-id="c7123-173">The operation failed because the engine could not allocate the resources required to cache the indices of the table.</span></span> <span data-ttu-id="c7123-174">Количество индексов, схема которых может быть кэширована, настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <em>JET_paramMaxOpenTables</em> , указанными в параметре <em>парамид</em> .</span><span class="sxs-lookup"><span data-stu-id="c7123-174">The number of indices whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-175">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="c7123-175">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="c7123-176">Не удалось выполнить операцию, так как подсистеме не удалось выделить ресурсы, необходимые для кэширования схемы таблицы.</span><span class="sxs-lookup"><span data-stu-id="c7123-176">The operation failed because the engine could not allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="c7123-177">Количество таблиц, схема которых может быть кэширована, настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <em>JET_paramMaxOpenTables</em> , указанными в параметре <em>парамид</em> .</span><span class="sxs-lookup"><span data-stu-id="c7123-177">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-178">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="c7123-178">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="c7123-179">Не удалось выполнить операцию, так как подсистеме не удалось выделить ресурсы, необходимые для создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="c7123-179">The operation failed because the engine could not allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="c7123-180">Временные ресурсы таблицы настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с JET_paramMaxTemporaryTables, указанными в параметре <em>парамид</em> .</span><span class="sxs-lookup"><span data-stu-id="c7123-180">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with JET_paramMaxTemporaryTables specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7123-181">При успешном выполнении возвращается новая временная таблица, содержащая закладки записей, которые соответствуют критериям, представленным в описаниях диапазона входных индексов.</span><span class="sxs-lookup"><span data-stu-id="c7123-181">On success, a new temporary table is returned that contains the bookmarks of the records that match the criteria represented by each of the input index range descriptions.</span></span>

<span data-ttu-id="c7123-182">При сбое временная таблица, содержащая результаты, не будет создана.</span><span class="sxs-lookup"><span data-stu-id="c7123-182">On failure, the temporary table containing the results will not be created.</span></span> <span data-ttu-id="c7123-183">Состояние временной базы данных может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="c7123-183">The state of the temporary database may be changed.</span></span> <span data-ttu-id="c7123-184">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="c7123-184">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span> <span data-ttu-id="c7123-185">Текущее расположение [JET_TABLEID](./jet-tableid.md)s, предоставленное этой функции, может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="c7123-185">The current position of the [JET_TABLEID](./jet-tableid.md)s provided to this function may be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c7123-186">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7123-186">Remarks</span></span>

<span data-ttu-id="c7123-187">**Жетинтерсектиндексес** можно использовать для эффективной фильтрации записей в таблице по нескольким критериям, если эти критерии могут быть выражены в виде вторичных индексов по этой таблице.</span><span class="sxs-lookup"><span data-stu-id="c7123-187">**JetIntersectIndexes** can be used to efficiently filter the records in a table by multiple criteria if those criteria can be expressed in terms of the secondary indices over that table.</span></span> <span data-ttu-id="c7123-188">Например, предположим, что у вас есть очень большая таблица, содержащая людей.</span><span class="sxs-lookup"><span data-stu-id="c7123-188">For example, consider that you have a very large table containing people.</span></span> <span data-ttu-id="c7123-189">Таблица может содержать столбцы с идентификатором пользователя, именем, фамилией и т. д.</span><span class="sxs-lookup"><span data-stu-id="c7123-189">The table can have columns for their user id, first name, last name, and so on.</span></span> <span data-ttu-id="c7123-190">Предположим, что каждый из этих столбцов индексируется отдельно и первичный индекс таблицы находится по идентификатору пользователя. Если вы хотите найти всех, чье имя начинается с A, а фамилия начинается с G, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c7123-190">Suppose that each of these columns is indexed separately and that the primary index of the table is over user id. If you wanted to find everyone whose first name starts with an A and whose last name starts with G, you would perform the following steps:</span></span>

1.  <span data-ttu-id="c7123-191">Откройте новый курсор в таблице и установите этот курсор для использования индекса над столбцом First Name.</span><span class="sxs-lookup"><span data-stu-id="c7123-191">Open a new cursor on the table, and set that cursor to use the index over the "first name" column.</span></span> <span data-ttu-id="c7123-192">Затем настройте диапазон индексов для всех пользователей, "имя" которых начинается с "A", и создайте [JET_IndexRange](./jet-indexrange-structure.md) структуру, содержащую этот курсор.</span><span class="sxs-lookup"><span data-stu-id="c7123-192">Then setup an index range for all people whose "first name" started with 'A', and build a [JET_IndexRange](./jet-indexrange-structure.md) struct that contains this cursor.</span></span>

2.  <span data-ttu-id="c7123-193">Повторите шаг 1 с новым курсором в индексе Last Name для всех пользователей, чье поле Last Name было запущено с "G".</span><span class="sxs-lookup"><span data-stu-id="c7123-193">Repeat step 1 with a new cursor on the "last name" index for all people whose "last name" started with 'G'.</span></span>

3.  <span data-ttu-id="c7123-194">Передайте эти критерии в **жетинтерсектиндексес** , чтобы вычислить результат во временную таблицу.</span><span class="sxs-lookup"><span data-stu-id="c7123-194">Pass these criteria to **JetIntersectIndexes** to compute the result into a temporary table.</span></span>

4.  <span data-ttu-id="c7123-195">Просмотрите временную таблицу и извлеките каждую из записей, которые передают критерии по закладке.</span><span class="sxs-lookup"><span data-stu-id="c7123-195">Traverse the temporary table and retrieve each of the records that pass the criteria by bookmark.</span></span>

<span data-ttu-id="c7123-196">Временная таблица, содержащая результирующий набор, представляет собой простую таблицу с одним столбцом, содержащим закладку каждой записи, которая передала все критерии, используемые для вычисления пересечения.</span><span class="sxs-lookup"><span data-stu-id="c7123-196">The temporary table containing the result set is a simple table with one column that contains the bookmark of each record that passed all the criteria used to compute the intersection.</span></span> <span data-ttu-id="c7123-197">Результирующий набор сортируется в том же порядке, что и первичный индекс, и не содержит повторяющихся записей.</span><span class="sxs-lookup"><span data-stu-id="c7123-197">The result set is sorted in the same order as the primary index and contains no duplicate entries.</span></span> <span data-ttu-id="c7123-198">Приложение может перечислить результаты пересечения, перечисляя строки во временной таблице, извлекая закладку для каждого результата с помощью [жетретриевеколумн](./jetretrievecolumn-function.md), а затем просмотрев запись в базе данных, вызывая [жетготобукмарк](./jetgotobookmark-function.md) с этой закладкой для курсора, расположенного на первичном индексе.</span><span class="sxs-lookup"><span data-stu-id="c7123-198">The application can enumerate the results of the intersection by enumerating the rows in the temporary table, retrieving the bookmark for each result using [JetRetrieveColumn](./jetretrievecolumn-function.md), and then visiting the record in the database by calling [JetGotoBookmark](./jetgotobookmark-function.md) with that bookmark on a cursor positioned on the primary index.</span></span>

<span data-ttu-id="c7123-199">Временная таблица, возвращаемая функцией **жетинтерсектиндексес** , может быть проверена только в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="c7123-199">The temporary table returned by **JetIntersectIndexes** can only be scanned in a forward direction.</span></span> <span data-ttu-id="c7123-200">Он также должен быть закрыт через [жетклосетабле](./jetclosetable-function.md) после завершения проверки.</span><span class="sxs-lookup"><span data-stu-id="c7123-200">It should also be closed via [JetCloseTable](./jetclosetable-function.md) when the scan has been completed.</span></span> <span data-ttu-id="c7123-201">Дополнительные сведения о временных таблицах и их работе см. в разделе [жетопентемпораритабле](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="c7123-201">For more information about temporary tables and how they work, see [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

<span data-ttu-id="c7123-202">**Жетинтерсектиндексес** обычно является эффективным и удобным способом фильтрации записей на основе нескольких индексированных критериев.</span><span class="sxs-lookup"><span data-stu-id="c7123-202">**JetIntersectIndexes** is generally an efficient and convenient way to filter records based on multiple indexed criteria.</span></span> <span data-ttu-id="c7123-203">Однако есть несколько важных советов, которые следует выполнить, чтобы максимально увеличить полезность этой функции.</span><span class="sxs-lookup"><span data-stu-id="c7123-203">However, there are some important tips that should be followed to maximize the usefulness of this feature.</span></span> <span data-ttu-id="c7123-204">Если известно, что один из критериев имеет настолько строгое значение, что результирующий диапазон индексов содержит очень мало записей, то, вероятно, лучше просто проанализировать диапазон индексов и отфильтровать записи на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="c7123-204">If you know that one of the criteria is so restrictive that the resulting index range has very few records then it is probably better to simply walk that index range and filter the records at the application level.</span></span> <span data-ttu-id="c7123-205">Кроме того, если известно, что у вас есть условия, которые гораздо менее точны, чем другие критерии пересечения, можно удалить эти менее четкие критерии из пересечения.</span><span class="sxs-lookup"><span data-stu-id="c7123-205">Further, if you know that you have criteria that are much less restrictive than other criteria in your intersection then you might consider dropping those much less restrictive criteria from the intersection.</span></span> <span data-ttu-id="c7123-206">Наконец, если известно, что один из критериев не является настолько ограничивающим, что результирующий диапазон индекса почти такой же большой, как и первичный индекс, маловероятно, что при пересечении с этим диапазоном индексов будет преимущество (уменьшение размера) результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="c7123-206">Finally, if you know that one of the criteria is not at all restrictive such that the resulting index range is almost as large as the primary index then it is unlikely that intersecting with that index range will benefit (reduce the size of) the result set.</span></span> <span data-ttu-id="c7123-207">Во всех случаях следует выбирать условия таким образом, чтобы на входе можно было выбрать наименьшее количество возможных записей индекса и создать наиболее конкретный набор закладок на выходе для максимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="c7123-207">In all cases, you should be selecting criteria in a manner that will take the fewest possible index entries on input and generate the most specific set of bookmarks on output for maximum performance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c7123-208">Требования</span><span class="sxs-lookup"><span data-stu-id="c7123-208">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7123-209"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c7123-209"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c7123-210">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c7123-210">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-211"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c7123-211"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c7123-212">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c7123-212">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-213"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c7123-213"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c7123-214">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c7123-214">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7123-215"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="c7123-215"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c7123-216">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c7123-216">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7123-217"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="c7123-217"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c7123-218">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c7123-218">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c7123-219">См. также:</span><span class="sxs-lookup"><span data-stu-id="c7123-219">See Also</span></span>

[<span data-ttu-id="c7123-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c7123-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c7123-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c7123-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c7123-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c7123-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c7123-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c7123-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c7123-224">JET_IndexRange</span><span class="sxs-lookup"><span data-stu-id="c7123-224">JET_IndexRange</span></span>](./jet-indexrange-structure.md)  
[<span data-ttu-id="c7123-225">JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="c7123-225">JET_RECORDLIST</span></span>](./jet-recordlist-structure.md)  
[<span data-ttu-id="c7123-226">жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="c7123-226">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="c7123-227">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="c7123-227">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="c7123-228">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="c7123-228">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
