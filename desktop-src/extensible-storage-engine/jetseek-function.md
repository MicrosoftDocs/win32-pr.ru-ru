---
description: Дополнительные сведения о функции Жетсик
title: Функция Жетсик
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703083"
---
# <a name="jetseek-function"></a><span data-ttu-id="20167-103">Функция Жетсик</span><span class="sxs-lookup"><span data-stu-id="20167-103">JetSeek Function</span></span>


<span data-ttu-id="20167-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20167-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetseek-function"></a><span data-ttu-id="20167-105">Функция Жетсик</span><span class="sxs-lookup"><span data-stu-id="20167-105">JetSeek Function</span></span>

<span data-ttu-id="20167-106">Функция **жетсик** эффективно позиционирует курсор на запись индекса, которая соответствует условиям поиска, заданным в ключе поиска в этом курсоре, и заданному неравенству.</span><span class="sxs-lookup"><span data-stu-id="20167-106">The **JetSeek** function efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="20167-107">Ключ поиска должен быть ранее создан с помощью [жетмакекэй](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="20167-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="20167-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="20167-108">Parameters</span></span>

<span data-ttu-id="20167-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="20167-109">*sesid*</span></span>

<span data-ttu-id="20167-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="20167-110">The session to use for this call.</span></span>

<span data-ttu-id="20167-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="20167-111">*tableid*</span></span>

<span data-ttu-id="20167-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="20167-112">The cursor to use for this call.</span></span>

<span data-ttu-id="20167-113">*грбит*</span><span class="sxs-lookup"><span data-stu-id="20167-113">*grbit*</span></span>

<span data-ttu-id="20167-114">Группа битов, содержащая параметры, используемые для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="20167-114">A group of bits that contain the options to be used for this call.</span></span> <span data-ttu-id="20167-115">*Грбит* должен быть ненулевым и должен включать одно или несколько значений, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="20167-115">*Grbit* must be nonzero and must include one or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20167-116">Значение</span><span class="sxs-lookup"><span data-stu-id="20167-116">Value</span></span></p></th>
<th><p><span data-ttu-id="20167-117">Значение</span><span class="sxs-lookup"><span data-stu-id="20167-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20167-118">JET_bitCheckUniqueness</span><span class="sxs-lookup"><span data-stu-id="20167-118">JET_bitCheckUniqueness</span></span></p></td>
<td><p><span data-ttu-id="20167-119">Будет возвращен Специальный код ошибки JET_wrnUniqueKey, если можно было бы недешево определить, что существует только одна запись индекса, соответствующая ключу поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-119">A special error code, JET_wrnUniqueKey, will be returned if it can be cheaply determined that there is exactly one index entry that matches the search key.</span></span></p>
<p><span data-ttu-id="20167-120">Этот параметр игнорируется, если не указано также JET_bitSeekEQ.</span><span class="sxs-lookup"><span data-stu-id="20167-120">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p>
<p><span data-ttu-id="20167-121">Этот параметр доступен только в выпусках Windows Server 2003 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="20167-121">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-122">JET_bitSeekEQ</span><span class="sxs-lookup"><span data-stu-id="20167-122">JET_bitSeekEQ</span></span></p></td>
<td><p><span data-ttu-id="20167-123">Курсор будет располагаться на записи индекса, ближайшей к началу индекса, точно совпадающему с ключом поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-123">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span> <span data-ttu-id="20167-124">Начало индекса — это элемент индекса, найденный при переходе к первой записи в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-124">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="20167-125">Начало индекса не совпадает с младшим концом индекса, который может изменяться в зависимости от порядка сортировки ключевых столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-125">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="20167-126">Этот параметр не имеет смысла использовать с ключом поиска, созданным с помощью <a href="gg269329(v=exchg.10).md">жетмакекэй</a> , с использованием подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="20167-126">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-127">JET_bitSeekGE</span><span class="sxs-lookup"><span data-stu-id="20167-127">JET_bitSeekGE</span></span></p></td>
<td><p><span data-ttu-id="20167-128">Курсор будет расположен на позиции индекса, ближайшей к началу индекса, который больше или равен элементу индекса, который в точности соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-128">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="20167-129">Начало индекса — это элемент индекса, найденный при переходе к первой записи в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-129">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="20167-130">Начало индекса не совпадает с младшим концом индекса, который может изменяться в зависимости от порядка сортировки ключевых столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-130">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="20167-131">Этот параметр не имеет смысла использовать с ключом поиска, созданным с помощью <a href="gg269329(v=exchg.10).md">жетмакекэй</a> , с помощью параметра подстановочного знака, предназначенного для поиска записей индекса, ближайших к концу индекса.</span><span class="sxs-lookup"><span data-stu-id="20167-131">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-132">JET_bitSeekGT</span><span class="sxs-lookup"><span data-stu-id="20167-132">JET_bitSeekGT</span></span></p></td>
<td><p><span data-ttu-id="20167-133">Курсор будет расположен на позиции индекса, ближайшей к началу индекса, который больше, чем элемент индекса, который точно соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-133">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="20167-134">Начало индекса — это элемент индекса, найденный при переходе к первой записи в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-134">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="20167-135">Начало индекса не совпадает с младшим концом индекса, который может изменяться в зависимости от порядка сортировки ключевых столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-135">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="20167-136">Этот параметр не имеет смысла использовать с ключом поиска, созданным с помощью <a href="gg269329(v=exchg.10).md">жетмакекэй</a> , с помощью параметра подстановочного знака, предназначенного для поиска записей индекса, ближайших к началу индекса.</span><span class="sxs-lookup"><span data-stu-id="20167-136">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-137">JET_bitSeekLE</span><span class="sxs-lookup"><span data-stu-id="20167-137">JET_bitSeekLE</span></span></p></td>
<td><p><span data-ttu-id="20167-138">Курсор будет расположен на позиции индекса, ближайшей к концу индекса, который меньше или равен элементу индекса, который в точности соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-138">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="20167-139">Конец индекса — это элемент индекса, найденный при переходе к последней записи в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-139">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="20167-140">Конец индекса не совпадает с верхним концом индекса, который может изменяться в зависимости от порядка сортировки ключевых столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-140">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="20167-141">Этот параметр не имеет смысла использовать с ключом поиска, созданным с помощью <a href="gg269329(v=exchg.10).md">жетмакекэй</a> , с помощью параметра подстановочного знака, предназначенного для поиска записей индекса, ближайших к началу индекса.</span><span class="sxs-lookup"><span data-stu-id="20167-141">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-142">JET_bitSeekLT</span><span class="sxs-lookup"><span data-stu-id="20167-142">JET_bitSeekLT</span></span></p></td>
<td><p><span data-ttu-id="20167-143">Курсор будет расположен в позиции индекса, ближайшей к концу индекса, который меньше, чем элемент индекса, который в точности соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-143">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="20167-144">Конец индекса — это элемент индекса, найденный при переходе к последней записи в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-144">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="20167-145">Конец индекса не совпадает с верхним концом индекса, который может изменяться в зависимости от порядка сортировки ключевых столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="20167-145">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="20167-146">Этот параметр не имеет смысла использовать с ключом поиска, созданным с помощью <a href="gg269329(v=exchg.10).md">жетмакекэй</a> , с помощью параметра подстановочного знака, предназначенного для поиска записей индекса, ближайших к концу индекса.</span><span class="sxs-lookup"><span data-stu-id="20167-146">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-147">JET_bitSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="20167-147">JET_bitSetIndexRange</span></span></p></td>
<td><p><span data-ttu-id="20167-148">Диапазон индексов будет автоматически настроен для всех ключей, точно соответствующих ключу поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-148">An index range will automatically be setup for all keys that exactly match the search key.</span></span> <span data-ttu-id="20167-149">Результирующий диапазон индекса идентичен тому, который в противном случае был бы создан вызовом <a href="gg294112(v=exchg.10).md">жетсетиндексранже</a> с параметрами JET_bitRangeInclusive и JET_bitRangeUpperLimit.</span><span class="sxs-lookup"><span data-stu-id="20167-149">The resulting index range is identical to one that would have otherwise been created by a call to <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> with the JET_bitRangeInclusive and JET_bitRangeUpperLimit options.</span></span> <span data-ttu-id="20167-150">Дополнительные сведения см. в разделе <a href="gg294112(v=exchg.10).md">жетсетиндексранже</a> .</span><span class="sxs-lookup"><span data-stu-id="20167-150">See <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> for more information.</span></span></p>
<p><span data-ttu-id="20167-151">Это удобный способ обнаружения всех элементов индекса, соответствующих тем же критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-151">This is a convenient method for discovering all the index entries that match the same search criteria.</span></span></p>
<p><span data-ttu-id="20167-152">Этот параметр игнорируется, если не указано также JET_bitSeekEQ.</span><span class="sxs-lookup"><span data-stu-id="20167-152">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="20167-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20167-153">Return Value</span></span>

<span data-ttu-id="20167-154">Эта функция позволяет возвратить любые [JET_ERRs](./jet-err.md) , определенные в этом API.</span><span class="sxs-lookup"><span data-stu-id="20167-154">This function allows for the return of any [JET_ERRs](./jet-err.md) that are defined in this API.</span></span> <span data-ttu-id="20167-155">Дополнительные сведения об ошибках Jet см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="20167-155">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20167-156">Код возврата</span><span class="sxs-lookup"><span data-stu-id="20167-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="20167-157">Описание</span><span class="sxs-lookup"><span data-stu-id="20167-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20167-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="20167-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="20167-159">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="20167-159">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="20167-160">Для <strong>жетсик</strong>это означает, что обнаружена запись индекса, которая точно соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-160">For <strong>JetSeek</strong>, this means that an index entry was found that exactly matched the search criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-161">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="20167-161">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="20167-162">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="20167-162">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-163">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="20167-163">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="20167-164">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="20167-164">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="20167-165">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="20167-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-166">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="20167-166">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="20167-167">Для курсора отсутствует текущий ключ поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-167">There is no current search key for the cursor.</span></span> <span data-ttu-id="20167-168"><strong>Жетсик</strong> требует, чтобы курсор имел допустимый ключ поиска, так как он будет использовать его для условий поиска, используемых для поиска записей индекса.</span><span class="sxs-lookup"><span data-stu-id="20167-168"><strong>JetSeek</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-169">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="20167-169">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="20167-170">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="20167-170">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-171">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="20167-171">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="20167-172">Не найдена запись индекса, соответствующая условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-172">No index entry was found that matched the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="20167-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="20167-174">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="20167-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-175">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="20167-175">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="20167-176">Обнаружена запись индекса, соответствующая условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-176">An index entry was found that matched the search criteria.</span></span> <span data-ttu-id="20167-177">Однако эта запись индекса не была точным соответствием.</span><span class="sxs-lookup"><span data-stu-id="20167-177">However, that index entry was not an exact match.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-178">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="20167-178">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="20167-179">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="20167-179">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="20167-180">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="20167-180">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-181">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="20167-181">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="20167-182">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="20167-182">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-183">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="20167-183">JET_wrnUniqueKey</span></span></p></td>
<td><p><span data-ttu-id="20167-184">Обнаружена ровно одна запись индекса, которая точно соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-184">Exactly one index entry was found that exactly matched the search criteria.</span></span> <span data-ttu-id="20167-185">Эта ошибка будет возвращена только в том случае, если было указано JET_bitSeekCheckUniqueness и было недешево определить, что совпадающая запись индекса является единственной записью индекса, которая точно соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-185">This error will only be returned if JET_bitSeekCheckUniqueness was specified and it was cheap to determine that the matching index entry was the only index entry that exactly matches the search criteria.</span></span></p>
<p><span data-ttu-id="20167-186">Эта ошибка будет возвращена только в Windows Server 2003 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="20167-186">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="20167-187">При успешном выполнении курсор будет размещен в записи индекса, соответствующей условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="20167-187">On success, the cursor will be positioned at an index entry that matches the search criteria.</span></span> <span data-ttu-id="20167-188">Если запись подготовлена к обновлению, это обновление будет отменено.</span><span class="sxs-lookup"><span data-stu-id="20167-188">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="20167-189">Если действует диапазон индексов, то диапазон индексов будет отменен.</span><span class="sxs-lookup"><span data-stu-id="20167-189">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="20167-190">Если для курсора был создан ключ поиска, то этот ключ поиска будет удален.</span><span class="sxs-lookup"><span data-stu-id="20167-190">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="20167-191">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20167-191">No change to the database state will occur.</span></span> <span data-ttu-id="20167-192">Если несколько записей индекса имеют одинаковое значение, всегда выбирается запись, ближайшая к началу индекса.</span><span class="sxs-lookup"><span data-stu-id="20167-192">When multiple index entries have the same value, the entry closest to the start of the index is always selected.</span></span>

<span data-ttu-id="20167-193">В случае сбоя позицию курсора останется неизменной, если не было возвращено JET_errRecordNotFound.</span><span class="sxs-lookup"><span data-stu-id="20167-193">On failure, the position of the cursor will remain unchanged unless JET_errRecordNotFound was returned.</span></span> <span data-ttu-id="20167-194">В этом случае курсор будет размещается в том месте, где элемент индекса, удовлетворяющий условиям поиска, заданным в поисковом ключе в этом курсоре, и заданное неравенство было бы.</span><span class="sxs-lookup"><span data-stu-id="20167-194">In that case, the cursor will be positioned where the index entry that matched the search criteria specified by the search key in that cursor and the specified inequality would have been.</span></span> <span data-ttu-id="20167-195">Курсор может быть перемещен относительно этой позиции, но по-прежнему не находится в допустимой записи индекса.</span><span class="sxs-lookup"><span data-stu-id="20167-195">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="20167-196">Если запись подготовлена к обновлению, это обновление будет отменено.</span><span class="sxs-lookup"><span data-stu-id="20167-196">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="20167-197">Если действует диапазон индексов, то диапазон индексов будет отменен.</span><span class="sxs-lookup"><span data-stu-id="20167-197">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="20167-198">Если для курсора был создан ключ поиска, то этот ключ поиска будет удален.</span><span class="sxs-lookup"><span data-stu-id="20167-198">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="20167-199">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20167-199">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="20167-200">Требования</span><span class="sxs-lookup"><span data-stu-id="20167-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20167-201"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="20167-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20167-202">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="20167-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="20167-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20167-204">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="20167-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="20167-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20167-206">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="20167-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20167-207"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="20167-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="20167-208">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="20167-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20167-209"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="20167-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="20167-210">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="20167-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="20167-211">См. также:</span><span class="sxs-lookup"><span data-stu-id="20167-211">See Also</span></span>

[<span data-ttu-id="20167-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="20167-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="20167-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="20167-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="20167-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="20167-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="20167-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="20167-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="20167-216">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="20167-216">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="20167-217">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="20167-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="20167-218">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="20167-218">JetStopService</span></span>](./jetstopservice-function.md)
