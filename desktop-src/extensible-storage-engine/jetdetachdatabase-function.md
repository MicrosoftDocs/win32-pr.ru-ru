---
description: Дополнительные сведения о функции Жетдетачдатабасе
title: Функция JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349925"
---
# <a name="jetdetachdatabase-function"></a><span data-ttu-id="c2584-103">Функция JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="c2584-103">JetDetachDatabase Function</span></span>


<span data-ttu-id="c2584-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c2584-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase-function"></a><span data-ttu-id="c2584-105">Функция JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="c2584-105">JetDetachDatabase Function</span></span>

<span data-ttu-id="c2584-106">Функция **жетдетачдатабасе** освобождает файл базы данных, который ранее был присоединен к сеансу базы данных.</span><span class="sxs-lookup"><span data-stu-id="c2584-106">The **JetDetachDatabase** function releases a database file that was previously attached to a database session.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a><span data-ttu-id="c2584-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2584-107">Parameters</span></span>

<span data-ttu-id="c2584-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="c2584-108">*sesid*</span></span>

<span data-ttu-id="c2584-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="c2584-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="c2584-110">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="c2584-110">*szFilename*</span></span>

<span data-ttu-id="c2584-111">Имя базы данных для отсоединения.</span><span class="sxs-lookup"><span data-stu-id="c2584-111">The name of the database to detach.</span></span> <span data-ttu-id="c2584-112">Если *сзфиленаме* имеет **значение NULL** или является пустой строкой, все базы данных, прикрепленные к *сесид* , будут отсоединены.</span><span class="sxs-lookup"><span data-stu-id="c2584-112">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

### <a name="return-value"></a><span data-ttu-id="c2584-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2584-113">Return Value</span></span>

<span data-ttu-id="c2584-114">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="c2584-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c2584-115">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c2584-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2584-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c2584-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="c2584-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c2584-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2584-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c2584-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c2584-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c2584-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2584-120">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="c2584-120">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="c2584-121">База данных архивируется и не может быть отсоединена.</span><span class="sxs-lookup"><span data-stu-id="c2584-121">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2584-122">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="c2584-122">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="c2584-123">База данных открыта с помощью <a href="gg269299(v=exchg.10).md">жетопендатабасе</a>.</span><span class="sxs-lookup"><span data-stu-id="c2584-123">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="c2584-124">Перед отсоединением базы данных должны быть закрыты.</span><span class="sxs-lookup"><span data-stu-id="c2584-124">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2584-125">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="c2584-125">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="c2584-126">База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a> или <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="c2584-126">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2584-127">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="c2584-127">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="c2584-128">Предпринята попытка отсоединить базу данных во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="c2584-128">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="c2584-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2584-129">Remarks</span></span>

<span data-ttu-id="c2584-130">Если присоединенная база данных была открыта (с [жетаттачдатабасе](./jetattachdatabase-function.md)), ее необходимо закрыть с помощью [жетклоседатабасе](./jetclosedatabase-function.md) перед отсоединением.</span><span class="sxs-lookup"><span data-stu-id="c2584-130">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="c2584-131">Только Windows 2000. базы данных, которые не были отсоединены до вызова [жеттерм](./jetterm-function.md) , будут автоматически присоединены при следующем вызове [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c2584-131">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c2584-132">Требования</span><span class="sxs-lookup"><span data-stu-id="c2584-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2584-133"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c2584-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c2584-134">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c2584-134">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2584-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c2584-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c2584-136">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c2584-136">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2584-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c2584-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c2584-138">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c2584-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2584-139"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="c2584-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c2584-140">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c2584-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2584-141"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="c2584-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c2584-142">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c2584-142">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2584-143"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="c2584-143"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c2584-144">Реализуется как <strong>жетдетачдатабасев</strong> (Юникод) и <strong>жетдетачдатабасеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c2584-144">Implemented as <strong>JetDetachDatabaseW</strong> (Unicode) and <strong>JetDetachDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c2584-145">См. также:</span><span class="sxs-lookup"><span data-stu-id="c2584-145">See Also</span></span>

[<span data-ttu-id="c2584-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c2584-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c2584-147">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c2584-147">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c2584-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c2584-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c2584-149">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c2584-149">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c2584-150">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="c2584-150">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="c2584-151">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="c2584-151">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="c2584-152">жеткреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="c2584-152">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="c2584-153">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="c2584-153">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="c2584-154">жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="c2584-154">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="c2584-155">жеттерм</span><span class="sxs-lookup"><span data-stu-id="c2584-155">JetTerm</span></span>](./jetterm-function.md)
