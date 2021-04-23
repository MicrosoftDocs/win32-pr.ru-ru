---
description: Дополнительные сведения о функции Жетжеттаблеинфо
title: Функция JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999440"
---
# <a name="jetgettableinfo-function"></a><span data-ttu-id="571d6-103">Функция JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="571d6-103">JetGetTableInfo Function</span></span>


<span data-ttu-id="571d6-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="571d6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableinfo-function"></a><span data-ttu-id="571d6-105">Функция JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="571d6-105">JetGetTableInfo Function</span></span>

<span data-ttu-id="571d6-106">Функция **жетжеттаблеинфо** извлекает различные фрагменты информации о таблице в базе данных.</span><span class="sxs-lookup"><span data-stu-id="571d6-106">The **JetGetTableInfo** function retrieves various pieces of information about a table in a database.</span></span>

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="571d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="571d6-107">Parameters</span></span>

<span data-ttu-id="571d6-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="571d6-108">*sesid*</span></span>

<span data-ttu-id="571d6-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="571d6-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="571d6-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="571d6-110">*tableid*</span></span>

<span data-ttu-id="571d6-111">Таблица, к которой применяются сведения.</span><span class="sxs-lookup"><span data-stu-id="571d6-111">The table that the information applies to.</span></span>

<span data-ttu-id="571d6-112">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="571d6-112">*pvResult*</span></span>

<span data-ttu-id="571d6-113">Указатель на буфер, который будет принимать сведения.</span><span class="sxs-lookup"><span data-stu-id="571d6-113">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="571d6-114">Тип буфера зависит от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="571d6-114">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="571d6-115">Вызывающий объект отвечает за то, чтобы правильно согласовать буфер.</span><span class="sxs-lookup"><span data-stu-id="571d6-115">It is the responsibility of the caller to align the buffer appropriately.</span></span>

<span data-ttu-id="571d6-116">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="571d6-116">*cbMax*</span></span>

<span data-ttu-id="571d6-117">Размер (в байтах) буфера, переданного в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="571d6-117">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="571d6-118">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="571d6-118">*InfoLevel*</span></span>

