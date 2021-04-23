---
description: Дополнительные сведения о функции Жетсетдатабасесизе
title: Функция Жетсетдатабасесизе
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143504"
---
# <a name="jetsetdatabasesize-function"></a><span data-ttu-id="20163-103">Функция Жетсетдатабасесизе</span><span class="sxs-lookup"><span data-stu-id="20163-103">JetSetDatabaseSize Function</span></span>


<span data-ttu-id="20163-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20163-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetdatabasesize-function"></a><span data-ttu-id="20163-105">Функция Жетсетдатабасесизе</span><span class="sxs-lookup"><span data-stu-id="20163-105">JetSetDatabaseSize Function</span></span>

<span data-ttu-id="20163-106">Функция **жетсетдатабасесизе** задает размер неоткрытого файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="20163-106">The **JetSetDatabaseSize** function sets the size of an unopened database file.</span></span>

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="20163-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="20163-107">Parameters</span></span>

<span data-ttu-id="20163-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="20163-108">*sesid*</span></span>

<span data-ttu-id="20163-109">Определяет контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="20163-109">Identifies the database session context to use for the API call.</span></span>

<span data-ttu-id="20163-110">*сздатабасенаме*</span><span class="sxs-lookup"><span data-stu-id="20163-110">*szDatabaseName*</span></span>

<span data-ttu-id="20163-111">Определяет имя файла базы данных, размер которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="20163-111">Identifies the name of the database file whose size is to be altered.</span></span>

<span data-ttu-id="20163-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="20163-112">*cpg*</span></span>

<span data-ttu-id="20163-113">Задает требуемый размер базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="20163-113">Specifies the desired size of the database, in pages.</span></span>

<span data-ttu-id="20163-114">*пкпгреал*</span><span class="sxs-lookup"><span data-stu-id="20163-114">*pcpgReal*</span></span>

<span data-ttu-id="20163-115">Указатель на число, которое получает размер базы данных на страницах после вызова API.</span><span class="sxs-lookup"><span data-stu-id="20163-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="20163-116">Если вызов API завершился неудачно, содержимое *пкпгреал* не определено.</span><span class="sxs-lookup"><span data-stu-id="20163-116">If the API call was unsuccessful, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="20163-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20163-117">Return Value</span></span>

<span data-ttu-id="20163-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="20163-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="20163-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="20163-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20163-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="20163-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="20163-121">Описание</span><span class="sxs-lookup"><span data-stu-id="20163-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20163-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="20163-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="20163-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="20163-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20163-124">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="20163-124">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="20163-125">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="20163-125">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="20163-126">JET_errDatabaseInconsistent и JET_errDatabaseDirtyShutdown имеют одно и то же числовое значение.</span><span class="sxs-lookup"><span data-stu-id="20163-126">JET_errDatabaseInconsistent and JET_errDatabaseDirtyShutdown are the same numeric value.</span></span> <span data-ttu-id="20163-127">База данных, размер которой необходимо настроить, должен быть в состоянии чистого отключения, известного как противоречивое состояние.</span><span class="sxs-lookup"><span data-stu-id="20163-127">The database whose size is to be adjusted must be in a clean shutdown, known as a consistent state.</span></span> <span data-ttu-id="20163-128">Непоследовательная база данных не повреждена, но она требует воспроизведения файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="20163-128">An inconsistent database is not corrupted, but it requires log files to be replayed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20163-129">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="20163-129">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="20163-130"><em>сздатабасенаме</em> не может быть пустой строкой, отличной от NULL.</span><span class="sxs-lookup"><span data-stu-id="20163-130"><em>szDatabaseName</em> must not be an empty, non-NULL string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20163-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="20163-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="20163-132">Недостаточно свободного места на томе для выполнения операции увеличения.</span><span class="sxs-lookup"><span data-stu-id="20163-132">There is insufficient free space on the volume to perform the grow operation.</span></span> <span data-ttu-id="20163-133"><strong>Жетсетдатабасесизе</strong> также может возвращать множество ошибок, связанных с файлами, включая, но не ограничиваясь:</span><span class="sxs-lookup"><span data-stu-id="20163-133"><strong>JetSetDatabaseSize</strong> may also return many file-related errors, including, but not limited to:</span></span></p>
<ul>
<li><p><span data-ttu-id="20163-134">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="20163-134">JET_errDiskIO</span></span></p></li>
<li><p><span data-ttu-id="20163-135">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="20163-135">JET_errFileNotFound</span></span></p></li>
<li><p><span data-ttu-id="20163-136">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="20163-136">JET_errInvalidPath</span></span></p></li>
<li><p><span data-ttu-id="20163-137">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="20163-137">JET_errFileAccessDenied</span></span></p></li>
<li><p><span data-ttu-id="20163-138">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="20163-138">JET_errOutOfFileHandles</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20163-139">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="20163-139">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="20163-140">Одна из причин, по которой эта ошибка может быть возвращена, — если <em>CPG</em> соответствует минимальному размеру базы данных.</span><span class="sxs-lookup"><span data-stu-id="20163-140">One of the reasons this error may be returned is if <em>cpg</em> does meet the minimum database size.</span></span> <span data-ttu-id="20163-141">Текущий минимальный размер базы данных — 256 страниц.</span><span class="sxs-lookup"><span data-stu-id="20163-141">The current minimum database size is 256 pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20163-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="20163-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="20163-143">Системе не хватает ресурсов памяти.</span><span class="sxs-lookup"><span data-stu-id="20163-143">The system is low on memory resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="20163-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20163-144">Remarks</span></span>

