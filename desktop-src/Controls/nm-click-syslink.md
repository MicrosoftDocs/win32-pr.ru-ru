---
title: Код уведомления NM_CLICK (Syslink) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что пользователь щелкнул гиперссылку с левой кнопкой мыши внутри элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- Элементы управления Windows для кода уведомления NM_CLICK (Syslink)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137874"
---
# <a name="nm_click-syslink-notification-code"></a><span data-ttu-id="d62f5-105">\_Код уведомления Click (Syslink) NM</span><span class="sxs-lookup"><span data-stu-id="d62f5-105">NM\_CLICK (syslink) notification code</span></span>

<span data-ttu-id="d62f5-106">Сообщает родительскому окну элемента управления, что пользователь щелкнул гиперссылку с левой кнопкой мыши внутри элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d62f5-106">Notifies a control's parent window that the user has clicked a hyperlink with the left mouse button within the control.</span></span> <span data-ttu-id="d62f5-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d62f5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d62f5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d62f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d62f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d62f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d62f5-110">Указатель на структуру [**нмлинк**](/windows/win32/api/commctrl/ns-commctrl-nmlink) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="d62f5-110">Pointer to an [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d62f5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d62f5-111">Return value</span></span>

<span data-ttu-id="d62f5-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="d62f5-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d62f5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d62f5-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d62f5-114">Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="d62f5-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d62f5-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d62f5-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d62f5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d62f5-116">Requirements</span></span>



| <span data-ttu-id="d62f5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d62f5-117">Requirement</span></span> | <span data-ttu-id="d62f5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d62f5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d62f5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d62f5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d62f5-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d62f5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d62f5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d62f5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d62f5-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d62f5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d62f5-123">Header</span><span class="sxs-lookup"><span data-stu-id="d62f5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d62f5-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d62f5-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d62f5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d62f5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d62f5-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d62f5-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d62f5-127">**нмлинк**</span><span class="sxs-lookup"><span data-stu-id="d62f5-127">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[<span data-ttu-id="d62f5-128">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="d62f5-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





