---
description: Дополнительные сведения о функции Жетжеттаблеколумнинфо
title: Функция Жетжеттаблеколумнинфо
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104274003"
---
# <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="02ac4-103">Функция Жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="02ac4-103">JetGetTableColumnInfo Function</span></span>


<span data-ttu-id="02ac4-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="02ac4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="02ac4-105">Функция Жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="02ac4-105">JetGetTableColumnInfo Function</span></span>

<span data-ttu-id="02ac4-106">Функция **жетжеттаблеколумнинфо** извлекает сведения о столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="02ac4-106">The **JetGetTableColumnInfo** function retrieves information about a table column.</span></span>

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a><span data-ttu-id="02ac4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="02ac4-107">Parameters</span></span>

<span data-ttu-id="02ac4-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="02ac4-108">*sesid*</span></span>

<span data-ttu-id="02ac4-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="02ac4-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="02ac4-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="02ac4-110">*tableid*</span></span>

<span data-ttu-id="02ac4-111">Таблица, содержащая столбец, для которого необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="02ac4-111">The table that contains the column to fetch information for.</span></span>

<span data-ttu-id="02ac4-112">*сзколумннаме*</span><span class="sxs-lookup"><span data-stu-id="02ac4-112">*szColumnName*</span></span>

<span data-ttu-id="02ac4-113">Имя столбца, для которого необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="02ac4-113">The name of the column to fetch information for.</span></span>

<span data-ttu-id="02ac4-114">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="02ac4-114">*pvResult*</span></span>

<span data-ttu-id="02ac4-115">Указатель на буфер, который будет принимать сведения.</span><span class="sxs-lookup"><span data-stu-id="02ac4-115">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="02ac4-116">Тип буфера зависит от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="02ac4-116">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="02ac4-117">Вызывающий объект должен быть настроен для правильного согласования буфера.</span><span class="sxs-lookup"><span data-stu-id="02ac4-117">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="02ac4-118">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="02ac4-118">*cbMax*</span></span>

<span data-ttu-id="02ac4-119">Размер (в байтах) буфера, переданного в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="02ac4-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="02ac4-120">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="02ac4-120">*InfoLevel*</span></span>

