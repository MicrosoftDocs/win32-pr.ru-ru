---
description: Дополнительные сведения о функции Жетенумератеколумнс
title: Функция JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265532"
---
# <a name="jetenumeratecolumns-function"></a><span data-ttu-id="c3a21-103">Функция JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="c3a21-103">JetEnumerateColumns Function</span></span>


<span data-ttu-id="c3a21-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c3a21-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenumeratecolumns-function"></a><span data-ttu-id="c3a21-105">Функция JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="c3a21-105">JetEnumerateColumns Function</span></span>

<span data-ttu-id="c3a21-106">Функция **жетенумератеколумнс** эффективно извлекает набор столбцов и их значений из текущей записи курсора или буфера копирования этого курсора.</span><span class="sxs-lookup"><span data-stu-id="c3a21-106">The **JetEnumerateColumns** function efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="c3a21-107">Возвращаемые столбцы и значения могут быть ограничены списком идентификаторов столбцов, *итагсекуенце* числами и другими характеристиками.</span><span class="sxs-lookup"><span data-stu-id="c3a21-107">The columns and values retrieved can be restricted by a list of column IDs, *itagSequence* numbers, and other characteristics.</span></span> <span data-ttu-id="c3a21-108">Этот интерфейс API извлечения столбца уникален в том, что он возвращает сведения в динамически выделяемой памяти, получаемой с [помощью предоставленного](/cpp/c-runtime-library/reference/realloc?view=vs-2019) пользователем обратного вызова, совместимого с переопределением.</span><span class="sxs-lookup"><span data-stu-id="c3a21-108">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="c3a21-109">Эта новая гибкость позволяет эффективно получать данные столбцов с определенными характеристиками (например, размер и количество элементов), неизвестных вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="c3a21-109">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="c3a21-110">Это устраняет необходимость использования режимов обнаружения [жетретриевеколумн](./jetretrievecolumn-function.md) для определения этих характеристик, чтобы настроить окончательный вызов [жетретриевеколумн](./jetretrievecolumn-function.md) , который будет успешно получать нужные данные.</span><span class="sxs-lookup"><span data-stu-id="c3a21-110">This eliminates the need for the use of the discovery modes of [JetRetrieveColumn](./jetretrievecolumn-function.md) to determine those characteristics in order to setup a final call to [JetRetrieveColumn](./jetretrievecolumn-function.md) that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="c3a21-111">**Windows XP: жетенумератеколумнс** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3a21-111">**Windows XP:  JetEnumerateColumns** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c3a21-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3a21-112">Parameters</span></span>

<span data-ttu-id="c3a21-113">*сесид*</span><span class="sxs-lookup"><span data-stu-id="c3a21-113">*sesid*</span></span>

<span data-ttu-id="c3a21-114">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c3a21-114">The session to use for this call.</span></span>

<span data-ttu-id="c3a21-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c3a21-115">*tableid*</span></span>

<span data-ttu-id="c3a21-116">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c3a21-116">The cursor to use for this call.</span></span>

<span data-ttu-id="c3a21-117">*ценумколумнид*</span><span class="sxs-lookup"><span data-stu-id="c3a21-117">*cEnumColumnId*</span></span>

<span data-ttu-id="c3a21-118">Массив идентификаторов столбцов, каждый из которых имеет необязательный массив *итагсекуенце* чисел для перечисления.</span><span class="sxs-lookup"><span data-stu-id="c3a21-118">An array of column IDs, each with an optional array of *itagSequence* numbers to enumerate.</span></span>

