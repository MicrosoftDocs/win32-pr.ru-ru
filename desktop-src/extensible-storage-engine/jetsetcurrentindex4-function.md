---
description: Дополнительные сведения о функции JetSetCurrentIndex4
title: Функция JetSetCurrentIndex4
TOCTitle: JetSetCurrentIndex4 Function
ms:assetid: 6076d02c-5701-4021-ba0a-da36bff166d1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269262(v=EXCHG.10)
ms:contentKeyID: 32765564
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex4W
- JetSetCurrentIndex4A
- JetSetCurrentIndex4
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 234b945e9ebe4421d348eab0e72556b544578b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710871"
---
# <a name="jetsetcurrentindex4-function"></a><span data-ttu-id="4dc3c-103">Функция JetSetCurrentIndex4</span><span class="sxs-lookup"><span data-stu-id="4dc3c-103">JetSetCurrentIndex4 Function</span></span>


<span data-ttu-id="4dc3c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4dc3c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex4-function"></a><span data-ttu-id="4dc3c-105">Функция JetSetCurrentIndex4</span><span class="sxs-lookup"><span data-stu-id="4dc3c-105">JetSetCurrentIndex4 Function</span></span>

<span data-ttu-id="4dc3c-106">Функция **JetSetCurrentIndex4** используется для задания текущего индекса курсора.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-106">The **JetSetCurrentIndex4** function is used to set the current index of a cursor.</span></span> <span data-ttu-id="4dc3c-107">Текущий индекс курсора определяет, какие записи в таблице видимы для этого курсора, и порядок, в котором они отображаются, выбрав набор записей индекса, который будет использоваться для предоставления этих записей.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex4(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in_opt      JET_INDEXID* pindexid,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a><span data-ttu-id="4dc3c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dc3c-108">Parameters</span></span>

<span data-ttu-id="4dc3c-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="4dc3c-109">*sesid*</span></span>

<span data-ttu-id="4dc3c-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-110">The session to use for this call.</span></span>

<span data-ttu-id="4dc3c-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="4dc3c-111">*tableid*</span></span>

<span data-ttu-id="4dc3c-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-112">The cursor to use for this call.</span></span>

<span data-ttu-id="4dc3c-113">*сзиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="4dc3c-113">*szIndexName*</span></span>

