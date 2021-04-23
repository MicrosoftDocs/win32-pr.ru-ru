---
description: Дополнительные сведения о функции Жетсетколумн
title: Функция JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701651"
---
# <a name="jetsetcolumn-function"></a><span data-ttu-id="52480-103">Функция JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="52480-103">JetSetColumn Function</span></span>


<span data-ttu-id="52480-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="52480-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumn-function"></a><span data-ttu-id="52480-105">Функция JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="52480-105">JetSetColumn Function</span></span>

<span data-ttu-id="52480-106">Функция **жетсетколумн** изменяет значение одного столбца в изменяемой записи, которое вставляется, или обновляет текущую запись.</span><span class="sxs-lookup"><span data-stu-id="52480-106">The **JetSetColumn** function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="52480-107">Он может перезаписать существующее значение, добавить новое значение в последовательность значений в столбце с несколькими значениями, удалить значение из последовательности значений в многозначном столбце или обновить все или часть длинного значения, столбца типа [JET_coltypLongText](./jet-coltyp.md) или [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="52480-107">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value, a column of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="52480-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52480-108">Parameters</span></span>

<span data-ttu-id="52480-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="52480-109">*sesid*</span></span>

<span data-ttu-id="52480-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="52480-110">The session to use for this call.</span></span>

<span data-ttu-id="52480-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="52480-111">*tableid*</span></span>

<span data-ttu-id="52480-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="52480-112">The cursor to use for this call.</span></span>

<span data-ttu-id="52480-113">*columnid*</span><span class="sxs-lookup"><span data-stu-id="52480-113">*columnid*</span></span>

<span data-ttu-id="52480-114">[JET_COLUMNID](./jet-columnid.md) извлекаемого столбца.</span><span class="sxs-lookup"><span data-stu-id="52480-114">The [JET_COLUMNID](./jet-columnid.md) of the column to be retrieved.</span></span> <span data-ttu-id="52480-115">Кроме того, может быть задано значение *columnid* , равное 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="52480-115">Alternatively, a *columnid* value of 0 (zero) can be given.</span></span> <span data-ttu-id="52480-116">Если задано значение *columnid* 0 (ноль), все столбцы с тегами, разреженные и Многозначные столбцы рассматриваются как один столбец.</span><span class="sxs-lookup"><span data-stu-id="52480-116">When *columnid* 0 (zero) is given, all tagged columns, sparse and multi-valued columns, are treated as a single column.</span></span> <span data-ttu-id="52480-117">Это упрощает извлечение всех разреженных столбцов, имеющихся в записи.</span><span class="sxs-lookup"><span data-stu-id="52480-117">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="52480-118">*пвдата*</span><span class="sxs-lookup"><span data-stu-id="52480-118">*pvData*</span></span>

<span data-ttu-id="52480-119">Входной буфер, содержащий данные, используемые для значения столбца.</span><span class="sxs-lookup"><span data-stu-id="52480-119">Input buffer containing data to use for column value.</span></span>

<span data-ttu-id="52480-120">*cbData*</span><span class="sxs-lookup"><span data-stu-id="52480-120">*cbData*</span></span>

<span data-ttu-id="52480-121">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="52480-121">Size in bytes of the input buffer.</span></span>

<span data-ttu-id="52480-122">*грбит*</span><span class="sxs-lookup"><span data-stu-id="52480-122">*grbit*</span></span>

<span data-ttu-id="52480-123">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, в том числе ноль или более следующих:</span><span class="sxs-lookup"><span data-stu-id="52480-123">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52480-124">Значение</span><span class="sxs-lookup"><span data-stu-id="52480-124">Value</span></span></p></th>
<th><p><span data-ttu-id="52480-125">Значение</span><span class="sxs-lookup"><span data-stu-id="52480-125">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52480-126">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="52480-126">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="52480-127">Этот параметр используется для добавления данных в столбец типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="52480-127">This option is used to append data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="52480-128">Аналогичное поведение можно добиться, определив размер существующего длинного значения и указав <em>иблонгвалуе</em> в <em>псетинфо</em>.</span><span class="sxs-lookup"><span data-stu-id="52480-128">The same behavior can be achieved by determining the size of the existing long value and specifying <em>ibLongValue</em> in <em>psetinfo</em>.</span></span> <span data-ttu-id="52480-129">Однако проще использовать этот <em>грбит</em> , поскольку знание размера существующего значения столбца не требуется.</span><span class="sxs-lookup"><span data-stu-id="52480-129">However, it's simpler to use this <em>grbit</em> since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-130">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="52480-130">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="52480-131">Этот параметр используется для замены существующего длинного значения новыми предоставленными данными.</span><span class="sxs-lookup"><span data-stu-id="52480-131">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="52480-132">При использовании этого параметра, как будто существующее длинное значение было установлено равным 0 (нулю), перед установкой новых данных.</span><span class="sxs-lookup"><span data-stu-id="52480-132">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-133">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="52480-133">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="52480-134">Этот параметр применим только к столбцам с тегами, разреженным или многозначным.</span><span class="sxs-lookup"><span data-stu-id="52480-134">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="52480-135">Это приводит к тому, что столбец возвращает значение столбца по умолчанию при последующих операциях получения столбца.</span><span class="sxs-lookup"><span data-stu-id="52480-135">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="52480-136">Все существующие значения столбцов удаляются.</span><span class="sxs-lookup"><span data-stu-id="52480-136">All existing column values are removed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-137">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="52480-137">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="52480-138">Этот параметр используется для принудительного хранения длинных значений, столбцов типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, которые хранятся отдельно от оставшейся части данных записи.</span><span class="sxs-lookup"><span data-stu-id="52480-138">This option is used to force a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="52480-139">Обычно это происходит, когда размер длинного значения предотвращает сохранение его с помощью оставшихся данных записи.</span><span class="sxs-lookup"><span data-stu-id="52480-139">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="52480-140">Однако этот параметр можно использовать для принудительного сохранения длинного значения.</span><span class="sxs-lookup"><span data-stu-id="52480-140">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="52480-141">Обратите внимание, что значения long размером четыре байта меньше не могут быть разными.</span><span class="sxs-lookup"><span data-stu-id="52480-141">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="52480-142">В таких случаях параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="52480-142">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-143">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="52480-143">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="52480-144">Этот параметр используется для интерпретации входного буфера в виде целого числа байтов, устанавливаемого в качестве длины длинного значения, описываемого значением <em>columnid</em> , и если оно предоставлено, порядковый номер в псетинфо- &gt; итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="52480-144">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given <em>columnid</em> and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="52480-145">Если указанный размер больше значения существующего столбца, столбец будет расширен с помощью нулей.</span><span class="sxs-lookup"><span data-stu-id="52480-145">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="52480-146">Если размер меньше значения существующего столбца, то значение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="52480-146">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-147">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="52480-147">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="52480-148">Этот параметр используется, чтобы обеспечить уникальность всех значений в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="52480-148">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="52480-149">Этот параметр сравнивает данные исходного столбца без преобразований с другими существующими значениями столбцов, и при обнаружении дубликата возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="52480-149">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="52480-150">Если указан этот параметр, то не могут быть также указаны JET_bitSetAppendLV, JET_bitSetOverwriteLV и JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="52480-150">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-151">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="52480-151">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="52480-152">Этот параметр используется, чтобы обеспечить уникальность всех значений в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="52480-152">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="52480-153">Этот параметр сравнивает ключевое нормализованное преобразование данных столбца с другими аналогично преобразованными значениями столбцов, и при обнаружении дубликата возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="52480-153">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="52480-154">Если указан этот параметр, то не могут быть также указаны JET_bitSetAppendLV, JET_bitSetOverwriteLV и JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="52480-154">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-155">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="52480-155">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="52480-156">Этот параметр используется для задания значения нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="52480-156">This option is used to set a value to zero length.</span></span> <span data-ttu-id="52480-157">Как правило, значение столбца устанавливается равным <strong>null</strong> путем передачи кбмакс 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="52480-157">Normally, a column value is set to <strong>NULL</strong> by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="52480-158">Однако для некоторых типов, таких как <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, значение столбца может быть равно 0 (нулевой) длине, а не <strong>null</strong>, и этот параметр используется для различения длины, <strong>равной null</strong> , и 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="52480-158">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 (zero) length instead of <strong>NULL</strong>, and this option is used to differentiate between <strong>NULL</strong> and 0 (zero) length.</span></span></p>
<p><span data-ttu-id="52480-159"><strong>Примечание</strong>  .  В общем случае, если столбец является столбцом фиксированной длины, этот бит игнорируется, а для столбца устанавливается значение <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="52480-159"><strong>Note</strong>  In general, if the column is a fixed-length column, this bit is ignored and the column is set to <strong>NULL</strong>.</span></span> <span data-ttu-id="52480-160">Однако если столбец является столбцом с фиксированной длиной, длина столбца устанавливается равным 0.</span><span class="sxs-lookup"><span data-stu-id="52480-160">However, if the column is a fixed-length tagged column, the column length is set to 0.</span></span> <span data-ttu-id="52480-161">Если столбец с меткой фиксированной длины имеет значение 0, попытки получить столбец с <a href="gg269198(v=exchg.10).md">жетретриевеколумн</a> или <a href="gg294135(v=exchg.10).md">жетретриевеколумнс</a> будут выполнены, но фактическая длина, возвращаемая в параметре <em>кбактуал</em> , равна 0.</span><span class="sxs-lookup"><span data-stu-id="52480-161">When the fixed-length tagged column is set to 0 length, attempts to retrieve the column with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> will succeed, but the actual length that is returned in the <em>cbActual</em> parameter is 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-162">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="52480-162">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="52480-163">Этот параметр используется для хранения всего длинного значения в записи.</span><span class="sxs-lookup"><span data-stu-id="52480-163">This option is used to store the entire long value in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-164">JET_bitSetCompressed</span><span class="sxs-lookup"><span data-stu-id="52480-164">JET_bitSetCompressed</span></span></p></td>
<td><p><span data-ttu-id="52480-165">Этот параметр используется для попытки сжатия данных при хранении данных.</span><span class="sxs-lookup"><span data-stu-id="52480-165">This option is used to attempt data compression when storing the data.</span></span></p>
<p><span data-ttu-id="52480-166"><strong>Windows 7:</strong>  JET_bitSetCompressed введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52480-166"><strong>Windows 7:</strong>  JET_bitSetCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-167">JET_bitSetUncompressed</span><span class="sxs-lookup"><span data-stu-id="52480-167">JET_bitSetUncompressed</span></span></p></td>
<td><p><span data-ttu-id="52480-168">Этот параметр используется для попыток сжатия при сохранении данных.</span><span class="sxs-lookup"><span data-stu-id="52480-168">This option is used not attempt compression when storing the data.</span></span></p>
<p><span data-ttu-id="52480-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52480-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52480-170">*псетинфо*</span><span class="sxs-lookup"><span data-stu-id="52480-170">*psetinfo*</span></span>

<span data-ttu-id="52480-171">Указатель на необязательные входные параметры, которые могут быть установлены для этой функции с помощью структуры [JET_SETINFO](./jet-setinfo-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="52480-171">Pointer to optional input parameters that can be set for this function using the [JET_SETINFO](./jet-setinfo-structure.md) structure.</span></span>

<span data-ttu-id="52480-172">Если *псетинфо* имеет **значение NULL** , функция ведет себя так, как будто *итагсекуенце* равен 1 и *иблонгвалуе* 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="52480-172">If *psetinfo* is given as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="52480-173">Это приводит к тому, что набор столбцов устанавливает первое значение многозначного столбца, а также для задания длинных данных, начиная со смещения 0 (нуля).</span><span class="sxs-lookup"><span data-stu-id="52480-173">This causes column set to set the first value of a multi-valued column, and to set long data beginning at offset 0 (zero).</span></span>

<span data-ttu-id="52480-174">Для этого параметра можно задать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="52480-174">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52480-175">Значение</span><span class="sxs-lookup"><span data-stu-id="52480-175">Value</span></span></p></th>
<th><p><span data-ttu-id="52480-176">Значение</span><span class="sxs-lookup"><span data-stu-id="52480-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52480-177">иблонгвалуе</span><span class="sxs-lookup"><span data-stu-id="52480-177">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="52480-178">Двоичное смещение в длинное значение столбца, где должны начинаться наборы данных.</span><span class="sxs-lookup"><span data-stu-id="52480-178">Binary offset into a long column value where set data should begin.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-179">итагсекуенце</span><span class="sxs-lookup"><span data-stu-id="52480-179">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="52480-180">Порядковый номер нужного значения столбца с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="52480-180">Sequence number of the desired multi-valued column value to set.</span></span> <span data-ttu-id="52480-181">Если <em>итагсекуенце</em> имеет значение 0 (ноль), то указанное значение должно быть добавлено к концу последовательности многозначных значений.</span><span class="sxs-lookup"><span data-stu-id="52480-181">If <em>itagSequence</em> is set to 0 (zero), then the value provided should be appended to then end of the sequence of multi-valued values.</span></span> <span data-ttu-id="52480-182">Если указанный порядковый номер больше, чем последнее существующее Многозначное значение, то к концу последовательности значений добавляется указанное значение.</span><span class="sxs-lookup"><span data-stu-id="52480-182">If the sequence number provided is greater than the last existing multi-valued value, then again the given value is appended to the end of the sequence of values.</span></span> <span data-ttu-id="52480-183">Если порядковый номер соответствует существующему значению, то это значение заменяется заданным значением.</span><span class="sxs-lookup"><span data-stu-id="52480-183">If the sequence number corresponds to an existing value then that value is replaced with the given value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="52480-184">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52480-184">Return Value</span></span>

<span data-ttu-id="52480-185">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="52480-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="52480-186">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="52480-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52480-187">Код возврата</span><span class="sxs-lookup"><span data-stu-id="52480-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="52480-188">Описание</span><span class="sxs-lookup"><span data-stu-id="52480-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52480-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="52480-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="52480-190">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="52480-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-191">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="52480-191">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="52480-192">Указанный идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="52480-192">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-193">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="52480-193">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="52480-194">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="52480-194">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-195">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="52480-195">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="52480-196">Столбец, описываемый данным <em>columnid</em> , не существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="52480-196">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-197">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="52480-197">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="52480-198">Предпринята недопустимая попытка обновить значение Long во время операции вставки копирования удаление исходного обновления.</span><span class="sxs-lookup"><span data-stu-id="52480-198">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-199">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="52480-199">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="52480-200">Данные значений столбцов, заданных во входном буфере, превышают ограничение по размеру либо естественным для столбца фиксированной длины, либо настроены для текстовых или двоичных столбцов фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="52480-200">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="52480-201">Эта ошибка также возвращается при передаче более 1024 байт данных для длинного столбца и установке флага JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="52480-201">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-202">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="52480-202">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="52480-203">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="52480-203">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="52480-204"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="52480-204"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-205">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="52480-205">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="52480-206">Заданный размер данных значения столбца не соответствует типу данных фиксированной длины, который является естественным.</span><span class="sxs-lookup"><span data-stu-id="52480-206">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-207">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="52480-207">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="52480-208">Предпринята недопустимая попытка обновить столбец автоинкремента во время операции вставки или обновления либо обновить столбец версии во время операции замены.</span><span class="sxs-lookup"><span data-stu-id="52480-208">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-209">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="52480-209">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="52480-210">Указанные параметры неизвестны или являются недопустимым сочетанием известных битовых параметров.</span><span class="sxs-lookup"><span data-stu-id="52480-210">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-211">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="52480-211">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="52480-212">Заданный псетинфо- &gt; кбструкт не является допустимым размером для структуры <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="52480-212">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-213">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="52480-213">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="52480-214">Операция задания столбца попыталась создать повторяющееся значение и указать либо JET_bitSetUniqueMultiValues, либо JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="52480-214">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-215">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="52480-215">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="52480-216">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="52480-216">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-217">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="52480-217">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="52480-218">Предпринята недопустимая попытка обновить значение длинного столбца, если вызывающий сеанс не был в транзакции.</span><span class="sxs-lookup"><span data-stu-id="52480-218">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-219">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="52480-219">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="52480-220">Предпринята недопустимая попытка установить<strong>ненулевое</strong> значение <strong>null</strong>для столбца.</span><span class="sxs-lookup"><span data-stu-id="52480-220">An illegal attempt was made to set a non-<strong>NULL</strong> column to <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-221">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="52480-221">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="52480-222">То же, что и JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="52480-222">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-223">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="52480-223">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="52480-224">Значение столбца не может быть присвоено значению во входном буфере, так как оно привело к превышению ограничения на размер страницы.</span><span class="sxs-lookup"><span data-stu-id="52480-224">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="52480-225">Столбцы типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> можно хранить отдельно от оставшихся данных записи.</span><span class="sxs-lookup"><span data-stu-id="52480-225">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="52480-226">Однако другие столбцы должны храниться вместе с записью, что может привести к превышению ограничения на размер записи.</span><span class="sxs-lookup"><span data-stu-id="52480-226">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="52480-227">Даже для длинных столбцов требуется 5-байтное пространство внутри записи в качестве компоновки, что также может привести к возвращению JET_errRecordTooBig.</span><span class="sxs-lookup"><span data-stu-id="52480-227">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="52480-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="52480-229">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="52480-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="52480-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="52480-231">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="52480-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="52480-232"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="52480-232"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="52480-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="52480-234">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="52480-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-235">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="52480-235">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="52480-236">Курсор в настоящее время не находится в процессе вставки новой записи или обновления существующей записи.</span><span class="sxs-lookup"><span data-stu-id="52480-236">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-237">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="52480-237">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="52480-238">Эта ошибка возникает, если настроенный размер хранилища версий недостаточно для хранения всех необработанных обновлений.</span><span class="sxs-lookup"><span data-stu-id="52480-238">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-239">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="52480-239">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="52480-240">Значение столбца во входном буфере превысило максимальную заданную длину для столбца переменной длины и было усечено.</span><span class="sxs-lookup"><span data-stu-id="52480-240">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52480-241">При успешном завершении требуемая часть значения столбца для данного столбца задается данными, скопированными из входного буфера.</span><span class="sxs-lookup"><span data-stu-id="52480-241">On success, the desired portion of a column value for the given column is set with data copied from the input buffer.</span></span> <span data-ttu-id="52480-242">Возможно, набор данных был усечен, если превышена максимальная длина, указанная для столбца переменной длины.</span><span class="sxs-lookup"><span data-stu-id="52480-242">The data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="52480-243">В случае сбоя положение курсора остается неизменным, и данные значения столбца не обновляются в буфере копирования.</span><span class="sxs-lookup"><span data-stu-id="52480-243">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="52480-244">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52480-244">Remarks</span></span>

<span data-ttu-id="52480-245">Задание значений типа Long, значения для столбцов [JET_coltypLongBinary](./jet-coltyp.md) типов [JET_coltypLongText](./jet-coltyp.md) или [JET_coltypLongBinary](./jet-coltyp.md), должно выполняться только в том случае, если вызывающий сеанс находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="52480-245">Setting long values, values for columns [JET_coltypLongBinary](./jet-coltyp.md) of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md), should be done only when the calling session is in a transaction.</span></span> <span data-ttu-id="52480-246">Если вызывающий сеанс не находится в транзакции, изменения длинных значений, которые хранятся отдельно, могут быть зафиксированы полностью даже после отмены операции обновления.</span><span class="sxs-lookup"><span data-stu-id="52480-246">If the calling session is not in a transaction, modifications to long values which are stored separately may be committed fully even when the update operation is later cancelled.</span></span> <span data-ttu-id="52480-247">Если вызывающий сеанс находится в транзакции, то результаты обновления можно полностью откатить, отменив обновление и выполнив откат транзакции сеанса.</span><span class="sxs-lookup"><span data-stu-id="52480-247">If the calling session is in a transaction, then the effects of the update can be fully rolled back by canceling the update and rolling back the session transaction.</span></span>

<span data-ttu-id="52480-248">Обновления индекса не выполняются в результате операций **жетсетколумн** .</span><span class="sxs-lookup"><span data-stu-id="52480-248">Index updates are not performed as a result of **JetSetColumn** operations.</span></span> <span data-ttu-id="52480-249">Вместо этого индексы обновляются только после завершения всех изменений столбцов и вызова [жетупдате](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="52480-249">Instead, indexes are updated only after all column modifications are complete and [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="52480-250">Это позволяет наиболее эффективно обновлять индексы, если индексы содержат более одного изменяемого столбца.</span><span class="sxs-lookup"><span data-stu-id="52480-250">This permits the most efficient updating of indexes when indexes involve more than one column being modified.</span></span>

<span data-ttu-id="52480-251">Размер записи ограничен в зависимости от размера страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="52480-251">A record is limited in size based on the database page size.</span></span> <span data-ttu-id="52480-252">Все длинные значения в записи больше пяти байт будут храниться отдельно от записи, если данные в записи превышают предел в результате операции **жетсетколумн** .</span><span class="sxs-lookup"><span data-stu-id="52480-252">Any long values in the record larger than five bytes will be stored separate from the record should the data in the record exceed its limit as a result of a **JetSetColumn** operation.</span></span> <span data-ttu-id="52480-253">JET_errRecordTooBig об ошибке будет возвращен только после того, как все данные столбца записи отделяемых будут сохранены отдельно от записи, а запись по-прежнему превышает предельный размер записи.</span><span class="sxs-lookup"><span data-stu-id="52480-253">The error JET_errRecordTooBig will only be returned after all separable record column data has been stored separately from the record and the record still exceeds the record size limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="52480-254">Требования</span><span class="sxs-lookup"><span data-stu-id="52480-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52480-255"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="52480-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="52480-256">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="52480-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="52480-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="52480-258">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="52480-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="52480-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="52480-260">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="52480-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52480-261"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="52480-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="52480-262">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="52480-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52480-263"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="52480-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="52480-264">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="52480-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="52480-265">См. также:</span><span class="sxs-lookup"><span data-stu-id="52480-265">See Also</span></span>

[<span data-ttu-id="52480-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="52480-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="52480-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="52480-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="52480-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="52480-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="52480-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="52480-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="52480-270">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="52480-270">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="52480-271">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="52480-271">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="52480-272">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="52480-272">JetSetColumns</span></span>](./jetsetcolumns-function.md)
