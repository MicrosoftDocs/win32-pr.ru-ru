---
description: Дополнительные сведения о функции Жетжетколумнинфо
title: Функция JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712418"
---
# <a name="jetgetcolumninfo-function"></a><span data-ttu-id="1e8c6-103">Функция JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="1e8c6-103">JetGetColumnInfo Function</span></span>


<span data-ttu-id="1e8c6-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1e8c6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcolumninfo-function"></a><span data-ttu-id="1e8c6-105">Функция JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="1e8c6-105">JetGetColumnInfo Function</span></span>

<span data-ttu-id="1e8c6-106">Функция **жетжетколумнинфо** извлекает сведения о столбце.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-106">The **JetGetColumnInfo** function retrieves information about a column.</span></span>

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="1e8c6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e8c6-107">Parameters</span></span>

<span data-ttu-id="1e8c6-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="1e8c6-108">*sesid*</span></span>

<span data-ttu-id="1e8c6-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="1e8c6-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="1e8c6-110">*dbid*</span></span>

<span data-ttu-id="1e8c6-111">Определяет, а также *сзтабленаме* таблицу, содержащую столбец, из которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-111">Identifies, along with *szTableName*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="1e8c6-112">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="1e8c6-112">*szTableName*</span></span>

<span data-ttu-id="1e8c6-113">Определяет, вместе с *DBID*— таблицу, содержащую столбец, из которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-113">Identifies, along with *dbid*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="1e8c6-114">*сзколумннаме*</span><span class="sxs-lookup"><span data-stu-id="1e8c6-114">*szColumnName*</span></span>

<span data-ttu-id="1e8c6-115">Имя столбца, для которого извлекается информация.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-115">The name of the column that information is fetched for.</span></span>

<span data-ttu-id="1e8c6-116">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="1e8c6-116">*pvResult*</span></span>

<span data-ttu-id="1e8c6-117">Указатель на буфер, который будет принимать сведения.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-117">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="1e8c6-118">Тип буфера зависит от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-118">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="1e8c6-119">Вызывающий объект должен быть настроен для правильного согласования буфера.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-119">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="1e8c6-120">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="1e8c6-120">*cbMax*</span></span>

<span data-ttu-id="1e8c6-121">Размер буфера (в байтах), переданного в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-121">The size, in bytes, of the buffer that is passed in *pvResult*.</span></span>

<span data-ttu-id="1e8c6-122">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="1e8c6-122">*InfoLevel*</span></span>

