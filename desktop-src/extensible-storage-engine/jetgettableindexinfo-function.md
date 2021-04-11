---
description: Дополнительные сведения о функции Жетжеттаблеиндексинфо
title: Функция JetGetTableIndexInfo
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 904391218fbd073cd273655ce74fdec116b6a22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272852"
---
# <a name="jetgettableindexinfo-function"></a><span data-ttu-id="6b501-103">Функция JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="6b501-103">JetGetTableIndexInfo Function</span></span>


<span data-ttu-id="6b501-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6b501-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableindexinfo-function"></a><span data-ttu-id="6b501-105">Функция JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="6b501-105">JetGetTableIndexInfo Function</span></span>

<span data-ttu-id="6b501-106">Функция **жетжеттаблеиндексинфо** получает сведения о индексе.</span><span class="sxs-lookup"><span data-stu-id="6b501-106">The **JetGetTableIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="6b501-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b501-107">Parameters</span></span>

<span data-ttu-id="6b501-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="6b501-108">*sesid*</span></span>

<span data-ttu-id="6b501-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="6b501-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="6b501-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="6b501-110">*tableid*</span></span>

<span data-ttu-id="6b501-111">Таблица базы данных, содержащая индекс, в котором содержатся необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="6b501-111">The database table that contains the index that holds the needed information.</span></span>

<span data-ttu-id="6b501-112">*сзиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="6b501-112">*szIndexName*</span></span>

<span data-ttu-id="6b501-113">Имя индекса, содержащего сведения, которые будут получены.</span><span class="sxs-lookup"><span data-stu-id="6b501-113">The name of the index that contains information that will be retrieved.</span></span>

<span data-ttu-id="6b501-114">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="6b501-114">*pvResult*</span></span>

<span data-ttu-id="6b501-115">Указатель на буфер, который будет принимать сведения.</span><span class="sxs-lookup"><span data-stu-id="6b501-115">Pointer to a buffer which will receive the information.</span></span> <span data-ttu-id="6b501-116">Буфер должен быть согласован, чтобы вместить требуемый тип.</span><span class="sxs-lookup"><span data-stu-id="6b501-116">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="6b501-117">Тип буфера зависит от параметра *инфолевел* .</span><span class="sxs-lookup"><span data-stu-id="6b501-117">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="6b501-118">*кбресулт*</span><span class="sxs-lookup"><span data-stu-id="6b501-118">*cbResult*</span></span>

<span data-ttu-id="6b501-119">Размер буфера (в байтах), переданного в параметре *пвресулт* .</span><span class="sxs-lookup"><span data-stu-id="6b501-119">The size, in bytes, of the buffer passed in the *pvResult* parameter.</span></span>

<span data-ttu-id="6b501-120">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="6b501-120">*InfoLevel*</span></span>

<span data-ttu-id="6b501-121">Указывает, какие сведения будут храниться в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="6b501-121">Specifies which information will be stored in *pvResult*.</span></span> <span data-ttu-id="6b501-122">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6b501-122">The valid values are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b501-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6b501-123">Value</span></span></p></th>
<th><p><span data-ttu-id="6b501-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6b501-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b501-125">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="6b501-125">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="6b501-126"><em>пвресулт</em> интерпретируется как структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="6b501-126"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="6b501-127">При успешном выполнении структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> получает сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="6b501-127">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="6b501-128">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-128">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-129">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="6b501-129">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="6b501-130"><em>пвресулт</em> интерпретируется как LCID.</span><span class="sxs-lookup"><span data-stu-id="6b501-130"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="6b501-131">При успешном выполнении код LCID содержит идентификатор локали индекса.</span><span class="sxs-lookup"><span data-stu-id="6b501-131">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="6b501-132">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-132">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-133">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="6b501-133">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="6b501-134"><em>пвресулт</em> интерпретируется как структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="6b501-134"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="6b501-135">При успешном выполнении структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> получает сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="6b501-135">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="6b501-136">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-136">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-137">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="6b501-137">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="6b501-138">JET_IdxInfoOLC устарел.</span><span class="sxs-lookup"><span data-stu-id="6b501-138">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-139">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="6b501-139">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="6b501-140">JET_IdxInfoResetOLC устарел.</span><span class="sxs-lookup"><span data-stu-id="6b501-140">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-141">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="6b501-141">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="6b501-142"><em>пвресулт</em> интерпретируется как ULong.</span><span class="sxs-lookup"><span data-stu-id="6b501-142"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="6b501-143">При успешном выполнении в ULONG содержится место использования индекса.</span><span class="sxs-lookup"><span data-stu-id="6b501-143">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="6b501-144">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-144">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-145">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="6b501-145">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="6b501-146">JET_IdxInfoSysTabCursor устарел.</span><span class="sxs-lookup"><span data-stu-id="6b501-146">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-147">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="6b501-147">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="6b501-148">JET_IdxInfoLangid не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="6b501-148">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="6b501-149">Вместо этого используйте JET_IdxInfoLCID и макрос <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">лангидфромлЦид</a> .</span><span class="sxs-lookup"><span data-stu-id="6b501-149">Use JET_IdxInfoLCID instead, and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-150">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="6b501-150">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="6b501-151"><em>пвресулт</em> интерпретируется как ULong.</span><span class="sxs-lookup"><span data-stu-id="6b501-151"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="6b501-152">В случае успеха ULONG содержит количество индексов в указанной таблице.</span><span class="sxs-lookup"><span data-stu-id="6b501-152">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="6b501-153"><em>сзиндекснаме</em> игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6b501-153"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="6b501-154">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-154">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-155">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="6b501-155">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="6b501-156"><em>пвресулт</em> интерпретируется как ushort.</span><span class="sxs-lookup"><span data-stu-id="6b501-156"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="6b501-157">При успешном выполнении объект USHORT содержит значение <em>кбварсегмак</em> , используемое при создании индекса.</span><span class="sxs-lookup"><span data-stu-id="6b501-157">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="6b501-158">Описание <em>кбварсегмак</em>см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="6b501-158">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="6b501-159">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-160">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="6b501-160">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="6b501-161"><em>пвресулт</em> интерпретируется как <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="6b501-161"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="6b501-162">При успешном выполнении структура <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> получает сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="6b501-162">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="6b501-163">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-163">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-164">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="6b501-164">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="6b501-165"><em>пвресулт</em> интерпретируется как ushort.</span><span class="sxs-lookup"><span data-stu-id="6b501-165"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="6b501-166">При успешном выполнении объект USHORT содержит значение Кбкэймост, используемое при создании индекса.</span><span class="sxs-lookup"><span data-stu-id="6b501-166">On success, the USHORT holds the value of cbKeyMost used when the index was created.</span></span> <span data-ttu-id="6b501-167">Описание Кбкэймост см. в разделе Структура <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="6b501-167">See the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure for a description of cbKeyMost.</span></span> <span data-ttu-id="6b501-168">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-168">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-169">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="6b501-169">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="6b501-170"><em>пвресулт</em> интерпретируется как структура <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="6b501-170"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="6b501-171">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="6b501-172"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6b501-172"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-173">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="6b501-173">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="6b501-174"><em>пвресулт</em> интерпретируется как структура <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="6b501-174"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="6b501-175">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="6b501-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6b501-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6b501-177">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b501-177">Return Value</span></span>

