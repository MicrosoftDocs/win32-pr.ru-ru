---
title: Код уведомления TTN_SHOW (Коммктрл. h)
description: Сообщает окну-владельцу, что элемент управления ToolTip будет отображаться. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988723"
---
# <a name="ttn_show-notification-code"></a><span data-ttu-id="14dbe-105">ТТН \_ отобразить код уведомления</span><span class="sxs-lookup"><span data-stu-id="14dbe-105">TTN\_SHOW notification code</span></span>

<span data-ttu-id="14dbe-106">Сообщает окну-владельцу, что элемент управления ToolTip будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="14dbe-106">Notifies the owner window that a tooltip control is about to be displayed.</span></span> <span data-ttu-id="14dbe-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="14dbe-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="14dbe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14dbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14dbe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14dbe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14dbe-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="14dbe-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14dbe-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14dbe-111">Return value</span></span>

<span data-ttu-id="14dbe-112">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="14dbe-112">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="14dbe-113">Чтобы отобразить подсказку в расположении по умолчанию, возвратите ноль.</span><span class="sxs-lookup"><span data-stu-id="14dbe-113">To display the tooltip in its default location, return zero.</span></span> <span data-ttu-id="14dbe-114">Чтобы настроить расположение подсказки, переместите окно подсказки с помощью функции [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) и возвратите **значение true**.</span><span class="sxs-lookup"><span data-stu-id="14dbe-114">To customize the tooltip position, reposition the tooltip window with the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function and return **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="14dbe-115">Для версий более ранних, чем 4,70, возвращаемое значение отсутствует.</span><span class="sxs-lookup"><span data-stu-id="14dbe-115">For versions earlier than 4.70, there is no return value.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="14dbe-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14dbe-116">Remarks</span></span>

<span data-ttu-id="14dbe-117">Прямоугольник окна подсказки немного больше, чем его отображаемый прямоугольник, и его происхождение смещается вверх и влево.</span><span class="sxs-lookup"><span data-stu-id="14dbe-117">A tooltip window rectangle is somewhat larger than its text display rectangle, and its origin is offset up and to the left.</span></span> <span data-ttu-id="14dbe-118">Если нужно точно разместить текстовую рамку подсказки, сообщение [**ТТМ \_ аджустрект**](ttm-adjustrect.md) преобразует текстовый прямоугольник в соответствующий прямоугольник окна подсказки и наоборот.</span><span class="sxs-lookup"><span data-stu-id="14dbe-118">If you need to accurately position the text display rectangle of a tooltip, the [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message converts a text display rectangle into the corresponding tooltip window rectangle and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="14dbe-119">Требования</span><span class="sxs-lookup"><span data-stu-id="14dbe-119">Requirements</span></span>



| <span data-ttu-id="14dbe-120">Требование</span><span class="sxs-lookup"><span data-stu-id="14dbe-120">Requirement</span></span> | <span data-ttu-id="14dbe-121">Значение</span><span class="sxs-lookup"><span data-stu-id="14dbe-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14dbe-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14dbe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14dbe-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14dbe-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14dbe-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14dbe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14dbe-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14dbe-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14dbe-126">Header</span><span class="sxs-lookup"><span data-stu-id="14dbe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="14dbe-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="14dbe-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

