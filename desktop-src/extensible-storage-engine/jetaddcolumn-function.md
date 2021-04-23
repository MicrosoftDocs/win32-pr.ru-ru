---
description: Дополнительные сведения о функции Жетаддколумн
title: Функция JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719648"
---
# <a name="jetaddcolumn-function"></a><span data-ttu-id="62838-103">Функция JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="62838-103">JetAddColumn Function</span></span>


<span data-ttu-id="62838-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="62838-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetaddcolumn-function"></a><span data-ttu-id="62838-105">Функция JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="62838-105">JetAddColumn Function</span></span>

<span data-ttu-id="62838-106">Функция **жетаддколумн** добавляет новый столбец в существующую таблицу в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="62838-106">The **JetAddColumn** function adds a new column to an existing table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="62838-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="62838-107">Parameters</span></span>

<span data-ttu-id="62838-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="62838-108">*sesid*</span></span>

<span data-ttu-id="62838-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="62838-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="62838-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="62838-110">*tableid*</span></span>

<span data-ttu-id="62838-111">Таблица, в которую добавляется столбец.</span><span class="sxs-lookup"><span data-stu-id="62838-111">The table to which to add the column.</span></span>

<span data-ttu-id="62838-112">*сзколумннаме*</span><span class="sxs-lookup"><span data-stu-id="62838-112">*szColumnName*</span></span>

<span data-ttu-id="62838-113">Имя добавляемого столбца.</span><span class="sxs-lookup"><span data-stu-id="62838-113">The name of the column to add.</span></span> <span data-ttu-id="62838-114">Имя должно соответствовать следующим критериям:</span><span class="sxs-lookup"><span data-stu-id="62838-114">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="62838-115">Длина должна быть меньше JET_cbNameMost символов, не включая завершающее **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="62838-115">It must be fewer than JET_cbNameMost characters in length, not including the terminating **NULL**.</span></span>

  - <span data-ttu-id="62838-116">Он должен содержать только символы из следующих наборов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей квадратной скобки ( \] ), т. е. символов ASCII 0x20, 0x22 до 0x7F</span><span class="sxs-lookup"><span data-stu-id="62838-116">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="62838-117">Оно не может начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="62838-117">It cannot begin with a space.</span></span>

  - <span data-ttu-id="62838-118">Он должен содержать по крайней мере один символ, не являющийся пробелом.</span><span class="sxs-lookup"><span data-stu-id="62838-118">It must contain at least one non-space character.</span></span>

<span data-ttu-id="62838-119">*пколумндеф*</span><span class="sxs-lookup"><span data-stu-id="62838-119">*pcolumndef*</span></span>

<span data-ttu-id="62838-120">Указатель на структуру [JET_COLUMNDEF](./jet-columndef-structure.md) , которая определяет данные, которые могут храниться в столбце.</span><span class="sxs-lookup"><span data-stu-id="62838-120">A pointer to a [JET_COLUMNDEF](./jet-columndef-structure.md) structure, which defines the data that can be stored in a column.</span></span>

<span data-ttu-id="62838-121">*пвдефаулт*</span><span class="sxs-lookup"><span data-stu-id="62838-121">*pvDefault*</span></span>

<span data-ttu-id="62838-122">Указатель на буфер, содержащий значение по умолчанию для столбца.</span><span class="sxs-lookup"><span data-stu-id="62838-122">A pointer to a buffer that contains the default value for the column.</span></span> <span data-ttu-id="62838-123">Длина буфера равна **кбдефаулт**.</span><span class="sxs-lookup"><span data-stu-id="62838-123">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="62838-124">Если значение по умолчанию отсутствует, установите **пвдефаулт** в **значение NULL** и **кбдефаулт** в ноль.</span><span class="sxs-lookup"><span data-stu-id="62838-124">If there is no default, set **pvDefault** to **NULL** and **cbDefault** to zero.</span></span> <span data-ttu-id="62838-125">Значения по умолчанию не могут превышать JET_cbColumnMost байты для фиксированных столбцов или JET_cbLVDefaultValueMost байты для длинных значений.</span><span class="sxs-lookup"><span data-stu-id="62838-125">Default values cannot be larger than JET_cbColumnMost bytes for fixed columns or JET_cbLVDefaultValueMost bytes for long values.</span></span> <span data-ttu-id="62838-126">Если значение по умолчанию больше этого значения, оно будет обрезано без уведомления.</span><span class="sxs-lookup"><span data-stu-id="62838-126">If a default value is larger than that, it will be silently truncated.</span></span>

