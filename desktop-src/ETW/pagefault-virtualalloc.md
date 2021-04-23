---
description: Этот класс является классом типа события для виртуальных событий выделения. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: Класс PageFault_VirtualAlloc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344002"
---
# <a name="pagefault_virtualalloc-class"></a><span data-ttu-id="9c445-104">\_Класс PageFault VirtualAlloc</span><span class="sxs-lookup"><span data-stu-id="9c445-104">PageFault\_VirtualAlloc class</span></span>

<span data-ttu-id="9c445-105">Этот класс является классом типа события для виртуальных событий выделения.</span><span class="sxs-lookup"><span data-stu-id="9c445-105">This class is the event type class for virtual allocation events.</span></span>

<span data-ttu-id="9c445-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9c445-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c445-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c445-107">Syntax</span></span>

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="9c445-108">Участники</span><span class="sxs-lookup"><span data-stu-id="9c445-108">Members</span></span>

<span data-ttu-id="9c445-109">Класс **PageFault \_ VirtualAlloc** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c445-109">The **PageFault\_VirtualAlloc** class has these types of members:</span></span>

-   [<span data-ttu-id="9c445-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c445-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c445-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c445-111">Properties</span></span>

<span data-ttu-id="9c445-112">Класс **PageFault \_ VirtualAlloc** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9c445-112">The **PageFault\_VirtualAlloc** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c445-113">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="9c445-113">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c445-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c445-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c445-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c445-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c445-116">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="9c445-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9c445-117">Начальный адрес, с которого была выделена или освобождена память.</span><span class="sxs-lookup"><span data-stu-id="9c445-117">The starting address at which memory was allocated or freed.</span></span>

</dd> <dt>

<span data-ttu-id="9c445-118">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="9c445-118">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c445-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c445-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c445-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c445-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c445-121">Квалификаторы: Вмидатаид (4), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="9c445-121">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="9c445-122">Тип выполнения выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="9c445-122">The type of memory allocation that was performed.</span></span> <span data-ttu-id="9c445-123">Возможные значения см. в описании параметра *флаллокатионтипе* функции [**виртуалаллоцекс**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .</span><span class="sxs-lookup"><span data-stu-id="9c445-123">For possible values, see the *flAllocationType* parameter of the [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) function.</span></span>

</dd> <dt>

<span data-ttu-id="9c445-124">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="9c445-124">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c445-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c445-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c445-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c445-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c445-127">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="9c445-127">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="9c445-128">Процесс, который владеет памятью (может отличаться от потока, выполнившего выделение).</span><span class="sxs-lookup"><span data-stu-id="9c445-128">The process that owned the memory (can be different from the thread that performed the allocation).</span></span>

</dd> <dt>

<span data-ttu-id="9c445-129">**регионсизе**</span><span class="sxs-lookup"><span data-stu-id="9c445-129">**RegionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c445-130">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="9c445-130">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9c445-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c445-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c445-132">Квалификаторы: Вмидатаид (2), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="9c445-132">Qualifiers: WmiDataId(2), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="9c445-133">Размер выделенной или освобожденной памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="9c445-133">The size, in bytes, of the memory that was allocated or freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c445-134">Требования</span><span class="sxs-lookup"><span data-stu-id="9c445-134">Requirements</span></span>



| <span data-ttu-id="9c445-135">Требование</span><span class="sxs-lookup"><span data-stu-id="9c445-135">Requirement</span></span> | <span data-ttu-id="9c445-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9c445-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9c445-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c445-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9c445-138">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9c445-138">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9c445-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c445-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9c445-140">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c445-140">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c445-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c445-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c445-142">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="9c445-142">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 
