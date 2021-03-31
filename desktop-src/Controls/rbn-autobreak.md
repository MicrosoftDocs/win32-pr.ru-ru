---
title: Сообщение RBN_AUTOBREAK (Коммктрл. h)
description: Уведомляет родительский элемент главной панели о том, что на панели появится разрыв. Родительский элемент определяет, следует ли сделать перерыв. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- Элементы управления Windows для RBN_AUTOBREAK сообщений
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892690"
---
# <a name="rbn_autobreak-message"></a><span data-ttu-id="e1cd0-106">\_Сообщение об АВТОразрыве РБН</span><span class="sxs-lookup"><span data-stu-id="e1cd0-106">RBN\_AUTOBREAK message</span></span>

<span data-ttu-id="e1cd0-107">Уведомляет родительский элемент [главной панели](rebar-controls.md) о том, что на панели появится разрыв.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-107">Notifies a [rebar's](rebar-controls.md) parent that a break will appear in the bar.</span></span> <span data-ttu-id="e1cd0-108">Родительский элемент определяет, следует ли сделать перерыв.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-108">The parent determines whether to make the break.</span></span> <span data-ttu-id="e1cd0-109">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e1cd0-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e1cd0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1cd0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1cd0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1cd0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1cd0-112">Указатель на структуру [**нмребараутобреак**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-112">Pointer to a [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1cd0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1cd0-113">Return value</span></span>

<span data-ttu-id="e1cd0-114">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1cd0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1cd0-115">Remarks</span></span>

<span data-ttu-id="e1cd0-116">Значение элемента **фаутобреак** структуры [**нмребараутобреак**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) указывает, должно ли в главной панели произойти прерывание.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-116">The value in the **fAutoBreak** member of the [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure indicates whether a break should occur in the rebar.</span></span>

<span data-ttu-id="e1cd0-117">Чтобы использовать этот код уведомления, укажите Comctl32.dll версии 6 в манифесте.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-117">To use this notification code, specify Comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="e1cd0-118">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e1cd0-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1cd0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e1cd0-119">Requirements</span></span>



| <span data-ttu-id="e1cd0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e1cd0-120">Requirement</span></span> | <span data-ttu-id="e1cd0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e1cd0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cd0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1cd0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1cd0-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1cd0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1cd0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1cd0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1cd0-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1cd0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1cd0-126">Header</span><span class="sxs-lookup"><span data-stu-id="e1cd0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1cd0-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1cd0-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





