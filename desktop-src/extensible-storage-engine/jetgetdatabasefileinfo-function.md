---
description: Дополнительные сведения о функции Жетжетдатабасефилеинфо
title: Функция Жетжетдатабасефилеинфо
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656713"
---
# <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="3165b-103">Функция Жетжетдатабасефилеинфо</span><span class="sxs-lookup"><span data-stu-id="3165b-103">JetGetDatabaseFileInfo Function</span></span>


<span data-ttu-id="3165b-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3165b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="3165b-105">Функция Жетжетдатабасефилеинфо</span><span class="sxs-lookup"><span data-stu-id="3165b-105">JetGetDatabaseFileInfo Function</span></span>

<span data-ttu-id="3165b-106">Функция **жетжетдатабасефилеинфо** извлекает различные типы сведений о базе данных.</span><span class="sxs-lookup"><span data-stu-id="3165b-106">The **JetGetDatabaseFileInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="3165b-107">Этот API может вызываться, когда база данных подключена или находится в режиме «в сети» (с [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md)) либо база данных или ядро СУБД находятся в режиме «вне сети» (с **жетжетдатабасефилеинфо**).</span><span class="sxs-lookup"><span data-stu-id="3165b-107">This API can be called while a database is attached or online (with [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) or while the database or database engine is offline (with **JetGetDatabaseFileInfo**).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="3165b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3165b-108">Parameters</span></span>

<span data-ttu-id="3165b-109">*сздатабасенаме*</span><span class="sxs-lookup"><span data-stu-id="3165b-109">*szDatabaseName*</span></span>

<span data-ttu-id="3165b-110">Путь к базе данных, из которой извлекаются сведения.</span><span class="sxs-lookup"><span data-stu-id="3165b-110">The path of the database from which to retrieve the information.</span></span>

<span data-ttu-id="3165b-111">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="3165b-111">*pvResult*</span></span>

<span data-ttu-id="3165b-112">Указатель на буфер, который будет принимать указанные сведения.</span><span class="sxs-lookup"><span data-stu-id="3165b-112">Pointer to a buffer that will receive the specified information.</span></span> <span data-ttu-id="3165b-113">Размер буфера в байтах передается в *кбмакс*.</span><span class="sxs-lookup"><span data-stu-id="3165b-113">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="3165b-114">Если эта функция завершается ошибкой, содержимое *пвресулт* не определено.</span><span class="sxs-lookup"><span data-stu-id="3165b-114">If this function fails, the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="3165b-115">Сведения, хранящиеся в *пвресулт* , зависят от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="3165b-115">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="3165b-116">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="3165b-116">*cbMax*</span></span>

<span data-ttu-id="3165b-117">Размер буфера (в байтах), переданного в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="3165b-117">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="3165b-118">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="3165b-118">*InfoLevel*</span></span>

<span data-ttu-id="3165b-119">*Инфолевел* указывает, какой тип сведений следует получить о указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="3165b-119">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="3165b-120">Это влияет на интерпретацию *пвресулт* .</span><span class="sxs-lookup"><span data-stu-id="3165b-120">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="3165b-121">Некоторые объекты *инфолевел* доступны только в автономной (**жетжетдатабасефилеинфо**) или интерактивной версии ([жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md)) API.</span><span class="sxs-lookup"><span data-stu-id="3165b-121">Some *InfoLevel* objects are available only in the offline (**JetGetDatabaseFileInfo**) or online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) version of the API.</span></span>