<span data-ttu-id="4dc3c-114">Имя индекса, выбранного для курсора.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-114">The name of the index to be selected for the cursor.</span></span> <span data-ttu-id="4dc3c-115">Если этот параметр имеет значение NULL или является пустой строкой, выбирается кластеризованный индекс.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="4dc3c-116">Если для таблицы определен первичный индекс, то этот индекс будет выбран, так как он совпадает с кластеризованным индексом.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="4dc3c-117">Если для таблицы не определен первичный индекс, будет выбран последовательный индекс.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="4dc3c-118">Последовательный индекс не имеет определения индекса.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-118">The sequential index has no index definition.</span></span> <span data-ttu-id="4dc3c-119">Дополнительные сведения см. в разделе [жеткреатеиндекс](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4dc3c-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="4dc3c-120">Если *pIndexID* не равно null, имя индекса будет игнорироваться, а индекс будет выбран по идентификатору индекса.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="4dc3c-121">*pIndexID*</span><span class="sxs-lookup"><span data-stu-id="4dc3c-121">*pindexid*</span></span>

<span data-ttu-id="4dc3c-122">Идентификатор индекса, выбранного для курсора.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-122">The ID of the index to be selected for the cursor.</span></span>

<span data-ttu-id="4dc3c-123">Идентификатор индекса является временным непрозрачным маркером, который можно использовать для быстрого выбора индекса.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-123">The index ID is a volatile, opaque handle that can be used to quickly select an index.</span></span> <span data-ttu-id="4dc3c-124">Этот идентификатор можно получить с помощью Жетжетиндексинфо или Жетжеттаблеиндексинфо с помощью параметра JET_IdxInfoIndexId.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-124">This ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo using the JET_IdxInfoIndexId option.</span></span>

<span data-ttu-id="4dc3c-125">Если *pIndexID* имеет значение null, то индекс будет выбран по имени индекса, а идентификатор индекса будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-125">If *pindexid* is NULL then the index will be selected by its index name and the index ID will be ignored.</span></span>

<span data-ttu-id="4dc3c-126">Если этот параметр отсутствует, предполагается, что его значение равно NULL.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-126">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="4dc3c-127">*грбит*</span><span class="sxs-lookup"><span data-stu-id="4dc3c-127">*grbit*</span></span>

<span data-ttu-id="4dc3c-128">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-128">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4dc3c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4dc3c-129">Value</span></span></p></th>
<th><p><span data-ttu-id="4dc3c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4dc3c-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-131">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="4dc3c-131">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-132">Этот параметр указывает, что курсор должен располагаться на первой записи указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-132">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="4dc3c-133">Если выбран кластеризованный индекс (первичный индекс или последовательный индекс), а текущий индекс является вторичным индексом, то JET_bitMoveFirst предполагается.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-133">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="4dc3c-134">Если текущий индекс выбран, этот параметр игнорируется и изменение положения курсора не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-134">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-135">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="4dc3c-135">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-136">Этот параметр указывает, что курсор должен располагаться на записи индекса нового индекса, который соответствует записи, связанной с записью индекса, в текущей позиции курсора по старому индексу.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-136">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="4dc3c-137">Если определение нового индекса содержит по крайней мере один ключевой столбец с несколькими значениями, то запись конечного индекса неоднозначно.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-137">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="4dc3c-138">В этом случае заданный <em>итагсекуенце</em> используется для выбора многозначного многозначного ключевого столбца, используемого для позиционирования курсора.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-138">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="4dc3c-139">Необходимо только передать один <em>итагсекуенце</em> даже в случае нескольких ключевых столбцов с несколькими значениями, так как ядро расширяет только все значения для наиболее значимого многозначного ключевого столбца.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-139">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="4dc3c-140">Дополнительные сведения см. в разделе <a href="gg294099(v=exchg.10).md">жеткреатеиндекс</a> .</span><span class="sxs-lookup"><span data-stu-id="4dc3c-140">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="4dc3c-141">Если указан JET_bitMoveFirst, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-141">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="4dc3c-142">Если текущий индекс выбран, этот параметр игнорируется и изменение положения курсора не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-142">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="4dc3c-143">Если этот параметр отсутствует, предполагается, что его значение JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-143">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4dc3c-144">*итагсекуенце*</span><span class="sxs-lookup"><span data-stu-id="4dc3c-144">*itagSequence*</span></span>

<span data-ttu-id="4dc3c-145">Порядковый номер значения столбца с несколькими значениями, который будет использоваться для позиционирования курсора на новом индексе.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-145">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span>

<span data-ttu-id="4dc3c-146">Этот параметр используется только в сочетании с JET_bitNoMove.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-146">This parameter is only used in conjunction with JET_bitNoMove.</span></span> <span data-ttu-id="4dc3c-147">Дополнительные сведения см. в описании этого параметра.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-147">See the description of this option for more details.</span></span>

<span data-ttu-id="4dc3c-148">Если этот параметр отсутствует или имеет значение 0, предполагается, что оно равно 1.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-148">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

### <a name="return-value"></a><span data-ttu-id="4dc3c-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dc3c-149">Return Value</span></span>

<span data-ttu-id="4dc3c-150">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-150">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4dc3c-151">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-151">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4dc3c-152">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4dc3c-152">Return code</span></span></p></th>
<th><p><span data-ttu-id="4dc3c-153">Описание</span><span class="sxs-lookup"><span data-stu-id="4dc3c-153">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-154">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4dc3c-154">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-155">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-155">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-156">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="4dc3c-156">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-157">Вторичный индекс выбирается с параметром JET_bitNoMove и для первого многозначного ключевого столбца в определении нового индекса, соответствующего указанному порядковому номеру, отсутствует значение.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-157">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the definition for the new index that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-158">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4dc3c-158">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-159">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-159">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4dc3c-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-161">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="4dc3c-162">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-163">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="4dc3c-163">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-164">Содержимое идентификатора индекса недопустимо или устарело, и его необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-164">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="4dc3c-165">Это может произойти для <strong>JetSetCurrentIndex4</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="4dc3c-165">This can happen for <strong>JetSetCurrentIndex4</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="4dc3c-166">pIndexID- &gt; кбструкт не имеет ожидаемого размера (Windows Server 2003 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-166">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-167">Работа обработчика была завершена, так как был получен идентификатор индекса.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-167">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-168">Все курсоры, ссылающиеся на таблицу, содержащую индекс, соответствующий ИДЕНТИФИКАТОРу индекса, были закрыты и обработчик удалил определение индекса из кэша схемы.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-168">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-169">Идентификатор индекса используется с курсором, открытым в неверной таблице.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-169">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-170">Индекс был удален или еще не виден в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-170">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-171">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="4dc3c-171">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-172">Одно из указанных имен объектов недопустимо.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-172">One of the specified object names was invalid.</span></span> <span data-ttu-id="4dc3c-173">Все имена объектов должны соответствовать одному и тому же набору правил.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-173">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="4dc3c-174">Ниже приведены эти правила.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-174">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="4dc3c-175">Имена объектов должны состоять из символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-175">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-176">Имена объектов должны иметь длину по крайней мере один символ.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-176">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-177">Длина имен объектов не может превышать JET_cbNameMost (64) символов.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-177">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-178">Имена объектов не могут начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-178">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-179">Имена объектов не могут содержать управляющие символы ASCII (0x00 – 0x1F).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-179">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-180">Имена объектов не могут содержать восклицательный знак (!), точку (.), открывающую квадратную скобку ([) или правую квадратную скобку (]).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-180">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="4dc3c-181">После проверки для имени объекта будет использоваться только часть строки вплоть до первого пробела (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-181">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="4dc3c-182">Это фактически означает, что имена объектов не могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-182">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-183">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4dc3c-183">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-184">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-184">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4dc3c-185">Это может произойти для <strong>JetSetCurrentIndex4</strong> , если <em>PINDEXID</em> не равен null, а pIndexID- &gt; кбструкт не имеет ожидаемого размера (Windows XP и более ранние выпуски).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-185">This can happen for <strong>JetSetCurrentIndex4</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-186">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="4dc3c-186">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-187">Вторичный индекс выбирается с параметром JET_bitNoMove и в новом индексе отсутствует запись индекса, соответствующая записи, связанной с записью индекса, в текущей позиции курсора по старому индексу.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-187">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-188">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4dc3c-188">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-189">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-189">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-190">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="4dc3c-190">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-191">Подсистема исчерпала пул ресурсов, используемых для открытия курсоров.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-191">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="4dc3c-192">С помощью <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>можно управлять максимальным количеством курсоров, которые могут быть открыты в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-192">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="4dc3c-193">Дополнительные сведения см. в разделе <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> .</span><span class="sxs-lookup"><span data-stu-id="4dc3c-193">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="4dc3c-194">Это может произойти для <strong>JetSetCurrentIndex4</strong> , когда был выбран вторичный индекс, и обработчик не может открыть внутренний курсор для использования этого индекса.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-194">This can happen for <strong>JetSetCurrentIndex4</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-195">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4dc3c-195">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-196">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-196">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-197">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4dc3c-197">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-198">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-198">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="4dc3c-199">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-200">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4dc3c-200">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4dc3c-201">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-201">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4dc3c-202">При успешном выполнении текущий индекс курсора задается равным запрошенному индексу.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-202">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="4dc3c-203">Теперь элементы индекса можно искать с помощью [жетсик](./jetseek-function.md) в соответствии с определением индекса запрошенного индекса.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-203">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="4dc3c-204">Элементы индекса можно также перечислить с помощью [жетмове](./jetmove-function.md) в порядке, указанном в определении индекса.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-204">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="4dc3c-205">Текущая позиция курсора либо установлена на первый элемент индекса (JET_bitMoveFirst), либо на конкретную запись индекса, связанную с текущей позицией курсора по старому индексу (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-205">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="4dc3c-206">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-206">No change to the database state will occur.</span></span>

<span data-ttu-id="4dc3c-207">В случае сбоя текущий индекс и текущая позиция курсора находятся в неопределенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-207">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="4dc3c-208">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-208">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4dc3c-209">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4dc3c-209">Remarks</span></span>

<span data-ttu-id="4dc3c-210">Если указание идентификатора индекса устарело, то API просто завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-210">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="4dc3c-211">В данном случае откат к текстовому имени индекса отсутствует, как можно было бы ожидать.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-211">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="4dc3c-212">Эта резервная копия должна выполняться вручную вызывающим объектом API.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-212">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4dc3c-213">Требования</span><span class="sxs-lookup"><span data-stu-id="4dc3c-213">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-214"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="4dc3c-214"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4dc3c-215">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-215">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-216"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4dc3c-216"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4dc3c-217">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-217">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-218"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4dc3c-218"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4dc3c-219">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-219">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-220"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="4dc3c-220"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4dc3c-221">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-221">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc3c-222"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="4dc3c-222"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4dc3c-223">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-223">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc3c-224"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="4dc3c-224"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4dc3c-225">Реализуется как <strong>JetSetCurrentIndex4W</strong> (Юникод) и <strong>JetSetCurrentIndex4A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-225">Implemented as <strong>JetSetCurrentIndex4W</strong> (Unicode) and <strong>JetSetCurrentIndex4A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4dc3c-226">См. также:</span><span class="sxs-lookup"><span data-stu-id="4dc3c-226">See Also</span></span>

[<span data-ttu-id="4dc3c-227">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4dc3c-227">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4dc3c-228">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4dc3c-228">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4dc3c-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4dc3c-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4dc3c-230">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4dc3c-230">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4dc3c-231">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="4dc3c-231">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="4dc3c-232">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="4dc3c-232">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="4dc3c-233">жетжеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="4dc3c-233">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="4dc3c-234">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="4dc3c-234">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="4dc3c-235">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="4dc3c-235">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="4dc3c-236">жетмове</span><span class="sxs-lookup"><span data-stu-id="4dc3c-236">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="4dc3c-237">жетсик</span><span class="sxs-lookup"><span data-stu-id="4dc3c-237">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="4dc3c-238">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="4dc3c-238">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