<span data-ttu-id="c3a21-119">Если *ценумколумнид* имеет значение 0 (ноль), то *рженумколумнид* игнорируется и значения всех столбцов перечисляются и возвращаются вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="c3a21-119">If *cEnumColumnId* is 0 (zero) then *rgEnumColumnId* is ignored and all column values are enumerated and returned to the caller.</span></span> <span data-ttu-id="c3a21-120">Если элемент массива ИДЕНТИФИКАТОРов столбцов ссылается на нулевой столбец с ИДЕНТИФИКАТОРом 0 (ноль), то перечисление этого столбца пропускается и создается соответствующий слот в выходных данных с состоянием столбца JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="c3a21-120">If an element of the column ID array refers to a column ID of 0 (zero) then enumeration of that column is skipped and a corresponding slot in the output will be generated with a column status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="c3a21-121">Если *ктагсекуенце* имеет значение 0 (ноль) для заданного элемента массива идентификаторов столбцов, *ргтагсекуенце* игнорируется, и все значения столбцов для этого идентификатора столбца перечисляются и возвращаются вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="c3a21-121">If *ctagSequence* is 0 (zero) for a given element of the column ID array then *rgtagSequence* is ignored and all column values for that column ID are enumerated and returned to the caller.</span></span> <span data-ttu-id="c3a21-122">Если элемент массива *итагсекуенце* Number ссылается на *итагсекуенце* число 0 (ноль), то перечисление этого числа *итагсекуенце* пропускается, а соответствующая ячейка в выходных данных будет формироваться со значением столбца status JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="c3a21-122">If an element of an *itagSequence* number array refers to a *itagSequence* number of 0 (zero) then the enumeration of that *itagSequence* number is skipped and a corresponding slot in the output will be generated with a column value status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="c3a21-123">*рженумколумнид*</span><span class="sxs-lookup"><span data-stu-id="c3a21-123">*rgEnumColumnId*</span></span>

<span data-ttu-id="c3a21-124">См. *ценумколумнид*.</span><span class="sxs-lookup"><span data-stu-id="c3a21-124">See *cEnumColumnId*.</span></span>

<span data-ttu-id="c3a21-125">*пценумколумн*</span><span class="sxs-lookup"><span data-stu-id="c3a21-125">*pcEnumColumn*</span></span>

<span data-ttu-id="c3a21-126">Возвращает перечислимый массив столбцов и их значения в памяти, выделенной через предоставленный *итагсекуенце* -совместимый обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="c3a21-126">Returns the enumerated array of columns and their values in memory allocated through the provided *itagSequence* compatible callback.</span></span>

<span data-ttu-id="c3a21-127">Если на входе запрашивается массив идентификаторов столбцов, порядок и размер выходного массива будут отражать порядок и размер входного массива.</span><span class="sxs-lookup"><span data-stu-id="c3a21-127">If an array of column IDs is requested on input then the order and size of the output array will reflect the order and size of the input array.</span></span> <span data-ttu-id="c3a21-128">Аналогично, если массив номеров *итагсекуенце* запрашивается для определенного идентификатора столбца на входе, порядок и размер выходного массива значений столбцов для этого столбца будут отражать порядок и размер входного массива.</span><span class="sxs-lookup"><span data-stu-id="c3a21-128">Similarly, if an array of *itagSequence* numbers is requested for a particular column ID on input then the order and size of the output array of column values for that column will reflect the order and size of the input array.</span></span>

<span data-ttu-id="c3a21-129">Для выходных параметров задано значение 0 (ноль) и **null** для любой ошибки, кроме JET_errBadColumnId и JET_errColumnNotFound.</span><span class="sxs-lookup"><span data-stu-id="c3a21-129">The output parameters are set to 0 (zero) and **NULL** on any error except for JET_errBadColumnId and JET_errColumnNotFound.</span></span> <span data-ttu-id="c3a21-130">При возвращении этих ошибок выходные данные являются допустимыми и полными для всех идентификаторов столбцов, кроме затронутых.</span><span class="sxs-lookup"><span data-stu-id="c3a21-130">When these errors are returned, the output data is valid and complete for all but the affected column IDs.</span></span> <span data-ttu-id="c3a21-131">Коду состояния для каждого из затронутых идентификаторов столбцов присваивается одна из этих ошибок, чтобы вызывающий объект мог определить, какие идентификаторы столбцов были некорректными, и потенциально предпринять корректирующие действия.</span><span class="sxs-lookup"><span data-stu-id="c3a21-131">The status code for each of the affected column IDs is set to one of these errors so that the caller may determine which column IDs were bad and potentially take corrective action.</span></span>

