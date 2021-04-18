---
title: Сообщение WM_ADSPROP_NOTIFY_APPLY (Адспроп. h)
description: Расширение страницы свойств службы каталогов Active Directory отправляет \_ сообщение об установке WM адспроп \_ Notify \_ в объект уведомления, если страница свойств PSN \_ Применить обработчик.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_APPLY Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654661"
---
# <a name="wm_adsprop_notify_apply-message"></a><span data-ttu-id="743ad-104">\_ \_ Сообщение об использовании уведомления WM адспроп \_</span><span class="sxs-lookup"><span data-stu-id="743ad-104">WM\_ADSPROP\_NOTIFY\_APPLY message</span></span>

<span data-ttu-id="743ad-105">Расширение страницы свойств службы каталогов Active Directory отправляет сообщение об **\_ \_ \_ установке WM адспроп notify** в объект уведомления, если страница свойств PSN \_ Применить обработчик.</span><span class="sxs-lookup"><span data-stu-id="743ad-105">An Active Directory directory service property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_APPLY** message to the notification object if the property page PSN\_APPLY handler succeeds.</span></span>


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="743ad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="743ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="743ad-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="743ad-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="743ad-108">Маркер объекта уведомления.</span><span class="sxs-lookup"><span data-stu-id="743ad-108">The handle of the notification object.</span></span> <span data-ttu-id="743ad-109">Чтобы получить этот маркер, вызовите [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="743ad-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="743ad-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="743ad-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="743ad-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="743ad-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="743ad-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="743ad-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="743ad-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="743ad-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="743ad-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="743ad-114">Return value</span></span>

<span data-ttu-id="743ad-115">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="743ad-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="743ad-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="743ad-116">Remarks</span></span>

<span data-ttu-id="743ad-117">При добавлении страниц в оснастку консоли управления (MMC) Active Directory Manager Active Directory вкладки свойств MMC создают объекты уведомлений по вызову функции [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) , а затем передает этот обработчик объекта уведомления на каждую страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="743ad-117">When adding pages to the Active Directory Manager MMC snap-in, Active Directory MMC property sheets create the notification objects by a call to the [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) function, and then passes the notification object handle to each property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="743ad-118">Требования</span><span class="sxs-lookup"><span data-stu-id="743ad-118">Requirements</span></span>



| <span data-ttu-id="743ad-119">Требование</span><span class="sxs-lookup"><span data-stu-id="743ad-119">Requirement</span></span> | <span data-ttu-id="743ad-120">Значение</span><span class="sxs-lookup"><span data-stu-id="743ad-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="743ad-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="743ad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="743ad-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="743ad-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="743ad-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="743ad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="743ad-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="743ad-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="743ad-125">Header</span><span class="sxs-lookup"><span data-stu-id="743ad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="743ad-126"><dt>Адспроп. h</dt></span><span class="sxs-lookup"><span data-stu-id="743ad-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="743ad-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="743ad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743ad-128">**адспропкреатенотифйобж**</span><span class="sxs-lookup"><span data-stu-id="743ad-128">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="743ad-129">Сообщения в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="743ad-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





