---
title: Код уведомления NM_CLICK (Toolbar) (Коммктрл. h)
description: Посылается элементом управления ToolBar, когда пользователь щелкает элемент с левой кнопкой мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Элементы управления Windows для кода уведомления NM_CLICK (панель инструментов)
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
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892814"
---
# <a name="nm_click-toolbar-notification-code"></a><span data-ttu-id="a8c41-105">\_Код уведомления Click (панель инструментов)</span><span class="sxs-lookup"><span data-stu-id="a8c41-105">NM\_CLICK (toolbar) notification code</span></span>

<span data-ttu-id="a8c41-106">Посылается элементом управления ToolBar, когда пользователь щелкает элемент с левой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="a8c41-106">Sent by a toolbar control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="a8c41-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c41-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a8c41-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8c41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8c41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8c41-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="a8c41-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="a8c41-111">Элемент **двитемспек** содержит индекс раздела, который был выбран.</span><span class="sxs-lookup"><span data-stu-id="a8c41-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8c41-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8c41-112">Return value</span></span>

<span data-ttu-id="a8c41-113">Возвращает **значение true** , чтобы указать, что нажатие кнопки мыши было обработано, и подавить обработку по умолчанию системой.</span><span class="sxs-lookup"><span data-stu-id="a8c41-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="a8c41-114">Возвращает **значение false** , чтобы разрешить обработку по умолчанию щелчка.</span><span class="sxs-lookup"><span data-stu-id="a8c41-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8c41-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8c41-115">Remarks</span></span>

<span data-ttu-id="a8c41-116">Если щелкнуть элемент с левой кнопкой мыши, панель инструментов отправит [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) с [млрд доллным кодом \_](bn-clicked.md) уведомления в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="a8c41-116">Clicking an item with the left mouse button causes the toolbar to send a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with the [BN\_CLICKED](bn-clicked.md) notification code to the parent window.</span></span> <span data-ttu-id="a8c41-117">\_После **\_ командного сообщения WM** будет отправлено уведомление о НАЖАТии кнопки "nm".</span><span class="sxs-lookup"><span data-stu-id="a8c41-117">The NM\_CLICK notification is sent after the **WM\_COMMAND** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c41-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a8c41-118">Requirements</span></span>



| <span data-ttu-id="a8c41-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a8c41-119">Requirement</span></span> | <span data-ttu-id="a8c41-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a8c41-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c41-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8c41-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c41-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8c41-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8c41-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8c41-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c41-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8c41-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8c41-125">Header</span><span class="sxs-lookup"><span data-stu-id="a8c41-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8c41-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8c41-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

