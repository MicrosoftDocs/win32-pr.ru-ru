---
title: Код уведомления NM_RCLICK (Toolbar) (Коммктрл. h)
description: Посылается элементом управления ToolBar, когда пользователь нажимает на панель инструментов правой кнопкой мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- Элементы управления Windows для кода уведомления NM_RCLICK (панель инструментов)
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6464c30a031aa55aef94bccd3ab852720fb14403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654723"
---
# <a name="nm_rclick-toolbar-notification-code"></a><span data-ttu-id="44247-105">\_Код уведомления "NM ркликк (панель инструментов)"</span><span class="sxs-lookup"><span data-stu-id="44247-105">NM\_RCLICK (toolbar) notification code</span></span>

<span data-ttu-id="44247-106">Посылается элементом управления ToolBar, когда пользователь нажимает на панель инструментов правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="44247-106">Sent by a toolbar control when the user clicks the toolbar with the right mouse button.</span></span> <span data-ttu-id="44247-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="44247-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="44247-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="44247-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44247-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44247-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44247-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="44247-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="44247-111">Если мышь была нажата на элементе панели инструментов, то элемент **двитемспек** содержит идентификатор элемента, а элемент **двитемдата** содержит данные элемента.</span><span class="sxs-lookup"><span data-stu-id="44247-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="44247-112">Если щелкнуть мышью разделитель или пробел на панели инструментов, элемент **двитемспек** будет содержать значение-1.</span><span class="sxs-lookup"><span data-stu-id="44247-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44247-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44247-113">Return value</span></span>

<span data-ttu-id="44247-114">Возвращает **значение false** , чтобы разрешить элементу управления ToolBar выполнять обработку события по умолчанию, или **значение true** , чтобы предотвратить обработку события элементом управления.</span><span class="sxs-lookup"><span data-stu-id="44247-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="44247-115">Требования</span><span class="sxs-lookup"><span data-stu-id="44247-115">Requirements</span></span>



| <span data-ttu-id="44247-116">Требование</span><span class="sxs-lookup"><span data-stu-id="44247-116">Requirement</span></span> | <span data-ttu-id="44247-117">Значение</span><span class="sxs-lookup"><span data-stu-id="44247-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44247-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44247-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44247-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44247-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44247-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44247-120">Minimum supported server</span></span><br/> | <span data-ttu-id="44247-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44247-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44247-122">Header</span><span class="sxs-lookup"><span data-stu-id="44247-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="44247-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="44247-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





