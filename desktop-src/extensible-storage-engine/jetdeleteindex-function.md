---
description: Дополнительные сведения о функции Жетделетеиндекс
title: Функция Жетделетеиндекс
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693730"
---
# <a name="jetdeleteindex-function"></a><span data-ttu-id="aaadb-103">Функция Жетделетеиндекс</span><span class="sxs-lookup"><span data-stu-id="aaadb-103">JetDeleteIndex Function</span></span>


<span data-ttu-id="aaadb-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="aaadb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeleteindex-function"></a><span data-ttu-id="aaadb-105">Функция Жетделетеиндекс</span><span class="sxs-lookup"><span data-stu-id="aaadb-105">JetDeleteIndex Function</span></span>

<span data-ttu-id="aaadb-106">Функция **жетделетеиндекс** Удаляет индекс из таблицы.</span><span class="sxs-lookup"><span data-stu-id="aaadb-106">The **JetDeleteIndex** function deletes an index from a table.</span></span>

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="aaadb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aaadb-107">Parameters</span></span>

<span data-ttu-id="aaadb-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="aaadb-108">*sesid*</span></span>

<span data-ttu-id="aaadb-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="aaadb-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="aaadb-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="aaadb-110">*tableid*</span></span>

<span data-ttu-id="aaadb-111">Таблица, содержащая удаляемый столбец.</span><span class="sxs-lookup"><span data-stu-id="aaadb-111">The table that contains the column that is to be deleted.</span></span>

<span data-ttu-id="aaadb-112">*сзиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="aaadb-112">*szIndexName*</span></span>

<span data-ttu-id="aaadb-113">Имя удаляемого индекса.</span><span class="sxs-lookup"><span data-stu-id="aaadb-113">The name of the index to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="aaadb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aaadb-114">Return Value</span></span>

<span data-ttu-id="aaadb-115">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="aaadb-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="aaadb-116">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="aaadb-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aaadb-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="aaadb-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="aaadb-118">Описание</span><span class="sxs-lookup"><span data-stu-id="aaadb-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aaadb-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="aaadb-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="aaadb-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aaadb-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaadb-121">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="aaadb-121">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="aaadb-122">Предпринята попытка удалить индекс из фиксированной таблицы (например, созданной с помощью JET_bitTableCreateFixedDDL).</span><span class="sxs-lookup"><span data-stu-id="aaadb-122">An attempt was made to delete an index from a fixed table (for example, one created with JET_bitTableCreateFixedDDL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaadb-123">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="aaadb-123">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="aaadb-124">Предпринята попытка удалить индекс из таблицы шаблонов.</span><span class="sxs-lookup"><span data-stu-id="aaadb-124">An attempt was made to delete an index from a template table.</span></span> <span data-ttu-id="aaadb-125">Таблица шаблонов имеет фиксированное значение DDL.</span><span class="sxs-lookup"><span data-stu-id="aaadb-125">A template table has fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaadb-126">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="aaadb-126">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="aaadb-127">Индекс с именем в <em>сзиндекснаме</em> не найден.</span><span class="sxs-lookup"><span data-stu-id="aaadb-127">The index named in <em>szIndexName</em> was not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaadb-128">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="aaadb-128">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="aaadb-129">Невозможно обновить таблицу, так как она была открыта только для чтения.</span><span class="sxs-lookup"><span data-stu-id="aaadb-129">The table cannot be updated because it was opened read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaadb-130">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="aaadb-130">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="aaadb-131">Несколько потоков попытались использовать один сеанс базы данных.</span><span class="sxs-lookup"><span data-stu-id="aaadb-131">Multiple threads attempted to use the same database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaadb-132">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="aaadb-132">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="aaadb-133">Транзакция была открыта как транзакция только для чтения.</span><span class="sxs-lookup"><span data-stu-id="aaadb-133">The transaction was opened as a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="aaadb-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aaadb-134">Remarks</span></span>

<span data-ttu-id="aaadb-135">При успешном выполнении индекс удаляется, поэтому его нельзя использовать в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="aaadb-135">When successful, the index is deleted and therefore cannot be used subsequently.</span></span> <span data-ttu-id="aaadb-136">При использовании индекса не должно быть активной транзакции.</span><span class="sxs-lookup"><span data-stu-id="aaadb-136">There must not be any active transaction using the index.</span></span>

<span data-ttu-id="aaadb-137">В случае успеха Валюта задается перед первой записью.</span><span class="sxs-lookup"><span data-stu-id="aaadb-137">On success, the currency is set before the first record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="aaadb-138">Требования</span><span class="sxs-lookup"><span data-stu-id="aaadb-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aaadb-139"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="aaadb-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aaadb-140">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="aaadb-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaadb-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="aaadb-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aaadb-142">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="aaadb-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaadb-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="aaadb-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aaadb-144">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="aaadb-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaadb-145"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="aaadb-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="aaadb-146">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="aaadb-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaadb-147"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="aaadb-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="aaadb-148">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="aaadb-148">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaadb-149"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="aaadb-149"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="aaadb-150">Реализуется как <strong>жетделетеиндексв</strong> (Юникод) и <strong>жетделетеиндекса</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="aaadb-150">Implemented as <strong>JetDeleteIndexW</strong> (Unicode) and <strong>JetDeleteIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="aaadb-151">См. также:</span><span class="sxs-lookup"><span data-stu-id="aaadb-151">See Also</span></span>

[<span data-ttu-id="aaadb-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="aaadb-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="aaadb-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="aaadb-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="aaadb-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="aaadb-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="aaadb-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="aaadb-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="aaadb-156">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="aaadb-156">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="aaadb-157">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="aaadb-157">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)
