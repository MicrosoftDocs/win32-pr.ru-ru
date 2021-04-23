---
description: Дополнительные сведения о функции Жетжетдатабасеинфо
title: Функция JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264775"
---
# <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="89751-103">Функция JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="89751-103">JetGetDatabaseInfo Function</span></span>


<span data-ttu-id="89751-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="89751-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="89751-105">Функция JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="89751-105">JetGetDatabaseInfo Function</span></span>

<span data-ttu-id="89751-106">Функция **жетжетдатабасеинфо** извлекает различные типы сведений о базе данных.</span><span class="sxs-lookup"><span data-stu-id="89751-106">The **JetGetDatabaseInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="89751-107">Этот API может вызываться, когда база данных подключена или находится в режиме «в сети» (с **жетжетдатабасеинфо**) либо база данных или ядро СУБД находятся в режиме «вне сети» (с [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="89751-107">This API can be called while a database is attached or online (with **JetGetDatabaseInfo**) or while the database or database engine is offline (with [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="89751-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="89751-108">Parameters</span></span>

<span data-ttu-id="89751-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="89751-109">*sesid*</span></span>

<span data-ttu-id="89751-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="89751-110">The session to use for this call.</span></span>

<span data-ttu-id="89751-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="89751-111">*dbid*</span></span>

<span data-ttu-id="89751-112">[JET_DBID](./jet-dbid.md) для базы данных, из которой извлекаются сведения.</span><span class="sxs-lookup"><span data-stu-id="89751-112">The [JET_DBID](./jet-dbid.md) for the database to retrieve the information from.</span></span>

<span data-ttu-id="89751-113">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="89751-113">*pvResult*</span></span>

<span data-ttu-id="89751-114">Указатель на буфер, который получит указанные сведения.</span><span class="sxs-lookup"><span data-stu-id="89751-114">Pointer to a buffer which will receive the specified information.</span></span> <span data-ttu-id="89751-115">Размер буфера в байтах передается в *кбмакс*.</span><span class="sxs-lookup"><span data-stu-id="89751-115">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="89751-116">При сбое содержимое *пвресулт* не определено.</span><span class="sxs-lookup"><span data-stu-id="89751-116">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="89751-117">Сведения, хранящиеся в *пвресулт* , зависят от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="89751-117">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="89751-118">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="89751-118">*cbMax*</span></span>

<span data-ttu-id="89751-119">Размер (в байтах) буфера, переданного в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="89751-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="89751-120">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="89751-120">*InfoLevel*</span></span>

<span data-ttu-id="89751-121">*Инфолевел* указывает, какой тип сведений следует получить о указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="89751-121">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="89751-122">Это влияет на интерпретацию *пвресулт* .</span><span class="sxs-lookup"><span data-stu-id="89751-122">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="89751-123">Некоторые *инфолевел* доступны только в автономной ([жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md)) или интерактивной версии (**жетжетдатабасеинфо**) API.</span><span class="sxs-lookup"><span data-stu-id="89751-123">Some *InfoLevel* are available only in the offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) or online (**JetGetDatabaseInfo**) version of the API.</span></span>

<span data-ttu-id="89751-124">Если предоставленный буфер *пвресулт* слишком мал, то в зависимости от *инфолевел* будет возвращаться либо JET_errInvalidBufferSize, либо JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="89751-124">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89751-125">Значение</span><span class="sxs-lookup"><span data-stu-id="89751-125">Value</span></span></p></th>
<th><p><span data-ttu-id="89751-126">Значение</span><span class="sxs-lookup"><span data-stu-id="89751-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89751-127">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="89751-127">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="89751-128">Пока не поддерживаются и не возвращают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89751-128">Not yet supported and return default values.</span></span> <span data-ttu-id="89751-129">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="89751-129">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-130">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="89751-130">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="89751-131">Эти <em>инфолевелс</em> являются устаревшими и сейчас не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="89751-131">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="89751-132">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="89751-132">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-133">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="89751-133">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="89751-134">Пока не поддерживаются и не возвращают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89751-134">Not yet supported and return default values.</span></span> <span data-ttu-id="89751-135">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="89751-135">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-136">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="89751-136">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="89751-137">Пока не поддерживаются и не возвращают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89751-137">Not yet supported and return default values.</span></span> <span data-ttu-id="89751-138">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="89751-138">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-139">JET_DbInfoFilename</span><span class="sxs-lookup"><span data-stu-id="89751-139">JET_DbInfoFilename</span></span></p></td>
<td><p><span data-ttu-id="89751-140"><em>пвресулт</em> будет интерпретирован как строковый буфер (char \*).</span><span class="sxs-lookup"><span data-stu-id="89751-140"><em>pvResult</em> will be interpreted as a string buffer (char \*).</span></span> <span data-ttu-id="89751-141">Рекомендуется MAX_PATH буфер, но не требуется.</span><span class="sxs-lookup"><span data-stu-id="89751-141">A MAX_PATH buffer is suggested, however not required.</span></span> <span data-ttu-id="89751-142">Если буфер не достаточно длинный, будет возвращен JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="89751-142">If the buffer is not long enough, JET_errBufferTooSmall will be returned.</span></span> <span data-ttu-id="89751-143">Строка будет заполнена путем к базе данных для этого DBID.</span><span class="sxs-lookup"><span data-stu-id="89751-143">The string will be populated with the path of the database for this DBID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-144">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="89751-144">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="89751-145"><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="89751-145"><em>pvResult</em> will be interpreted as a DWORD (4 bytes).</span></span> <span data-ttu-id="89751-146">Возвращает размер базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="89751-146">Returns the size of the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-147">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="89751-147">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="89751-148">Эти <em>инфолевелс</em> являются устаревшими и сейчас не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="89751-148">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="89751-149">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="89751-149">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-150">JET_DbInfoLCID</span><span class="sxs-lookup"><span data-stu-id="89751-150">JET_DbInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="89751-151">(Windows XP и более поздние версии) Этот <em>инфолевел</em> был первоначально указан как JET_DbInfoLangid (Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="89751-151">(Windows XP and later) This <em>InfoLevel</em> was originally specified as: JET_DbInfoLangid (Windows 2000)</span></span></p>
<p><span data-ttu-id="89751-152"><em>пвресулт</em> будет интерпретироваться как длинное.</span><span class="sxs-lookup"><span data-stu-id="89751-152"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="89751-153">Он возвращает код локали (LCID), связанный с этой базой данных.</span><span class="sxs-lookup"><span data-stu-id="89751-153">This returns the Locale identifier (LCID) associate with this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-154">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="89751-154">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="89751-155"><em>пвресулт</em> будет интерпретирован как <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="89751-155"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="89751-156">Структура <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> будет заполнена сведениями, относящимися к указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="89751-156">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the database specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-157">JET_DbInfoOptions</span><span class="sxs-lookup"><span data-stu-id="89751-157">JET_DbInfoOptions</span></span></p></td>
<td><p><span data-ttu-id="89751-158"><em>пвресулт</em> будет интерпретирован как <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span><span class="sxs-lookup"><span data-stu-id="89751-158"><em>pvResult</em> will be interpreted as a <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span></span> <span data-ttu-id="89751-159">Он возвращает значение, указывающее, открыта ли база данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="89751-159">This returns whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="89751-160">Если база данных находится в монопольном режиме JET_bitDbExclusive будет задана в предоставленном <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> , в противном случае устанавливается ноль.</span><span class="sxs-lookup"><span data-stu-id="89751-160">If the database is in exclusive mode JET_bitDbExclusive will be set in the <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> provided, otherwise zero is set.</span></span> <span data-ttu-id="89751-161">Обратите внимание, что другие параметры <em>грбит</em> базы данных для <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a> и <a href="gg269299(v=exchg.10).md">жетопендатабасе</a> не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="89751-161">Note other database <em>grbit</em> options for <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> and <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> are not returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-162">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="89751-162">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="89751-163">Доступно только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="89751-163">Available only on Windows XP and later.</span></span> <span data-ttu-id="89751-164"><em>пвресулт</em> будет интерпретироваться как длинное целое без знака.</span><span class="sxs-lookup"><span data-stu-id="89751-164"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="89751-165">Это приведет к возврату размера страницы базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="89751-165">This will return the page size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-166">JET_DbInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="89751-166">JET_DbInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="89751-167"><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как DWORD.</span><span class="sxs-lookup"><span data-stu-id="89751-167"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="89751-168">Он возвращает доступное место для базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="89751-168">This returns the available space for the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-169">JET_DbInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="89751-169">JET_DbInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="89751-170"><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как DWORD.</span><span class="sxs-lookup"><span data-stu-id="89751-170"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="89751-171">В результате будет возвращено пространство для базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="89751-171">This returns the owned space for the database in pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-172">JET_DbInfoTransactions</span><span class="sxs-lookup"><span data-stu-id="89751-172">JET_DbInfoTransactions</span></span></p></td>
<td><p><span data-ttu-id="89751-173"><em>пвресулт</em> будет интерпретироваться как длинное.</span><span class="sxs-lookup"><span data-stu-id="89751-173"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="89751-174">Будет возвращено значение, превышающее максимальный уровень, до которого транзакции могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="89751-174">This will return one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="89751-175">Если <a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a> вызывается (во вложенном режиме, то есть в том же сеансе без фиксации или отката), то при последнем вызове JET_errTransTooDeep будет возвращено из <a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a>.</span><span class="sxs-lookup"><span data-stu-id="89751-175">If <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call JET_errTransTooDeep will be returned from <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span></span> <span data-ttu-id="89751-176">Обратите внимание, что значение в Windows 2000, Windows XP и Windows Server 2003 — 7.</span><span class="sxs-lookup"><span data-stu-id="89751-176">Note the value in Windows 2000, Windows XP, and Windows Server 2003 is 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-177">JET_DbInfoVersion</span><span class="sxs-lookup"><span data-stu-id="89751-177">JET_DbInfoVersion</span></span></p></td>
<td><p><span data-ttu-id="89751-178"><em>пвресулт</em> будет интерпретироваться как длинное.</span><span class="sxs-lookup"><span data-stu-id="89751-178"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="89751-179">Он возвращает собственный основной номер версии ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="89751-179">This returns the database engine's native major version.</span></span> <span data-ttu-id="89751-180">Это значение равно 0x620 для Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89751-180">This value is 0x620 for Windows 2000, Windows XP, and Windows Server 2003.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="89751-181">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89751-181">Return Value</span></span>

<span data-ttu-id="89751-182">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="89751-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="89751-183">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="89751-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89751-184">Код возврата</span><span class="sxs-lookup"><span data-stu-id="89751-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="89751-185">Описание</span><span class="sxs-lookup"><span data-stu-id="89751-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89751-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="89751-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="89751-187">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="89751-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-188">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="89751-188">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="89751-189">Размер буфера, заданного в <em>кбмакс</em> , слишком мал (или неправильный) для хранения требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="89751-189">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-190">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="89751-190">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="89751-191">Запрошенный <em>инфолевел</em> был JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="89751-191">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="89751-192">Такой способ связывания не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="89751-192">This is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-193">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="89751-193">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="89751-194">Размер буфера, заданного в <em>кбмакс</em> , слишком мал (или неправильный) для хранения требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="89751-194">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-195">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="89751-195">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="89751-196">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="89751-196">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="89751-197">Эта ошибка будет возвращена <strong>жетжетдатабасеинфо</strong> , если предоставленная <a href="gg269248(v=exchg.10).md">JET_DBID</a> не является допустимой (присоединенной) базой данных.</span><span class="sxs-lookup"><span data-stu-id="89751-197">This error will be returned by <strong>JetGetDatabaseInfo</strong> when the <a href="gg269248(v=exchg.10).md">JET_DBID</a> provided is not a valid (attached) database.</span></span> <span data-ttu-id="89751-198">Эта ошибка будет возвращена <a href="gg269239(v=exchg.10).md">жетжетдатабасефилеинфо</a> и <strong>жетжетдатабасеинфо</strong> , когда запрошенный <em>инфолевел</em> не поддерживается этой версией функции.</span><span class="sxs-lookup"><span data-stu-id="89751-198">This error will be returned by <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> and <strong>JetGetDatabaseInfo</strong> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89751-199">При успешном выполнении запрошенные данные будут возвращены в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="89751-199">On success, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="89751-200">В случае сбоя выходной буфер будет находиться в неопределенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="89751-200">On failure, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="89751-201">Требования</span><span class="sxs-lookup"><span data-stu-id="89751-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89751-202"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="89751-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="89751-203">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="89751-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="89751-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="89751-205">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="89751-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="89751-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="89751-207">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="89751-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-208"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="89751-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="89751-209">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="89751-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89751-210"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="89751-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="89751-211">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="89751-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89751-212"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="89751-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="89751-213">Реализуется как <strong>жетжетдатабасеинфов</strong> (Юникод) и <strong>жетжетдатабасеинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="89751-213">Implemented as <strong>JetGetDatabaseInfoW</strong> (Unicode) and <strong>JetGetDatabaseInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="89751-214">См. также:</span><span class="sxs-lookup"><span data-stu-id="89751-214">See Also</span></span>

[<span data-ttu-id="89751-215">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="89751-215">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="89751-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="89751-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="89751-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="89751-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="89751-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="89751-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="89751-219">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="89751-219">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="89751-220">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="89751-220">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="89751-221">жетжетдатабасефилеинфо</span><span class="sxs-lookup"><span data-stu-id="89751-221">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
