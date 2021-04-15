---
description: 'Дополнительные сведения: структура JET_DBINFOUPGRADE'
title: Структура JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682669"
---
# <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="83d22-103">Структура JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="83d22-103">JET_DBINFOUPGRADE Structure</span></span>


<span data-ttu-id="83d22-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="83d22-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="83d22-105">Структура JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="83d22-105">JET_DBINFOUPGRADE Structure</span></span>

<span data-ttu-id="83d22-106">Структура **JET_DBINFOUPGRADE** содержит сведения о состоянии обновления базы данных.</span><span class="sxs-lookup"><span data-stu-id="83d22-106">The **JET_DBINFOUPGRADE** structure holds information about the upgrade status of the database.</span></span> <span data-ttu-id="83d22-107">Это значение извлекается, только если **JET_DBINFOUPGRADE** передано в [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md) или [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="83d22-107">This value is retrieved only if **JET_DBINFOUPGRADE** was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="83d22-108">Эта структура не является обязательной для текущих версий операционной системы ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="83d22-108">This structure is not required for current operating system versions of the database engine.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a><span data-ttu-id="83d22-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="83d22-109">Members</span></span>

<span data-ttu-id="83d22-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="83d22-110">**cbStruct**</span></span>

<span data-ttu-id="83d22-111">Задайте размер структуры **JET_DBINFOUPGRADE** в байтах.</span><span class="sxs-lookup"><span data-stu-id="83d22-111">Set to the size of the **JET_DBINFOUPGRADE** structure, in bytes.</span></span>

<span data-ttu-id="83d22-112">**кбфилесизелов**</span><span class="sxs-lookup"><span data-stu-id="83d22-112">**cbFilesizeLow**</span></span>

<span data-ttu-id="83d22-113">Нижний **DWORD** , отражающий текущий размер файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="83d22-113">The low **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="83d22-114">**кбфилесизехигх**</span><span class="sxs-lookup"><span data-stu-id="83d22-114">**cbFilesizeHigh**</span></span>

<span data-ttu-id="83d22-115">Верхний **DWORD** , отражающий текущий размер файла для базы данных.</span><span class="sxs-lookup"><span data-stu-id="83d22-115">The high **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="83d22-116">**кбфриспацерекуиредлов**</span><span class="sxs-lookup"><span data-stu-id="83d22-116">**cbFreeSpaceRequiredLow**</span></span>

<span data-ttu-id="83d22-117">Нижний **DWORD** предполагаемого свободного места на диске, необходимый для обновления на месте.</span><span class="sxs-lookup"><span data-stu-id="83d22-117">The low **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="83d22-118">**кбфриспацерекуиредхигх**</span><span class="sxs-lookup"><span data-stu-id="83d22-118">**cbFreeSpaceRequiredHigh**</span></span>

<span data-ttu-id="83d22-119">Большой **DWORD** предполагаемого свободного места на диске, необходимый для обновления на месте.</span><span class="sxs-lookup"><span data-stu-id="83d22-119">The high **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="83d22-120">**ксектаупграде**</span><span class="sxs-lookup"><span data-stu-id="83d22-120">**csecToUpgrade**</span></span>

<span data-ttu-id="83d22-121">Предполагаемое время, необходимое для обновления, в секундах.</span><span class="sxs-lookup"><span data-stu-id="83d22-121">The estimated time required to upgrade, in seconds.</span></span>

<span data-ttu-id="83d22-122">**улфлагс**</span><span class="sxs-lookup"><span data-stu-id="83d22-122">**ulFlags**</span></span>

<span data-ttu-id="83d22-123">Битовое поле, состоящие из одного или нескольких следующих флагов: **фупградабле**, **фалреадюпградед**.</span><span class="sxs-lookup"><span data-stu-id="83d22-123">A bit field made of zero or more of the following flags: **fUpgradable**, **fAlreadyUpgraded**.</span></span>

<span data-ttu-id="83d22-124">**фупградабле**</span><span class="sxs-lookup"><span data-stu-id="83d22-124">**fUpgradable**</span></span>

<span data-ttu-id="83d22-125">База данных обновляема.</span><span class="sxs-lookup"><span data-stu-id="83d22-125">The database is upgradeable.</span></span>

<span data-ttu-id="83d22-126">**фалреадюпградед**</span><span class="sxs-lookup"><span data-stu-id="83d22-126">**fAlreadyUpgraded**</span></span>

<span data-ttu-id="83d22-127">База данных обновляется до текущего формата базы данных.</span><span class="sxs-lookup"><span data-stu-id="83d22-127">The database is upgraded to the current database format.</span></span>

### <a name="remarks"></a><span data-ttu-id="83d22-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83d22-128">Remarks</span></span>

<span data-ttu-id="83d22-129">Структура **JET_DBINFOUPGRADE** заполняется вызовом [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md) или [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="83d22-129">A **JET_DBINFOUPGRADE** structure is populated by a call to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="83d22-130">Если функция не выполнена, содержимое структуры не определено.</span><span class="sxs-lookup"><span data-stu-id="83d22-130">If the function does not succeed, the contents of the structure are undefined.</span></span>

### <a name="requirements"></a><span data-ttu-id="83d22-131">Требования</span><span class="sxs-lookup"><span data-stu-id="83d22-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83d22-132"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="83d22-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="83d22-133">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="83d22-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83d22-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="83d22-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="83d22-135">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="83d22-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83d22-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="83d22-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="83d22-137">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="83d22-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="83d22-138">См. также:</span><span class="sxs-lookup"><span data-stu-id="83d22-138">See Also</span></span>

[<span data-ttu-id="83d22-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="83d22-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="83d22-140">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="83d22-140">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="83d22-141">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="83d22-141">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="83d22-142">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="83d22-142">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="83d22-143">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="83d22-143">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="83d22-144">жетжетобжектинфо</span><span class="sxs-lookup"><span data-stu-id="83d22-144">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="83d22-145">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="83d22-145">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="83d22-146">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="83d22-146">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
