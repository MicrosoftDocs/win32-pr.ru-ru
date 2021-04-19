---
description: Дополнительные сведения о функции JetDetachDatabase2
title: Функция JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693350"
---
# <a name="jetdetachdatabase2-function"></a><span data-ttu-id="db7fe-103">Функция JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="db7fe-103">JetDetachDatabase2 Function</span></span>


<span data-ttu-id="db7fe-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="db7fe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase2-function"></a><span data-ttu-id="db7fe-105">Функция JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="db7fe-105">JetDetachDatabase2 Function</span></span>

<span data-ttu-id="db7fe-106">Функция **JetDetachDatabase2** освобождает файл базы данных, который ранее был присоединен к сеансу базы данных.</span><span class="sxs-lookup"><span data-stu-id="db7fe-106">The **JetDetachDatabase2** function releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="db7fe-107">**Windows XP:**  **JetDetachDatabase2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db7fe-107">**Windows XP:**  **JetDetachDatabase2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="db7fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="db7fe-108">Parameters</span></span>

<span data-ttu-id="db7fe-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="db7fe-109">*sesid*</span></span>

<span data-ttu-id="db7fe-110">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="db7fe-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="db7fe-111">*сзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="db7fe-111">*szFilename*</span></span>

<span data-ttu-id="db7fe-112">Имя базы данных для отсоединения.</span><span class="sxs-lookup"><span data-stu-id="db7fe-112">The name of the database to detach.</span></span> <span data-ttu-id="db7fe-113">Если *сзфиленаме* имеет **значение NULL** или является пустой строкой, все базы данных, прикрепленные к *сесид* , будут отсоединены.</span><span class="sxs-lookup"><span data-stu-id="db7fe-113">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

<span data-ttu-id="db7fe-114">*грбит*</span><span class="sxs-lookup"><span data-stu-id="db7fe-114">*grbit*</span></span>

<span data-ttu-id="db7fe-115">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="db7fe-115">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db7fe-116">Значение</span><span class="sxs-lookup"><span data-stu-id="db7fe-116">Value</span></span></p></th>
<th><p><span data-ttu-id="db7fe-117">Значение</span><span class="sxs-lookup"><span data-stu-id="db7fe-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db7fe-118">JET_bitForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="db7fe-118">JET_bitForceCloseAndDetach</span></span></p></td>
<td><p><span data-ttu-id="db7fe-119">Принудительное закрытие и отсоединение базы данных.</span><span class="sxs-lookup"><span data-stu-id="db7fe-119">Forces the database to be closed and detached.</span></span> <span data-ttu-id="db7fe-120">Если JET_bitForceCloseAndDetach не поддерживается, будет возвращено JET_errForceDetachNotAllowed.</span><span class="sxs-lookup"><span data-stu-id="db7fe-120">If JET_bitForceCloseAndDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db7fe-121">JET_bitForceDetach</span><span class="sxs-lookup"><span data-stu-id="db7fe-121">JET_bitForceDetach</span></span></p></td>
<td><p><span data-ttu-id="db7fe-122">Принудительное отключение базы данных.</span><span class="sxs-lookup"><span data-stu-id="db7fe-122">Forces the database to be detached.</span></span> <span data-ttu-id="db7fe-123">Если JET_bitForceDetach не поддерживается, будет возвращено JET_errForceDetachNotAllowed.</span><span class="sxs-lookup"><span data-stu-id="db7fe-123">If JET_bitForceDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="db7fe-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db7fe-124">Return Value</span></span>

<span data-ttu-id="db7fe-125">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="db7fe-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="db7fe-126">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="db7fe-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db7fe-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="db7fe-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="db7fe-128">Описание</span><span class="sxs-lookup"><span data-stu-id="db7fe-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db7fe-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="db7fe-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="db7fe-130">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="db7fe-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db7fe-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="db7fe-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="db7fe-132">База данных архивируется и не может быть отсоединена.</span><span class="sxs-lookup"><span data-stu-id="db7fe-132">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db7fe-133">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="db7fe-133">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="db7fe-134">База данных открыта с помощью <a href="gg269299(v=exchg.10).md">жетопендатабасе</a>.</span><span class="sxs-lookup"><span data-stu-id="db7fe-134">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="db7fe-135">Перед отсоединением базы данных должны быть закрыты.</span><span class="sxs-lookup"><span data-stu-id="db7fe-135">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db7fe-136">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="db7fe-136">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="db7fe-137">База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a> или <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="db7fe-137">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db7fe-138">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="db7fe-138">JET_errForceDetachNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="db7fe-139">JET_bitForceDetach не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="db7fe-139">JET_bitForceDetach is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db7fe-140">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="db7fe-140">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="db7fe-141">Предпринята попытка отсоединить базу данных во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="db7fe-141">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="db7fe-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db7fe-142">Remarks</span></span>

<span data-ttu-id="db7fe-143">Если присоединенная база данных была открыта (с [жетаттачдатабасе](./jetattachdatabase-function.md)), ее необходимо закрыть с помощью [жетклоседатабасе](./jetclosedatabase-function.md) перед отсоединением.</span><span class="sxs-lookup"><span data-stu-id="db7fe-143">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="db7fe-144">Только Windows 2000. базы данных, которые не были отсоединены до вызова [жеттерм](./jetterm-function.md) , будут автоматически присоединены при следующем вызове [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="db7fe-144">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="db7fe-145">Требования</span><span class="sxs-lookup"><span data-stu-id="db7fe-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db7fe-146"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="db7fe-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="db7fe-147">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db7fe-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db7fe-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="db7fe-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="db7fe-149">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="db7fe-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db7fe-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="db7fe-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="db7fe-151">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="db7fe-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db7fe-152"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="db7fe-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="db7fe-153">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="db7fe-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db7fe-154"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="db7fe-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="db7fe-155">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="db7fe-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db7fe-156"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="db7fe-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="db7fe-157">Реализуется как <strong>JetDetachDatabase2W</strong> (Юникод) и <strong>JetDetachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="db7fe-157">Implemented as <strong>JetDetachDatabase2W</strong> (Unicode) and <strong>JetDetachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="db7fe-158">См. также:</span><span class="sxs-lookup"><span data-stu-id="db7fe-158">See Also</span></span>

[<span data-ttu-id="db7fe-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="db7fe-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="db7fe-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="db7fe-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="db7fe-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="db7fe-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="db7fe-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="db7fe-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="db7fe-163">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="db7fe-163">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="db7fe-164">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="db7fe-164">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="db7fe-165">жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="db7fe-165">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="db7fe-166">жеткреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="db7fe-166">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="db7fe-167">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="db7fe-167">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="db7fe-168">жетинит</span><span class="sxs-lookup"><span data-stu-id="db7fe-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="db7fe-169">жетопендатабасе</span><span class="sxs-lookup"><span data-stu-id="db7fe-169">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="db7fe-170">жеттерм</span><span class="sxs-lookup"><span data-stu-id="db7fe-170">JetTerm</span></span>](./jetterm-function.md)