<span data-ttu-id="571d6-119">Тип сведений, которые будут получены для таблицы, заданной *tableid*.</span><span class="sxs-lookup"><span data-stu-id="571d6-119">The type of information that will be retrieved for the table that is specified by *tableid*.</span></span> <span data-ttu-id="571d6-120">Формат данных, хранящихся в *пвресулт* , зависит от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="571d6-120">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="571d6-121">Для этого параметра можно задать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="571d6-121">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="571d6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="571d6-122">Value</span></span></p></th>
<th><p><span data-ttu-id="571d6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="571d6-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="571d6-124">JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="571d6-124">JET_TblInfo</span></span></p></td>
<td><p><span data-ttu-id="571d6-125"><em>пвресулт</em> интерпретируется как структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="571d6-125"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span> <span data-ttu-id="571d6-126">Если метод выполняется правильно, <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> структура заполняется соответствующими данными.</span><span class="sxs-lookup"><span data-stu-id="571d6-126">If the method succeeds, the <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is filled in with the appropriate data.</span></span> <span data-ttu-id="571d6-127">В случае неудачи содержимое не определено.</span><span class="sxs-lookup"><span data-stu-id="571d6-127">If it fails, the contents are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-128">JET_TblInfoDbid</span><span class="sxs-lookup"><span data-stu-id="571d6-128">JET_TblInfoDbid</span></span></p></td>
<td><p><span data-ttu-id="571d6-129"><em>пвресулт</em> обрабатывается как массив из двух объектов <a href="gg269248(v=exchg.10).md">JET_DBID</a> .</span><span class="sxs-lookup"><span data-stu-id="571d6-129"><em>pvResult</em> is treated as an array of two <a href="gg269248(v=exchg.10).md">JET_DBID</a> objects.</span></span> <span data-ttu-id="571d6-130">Идентификатор базы данных, владеющей таблицей, хранится в этом массиве дважды.</span><span class="sxs-lookup"><span data-stu-id="571d6-130">The database identifier of the database that owns the table is stored in this array twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-131">JET_TblInfoDumpTable</span><span class="sxs-lookup"><span data-stu-id="571d6-131">JET_TblInfoDumpTable</span></span></p></td>
<td><p><span data-ttu-id="571d6-132">JET_TblInfoDumpTable не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="571d6-132">JET_TblInfoDumpTable is deprecated.</span></span> <span data-ttu-id="571d6-133">API возвратит JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="571d6-133">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-134">JET_TblInfoName</span><span class="sxs-lookup"><span data-stu-id="571d6-134">JET_TblInfoName</span></span></p></td>
<td><p><span data-ttu-id="571d6-135">JET_TblInfoName извлекает имя таблицы и сохраняет ее в <em>пвресулт</em>.</span><span class="sxs-lookup"><span data-stu-id="571d6-135">JET_TblInfoName retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="571d6-136">Если буфер слишком мал, поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="571d6-136">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-137">JET_TblInfoMostMany</span><span class="sxs-lookup"><span data-stu-id="571d6-137">JET_TblInfoMostMany</span></span></p></td>
<td><p><span data-ttu-id="571d6-138">JET_TblInfoMostMany извлекает имя таблицы и сохраняет ее в <em>пвресулт</em>.</span><span class="sxs-lookup"><span data-stu-id="571d6-138">JET_TblInfoMostMany retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="571d6-139">Если буфер слишком мал, поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="571d6-139">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-140">JET_TblInfoOLC</span><span class="sxs-lookup"><span data-stu-id="571d6-140">JET_TblInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="571d6-141">JET_TblInfoOLC не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="571d6-141">JET_TblInfoOLC is deprecated.</span></span> <span data-ttu-id="571d6-142">API возвратит JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="571d6-142">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-143">JET_TblInfoRvt</span><span class="sxs-lookup"><span data-stu-id="571d6-143">JET_TblInfoRvt</span></span></p></td>
<td><p><span data-ttu-id="571d6-144">JET_TblInfoRvt не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="571d6-144">JET_TblInfoRvt is deprecated.</span></span> <span data-ttu-id="571d6-145">API возвратит JET_errQueryNotSupported.</span><span class="sxs-lookup"><span data-stu-id="571d6-145">The API will return JET_errQueryNotSupported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-146">JET_TblInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="571d6-146">JET_TblInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="571d6-147">JET_TblInfoResetOLC не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="571d6-147">JET_TblInfoResetOLC is deprecated.</span></span> <span data-ttu-id="571d6-148">API возвратит JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="571d6-148">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-149">JET_TblInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="571d6-149">JET_TblInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="571d6-150"><em>пвресулт</em> интерпретируется как массив из двух ulong:</span><span class="sxs-lookup"><span data-stu-id="571d6-150"><em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="571d6-151">Первый <strong>ulong</strong> — число страниц в таблице.</span><span class="sxs-lookup"><span data-stu-id="571d6-151">The first <strong>ULONG</strong> is the number of pages in the table.</span></span></p></li>
<li><p><span data-ttu-id="571d6-152">Второй <strong>ulong</strong> является целевой плотностью страниц для таблицы.</span><span class="sxs-lookup"><span data-stu-id="571d6-152">The second <strong>ULONG</strong> is the target density of pages for the table.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-153">JET_TblInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="571d6-153">JET_TblInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="571d6-154"><em>пвресулт</em> интерпретируется как <strong>ulong</strong>.</span><span class="sxs-lookup"><span data-stu-id="571d6-154"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="571d6-155"><strong>Ulong</strong> — это сумма количества страниц, доступных в таблице, ее индексах и дереве значений long.</span><span class="sxs-lookup"><span data-stu-id="571d6-155">The <strong>ULONG</strong> is the sum of the number of pages that are available in the table, its indexes, and the long value tree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-156">JET_TblInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="571d6-156">JET_TblInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="571d6-157"><em>пвресулт</em> интерпретируется как <strong>ulong</strong>.</span><span class="sxs-lookup"><span data-stu-id="571d6-157"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="571d6-158"><strong>Ulong</strong> представляет собой сумму количества страниц, принадлежащих таблице (включая ее индексы, а также дерево длинных значений и все доступные страницы).</span><span class="sxs-lookup"><span data-stu-id="571d6-158">The <strong>ULONG</strong> is the sum of the number of pages that are owned by the table (including its indexes, and the long value tree and any available pages therein).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-159">JET_TblInfoSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="571d6-159">JET_TblInfoSpaceUsage</span></span></p></td>
<td><p><span data-ttu-id="571d6-160">Поведение API зависит от размера буфера, передаваемого в API.</span><span class="sxs-lookup"><span data-stu-id="571d6-160">The behavior of the API depends on how large the buffer that is passed to the API is.</span></span> <span data-ttu-id="571d6-161">Два значения <em>кбмакс</em> должны быть не меньше (2 \* sizeof (ulong)).</span><span class="sxs-lookup"><span data-stu-id="571d6-161">Two <em>cbMax</em> values must be at least ( 2 \* sizeof( ULONG ) ).</span></span></p>
<ul>
<li><p><span data-ttu-id="571d6-162">Если <em>кбмакс</em> имеет значение (2 \* sizeof (ulong)), <em>пвресулт</em> интерпретируется как массив из двух ulong:</span><span class="sxs-lookup"><span data-stu-id="571d6-162">If <em>cbMax</em> is ( 2 \* sizeof( ULONG ) ), <em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="571d6-163">Первый <strong>ulong</strong> — число принадлежащих экстентов таблицы.</span><span class="sxs-lookup"><span data-stu-id="571d6-163">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="571d6-164">Второй <strong>ulong</strong> — число доступных экстентов таблицы.</span><span class="sxs-lookup"><span data-stu-id="571d6-164">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="571d6-165"><em>пвресулт</em> интерпретируется как массив:</span><span class="sxs-lookup"><span data-stu-id="571d6-165"><em>pvResult</em> is interpreted as an array of:</span></span></p>
<ul>
<li><p><span data-ttu-id="571d6-166">Первый <strong>ulong</strong> — число принадлежащих экстентов таблицы.</span><span class="sxs-lookup"><span data-stu-id="571d6-166">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="571d6-167">Второй <strong>ulong</strong> — число доступных экстентов таблицы.</span><span class="sxs-lookup"><span data-stu-id="571d6-167">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-168">JET_TblInfoTemplateTableName</span><span class="sxs-lookup"><span data-stu-id="571d6-168">JET_TblInfoTemplateTableName</span></span></p></td>
<td><p><span data-ttu-id="571d6-169"><em>пвресулт</em> интерпретируется как строковый буфер.</span><span class="sxs-lookup"><span data-stu-id="571d6-169"><em>pvResult</em> is interpreted as a string buffer.</span></span> <span data-ttu-id="571d6-170">Буфер должен быть не менее JET_cbNameMost + 1, включая завершающее <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="571d6-170">The buffer must be at least JET_cbNameMost + 1, including the terminating <strong>NULL</strong>.</span></span> <span data-ttu-id="571d6-171">Если таблица является производной, буфер будет заполнен именем таблицы, из которой производные таблицы наследовали ее DDL.</span><span class="sxs-lookup"><span data-stu-id="571d6-171">If the table is a derived table, the buffer will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="571d6-172">Если таблица не является производной, буфер будет пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="571d6-172">If the table is not a derived table, the buffer will an empty string.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="571d6-173">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="571d6-173">Return Value</span></span>

