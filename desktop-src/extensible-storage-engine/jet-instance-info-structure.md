---
description: 'Дополнительные сведения: структура JET_INSTANCE_INFO'
title: Структура JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
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
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912999"
---
# <a name="jet_instance_info-structure"></a><span data-ttu-id="37e91-103">Структура JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="37e91-103">JET_INSTANCE_INFO Structure</span></span>


<span data-ttu-id="37e91-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="37e91-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance_info-structure"></a><span data-ttu-id="37e91-105">Структура JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="37e91-105">JET_INSTANCE_INFO Structure</span></span>

<span data-ttu-id="37e91-106">Структура **JET_INSTANCE_INFO** получает сведения о выполняемых экземплярах базы данных при использовании с функциями [жетжетинстанцеинфо](./jetgetinstanceinfo-function.md) и [жетосснапшотфризе](./jetossnapshotfreeze-function.md) .</span><span class="sxs-lookup"><span data-stu-id="37e91-106">The **JET_INSTANCE_INFO** structure receives information about running database instances when used with the [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) and [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) functions.</span></span>

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a><span data-ttu-id="37e91-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="37e91-107">Members</span></span>

<span data-ttu-id="37e91-108">**хинстанцеид**</span><span class="sxs-lookup"><span data-stu-id="37e91-108">**hInstanceId**</span></span>

<span data-ttu-id="37e91-109">[JET_INSTANCE](./jet-instance.md) заданного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="37e91-109">The [JET_INSTANCE](./jet-instance.md) of the given instance.</span></span>

<span data-ttu-id="37e91-110">**сзинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="37e91-110">**szInstanceName**</span></span>

<span data-ttu-id="37e91-111">Имя экземпляра базы данных.</span><span class="sxs-lookup"><span data-stu-id="37e91-111">The name of the database instance.</span></span> <span data-ttu-id="37e91-112">Это значение может быть **равно NULL** , если у экземпляра нет имени.</span><span class="sxs-lookup"><span data-stu-id="37e91-112">This value can be **NULL** if the instance does not have a name.</span></span>

<span data-ttu-id="37e91-113">**cDatabase**</span><span class="sxs-lookup"><span data-stu-id="37e91-113">**cDatabases**</span></span>

<span data-ttu-id="37e91-114">Число баз данных, присоединенных к экземпляру базы данных.</span><span class="sxs-lookup"><span data-stu-id="37e91-114">The number of databases that are attached to the database instance.</span></span> <span data-ttu-id="37e91-115">Кроме того, **CDatabase** содержит размер массивов строк, возвращаемых в **сздатабасефиленаме**, **сздатабаседисплайнаме** и **сздатабасеслвфиленаме**.</span><span class="sxs-lookup"><span data-stu-id="37e91-115">**cDatabases** also holds the size of the arrays of strings that are returned in **szDatabaseFileName**, **szDatabaseDisplayName**, and **szDatabaseSLVFileName**.</span></span>

<span data-ttu-id="37e91-116">**сздатабасефиленаме**</span><span class="sxs-lookup"><span data-stu-id="37e91-116">**szDatabaseFileName**</span></span>

<span data-ttu-id="37e91-117">Массив строк, содержащий имя файла базы данных, присоединенной к экземпляру базы данных.</span><span class="sxs-lookup"><span data-stu-id="37e91-117">An array of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="37e91-118">Массив содержит элементы **CDatabase** .</span><span class="sxs-lookup"><span data-stu-id="37e91-118">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="37e91-119">**сздатабаседисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="37e91-119">**szDatabaseDisplayName**</span></span>

<span data-ttu-id="37e91-120">Массив строк, содержащий отображаемое имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="37e91-120">An array of strings, each holding the display name of a database.</span></span> <span data-ttu-id="37e91-121">В настоящее время строка может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="37e91-121">Currently the string can be NULL.</span></span> <span data-ttu-id="37e91-122">Массив содержит элементы **CDatabase** .</span><span class="sxs-lookup"><span data-stu-id="37e91-122">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="37e91-123">**сздатабасеслвфиленаме**</span><span class="sxs-lookup"><span data-stu-id="37e91-123">**szDatabaseSLVFileName**</span></span>

<span data-ttu-id="37e91-124">Массив строк, содержащий имя файла файла SLV, присоединенного к экземпляру базы данных.</span><span class="sxs-lookup"><span data-stu-id="37e91-124">An array of strings, each holding the file name of the SLV file that is attached to the database instance.</span></span> <span data-ttu-id="37e91-125">Массив содержит элементы **CDatabase** .</span><span class="sxs-lookup"><span data-stu-id="37e91-125">The array has **cDatabases** elements.</span></span> <span data-ttu-id="37e91-126">Файлы SLV не поддерживаются, поэтому это поле следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="37e91-126">SLV files are not supported, so this field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="37e91-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37e91-127">Remarks</span></span>

<span data-ttu-id="37e91-128">К каждому экземпляру базы данных может быть присоединено несколько баз данных.</span><span class="sxs-lookup"><span data-stu-id="37e91-128">Each database instance can have several databases attached to it.</span></span>

<span data-ttu-id="37e91-129">Для данной структуры **JET_INSTANCE_INFO** массив строк, возвращаемых для баз данных, находится в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="37e91-129">For a given **JET_INSTANCE_INFO** structure, the array of strings that is returned for the databases are in the same order.</span></span> <span data-ttu-id="37e91-130">Например, "Сздатабаседисплайнаме \[ i \] " и "сздатабасефиленаме \[ i \] " ссылаются на одну и ту же базу данных.</span><span class="sxs-lookup"><span data-stu-id="37e91-130">For example, "szDatabaseDisplayName\[ i \]" and "szDatabaseFileName\[ i \]" both refer to the same database.</span></span>

### <a name="requirements"></a><span data-ttu-id="37e91-131">Требования</span><span class="sxs-lookup"><span data-stu-id="37e91-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37e91-132"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="37e91-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="37e91-133">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="37e91-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37e91-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="37e91-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="37e91-135">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="37e91-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37e91-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="37e91-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="37e91-137">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="37e91-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37e91-138"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="37e91-138"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="37e91-139">Реализуется как <strong>JET_INSTANCE_INFO_W</strong> (Юникод) и <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="37e91-139">Implemented as <strong>JET_INSTANCE_INFO_W</strong> (Unicode) and <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="37e91-140">См. также:</span><span class="sxs-lookup"><span data-stu-id="37e91-140">See Also</span></span>

[<span data-ttu-id="37e91-141">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="37e91-141">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="37e91-142">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="37e91-142">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="37e91-143">жетжетинстанцеинфо</span><span class="sxs-lookup"><span data-stu-id="37e91-143">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="37e91-144">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="37e91-144">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)
