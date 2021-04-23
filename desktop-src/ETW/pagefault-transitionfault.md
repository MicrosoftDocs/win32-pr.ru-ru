---
description: Этот класс является классом типа события для событий сбоя страницы. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: Класс PageFault_TransitionFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4721e2d342750b12baa58bb69f72606511c14143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911043"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="11f94-104">\_Класс PageFault транситионфаулт</span><span class="sxs-lookup"><span data-stu-id="11f94-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="11f94-105">Этот класс является классом типа события для событий сбоя страницы.</span><span class="sxs-lookup"><span data-stu-id="11f94-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="11f94-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="11f94-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f94-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11f94-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="11f94-108">Участники</span><span class="sxs-lookup"><span data-stu-id="11f94-108">Members</span></span>

<span data-ttu-id="11f94-109">Класс **PageFault \_ транситионфаулт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11f94-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="11f94-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="11f94-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11f94-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="11f94-111">Properties</span></span>

<span data-ttu-id="11f94-112">Класс **PageFault \_ транситионфаулт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="11f94-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11f94-113">програмкаунтер</span><span class="sxs-lookup"><span data-stu-id="11f94-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f94-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11f94-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11f94-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11f94-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11f94-116">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="11f94-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="11f94-117">Указатель на текущую выполняемую инструкцию.</span><span class="sxs-lookup"><span data-stu-id="11f94-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="11f94-118">виртуаладдресс</span><span class="sxs-lookup"><span data-stu-id="11f94-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f94-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11f94-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11f94-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11f94-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11f94-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="11f94-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="11f94-122">Виртуальный адрес страницы, вызвавшей сбой страницы.</span><span class="sxs-lookup"><span data-stu-id="11f94-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11f94-123">Требования</span><span class="sxs-lookup"><span data-stu-id="11f94-123">Requirements</span></span>



| <span data-ttu-id="11f94-124">Требование</span><span class="sxs-lookup"><span data-stu-id="11f94-124">Requirement</span></span> | <span data-ttu-id="11f94-125">Значение</span><span class="sxs-lookup"><span data-stu-id="11f94-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="11f94-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11f94-126">Minimum supported client</span></span><br/> | <span data-ttu-id="11f94-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11f94-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="11f94-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11f94-128">Minimum supported server</span></span><br/> | <span data-ttu-id="11f94-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11f94-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="11f94-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11f94-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f94-131">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="11f94-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




