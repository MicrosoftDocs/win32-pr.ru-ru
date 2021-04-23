---
title: Код уведомления NM_CLICK (TAB) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Вкладка", что пользователь щелкнул левой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b892aded-d6b8-4a04-bfdd-0153b65eaccc
keywords:
- Элементы управления Windows для кода уведомления NM_CLICK (TAB)
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
ms.openlocfilehash: e451a7a87d1b02140f59797c7485b8eb250dad13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137871"
---
# <a name="nm_click-tab-notification-code"></a><span data-ttu-id="a14bd-105">\_Код уведомления Click (TAB) NM</span><span class="sxs-lookup"><span data-stu-id="a14bd-105">NM\_CLICK (tab) notification code</span></span>

<span data-ttu-id="a14bd-106">Сообщает родительскому окну элемента управления "Вкладка", что пользователь щелкнул левой кнопкой мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="a14bd-106">Notifies the parent window of a tab control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="a14bd-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a14bd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a14bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a14bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a14bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a14bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a14bd-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="a14bd-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a14bd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a14bd-111">Return value</span></span>

<span data-ttu-id="a14bd-112">Возвращаемое значение игнорируется элементом управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="a14bd-112">The return value is ignored by the tab control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14bd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a14bd-113">Requirements</span></span>



| <span data-ttu-id="a14bd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a14bd-114">Requirement</span></span> | <span data-ttu-id="a14bd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a14bd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a14bd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a14bd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a14bd-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a14bd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a14bd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a14bd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a14bd-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a14bd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a14bd-120">Header</span><span class="sxs-lookup"><span data-stu-id="a14bd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a14bd-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a14bd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