<span data-ttu-id="571d6-174">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="571d6-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="571d6-175">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="571d6-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="571d6-176">Код возврата</span><span class="sxs-lookup"><span data-stu-id="571d6-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="571d6-177">Описание</span><span class="sxs-lookup"><span data-stu-id="571d6-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="571d6-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="571d6-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="571d6-179">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="571d6-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-180">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="571d6-180">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="571d6-181">Буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="571d6-181">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-182">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="571d6-182">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="571d6-183">Указан устаревший <em>инфолевел</em> .</span><span class="sxs-lookup"><span data-stu-id="571d6-183">A deprecated <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-184">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="571d6-184">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="571d6-185">Размер буфера не подходит.</span><span class="sxs-lookup"><span data-stu-id="571d6-185">The buffer was not the right size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-186">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="571d6-186">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="571d6-187">Переданная таблица была временной таблицей, и запрошенный <em>инфолевел</em> не может быть получен для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="571d6-187">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-188">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="571d6-188">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="571d6-189">Переданная таблица была временной таблицей, и запрошенный <em>инфолевел</em> не может быть получен для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="571d6-189">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-190">JET_errQueryNotSupported</span><span class="sxs-lookup"><span data-stu-id="571d6-190">JET_errQueryNotSupported</span></span></p></td>
<td><p><span data-ttu-id="571d6-191"><em>Инфолевел</em> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="571d6-191">The <em>InfoLevel</em> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-192">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="571d6-192">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="571d6-193">Таблица используется другой операцией базы данных.</span><span class="sxs-lookup"><span data-stu-id="571d6-193">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-194">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="571d6-194">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="571d6-195">Таблица заблокирована другой операцией базы данных.</span><span class="sxs-lookup"><span data-stu-id="571d6-195">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-196">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="571d6-196">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="571d6-197">Таблица используется системой.</span><span class="sxs-lookup"><span data-stu-id="571d6-197">The table is being used by the system.</span></span> <span data-ttu-id="571d6-198">Это предупреждение является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="571d6-198">This warning is nonfatal.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="571d6-199">Комментарии</span><span class="sxs-lookup"><span data-stu-id="571d6-199">Remarks</span></span>