<span data-ttu-id="6b501-178">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="6b501-178">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6b501-179">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6b501-179">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b501-180">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6b501-180">Return code</span></span></p></th>
<th><p><span data-ttu-id="6b501-181">Описание</span><span class="sxs-lookup"><span data-stu-id="6b501-181">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b501-182">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6b501-182">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6b501-183">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6b501-183">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-184">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="6b501-184">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="6b501-185">Указанный индекс не найден в указанной таблице.</span><span class="sxs-lookup"><span data-stu-id="6b501-185">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-186">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="6b501-186">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="6b501-187">Буфер, переданный как <em>пвресулт</em> , слишком мал.</span><span class="sxs-lookup"><span data-stu-id="6b501-187">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="6b501-188">Содержимое буфера не определено.</span><span class="sxs-lookup"><span data-stu-id="6b501-188">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6b501-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b501-189">Remarks</span></span>

<span data-ttu-id="6b501-190">[Жетжетиндексинфо](./jetgetindexinfo-function.md) и **жетжеттаблеиндексинфо** извлекают идентичные сведения о индексе.</span><span class="sxs-lookup"><span data-stu-id="6b501-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) and **JetGetTableIndexInfo** retrieve identical information about an index.</span></span> <span data-ttu-id="6b501-191">Разница заключается в том, как указана таблица.</span><span class="sxs-lookup"><span data-stu-id="6b501-191">The difference is in how the table is specified.</span></span> <span data-ttu-id="6b501-192">[Жетжетиндексинфо](./jetgetindexinfo-function.md) ждет базу данных (*DBID*) и имя таблицы (*сзтабленаме*), а **жетжеттаблеиндексинфо** — идентификатор таблицы (*TableID*).</span><span class="sxs-lookup"><span data-stu-id="6b501-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) expects a database (*dbid*) and name of a table (*szTableName*), while **JetGetTableIndexInfo** expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="6b501-193">Требования</span><span class="sxs-lookup"><span data-stu-id="6b501-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b501-194"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="6b501-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6b501-195">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6b501-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6b501-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6b501-197">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6b501-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6b501-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6b501-199">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6b501-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-200"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="6b501-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6b501-201">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6b501-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b501-202"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="6b501-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6b501-203">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6b501-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b501-204"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="6b501-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6b501-205">Реализуется как <strong>жетжеттаблеиндексинфов</strong> (Юникод) и <strong>жетжеттаблеиндексинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6b501-205">Implemented as <strong>JetGetTableIndexInfoW</strong> (Unicode) and <strong>JetGetTableIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6b501-206">См. также:</span><span class="sxs-lookup"><span data-stu-id="6b501-206">See Also</span></span>

[<span data-ttu-id="6b501-207">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="6b501-207">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="6b501-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6b501-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6b501-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6b501-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6b501-210">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6b501-210">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6b501-211">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6b501-211">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6b501-212">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="6b501-212">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="6b501-213">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="6b501-213">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="6b501-214">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="6b501-214">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)
