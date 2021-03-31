---
title: Код уведомления TBN_DROPDOWN (Коммктрл. h)
description: Посылается элементом управления ToolBar, когда пользователь нажимает кнопку раскрывающегося списка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988470"
---
# <a name="tbn_dropdown-notification-code"></a><span data-ttu-id="9eab3-105">\_Код уведомления раскрывающегося списка ТБН</span><span class="sxs-lookup"><span data-stu-id="9eab3-105">TBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="9eab3-106">Посылается элементом управления ToolBar, когда пользователь нажимает кнопку раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="9eab3-106">Sent by a toolbar control when the user clicks a dropdown button.</span></span> <span data-ttu-id="9eab3-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9eab3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9eab3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9eab3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eab3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9eab3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9eab3-110">Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="9eab3-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="9eab3-111">Для этого кода уведомления допустимы только элементы **HDR** и **Член iItem** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="9eab3-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eab3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9eab3-112">Return value</span></span>

<span data-ttu-id="9eab3-113">Возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9eab3-113">Returns one of the following values:</span></span>



| <span data-ttu-id="9eab3-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9eab3-114">Return code</span></span>                                                                                          | <span data-ttu-id="9eab3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9eab3-115">Description</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9eab3-116"><dt>**ТБДДРЕТ \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="9eab3-116"><dt>**TBDDRET\_DEFAULT**</dt></span></span> </dl>      | <span data-ttu-id="9eab3-117">Раскрывающийся список был обработан.</span><span class="sxs-lookup"><span data-stu-id="9eab3-117">The drop-down was handled.</span></span><br/>                                             |
| <dl> <span data-ttu-id="9eab3-118"><dt>**ТБДДРЕТ \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="9eab3-118"><dt>**TBDDRET\_NODEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="9eab3-119">Раскрывающийся список не был обработан.</span><span class="sxs-lookup"><span data-stu-id="9eab3-119">The drop-down was not handled.</span></span><br/>                                         |
| <dl> <span data-ttu-id="9eab3-120"><dt>**ТБДДРЕТ \_ треатпрессед**</dt></span><span class="sxs-lookup"><span data-stu-id="9eab3-120"><dt>**TBDDRET\_TREATPRESSED**</dt></span></span> </dl> | <span data-ttu-id="9eab3-121">Раскрывающийся список был обработан, но рассматривает кнопку как обычную кнопку.</span><span class="sxs-lookup"><span data-stu-id="9eab3-121">The drop-down was handled, but treat the button like a regular button.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9eab3-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9eab3-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9eab3-123">Кнопки раскрывающегося списка могут быть простыми ([**\_ раскрывающийся список бтнс**](toolbar-control-and-button-styles.md) ), отображать стрелку рядом с изображением кнопки (стиль [**бтнс \_ вхоледропдовн**](toolbar-control-and-button-styles.md) ) или отображать стрелку, отделенную от изображения ([**тбстиле \_ \_ дравддарровс**](toolbar-extended-styles.md) Style).</span><span class="sxs-lookup"><span data-stu-id="9eab3-123">Dropdown buttons can be plain ([**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style), display an arrow next to the button image ([**BTNS\_WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style), or display an arrow that is separated from the image ([**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style).</span></span> <span data-ttu-id="9eab3-124">Если используется разделенная стрелка, \_ раскрывающийся список ТБН отправляется только в том случае, если пользователь нажимает на кнопку стрелку.</span><span class="sxs-lookup"><span data-stu-id="9eab3-124">If a separated arrow is used, TBN\_DROPDOWN is sent only if the user clicks the arrow portion of the button.</span></span> <span data-ttu-id="9eab3-125">Если пользователь нажимает на главную часть кнопки, отправляется сообщение [**\_ команды WM**](/windows/desktop/menurc/wm-command) с идентификатором кнопки, точно так же, как и стандартная кнопка.</span><span class="sxs-lookup"><span data-stu-id="9eab3-125">If the user clicks the main part of the button, a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with button's ID is sent, just as with a standard button.</span></span> <span data-ttu-id="9eab3-126">Для двух других стилей кнопки dropdown \_ раскрывающийся список ТБН отправляется, когда пользователь щелкает любую часть кнопки.</span><span class="sxs-lookup"><span data-stu-id="9eab3-126">For the other two styles of dropdown button, TBN\_DROPDOWN is sent when the user clicks any part of the button.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9eab3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9eab3-127">Requirements</span></span>



| <span data-ttu-id="9eab3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9eab3-128">Requirement</span></span> | <span data-ttu-id="9eab3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9eab3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9eab3-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9eab3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9eab3-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9eab3-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9eab3-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9eab3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9eab3-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9eab3-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9eab3-134">Header</span><span class="sxs-lookup"><span data-stu-id="9eab3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eab3-135"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eab3-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

