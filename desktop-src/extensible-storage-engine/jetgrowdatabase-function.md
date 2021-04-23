---
description: Дополнительные сведения о функции Жетгровдатабасе
title: Функция Жетгровдатабасе
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647401"
---
# <a name="jetgrowdatabase-function"></a><span data-ttu-id="65db2-103">Функция Жетгровдатабасе</span><span class="sxs-lookup"><span data-stu-id="65db2-103">JetGrowDatabase Function</span></span>


<span data-ttu-id="65db2-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="65db2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgrowdatabase-function"></a><span data-ttu-id="65db2-105">Функция Жетгровдатабасе</span><span class="sxs-lookup"><span data-stu-id="65db2-105">JetGrowDatabase Function</span></span>

<span data-ttu-id="65db2-106">Функция **жетгровдатабасе** расширяет размер открытой в данный момент базы данных.</span><span class="sxs-lookup"><span data-stu-id="65db2-106">The **JetGrowDatabase** function extends the size of a database that is currently open.</span></span>

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="65db2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="65db2-107">Parameters</span></span>

<span data-ttu-id="65db2-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="65db2-108">*sesid*</span></span>

<span data-ttu-id="65db2-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="65db2-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="65db2-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="65db2-110">*dbid*</span></span>

<span data-ttu-id="65db2-111">База данных, которая будет расширена.</span><span class="sxs-lookup"><span data-stu-id="65db2-111">The database that will be extended.</span></span>

<span data-ttu-id="65db2-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="65db2-112">*cpg*</span></span>

<span data-ttu-id="65db2-113">Требуемый размер базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="65db2-113">The desired size of the database, in pages.</span></span>

<span data-ttu-id="65db2-114">*пкпгреал*</span><span class="sxs-lookup"><span data-stu-id="65db2-114">*pcpgReal*</span></span>

<span data-ttu-id="65db2-115">Указатель на число, которое получает размер базы данных на страницах после вызова API.</span><span class="sxs-lookup"><span data-stu-id="65db2-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="65db2-116">Если вызов API завершается неудачей, содержимое *пкпгреал* не определяется.</span><span class="sxs-lookup"><span data-stu-id="65db2-116">If the API call fails, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="65db2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65db2-117">Return Value</span></span>

<span data-ttu-id="65db2-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="65db2-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="65db2-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="65db2-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65db2-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="65db2-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="65db2-121">Описание</span><span class="sxs-lookup"><span data-stu-id="65db2-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65db2-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="65db2-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="65db2-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="65db2-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65db2-124">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="65db2-124">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="65db2-125">Недостаточно свободного места на томе для выполнения операции увеличения.</span><span class="sxs-lookup"><span data-stu-id="65db2-125">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65db2-126">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="65db2-126">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="65db2-127"><a href="gg269242(v=exchg.10).md">Жетсетдатабасесизе</a>вернул ошибку, связанную с файлом.</span><span class="sxs-lookup"><span data-stu-id="65db2-127">A file-related error was returned by <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span> <span data-ttu-id="65db2-128">Дополнительные сведения о других ошибках, связанных с файлами, которые могут быть возвращены, см. в разделе <a href="gg269242(v=exchg.10).md">жетсетдатабасесизе</a>.</span><span class="sxs-lookup"><span data-stu-id="65db2-128">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="65db2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65db2-129">Remarks</span></span>

<span data-ttu-id="65db2-130">Если **жетгровдатабасе** вызывается до вставки больших объемов данных, то файл базы данных будет увеличен за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="65db2-130">If **JetGrowDatabase** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="65db2-131">Это снизит вероятность того, что файл базы данных станет фрагментированным на уровне файловой системы, а также сократит число попыток увеличения размера файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="65db2-131">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="65db2-132">Увеличение файла базы данных выполняется один раз быстрее, чем в несколько раз.</span><span class="sxs-lookup"><span data-stu-id="65db2-132">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="65db2-133">В настоящее время поддерживается только увеличение размера файла.</span><span class="sxs-lookup"><span data-stu-id="65db2-133">Only growing the file is currently supported.</span></span> <span data-ttu-id="65db2-134">Чтобы сжать файл, используйте функцию дефрагментации служебной программы **esentutl.exe** .</span><span class="sxs-lookup"><span data-stu-id="65db2-134">To shrink a file, use the defragmentation feature of the **esentutl.exe** utility program.</span></span>

<span data-ttu-id="65db2-135">Сведения о том, как задать размер открытой базы данных, см. в разделе [жетсетдатабасесизе](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="65db2-135">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="65db2-136">Размер файла может не совпадать с количеством страниц, возвращаемых в *пкпгреал*.</span><span class="sxs-lookup"><span data-stu-id="65db2-136">The file size might not match the number of pages that are returned in *pcpgReal*.</span></span> <span data-ttu-id="65db2-137">Существует два дополнительных зарезервированных страницы, которые могут не учитываться в *пкпгреал*.</span><span class="sxs-lookup"><span data-stu-id="65db2-137">There are two additional reserved pages that might not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="65db2-138">Требования</span><span class="sxs-lookup"><span data-stu-id="65db2-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65db2-139"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="65db2-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="65db2-140">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="65db2-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65db2-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="65db2-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="65db2-142">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="65db2-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65db2-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="65db2-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="65db2-144">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="65db2-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65db2-145"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="65db2-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="65db2-146">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="65db2-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65db2-147"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="65db2-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="65db2-148">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="65db2-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="65db2-149">См. также:</span><span class="sxs-lookup"><span data-stu-id="65db2-149">See Also</span></span>

[<span data-ttu-id="65db2-150">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="65db2-150">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="65db2-151">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="65db2-151">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="65db2-152">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="65db2-152">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="65db2-153">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="65db2-153">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="65db2-154">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="65db2-154">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="65db2-155">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="65db2-155">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="65db2-156">жетсетдатабасесизе</span><span class="sxs-lookup"><span data-stu-id="65db2-156">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
