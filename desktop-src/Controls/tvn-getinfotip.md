---
title: Код уведомления TVN_GETINFOTIP (Коммктрл. h)
description: Посылается элементом управления "представление дерева", имеющим стиль подсказки "ТЕЛЕВИЗОРы" \_ . Этот код уведомления отправляется, когда элемент управления запрашивает дополнительную текстовую информацию для отображения в подсказке. Код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802842"
---
# <a name="tvn_getinfotip-notification-code"></a><span data-ttu-id="95b78-106">\_Код уведомления ТВН жетинфотип</span><span class="sxs-lookup"><span data-stu-id="95b78-106">TVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="95b78-107">Посылается элементом управления "представление дерева", имеющим стиль [**\_ подсказки "телевизоры**](tree-view-control-window-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="95b78-107">Sent by a tree-view control that has the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span> <span data-ttu-id="95b78-108">Этот код уведомления отправляется, когда элемент управления запрашивает дополнительную текстовую информацию для отображения в подсказке.</span><span class="sxs-lookup"><span data-stu-id="95b78-108">This notification code is sent when the control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="95b78-109">Код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="95b78-109">The notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a><span data-ttu-id="95b78-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="95b78-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b78-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95b78-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95b78-112">Указатель на структуру [**нмтвжетинфотип**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="95b78-112">Pointer to an [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b78-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95b78-113">Return value</span></span>

<span data-ttu-id="95b78-114">Элемент управления игнорирует возвращаемое значение для этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="95b78-114">The control ignores the return value for this notification code.</span></span>

## <a name="remarks"></a><span data-ttu-id="95b78-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95b78-115">Remarks</span></span>

<span data-ttu-id="95b78-116">Этот код уведомления отправляется только элементами управления "дерево", имеющим стиль [**\_ подсказки для телевизоров**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="95b78-116">This notification code is only sent by tree-view controls that have the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b78-117">Требования</span><span class="sxs-lookup"><span data-stu-id="95b78-117">Requirements</span></span>



| <span data-ttu-id="95b78-118">Требование</span><span class="sxs-lookup"><span data-stu-id="95b78-118">Requirement</span></span> | <span data-ttu-id="95b78-119">Значение</span><span class="sxs-lookup"><span data-stu-id="95b78-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95b78-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95b78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95b78-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95b78-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95b78-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95b78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95b78-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95b78-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95b78-124">Header</span><span class="sxs-lookup"><span data-stu-id="95b78-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95b78-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b78-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="95b78-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="95b78-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="95b78-127">**ТВН \_ ЖЕТИНФОТИПВ** (Юникод) и **ТВН \_ жетинфотипа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="95b78-127">**TVN\_GETINFOTIPW** (Unicode) and **TVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