<span data-ttu-id="c3a21-132">*прженумколумн*</span><span class="sxs-lookup"><span data-stu-id="c3a21-132">*prgEnumColumn*</span></span>

<span data-ttu-id="c3a21-133">См. *пценумколумн*.</span><span class="sxs-lookup"><span data-stu-id="c3a21-133">See *pcEnumColumn*.</span></span>

<span data-ttu-id="c3a21-134">*пфнреаллок*</span><span class="sxs-lookup"><span data-stu-id="c3a21-134">*pfnRealloc*</span></span>

<span data-ttu-id="c3a21-135">Определяет [совместимый](/cpp/c-runtime-library/reference/realloc?view=vs-2019) с перераспределением обратный вызов и Необязательный указатель контекста, используемый для выделения памяти для выходного массива столбцов и их значений.</span><span class="sxs-lookup"><span data-stu-id="c3a21-135">Identifies a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback and an optional context pointer used to allocate memory for the output array of columns and their values.</span></span>

<span data-ttu-id="c3a21-136">*пвреаллокконтекст*</span><span class="sxs-lookup"><span data-stu-id="c3a21-136">*pvReallocContext*</span></span>

<span data-ttu-id="c3a21-137">См. *пфнреаллок*.</span><span class="sxs-lookup"><span data-stu-id="c3a21-137">See *pfnRealloc*.</span></span>

<span data-ttu-id="c3a21-138">*кбдатамост*</span><span class="sxs-lookup"><span data-stu-id="c3a21-138">*cbDataMost*</span></span>

<span data-ttu-id="c3a21-139">Устанавливает ограничение на объем данных, возвращаемых из длинного текстового или длинного двоичного столбца.</span><span class="sxs-lookup"><span data-stu-id="c3a21-139">Sets a cap on the amount of data to return from a long text or long binary column.</span></span>

<span data-ttu-id="c3a21-140">Этот параметр можно использовать, чтобы предотвратить перечисление слишком большого значения столбца.</span><span class="sxs-lookup"><span data-stu-id="c3a21-140">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span> <span data-ttu-id="c3a21-141">Обычно такое перечисление может привести к сбою вызова API с JET_errOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="c3a21-141">Ordinarily, such an enumeration might fail the API call with JET_errOutOfMemory.</span></span> <span data-ttu-id="c3a21-142">Если значение большого столбца усекается таким образом, значение столбца будет JET_wrnColumnTruncated.</span><span class="sxs-lookup"><span data-stu-id="c3a21-142">If a large column value is truncated in such a manner then the column value's status will be JET_wrnColumnTruncated.</span></span>

<span data-ttu-id="c3a21-143">*грбит*</span><span class="sxs-lookup"><span data-stu-id="c3a21-143">*grbit*</span></span>

