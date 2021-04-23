---
description: Этот класс является классом типа события для событий сбоя страницы. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: Класс PageFault_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4bf1f49c909833d75af844c8f2f943a01b6a5d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265252"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="fabf5-104">\_Класс PageFault TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="fabf5-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="fabf5-105">Этот класс является классом типа события для событий сбоя страницы.</span><span class="sxs-lookup"><span data-stu-id="fabf5-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="fabf5-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="fabf5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fabf5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fabf5-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="fabf5-108">Участники</span><span class="sxs-lookup"><span data-stu-id="fabf5-108">Members</span></span>

<span data-ttu-id="fabf5-109">Класс **PageFault \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fabf5-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="fabf5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fabf5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fabf5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="fabf5-111">Properties</span></span>

<span data-ttu-id="fabf5-112">Класс **PageFault \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fabf5-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fabf5-113">програмкаунтер</span><span class="sxs-lookup"><span data-stu-id="fabf5-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fabf5-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fabf5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fabf5-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fabf5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fabf5-116">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="fabf5-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fabf5-117">Указатель на текущую выполняемую инструкцию.</span><span class="sxs-lookup"><span data-stu-id="fabf5-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="fabf5-118">виртуаладдресс</span><span class="sxs-lookup"><span data-stu-id="fabf5-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fabf5-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fabf5-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fabf5-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fabf5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fabf5-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="fabf5-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fabf5-122">Виртуальный адрес страницы, вызвавшей сбой страницы.</span><span class="sxs-lookup"><span data-stu-id="fabf5-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fabf5-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="fabf5-123">Remarks</span></span>

<span data-ttu-id="fabf5-124">Ошибка страницы возникает, когда страница, заданная в кэше памяти, не найдена и должна быть получена из любого места в памяти (кратковременная ошибка) или с диска (жесткий сбой).</span><span class="sxs-lookup"><span data-stu-id="fabf5-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="fabf5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fabf5-125">Requirements</span></span>



| <span data-ttu-id="fabf5-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fabf5-126">Requirement</span></span> | <span data-ttu-id="fabf5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fabf5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fabf5-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fabf5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fabf5-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fabf5-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fabf5-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fabf5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fabf5-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fabf5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fabf5-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fabf5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fabf5-133">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="fabf5-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




