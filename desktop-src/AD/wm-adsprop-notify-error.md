---
title: Сообщение WM_ADSPROP_NOTIFY_ERROR (Адспроп. h)
description: Сообщение об ошибке WM \_ адспроп \_ Notify \_ добавляет сообщение об ошибке в список сообщений об ошибках, которые отображаются путем вызова функции адспропшоверрордиалог.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_ERROR Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135974"
---
# <a name="wm_adsprop_notify_error-message"></a><span data-ttu-id="fc2e8-104">\_ \_ \_ Сообщение об ошибке АДСПРОП для уведомления WM</span><span class="sxs-lookup"><span data-stu-id="fc2e8-104">WM\_ADSPROP\_NOTIFY\_ERROR message</span></span>

<span data-ttu-id="fc2e8-105">Сообщение об ошибке **WM \_ адспроп \_ Notify \_** добавляет сообщение об ошибке в список сообщений об ошибках, которые отображаются путем вызова функции [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .</span><span class="sxs-lookup"><span data-stu-id="fc2e8-105">The **WM\_ADSPROP\_NOTIFY\_ERROR** message adds an error message to a list of error messages that are displayed by calling the [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) function.</span></span>


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="fc2e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc2e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc2e8-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="fc2e8-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2e8-108">Маркер объекта уведомления.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-108">Handle of the notification object.</span></span> <span data-ttu-id="fc2e8-109">Это параметр *хнотифйобжект* , полученный [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="fc2e8-109">This is the *hNotifyObject* parameter obtained by [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="fc2e8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc2e8-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2e8-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc2e8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc2e8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2e8-113">Указатель на структуру [**адспроперрор**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) , содержащую данные сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-113">Pointer to an [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) structure that contains error message data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc2e8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc2e8-114">Return value</span></span>

<span data-ttu-id="fc2e8-115">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc2e8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc2e8-116">Remarks</span></span>

<span data-ttu-id="fc2e8-117">Функция [**адспропсендеррормессаже**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) является предпочтительным методом отправки этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-117">The [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) function is the preferred method of sending this message.</span></span>

<span data-ttu-id="fc2e8-118">Сообщения об ошибках, добавленные сообщением **\_ \_ \_ об ошибке с уведомлением WM адспроп** , накапливаются до вызова [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .</span><span class="sxs-lookup"><span data-stu-id="fc2e8-118">The error messages added by the **WM\_ADSPROP\_NOTIFY\_ERROR** message are accumulated until [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) is called.</span></span> <span data-ttu-id="fc2e8-119">**Адспропшоверрордиалог** объединяет и отображает накопленные сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-119">**ADsPropShowErrorDialog** combines and displays the accumulated error messages.</span></span> <span data-ttu-id="fc2e8-120">При отклонении диалогового окна об ошибке накопленные сообщения об ошибках удаляются.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-120">When the error dialog is dismissed, the accumulated error messages are deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2e8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fc2e8-121">Requirements</span></span>



| <span data-ttu-id="fc2e8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fc2e8-122">Requirement</span></span> | <span data-ttu-id="fc2e8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fc2e8-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2e8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc2e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fc2e8-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc2e8-125">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="fc2e8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc2e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fc2e8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc2e8-127">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="fc2e8-128">Header</span><span class="sxs-lookup"><span data-stu-id="fc2e8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc2e8-129"><dt>Адспроп. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc2e8-129"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc2e8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc2e8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2e8-131">Сообщения в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="fc2e8-131">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="fc2e8-132">**адспроперрор**</span><span class="sxs-lookup"><span data-stu-id="fc2e8-132">**ADSPROPERROR**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[<span data-ttu-id="fc2e8-133">**адспропсендеррормессаже**</span><span class="sxs-lookup"><span data-stu-id="fc2e8-133">**ADsPropSendErrorMessage**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[<span data-ttu-id="fc2e8-134">**адспропшоверрордиалог**</span><span class="sxs-lookup"><span data-stu-id="fc2e8-134">**ADsPropShowErrorDialog**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





