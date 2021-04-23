---
description: Событие для каждого пользователя, предоставляемое для ведения журнала при инициации беседы клиентами мгновенных сообщений.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: Событие WPCEVENT_IM_INVITATION (Впцевент. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712575"
---
# <a name="wpcevent_im_invitation-event"></a><span data-ttu-id="7753d-103">\_ \_ Событие приглашения впцевент IM</span><span class="sxs-lookup"><span data-stu-id="7753d-103">WPCEVENT\_IM\_INVITATION event</span></span>

<span data-ttu-id="7753d-104">Событие для каждого пользователя, предоставляемое для ведения журнала при инициации беседы клиентами мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7753d-104">Per-user event provided for logging initiation of conversations by Instant Messaging clients.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="7753d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="7753d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7753d-106">*AppName*</span><span class="sxs-lookup"><span data-stu-id="7753d-106">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-107">Имя приложения, создающего событие.</span><span class="sxs-lookup"><span data-stu-id="7753d-107">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="7753d-108">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="7753d-108">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-109">Строка версии для приложения, создающего событие.</span><span class="sxs-lookup"><span data-stu-id="7753d-109">The version string for the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="7753d-110">*AccountName*</span><span class="sxs-lookup"><span data-stu-id="7753d-110">*AccountName*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-111">Строка идентификатора учетной записи мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7753d-111">The instant messaging account identity string.</span></span>

</dd> <dt>

<span data-ttu-id="7753d-112">*конвид*</span><span class="sxs-lookup"><span data-stu-id="7753d-112">*ConvID*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-113">Идентификатор диалога.</span><span class="sxs-lookup"><span data-stu-id="7753d-113">The identifier for the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="7753d-114">*рекуестингип*</span><span class="sxs-lookup"><span data-stu-id="7753d-114">*RequestingIP*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-115">Строка, содержащая IP-адрес компьютера, отправляющего приглашение.</span><span class="sxs-lookup"><span data-stu-id="7753d-115">A string that contains the IP address of the computer that is sending the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="7753d-116">*Отправитель*</span><span class="sxs-lookup"><span data-stu-id="7753d-116">*Sender*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-117">Строка удостоверения учетной записи для обмена мгновенными сообщениями для учетной записи, которая выдает приглашение.</span><span class="sxs-lookup"><span data-stu-id="7753d-117">The instant messaging account identity string for the account that is issuing the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="7753d-118">*Причина*</span><span class="sxs-lookup"><span data-stu-id="7753d-118">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-119">Значение перечисления [**впкфлаг \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) , которое указывает сведения о том, какие события заблокированы и какие элементы управления будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="7753d-119">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="7753d-120">*реЦипкаунт*</span><span class="sxs-lookup"><span data-stu-id="7753d-120">*RecipCount*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-121">Число получателей, получивших приглашение, и имеющих удостоверения, определенные в поле получателя.</span><span class="sxs-lookup"><span data-stu-id="7753d-121">The count of recipients who are receiving the invitation and who have identities defined in the recipient field.</span></span>

</dd> <dt>

<span data-ttu-id="7753d-122">*Recipient*</span><span class="sxs-lookup"><span data-stu-id="7753d-122">*Recipient*</span></span> 
</dt> <dd>

<span data-ttu-id="7753d-123">Строка с разделителями, содержащая строки идентификаторов учетных записей мгновенных сообщений для получателей приглашения.</span><span class="sxs-lookup"><span data-stu-id="7753d-123">A delimited string that contains instant messaging account identity strings for the recipients of the invitation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7753d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7753d-124">Requirements</span></span>



| <span data-ttu-id="7753d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7753d-125">Requirement</span></span> | <span data-ttu-id="7753d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7753d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7753d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7753d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7753d-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7753d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7753d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7753d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7753d-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7753d-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="7753d-131">Header</span><span class="sxs-lookup"><span data-stu-id="7753d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7753d-132"><dt>Впцевент. h</dt></span><span class="sxs-lookup"><span data-stu-id="7753d-132"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7753d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7753d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7753d-134">Использование API ведения журнала для родительского контроля</span><span class="sxs-lookup"><span data-stu-id="7753d-134">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="7753d-135">**WPC \_ args \_ конверсатионинитевент**</span><span class="sxs-lookup"><span data-stu-id="7753d-135">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