<span data-ttu-id="3165b-122">Если предоставленный буфер *пвресулт* слишком мал, возвращается либо JET_errInvalidBufferSize, либо JET_errBufferTooSmall, в зависимости от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="3165b-122">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned, depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3165b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3165b-123">Value</span></span></p></th>
<th><p><span data-ttu-id="3165b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3165b-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3165b-125">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="3165b-125">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="3165b-126"><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как QWORD (8 байт).</span><span class="sxs-lookup"><span data-stu-id="3165b-126"><em>pvResult</em> will be interpreted as a QWORD (8 bytes).</span></span> <span data-ttu-id="3165b-127">Возвращает размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="3165b-127">Returns the size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-128">JET_DbInfoUpgrade</span><span class="sxs-lookup"><span data-stu-id="3165b-128">JET_DbInfoUpgrade</span></span></p></td>
<td><p><span data-ttu-id="3165b-129"><em>пвресулт</em> будет интерпретирован как <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span><span class="sxs-lookup"><span data-stu-id="3165b-129"><em>pvResult</em> will be interpreted as a <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span></span> <span data-ttu-id="3165b-130">Структура <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> будет заполнена сведениями, относящимися к указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="3165b-130">The <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-131">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="3165b-131">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="3165b-132"><em>пвресулт</em> будет интерпретирован как <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="3165b-132"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="3165b-133">Структура <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> будет заполнена сведениями, относящимися к указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="3165b-133">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-134">JET_DbInfoDBInUse</span><span class="sxs-lookup"><span data-stu-id="3165b-134">JET_DbInfoDBInUse</span></span></p></td>
<td><p><span data-ttu-id="3165b-135"><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как bool (4 байта).</span><span class="sxs-lookup"><span data-stu-id="3165b-135"><em>pvResult</em> will be interpreted as a BOOL (4 bytes).</span></span> <span data-ttu-id="3165b-136">Это приведет к возвращению наличия открытых или подключенных баз данных в настоящий момент в ядре СУБД.</span><span class="sxs-lookup"><span data-stu-id="3165b-136">This will return whether the database engine currently has any open or attached databases.</span></span></p>
<p><span data-ttu-id="3165b-137"><strong>Windows XP:  </strong> Это значение вводится в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3165b-137"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-138">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="3165b-138">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="3165b-139"><em>пвресулт</em> будет интерпретироваться как длинное целое без знака.</span><span class="sxs-lookup"><span data-stu-id="3165b-139"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="3165b-140">Это приведет к возврату размера страницы базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="3165b-140">This will return the page size of the database in bytes.</span></span></p>
<p><span data-ttu-id="3165b-141"><strong>Windows XP:  </strong> Это значение вводится в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3165b-141"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-142">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="3165b-142">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="3165b-143">Эти <em>инфолевелс</em> пока не поддерживаются и возвращают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3165b-143">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="3165b-144">Не используйте эти <em>инфолевелс</em>.</span><span class="sxs-lookup"><span data-stu-id="3165b-144">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-145">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="3165b-145">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="3165b-146">Эти <em>инфолевелс</em> пока не поддерживаются и возвращают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3165b-146">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="3165b-147">Не используйте эти <em>инфолевелс</em>.</span><span class="sxs-lookup"><span data-stu-id="3165b-147">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-148">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="3165b-148">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="3165b-149">То же, что и JET_DbInfoCp.</span><span class="sxs-lookup"><span data-stu-id="3165b-149">Same as JET_DbInfoCp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-150">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="3165b-150">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="3165b-151">Эти <em>инфолевелс</em> являются устаревшими и сейчас не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3165b-151">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="3165b-152">Не используйте эти <em>инфолевелс</em>.</span><span class="sxs-lookup"><span data-stu-id="3165b-152">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-153">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="3165b-153">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="3165b-154">То же, что и JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="3165b-154">Same as JET_DbInfoIsam.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-155">JET_DbInfoFileType</span><span class="sxs-lookup"><span data-stu-id="3165b-155">JET_DbInfoFileType</span></span></p></td>
<td><p><span data-ttu-id="3165b-156"><strong>Windows Vista:  </strong> Это значение <em>инфолевел</em> введено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3165b-156"><strong>Windows Vista:  </strong>This <em>InfoLevel</em> value is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="3165b-157"><em>пвресулт</em> будет рассматриваться как указатель на DWORD.</span><span class="sxs-lookup"><span data-stu-id="3165b-157"><em>pvResult</em> will be treated as a pointer to a DWORD.</span></span> <span data-ttu-id="3165b-158">Возвращает значение перечисления, указывающее тип файла, который подсистема считает этим средством.</span><span class="sxs-lookup"><span data-stu-id="3165b-158">Returns an enumeration value, indicating what kind of file the engine considers this to be.</span></span> <span data-ttu-id="3165b-159">Типы файлов перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3165b-159">File types are listed in the following table.</span></span> <span data-ttu-id="3165b-160">Дополнительные сведения об этих типах файлов и их использовании в подсистеме см. в разделе <a href="gg294069(v=exchg.10).md">Расширенные файлы подсистемы хранилища</a>.</span><span class="sxs-lookup"><span data-stu-id="3165b-160">For more information about these types of files and their usage to the engine, see <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3165b-161">Значение</span><span class="sxs-lookup"><span data-stu-id="3165b-161">Value</span></span></p></th>
<th><p><span data-ttu-id="3165b-162">Значение</span><span class="sxs-lookup"><span data-stu-id="3165b-162">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3165b-163">JET_filetypeUnknown</span><span class="sxs-lookup"><span data-stu-id="3165b-163">JET_filetypeUnknown</span></span></p></td>
<td><p><span data-ttu-id="3165b-164">Тип файла неизвестен или не является типом файла ESE.</span><span class="sxs-lookup"><span data-stu-id="3165b-164">The type of file is unknown, or not an ESE file type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-165">JET_filetypeDatabase</span><span class="sxs-lookup"><span data-stu-id="3165b-165">JET_filetypeDatabase</span></span></p></td>
<td><p><span data-ttu-id="3165b-166">Файл является файлом базы данных.</span><span class="sxs-lookup"><span data-stu-id="3165b-166">The file is a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-167">JET_filetypeLog</span><span class="sxs-lookup"><span data-stu-id="3165b-167">JET_filetypeLog</span></span></p></td>
<td><p><span data-ttu-id="3165b-168">Файл является файлом журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="3165b-168">The file is a transaction log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-169">JET_filetypeCheckpoint</span><span class="sxs-lookup"><span data-stu-id="3165b-169">JET_filetypeCheckpoint</span></span></p></td>
<td><p><span data-ttu-id="3165b-170">Файл является файлом контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="3165b-170">The file is a checkpoint file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-171">JET_filetypeTempDatabase</span><span class="sxs-lookup"><span data-stu-id="3165b-171">JET_filetypeTempDatabase</span></span></p></td>
<td><p><span data-ttu-id="3165b-172">Файл является временным файлом базы данных.</span><span class="sxs-lookup"><span data-stu-id="3165b-172">The file is a temporary database file.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3165b-173">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3165b-173">Return Value</span></span>

