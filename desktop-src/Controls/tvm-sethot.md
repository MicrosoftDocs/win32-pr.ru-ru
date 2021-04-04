---
title: Сообщение TVM_SETHOT (Коммктрл. h)
description: Задает горячий элемент для элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Сесот TreeView.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- Элементы управления Windows для TVM_SETHOT сообщений
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989223"
---
# <a name="tvm_sethot-message"></a><span data-ttu-id="3c3a0-105">\_Сообщение TVM сесот</span><span class="sxs-lookup"><span data-stu-id="3c3a0-105">TVM\_SETHOT message</span></span>

<span data-ttu-id="3c3a0-106">\[Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="3c3a0-107">Это сообщение может не поддерживаться в будущих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c3a0-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="3c3a0-108">Задает горячий элемент для элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="3c3a0-108">Sets the hot item for a tree-view control.</span></span> <span data-ttu-id="3c3a0-109">Это сообщение можно отправить явно или с помощью макроса [**\_ сесот TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .</span><span class="sxs-lookup"><span data-stu-id="3c3a0-109">You can send this message explicitly or by using the [**TreeView\_SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c3a0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c3a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c3a0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c3a0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c3a0-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-112">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3c3a0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c3a0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c3a0-114">Обработчик нового горячего элемента.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-114">Handle to the new hot item.</span></span> <span data-ttu-id="3c3a0-115">Если это значение равно **null**, элемент управления "представление дерева" будет иметь значение без горячего элемента.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-115">If this value is **NULL**, the tree-view control will be set to have no hot item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c3a0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c3a0-116">Return value</span></span>

<span data-ttu-id="3c3a0-117">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="3c3a0-118">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="3c3a0-118">Security Considerations</span></span>

<span data-ttu-id="3c3a0-119">Использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c3a0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c3a0-120">Remarks</span></span>

<span data-ttu-id="3c3a0-121">*Горячий элемент* — это элемент, над которым наводится указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-121">The *hot item* is the item that the mouse is hovering over.</span></span> <span data-ttu-id="3c3a0-122">Это сообщение выглядит как «горячий элемент», даже если указатель мыши не наведен на него.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-122">This message makes an item look like it is the hot item even if the mouse is not hovering over it.</span></span>

<span data-ttu-id="3c3a0-123">Это сообщение не имеет видимого результата, если не задан стиль [**\_ траккселект телевизоров**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3c3a0-123">This message has no visible effect if the [**TVS\_TRACKSELECT**](tree-view-control-window-styles.md) style is not set.</span></span>

<span data-ttu-id="3c3a0-124">В случае успешности это сообщение вызывает перерисовку горячего элемента.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-124">If it succeeds, this message causes the hot item to be redrawn.</span></span>

<span data-ttu-id="3c3a0-125">Это сообщение пропускается, если *lParam* имеет **значение NULL** , а элемент управления "представление дерева" отслеживает мышь.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-125">This message is ignored if *lParam* is **NULL** and the tree-view control is tracking the mouse.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c3a0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3c3a0-126">Requirements</span></span>



| <span data-ttu-id="3c3a0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3c3a0-127">Requirement</span></span> | <span data-ttu-id="3c3a0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3c3a0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3a0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c3a0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3c3a0-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c3a0-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c3a0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c3a0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3c3a0-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c3a0-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c3a0-133">Header</span><span class="sxs-lookup"><span data-stu-id="3c3a0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c3a0-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c3a0-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c3a0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c3a0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3a0-136">**\_Сесот TreeView**</span><span class="sxs-lookup"><span data-stu-id="3c3a0-136">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





