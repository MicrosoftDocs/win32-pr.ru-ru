---
title: Код уведомления LVN_GETEMPTYMARKUP (Коммктрл. h)
description: Посылается элементом управления List-View родительскому окну, если элемент управления не имеет элементов. \_Код уведомления ЛВН жетемптимаркуп — это запрос родительского окна для предоставления текста разметки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892829"
---
# <a name="lvn_getemptymarkup-notification-code"></a><span data-ttu-id="fde3d-106">\_Код уведомления ЛВН жетемптимаркуп</span><span class="sxs-lookup"><span data-stu-id="fde3d-106">LVN\_GETEMPTYMARKUP notification code</span></span>

<span data-ttu-id="fde3d-107">Посылается элементом управления List-View родительскому окну, если элемент управления не имеет элементов.</span><span class="sxs-lookup"><span data-stu-id="fde3d-107">Sent by list-view control to its parent window when the control has no items.</span></span> <span data-ttu-id="fde3d-108">\_Код уведомления ЛВН жетемптимаркуп — это запрос родительского окна для предоставления текста разметки.</span><span class="sxs-lookup"><span data-stu-id="fde3d-108">The LVN\_GETEMPTYMARKUP notification code is a request for the parent window to provide markup text.</span></span> <span data-ttu-id="fde3d-109">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fde3d-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fde3d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fde3d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde3d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fde3d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fde3d-112">Указатель на структуру [**нмлвемптимаркуп**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="fde3d-112">Pointer to a [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="fde3d-113">Задайте элементы этой структуры, чтобы предоставить текст разметки для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="fde3d-113">Set the members of this structure to provide markup text for the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde3d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fde3d-114">Return value</span></span>

<span data-ttu-id="fde3d-115">Возвращает **значение true** , чтобы задать текст разметки в элементе управления "список", или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fde3d-115">Return **TRUE** to set the markup text in the list-view control, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde3d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fde3d-116">Remarks</span></span>

<span data-ttu-id="fde3d-117">Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвемптимаркуп**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="fde3d-117">The notification receiver casts *lParam* to retrieve the [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="fde3d-118">Параметр *wParam* содержит идентификатор элемента управления, который отправляет это сообщение.</span><span class="sxs-lookup"><span data-stu-id="fde3d-118">The *wParam* parameter contains the ID of the control that sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde3d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fde3d-119">Requirements</span></span>



| <span data-ttu-id="fde3d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fde3d-120">Requirement</span></span> | <span data-ttu-id="fde3d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fde3d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fde3d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fde3d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fde3d-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fde3d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fde3d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fde3d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fde3d-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fde3d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fde3d-126">Header</span><span class="sxs-lookup"><span data-stu-id="fde3d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde3d-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde3d-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





