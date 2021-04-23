---
description: Дополнительные сведения о функции Жетресизедатабасе
title: Функция Жетресизедатабасе
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703279"
---
# <a name="jetresizedatabase-function"></a><span data-ttu-id="c4d07-103">Функция Жетресизедатабасе</span><span class="sxs-lookup"><span data-stu-id="c4d07-103">JetResizeDatabase Function</span></span>


<span data-ttu-id="c4d07-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c4d07-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="c4d07-105">Функция **жетресизедатабасе** расширяет или сжимает размер открытой в данный момент базы данных.</span><span class="sxs-lookup"><span data-stu-id="c4d07-105">The **JetResizeDatabase** function extends or shrinks the size of a database that is currently open.</span></span>

<span data-ttu-id="c4d07-106">Функция **жетресизедатабасе** была введена в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c4d07-106">The **JetResizeDatabase** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="c4d07-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4d07-107">Parameters</span></span>

<span data-ttu-id="c4d07-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="c4d07-108">*sesid*</span></span>

<span data-ttu-id="c4d07-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="c4d07-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="c4d07-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="c4d07-110">*dbid*</span></span>

<span data-ttu-id="c4d07-111">База данных, которая будет расширена.</span><span class="sxs-lookup"><span data-stu-id="c4d07-111">The database that will be extended.</span></span>

<span data-ttu-id="c4d07-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="c4d07-112">*cpg*</span></span>

<span data-ttu-id="c4d07-113">Запрошенный размер базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="c4d07-113">The requested size of the database, in pages.</span></span>

<span data-ttu-id="c4d07-114">*пкпгактуал*</span><span class="sxs-lookup"><span data-stu-id="c4d07-114">*pcpgActual*</span></span>

<span data-ttu-id="c4d07-115">Указатель на число, которое получает размер базы данных на страницах после вызова API.</span><span class="sxs-lookup"><span data-stu-id="c4d07-115">A pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="c4d07-116">В случае сбоя вызова API содержимое параметра *пкпгактуал* не определено.</span><span class="sxs-lookup"><span data-stu-id="c4d07-116">If the API call fails, the contents of *pcpgActual* parameter are undefined.</span></span>

<span data-ttu-id="c4d07-117">*грбит*</span><span class="sxs-lookup"><span data-stu-id="c4d07-117">*grbit*</span></span>

<span data-ttu-id="c4d07-118">Группа битов, которая указывает ноль или более значений, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c4d07-118">A group of bits that specifies zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4d07-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c4d07-119">Value</span></span></p></th>
<th><p><span data-ttu-id="c4d07-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c4d07-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4d07-121">JET_bitResizeDatabaseOnlyGrow</span><span class="sxs-lookup"><span data-stu-id="c4d07-121">JET_bitResizeDatabaseOnlyGrow</span></span></p></td>
<td><p><span data-ttu-id="c4d07-122">Увеличивать только базу данных.</span><span class="sxs-lookup"><span data-stu-id="c4d07-122">Only grow the database.</span></span> <span data-ttu-id="c4d07-123">Если при вызове изменения размера база данных будет сжата, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="c4d07-123">If the resize call would shrink the database, do nothing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c4d07-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4d07-124">Return value</span></span>

<span data-ttu-id="c4d07-125">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c4d07-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="c4d07-126">Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c4d07-126">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4d07-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c4d07-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="c4d07-128">Описание</span><span class="sxs-lookup"><span data-stu-id="c4d07-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4d07-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c4d07-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c4d07-130">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c4d07-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4d07-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="c4d07-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="c4d07-132">Недостаточно свободного места на томе для выполнения операции увеличения.</span><span class="sxs-lookup"><span data-stu-id="c4d07-132">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4d07-133">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="c4d07-133">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="c4d07-134">Функция <a href="gg269242(v=exchg.10).md">жетсетдатабасесизе</a> вернула ошибку, связанную с файлом.</span><span class="sxs-lookup"><span data-stu-id="c4d07-134">A file-related error was returned by the <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> function.</span></span> <span data-ttu-id="c4d07-135">Дополнительные сведения о других ошибках, связанных с файлами, которые могут быть возвращены, см. в разделе <a href="gg269242(v=exchg.10).md">жетсетдатабасесизе</a>.</span><span class="sxs-lookup"><span data-stu-id="c4d07-135">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="c4d07-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4d07-136">Remarks</span></span>

<span data-ttu-id="c4d07-137">Если функция **жетресизедатабасе** вызывается до вставки больших объемов данных, файл базы данных будет увеличен за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="c4d07-137">If the **JetResizeDatabase** function is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="c4d07-138">Это снизит вероятность того, что файл базы данных станет фрагментированным на уровне файловой системы, а также сократит число попыток увеличения размера файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="c4d07-138">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="c4d07-139">Увеличение файла базы данных выполняется один раз быстрее, чем в несколько раз.</span><span class="sxs-lookup"><span data-stu-id="c4d07-139">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="c4d07-140">Сведения о том, как задать размер открытой базы данных, см. в разделе [жетсетдатабасесизе](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4d07-140">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="c4d07-141">Размер файла может не совпадать с количеством страниц, возвращаемых в параметре *пкпгреал* .</span><span class="sxs-lookup"><span data-stu-id="c4d07-141">The file size might not match the number of pages that are returned in the *pcpgReal* parameter.</span></span> <span data-ttu-id="c4d07-142">В параметре *пкпгреал* могут не учитываться две дополнительные зарезервированные страницы.</span><span class="sxs-lookup"><span data-stu-id="c4d07-142">Two additional reserved pages might not be counted in the *pcpgReal* parameter.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c4d07-143">Требования</span><span class="sxs-lookup"><span data-stu-id="c4d07-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4d07-144"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c4d07-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d07-145">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c4d07-145">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4d07-146"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c4d07-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d07-147">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c4d07-147">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4d07-148"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c4d07-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d07-149">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c4d07-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4d07-150"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="c4d07-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d07-151">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c4d07-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4d07-152"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="c4d07-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d07-153">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c4d07-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c4d07-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4d07-154">See also</span></span>

[<span data-ttu-id="c4d07-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c4d07-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c4d07-156">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c4d07-156">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c4d07-157">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c4d07-157">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c4d07-158">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c4d07-158">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c4d07-159">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="c4d07-159">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="c4d07-160">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="c4d07-160">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="c4d07-161">жетсетдатабасесизе</span><span class="sxs-lookup"><span data-stu-id="c4d07-161">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