<span data-ttu-id="02ac4-121">Тип данных, которые будут получены для столбца, заданного параметром *сзколумннаме*.</span><span class="sxs-lookup"><span data-stu-id="02ac4-121">The type of information that will be retrieved for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="02ac4-122">Формат данных, хранящихся в *пвресулт* , зависит от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="02ac4-122">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span> <span data-ttu-id="02ac4-123">Сведения о схеме временной таблицы см. в разделе [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="02ac4-123">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

  - <span data-ttu-id="02ac4-124">JET_ColInfoListSortColumnid будет сортировать временную таблицу по *columnid*.</span><span class="sxs-lookup"><span data-stu-id="02ac4-124">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="02ac4-125">JET_ColInfoListCompact будет сжимать выходные данные.</span><span class="sxs-lookup"><span data-stu-id="02ac4-125">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="02ac4-126">Дополнительные сведения о компактном выходе см. в разделе [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="02ac4-126">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="02ac4-127">Для этого параметра можно задать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="02ac4-127">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02ac4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="02ac4-128">Value</span></span></p></th>
<th><p><span data-ttu-id="02ac4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="02ac4-129">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-130">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="02ac4-130">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="02ac4-131"><em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, а поля структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> заполняются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="02ac4-131"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span> <span data-ttu-id="02ac4-132">JET_ColInfo и JET_ColInfoByColid получают одни и те же сведения.</span><span class="sxs-lookup"><span data-stu-id="02ac4-132">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-133">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="02ac4-133">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="02ac4-134"><em>пвресулт</em> интерпретируется как структура <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="02ac4-134"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="02ac4-135">Это похоже на структуру <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="02ac4-135">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="02ac4-136">Если эта функция выполнена, структура заполняется соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="02ac4-136">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="02ac4-137">Если эта функция завершается ошибкой, структура содержит неопределенные данные.</span><span class="sxs-lookup"><span data-stu-id="02ac4-137">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-138">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="02ac4-138">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="02ac4-139"><em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является строковым именем столбца, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="02ac4-139"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span> <span data-ttu-id="02ac4-140">JET_ColInfo и JET_ColInfoByColid получают одни и те же сведения.</span><span class="sxs-lookup"><span data-stu-id="02ac4-140">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-141">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="02ac4-141">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="02ac4-142"><em>пвресулт</em> интерпретируется как структура <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="02ac4-142"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="02ac4-143">Если эта функция выполнена, структура заполняется соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="02ac4-143">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="02ac4-144">Открывается временная таблица, которая определяется элементом <em>tableid</em> <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="02ac4-144">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="02ac4-145">Таблица должна быть закрыта с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>.</span><span class="sxs-lookup"><span data-stu-id="02ac4-145">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="02ac4-146">Если эта функция завершается ошибкой, структура содержит неопределенные данные.</span><span class="sxs-lookup"><span data-stu-id="02ac4-146">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-147">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="02ac4-147">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="02ac4-148"><em>пвресулт</em> интерпретируется как структура <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="02ac4-148"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="02ac4-149">Если эта функция выполнена, структура заполняется соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="02ac4-149">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="02ac4-150">Открывается временная таблица, которая определяется элементом <em>tableid</em> <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="02ac4-150">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="02ac4-151">Таблица должна быть закрыта с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>.</span><span class="sxs-lookup"><span data-stu-id="02ac4-151">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="02ac4-152">Если эта функция завершается ошибкой, структура содержит неопределенные данные.</span><span class="sxs-lookup"><span data-stu-id="02ac4-152">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-153">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="02ac4-153">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="02ac4-154">То же, что и JET_ColInfoList, однако результирующая таблица сортируется по <em>columnid</em>, а не по имени столбца.</span><span class="sxs-lookup"><span data-stu-id="02ac4-154">Same as JET_ColInfoList, however the resulting table is sorted by <em>columnid</em>, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-155">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="02ac4-155">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="02ac4-156">JET_ColInfoSysTabCursor не рекомендуется, и его использование будет возвращать JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="02ac4-156">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-157">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="02ac4-157">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="02ac4-158">То же, что и JET_ColInfoBase, <em>пвресулт</em> интерпретируется как <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является строковым именем столбца, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="02ac4-158">Same as JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="02ac4-159"><strong>Windows Vista:  </strong> Он доступен в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="02ac4-159"><strong>Windows Vista:  </strong>This is available in Windows Vista and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="02ac4-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="02ac4-161">Возвращать только столбцы, не являющиеся производными (если таблица является производной от шаблона).</span><span class="sxs-lookup"><span data-stu-id="02ac4-161">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="02ac4-162">Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="02ac4-162">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="02ac4-163"><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02ac4-163"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-164">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="02ac4-164">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="02ac4-165">Возвращать только имя столбца и значение columnid для каждого столбца.</span><span class="sxs-lookup"><span data-stu-id="02ac4-165">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="02ac4-166">Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="02ac4-166">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="02ac4-167"><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02ac4-167"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-168">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="02ac4-168">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="02ac4-169">Сортировать возвращенный список столбцов по columnid (по умолчанию сортировка списка по имени столбца).</span><span class="sxs-lookup"><span data-stu-id="02ac4-169">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="02ac4-170">Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="02ac4-170">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="02ac4-171"><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02ac4-171"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="02ac4-172">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02ac4-172">Return Value</span></span>

<span data-ttu-id="02ac4-173">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="02ac4-173">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="02ac4-174">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="02ac4-174">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02ac4-175">Код возврата</span><span class="sxs-lookup"><span data-stu-id="02ac4-175">Return code</span></span></p></th>
<th><p><span data-ttu-id="02ac4-176">Описание</span><span class="sxs-lookup"><span data-stu-id="02ac4-176">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-177">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="02ac4-177">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="02ac4-178">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="02ac4-178">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-179">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="02ac4-179">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="02ac4-180">Столбец с именем <em>сзколумннаме</em> не найден в таблице.</span><span class="sxs-lookup"><span data-stu-id="02ac4-180">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-181">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="02ac4-181">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="02ac4-182">Указан недопустимый <em>инфолевел</em> .</span><span class="sxs-lookup"><span data-stu-id="02ac4-182">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-183">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="02ac4-183">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="02ac4-184">Эта ошибка может быть возвращена, если:</span><span class="sxs-lookup"><span data-stu-id="02ac4-184">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="02ac4-185">Задано неправильное имя для <em>сзтабленаме</em> .</span><span class="sxs-lookup"><span data-stu-id="02ac4-185">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="02ac4-186">Задано неправильное имя для <em>сзколумннаме</em> .</span><span class="sxs-lookup"><span data-stu-id="02ac4-186">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="02ac4-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="02ac4-188">Эта ошибка может быть возвращена, если:</span><span class="sxs-lookup"><span data-stu-id="02ac4-188">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="02ac4-189">Указан недопустимый <em>инфолевел</em> .</span><span class="sxs-lookup"><span data-stu-id="02ac4-189">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="02ac4-190">Передан <em>СЗТАБЛЕНАМЕ</em> null.</span><span class="sxs-lookup"><span data-stu-id="02ac4-190">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="02ac4-191">Буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="02ac4-191">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="02ac4-192">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02ac4-192">Remarks</span></span>

<span data-ttu-id="02ac4-193">**Жетжеттаблеколумнинфо** и [жетжетколумнинфо](./jetgetcolumninfo-function.md) извлекают сведения о столбце.</span><span class="sxs-lookup"><span data-stu-id="02ac4-193">**JetGetTableColumnInfo** and [JetGetColumnInfo](./jetgetcolumninfo-function.md) both retrieve information about a column.</span></span> <span data-ttu-id="02ac4-194">Различие между ними заключается в том, как определяется таблица:</span><span class="sxs-lookup"><span data-stu-id="02ac4-194">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="02ac4-195">**Жетжеттаблеколумнинфо** определяет таблицу по *TableID*.</span><span class="sxs-lookup"><span data-stu-id="02ac4-195">**JetGetTableColumnInfo** identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="02ac4-196">[Жетжетколумнинфо](./jetgetcolumninfo-function.md) определяет таблицу, используя сочетание *DBID* и *сзтабленаме* .</span><span class="sxs-lookup"><span data-stu-id="02ac4-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="02ac4-197">При получении данных с помощью JET_ColInfoList, JET_ColInfoListSortColumnid или JET_ColInfoListCompact будет открыта временная таблица.</span><span class="sxs-lookup"><span data-stu-id="02ac4-197">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="02ac4-198">Временная таблица содержит данные, а структура [JET_COLUMNLIST](./jet-columnlist-structure.md) содержит достаточно сведений для прохода по временной таблице.</span><span class="sxs-lookup"><span data-stu-id="02ac4-198">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="02ac4-199">Временная таблица должна быть закрыта с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="02ac4-199">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="02ac4-200">Требования</span><span class="sxs-lookup"><span data-stu-id="02ac4-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-201"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="02ac4-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="02ac4-202">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="02ac4-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="02ac4-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="02ac4-204">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="02ac4-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="02ac4-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="02ac4-206">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="02ac4-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-207"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="02ac4-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="02ac4-208">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="02ac4-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ac4-209"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="02ac4-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="02ac4-210">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="02ac4-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ac4-211"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="02ac4-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="02ac4-212">Реализуется как <strong>жетжеттаблеколумнинфов</strong> (Юникод) и <strong>жетжеттаблеколумнинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="02ac4-212">Implemented as <strong>JetGetTableColumnInfoW</strong> (Unicode) and <strong>JetGetTableColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="02ac4-213">См. также:</span><span class="sxs-lookup"><span data-stu-id="02ac4-213">See Also</span></span>

[<span data-ttu-id="02ac4-214">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="02ac4-214">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="02ac4-215">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="02ac4-215">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="02ac4-216">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="02ac4-216">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="02ac4-217">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="02ac4-217">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="02ac4-218">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="02ac4-218">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="02ac4-219">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="02ac4-219">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="02ac4-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="02ac4-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="02ac4-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="02ac4-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="02ac4-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="02ac4-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="02ac4-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="02ac4-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="02ac4-224">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="02ac4-224">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="02ac4-225">жетжетколумнинфо</span><span class="sxs-lookup"><span data-stu-id="02ac4-225">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="02ac4-226">жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="02ac4-226">JetGetTableColumnInfo</span></span>]()
