---
description: 'Дополнительные сведения: структура JET_OBJECTINFO'
title: Структура JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081187"
---
# <a name="jet_objectinfo-structure"></a><span data-ttu-id="1be4f-103">Структура JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="1be4f-103">JET_OBJECTINFO Structure</span></span>


<span data-ttu-id="1be4f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1be4f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectinfo-structure"></a><span data-ttu-id="1be4f-105">Структура JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="1be4f-105">JET_OBJECTINFO Structure</span></span>

<span data-ttu-id="1be4f-106">Структура **JET_OBJECTINFO** содержит сведения об объекте.</span><span class="sxs-lookup"><span data-stu-id="1be4f-106">The **JET_OBJECTINFO** structure holds information about an object.</span></span> <span data-ttu-id="1be4f-107">В настоящее время поддерживаются только таблицы типов объектов.</span><span class="sxs-lookup"><span data-stu-id="1be4f-107">Tables are the only object types that are currently supported.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a><span data-ttu-id="1be4f-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="1be4f-108">Members</span></span>

<span data-ttu-id="1be4f-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="1be4f-109">**cbStruct**</span></span>

<span data-ttu-id="1be4f-110">Размер структуры **JET_OBJECTINFO** в байтах.</span><span class="sxs-lookup"><span data-stu-id="1be4f-110">The size, in bytes, of the **JET_OBJECTINFO** structure.</span></span>

<span data-ttu-id="1be4f-111">**обжтип**</span><span class="sxs-lookup"><span data-stu-id="1be4f-111">**objtyp**</span></span>

