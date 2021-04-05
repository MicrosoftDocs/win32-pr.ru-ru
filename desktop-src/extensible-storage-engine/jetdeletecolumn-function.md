---
description: Дополнительные сведения о функции Жетделетеколумн
title: Функция Жетделетеколумн
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104000537"
---
# <a name="jetdeletecolumn-function"></a><span data-ttu-id="b27a5-103">Функция Жетделетеколумн</span><span class="sxs-lookup"><span data-stu-id="b27a5-103">JetDeleteColumn Function</span></span>


<span data-ttu-id="b27a5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b27a5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn-function"></a><span data-ttu-id="b27a5-105">Функция Жетделетеколумн</span><span class="sxs-lookup"><span data-stu-id="b27a5-105">JetDeleteColumn Function</span></span>

<span data-ttu-id="b27a5-106">Функция **жетделетеколумн** удаляет столбец из таблицы базы данных ESE.</span><span class="sxs-lookup"><span data-stu-id="b27a5-106">The **JetDeleteColumn** function deletes a column from an ESE database table.</span></span>

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a><span data-ttu-id="b27a5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b27a5-107">Parameters</span></span>

<span data-ttu-id="b27a5-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="b27a5-108">*sesid*</span></span>

<span data-ttu-id="b27a5-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="b27a5-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="b27a5-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b27a5-110">*tableid*</span></span>

<span data-ttu-id="b27a5-111">Таблица, из которой необходимо удалить столбец.</span><span class="sxs-lookup"><span data-stu-id="b27a5-111">The table from which to delete the column.</span></span>

<span data-ttu-id="b27a5-112">*сзколумннаме*</span><span class="sxs-lookup"><span data-stu-id="b27a5-112">*szColumnName*</span></span>

<span data-ttu-id="b27a5-113">Имя удаляемого столбца.</span><span class="sxs-lookup"><span data-stu-id="b27a5-113">The name of the column to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="b27a5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b27a5-114">Return Value</span></span>

<span data-ttu-id="b27a5-115">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="b27a5-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b27a5-116">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b27a5-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b27a5-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b27a5-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="b27a5-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b27a5-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b27a5-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b27a5-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b27a5-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b27a5-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27a5-121">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="b27a5-121">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="b27a5-122">Столбец используется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="b27a5-122">The column is currently in use.</span></span> <span data-ttu-id="b27a5-123">В настоящее время он может использоваться индексом.</span><span class="sxs-lookup"><span data-stu-id="b27a5-123">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27a5-124">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="b27a5-124">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="b27a5-125">Предпринята попытка изменить фиксированный DDL.</span><span class="sxs-lookup"><span data-stu-id="b27a5-125">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27a5-126">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="b27a5-126">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="b27a5-127">Столбец с именем в <em>сзколумннаме</em> существует в таблице шаблонов, а DDL таблицы шаблона изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="b27a5-127">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27a5-128">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="b27a5-128">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="b27a5-129">Это может быть возвращено, если было задано неправильное имя <em>сзколумннаме</em> .</span><span class="sxs-lookup"><span data-stu-id="b27a5-129">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27a5-130">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="b27a5-130">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="b27a5-131">Таблица недоступна для записи.</span><span class="sxs-lookup"><span data-stu-id="b27a5-131">The table is not writable.</span></span> <span data-ttu-id="b27a5-132">Это может возвращаться, если база данных была открыта в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b27a5-132">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27a5-133">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="b27a5-133">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="b27a5-134">Транзакция является транзакцией только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b27a5-134">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b27a5-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b27a5-135">Remarks</span></span>

<span data-ttu-id="b27a5-136">Вызов **жетделетеколумн** идентичен вызову [JetDeleteColumn2](./jetdeletecolumn2-function.md) с параметром *грбит* , равным нулю (0).</span><span class="sxs-lookup"><span data-stu-id="b27a5-136">Calling **JetDeleteColumn** is identical to calling [JetDeleteColumn2](./jetdeletecolumn2-function.md) with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="b27a5-137">Требования</span><span class="sxs-lookup"><span data-stu-id="b27a5-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b27a5-138"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="b27a5-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b27a5-139">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b27a5-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27a5-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b27a5-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b27a5-141">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b27a5-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27a5-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b27a5-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b27a5-143">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b27a5-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27a5-144"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="b27a5-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b27a5-145">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b27a5-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27a5-146"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="b27a5-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b27a5-147">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b27a5-147">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27a5-148"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="b27a5-148"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b27a5-149">Реализуется как <strong>жетделетеколумнв</strong> (Юникод) и <strong>жетделетеколумна</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b27a5-149">Implemented as <strong>JetDeleteColumnW</strong> (Unicode) and <strong>JetDeleteColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b27a5-150">См. также:</span><span class="sxs-lookup"><span data-stu-id="b27a5-150">See Also</span></span>

[<span data-ttu-id="b27a5-151">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b27a5-151">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b27a5-152">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b27a5-152">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b27a5-153">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b27a5-153">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b27a5-154">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b27a5-154">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b27a5-155">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="b27a5-155">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
