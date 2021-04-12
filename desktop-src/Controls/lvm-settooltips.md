---
title: Сообщение LVM_SETTOOLTIPS (Коммктрл. h)
description: Задает элемент управления ToolTip, который будет использоваться элементом управления "представление списка" для отображения всплывающих подсказок. Это сообщение можно отправить явным образом или использовать \_ макрос Сеттултипс ListView.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- Элементы управления Windows для LVM_SETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489966"
---
# <a name="lvm_settooltips-message"></a><span data-ttu-id="b6ab0-105">\_Сообщение LVM сеттултипс</span><span class="sxs-lookup"><span data-stu-id="b6ab0-105">LVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="b6ab0-106">Задает элемент управления ToolTip, который будет использоваться элементом управления "представление списка" для отображения всплывающих подсказок.</span><span class="sxs-lookup"><span data-stu-id="b6ab0-106">Sets the tooltip control that the list-view control will use to display tooltips.</span></span> <span data-ttu-id="b6ab0-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сеттултипс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="b6ab0-107">You can send this message explicitly or use the [**ListView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6ab0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6ab0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ab0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6ab0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b6ab0-110">Обрабатываемый элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b6ab0-110">Handle to the tooltip control to be set.</span></span></dd> <dt>

<span data-ttu-id="b6ab0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6ab0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6ab0-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b6ab0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6ab0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6ab0-113">Return value</span></span>

<span data-ttu-id="b6ab0-114">Возвращает маркер предыдущего элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b6ab0-114">Returns the handle to the previous tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ab0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b6ab0-115">Requirements</span></span>



| <span data-ttu-id="b6ab0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b6ab0-116">Requirement</span></span> | <span data-ttu-id="b6ab0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b6ab0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ab0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6ab0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ab0-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6ab0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6ab0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6ab0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ab0-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6ab0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6ab0-122">Header</span><span class="sxs-lookup"><span data-stu-id="b6ab0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6ab0-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab0-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ab0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6ab0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ab0-125">**LVM \_ подсказки**</span><span class="sxs-lookup"><span data-stu-id="b6ab0-125">**LVM\_GETTOOLTIPS**</span></span>](lvm-gettooltips.md)
</dt> </dl>

 

 