<span data-ttu-id="c3a21-144">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="c3a21-144">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3a21-145">Значение</span><span class="sxs-lookup"><span data-stu-id="c3a21-145">Value</span></span></p></th>
<th><p><span data-ttu-id="c3a21-146">Значение</span><span class="sxs-lookup"><span data-stu-id="c3a21-146">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-147">JET_bitEnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="c3a21-147">JET_bitEnumerateCompressOutput</span></span></p></td>
<td><p><span data-ttu-id="c3a21-148">При перечислении значений столбцов все столбцы, для которых мы получаем все значения и которые имеют только одно значение столбца, отличного от NULL, могут быть возвращены в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="c3a21-148">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="c3a21-149">Для таких столбцов будет задано значение JET_wrnColumnSingleValue, а размер значения столбца и объем памяти, содержащей значение столбца, будут возвращаться непосредственно в структуре <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="c3a21-149">The status for such columns will be set to JET_wrnColumnSingleValue and the size of the column value and the memory containing the column value will be returned directly in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="c3a21-150">Не гарантируется, что все подходящие столбцы сжимаются таким образом.</span><span class="sxs-lookup"><span data-stu-id="c3a21-150">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="c3a21-151">Дополнительные сведения см. в разделе <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="c3a21-151">See <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-152">JET_bitEnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="c3a21-152">JET_bitEnumerateCopy</span></span></p></td>
<td><p><span data-ttu-id="c3a21-153">Этот параметр указывает, что необходимо перечислить измененные значения столбца записи, а не исходные значения столбца.</span><span class="sxs-lookup"><span data-stu-id="c3a21-153">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="c3a21-154">Если значение столбца не было изменено, исходное значение столбца перечисляется.</span><span class="sxs-lookup"><span data-stu-id="c3a21-154">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="c3a21-155">Таким образом, значение столбца, которое еще не было вставлено или Обновлено, может быть перечислено при вставке или обновлении записи.</span><span class="sxs-lookup"><span data-stu-id="c3a21-155">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span></p>
<p><span data-ttu-id="c3a21-156">Этот параметр идентичен JET_bitRetrieveCopy при использовании с <a href="gg269198(v=exchg.10).md">жетретриевеколумн</a> или <a href="gg294135(v=exchg.10).md">жетретриевеколумнс</a>.</span><span class="sxs-lookup"><span data-stu-id="c3a21-156">This option is identical to JET_bitRetrieveCopy when used with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-157">JET_bitEnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="c3a21-157">JET_bitEnumerateIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="c3a21-158">Если данный столбец отсутствует в записи, значение столбца не будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="c3a21-158">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="c3a21-159">Обычно в этом случае возвращается значение по умолчанию для столбца, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="c3a21-159">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="c3a21-160">Гарантируется, что если в столбце задано значение, отличное от значения по умолчанию, то будет возвращено другое значение (т. е. Если для столбца со значением по умолчанию явно задано значение <strong>null</strong> , то в качестве значения для этого столбца будет возвращено значение <strong>null</strong> ).</span><span class="sxs-lookup"><span data-stu-id="c3a21-160">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to <strong>NULL</strong> then a <strong>NULL</strong> will be returned as the value for that column).</span></span> <span data-ttu-id="c3a21-161">Обратите внимание, что даже при запросе этого параметра по-прежнему можно увидеть значение столбца, которое должно быть равно значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3a21-161">Note that, even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="c3a21-162">Для удаления значений столбцов, соответствующих значениям по умолчанию, никаких усилий не предпринимается.</span><span class="sxs-lookup"><span data-stu-id="c3a21-162">No effort is made to remove column values that match their default values.</span></span></p>
<p><span data-ttu-id="c3a21-163">Важно отметить, что этот параметр влияет на выходные данные <strong>жетенумератеколумнс</strong> при использовании с JET_bitEnumeratePresenceOnly или JET_bitEnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="c3a21-163">It is important to note that this option affects the output of <strong>JetEnumerateColumns</strong> when used with JET_bitEnumeratePresenceOnly or JET_bitEnumerateTaggedOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-164">JET_bitEnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="c3a21-164">JET_bitEnumerateIgnoreUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="c3a21-165">Если данный столбец отсутствует в записи и имеет определенное пользователем значение по умолчанию, значение столбца не будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="c3a21-165">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="c3a21-166">Этот параметр предотвратит вызов функции обратного вызова, которая будет вычислять определенное пользователем значение по умолчанию для столбца, при перечислении значений для этого столбца.</span><span class="sxs-lookup"><span data-stu-id="c3a21-166">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></p>
<p><span data-ttu-id="c3a21-167"><strong>Windows Server 2003 и более ранние версии:  </strong> Для Windows Server 2003 и более ранних версий операция завершится ошибкой с JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="c3a21-167"><strong>Windows Server 2003 and earlier:  </strong>For Windows Server 2003 and earlier releases, the operation will fail with JET_errCallbackFailed.</span></span></p>
<p><span data-ttu-id="c3a21-168"><strong>Windows Server 2003 SP1:  </strong> Это возможное значение доступно только для Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="c3a21-168"><strong>Windows Server 2003 SP1:  </strong>This possible value is only available for Windows Server 2003 SP1 and later operating systems.</span></span> <span data-ttu-id="c3a21-169">Если это возможное значение указано и таблица содержит столбец с пользовательским значением по умолчанию, операция завершится с JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="c3a21-169">If this possible value is specified and the table contains a column that has a user defined default value, then the operation will fail with JET_errCallbackFailed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-170">JET_bitEnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="c3a21-170">JET_bitEnumeratePresenceOnly</span></span></p></td>
<td><p><span data-ttu-id="c3a21-171">Если для запрошенного столбца или значения столбца существует значение, отличное от NULL, связанные данные не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="c3a21-171">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="c3a21-172">Вместо этого связанное состояние для этого столбца или значения столбца будет установлено в значение JET_wrnColumnPresent.</span><span class="sxs-lookup"><span data-stu-id="c3a21-172">Instead, the associated status for that column or column value will be set to JET_wrnColumnPresent.</span></span> <span data-ttu-id="c3a21-173">Если значение столбца или столбца равно <strong>null</strong> , JET_wrnColumnNull будут возвращены как обычно.</span><span class="sxs-lookup"><span data-stu-id="c3a21-173">If the column or column value is <strong>NULL</strong> then JET_wrnColumnNull will be returned as usual.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-174">JET_bitEnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="c3a21-174">JET_bitEnumerateTaggedOnly</span></span></p></td>
<td><p><span data-ttu-id="c3a21-175">При перечислении всех значений столбцов в записи (например, если <em>ценумколумнид</em> равен нулю) будут возвращены только значения столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="c3a21-175">When enumerating all column values in the record (for example,that is when <em>cEnumColumnId</em> is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="c3a21-176">Этот параметр не допускается при перечислении определенного массива идентификаторов столбцов.</span><span class="sxs-lookup"><span data-stu-id="c3a21-176">This option is not allowed when enumerating a specific array of column IDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-177">JET_bitEnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="c3a21-177">JET_bitEnumerateInRecordOnly</span></span></p></td>
<td><p><span data-ttu-id="c3a21-178"><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3a21-178"><strong>Windows 7:  </strong>JET_bitEnumerateInRecordOnly is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c3a21-179">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3a21-179">Return Value</span></span>

<span data-ttu-id="c3a21-180">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="c3a21-180">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c3a21-181">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c3a21-181">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3a21-182">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c3a21-182">Return code</span></span></p></th>
<th><p><span data-ttu-id="c3a21-183">Описание</span><span class="sxs-lookup"><span data-stu-id="c3a21-183">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-184">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c3a21-184">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c3a21-185">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c3a21-185">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-186">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="c3a21-186">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="c3a21-187">Указанный идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="c3a21-187">The column ID given is outside the legal limits of a column ID.</span></span> <span data-ttu-id="c3a21-188">Эта ошибка будет возвращена <strong>жетенумератеколумнс</strong> , если были запрошены определенные идентификаторы столбцов, один из этих идентификаторов столбцов был недопустимым, а первый недопустимый идентификатор столбца завершился с ошибкой для своего кода состояния столбца.</span><span class="sxs-lookup"><span data-stu-id="c3a21-188">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column ids were requested, one of those column ids was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-189">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c3a21-189">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c3a21-190">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="c3a21-190">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-191">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="c3a21-191">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="c3a21-192">Столбец, описываемый данным ИДЕНТИФИКАТОРом столбца, не существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="c3a21-192">The column described by the given column ID does not exist in the table.</span></span> <span data-ttu-id="c3a21-193">Эта ошибка будет возвращена <strong>жетенумератеколумнс</strong> , если были запрошены определенные идентификаторы столбцов, один из этих идентификаторов столбцов был недопустимым, а первый недопустимый идентификатор столбца завершился с ошибкой для своего кода состояния столбца.</span><span class="sxs-lookup"><span data-stu-id="c3a21-193">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column IDs were requested, one of those column IDs was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c3a21-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c3a21-195">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="c3a21-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c3a21-196"><strong>Windows XP:  </strong> Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c3a21-196"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="c3a21-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="c3a21-198">Один из запрошенных параметров недопустим или не реализован.</span><span class="sxs-lookup"><span data-stu-id="c3a21-198">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="c3a21-199">Эта ошибка будет возвращена <strong>жетенумератеколумнс</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="c3a21-199">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="c3a21-200">Указан JET_bitEnumerateLocal.</span><span class="sxs-lookup"><span data-stu-id="c3a21-200">JET_bitEnumerateLocal is specified.</span></span></p></li>
<li><p><span data-ttu-id="c3a21-201">Указан недопустимый <em>грбит</em> .</span><span class="sxs-lookup"><span data-stu-id="c3a21-201">An illegal <em>grbit</em> is specified.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-202">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c3a21-202">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c3a21-203">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="c3a21-203">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="c3a21-204">Эта ошибка будет возвращена <strong>жетенумератеколумнс</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="c3a21-204">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="c3a21-205"><em>пценумколумн</em> имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3a21-205"><em>pcEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c3a21-206"><em>прженумколумн</em> имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3a21-206"><em>prgEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c3a21-207"><em>пфнреаллок</em> имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3a21-207"><em>pfnRealloc</em> is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-208">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="c3a21-208">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="c3a21-209">Курсор не располагается на записи.</span><span class="sxs-lookup"><span data-stu-id="c3a21-209">The cursor is not positioned on a record.</span></span> <span data-ttu-id="c3a21-210">Это может произойти по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="c3a21-210">This can happen for many different reasons.</span></span> <span data-ttu-id="c3a21-211">Например, это произойдет, если курсор находится в данный момент после последней записи в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="c3a21-211">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-212">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c3a21-212">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c3a21-213">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="c3a21-213">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-214">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="c3a21-214">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="c3a21-215">Курсор располагается на записи, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="c3a21-215">The cursor is positioned on a record that has been deleted.</span></span> <span data-ttu-id="c3a21-216">Это может произойти по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="c3a21-216">This can happen for many different reasons.</span></span> <span data-ttu-id="c3a21-217">Наиболее распространенной причиной является то, что сеанс не находится в транзакции, курсор был помещен в запись, эта запись была удалена, а затем курсор попытался ссылаться на эту запись.</span><span class="sxs-lookup"><span data-stu-id="c3a21-217">The most common reason is that the session is not in a transaction, the cursor was positioned on a record, that record was deleted, and then the cursor attempted to reference that record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-218">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c3a21-218">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c3a21-219">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="c3a21-219">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-220">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c3a21-220">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c3a21-221">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="c3a21-221">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c3a21-222"><strong>Windows XP:  </strong> Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c3a21-222"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-223">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c3a21-223">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c3a21-224">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="c3a21-224">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c3a21-225">При успешном выполнении запрошенные данные будут возвращены в выходные буферы.</span><span class="sxs-lookup"><span data-stu-id="c3a21-225">On success, the requested data will be returned in the output buffers.</span></span> <span data-ttu-id="c3a21-226">Вызывающая сторона обязана освободить любую память, выделенную этим обратным вызовом, и возвратить ее в выходные буферы.</span><span class="sxs-lookup"><span data-stu-id="c3a21-226">It is the caller's responsibility to free any memory allocated by this callback and returned in the output buffers.</span></span> <span data-ttu-id="c3a21-227">Эта память должна быть освобождена с помощью указанного обратного вызова, совместимого с [перераспределениями](/cpp/c-runtime-library/reference/realloc?view=vs-2019) .</span><span class="sxs-lookup"><span data-stu-id="c3a21-227">That memory should be freed through the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="c3a21-228">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c3a21-228">No change to the database state will occur.</span></span>

<span data-ttu-id="c3a21-229">При сбое ни один из запрошенных данных не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="c3a21-229">On failure, none of the requested data will be returned.</span></span> <span data-ttu-id="c3a21-230">Память, выделенная во время вызова, будет освобождена автоматически с помощью указанного обратного вызова [, совместимого](/cpp/c-runtime-library/reference/realloc?view=vs-2019) с перераспределением.</span><span class="sxs-lookup"><span data-stu-id="c3a21-230">Any memory that was allocated during the call will be freed automatically using the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="c3a21-231">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c3a21-231">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c3a21-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3a21-232">Remarks</span></span>

<span data-ttu-id="c3a21-233">Если перечисляются все значения столбцов в записи и вы не указали JET_bitEnumerateIgnoreDefaults то предположить, что столбец или значение столбца с кодом состояния JET_wrnColumnNull не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="c3a21-233">If you are enumerating all column values in the record and you did not specify JET_bitEnumerateIgnoreDefaults then you cannot assume that you will never see a column or column value with a status code of JET_wrnColumnNull.</span></span> <span data-ttu-id="c3a21-234">Этот код состояния можно увидеть, если столбец имеет значение по умолчанию и явно установил значение **null** или если столбец является неразреженным (например, фиксированный или переменный столбец).</span><span class="sxs-lookup"><span data-stu-id="c3a21-234">You can see this status code if a column has a default value and was explicitly set to **NULL** or if the column is a non-sparse column (for example, a fixed or variable column).</span></span>

<span data-ttu-id="c3a21-235">Параметр *кбдатамост* не применяется ко всем значениям столбцов.</span><span class="sxs-lookup"><span data-stu-id="c3a21-235">The *cbDataMost* parameter does not apply to all column values.</span></span> <span data-ttu-id="c3a21-236">Этот параметр усекает только длинные текстовые и длинные двоичные значения столбцов, которые настолько велики, что они хранились отдельно от записи.</span><span class="sxs-lookup"><span data-stu-id="c3a21-236">This parameter will only truncate long text and long binary column values that are so large that they have been stored separately from the record.</span></span>

<span data-ttu-id="c3a21-237">Если **жетенумератеколумнс** возвращает данные в выходных параметрах, вызывающий объект отвечает за освобождение памяти в массиве, а также на любую память, на которую ссылаются указатели, внедренные в этот массив.</span><span class="sxs-lookup"><span data-stu-id="c3a21-237">If **JetEnumerateColumns** returns data in its output parameters then the caller is responsible for freeing the memory in the array as well as any memory referred to by pointers embedded in that array.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c3a21-238">Требования</span><span class="sxs-lookup"><span data-stu-id="c3a21-238">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-239"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c3a21-239"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c3a21-240">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3a21-240">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-241"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c3a21-241"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c3a21-242">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c3a21-242">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-243"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c3a21-243"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c3a21-244">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c3a21-244">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3a21-245"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="c3a21-245"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c3a21-246">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c3a21-246">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3a21-247"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="c3a21-247"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c3a21-248">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c3a21-248">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c3a21-249">См. также:</span><span class="sxs-lookup"><span data-stu-id="c3a21-249">See Also</span></span>

[<span data-ttu-id="c3a21-250">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c3a21-250">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c3a21-251">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c3a21-251">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c3a21-252">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c3a21-252">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c3a21-253">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c3a21-253">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c3a21-254">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="c3a21-254">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="c3a21-255">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="c3a21-255">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="c3a21-256">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="c3a21-256">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="c3a21-257">JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="c3a21-257">JET_PFNREALLOC</span></span>](./jet-pfnrealloc-callback-function.md)  
[<span data-ttu-id="c3a21-258">realloc</span><span class="sxs-lookup"><span data-stu-id="c3a21-258">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[<span data-ttu-id="c3a21-259">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="c3a21-259">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="c3a21-260">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="c3a21-260">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
