---
title: Код уведомления NM_KEYDOWN (Toolbar) (Коммктрл. h)
description: Код уведомления NM_KEYDOWN (панель инструментов) — отправляется элементом управления, когда элемент управления имеет фокус клавиатуры и пользователь нажимает клавишу. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- Элементы управления Windows для кода уведомления NM_KEYDOWN (панель инструментов)
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d53818cf417e1efac686e94d3b4ef5919f819ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112362"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="099b1-105">\_Код уведомления NM (панель инструментов)</span><span class="sxs-lookup"><span data-stu-id="099b1-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="099b1-106">Посылается элементом управления, когда элемент управления имеет фокус клавиатуры и пользователь нажимает клавишу.</span><span class="sxs-lookup"><span data-stu-id="099b1-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="099b1-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="099b1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="099b1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="099b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="099b1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="099b1-110">Указатель на структуру [**нмкэй**](/windows/win32/api/commctrl/ns-commctrl-nmkey) , которая содержит дополнительные сведения о ключе, вызвавшем код уведомления.</span><span class="sxs-lookup"><span data-stu-id="099b1-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099b1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="099b1-111">Return value</span></span>

<span data-ttu-id="099b1-112">Возвращает ненулевое значение, чтобы элемент управления не обрабатывал ключ, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="099b1-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="099b1-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="099b1-113">Remarks</span></span>

<span data-ttu-id="099b1-114">В настоящее время этот код уведомления отправляется только элементом управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="099b1-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="099b1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="099b1-115">Requirements</span></span>



| <span data-ttu-id="099b1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="099b1-116">Requirement</span></span> | <span data-ttu-id="099b1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="099b1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="099b1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="099b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="099b1-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="099b1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="099b1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="099b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="099b1-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="099b1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="099b1-122">Header</span><span class="sxs-lookup"><span data-stu-id="099b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="099b1-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="099b1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





