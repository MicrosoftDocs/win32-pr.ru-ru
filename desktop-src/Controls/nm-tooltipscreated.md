---
title: Код уведомления NM_TOOLTIPSCREATED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что элемент управления создал элемент управления ToolTip. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- NM_TOOLTIPSCREATED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071451"
---
# <a name="nm_tooltipscreated-notification-code"></a><span data-ttu-id="d4970-105">\_Код уведомления тултипскреатед (NM)</span><span class="sxs-lookup"><span data-stu-id="d4970-105">NM\_TOOLTIPSCREATED notification code</span></span>

<span data-ttu-id="d4970-106">Сообщает родительскому окну элемента управления, что элемент управления создал элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d4970-106">Notifies a control's parent window that the control has created a tooltip control.</span></span> <span data-ttu-id="d4970-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d4970-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d4970-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4970-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4970-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4970-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4970-110">Указатель на структуру [**нмтултипскреатед**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="d4970-110">A pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4970-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4970-111">Return value</span></span>

<span data-ttu-id="d4970-112">Если не указано иное, элемент управления игнорирует возвращаемое значение из этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="d4970-112">Unless otherwise specified, the control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4970-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d4970-113">Requirements</span></span>



| <span data-ttu-id="d4970-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d4970-114">Requirement</span></span> | <span data-ttu-id="d4970-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d4970-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4970-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4970-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d4970-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4970-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4970-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4970-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d4970-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4970-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4970-120">Header</span><span class="sxs-lookup"><span data-stu-id="d4970-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4970-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4970-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





