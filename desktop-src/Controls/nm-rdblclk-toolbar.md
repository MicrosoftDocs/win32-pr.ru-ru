---
title: Код уведомления NM_RDBLCLK (Toolbar) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что пользователь дважды щелкнул правой кнопкой мыши внутри элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- Элементы управления Windows для кода уведомления NM_RDBLCLK (панель инструментов)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492147"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a><span data-ttu-id="c9a28-105">\_Код уведомления "NM рдблклк (панель инструментов)"</span><span class="sxs-lookup"><span data-stu-id="c9a28-105">NM\_RDBLCLK (toolbar) notification code</span></span>

<span data-ttu-id="c9a28-106">Сообщает родительскому окну элемента управления, что пользователь дважды щелкнул правой кнопкой мыши внутри элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c9a28-106">Notifies a control's parent window that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="c9a28-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c9a28-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c9a28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9a28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9a28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9a28-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a28-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="c9a28-111">Если мышь была нажата на элементе панели инструментов, то элемент **двитемспек** содержит идентификатор элемента, а элемент **двитемдата** содержит данные элемента.</span><span class="sxs-lookup"><span data-stu-id="c9a28-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="c9a28-112">Если щелкнуть мышью разделитель или пробел на панели инструментов, элемент **двитемспек** будет содержать значение-1.</span><span class="sxs-lookup"><span data-stu-id="c9a28-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a28-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9a28-113">Return value</span></span>

<span data-ttu-id="c9a28-114">Возвращает **значение false** , чтобы разрешить элементу управления ToolBar выполнять обработку события по умолчанию, или **значение true** , чтобы предотвратить обработку события элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c9a28-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a28-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c9a28-115">Requirements</span></span>



| <span data-ttu-id="c9a28-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c9a28-116">Requirement</span></span> | <span data-ttu-id="c9a28-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c9a28-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a28-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9a28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a28-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9a28-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9a28-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9a28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a28-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9a28-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9a28-122">Header</span><span class="sxs-lookup"><span data-stu-id="c9a28-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9a28-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a28-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





