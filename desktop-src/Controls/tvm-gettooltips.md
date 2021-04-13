---
title: Сообщение TVM_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для дочернего элемента управления ToolTip, используемого элементом управления "дерево-представление". Это сообщение можно отправить явным образом или с помощью \_ макроса TreeView.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- Элементы управления Windows для TVM_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489789"
---
# <a name="tvm_gettooltips-message"></a><span data-ttu-id="86c5b-105">Сообщение TVM с \_ ПОДсказками</span><span class="sxs-lookup"><span data-stu-id="86c5b-105">TVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="86c5b-106">Получает маркер для дочернего элемента управления ToolTip, используемого элементом управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="86c5b-106">Retrieves the handle to the child tooltip control used by a tree-view control.</span></span> <span data-ttu-id="86c5b-107">Это сообщение можно отправить явным образом или с помощью макроса [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="86c5b-107">You can send this message explicitly or by using the [**TreeView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="86c5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="86c5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c5b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86c5b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="86c5b-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="86c5b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="86c5b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86c5b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="86c5b-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="86c5b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c5b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86c5b-113">Return value</span></span>

<span data-ttu-id="86c5b-114">Возвращает указатель на дочерний элемент управления ToolTip или **значение NULL** , если элемент управления не использует подсказки.</span><span class="sxs-lookup"><span data-stu-id="86c5b-114">Returns the handle to the child tooltip control, or **NULL** if the control is not using tooltips.</span></span>

## <a name="remarks"></a><span data-ttu-id="86c5b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86c5b-115">Remarks</span></span>

<span data-ttu-id="86c5b-116">При создании элементы управления "представление в виде дерева" автоматически создают дочерний элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="86c5b-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="86c5b-117">Чтобы элемент управления "дерево" не использовал подсказки, создайте элемент управления с стилем " [**\_ подсказки" телевизоров**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="86c5b-117">To cause a tree-view control not to use tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c5b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="86c5b-118">Requirements</span></span>



| <span data-ttu-id="86c5b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="86c5b-119">Requirement</span></span> | <span data-ttu-id="86c5b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="86c5b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86c5b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86c5b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="86c5b-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86c5b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86c5b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86c5b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="86c5b-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="86c5b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86c5b-125">Header</span><span class="sxs-lookup"><span data-stu-id="86c5b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c5b-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="86c5b-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c5b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86c5b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c5b-128">**TVM \_ сеттултипс**</span><span class="sxs-lookup"><span data-stu-id="86c5b-128">**TVM\_SETTOOLTIPS**</span></span>](tvm-settooltips.md)
</dt> </dl>

 

 





