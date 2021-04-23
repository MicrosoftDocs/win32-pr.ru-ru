---
title: Код уведомления NM_LDOWN (Toolbar) (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что была нажата левая кнопка мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- Элементы управления Windows для кода уведомления NM_LDOWN (панель инструментов)
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60f1f05d85aa8885acf31a36098056d68612ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891418"
---
# <a name="nm_ldown-toolbar-notification-code"></a><span data-ttu-id="d3ca4-105">\_Код уведомления "NM лдовн (панель инструментов)"</span><span class="sxs-lookup"><span data-stu-id="d3ca4-105">NM\_LDOWN (toolbar) notification code</span></span>

<span data-ttu-id="d3ca4-106">Сообщает родительскому окну панели инструментов, что была нажата левая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-106">Notifies a toolbar's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="d3ca4-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ca4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d3ca4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3ca4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ca4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3ca4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3ca4-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="d3ca4-111">Если мышь была нажата на элементе панели инструментов, то элемент **двитемспек** содержит идентификатор элемента, а элемент **двитемдата** содержит данные элемента.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="d3ca4-112">Если щелкнуть мышью разделитель или пробел на панели инструментов, элемент **двитемспек** будет содержать значение-1.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ca4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3ca4-113">Return value</span></span>

<span data-ttu-id="d3ca4-114">Возвращает **значение false** , чтобы разрешить элементу управления ToolBar выполнять обработку события по умолчанию, или **значение true** , чтобы предотвратить обработку события элементом управления.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ca4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3ca4-115">Remarks</span></span>

<span data-ttu-id="d3ca4-116">Это уведомление отправляется после отправки кода уведомления [ \_ раскрывающегося списка ТБН](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ca4-116">This notification is sent after the [TBN\_DROPDOWN](tbn-dropdown.md) notification code has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ca4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d3ca4-117">Requirements</span></span>



| <span data-ttu-id="d3ca4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d3ca4-118">Requirement</span></span> | <span data-ttu-id="d3ca4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d3ca4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ca4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3ca4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ca4-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3ca4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3ca4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3ca4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ca4-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3ca4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3ca4-124">Header</span><span class="sxs-lookup"><span data-stu-id="d3ca4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ca4-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ca4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





