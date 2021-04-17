---
description: Дополнительные сведения о функции JetSetCurrentIndex3
title: Функция JetSetCurrentIndex3
TOCTitle: JetSetCurrentIndex3 Function
ms:assetid: 50050bd3-4b74-4be7-985c-754ced8aded1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269244(v=EXCHG.10)
ms:contentKeyID: 32765546
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex3A
- JetSetCurrentIndex3W
- JetSetCurrentIndex3
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b97aa356d44ab72f7cd240a42351d9962777ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710935"
---
# <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="4f169-103">Функция JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="4f169-103">JetSetCurrentIndex3 Function</span></span>


<span data-ttu-id="4f169-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4f169-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="4f169-105">Функция JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="4f169-105">JetSetCurrentIndex3 Function</span></span>

<span data-ttu-id="4f169-106">Функция **JetSetCurrentIndex3** используется для задания текущего индекса курсора.</span><span class="sxs-lookup"><span data-stu-id="4f169-106">The **JetSetCurrentIndex3** function is used to set the current index of a cursor.</span></span> <span data-ttu-id="4f169-107">Текущий индекс курсора определяет, какие записи в таблице видимы для этого курсора, и порядок, в котором они отображаются, выбрав набор записей индекса, который будет использоваться для предоставления этих записей.</span><span class="sxs-lookup"><span data-stu-id="4f169-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a><span data-ttu-id="4f169-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f169-108">Parameters</span></span>

<span data-ttu-id="4f169-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="4f169-109">*sesid*</span></span>

<span data-ttu-id="4f169-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="4f169-110">The session to use for this call.</span></span>

<span data-ttu-id="4f169-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="4f169-111">*tableid*</span></span>

<span data-ttu-id="4f169-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="4f169-112">The cursor to use for this call.</span></span>

<span data-ttu-id="4f169-113">*сзиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="4f169-113">*szIndexName*</span></span>

