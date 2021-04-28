---
description: PageFault_TransitionFault класс — этот класс является классом типа события для событий сбоя страницы. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: 6c8ee12cf201b9ee83d231bf1f5e499550aa3cd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106462"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="18a69-104">\_Класс PageFault транситионфаулт</span><span class="sxs-lookup"><span data-stu-id="18a69-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="18a69-105">Этот класс является классом типа события для событий сбоя страницы.</span><span class="sxs-lookup"><span data-stu-id="18a69-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="18a69-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="18a69-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a69-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18a69-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="18a69-108">Члены</span><span class="sxs-lookup"><span data-stu-id="18a69-108">Members</span></span>

<span data-ttu-id="18a69-109">Класс **PageFault \_ транситионфаулт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18a69-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="18a69-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="18a69-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18a69-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="18a69-111">Properties</span></span>

<span data-ttu-id="18a69-112">Класс **PageFault \_ транситионфаулт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18a69-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18a69-113">програмкаунтер</span><span class="sxs-lookup"><span data-stu-id="18a69-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18a69-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18a69-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18a69-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18a69-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18a69-116">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="18a69-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="18a69-117">Указатель на текущую выполняемую инструкцию.</span><span class="sxs-lookup"><span data-stu-id="18a69-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="18a69-118">виртуаладдресс</span><span class="sxs-lookup"><span data-stu-id="18a69-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18a69-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18a69-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18a69-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18a69-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18a69-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="18a69-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="18a69-122">Виртуальный адрес страницы, вызвавшей сбой страницы.</span><span class="sxs-lookup"><span data-stu-id="18a69-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18a69-123">Требования</span><span class="sxs-lookup"><span data-stu-id="18a69-123">Requirements</span></span>



| <span data-ttu-id="18a69-124">Требование</span><span class="sxs-lookup"><span data-stu-id="18a69-124">Requirement</span></span> | <span data-ttu-id="18a69-125">Значение</span><span class="sxs-lookup"><span data-stu-id="18a69-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="18a69-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18a69-126">Minimum supported client</span></span><br/> | <span data-ttu-id="18a69-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="18a69-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="18a69-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18a69-128">Minimum supported server</span></span><br/> | <span data-ttu-id="18a69-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="18a69-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="18a69-130">См. также</span><span class="sxs-lookup"><span data-stu-id="18a69-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a69-131">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="18a69-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




