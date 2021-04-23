---
description: 'Дополнительные сведения: структура JET_SETCOLUMN'
title: Структура JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809040"
---
# <a name="jet_setcolumn-structure"></a><span data-ttu-id="bace5-103">Структура JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="bace5-103">JET_SETCOLUMN Structure</span></span>


<span data-ttu-id="bace5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bace5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setcolumn-structure"></a><span data-ttu-id="bace5-105">Структура JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="bace5-105">JET_SETCOLUMN Structure</span></span>

<span data-ttu-id="bace5-106">Структура **JET_SETCOLUMN** содержит входные и выходные параметры для [жетсетколумнс](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bace5-106">The **JET_SETCOLUMN** structure contains input and output parameters for [JetSetColumns](./jetsetcolumns-function.md).</span></span> <span data-ttu-id="bace5-107">Поля в структуре описывают, какое значение столбца следует задать, как задать его и где можно получить данные набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="bace5-107">Fields in the structure describe what column value to set, how to set it, and where to get the column set data.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a><span data-ttu-id="bace5-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="bace5-108">Members</span></span>

<span data-ttu-id="bace5-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="bace5-109">**columnid**</span></span>

<span data-ttu-id="bace5-110">Идентификатор столбца для устанавливаемого столбца.</span><span class="sxs-lookup"><span data-stu-id="bace5-110">The column identifier for a column to set.</span></span>

<span data-ttu-id="bace5-111">**пвдата**</span><span class="sxs-lookup"><span data-stu-id="bace5-111">**pvData**</span></span>

<span data-ttu-id="bace5-112">Указатель на данные, которые необходимо задать в столбце.</span><span class="sxs-lookup"><span data-stu-id="bace5-112">A pointer to data to set into a column.</span></span>

<span data-ttu-id="bace5-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="bace5-113">**cbData**</span></span>

<span data-ttu-id="bace5-114">Размер выделения в байтах, начиная с **пвдата** в байтах.</span><span class="sxs-lookup"><span data-stu-id="bace5-114">The size of allocation, in bytes, starting at **pvData** in bytes.</span></span>

<span data-ttu-id="bace5-115">**грбит**</span><span class="sxs-lookup"><span data-stu-id="bace5-115">**grbit**</span></span>

<span data-ttu-id="bace5-116">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bace5-116">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bace5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bace5-117">Value</span></span></p></th>
<th><p><span data-ttu-id="bace5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bace5-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bace5-119">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="bace5-119">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="bace5-120">Добавляет данные в столбец типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="bace5-120">Appends data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="bace5-121">Аналогичное поведение можно добиться, определив размер существующего длинного значения и указав <strong>иблонгвалуе</strong> в <strong>псетинфо</strong>.</span><span class="sxs-lookup"><span data-stu-id="bace5-121">The same behavior can be achieved by determining the size of the existing long value and specifying <strong>ibLongValue</strong> in <strong>psetinfo</strong>.</span></span> <span data-ttu-id="bace5-122">Однако проще использовать этот <em>грбит</em>, так как знание размера существующего значения столбца не требуется.</span><span class="sxs-lookup"><span data-stu-id="bace5-122">However, it's simpler to use this <em>grbit</em>, since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bace5-123">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="bace5-123">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="bace5-124">Заменяет существующее длинное значение новыми данными.</span><span class="sxs-lookup"><span data-stu-id="bace5-124">Replaces the existing long value with the new data.</span></span> <span data-ttu-id="bace5-125">При использовании этого параметра, как будто существующее длинное значение было установлено равным 0 (нулю), перед установкой новых данных.</span><span class="sxs-lookup"><span data-stu-id="bace5-125">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bace5-126">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="bace5-126">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="bace5-127">Интерпретирует входной буфер как целое число байтов, чтобы задать в качестве длины длинного значения, описываемого значением columnid, и если оно предоставлено, порядковый номер в псетинфо- &gt; итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="bace5-127">Interprets the input buffer as an integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="bace5-128">Если указанный размер больше значения существующего столбца, столбец будет расширен с помощью нулей.</span><span class="sxs-lookup"><span data-stu-id="bace5-128">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="bace5-129">Если размер меньше значения существующего столбца, то значение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="bace5-129">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bace5-130">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="bace5-130">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="bace5-131">Задает нулевую длину значения.</span><span class="sxs-lookup"><span data-stu-id="bace5-131">Sets a value to zero length.</span></span> <span data-ttu-id="bace5-132">Как правило, значение столбца устанавливается равным NULL путем передачи Кбмакс 0.</span><span class="sxs-lookup"><span data-stu-id="bace5-132">Normally, a column value is set to NULL by passing a cbMax of 0.</span></span> <span data-ttu-id="bace5-133">Однако для некоторых типов, например <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, значение столбца может быть равно 0, а не NULL, и этот параметр используется для РАЗЛИЧЕНИЯ значений NULL и нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="bace5-133">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 length instead of NULL, and this option is used to differentiate between NULL and 0 length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bace5-134">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="bace5-134">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="bace5-135">Принудительное хранение длинных значений, столбцов типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, которые хранятся отдельно от оставшейся части данных записи.</span><span class="sxs-lookup"><span data-stu-id="bace5-135">Forces a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="bace5-136">Обычно это происходит, когда размер длинного значения предотвращает сохранение его с помощью оставшихся данных записи.</span><span class="sxs-lookup"><span data-stu-id="bace5-136">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="bace5-137">Однако этот параметр можно использовать для принудительного сохранения длинного значения.</span><span class="sxs-lookup"><span data-stu-id="bace5-137">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="bace5-138">Обратите внимание, что значения типа Long, равные четырем байтам, не могут быть принудительно отделены.</span><span class="sxs-lookup"><span data-stu-id="bace5-138">Note that long values four bytes in size or smaller cannot be forced to be separate.</span></span> <span data-ttu-id="bace5-139">В таких случаях параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bace5-139">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bace5-140">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="bace5-140">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="bace5-141">Применяет уникальные значения в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="bace5-141">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="bace5-142">Этот параметр сравнивает данные исходного столбца без преобразований с другими существующими значениями столбцов, и при обнаружении дубликата возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="bace5-142">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="bace5-143">Если этот параметр задан, также нельзя указывать JET_bitSetAppendLv, JET_bitSetOverwriteLV и JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="bace5-143">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bace5-144">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="bace5-144">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="bace5-145">Применяет уникальные значения в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="bace5-145">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="bace5-146">Этот параметр сравнивает ключевое нормализованное преобразование данных столбца с другими аналогичными преобразованными значениями столбцов, и при обнаружении дубликата возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="bace5-146">This option compares the key normalized transformation of column data to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="bace5-147">Если этот параметр задан, также нельзя указывать JET_bitSetAppendLv, JET_bitSetOverwriteLV и JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="bace5-147">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bace5-148">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="bace5-148">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="bace5-149">Приводит к тому, что столбец возвращает значение столбца по умолчанию при последующих операциях получения столбца.</span><span class="sxs-lookup"><span data-stu-id="bace5-149">Causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="bace5-150">Все существующие значения столбцов удаляются.</span><span class="sxs-lookup"><span data-stu-id="bace5-150">All existing column values are removed.</span></span> <span data-ttu-id="bace5-151">Этот параметр применим только к столбцам с тегами, разреженным или многозначным.</span><span class="sxs-lookup"><span data-stu-id="bace5-151">This option is only applicable for tagged, sparse, or multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bace5-152">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="bace5-152">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="bace5-153">Сохраняет значение Long, столбцы типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или JET_coltypeLongBinary, сохраняя при возможности оставшиеся данные записи.</span><span class="sxs-lookup"><span data-stu-id="bace5-153">Keeps the long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or JET_coltypeLongBinary, stored with the remaining record data if possible.</span></span> <span data-ttu-id="bace5-154">Обычно длинные столбцы хранятся отдельно, если их длина превышает 1024 байт или в противном случае длина записи превысит ограничение размера страницы.</span><span class="sxs-lookup"><span data-stu-id="bace5-154">Normally, long columns are stored separately when their length exceeds 1024 bytes or would otherwise cause the record length to exceed its page size related size limitation.</span></span> <span data-ttu-id="bace5-155">Однако если этот параметр задан, операция задания столбца завершится с ошибкой JET_errColumnTooBig вместо того, чтобы хранить значение этого столбца отдельно от оставшихся данных записи.</span><span class="sxs-lookup"><span data-stu-id="bace5-155">However, if this option is set, the set column operation will fail with error JET_errColumnTooBig rather than store this column value separate from the remaining record data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bace5-156">**иблонгвалуе**</span><span class="sxs-lookup"><span data-stu-id="bace5-156">**ibLongValue**</span></span>

<span data-ttu-id="bace5-157">Смещение для первого байта, получаемого из столбца типа [JET_coltypLongBinary](./jet-coltyp.md)или [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="bace5-157">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="bace5-158">**итагсекуенце**</span><span class="sxs-lookup"><span data-stu-id="bace5-158">**itagSequence**</span></span>

<span data-ttu-id="bace5-159">Описывает порядковый номер значения в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="bace5-159">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="bace5-160">Значение **итагсекуенце** , равное 0, указывает, что набор значений столбца должен быть добавлен в качестве нового экземпляра многозначного столбца.</span><span class="sxs-lookup"><span data-stu-id="bace5-160">An **itagSequence** of 0 indicates that the column value set should be added as a new instance of a multi-valued column.</span></span>

<span data-ttu-id="bace5-161">**Err**</span><span class="sxs-lookup"><span data-stu-id="bace5-161">**err**</span></span>

<span data-ttu-id="bace5-162">Коды ошибок и предупреждения, возвращаемые операцией Set Column.</span><span class="sxs-lookup"><span data-stu-id="bace5-162">Error codes and warnings returned from the set column operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="bace5-163">Требования</span><span class="sxs-lookup"><span data-stu-id="bace5-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bace5-164"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="bace5-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bace5-165">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bace5-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bace5-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bace5-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bace5-167">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bace5-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bace5-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bace5-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bace5-169">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bace5-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bace5-170">См. также:</span><span class="sxs-lookup"><span data-stu-id="bace5-170">See Also</span></span>

[<span data-ttu-id="bace5-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="bace5-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="bace5-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="bace5-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="bace5-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bace5-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bace5-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bace5-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bace5-175">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="bace5-175">JetSetColumns</span></span>](./jetsetcolumns-function.md)
