---
description: 'Дополнительные сведения: структура JET_SIGNATURE'
title: Структура JET_SIGNATURE
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692516"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="e0317-103">Структура JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="e0317-103">JET_SIGNATURE Structure</span></span>


<span data-ttu-id="e0317-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0317-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_signature-structure"></a><span data-ttu-id="e0317-105">Структура JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="e0317-105">JET_SIGNATURE Structure</span></span>

<span data-ttu-id="e0317-106">Структура **JET_SIGNATURE** содержит сведения, однозначно определяющие базу данных.</span><span class="sxs-lookup"><span data-stu-id="e0317-106">The **JET_SIGNATURE** structure contains information that uniquely identifies a database.</span></span>

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a><span data-ttu-id="e0317-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="e0317-107">Members</span></span>

<span data-ttu-id="e0317-108">**улрандом**</span><span class="sxs-lookup"><span data-stu-id="e0317-108">**ulRandom**</span></span>

<span data-ttu-id="e0317-109">Номер, назначенный случайным образом.</span><span class="sxs-lookup"><span data-stu-id="e0317-109">A randomly assigned number.</span></span>

<span data-ttu-id="e0317-110">**логтимекреате**</span><span class="sxs-lookup"><span data-stu-id="e0317-110">**logtimeCreate**</span></span>

<span data-ttu-id="e0317-111">[JET_LOGTIME](./jet-logtime-structure.md) во время выполнения [жеткреатедатабасе](./jetcreatedatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e0317-111">The [JET_LOGTIME](./jet-logtime-structure.md) at the time of [JetCreateDatabase](./jetcreatedatabase-function.md) is executed.</span></span>

<span data-ttu-id="e0317-112">**сзкомпутернаме**</span><span class="sxs-lookup"><span data-stu-id="e0317-112">**szComputerName**</span></span>

<span data-ttu-id="e0317-113">Необязательное строковое значение NetBIOS-имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="e0317-113">The optional string value of the NetBIOS name for the computer.</span></span> <span data-ttu-id="e0317-114">Это значение не может быть задано.</span><span class="sxs-lookup"><span data-stu-id="e0317-114">This value may not be set.</span></span>

### <a name="remarks"></a><span data-ttu-id="e0317-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0317-115">Remarks</span></span>

<span data-ttu-id="e0317-116">Его можно найти в качестве элемента [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e0317-116">This can be found as an element of [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="e0317-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e0317-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0317-118"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e0317-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e0317-119">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e0317-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0317-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e0317-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e0317-121">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e0317-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0317-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e0317-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e0317-123">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e0317-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e0317-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="e0317-124">See Also</span></span>

[<span data-ttu-id="e0317-125">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="e0317-125">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="e0317-126">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="e0317-126">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="e0317-127">жеткреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="e0317-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)
