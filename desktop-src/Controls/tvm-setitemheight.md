---
title: Сообщение TVM_SETITEMHEIGHT (Коммктрл. h)
description: Задает высоту элементов представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса Сетитемхеигхт TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- Элементы управления Windows для TVM_SETITEMHEIGHT сообщений
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988817"
---
# <a name="tvm_setitemheight-message"></a><span data-ttu-id="92546-105">\_Сообщение TVM сетитемхеигхт</span><span class="sxs-lookup"><span data-stu-id="92546-105">TVM\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="92546-106">Задает высоту элементов представления дерева.</span><span class="sxs-lookup"><span data-stu-id="92546-106">Sets the height of the tree-view items.</span></span> <span data-ttu-id="92546-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетитемхеигхт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .</span><span class="sxs-lookup"><span data-stu-id="92546-107">You can send this message explicitly or by using the [**TreeView\_SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="92546-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="92546-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92546-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92546-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92546-110">Новая высота каждого элемента в представлении в виде дерева (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="92546-110">New height of every item in the tree view, in pixels.</span></span> <span data-ttu-id="92546-111">Высота меньше 1 будет равна 1.</span><span class="sxs-lookup"><span data-stu-id="92546-111">Heights less than 1 will be set to 1.</span></span> <span data-ttu-id="92546-112">Если этот аргумент не является четным, а элемент управления "представление дерева" не имеет [**стиля \_ Ноневенхеигхт "телевизоры**](tree-view-control-window-styles.md) ", это значение округляется вниз до ближайшего четного значения.</span><span class="sxs-lookup"><span data-stu-id="92546-112">If this argument is not even and the tree-view control does not have the [**TVS\_NONEVENHEIGHT**](tree-view-control-window-styles.md) style, this value will be rounded down to the nearest even value.</span></span> <span data-ttu-id="92546-113">Если этот аргумент равен-1, элемент управления вернется к использованию высоты элемента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92546-113">If this argument is -1, the control will revert to using its default item height.</span></span>

</dd> <dt>

<span data-ttu-id="92546-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92546-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="92546-115">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="92546-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92546-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92546-116">Return value</span></span>

<span data-ttu-id="92546-117">Возвращает предыдущую высоту элементов в пикселях.</span><span class="sxs-lookup"><span data-stu-id="92546-117">Returns the previous height of the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="92546-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92546-118">Remarks</span></span>

<span data-ttu-id="92546-119">Элемент управления "представление дерева" использует это значение для высоты всех элементов.</span><span class="sxs-lookup"><span data-stu-id="92546-119">The tree-view control uses this value for the height of all items.</span></span> <span data-ttu-id="92546-120">Чтобы изменить высоту отдельных элементов, см. Описание элемента **иинтеграл** структуры [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="92546-120">To modify the height of individual items, see the description of the **iIntegral** member of the [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="92546-121">Требования</span><span class="sxs-lookup"><span data-stu-id="92546-121">Requirements</span></span>



| <span data-ttu-id="92546-122">Требование</span><span class="sxs-lookup"><span data-stu-id="92546-122">Requirement</span></span> | <span data-ttu-id="92546-123">Значение</span><span class="sxs-lookup"><span data-stu-id="92546-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92546-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92546-124">Minimum supported client</span></span><br/> | <span data-ttu-id="92546-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92546-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92546-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92546-126">Minimum supported server</span></span><br/> | <span data-ttu-id="92546-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92546-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92546-128">Header</span><span class="sxs-lookup"><span data-stu-id="92546-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="92546-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="92546-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92546-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92546-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92546-131">**TVM \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="92546-131">**TVM\_GETITEMHEIGHT**</span></span>](tvm-getitemheight.md)
</dt> </dl>

 

 





