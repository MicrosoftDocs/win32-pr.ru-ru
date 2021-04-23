---
title: Перечисление Вмвиртуалпцевент (Впккоминтерфацес. h)
description: Указывает события виртуальных ПК Windows.
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- Перечисление Вмвиртуалпцевент Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de7ecb639d0b62165dec691d522bed8116670c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072012"
---
# <a name="vmvirtualpcevent-enumeration"></a><span data-ttu-id="48637-104">Перечисление Вмвиртуалпцевент</span><span class="sxs-lookup"><span data-stu-id="48637-104">VMVirtualPCEvent enumeration</span></span>

<span data-ttu-id="48637-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48637-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="48637-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="48637-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="48637-107">Указывает события виртуальных ПК Windows.</span><span class="sxs-lookup"><span data-stu-id="48637-107">Specifies the Windows Virtual PC events.</span></span>

## <a name="syntax"></a><span data-ttu-id="48637-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48637-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a><span data-ttu-id="48637-109">Константы</span><span class="sxs-lookup"><span data-stu-id="48637-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="48637-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**Вмвиртуалпцевент \_ вмстатечанже**</span><span class="sxs-lookup"><span data-stu-id="48637-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent\_VMStateChange**</span></span>
</dt> <dd>

<span data-ttu-id="48637-111">Состояние виртуальной машины изменилось.</span><span class="sxs-lookup"><span data-stu-id="48637-111">A virtual machine's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="48637-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**Вмвиртуалпцевент \_ евентлогжед**</span><span class="sxs-lookup"><span data-stu-id="48637-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent\_EventLogged**</span></span>
</dt> <dd>

<span data-ttu-id="48637-113">Виртуальный ПК зарегистрировал событие.</span><span class="sxs-lookup"><span data-stu-id="48637-113">Virtual PC has logged an event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48637-114">Требования</span><span class="sxs-lookup"><span data-stu-id="48637-114">Requirements</span></span>



| <span data-ttu-id="48637-115">Требование</span><span class="sxs-lookup"><span data-stu-id="48637-115">Requirement</span></span> | <span data-ttu-id="48637-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48637-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48637-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48637-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48637-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="48637-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="48637-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48637-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48637-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="48637-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="48637-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="48637-121">End of client support</span></span><br/>    | <span data-ttu-id="48637-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48637-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="48637-123">Продукт</span><span class="sxs-lookup"><span data-stu-id="48637-123">Product</span></span><br/>                  | <span data-ttu-id="48637-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="48637-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="48637-125">Header</span><span class="sxs-lookup"><span data-stu-id="48637-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="48637-126"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="48637-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48637-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48637-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48637-128">**ивмвиртуалпцевентс**</span><span class="sxs-lookup"><span data-stu-id="48637-128">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