<span data-ttu-id="1be4f-112">Содержит [JET_OBJTYP](./jet-objtyp.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="1be4f-112">Holds the [JET_OBJTYP](./jet-objtyp.md) of the structure.</span></span> <span data-ttu-id="1be4f-113">В настоящее время возвращаются только таблицы (то есть JET_objtypTable).</span><span class="sxs-lookup"><span data-stu-id="1be4f-113">Currently only tables will be returned (that is, JET_objtypTable).</span></span>

<span data-ttu-id="1be4f-114">**дткреате**</span><span class="sxs-lookup"><span data-stu-id="1be4f-114">**dtCreate**</span></span>

<span data-ttu-id="1be4f-115">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="1be4f-115">Obsolete.</span></span> <span data-ttu-id="1be4f-116">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="1be4f-116">Do not use.</span></span>

<span data-ttu-id="1be4f-117">**дтупдате**</span><span class="sxs-lookup"><span data-stu-id="1be4f-117">**dtUpdate**</span></span>

<span data-ttu-id="1be4f-118">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="1be4f-118">Obsolete.</span></span> <span data-ttu-id="1be4f-119">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="1be4f-119">Do not use.</span></span>

<span data-ttu-id="1be4f-120">**грбит**</span><span class="sxs-lookup"><span data-stu-id="1be4f-120">**grbit**</span></span>

<span data-ttu-id="1be4f-121">Группа битов, содержащая параметры, доступные для данного вызова, которые включают ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1be4f-121">A group of bits that contain the options that are available for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1be4f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1be4f-122">Value</span></span></p></th>
<th><p><span data-ttu-id="1be4f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1be4f-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be4f-124">JET_bitTableInfoBookmark</span><span class="sxs-lookup"><span data-stu-id="1be4f-124">JET_bitTableInfoBookmark</span></span></p></td>
<td><p><span data-ttu-id="1be4f-125">В таблице могут быть закладки.</span><span class="sxs-lookup"><span data-stu-id="1be4f-125">The table can have bookmarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be4f-126">JET_bitTableInfoRollback</span><span class="sxs-lookup"><span data-stu-id="1be4f-126">JET_bitTableInfoRollback</span></span></p></td>
<td><p><span data-ttu-id="1be4f-127">Можно выполнить откат таблицы.</span><span class="sxs-lookup"><span data-stu-id="1be4f-127">The table can be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be4f-128">JET_bitTableInfoUpdatable</span><span class="sxs-lookup"><span data-stu-id="1be4f-128">JET_bitTableInfoUpdatable</span></span></p></td>
<td><p><span data-ttu-id="1be4f-129">Таблицу можно обновить.</span><span class="sxs-lookup"><span data-stu-id="1be4f-129">The table can be updated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1be4f-130">**flags**</span><span class="sxs-lookup"><span data-stu-id="1be4f-130">**flags**</span></span>

<span data-ttu-id="1be4f-131">Битовое поле, которое содержит ноль или более следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="1be4f-131">A bit field that contains zero or more of the following flags.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1be4f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1be4f-132">Value</span></span></p></th>
<th><p><span data-ttu-id="1be4f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1be4f-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be4f-134">JET_bitObjectSystem</span><span class="sxs-lookup"><span data-stu-id="1be4f-134">JET_bitObjectSystem</span></span></p></td>
<td><p><span data-ttu-id="1be4f-135">Таблица является системной таблицей и предназначена только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="1be4f-135">The table is a System Table and is for internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be4f-136">JET_bitObjectTableDerived</span><span class="sxs-lookup"><span data-stu-id="1be4f-136">JET_bitObjectTableDerived</span></span></p></td>
<td><p><span data-ttu-id="1be4f-137">Таблица, унаследованная на языке DDL из таблицы шаблонов.</span><span class="sxs-lookup"><span data-stu-id="1be4f-137">The table inherited DDL from a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be4f-138">JET_bitObjectTableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="1be4f-138">JET_bitObjectTableFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="1be4f-139">Невозможно изменить DDL для таблицы.</span><span class="sxs-lookup"><span data-stu-id="1be4f-139">The DDL for the table cannot be modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be4f-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="1be4f-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="1be4f-141">Используется в сочетании с JET_bitObjectTableTemplate для запрета фиксированных или переменных столбцов в производных таблицах (чтобы в будущем можно было добавить в шаблон фиксированные или переменные столбцы).</span><span class="sxs-lookup"><span data-stu-id="1be4f-141">Used in conjunction with JET_bitObjectTableTemplate to disallow fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span></p>
<p><span data-ttu-id="1be4f-142"><strong>Windows XP:  </strong> Это значение вводится в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1be4f-142"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be4f-143">JET_bitObjectTableTemplate</span><span class="sxs-lookup"><span data-stu-id="1be4f-143">JET_bitObjectTableTemplate</span></span></p></td>
<td><p><span data-ttu-id="1be4f-144">Таблица является таблицей шаблонов.</span><span class="sxs-lookup"><span data-stu-id="1be4f-144">The table is a template table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1be4f-145">**крекорд**</span><span class="sxs-lookup"><span data-stu-id="1be4f-145">**cRecord**</span></span>

<span data-ttu-id="1be4f-146">Число записей в таблице.</span><span class="sxs-lookup"><span data-stu-id="1be4f-146">The number of records in the table.</span></span>

<span data-ttu-id="1be4f-147">Это значение извлекается, только если **JET_OBJECTINFO** был передан в [жетжетобжектинфо](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="1be4f-147">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

<span data-ttu-id="1be4f-148">**кпаже**</span><span class="sxs-lookup"><span data-stu-id="1be4f-148">**cPage**</span></span>

<span data-ttu-id="1be4f-149">Количество страниц, используемых таблицей.</span><span class="sxs-lookup"><span data-stu-id="1be4f-149">The number of pages that are being used by the table.</span></span>

<span data-ttu-id="1be4f-150">Это значение извлекается, только если **JET_OBJECTINFO** был передан в [жетжетобжектинфо](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="1be4f-150">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="1be4f-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1be4f-151">Remarks</span></span>

<span data-ttu-id="1be4f-152">Структура **JET_OBJECTINFO** заполняется вызовом [жетжетобжектинфо](./jetgetobjectinfo-function.md) или [жетжеттаблеинфо](./jetgettableinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="1be4f-152">A **JET_OBJECTINFO** structure gets populated by a call to [JetGetObjectInfo](./jetgetobjectinfo-function.md) or [JetGetTableInfo](./jetgettableinfo-function.md).</span></span> <span data-ttu-id="1be4f-153">Если вызов API не выполняется, содержимое структуры не определено.</span><span class="sxs-lookup"><span data-stu-id="1be4f-153">If the API call does not succeed, the contents of the structure are undefined.</span></span>

<span data-ttu-id="1be4f-154">Если применимо, статистика таблицы включает количество записей и количество страниц в кластеризованном индексе (то есть индекс, содержащий данные записи).</span><span class="sxs-lookup"><span data-stu-id="1be4f-154">If applicable, the table statistics include the number of records and the number of pages that are in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="1be4f-155">Доступ к статистике индекса осуществляется отдельно по имени с помощью [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="1be4f-155">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="1be4f-156">Требования</span><span class="sxs-lookup"><span data-stu-id="1be4f-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be4f-157"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1be4f-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1be4f-158">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1be4f-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be4f-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1be4f-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1be4f-160">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1be4f-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be4f-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1be4f-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1be4f-162">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1be4f-162">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1be4f-163">См. также:</span><span class="sxs-lookup"><span data-stu-id="1be4f-163">See Also</span></span>

[<span data-ttu-id="1be4f-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1be4f-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1be4f-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1be4f-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1be4f-166">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="1be4f-166">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="1be4f-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1be4f-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1be4f-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1be4f-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1be4f-169">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="1be4f-169">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="1be4f-170">жетжетобжектинфо</span><span class="sxs-lookup"><span data-stu-id="1be4f-170">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="1be4f-171">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="1be4f-171">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="1be4f-172">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="1be4f-172">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
