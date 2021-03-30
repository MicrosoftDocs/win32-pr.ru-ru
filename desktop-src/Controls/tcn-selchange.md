---
title: Код уведомления TCN_SELCHANGE (Коммктрл. h)
description: Сообщает родительскому окну элемента управления вкладки, что выбранная в данный момент вкладка была изменена. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- TCN_SELCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801048"
---
# <a name="tcn_selchange-notification-code"></a><span data-ttu-id="e3f28-105">\_Код уведомления ТКН селчанже</span><span class="sxs-lookup"><span data-stu-id="e3f28-105">TCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="e3f28-106">Сообщает родительскому окну элемента управления вкладки, что выбранная в данный момент вкладка была изменена.</span><span class="sxs-lookup"><span data-stu-id="e3f28-106">Notifies a tab control's parent window that the currently selected tab has changed.</span></span> <span data-ttu-id="e3f28-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e3f28-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e3f28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3f28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3f28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3f28-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="e3f28-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f28-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3f28-111">Return value</span></span>

<span data-ttu-id="e3f28-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e3f28-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f28-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3f28-113">Remarks</span></span>

<span data-ttu-id="e3f28-114">Чтобы определить текущую выбранную вкладку, используйте макрос [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="e3f28-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f28-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e3f28-115">Requirements</span></span>



| <span data-ttu-id="e3f28-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e3f28-116">Requirement</span></span> | <span data-ttu-id="e3f28-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e3f28-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f28-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3f28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f28-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3f28-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3f28-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3f28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f28-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3f28-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3f28-122">Header</span><span class="sxs-lookup"><span data-stu-id="e3f28-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3f28-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f28-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f28-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3f28-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f28-125">ТКН \_ селчангинг</span><span class="sxs-lookup"><span data-stu-id="e3f28-125">TCN\_SELCHANGING</span></span>](tcn-selchanging.md)
</dt> </dl>

 

 





