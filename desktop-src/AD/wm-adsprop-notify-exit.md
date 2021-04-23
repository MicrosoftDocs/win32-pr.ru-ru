---
title: Сообщение WM_ADSPROP_NOTIFY_EXIT (Адспроп. h)
description: Расширение страницы свойств Active Directory отправляет \_ сообщение о выходе WM адспроп \_ Notify \_ в объект уведомления, когда объект уведомления больше не требуется.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_EXIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989199"
---
# <a name="wm_adsprop_notify_exit-message"></a><span data-ttu-id="b5ce0-104">\_ \_ Сообщение о выходе из уведомления WM адспроп \_</span><span class="sxs-lookup"><span data-stu-id="b5ce0-104">WM\_ADSPROP\_NOTIFY\_EXIT message</span></span>

<span data-ttu-id="b5ce0-105">Расширение страницы свойств Active Directory отправляет сообщение о **\_ \_ \_ выходе WM адспроп notify** в объект уведомления, когда объект уведомления больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-105">An Active Directory property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_EXIT** message to the notification object when the notification object is no longer required.</span></span>


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="b5ce0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5ce0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ce0-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b5ce0-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ce0-108">Маркер объекта уведомления.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-108">The handle of the notification object.</span></span> <span data-ttu-id="b5ce0-109">Чтобы получить этот маркер, вызовите [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="b5ce0-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="b5ce0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5ce0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ce0-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5ce0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5ce0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ce0-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ce0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5ce0-114">Return value</span></span>

<span data-ttu-id="b5ce0-115">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ce0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5ce0-116">Remarks</span></span>

<span data-ttu-id="b5ce0-117">Объект уведомления удалит себя в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-117">The notification object will delete itself in response to this message.</span></span> <span data-ttu-id="b5ce0-118">При отправке этого сообщения обработчик объекта уведомления должен считаться недопустимым.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-118">When this message has been sent, the notification object handle should be considered invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ce0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b5ce0-119">Requirements</span></span>



| <span data-ttu-id="b5ce0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b5ce0-120">Requirement</span></span> | <span data-ttu-id="b5ce0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b5ce0-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ce0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5ce0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ce0-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5ce0-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="b5ce0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5ce0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ce0-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5ce0-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="b5ce0-126">Header</span><span class="sxs-lookup"><span data-stu-id="b5ce0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5ce0-127"><dt>Адспроп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ce0-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ce0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5ce0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ce0-129">**адспропкреатенотифйобж**</span><span class="sxs-lookup"><span data-stu-id="b5ce0-129">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="b5ce0-130">Сообщения в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="b5ce0-130">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





