---
title: Сообщение LVM_GETTOOLTIPS (Коммктрл. h)
description: Извлекает элемент управления ToolTip, используемый элементом управления "представление списка" для отображения всплывающих подсказок. Это сообщение можно отправить явным образом или воспользоваться \_ макросом ListView.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- Элементы управления Windows для LVM_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492402"
---
# <a name="lvm_gettooltips-message"></a><span data-ttu-id="b9ff9-105">Сообщение LVM с \_ ПОДсказками</span><span class="sxs-lookup"><span data-stu-id="b9ff9-105">LVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="b9ff9-106">Извлекает элемент управления ToolTip, используемый элементом управления "представление списка" для отображения всплывающих подсказок.</span><span class="sxs-lookup"><span data-stu-id="b9ff9-106">Retrieves the tooltip control that the list-view control uses to display tooltips.</span></span> <span data-ttu-id="b9ff9-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="b9ff9-107">You can send this message explicitly or use the [**ListView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9ff9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9ff9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ff9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9ff9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b9ff9-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b9ff9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b9ff9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9ff9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b9ff9-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b9ff9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ff9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9ff9-113">Return value</span></span>

<span data-ttu-id="b9ff9-114">Возвращает маркер элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b9ff9-114">Returns the handle of the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ff9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b9ff9-115">Requirements</span></span>



| <span data-ttu-id="b9ff9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b9ff9-116">Requirement</span></span> | <span data-ttu-id="b9ff9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b9ff9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ff9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9ff9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ff9-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9ff9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b9ff9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9ff9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ff9-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b9ff9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b9ff9-122">Header</span><span class="sxs-lookup"><span data-stu-id="b9ff9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9ff9-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff9-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ff9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9ff9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ff9-125">**LVM \_ сеттултипс**</span><span class="sxs-lookup"><span data-stu-id="b9ff9-125">**LVM\_SETTOOLTIPS**</span></span>](lvm-settooltips.md)
</dt> </dl>

 

 





