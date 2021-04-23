---
description: 'Дополнительные сведения: структура JET_RSTINFO'
title: Структура JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144275"
---
# <a name="jet_rstinfo-structure"></a><span data-ttu-id="f55c7-103">Структура JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="f55c7-103">JET_RSTINFO Structure</span></span>


<span data-ttu-id="f55c7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f55c7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstinfo-structure"></a><span data-ttu-id="f55c7-105">Структура JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="f55c7-105">JET_RSTINFO Structure</span></span>

<span data-ttu-id="f55c7-106">Структура **JET_RSTINFO** содержит управляющие данные для процесса восстановления, такие как сведения о перерасположении базы данных, а также возможность управления остановкой восстановления.</span><span class="sxs-lookup"><span data-stu-id="f55c7-106">The **JET_RSTINFO** structure contains control information for the recovery process like database relocation information and ability to control stopping recovery.</span></span>

<span data-ttu-id="f55c7-107">**Windows Vista:** Структура **JET_RSTINFO** появилась в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f55c7-107">**Windows Vista:** The **JET_RSTINFO** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a><span data-ttu-id="f55c7-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="f55c7-108">Members</span></span>

<span data-ttu-id="f55c7-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="f55c7-109">**cbStruct**</span></span>

<span data-ttu-id="f55c7-110">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="f55c7-110">The size of the structure.</span></span>

<span data-ttu-id="f55c7-111">**ргрстмап**</span><span class="sxs-lookup"><span data-stu-id="f55c7-111">**rgrstmap**</span></span>

<span data-ttu-id="f55c7-112">Структура, описывающая старый и новый пути к восстановленной базе данных.</span><span class="sxs-lookup"><span data-stu-id="f55c7-112">The structure that describes the old and new path of a restored database.</span></span>

<span data-ttu-id="f55c7-113">**крстмап**</span><span class="sxs-lookup"><span data-stu-id="f55c7-113">**crstmap**</span></span>

<span data-ttu-id="f55c7-114">Число записей массива в ргрстмап.</span><span class="sxs-lookup"><span data-stu-id="f55c7-114">Count of array entries in the rgrstmap.</span></span>

<span data-ttu-id="f55c7-115">**лгпосстоп**</span><span class="sxs-lookup"><span data-stu-id="f55c7-115">**lgposStop**</span></span>

<span data-ttu-id="f55c7-116">Позиция журнала для отмены восстановления в.</span><span class="sxs-lookup"><span data-stu-id="f55c7-116">The log position to stop recovery at.</span></span> <span data-ttu-id="f55c7-117">Отмена не будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="f55c7-117">No undo will be done.</span></span>

<span data-ttu-id="f55c7-118">**логтиместоп**</span><span class="sxs-lookup"><span data-stu-id="f55c7-118">**logtimeStop**</span></span>

<span data-ttu-id="f55c7-119">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="f55c7-119">Reserved for future use.</span></span>

<span data-ttu-id="f55c7-120">**пфнстатус**</span><span class="sxs-lookup"><span data-stu-id="f55c7-120">**pfnStatus**</span></span>

<span data-ttu-id="f55c7-121">Функция состояния для создания отчета о состоянии восстановления.</span><span class="sxs-lookup"><span data-stu-id="f55c7-121">A status function for reporting status of recovery.</span></span>

### <a name="requirements"></a><span data-ttu-id="f55c7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f55c7-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f55c7-123"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f55c7-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f55c7-124">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f55c7-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f55c7-125"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f55c7-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f55c7-126">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f55c7-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f55c7-127"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f55c7-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f55c7-128">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f55c7-128">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f55c7-129"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="f55c7-129"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f55c7-130">Реализуется как <strong>JET_RSTINFO_W</strong> (Юникод) и <strong>JET_RSTINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f55c7-130">Implemented as <strong>JET_RSTINFO_W</strong> (Unicode) and <strong>JET_RSTINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f55c7-131">См. также:</span><span class="sxs-lookup"><span data-stu-id="f55c7-131">See Also</span></span>

[<span data-ttu-id="f55c7-132">JetInit3</span><span class="sxs-lookup"><span data-stu-id="f55c7-132">JetInit3</span></span>](./jetinit3-function.md)