<span data-ttu-id="20163-145">Если **жетсетдатабасесизе** вызывается до вставки больших объемов данных, то файл базы данных будет увеличен за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="20163-145">If **JetSetDatabaseSize** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="20163-146">Это снизит вероятность того, что файл базы данных станет фрагментированным на уровне файловой системы, а также сократит число попыток увеличения размера файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="20163-146">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="20163-147">Увеличение файла базы данных выполняется один раз быстрее, чем в несколько раз.</span><span class="sxs-lookup"><span data-stu-id="20163-147">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="20163-148">В настоящее время поддерживается только увеличение размера файла.</span><span class="sxs-lookup"><span data-stu-id="20163-148">Only growing the file is currently supported.</span></span> <span data-ttu-id="20163-149">Чтобы сжать файл, используйте функцию дефрагментации служебной программы esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="20163-149">To shrink a file, use the defragmentation feature of the esentutl.exe utility program.</span></span>

<span data-ttu-id="20163-150">Если *CPG* меньше текущего размера базы данных, операция будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="20163-150">If *cpg* is smaller than the current size of the database, the operation will be ignored.</span></span> <span data-ttu-id="20163-151">Если *CPG* меньше, чем минимальный размер базы данных (в настоящее время 256 страниц), он возвратит JET_errInvalidParameter.</span><span class="sxs-lookup"><span data-stu-id="20163-151">If *cpg* is less than the minimum database size (currently 256 pages), it will return JET_errInvalidParameter.</span></span>

<span data-ttu-id="20163-152">Чтобы задать размер открытой базы данных, см. раздел [жетгровдатабасе](./jetgrowdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="20163-152">To set the size of a database that is opened, see [JetGrowDatabase](./jetgrowdatabase-function.md).</span></span>

<span data-ttu-id="20163-153">Размер файла может не совпадать с количеством страниц, возвращаемых в *пкпгреал*.</span><span class="sxs-lookup"><span data-stu-id="20163-153">The file size may not match the number of pages returned in *pcpgReal*.</span></span> <span data-ttu-id="20163-154">Существует два дополнительных зарезервированных страницы, которые не могут быть учтены в *пкпгреал*.</span><span class="sxs-lookup"><span data-stu-id="20163-154">There are two additional reserved pages that may not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="20163-155">Требования</span><span class="sxs-lookup"><span data-stu-id="20163-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20163-156"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="20163-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20163-157">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="20163-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20163-158"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="20163-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20163-159">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="20163-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20163-160"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="20163-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20163-161">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="20163-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20163-162"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="20163-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="20163-163">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="20163-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20163-164"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="20163-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="20163-165">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="20163-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20163-166"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="20163-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="20163-167">Реализуется как <strong>жетсетдатабасесизев</strong> (Юникод) и <strong>жетсетдатабасесизеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="20163-167">Implemented as <strong>JetSetDatabaseSizeW</strong> (Unicode) and <strong>JetSetDatabaseSizeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="20163-168">См. также:</span><span class="sxs-lookup"><span data-stu-id="20163-168">See Also</span></span>

[<span data-ttu-id="20163-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="20163-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="20163-170">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="20163-170">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="20163-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="20163-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="20163-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="20163-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="20163-173">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="20163-173">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="20163-174">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="20163-174">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="20163-175">жетгровдатабасе</span><span class="sxs-lookup"><span data-stu-id="20163-175">JetGrowDatabase</span></span>](./jetgrowdatabase-function.md)
