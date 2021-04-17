---
description: Хранит сведения о разделах общей памяти.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Структура SHAREDMEMORY_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674061"
---
# <a name="sharedmemory_header-structure"></a><span data-ttu-id="e9e5d-103">\_Структура заголовка шаредмемори</span><span class="sxs-lookup"><span data-stu-id="e9e5d-103">SHAREDMEMORY\_HEADER structure</span></span>

<span data-ttu-id="e9e5d-104">Хранит сведения о разделах общей памяти.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-104">Stores information about shared memory sections.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e5d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9e5d-105">Syntax</span></span>


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a><span data-ttu-id="e9e5d-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e9e5d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9e5d-107">**кбтотал**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-107">**cbTotal**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-108">Размер (в байтах) данных, на которые ссылается эта структура заголовка.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-108">The size, in bytes, of the data referenced by this header structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-109">**кбоффсетснс**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-109">**cbOffsetSns**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-110">Размер (в байтах), в котором серийные номера смещены от структуры заголовка.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-110">The size, in bytes, that the serial numbers are offset from the header structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-111">**идксевент**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-111">**idxEvent**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-112">Индекс события.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-112">The event index.</span></span> <span data-ttu-id="e9e5d-113">Это значение увеличивается с помощью последовательных событий.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-113">This value is incremented with successive events.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-114">**двевент**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-114">**dwEvent**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-115">Событие, связанное с этим заголовком.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-115">The event associated with this header.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-116">**согласуется**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-116">**cid**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-117">Идентификатор курсора, на который ссылается заголовок общей памяти.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-117">The cursor identifier referenced by the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-118">**sn**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-118">**sn**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-119">Серийный номер заголовка общей памяти.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-119">The serial number for the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-120">**сисевт**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-120">**sysEvt**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-121">Системное событие с префиксом SE \_ \* , связанное с этим заголовком.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-121">The system event, prefixed SE\_\*, associated with this header.</span></span> <span data-ttu-id="e9e5d-122">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e9e5d-122">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-123">**сисевтдата**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-123">**sysEvtData**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-124">Структура [**\_ \_ данных системных событий**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) , связанная с системным событием.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-124">The [**SYSTEM\_EVENT\_DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) structure associated with the system event.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-125">**кпаккетс**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-125">**cPackets**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-126">Число пакетов, связанных с текущим разделом общей памяти.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-126">A count of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-127">**кбпаккетс**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-127">**cbPackets**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-128">Размер пакетов в байтах, связанных с текущим разделом общей памяти.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-128">The size, in bytes, of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="e9e5d-129">**фснспресент**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-129">**fSnsPresent**</span></span>
</dt> <dd>

<span data-ttu-id="e9e5d-130">Флаг, указывающий, имеются ли серийные номера в текущем разделе общей памяти.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-130">A flag indicating whether serial numbers are present in the current shared memory section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9e5d-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9e5d-131">Remarks</span></span>

<span data-ttu-id="e9e5d-132">Для элемента **сисевт** определены следующие значения.</span><span class="sxs-lookup"><span data-stu-id="e9e5d-132">The following values are defined for the **sysEvt** member.</span></span>


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a><span data-ttu-id="e9e5d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9e5d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e5d-134">**\_данные системных событий \_**</span><span class="sxs-lookup"><span data-stu-id="e9e5d-134">**SYSTEM\_EVENT\_DATA**</span></span>](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



