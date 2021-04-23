---
title: Сообщение BM_SETSTATE (Winuser. h)
description: Задает состояние выделения для кнопки. Состояние выделения указывает, будет ли кнопка выделена, как будто пользователь отправил ее. Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки SetState.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- Элементы управления Windows для BM_SETSTATE сообщений
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654453"
---
# <a name="bm_setstate-message"></a><span data-ttu-id="195a3-106">\_Сообщение BM SETSTATE</span><span class="sxs-lookup"><span data-stu-id="195a3-106">BM\_SETSTATE message</span></span>

<span data-ttu-id="195a3-107">Задает состояние выделения для кнопки.</span><span class="sxs-lookup"><span data-stu-id="195a3-107">Sets the highlight state of a button.</span></span> <span data-ttu-id="195a3-108">Состояние выделения указывает, будет ли кнопка выделена, как будто пользователь отправил ее.</span><span class="sxs-lookup"><span data-stu-id="195a3-108">The highlight state indicates whether the button is highlighted as if the user had pushed it.</span></span> <span data-ttu-id="195a3-109">Это сообщение можно отправить явным образом или воспользоваться макросом [**кнопки \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .</span><span class="sxs-lookup"><span data-stu-id="195a3-109">You can send this message explicitly or use the [**Button\_SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="195a3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="195a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="195a3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="195a3-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="195a3-112">**Логическое** значение, указывающее, выделяется ли кнопка.</span><span class="sxs-lookup"><span data-stu-id="195a3-112">A **BOOL** that specifies whether the button is highlighted.</span></span> <span data-ttu-id="195a3-113">Значение **true** выделяет кнопку.</span><span class="sxs-lookup"><span data-stu-id="195a3-113">A value of **TRUE** highlights the button.</span></span> <span data-ttu-id="195a3-114">Значение **false** удаляет все выделения.</span><span class="sxs-lookup"><span data-stu-id="195a3-114">A value of **FALSE** removes any highlighting.</span></span>

</dd> <dt>

<span data-ttu-id="195a3-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="195a3-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="195a3-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="195a3-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="195a3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="195a3-117">Return value</span></span>

<span data-ttu-id="195a3-118">Это сообщение всегда возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="195a3-118">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="195a3-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="195a3-119">Remarks</span></span>

<span data-ttu-id="195a3-120">Выделение влияет только на внешний вид кнопки.</span><span class="sxs-lookup"><span data-stu-id="195a3-120">Highlighting affects only the appearance of a button.</span></span> <span data-ttu-id="195a3-121">Он не влияет на состояние флажка переключателя или на флажок.</span><span class="sxs-lookup"><span data-stu-id="195a3-121">It has no effect on the check state of a radio button or check box.</span></span>

<span data-ttu-id="195a3-122">Кнопка автоматически выделяется, когда пользователь наводит на нее курсор и нажимает и удерживает левую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="195a3-122">A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button.</span></span> <span data-ttu-id="195a3-123">Выделение удаляется, когда пользователь отпускает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="195a3-123">The highlighting is removed when the user releases the mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="195a3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="195a3-124">Requirements</span></span>



| <span data-ttu-id="195a3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="195a3-125">Requirement</span></span> | <span data-ttu-id="195a3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="195a3-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="195a3-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="195a3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="195a3-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="195a3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="195a3-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="195a3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="195a3-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="195a3-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="195a3-131">Header</span><span class="sxs-lookup"><span data-stu-id="195a3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="195a3-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="195a3-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="195a3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="195a3-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="195a3-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="195a3-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="195a3-135">**BM \_**</span><span class="sxs-lookup"><span data-stu-id="195a3-135">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="195a3-136">**BM \_ сетчекк**</span><span class="sxs-lookup"><span data-stu-id="195a3-136">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