<span data-ttu-id="3165b-174">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="3165b-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3165b-175">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3165b-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3165b-176">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3165b-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="3165b-177">Описание</span><span class="sxs-lookup"><span data-stu-id="3165b-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3165b-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3165b-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3165b-179">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3165b-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-180">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="3165b-180">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="3165b-181">Запрошенный <em>инфолевел</em> был JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="3165b-181">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="3165b-182">Такой способ связывания не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3165b-182">This is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-183">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="3165b-183">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="3165b-184">Буфер, указанный в <em>кбмакс</em> , слишком мал для получения требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="3165b-184">The buffer that is given in <em>cbMax</em> is too small for the desired information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-185">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="3165b-185">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="3165b-186">Буфер, указанный в <em>кбмакс</em> , имеет неправильный размер для требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="3165b-186">The buffer that is given in <em>cbMax</em> is not the correct size for the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3165b-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3165b-188">Один из предоставленных параметров содержит непредвиденное значение, или сочетание нескольких значений параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="3165b-188">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="3165b-189">Эта ошибка будет возвращена <a href="gg294076(v=exchg.10).md">жетжетдатабасеинфо</a> , если предоставленный DBID не является допустимой (присоединенной) базой данных.</span><span class="sxs-lookup"><span data-stu-id="3165b-189">This error will be returned by <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when the DBID provided is not a valid (attached) database.</span></span> <span data-ttu-id="3165b-190">Эта ошибка будет возвращена <strong>жетжетдатабасефилеинфо</strong> и <a href="gg294076(v=exchg.10).md">жетжетдатабасеинфо</a> , когда запрошенный <em>инфолевел</em> не поддерживается этой версией функции.</span><span class="sxs-lookup"><span data-stu-id="3165b-190">This error will be returned by <strong>JetGetDatabaseFileInfo</strong> and <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3165b-191">Если эта функция выполнена, запрошенные данные будут возвращены в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="3165b-191">If this function succeeds, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="3165b-192">Если эта функция завершается ошибкой, выходной буфер будет находиться в неопределенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="3165b-192">If this function fails, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3165b-193">Требования</span><span class="sxs-lookup"><span data-stu-id="3165b-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3165b-194"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="3165b-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3165b-195">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3165b-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3165b-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3165b-197">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3165b-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3165b-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3165b-199">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3165b-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-200"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="3165b-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3165b-201">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3165b-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3165b-202"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="3165b-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3165b-203">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3165b-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3165b-204"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="3165b-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3165b-205">Реализуется как <strong>жетжетдатабасефилеинфов</strong> (Юникод) и <strong>жетжетдатабасефилеинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3165b-205">Implemented as <strong>JetGetDatabaseFileInfoW</strong> (Unicode) and <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3165b-206">См. также:</span><span class="sxs-lookup"><span data-stu-id="3165b-206">See Also</span></span>

[<span data-ttu-id="3165b-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3165b-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3165b-208">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="3165b-208">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="3165b-209">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="3165b-209">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="3165b-210">жетжетдатабасеинфо</span><span class="sxs-lookup"><span data-stu-id="3165b-210">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)
