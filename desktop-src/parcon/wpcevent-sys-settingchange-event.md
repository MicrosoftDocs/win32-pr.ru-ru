---
description: Событие системного уровня, созданное при изменении параметров родительского контроля.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: Событие WPCEVENT_SYS_SETTINGCHANGE (Впцевент. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712853"
---
# <a name="wpcevent_sys_settingchange-event"></a><span data-ttu-id="ac067-103">\_ \_ Событие сеттингчанже впцевент sys</span><span class="sxs-lookup"><span data-stu-id="ac067-103">WPCEVENT\_SYS\_SETTINGCHANGE event</span></span>

<span data-ttu-id="ac067-104">Событие системного уровня, созданное при изменении параметров родительского контроля.</span><span class="sxs-lookup"><span data-stu-id="ac067-104">System-level event generated on a Parental Controls setting change.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a><span data-ttu-id="ac067-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac067-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac067-106">*Класс*</span><span class="sxs-lookup"><span data-stu-id="ac067-106">*Class*</span></span> 
</dt> <dd>

<span data-ttu-id="ac067-107">Класс, создающий событие.</span><span class="sxs-lookup"><span data-stu-id="ac067-107">The class that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="ac067-108">*Параметр*</span><span class="sxs-lookup"><span data-stu-id="ac067-108">*Setting*</span></span> 
</dt> <dd>

<span data-ttu-id="ac067-109">Значение перечисления **\_ параметров WPC** .</span><span class="sxs-lookup"><span data-stu-id="ac067-109">A value of the **WPC\_SETTINGS** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ac067-110">*Владелец*</span><span class="sxs-lookup"><span data-stu-id="ac067-110">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="ac067-111">Идентификатор безопасности пользователя, создающего событие.</span><span class="sxs-lookup"><span data-stu-id="ac067-111">The security identifier of the user who is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="ac067-112">*олдвал*</span><span class="sxs-lookup"><span data-stu-id="ac067-112">*OldVal*</span></span> 
</dt> <dd>

<span data-ttu-id="ac067-113">Предыдущее значение этого параметра, если оно было удалено или изменено.</span><span class="sxs-lookup"><span data-stu-id="ac067-113">The previous value of this setting, if deleted or changed.</span></span>

</dd> <dt>

<span data-ttu-id="ac067-114">*неввал*</span><span class="sxs-lookup"><span data-stu-id="ac067-114">*NewVal*</span></span> 
</dt> <dd>

<span data-ttu-id="ac067-115">Новое значение этого параметра, если оно добавлено или изменено.</span><span class="sxs-lookup"><span data-stu-id="ac067-115">The new value of this setting, if added or changed.</span></span>

</dd> <dt>

<span data-ttu-id="ac067-116">*Причина*</span><span class="sxs-lookup"><span data-stu-id="ac067-116">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="ac067-117">Значение перечисления [**впкфлаг \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) , которое указывает сведения о том, какие события заблокированы и какие элементы управления будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="ac067-117">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="ac067-118">*Необязательный*</span><span class="sxs-lookup"><span data-stu-id="ac067-118">*Optional*</span></span> 
</dt> <dd>

<span data-ttu-id="ac067-119">Необязательное поле.</span><span class="sxs-lookup"><span data-stu-id="ac067-119">An optional field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac067-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ac067-120">Requirements</span></span>



| <span data-ttu-id="ac067-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ac067-121">Requirement</span></span> | <span data-ttu-id="ac067-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ac067-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac067-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac067-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ac067-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac067-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac067-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac067-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ac067-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac067-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="ac067-127">Header</span><span class="sxs-lookup"><span data-stu-id="ac067-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac067-128"><dt>Впцевент. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac067-128"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac067-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac067-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac067-130">Использование API ведения журнала для родительского контроля</span><span class="sxs-lookup"><span data-stu-id="ac067-130">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="ac067-131">**WPC \_ args \_ конверсатионинитевент**</span><span class="sxs-lookup"><span data-stu-id="ac067-131">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




