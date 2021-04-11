---
title: Сообщение WM_ADSPROP_NOTIFY_PAGEHWND (Адспроп. h)
description: Расширение страницы свойств службы каталогов Active Directory вызывает метод Адспропсесвнд для информирования объекта уведомления об маркере окна страницы свойств.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_PAGEHWND Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137190"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a><span data-ttu-id="97ef6-104">\_Адспроп \_ уведомления WM \_ пажехвнд</span><span class="sxs-lookup"><span data-stu-id="97ef6-104">WM\_ADSPROP\_NOTIFY\_PAGEHWND message</span></span>

<span data-ttu-id="97ef6-105">Расширение страницы свойств службы каталогов Active Directory вызывает метод [**адспропсесвнд**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) для информирования объекта уведомления об маркере окна страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="97ef6-105">An Active Directory directory service property sheet extension calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) to inform the notification object of the property page window handle.</span></span> <span data-ttu-id="97ef6-106">Функция **адспропсесвнд** отправляет сообщение **WM \_ адспроп \_ Notify \_ пажехвнд** объекту уведомления, который информирует объект уведомления об маркере окна страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="97ef6-106">The **ADsPropSetHwnd** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEHWND** message to the notification object, which informs the notification object of the property page window handle.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a><span data-ttu-id="97ef6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="97ef6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97ef6-108">*хнотифйобж*</span><span class="sxs-lookup"><span data-stu-id="97ef6-108">*hNotifyObj*</span></span> 
</dt> <dd>

<span data-ttu-id="97ef6-109">Маркер объекта уведомления.</span><span class="sxs-lookup"><span data-stu-id="97ef6-109">The handle of the notification object.</span></span> <span data-ttu-id="97ef6-110">Чтобы получить этот маркер, вызовите [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="97ef6-110">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="97ef6-111">*хпаже*</span><span class="sxs-lookup"><span data-stu-id="97ef6-111">*hPage*</span></span> 
</dt> <dd>

<span data-ttu-id="97ef6-112">Описатель окна страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="97ef6-112">A window handle of the property page.</span></span>

</dd> <dt>

<span data-ttu-id="97ef6-113">*птзтитле*</span><span class="sxs-lookup"><span data-stu-id="97ef6-113">*ptzTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="97ef6-114">Указатель на заканчивающийся нулем буфер **WCHAR** , который содержит заголовок страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="97ef6-114">Pointer to a NULL-terminated **WCHAR** buffer that contains the title of the property page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97ef6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97ef6-115">Return value</span></span>

<span data-ttu-id="97ef6-116">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="97ef6-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97ef6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97ef6-117">Remarks</span></span>

<span data-ttu-id="97ef6-118">Расширение страницы свойств Active Directory обычно вызывает функцию [**адспропсесвнд**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) при обработке сообщения [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="97ef6-118">An Active Directory property sheet extension normally calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) function while processing the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ef6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="97ef6-119">Requirements</span></span>



| <span data-ttu-id="97ef6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="97ef6-120">Requirement</span></span> | <span data-ttu-id="97ef6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="97ef6-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97ef6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97ef6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="97ef6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97ef6-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="97ef6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97ef6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="97ef6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97ef6-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="97ef6-126">Header</span><span class="sxs-lookup"><span data-stu-id="97ef6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ef6-127"><dt>Адспроп. h</dt></span><span class="sxs-lookup"><span data-stu-id="97ef6-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ef6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97ef6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ef6-129">Сообщения в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="97ef6-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="97ef6-130">**адспропсесвнд**</span><span class="sxs-lookup"><span data-stu-id="97ef6-130">**ADsPropSetHwnd**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[<span data-ttu-id="97ef6-131">**адспропкреатенотифйобж**</span><span class="sxs-lookup"><span data-stu-id="97ef6-131">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="97ef6-132">**WM \_ инитдиалог**</span><span class="sxs-lookup"><span data-stu-id="97ef6-132">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

