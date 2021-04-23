---
description: 'Дополнительные сведения: структура JET_RSTMAP'
title: Структура JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809065"
---
# <a name="jet_rstmap-structure"></a><span data-ttu-id="0ff3d-103">Структура JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="0ff3d-103">JET_RSTMAP Structure</span></span>


<span data-ttu-id="0ff3d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0ff3d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstmap-structure"></a><span data-ttu-id="0ff3d-105">Структура JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="0ff3d-105">JET_RSTMAP Structure</span></span>

<span data-ttu-id="0ff3d-106">Структура **JET_RSTMAP** позволяет переназначить пути к файлам базы данных, которые хранятся в журналах транзакций во время восстановления, при использовании функций [жетинит](./jetinit-function.md) и [жетекстерналресторе](./jetexternalrestore-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff3d-106">The **JET_RSTMAP** structure enables the remapping of database file paths that are stored in the transaction logs during recovery, when used by the [JetInit](./jetinit-function.md) and [JetExternalRestore](./jetexternalrestore-function.md) functions.</span></span> <span data-ttu-id="0ff3d-107">Это позволяет перемещать базы данных в автономном режиме или при восстановлении из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-107">This enables the databases to be moved when offline or when restored from backup.</span></span>

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a><span data-ttu-id="0ff3d-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="0ff3d-108">Members</span></span>

<span data-ttu-id="0ff3d-109">**сздатабасенаме**</span><span class="sxs-lookup"><span data-stu-id="0ff3d-109">**szDatabaseName**</span></span>

<span data-ttu-id="0ff3d-110">Текущий абсолютный путь к базе данных, связанной с журналами транзакций, которые воспроизводятся во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-110">The current absolute path of a database that is associated with the transaction logs that are replayed during recovery.</span></span>

<span data-ttu-id="0ff3d-111">**сзневдатабасенаме**</span><span class="sxs-lookup"><span data-stu-id="0ff3d-111">**szNewDatabaseName**</span></span>

<span data-ttu-id="0ff3d-112">Новый абсолютный путь к базе данных.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-112">The new absolute path for the database.</span></span>

### <a name="requirements"></a><span data-ttu-id="0ff3d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0ff3d-113">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ff3d-114"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="0ff3d-114"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0ff3d-115">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-115">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ff3d-116"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0ff3d-116"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0ff3d-117">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-117">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ff3d-118"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0ff3d-118"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0ff3d-119">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-119">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ff3d-120"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="0ff3d-120"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0ff3d-121">Реализуется как <strong>JET_RSTMAP_W</strong> (Юникод) и <strong>JET_RSTMAP_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0ff3d-121">Implemented as <strong>JET_RSTMAP_W</strong> (Unicode) and <strong>JET_RSTMAP_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0ff3d-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="0ff3d-122">See Also</span></span>

[<span data-ttu-id="0ff3d-123">жетекстерналресторе</span><span class="sxs-lookup"><span data-stu-id="0ff3d-123">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="0ff3d-124">жетинит</span><span class="sxs-lookup"><span data-stu-id="0ff3d-124">JetInit</span></span>](./jetinit-function.md)
