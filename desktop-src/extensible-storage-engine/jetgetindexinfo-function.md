---
description: Дополнительные сведения о функции Жетжетиндексинфо
title: Функция JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647497"
---
# <a name="jetgetindexinfo-function"></a><span data-ttu-id="e4a36-103">Функция JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="e4a36-103">JetGetIndexInfo Function</span></span>


<span data-ttu-id="e4a36-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e4a36-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetindexinfo-function"></a><span data-ttu-id="e4a36-105">Функция JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="e4a36-105">JetGetIndexInfo Function</span></span>

<span data-ttu-id="e4a36-106">Функция **жетжетиндексинфо** получает сведения о индексе.</span><span class="sxs-lookup"><span data-stu-id="e4a36-106">The **JetGetIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="e4a36-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4a36-107">Parameters</span></span>

<span data-ttu-id="e4a36-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="e4a36-108">*sesid*</span></span>

<span data-ttu-id="e4a36-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="e4a36-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="e4a36-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="e4a36-110">*dbid*</span></span>

<span data-ttu-id="e4a36-111">Идентификатор базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="e4a36-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="e4a36-112">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="e4a36-112">*szTableName*</span></span>

<span data-ttu-id="e4a36-113">Имя таблицы, содержащей индекс, с извлекаемыми данными.</span><span class="sxs-lookup"><span data-stu-id="e4a36-113">The name of the table containing the index with the information to retrieve.</span></span>

<span data-ttu-id="e4a36-114">*сзиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="e4a36-114">*szIndexName*</span></span>

<span data-ttu-id="e4a36-115">Имя индекса с извлекаемыми данными.</span><span class="sxs-lookup"><span data-stu-id="e4a36-115">The name of the index with the information to retrieve.</span></span>

<span data-ttu-id="e4a36-116">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="e4a36-116">*pvResult*</span></span>

<span data-ttu-id="e4a36-117">Указатель на буфер, который будет принимать нужные сведения.</span><span class="sxs-lookup"><span data-stu-id="e4a36-117">Pointer to a buffer that will receive the desired information.</span></span> <span data-ttu-id="e4a36-118">Буфер должен быть согласован, чтобы вместить требуемый тип.</span><span class="sxs-lookup"><span data-stu-id="e4a36-118">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="e4a36-119">Тип буфера зависит от параметра *инфолевел* .</span><span class="sxs-lookup"><span data-stu-id="e4a36-119">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="e4a36-120">*кбресулт*</span><span class="sxs-lookup"><span data-stu-id="e4a36-120">*cbResult*</span></span>

<span data-ttu-id="e4a36-121">Размер (в байтах) буфера, переданного в качестве *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="e4a36-121">The size, in bytes, of the buffer passed as *pvResult*.</span></span>

<span data-ttu-id="e4a36-122">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="e4a36-122">*InfoLevel*</span></span>

<span data-ttu-id="e4a36-123">Сведения, которые будут храниться в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="e4a36-123">The information that will be stored in *pvResult*.</span></span> <span data-ttu-id="e4a36-124">Для этого параметра можно использовать следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="e4a36-124">The following options can be used for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4a36-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e4a36-125">Value</span></span></p></th>
<th><p><span data-ttu-id="e4a36-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e4a36-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-127">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="e4a36-127">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="e4a36-128"><em>пвресулт</em> интерпретируется как структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="e4a36-128"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="e4a36-129">При успешном выполнении структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> получает сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="e4a36-129">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="e4a36-130">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-130">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-131">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="e4a36-131">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="e4a36-132"><em>пвресулт</em> интерпретируется как ULong.</span><span class="sxs-lookup"><span data-stu-id="e4a36-132"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="e4a36-133">В случае успеха ULONG содержит количество индексов в указанной таблице.</span><span class="sxs-lookup"><span data-stu-id="e4a36-133">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="e4a36-134"><em>сзиндекснаме</em> игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e4a36-134"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="e4a36-135">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-135">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-136">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="e4a36-136">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="e4a36-137"><em>пвресулт</em> интерпретируется как <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="e4a36-137"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="e4a36-138">При успешном выполнении структура <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> получает сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="e4a36-138">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="e4a36-139">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-139">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-140">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="e4a36-140">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="e4a36-141">JET_IdxInfoLangid не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="e4a36-141">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="e4a36-142">Вместо этого используйте JET_IdxInfoLCID и макрос <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">лангидфромлЦид</a> .</span><span class="sxs-lookup"><span data-stu-id="e4a36-142">Use JET_IdxInfoLCID and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-143">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="e4a36-143">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="e4a36-144"><em>пвресулт</em> интерпретируется как LCID.</span><span class="sxs-lookup"><span data-stu-id="e4a36-144"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="e4a36-145">При успешном выполнении код LCID содержит идентификатор локали индекса.</span><span class="sxs-lookup"><span data-stu-id="e4a36-145">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="e4a36-146">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-146">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="e4a36-147"><strong>Windows XP:  </strong> JET_IdxInfoLCID введен в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e4a36-147"><strong>Windows XP:  </strong>JET_IdxInfoLCID is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-148">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="e4a36-148">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="e4a36-149"><em>пвресулт</em> интерпретируется как структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="e4a36-149"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="e4a36-150">При успешном выполнении структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> получает сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="e4a36-150">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="e4a36-151">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-151">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-152">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="e4a36-152">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="e4a36-153">JET_IdxInfoOLC устарел.</span><span class="sxs-lookup"><span data-stu-id="e4a36-153">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-154">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="e4a36-154">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="e4a36-155">JET_IdxInfoResetOLC устарел.</span><span class="sxs-lookup"><span data-stu-id="e4a36-155">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-156">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="e4a36-156">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="e4a36-157"><em>пвресулт</em> интерпретируется как ULong.</span><span class="sxs-lookup"><span data-stu-id="e4a36-157"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="e4a36-158">При успешном выполнении в ULONG содержится место использования индекса.</span><span class="sxs-lookup"><span data-stu-id="e4a36-158">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="e4a36-159">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-160">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="e4a36-160">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="e4a36-161">JET_IdxInfoSysTabCursor устарел.</span><span class="sxs-lookup"><span data-stu-id="e4a36-161">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-162">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="e4a36-162">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="e4a36-163"><em>пвресулт</em> интерпретируется как ushort.</span><span class="sxs-lookup"><span data-stu-id="e4a36-163"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="e4a36-164">При успешном выполнении объект USHORT содержит значение <em>кбварсегмак</em> , используемое при создании индекса.</span><span class="sxs-lookup"><span data-stu-id="e4a36-164">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="e4a36-165">Описание <em>кбварсегмак</em>см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="e4a36-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="e4a36-166">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-166">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-167">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="e4a36-167">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="e4a36-168"><em>пвресулт</em> интерпретируется как ushort.</span><span class="sxs-lookup"><span data-stu-id="e4a36-168"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="e4a36-169">При успешном выполнении объект USHORT содержит значение <em>кбкэймост</em> , используемое при создании индекса.</span><span class="sxs-lookup"><span data-stu-id="e4a36-169">On success, the USHORT holds the value of <em>cbKeyMost</em> used when the index was created.</span></span> <span data-ttu-id="e4a36-170">Описание <em>кбкэймост</em>см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="e4a36-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbKeyMost</em>.</span></span> <span data-ttu-id="e4a36-171">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="e4a36-172"><strong>Windows Vista:  </strong> JET_IdxInfoKeyMost введен в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e4a36-172"><strong>Windows Vista:  </strong>JET_IdxInfoKeyMost is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-173">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="e4a36-173">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="e4a36-174"><em>пвресулт</em> интерпретируется как структура <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="e4a36-174"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="e4a36-175">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="e4a36-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e4a36-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-177">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="e4a36-177">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="e4a36-178"><em>пвресулт</em> интерпретируется как структура <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="e4a36-178"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="e4a36-179">При сбое содержимое <em>пвбуффер</em> не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-179">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="e4a36-180"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e4a36-180"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e4a36-181">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4a36-181">Return Value</span></span>