<span data-ttu-id="4f169-114">Имя индекса, выбранного для курсора.</span><span class="sxs-lookup"><span data-stu-id="4f169-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="4f169-115">Если этот параметр имеет значение NULL или является пустой строкой, выбирается кластеризованный индекс.</span><span class="sxs-lookup"><span data-stu-id="4f169-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="4f169-116">Если для таблицы определен первичный индекс, то этот индекс будет выбран, так как он совпадает с кластеризованным индексом.</span><span class="sxs-lookup"><span data-stu-id="4f169-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="4f169-117">Если для таблицы не определен первичный индекс, будет выбран последовательный индекс.</span><span class="sxs-lookup"><span data-stu-id="4f169-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="4f169-118">Последовательный индекс не имеет определения индекса.</span><span class="sxs-lookup"><span data-stu-id="4f169-118">The sequential index has no index definition.</span></span> <span data-ttu-id="4f169-119">Дополнительные сведения см. в разделе [жеткреатеиндекс](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4f169-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="4f169-120">Если *pIndexID* не равно null, имя индекса будет игнорироваться, а индекс будет выбран по идентификатору индекса.</span><span class="sxs-lookup"><span data-stu-id="4f169-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="4f169-121">*грбит*</span><span class="sxs-lookup"><span data-stu-id="4f169-121">*grbit*</span></span>

<span data-ttu-id="4f169-122">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4f169-122">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f169-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4f169-123">Value</span></span></p></th>
<th><p><span data-ttu-id="4f169-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4f169-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f169-125">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="4f169-125">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="4f169-126">Этот параметр указывает, что курсор должен располагаться на первой записи указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="4f169-126">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="4f169-127">Если выбран кластеризованный индекс (первичный индекс или последовательный индекс), а текущий индекс является вторичным индексом, то JET_bitMoveFirst предполагается.</span><span class="sxs-lookup"><span data-stu-id="4f169-127">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="4f169-128">Если текущий индекс выбран, этот параметр игнорируется и изменение положения курсора не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f169-128">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-129">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="4f169-129">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="4f169-130">Этот параметр указывает, что курсор должен располагаться на записи индекса нового индекса, который соответствует записи, связанной с записью индекса, в текущей позиции курсора по старому индексу.</span><span class="sxs-lookup"><span data-stu-id="4f169-130">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="4f169-131">Если определение нового индекса содержит по крайней мере один ключевой столбец с несколькими значениями, то запись конечного индекса неоднозначно.</span><span class="sxs-lookup"><span data-stu-id="4f169-131">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="4f169-132">В этом случае заданный <em>итагсекуенце</em> используется для выбора многозначного многозначного ключевого столбца, используемого для позиционирования курсора.</span><span class="sxs-lookup"><span data-stu-id="4f169-132">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="4f169-133">Необходимо только передать один <em>итагсекуенце</em> даже в случае нескольких ключевых столбцов с несколькими значениями, так как ядро расширяет только все значения для наиболее значимого многозначного ключевого столбца.</span><span class="sxs-lookup"><span data-stu-id="4f169-133">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="4f169-134">Дополнительные сведения см. в разделе <a href="gg294099(v=exchg.10).md">жеткреатеиндекс</a> .</span><span class="sxs-lookup"><span data-stu-id="4f169-134">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="4f169-135">Если указан JET_bitMoveFirst, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4f169-135">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="4f169-136">Если текущий индекс выбран, этот параметр игнорируется и изменение положения курсора не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f169-136">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="4f169-137">Если этот параметр отсутствует, предполагается, что его значение JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="4f169-137">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f169-138">*итагсекуенце*</span><span class="sxs-lookup"><span data-stu-id="4f169-138">*itagSequence*</span></span>

<span data-ttu-id="4f169-139">Порядковый номер значения столбца с несколькими значениями, который будет использоваться для позиционирования курсора на новом индексе.</span><span class="sxs-lookup"><span data-stu-id="4f169-139">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span>

<span data-ttu-id="4f169-140">Этот параметр используется только в сочетании с JET_bitNoMove.</span><span class="sxs-lookup"><span data-stu-id="4f169-140">This parameter is only used in conjunction with JET_bitNoMove.</span></span> <span data-ttu-id="4f169-141">Дополнительные сведения см. в описании этого параметра.</span><span class="sxs-lookup"><span data-stu-id="4f169-141">See the description of this option for more details.</span></span>

<span data-ttu-id="4f169-142">Если этот параметр отсутствует или имеет значение 0, предполагается, что оно равно 1.</span><span class="sxs-lookup"><span data-stu-id="4f169-142">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

### <a name="return-value"></a><span data-ttu-id="4f169-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f169-143">Return Value</span></span>

<span data-ttu-id="4f169-144">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="4f169-144">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4f169-145">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4f169-145">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f169-146">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4f169-146">Return code</span></span></p></th>
<th><p><span data-ttu-id="4f169-147">Описание</span><span class="sxs-lookup"><span data-stu-id="4f169-147">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f169-148">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4f169-148">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4f169-149">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4f169-149">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-150">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="4f169-150">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="4f169-151">Вторичный индекс выбирается с параметром JET_bitNoMove и для первого многозначного ключевого столбца в определении нового индекса, который соответствует указанному порядковому номеру, отсутствует значение.</span><span class="sxs-lookup"><span data-stu-id="4f169-151">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f169-152">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4f169-152">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4f169-153">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="4f169-153">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-154">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4f169-154">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4f169-155">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="4f169-155">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="4f169-156">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="4f169-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f169-157">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="4f169-157">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="4f169-158">Содержимое идентификатора индекса недопустимо или устарело, и его необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="4f169-158">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="4f169-159">Это может произойти для <strong>JetSetCurrentIndex3</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="4f169-159">This can happen for <strong>JetSetCurrentIndex3</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="4f169-160">pIndexID- &gt; кбструкт не имеет ожидаемого размера (Windows Server 2003 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="4f169-160">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="4f169-161">Работа обработчика была завершена, так как был получен идентификатор индекса.</span><span class="sxs-lookup"><span data-stu-id="4f169-161">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="4f169-162">Все курсоры, ссылающиеся на таблицу, содержащую индекс, соответствующий ИДЕНТИФИКАТОРу индекса, были закрыты и подсистема удалила определение этого индекса из кэша схемы.</span><span class="sxs-lookup"><span data-stu-id="4f169-162">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for that index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="4f169-163">Идентификатор индекса используется с курсором, открытым в неверной таблице.</span><span class="sxs-lookup"><span data-stu-id="4f169-163">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="4f169-164">Индекс был удален или еще не виден в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4f169-164">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-165">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="4f169-165">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="4f169-166">Одно из указанных имен объектов недопустимо.</span><span class="sxs-lookup"><span data-stu-id="4f169-166">One of the specified object names was invalid.</span></span> <span data-ttu-id="4f169-167">Все имена объектов должны соответствовать одному и тому же набору правил.</span><span class="sxs-lookup"><span data-stu-id="4f169-167">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="4f169-168">Ниже приведены эти правила.</span><span class="sxs-lookup"><span data-stu-id="4f169-168">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="4f169-169">Имена объектов должны состоять из символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="4f169-169">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="4f169-170">Имена объектов должны иметь длину по крайней мере один символ.</span><span class="sxs-lookup"><span data-stu-id="4f169-170">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="4f169-171">Длина имен объектов не может превышать JET_cbNameMost (64) символов.</span><span class="sxs-lookup"><span data-stu-id="4f169-171">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="4f169-172">Имена объектов не могут начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="4f169-172">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="4f169-173">Имена объектов не могут содержать управляющие символы ASCII (0x00 – 0x1F).</span><span class="sxs-lookup"><span data-stu-id="4f169-173">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="4f169-174">Имена объектов не могут содержать восклицательный знак (!), точку (.), открывающую квадратную скобку ([) или правую квадратную скобку (]).</span><span class="sxs-lookup"><span data-stu-id="4f169-174">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="4f169-175">После проверки для имени объекта будет использоваться только часть строки вплоть до первого пробела (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="4f169-175">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="4f169-176">Это фактически означает, что имена объектов не могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="4f169-176">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f169-177">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4f169-177">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4f169-178">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="4f169-178">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4f169-179">Это может произойти для <strong>JetSetCurrentIndex3</strong> , если <em>PINDEXID</em> не равен null, а pIndexID- &gt; кбструкт не имеет ожидаемого размера (Windows XP и более ранние выпуски).</span><span class="sxs-lookup"><span data-stu-id="4f169-179">This can happen for <strong>JetSetCurrentIndex3</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-180">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="4f169-180">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="4f169-181">Вторичный индекс выбирается с параметром JET_bitNoMove и в новом индексе отсутствует запись индекса, соответствующая записи, связанной с записью индекса, в текущей позиции курсора по старому индексу.</span><span class="sxs-lookup"><span data-stu-id="4f169-181">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f169-182">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4f169-182">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4f169-183">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="4f169-183">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-184">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="4f169-184">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="4f169-185">Подсистема исчерпала пул ресурсов, используемых для открытия курсоров.</span><span class="sxs-lookup"><span data-stu-id="4f169-185">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="4f169-186">С помощью <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>можно управлять максимальным количеством курсоров, которые могут быть открыты в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="4f169-186">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="4f169-187">Дополнительные сведения см. в разделе <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> .</span><span class="sxs-lookup"><span data-stu-id="4f169-187">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="4f169-188">Это может произойти для <strong>JetSetCurrentIndex3</strong> , когда был выбран вторичный индекс, и обработчик не может открыть внутренний курсор для использования этого индекса.</span><span class="sxs-lookup"><span data-stu-id="4f169-188">This can happen for <strong>JetSetCurrentIndex3</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f169-189">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4f169-189">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4f169-190">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="4f169-190">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-191">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4f169-191">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4f169-192">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="4f169-192">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="4f169-193">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="4f169-193">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f169-194">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4f169-194">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4f169-195">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="4f169-195">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f169-196">При успешном выполнении текущий индекс курсора задается равным запрошенному индексу.</span><span class="sxs-lookup"><span data-stu-id="4f169-196">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="4f169-197">Теперь элементы индекса можно искать с помощью [жетсик](./jetseek-function.md) в соответствии с определением индекса запрошенного индекса.</span><span class="sxs-lookup"><span data-stu-id="4f169-197">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="4f169-198">Элементы индекса можно также перечислить с помощью [жетмове](./jetmove-function.md) в порядке, указанном в определении индекса.</span><span class="sxs-lookup"><span data-stu-id="4f169-198">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="4f169-199">Текущая позиция курсора либо установлена на первый элемент индекса (JET_bitMoveFirst), либо на конкретную запись индекса, связанную с текущей позицией курсора по старому индексу (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="4f169-199">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="4f169-200">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f169-200">No change to the database state will occur.</span></span>

<span data-ttu-id="4f169-201">В случае сбоя текущий индекс и текущая позиция курсора находятся в неопределенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4f169-201">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="4f169-202">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f169-202">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4f169-203">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f169-203">Remarks</span></span>

<span data-ttu-id="4f169-204">Если указание идентификатора индекса устарело, то API просто завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4f169-204">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="4f169-205">В данном случае откат к текстовому имени индекса отсутствует, как можно было бы ожидать.</span><span class="sxs-lookup"><span data-stu-id="4f169-205">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="4f169-206">Эта резервная копия должна выполняться вручную вызывающим объектом API.</span><span class="sxs-lookup"><span data-stu-id="4f169-206">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4f169-207">Требования</span><span class="sxs-lookup"><span data-stu-id="4f169-207">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f169-208"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="4f169-208"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4f169-209">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4f169-209">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-210"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4f169-210"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4f169-211">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4f169-211">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f169-212"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4f169-212"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4f169-213">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4f169-213">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-214"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="4f169-214"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4f169-215">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4f169-215">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f169-216"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="4f169-216"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4f169-217">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4f169-217">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f169-218"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="4f169-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4f169-219">Реализуется как <strong>JetSetCurrentIndex3W</strong> (Юникод) и <strong>JetSetCurrentIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4f169-219">Implemented as <strong>JetSetCurrentIndex3W</strong> (Unicode) and <strong>JetSetCurrentIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4f169-220">См. также:</span><span class="sxs-lookup"><span data-stu-id="4f169-220">See Also</span></span>

[<span data-ttu-id="4f169-221">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4f169-221">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4f169-222">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4f169-222">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4f169-223">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4f169-223">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4f169-224">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4f169-224">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4f169-225">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="4f169-225">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="4f169-226">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="4f169-226">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="4f169-227">жетжеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="4f169-227">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="4f169-228">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="4f169-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="4f169-229">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="4f169-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="4f169-230">жетмове</span><span class="sxs-lookup"><span data-stu-id="4f169-230">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="4f169-231">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="4f169-231">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="4f169-232">жетсик</span><span class="sxs-lookup"><span data-stu-id="4f169-232">JetSeek</span></span>](./jetseek-function.md)