<span data-ttu-id="62838-127">Если *грбит* имеет JET_bitColumnUserDefinedDefault, **пвдефаулт** будет интерпретироваться как указатель на структуру [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="62838-127">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure.</span></span>

<span data-ttu-id="62838-128">*кбдефаулт*</span><span class="sxs-lookup"><span data-stu-id="62838-128">*cbDefault*</span></span>

<span data-ttu-id="62838-129">Размер (в байтах) буфера, указанного в **пвдефаулт**.</span><span class="sxs-lookup"><span data-stu-id="62838-129">The size, in bytes, of the buffer that is specified in **pvDefault**.</span></span>

<span data-ttu-id="62838-130">*пколумнид*</span><span class="sxs-lookup"><span data-stu-id="62838-130">*pcolumnid*</span></span>

<span data-ttu-id="62838-131">Указатель на структуру [JET_COLUMNID](./jet-columnid.md) , которая, в случае успеха, получит идентификатор только что созданного столбца.</span><span class="sxs-lookup"><span data-stu-id="62838-131">A pointer to a [JET_COLUMNID](./jet-columnid.md) structure, which, on success, will receive the identifier of the newly created column.</span></span> <span data-ttu-id="62838-132">При сбое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="62838-132">On failure, the value is undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="62838-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62838-133">Return Value</span></span>

<span data-ttu-id="62838-134">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="62838-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="62838-135">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="62838-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62838-136">Код возврата</span><span class="sxs-lookup"><span data-stu-id="62838-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="62838-137">Описание</span><span class="sxs-lookup"><span data-stu-id="62838-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62838-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="62838-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="62838-139">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="62838-139">The operation was successful.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-140">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="62838-140">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="62838-141">Была предпринята попытка изменить определение данных для фиксированной таблицы DDL.</span><span class="sxs-lookup"><span data-stu-id="62838-141">An attempt was made to modify the data definition of a fixed DDL table.</span></span> <span data-ttu-id="62838-142">Примером таблицы с фиксированной DDL-таблицей является таблица шаблонов.</span><span class="sxs-lookup"><span data-stu-id="62838-142">An example of a table with fixed DDL is a Template Table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="62838-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="62838-144">В API передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="62838-144">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="62838-145">Ниже приведены некоторые примеры недопустимых параметров.</span><span class="sxs-lookup"><span data-stu-id="62838-145">Some examples of invalid parameters are:</span></span></p>
<ul>
<li><p><span data-ttu-id="62838-146">Передача неправильного размера структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> в ее члене <em>кбструкт</em> .</span><span class="sxs-lookup"><span data-stu-id="62838-146">Passing in the wrong size of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure in its <em>cbStruct</em> member.</span></span></p></li>
<li><p><span data-ttu-id="62838-147">Передача JET_bitColumnUserDefinedDefault, но не установка <strong>кбдефаулт</strong> в sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="62838-147">Passing in JET_bitColumnUserDefinedDefault, but not setting <strong>cbDefault</strong> to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-148">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="62838-148">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="62838-149">Предпринята попытка добавить столбец с установленным битом JET_bitColumnUnversioned, но сеанс в данный момент находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="62838-149">An attempt was made to add a column with the JET_bitColumnUnversioned bit set, but the session is currently in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-150">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="62838-150">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="62838-151">Столбец уже существует.</span><span class="sxs-lookup"><span data-stu-id="62838-151">A column already exists.</span></span> <span data-ttu-id="62838-152">Предпринята попытка добавить столбец без сведений о версии, и этот столбец уже существует.</span><span class="sxs-lookup"><span data-stu-id="62838-152">An attempt was made to add a column without version information, and that column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-153">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="62838-153">JET_errTableNotEmpty</span></span></p></td>
<td><p><span data-ttu-id="62838-154">Таблица содержит данные.</span><span class="sxs-lookup"><span data-stu-id="62838-154">The table contains data.</span></span> <span data-ttu-id="62838-155">Столбец депонированного обновления можно добавить только в пустую таблицу.</span><span class="sxs-lookup"><span data-stu-id="62838-155">An Escrow Update column can only be added to an empty table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-156">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="62838-156">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="62838-157">Запись слишком велика.</span><span class="sxs-lookup"><span data-stu-id="62838-157">The record is too big.</span></span> <span data-ttu-id="62838-158">Сумма параметра <strong>кбмакс</strong> для фиксированных столбцов не должна превышать определенное значение.</span><span class="sxs-lookup"><span data-stu-id="62838-158">The sum of the <strong>cbMax</strong> parameter for the fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-159">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="62838-159">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="62838-160">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="62838-160">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="62838-161">Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="62838-161">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-162">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="62838-162">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="62838-163">Была предпринята попытка добавить избыточный столбец.</span><span class="sxs-lookup"><span data-stu-id="62838-163">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="62838-164">Не должно быть более одного столбца автоинкремента и не более одного столбца версий для каждой таблицы.</span><span class="sxs-lookup"><span data-stu-id="62838-164">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-165">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="62838-165">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="62838-166">Не удалось разрешить функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="62838-166">The callback function could not be resolved.</span></span> <span data-ttu-id="62838-167">Возможно, Библиотека DLL не найдена или не найдена функция в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="62838-167">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="62838-168">В журнале событий будут предоставлены дополнительные сведения, если включено достаточное протоколирование.</span><span class="sxs-lookup"><span data-stu-id="62838-168">The event log will provide more details if sufficient logging is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="62838-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="62838-170">Предупреждение, указывающее, что максимальная длина (<strong>кбмакс</strong>) фиксированного или переменного столбца превышает JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="62838-170">A warning indicating that the maximum length (<strong>cbMax</strong>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="62838-171">Это ограничение не применяется к длинным значениям ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> и <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="62838-171">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-172">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="62838-172">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="62838-173">Недопустимое имя передано в качестве <strong>сзколумннаме</strong>.</span><span class="sxs-lookup"><span data-stu-id="62838-173">An invalid name was passed as <strong>szColumnName</strong>.</span></span> <span data-ttu-id="62838-174">Дополнительные сведения об ограничениях см. в разделе критерии для <strong>сзколумннаме</strong>.</span><span class="sxs-lookup"><span data-stu-id="62838-174">For more information about the restrictions, see the criteria for <strong>szColumnName</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-175">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="62838-175">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="62838-176">Поле <strong>колтип</strong> не было задано как допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="62838-176">The <strong>coltyp</strong> field was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-177">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="62838-177">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="62838-178">Параметр <strong>CP</strong> структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не был задан как действительная кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="62838-178">The <strong>cp</strong> parameter of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="62838-179">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="62838-179">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="62838-180">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="62838-180">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-181">JET_errTaggedNotNULL</span><span class="sxs-lookup"><span data-stu-id="62838-181">JET_errTaggedNotNULL</span></span></p></td>
<td><p><span data-ttu-id="62838-182">JET_bitColumnNotNULL не может использоваться с тегами, длинными значениями или столбцами SLV.</span><span class="sxs-lookup"><span data-stu-id="62838-182">JET_bitColumnNotNULL cannot be used with tagged, Long Value, or SLV columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-183">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="62838-183">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="62838-184">Указано недопустимое сочетание <em>грбитс</em> .</span><span class="sxs-lookup"><span data-stu-id="62838-184">An invalid combination of <em>grbits</em> was specified.</span></span> <span data-ttu-id="62838-185">Вот некоторые из причин возникновения этой ошибки:</span><span class="sxs-lookup"><span data-stu-id="62838-185">Some of the reasons for this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="62838-186">JET_bitColumnFixed использовался для столбца с тегом, длинным значением или в столбце SLV.</span><span class="sxs-lookup"><span data-stu-id="62838-186">JET_bitColumnFixed was used on a tagged, Long Value, or SLV column.</span></span></p></li>
<li><p><span data-ttu-id="62838-187">JET_bitColumnEscrowUpdate был использован для столбца, который не был типа <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="62838-187">JET_bitColumnEscrowUpdate was used on a column that was not of type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="62838-188">JET_bitColumnEscrowUpdate использовался в столбце версии (JET_bitColumnVersion).</span><span class="sxs-lookup"><span data-stu-id="62838-188">JET_bitColumnEscrowUpdate was used on a Version column (JET_bitColumnVersion).</span></span></p></li>
<li><p><span data-ttu-id="62838-189">JET_bitColumnEscrowUpdate использовался в столбце Аутоинкремемнт (JET_bitColumnAutoincrement).</span><span class="sxs-lookup"><span data-stu-id="62838-189">JET_bitColumnEscrowUpdate was used on an AutoIncrememnt column (JET_bitColumnAutoincrement).</span></span></p></li>
<li><p><span data-ttu-id="62838-190">JET_bitColumnEscrowUpdate использовался для столбца, не имеющего значения по умолчанию (<strong>кбдефаулт</strong> равен нулю).</span><span class="sxs-lookup"><span data-stu-id="62838-190">JET_bitColumnEscrowUpdate was used on a column that did not have a default value (<strong>cbDefault</strong> was equal to zero).</span></span></p></li>
<li><p><span data-ttu-id="62838-191">JET_bitColumnFinalize использовался для столбца, который не является столбцом условно-обновления (JET_bitColumnEscrowUpdate не был задан).</span><span class="sxs-lookup"><span data-stu-id="62838-191">JET_bitColumnFinalize was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="62838-192">JET_bitColumnDeleteOnZero использовался для столбца, который не является столбцом условно-обновления (JET_bitColumnEscrowUpdate не был задан).</span><span class="sxs-lookup"><span data-stu-id="62838-192">JET_bitColumnDeleteOnZero was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="62838-193">JET_bitColumnAutoincrement использовался для столбца, который не был <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="62838-193">JET_bitColumnAutoincrement was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p>
<p><span data-ttu-id="62838-194"><strong>Windows 2000:  </strong> Эта причина для кода ошибки используется только в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="62838-194"><strong>Windows 2000:  </strong>This reason for the error code is used only in Windows 2000.</span></span></p>
<p><span data-ttu-id="62838-195">JET_bitColumnAutoincrement использовался для столбца, который не был ни <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> , ни <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span><span class="sxs-lookup"><span data-stu-id="62838-195">JET_bitColumnAutoincrement was used on a column that was neither <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nor <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span></span></p>
<p><span data-ttu-id="62838-196"><strong>Windows XP:  </strong> По этой причине код ошибки используется в операционных системах Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="62838-196"><strong>Windows XP:  </strong>This reason for the error code is used in Windows XP and later operating systems.</span></span></p></li>
<li><p><span data-ttu-id="62838-197">JET_bitColumnVersion использовался для столбца, который не был <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="62838-197">JET_bitColumnVersion was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="62838-198">JET_bitColumnVersion использовался в столбце AutoIncrement.</span><span class="sxs-lookup"><span data-stu-id="62838-198">JET_bitColumnVersion was used on an autoincrement column.</span></span></p></li>
<li><p><span data-ttu-id="62838-199">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="62838-199">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFixed.</span></span></p></li>
<li><p><span data-ttu-id="62838-200">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnNotNULL.</span><span class="sxs-lookup"><span data-stu-id="62838-200">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnNotNULL.</span></span></p></li>
<li><p><span data-ttu-id="62838-201">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="62838-201">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnVersion.</span></span></p></li>
<li><p><span data-ttu-id="62838-202">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="62838-202">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnAutoincrement.</span></span></p></li>
<li><p><span data-ttu-id="62838-203">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnUpdatable.</span><span class="sxs-lookup"><span data-stu-id="62838-203">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnUpdatable.</span></span></p></li>
<li><p><span data-ttu-id="62838-204">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="62838-204">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnEscrowUpdate.</span></span></p></li>
<li><p><span data-ttu-id="62838-205">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="62838-205">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFinalize.</span></span></p></li>
<li><p><span data-ttu-id="62838-206">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="62838-206">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnDeleteOnZero.</span></span></p></li>
<li><p><span data-ttu-id="62838-207">JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="62838-207">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnMaybeNull.</span></span></p></li>
<li><p><span data-ttu-id="62838-208">JET_bitColumnUserDefinedDefault использовался для столбца без тегов (с фиксированным или переменным).</span><span class="sxs-lookup"><span data-stu-id="62838-208">JET_bitColumnUserDefinedDefault was used on a non-tagged column (that is fixed or variable).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-209">JET_errMultiValuedColumnMustBeTagged</span><span class="sxs-lookup"><span data-stu-id="62838-209">JET_errMultiValuedColumnMustBeTagged</span></span></p></td>
<td><p><span data-ttu-id="62838-210">Столбец с несколькими значениями (JET_bitColumnMultiValued) может использоваться только для столбца с тегом или длинным значением (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="62838-210">A multi-valued column (JET_bitColumnMultiValued) can only be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-211">JET_errCannotBeTagged</span><span class="sxs-lookup"><span data-stu-id="62838-211">JET_errCannotBeTagged</span></span></p></td>
<td><p><span data-ttu-id="62838-212">Предпринята попытка использовать столбец с тегами, если столбец не может быть помечен.</span><span class="sxs-lookup"><span data-stu-id="62838-212">An attempt was made to use a tagged column when the column might not be tagged.</span></span> <span data-ttu-id="62838-213">Ниже перечислены некоторые ограничения, позволяющие разрешать столбцы с тегами.</span><span class="sxs-lookup"><span data-stu-id="62838-213">Some of the constraints for disallowing tagged columns are:</span></span></p>
<ul>
<li><p><span data-ttu-id="62838-214">Столбец депонированного обновления (JET_bitColumnEscrowUpdate) не может использоваться для столбца с тегом или длинным значением (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="62838-214">An Escrow Update column (JET_bitColumnEscrowUpdate) cannot be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></li>
<li><p><span data-ttu-id="62838-215">Столбец с автоувеличением может не помечаться тегами.</span><span class="sxs-lookup"><span data-stu-id="62838-215">An autoincrement column might not be tagged.</span></span></p></li>
<li><p><span data-ttu-id="62838-216">Столбец версии не может быть помечен.</span><span class="sxs-lookup"><span data-stu-id="62838-216">A Version column might not be tagged.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-217">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="62838-217">JET_errExclusiveTableLockRequired</span></span></p></td>
<td><p><span data-ttu-id="62838-218">Для этой операции требуется монопольная блокировка таблицы.</span><span class="sxs-lookup"><span data-stu-id="62838-218">An exclusive lock on the table was required for this operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-219">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="62838-219">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="62838-220">Предупреждение, указывающее, что максимальная длина (<em>кбмакс</em>) фиксированного или переменного столбца превышает JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="62838-220">A warning indicating that the maximum length (<em>cbMax</em>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="62838-221">Это ограничение не применяется к длинным значениям ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> и <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="62838-221">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="62838-222">Требования</span><span class="sxs-lookup"><span data-stu-id="62838-222">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62838-223"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="62838-223"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="62838-224">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="62838-224">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-225"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="62838-225"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="62838-226">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="62838-226">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-227"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="62838-227"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="62838-228">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="62838-228">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-229"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="62838-229"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="62838-230">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="62838-230">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62838-231"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="62838-231"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="62838-232">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="62838-232">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62838-233"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="62838-233"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="62838-234">Реализуется как <strong>жетаддколумнв</strong> (Юникод) и <strong>жетаддколумна</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="62838-234">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="62838-235">См. также:</span><span class="sxs-lookup"><span data-stu-id="62838-235">See Also</span></span>

[<span data-ttu-id="62838-236">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="62838-236">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="62838-237">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="62838-237">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="62838-238">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="62838-238">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="62838-239">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="62838-239">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="62838-240">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="62838-240">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="62838-241">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="62838-241">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="62838-242">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="62838-242">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="62838-243">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="62838-243">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="62838-244">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="62838-244">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="62838-245">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="62838-245">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