<span data-ttu-id="571d6-200">Некоторые части информации недопустимы для временных таблиц (см. [жетопентемптабле](./jetopentemptable-function.md)).</span><span class="sxs-lookup"><span data-stu-id="571d6-200">Some pieces of information are not valid for temporary tables (See [JetOpenTempTable](./jetopentemptable-function.md)).</span></span>

<span data-ttu-id="571d6-201">Статистика таблицы включает число записей и количество страниц в кластеризованном индексе (то есть индекс, содержащий данные записи).</span><span class="sxs-lookup"><span data-stu-id="571d6-201">The table statistics include the number of records and the number of pages in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="571d6-202">Доступ к статистике индекса осуществляется отдельно по имени с помощью [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="571d6-202">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="571d6-203">Требования</span><span class="sxs-lookup"><span data-stu-id="571d6-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="571d6-204"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="571d6-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="571d6-205">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="571d6-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="571d6-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="571d6-207">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="571d6-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="571d6-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="571d6-209">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="571d6-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-210"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="571d6-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="571d6-211">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="571d6-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="571d6-212"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="571d6-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="571d6-213">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="571d6-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571d6-214"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="571d6-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="571d6-215">Реализуется как <strong>жетжеттаблеинфов</strong> (Юникод) и <strong>жетжеттаблеинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="571d6-215">Implemented as <strong>JetGetTableInfoW</strong> (Unicode) and <strong>JetGetTableInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="571d6-216">См. также:</span><span class="sxs-lookup"><span data-stu-id="571d6-216">See Also</span></span>

[<span data-ttu-id="571d6-217">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="571d6-217">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="571d6-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="571d6-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="571d6-219">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="571d6-219">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="571d6-220">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="571d6-220">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="571d6-221">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="571d6-221">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="571d6-222">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="571d6-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="571d6-223">жетжетобжектинфо</span><span class="sxs-lookup"><span data-stu-id="571d6-223">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="571d6-224">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="571d6-224">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="571d6-225">жетопентемптабле</span><span class="sxs-lookup"><span data-stu-id="571d6-225">JetOpenTempTable</span></span>](./jetopentemptable-function.md)
