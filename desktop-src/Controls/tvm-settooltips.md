---
title: Сообщение TVM_SETTOOLTIPS (Коммктрл. h)
description: Задает элемент управления дочерней подсказкой элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Сеттултипс TreeView.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- Элементы управления Windows для TVM_SETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135858"
---
# <a name="tvm_settooltips-message"></a><span data-ttu-id="b6701-105">\_Сообщение TVM сеттултипс</span><span class="sxs-lookup"><span data-stu-id="b6701-105">TVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="b6701-106">Задает элемент управления дочерней подсказкой элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="b6701-106">Sets a tree-view control's child tooltip control.</span></span> <span data-ttu-id="b6701-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сеттултипс TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="b6701-107">You can send this message explicitly or by using the [**TreeView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6701-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6701-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6701-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6701-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6701-110">Обработчик для элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b6701-110">Handle to a tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="b6701-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6701-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b6701-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b6701-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6701-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6701-113">Return value</span></span>

<span data-ttu-id="b6701-114">Возвращает маркер элемента управления ToolTip, установленный ранее для элемента управления "дерево-представление", или **значение NULL** , если подсказки ранее не использовались.</span><span class="sxs-lookup"><span data-stu-id="b6701-114">Returns the handle to tooltip control previously set for the tree-view control, or **NULL** if tooltips were not previously used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6701-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6701-115">Remarks</span></span>

<span data-ttu-id="b6701-116">При создании элементы управления "представление в виде дерева" автоматически создают дочерний элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b6701-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="b6701-117">Чтобы элемент управления "дерево" не использовал всплывающие подсказки, создайте элемент управления с стилем " [**\_ подсказки" телевизоров**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b6701-117">To prevent a tree-view control from using tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6701-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b6701-118">Requirements</span></span>



| <span data-ttu-id="b6701-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b6701-119">Requirement</span></span> | <span data-ttu-id="b6701-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b6701-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6701-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6701-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6701-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6701-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6701-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6701-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6701-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6701-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6701-125">Header</span><span class="sxs-lookup"><span data-stu-id="b6701-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6701-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6701-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6701-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6701-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6701-128">**TVM \_ подсказки**</span><span class="sxs-lookup"><span data-stu-id="b6701-128">**TVM\_GETTOOLTIPS**</span></span>](tvm-gettooltips.md)
</dt> </dl>

 

 





