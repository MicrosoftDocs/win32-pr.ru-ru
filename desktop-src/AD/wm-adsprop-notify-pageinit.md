---
title: Сообщение WM_ADSPROP_NOTIFY_PAGEINIT (Адспроп. h)
description: Расширение страницы свойств Active Directory вызывает метод Адспропжетинитинфо для получения данных о объекте каталога, к которому применяется расширение страницы свойств.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_PAGEINIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533986"
---
# <a name="wm_adsprop_notify_pageinit-message"></a><span data-ttu-id="86904-104">\_Адспроп \_ уведомления WM \_ пажеинит</span><span class="sxs-lookup"><span data-stu-id="86904-104">WM\_ADSPROP\_NOTIFY\_PAGEINIT message</span></span>

<span data-ttu-id="86904-105">Расширение страницы свойств Active Directory вызывает метод [**адспропжетинитинфо**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) для получения данных о объекте каталога, к которому применяется расширение страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="86904-105">An Active Directory property sheet extension calls the [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) to obtain data about regarding the directory object that the property sheet extension applies to.</span></span> <span data-ttu-id="86904-106">Функция **адспропжетинитинфо** отправляет сообщение **WM \_ адспроп \_ Notify \_ пажеинит** в объект уведомления для достижения этого результата.</span><span class="sxs-lookup"><span data-stu-id="86904-106">The **ADsPropGetInitInfo** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEINIT** message to the notification object to achieve this result.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a><span data-ttu-id="86904-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="86904-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86904-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="86904-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="86904-109">Маркер объекта уведомления.</span><span class="sxs-lookup"><span data-stu-id="86904-109">Handle of the notification object.</span></span> <span data-ttu-id="86904-110">Это параметр *хнотифйобжект* , полученный при вызове [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="86904-110">This is the *hNotifyObject* parameter obtained by a call to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="86904-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86904-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86904-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="86904-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="86904-113">*падспропинитпарамс*</span><span class="sxs-lookup"><span data-stu-id="86904-113">*pADsPropInitParams*</span></span> 
</dt> <dd>

<span data-ttu-id="86904-114">Указатель на структуру [**адспропинитпарамс**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) , которая получает сведения об объекте каталога.</span><span class="sxs-lookup"><span data-stu-id="86904-114">Pointer to an [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) structure that receives the directory object information.</span></span> <span data-ttu-id="86904-115">Это параметр *пинитпарамс* , передаваемый в [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="86904-115">This is the *pInitParams* parameter passed to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86904-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86904-116">Return value</span></span>

<span data-ttu-id="86904-117">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="86904-117">This message has no return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="86904-118">Требования</span><span class="sxs-lookup"><span data-stu-id="86904-118">Requirements</span></span>



| <span data-ttu-id="86904-119">Требование</span><span class="sxs-lookup"><span data-stu-id="86904-119">Requirement</span></span> | <span data-ttu-id="86904-120">Значение</span><span class="sxs-lookup"><span data-stu-id="86904-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="86904-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86904-121">Minimum supported client</span></span><br/> | <span data-ttu-id="86904-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86904-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="86904-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86904-123">Minimum supported server</span></span><br/> | <span data-ttu-id="86904-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86904-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="86904-125">Header</span><span class="sxs-lookup"><span data-stu-id="86904-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="86904-126"><dt>Адспроп. h</dt></span><span class="sxs-lookup"><span data-stu-id="86904-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86904-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86904-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86904-128">Сообщения в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="86904-128">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="86904-129">**адспропжетинитинфо**</span><span class="sxs-lookup"><span data-stu-id="86904-129">**ADsPropGetInitInfo**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[<span data-ttu-id="86904-130">**адспропинитпарамс**</span><span class="sxs-lookup"><span data-stu-id="86904-130">**ADSPROPINITPARAMS**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





