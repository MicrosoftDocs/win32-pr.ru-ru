---
description: 'Дополнительные сведения: структура JET_OBJECTLIST'
title: Структура JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347515"
---
# <a name="jet_objectlist-structure"></a><span data-ttu-id="9ea50-103">Структура JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="9ea50-103">JET_OBJECTLIST Structure</span></span>


<span data-ttu-id="9ea50-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9ea50-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectlist-structure"></a><span data-ttu-id="9ea50-105">Структура JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="9ea50-105">JET_OBJECTLIST Structure</span></span>

<span data-ttu-id="9ea50-106">Структура **JET_OBJECTLIST** проходит по временной таблице, созданной с помощью [жетжетобжектинфо](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-106">The **JET_OBJECTLIST** structure traverses a temporary table that was created with [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span> <span data-ttu-id="9ea50-107">Каждая строка во временной таблице описывает объект в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9ea50-107">Each row in the temporary table describes an object in the database.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a><span data-ttu-id="9ea50-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="9ea50-108">Members</span></span>

<span data-ttu-id="9ea50-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="9ea50-109">**cbStruct**</span></span>

<span data-ttu-id="9ea50-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="9ea50-110">The size of the structure, in bytes.</span></span> <span data-ttu-id="9ea50-111">Вызов API обновит это поле, поэтому вызывающий должен убедиться, что это значение соответствует sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="9ea50-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="9ea50-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="9ea50-112">**tableid**</span></span>

<span data-ttu-id="9ea50-113">Идентификатор созданной временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="9ea50-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="9ea50-114">Вызывающий объект должен содержать код, который будет закрывать таблицу.</span><span class="sxs-lookup"><span data-stu-id="9ea50-114">The caller must contain code that will close the table.</span></span>

<span data-ttu-id="9ea50-115">**крекорд**</span><span class="sxs-lookup"><span data-stu-id="9ea50-115">**cRecord**</span></span>

<span data-ttu-id="9ea50-116">Количество записей во временной таблице, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="9ea50-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="9ea50-117">**колумнидконтаинернаме**</span><span class="sxs-lookup"><span data-stu-id="9ea50-117">**columnidcontainername**</span></span>

<span data-ttu-id="9ea50-118">Идентификатор столбца имени типа контейнера.</span><span class="sxs-lookup"><span data-stu-id="9ea50-118">The column identifier of the name of the type of container.</span></span>

<span data-ttu-id="9ea50-119">Единственными поддерживаемыми в настоящее время контейнерами являются таблицы.</span><span class="sxs-lookup"><span data-stu-id="9ea50-119">The only containers that are currently supported are tables.</span></span> <span data-ttu-id="9ea50-120">Этот столбец является [JET_coltypTextом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-120">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="9ea50-121">**колумнидобжектнаме**</span><span class="sxs-lookup"><span data-stu-id="9ea50-121">**columnidobjectname**</span></span>

<span data-ttu-id="9ea50-122">Идентификатор столбца имени объекта.</span><span class="sxs-lookup"><span data-stu-id="9ea50-122">The column identifier of the name of the object.</span></span>

<span data-ttu-id="9ea50-123">Этот столбец является [JET_coltypTextом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-123">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="9ea50-124">**колумнидобжтип**</span><span class="sxs-lookup"><span data-stu-id="9ea50-124">**columnidobjtyp**</span></span>

<span data-ttu-id="9ea50-125">Идентификатор столбца типа объекта.</span><span class="sxs-lookup"><span data-stu-id="9ea50-125">The column identifier of the type of the object.</span></span> <span data-ttu-id="9ea50-126">Единственными поддерживаемыми в настоящее время контейнерами являются таблицы, поэтому это поле будет JET_objtypTable.</span><span class="sxs-lookup"><span data-stu-id="9ea50-126">The only containers that are currently supported are tables, so this field will be JET_objtypTable.</span></span>

<span data-ttu-id="9ea50-127">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-127">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9ea50-128">**колумниддткреате**</span><span class="sxs-lookup"><span data-stu-id="9ea50-128">**columniddtCreate**</span></span>

<span data-ttu-id="9ea50-129">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="9ea50-129">Obsolete.</span></span> <span data-ttu-id="9ea50-130">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="9ea50-130">Do not use.</span></span>

<span data-ttu-id="9ea50-131">**колумниддтупдате**</span><span class="sxs-lookup"><span data-stu-id="9ea50-131">**columniddtUpdate**</span></span>

<span data-ttu-id="9ea50-132">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="9ea50-132">Obsolete.</span></span> <span data-ttu-id="9ea50-133">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="9ea50-133">Do not use.</span></span>

<span data-ttu-id="9ea50-134">**колумнидгрбит**</span><span class="sxs-lookup"><span data-stu-id="9ea50-134">**columnidgrbit**</span></span>

<span data-ttu-id="9ea50-135">Идентификатор столбца **грбитс** , который применим к объекту.</span><span class="sxs-lookup"><span data-stu-id="9ea50-135">The column identifier of the **grbits** that are applicable to the object.</span></span> <span data-ttu-id="9ea50-136">Список применимых **грбитс** см. в разделе [JET_TABLECREATE](./jet-tablecreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-136">For a list of applicable **grbits**, see [JET_TABLECREATE](./jet-tablecreate-structure.md).</span></span>

<span data-ttu-id="9ea50-137">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-137">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9ea50-138">**колумнидфлагс**</span><span class="sxs-lookup"><span data-stu-id="9ea50-138">**columnidflags**</span></span>

<span data-ttu-id="9ea50-139">Идентификатор столбца флагов, применимых к объекту.</span><span class="sxs-lookup"><span data-stu-id="9ea50-139">The column identifier of the flags that are applicable to the object.</span></span> <span data-ttu-id="9ea50-140">Список применимых флагов см. в разделе [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-140">For a list of applicable flags, see [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span></span>

<span data-ttu-id="9ea50-141">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-141">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9ea50-142">**колумнидкрекорд**</span><span class="sxs-lookup"><span data-stu-id="9ea50-142">**columnidcRecord**</span></span>

<span data-ttu-id="9ea50-143">Идентификатор столбца количества записей, имеющихся в таблице с именем в **колумнидобжектнаме**.</span><span class="sxs-lookup"><span data-stu-id="9ea50-143">The column identifier of the number of records that are present in the table that is named in **columnidobjectname**.</span></span>

<span data-ttu-id="9ea50-144">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-144">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9ea50-145">**колумнидкпаже**</span><span class="sxs-lookup"><span data-stu-id="9ea50-145">**columnidcPage**</span></span>

<span data-ttu-id="9ea50-146">Идентификатор столбца числа страниц, используемых объектом.</span><span class="sxs-lookup"><span data-stu-id="9ea50-146">The column identifier of the number of pages the object uses.</span></span>

<span data-ttu-id="9ea50-147">Этот столбец является [JET_coltypLongом](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9ea50-147">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="9ea50-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ea50-148">Remarks</span></span>

<span data-ttu-id="9ea50-149">Каждая строка во временной таблице соответствует объекту в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9ea50-149">Each row in the temporary table corresponds to an object in the database.</span></span>

<span data-ttu-id="9ea50-150">При создании временной таблицы с параметром *инфолевел* в функции [жетжетобжектинфо](./jetgetobjectinfo-function.md) , для которой задано значение JET_ObjInfoListNoStats, столбцы, идентифицируемые **колумнидкрекорд** и **колумнидкпаже** , не будут содержать осмысленной информации.</span><span class="sxs-lookup"><span data-stu-id="9ea50-150">When the temporary table is created with the *InfoLevel* parameter in the [JetGetObjectInfo](./jetgetobjectinfo-function.md) function set to JET_ObjInfoListNoStats, the columns identified by **columnidcRecord** and **columnidcPage** will not contain meaningful information.</span></span>

<span data-ttu-id="9ea50-151">Сейчас в временной таблице будут только сведения о таблицах.</span><span class="sxs-lookup"><span data-stu-id="9ea50-151">Currently, only information about tables will be in the temporary table.</span></span>

### <a name="requirements"></a><span data-ttu-id="9ea50-152">Требования</span><span class="sxs-lookup"><span data-stu-id="9ea50-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ea50-153"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9ea50-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9ea50-154">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9ea50-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ea50-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9ea50-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9ea50-156">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9ea50-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ea50-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9ea50-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9ea50-158">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9ea50-158">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9ea50-159">См. также:</span><span class="sxs-lookup"><span data-stu-id="9ea50-159">See Also</span></span>

[<span data-ttu-id="9ea50-160">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="9ea50-160">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="9ea50-161">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9ea50-161">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="9ea50-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9ea50-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9ea50-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9ea50-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9ea50-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9ea50-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9ea50-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9ea50-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9ea50-166">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="9ea50-166">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="9ea50-167">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="9ea50-167">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="9ea50-168">жетжетобжектинфо</span><span class="sxs-lookup"><span data-stu-id="9ea50-168">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)
