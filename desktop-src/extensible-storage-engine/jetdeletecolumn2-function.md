---
description: Дополнительные сведения о функции JetDeleteColumn2
title: Функция JetDeleteColumn2
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713142"
---
# <a name="jetdeletecolumn2-function"></a><span data-ttu-id="7d70d-103">Функция JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="7d70d-103">JetDeleteColumn2 Function</span></span>


<span data-ttu-id="7d70d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7d70d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn2-function"></a><span data-ttu-id="7d70d-105">Функция JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="7d70d-105">JetDeleteColumn2 Function</span></span>

<span data-ttu-id="7d70d-106">Функция **JetDeleteColumn2** удаляет столбец из таблицы базы данных ESE и позволяет установить параметр *грбит* .</span><span class="sxs-lookup"><span data-stu-id="7d70d-106">The **JetDeleteColumn2** function deletes a column from an ESE database table and enables a *grbit* option to be set.</span></span>

<span data-ttu-id="7d70d-107">**Windows XP: JetDeleteColumn2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7d70d-107">**Windows XP:  JetDeleteColumn2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7d70d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d70d-108">Parameters</span></span>

<span data-ttu-id="7d70d-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="7d70d-109">*sesid*</span></span>

<span data-ttu-id="7d70d-110">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="7d70d-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="7d70d-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="7d70d-111">*tableid*</span></span>

<span data-ttu-id="7d70d-112">Таблица, содержащая удаляемый столбец.</span><span class="sxs-lookup"><span data-stu-id="7d70d-112">The table that contains the column to be deleted.</span></span>

<span data-ttu-id="7d70d-113">*сзколумннаме*</span><span class="sxs-lookup"><span data-stu-id="7d70d-113">*szColumnName*</span></span>

<span data-ttu-id="7d70d-114">Имя удаляемого столбца.</span><span class="sxs-lookup"><span data-stu-id="7d70d-114">The name of the column to be deleted.</span></span>

<span data-ttu-id="7d70d-115">*грбит*</span><span class="sxs-lookup"><span data-stu-id="7d70d-115">*grbit*</span></span>

<span data-ttu-id="7d70d-116">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="7d70d-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d70d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7d70d-117">Value</span></span></p></th>
<th><p><span data-ttu-id="7d70d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7d70d-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d70d-119">JET_bitDeleteColumnIgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="7d70d-119">JET_bitDeleteColumnIgnoreTemplateColumns</span></span></p></td>
<td><p><span data-ttu-id="7d70d-120">Установка JET_bitDeleteColumIgnoreTemplateColumns приведет к тому, что API будет пытаться только удалить столбцы в производной таблице.</span><span class="sxs-lookup"><span data-stu-id="7d70d-120">Setting JET_bitDeleteColumIgnoreTemplateColumns will cause the API to only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="7d70d-121">Если столбец с таким именем существует в базовой таблице, он будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="7d70d-121">If a column of that name exists in the base table it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7d70d-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d70d-122">Return Value</span></span>

<span data-ttu-id="7d70d-123">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="7d70d-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7d70d-124">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7d70d-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d70d-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7d70d-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="7d70d-126">Описание</span><span class="sxs-lookup"><span data-stu-id="7d70d-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d70d-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7d70d-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7d70d-128">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7d70d-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d70d-129">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="7d70d-129">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="7d70d-130">Столбец используется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="7d70d-130">The column is currently in use.</span></span> <span data-ttu-id="7d70d-131">В настоящее время он может использоваться индексом.</span><span class="sxs-lookup"><span data-stu-id="7d70d-131">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d70d-132">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="7d70d-132">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="7d70d-133">Предпринята попытка изменить фиксированный DDL.</span><span class="sxs-lookup"><span data-stu-id="7d70d-133">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d70d-134">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="7d70d-134">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="7d70d-135">Столбец с именем в <em>сзколумннаме</em> существует в таблице шаблонов, а DDL таблицы шаблона изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="7d70d-135">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d70d-136">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="7d70d-136">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="7d70d-137">Это может быть возвращено, если было задано неправильное имя <em>сзколумннаме</em> .</span><span class="sxs-lookup"><span data-stu-id="7d70d-137">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d70d-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="7d70d-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="7d70d-139">Таблица недоступна для записи.</span><span class="sxs-lookup"><span data-stu-id="7d70d-139">The table is not writable.</span></span> <span data-ttu-id="7d70d-140">Это может возвращаться, если база данных была открыта в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7d70d-140">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d70d-141">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="7d70d-141">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="7d70d-142">Транзакция является транзакцией только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7d70d-142">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="7d70d-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d70d-143">Remarks</span></span>

<span data-ttu-id="7d70d-144">Вызов [жетделетеколумн](./jetdeletecolumn-function.md) идентичен вызову **JetDeleteColumn2** с параметром *грбит* , равным нулю (0).</span><span class="sxs-lookup"><span data-stu-id="7d70d-144">Calling [JetDeleteColumn](./jetdeletecolumn-function.md) is identical to calling **JetDeleteColumn2** with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="7d70d-145">Требования</span><span class="sxs-lookup"><span data-stu-id="7d70d-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d70d-146"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="7d70d-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7d70d-147">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7d70d-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d70d-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7d70d-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7d70d-149">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7d70d-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d70d-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7d70d-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7d70d-151">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7d70d-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d70d-152"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="7d70d-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7d70d-153">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7d70d-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d70d-154"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="7d70d-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7d70d-155">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7d70d-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d70d-156"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="7d70d-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7d70d-157">Реализуется как <strong>JetDeleteColumn2W</strong> (Юникод) и <strong>JetDeleteColumn2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7d70d-157">Implemented as <strong>JetDeleteColumn2W</strong> (Unicode) and <strong>JetDeleteColumn2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7d70d-158">См. также:</span><span class="sxs-lookup"><span data-stu-id="7d70d-158">See Also</span></span>

[<span data-ttu-id="7d70d-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7d70d-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7d70d-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7d70d-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7d70d-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7d70d-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7d70d-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7d70d-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7d70d-163">жетделетеколумн</span><span class="sxs-lookup"><span data-stu-id="7d70d-163">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)
