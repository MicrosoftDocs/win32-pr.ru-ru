---
description: Событие для каждого пользователя, которое поддерживает до трех полей.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: Событие WPCEVENT_CUSTOM (Впцевент. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264348"
---
# <a name="wpcevent_custom-event"></a><span data-ttu-id="ec400-103">\_Пользовательское событие впцевент</span><span class="sxs-lookup"><span data-stu-id="ec400-103">WPCEVENT\_CUSTOM event</span></span>

<span data-ttu-id="ec400-104">Событие для каждого пользователя, которое поддерживает до трех полей.</span><span class="sxs-lookup"><span data-stu-id="ec400-104">Per-user event that supports up to three fields.</span></span>

<span data-ttu-id="ec400-105">События отображаются в **средстве просмотра действий** в **другом** разделе со следующей иерархией:</span><span class="sxs-lookup"><span data-stu-id="ec400-105">Events are displayed in the **Activity Viewer** in the **Other** section with the following hierarchy:</span></span>

1.  <span data-ttu-id="ec400-106">Publisher</span><span class="sxs-lookup"><span data-stu-id="ec400-106">Publisher</span></span>

2.  <span data-ttu-id="ec400-107">Приложение</span><span class="sxs-lookup"><span data-stu-id="ec400-107">Application</span></span>

3.  <span data-ttu-id="ec400-108">Событие</span><span class="sxs-lookup"><span data-stu-id="ec400-108">Event</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="ec400-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec400-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec400-110">*Издатель*</span><span class="sxs-lookup"><span data-stu-id="ec400-110">*Publisher*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-111">Издатель события (например, название компании).</span><span class="sxs-lookup"><span data-stu-id="ec400-111">The publisher of the event (for example, a company name).</span></span>

</dd> <dt>

<span data-ttu-id="ec400-112">*AppName*</span><span class="sxs-lookup"><span data-stu-id="ec400-112">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-113">Имя приложения, создающего событие.</span><span class="sxs-lookup"><span data-stu-id="ec400-113">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="ec400-114">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="ec400-114">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-115">Версия приложения, создающего событие.</span><span class="sxs-lookup"><span data-stu-id="ec400-115">The version of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="ec400-116">*Событие*</span><span class="sxs-lookup"><span data-stu-id="ec400-116">*Event*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-117">Имя события.</span><span class="sxs-lookup"><span data-stu-id="ec400-117">The name for the event.</span></span>

</dd> <dt>

<span data-ttu-id="ec400-118">*Значение1*</span><span class="sxs-lookup"><span data-stu-id="ec400-118">*Value1*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-119">Настраиваемое поле 1.</span><span class="sxs-lookup"><span data-stu-id="ec400-119">Custom field 1.</span></span>

</dd> <dt>

<span data-ttu-id="ec400-120">*Value2*</span><span class="sxs-lookup"><span data-stu-id="ec400-120">*Value2*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-121">Настраиваемое поле 2.</span><span class="sxs-lookup"><span data-stu-id="ec400-121">Custom field 2.</span></span>

</dd> <dt>

<span data-ttu-id="ec400-122">*Значение3*</span><span class="sxs-lookup"><span data-stu-id="ec400-122">*Value3*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-123">Настраиваемое поле 3.</span><span class="sxs-lookup"><span data-stu-id="ec400-123">Custom field 3.</span></span>

</dd> <dt>

<span data-ttu-id="ec400-124">*Блокировано*</span><span class="sxs-lookup"><span data-stu-id="ec400-124">*Blocked*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-125">Значение перечисления [**впкфлаг \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) , которое указывает сведения о том, какие события заблокированы и какие элементы управления будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="ec400-125">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="ec400-126">*Причина*</span><span class="sxs-lookup"><span data-stu-id="ec400-126">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="ec400-127">Пользовательская строка, предоставляющая дополнительные сведения о причине блокировки или запрета блокировки.</span><span class="sxs-lookup"><span data-stu-id="ec400-127">A custom string that provides extra information about the reason for blocking or not blocking.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec400-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ec400-128">Requirements</span></span>



| <span data-ttu-id="ec400-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ec400-129">Requirement</span></span> | <span data-ttu-id="ec400-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ec400-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec400-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec400-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ec400-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec400-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec400-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec400-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ec400-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ec400-134">None supported</span></span><br/>                                                             |
| <span data-ttu-id="ec400-135">Header</span><span class="sxs-lookup"><span data-stu-id="ec400-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec400-136"><dt>Впцевент. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec400-136"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec400-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec400-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec400-138">Использование API ведения журнала для родительского контроля</span><span class="sxs-lookup"><span data-stu-id="ec400-138">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="ec400-139">**WPC \_ args \_ конверсатионинитевент**</span><span class="sxs-lookup"><span data-stu-id="ec400-139">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