<span data-ttu-id="1e8c6-123">Тип извлекаемых данных для столбца, заданного параметром *сзколумннаме*.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-123">The type of information to retrieve for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="1e8c6-124">Формат данных, хранящихся в *пвресулт* , зависит от этого параметра.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-124">The format of the data stored in *pvResult* is dependent on this parameter.</span></span> <span data-ttu-id="1e8c6-125">Сведения о схеме временной таблицы см. в разделе [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1e8c6-125">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="1e8c6-126">Эти *инфолевелс* отличаются следующими:</span><span class="sxs-lookup"><span data-stu-id="1e8c6-126">These *InfoLevels* are differentiated by:</span></span>

  - <span data-ttu-id="1e8c6-127">JET_ColInfoListSortColumnid будет сортировать временную таблицу по *columnid*.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-127">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="1e8c6-128">JET_ColInfoListCompact будет сжимать выходные данные.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-128">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="1e8c6-129">Дополнительные сведения о компактном выходе см. в разделе [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1e8c6-129">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="1e8c6-130">Для использования с этим параметром доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-130">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e8c6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1e8c6-131">Value</span></span></p></th>
<th><p><span data-ttu-id="1e8c6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1e8c6-132">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-133">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="1e8c6-133">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-134">JET_ColInfo и JET_ColInfoByColid получают одни и те же сведения.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-134">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span> <span data-ttu-id="1e8c6-135"><em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, а поля структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> заполняются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-135"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-136">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="1e8c6-136">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-137"><em>пвресулт</em> интерпретируется как структура <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-137"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="1e8c6-138">Это похоже на структуру <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-138">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="1e8c6-139">Если эта функция выполнена, структура заполняется соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-139">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="1e8c6-140">Если эта функция завершается ошибкой, структура содержит неопределенные данные.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-140">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-141">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="1e8c6-141">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-142">Как и JET_ColInfo, <em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является именем столбца строк, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-142">Like JET_ColInfo, <em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-143">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="1e8c6-143">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-144"><em>пвресулт</em> интерпретируется как структура <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-144"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="1e8c6-145">Если эта функция выполнена, структура заполняется соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-145">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="1e8c6-146">Открывается временная таблица, которая определяется элементом <strong>tableid</strong> структуры <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-146">A temporary table is opened and is identified by the <strong>tableid</strong> member of the <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="1e8c6-147">Таблица должна быть закрыта с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-147">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="1e8c6-148">Если эта функция завершается ошибкой, структура содержит неопределенные данные.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-148">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-149">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="1e8c6-149">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-150">То же, что и JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-150">Same as JET_ColInfoList.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-151">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="1e8c6-151">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-152">То же, что и JET_ColInfoList; Однако результирующая таблица сортируется по columnid, а не к имени столбца.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-152">Same as JET_ColInfoList; however the resulting table is sorted by columnid, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-153">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="1e8c6-153">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-154">JET_ColInfoSysTabCursor не рекомендуется, и его использование будет возвращать JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-154">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-155">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="1e8c6-155">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-156">Как и JET_ColInfoBase, <em>пвресулт</em> интерпретируется как <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является именем столбца строк, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-156">Like JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="1e8c6-157"><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-157"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="1e8c6-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-159">Возвращать только столбцы, не являющиеся производными (если таблица является производной от шаблона).</span><span class="sxs-lookup"><span data-stu-id="1e8c6-159">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="1e8c6-160">Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-160">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="1e8c6-161"><strong>Windows Vista:  </strong> Это значение введено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-161"><strong>Windows Vista:  </strong>This value is introduced Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-162">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="1e8c6-162">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-163">Возвращать только имя столбца и значение columnid для каждого столбца.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-163">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="1e8c6-164">Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-164">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="1e8c6-165"><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-165"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-166">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="1e8c6-166">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-167">Сортировать возвращенный список столбцов по columnid (по умолчанию сортировка списка по имени столбца).</span><span class="sxs-lookup"><span data-stu-id="1e8c6-167">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="1e8c6-168">Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-168">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="1e8c6-169"><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-169"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1e8c6-170">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e8c6-170">Return Value</span></span>

<span data-ttu-id="1e8c6-171">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-171">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1e8c6-172">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1e8c6-172">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e8c6-173">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1e8c6-173">Return code</span></span></p></th>
<th><p><span data-ttu-id="1e8c6-174">Описание</span><span class="sxs-lookup"><span data-stu-id="1e8c6-174">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-175">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1e8c6-175">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-176">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-176">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-177">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="1e8c6-177">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-178">Столбец с именем <em>сзколумннаме</em> не найден в таблице.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-178">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-179">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="1e8c6-179">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-180">Указан недопустимый <em>инфолевел</em> .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-180">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-181">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="1e8c6-181">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-182">Эта ошибка может быть возвращена, если:</span><span class="sxs-lookup"><span data-stu-id="1e8c6-182">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="1e8c6-183">Задано неправильное имя для <em>сзтабленаме</em> .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-183">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="1e8c6-184">Задано неправильное имя для <em>сзколумннаме</em> .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-184">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-185">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1e8c6-185">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1e8c6-186">Эта ошибка может быть возвращена, если:</span><span class="sxs-lookup"><span data-stu-id="1e8c6-186">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="1e8c6-187">Указан недопустимый <em>инфолевел</em> .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-187">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="1e8c6-188">Передан <em>СЗТАБЛЕНАМЕ</em> null.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-188">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="1e8c6-189">Буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-189">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1e8c6-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e8c6-190">Remarks</span></span>

<span data-ttu-id="1e8c6-191">[Жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) и **жетжетколумнинфо** извлекают сведения о столбце.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) and **JetGetColumnInfo** both retrieve information about a column.</span></span> <span data-ttu-id="1e8c6-192">Различие между ними заключается в том, как определяется таблица:</span><span class="sxs-lookup"><span data-stu-id="1e8c6-192">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="1e8c6-193">[Жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) определяет таблицу по *TableID*.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="1e8c6-194">**Жетжетколумнинфо** определяет таблицу, используя сочетание *DBID* и *сзтабленаме* .</span><span class="sxs-lookup"><span data-stu-id="1e8c6-194">**JetGetColumnInfo** identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="1e8c6-195">При получении данных с помощью JET_ColInfoList, JET_ColInfoListSortColumnid или JET_ColInfoListCompact будет открыта временная таблица.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-195">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="1e8c6-196">Временная таблица содержит данные, а структура [JET_COLUMNLIST](./jet-columnlist-structure.md) содержит достаточно сведений для прохода по временной таблице.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-196">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="1e8c6-197">Временная таблица должна быть закрыта с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="1e8c6-197">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="1e8c6-198">Требования</span><span class="sxs-lookup"><span data-stu-id="1e8c6-198">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-199"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1e8c6-199"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1e8c6-200">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-200">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-201"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1e8c6-201"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1e8c6-202">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-202">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-203"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1e8c6-203"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1e8c6-204">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-204">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-205"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="1e8c6-205"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1e8c6-206">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-206">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e8c6-207"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="1e8c6-207"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1e8c6-208">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1e8c6-208">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e8c6-209"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="1e8c6-209"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1e8c6-210">Реализуется как <strong>жетжетколумнинфов</strong> (Юникод) и <strong>жетжетколумнинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1e8c6-210">Implemented as <strong>JetGetColumnInfoW</strong> (Unicode) and <strong>JetGetColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1e8c6-211">См. также:</span><span class="sxs-lookup"><span data-stu-id="1e8c6-211">See Also</span></span>

[<span data-ttu-id="1e8c6-212">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="1e8c6-212">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="1e8c6-213">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="1e8c6-213">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="1e8c6-214">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="1e8c6-214">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="1e8c6-215">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="1e8c6-215">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="1e8c6-216">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="1e8c6-216">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="1e8c6-217">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="1e8c6-217">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="1e8c6-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1e8c6-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1e8c6-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1e8c6-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1e8c6-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1e8c6-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1e8c6-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1e8c6-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1e8c6-222">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="1e8c6-222">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="1e8c6-223">жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="1e8c6-223">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
