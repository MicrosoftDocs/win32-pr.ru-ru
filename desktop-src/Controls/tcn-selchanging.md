---
title: Код уведомления TCN_SELCHANGING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления вкладки, что выбранная в данный момент вкладка будет изменена. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- TCN_SELCHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654407"
---
# <a name="tcn_selchanging-notification-code"></a><span data-ttu-id="9a22d-105">\_Код уведомления ТКН селчангинг</span><span class="sxs-lookup"><span data-stu-id="9a22d-105">TCN\_SELCHANGING notification code</span></span>

<span data-ttu-id="9a22d-106">Сообщает родительскому окну элемента управления вкладки, что выбранная в данный момент вкладка будет изменена.</span><span class="sxs-lookup"><span data-stu-id="9a22d-106">Notifies a tab control's parent window that the currently selected tab is about to change.</span></span> <span data-ttu-id="9a22d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9a22d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9a22d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a22d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a22d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a22d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a22d-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="9a22d-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a22d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a22d-111">Return value</span></span>

<span data-ttu-id="9a22d-112">Возвращает **значение true** , чтобы предотвратить изменение выбора, или **false** , чтобы разрешить изменение выбора.</span><span class="sxs-lookup"><span data-stu-id="9a22d-112">Returns **TRUE** to prevent the selection from changing, or **FALSE** to allow the selection to change.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a22d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a22d-113">Remarks</span></span>

<span data-ttu-id="9a22d-114">Чтобы определить текущую выбранную вкладку, используйте макрос [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="9a22d-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a22d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9a22d-115">Requirements</span></span>



| <span data-ttu-id="9a22d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9a22d-116">Requirement</span></span> | <span data-ttu-id="9a22d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9a22d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a22d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a22d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9a22d-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a22d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a22d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a22d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9a22d-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a22d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a22d-122">Header</span><span class="sxs-lookup"><span data-stu-id="9a22d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a22d-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a22d-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a22d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a22d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a22d-125">ТКН \_ селчанже</span><span class="sxs-lookup"><span data-stu-id="9a22d-125">TCN\_SELCHANGE</span></span>](tcn-selchange.md)
</dt> </dl>

 

 