<span data-ttu-id="e4a36-182">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="e4a36-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e4a36-183">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e4a36-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4a36-184">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e4a36-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="e4a36-185">Описание</span><span class="sxs-lookup"><span data-stu-id="e4a36-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e4a36-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e4a36-187">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e4a36-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-188">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="e4a36-188">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="e4a36-189">Указанный индекс не найден в указанной таблице.</span><span class="sxs-lookup"><span data-stu-id="e4a36-189">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-190">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="e4a36-190">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="e4a36-191">Буфер, переданный как <em>пвресулт</em> , слишком мал.</span><span class="sxs-lookup"><span data-stu-id="e4a36-191">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="e4a36-192">Содержимое буфера не определено.</span><span class="sxs-lookup"><span data-stu-id="e4a36-192">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e4a36-193">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4a36-193">Remarks</span></span>

<span data-ttu-id="e4a36-194">**Жетжетиндексинфо** и [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md) извлекают идентичные сведения о индексе.</span><span class="sxs-lookup"><span data-stu-id="e4a36-194">**JetGetIndexInfo** and [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) retrieve identical information about an index.</span></span> <span data-ttu-id="e4a36-195">Разница заключается в том, как указана таблица.</span><span class="sxs-lookup"><span data-stu-id="e4a36-195">The difference is in how the table is specified.</span></span> <span data-ttu-id="e4a36-196">**Жетжетиндексинфо** ждет базу данных (*DBID*) и имя таблицы (*сзтабленаме*), а [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md) — идентификатор таблицы (*TableID*).</span><span class="sxs-lookup"><span data-stu-id="e4a36-196">**JetGetIndexInfo** expects a database (*dbid*) and name of a table (*szTableName*), while [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="e4a36-197">Требования</span><span class="sxs-lookup"><span data-stu-id="e4a36-197">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-198"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e4a36-198"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e4a36-199">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e4a36-199">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-200"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e4a36-200"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e4a36-201">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e4a36-201">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-202"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e4a36-202"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e4a36-203">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e4a36-203">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-204"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="e4a36-204"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e4a36-205">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e4a36-205">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a36-206"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="e4a36-206"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e4a36-207">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e4a36-207">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a36-208"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="e4a36-208"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e4a36-209">Реализуется как <strong>жетжетиндексинфов</strong> (Юникод) и <strong>жетжетиндексинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e4a36-209">Implemented as <strong>JetGetIndexInfoW</strong> (Unicode) and <strong>JetGetIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e4a36-210">См. также:</span><span class="sxs-lookup"><span data-stu-id="e4a36-210">See Also</span></span>

[<span data-ttu-id="e4a36-211">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e4a36-211">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e4a36-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e4a36-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e4a36-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e4a36-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e4a36-214">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="e4a36-214">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="e4a36-215">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="e4a36-215">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="e4a36-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e4a36-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e4a36-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e4a36-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e4a36-218">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="e4a36-218">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
