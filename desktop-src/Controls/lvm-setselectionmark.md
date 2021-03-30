---
title: Сообщение LVM_SETSELECTIONMARK (Коммктрл. h)
description: Задает метку выделения в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Сетселектионмарк ListView.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- Элементы управления Windows для LVM_SETSELECTIONMARK сообщений
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801102"
---
# <a name="lvm_setselectionmark-message"></a><span data-ttu-id="027c6-105">\_Сообщение LVM сетселектионмарк</span><span class="sxs-lookup"><span data-stu-id="027c6-105">LVM\_SETSELECTIONMARK message</span></span>

<span data-ttu-id="027c6-106">Задает метку выделения в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="027c6-106">Sets the selection mark in a list-view control.</span></span> <span data-ttu-id="027c6-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетселектионмарк ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="027c6-107">You can send this message explicitly or use the [**ListView\_SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="027c6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="027c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="027c6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="027c6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="027c6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="027c6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="027c6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="027c6-112">Отсчитываемый от нуля индекс новой метки выделения.</span><span class="sxs-lookup"><span data-stu-id="027c6-112">Zero-based index of the new selection mark.</span></span> <span data-ttu-id="027c6-113">Если задано значение-1, отметка выделения удаляется.</span><span class="sxs-lookup"><span data-stu-id="027c6-113">If set to -1, the selection mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027c6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="027c6-114">Return value</span></span>

<span data-ttu-id="027c6-115">Возвращает предыдущую отметку выделения или-1, если Предыдущая метка выбора отсутствует.</span><span class="sxs-lookup"><span data-stu-id="027c6-115">Returns the previous selection mark, or -1 if there is no previous selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="027c6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="027c6-116">Remarks</span></span>

<span data-ttu-id="027c6-117">*Отметка выделения* — это индекс элемента, с которого начинается выбор нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="027c6-117">The *selection mark* is the item index from which a multiple selection starts.</span></span> <span data-ttu-id="027c6-118">Это сообщение не влияет на состояние выбора элемента.</span><span class="sxs-lookup"><span data-stu-id="027c6-118">This message does not affect the selection state of the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="027c6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="027c6-119">Requirements</span></span>



| <span data-ttu-id="027c6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="027c6-120">Requirement</span></span> | <span data-ttu-id="027c6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="027c6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="027c6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="027c6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="027c6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="027c6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="027c6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="027c6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="027c6-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="027c6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="027c6-126">Header</span><span class="sxs-lookup"><span data-stu-id="027c6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="027c6-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="027c6-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="027c6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="027c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027c6-129">**LVM \_ жетселектионмарк**</span><span class="sxs-lookup"><span data-stu-id="027c6-129">**LVM\_GETSELECTIONMARK**</span></span>](lvm-getselectionmark.md)
</dt> </dl>

 

 





