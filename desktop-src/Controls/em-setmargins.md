---
title: Сообщение EM_SETMARGINS (Winuser. h)
description: Задает ширину левого и правого полей для элемента управления "поле ввода". Сообщение перерисовывает элемент управления для отражения новых полей. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- Элементы управления Windows для EM_SETMARGINS сообщений
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988828"
---
# <a name="em_setmargins-message"></a><span data-ttu-id="1fd54-106">\_Сообщение СЕТМАРГИНС EM</span><span class="sxs-lookup"><span data-stu-id="1fd54-106">EM\_SETMARGINS message</span></span>

<span data-ttu-id="1fd54-107">Задает ширину левого и правого полей для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="1fd54-107">Sets the widths of the left and right margins for an edit control.</span></span> <span data-ttu-id="1fd54-108">Сообщение перерисовывает элемент управления для отражения новых полей.</span><span class="sxs-lookup"><span data-stu-id="1fd54-108">The message redraws the control to reflect the new margins.</span></span> <span data-ttu-id="1fd54-109">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1fd54-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1fd54-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1fd54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fd54-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fd54-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fd54-112">Поля, которые нужно задать.</span><span class="sxs-lookup"><span data-stu-id="1fd54-112">The margins to set.</span></span> <span data-ttu-id="1fd54-113">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1fd54-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1fd54-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1fd54-114">Value</span></span>                                                                                                                                                            | <span data-ttu-id="1fd54-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1fd54-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <span data-ttu-id="1fd54-116"><dt>**EC \_ LEFTMARGIN**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd54-116"><dt>**EC\_LEFTMARGIN**</dt></span></span> </dl>    | <span data-ttu-id="1fd54-117">Задает левое поле.</span><span class="sxs-lookup"><span data-stu-id="1fd54-117">Sets the left margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <span data-ttu-id="1fd54-118"><dt>**EC \_ RIGHTMARGIN**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd54-118"><dt>**EC\_RIGHTMARGIN**</dt></span></span> </dl> | <span data-ttu-id="1fd54-119">Задает правое поле.</span><span class="sxs-lookup"><span data-stu-id="1fd54-119">Sets the right margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <span data-ttu-id="1fd54-120"><dt>**EC \_ усефонтинфо**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd54-120"><dt>**EC\_USEFONTINFO**</dt></span></span> </dl> | <span data-ttu-id="1fd54-121">**Элементы управления Rich Edit:** Задает ширину левого и правого поля, вычисленную с использованием метрик текста текущего шрифта элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1fd54-121">**Rich edit controls:** Sets the left and right margins to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="1fd54-122">Если для элемента управления не задан шрифт, поля задаются равными нулю.</span><span class="sxs-lookup"><span data-stu-id="1fd54-122">If no font has been set for the control, the margins are set to zero.</span></span> <span data-ttu-id="1fd54-123">Параметр *lParam* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1fd54-123">The *lParam* parameter is ignored.</span></span> <br/> <span data-ttu-id="1fd54-124">**Изменить элементы управления:** Значение **EC \_ усефонтинфо** нельзя использовать в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1fd54-124">**Edit controls:** The **EC\_USEFONTINFO** value cannot be used in the *wParam* parameter.</span></span> <span data-ttu-id="1fd54-125">Его можно использовать только в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1fd54-125">It can only be used in the *lParam* parameter.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1fd54-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fd54-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fd54-127">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает новую ширину левого поля в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1fd54-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new width of the left margin, in pixels.</span></span> <span data-ttu-id="1fd54-128">Это значение игнорируется, если *wParam* не включает **EC \_ LEFTMARGIN**.</span><span class="sxs-lookup"><span data-stu-id="1fd54-128">This value is ignored if *wParam* does not include **EC\_LEFTMARGIN**.</span></span>

<span data-ttu-id="1fd54-129">**Изменение элементов управления и Расширенное редактирование 3,0 и более поздних версий:** [**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) может указать значение **EC \_ усефонтинфо** , чтобы задать для левого поля меньшую ширину, вычисленную с использованием метрик текста текущего шрифта элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1fd54-129">**Edit controls and Rich Edit 3.0 and later:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the left margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="1fd54-130">Если для элемента управления не задан шрифт, поле устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="1fd54-130">If no font has been set for the control, the margin is set to zero.</span></span>

<span data-ttu-id="1fd54-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает новую ширину правого поля в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1fd54-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new width of the right margin, in pixels.</span></span> <span data-ttu-id="1fd54-132">Это значение игнорируется, если *wParam* не включает **EC \_ RIGHTMARGIN**.</span><span class="sxs-lookup"><span data-stu-id="1fd54-132">This value is ignored if *wParam* does not include **EC\_RIGHTMARGIN**.</span></span>

<span data-ttu-id="1fd54-133">**Изменение элементов управления и Расширенное редактирование 3,0 и более поздних версий:** [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) может указать значение **EC \_ усефонтинфо** , чтобы задать для правого поля меньшую ширину, вычисленную с использованием метрик текста текущего шрифта элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1fd54-133">**Edit controls and Rich Edit 3.0 and later:** The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the right margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="1fd54-134">Если для элемента управления не задан шрифт, поле устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="1fd54-134">If no font has been set for the control, the margin is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fd54-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1fd54-135">Return value</span></span>

<span data-ttu-id="1fd54-136">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1fd54-136">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fd54-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fd54-137">Remarks</span></span>

<span data-ttu-id="1fd54-138">**Изменить элементы управления:** В параметре *wParam* нельзя использовать **EC \_ усефонтинфо** , но его можно использовать в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1fd54-138">**Edit controls:** You cannot use **EC\_USEFONTINFO** in the *wParam* parameter, but you can use it in the *lParam* parameter.</span></span>

<span data-ttu-id="1fd54-139">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1fd54-139">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1fd54-140">Все версии расширенного редактирования поддерживают использование **EC \_ усефонтинфо** в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1fd54-140">All rich edit versions support the use of **EC\_USEFONTINFO** in the *wParam* parameter.</span></span> <span data-ttu-id="1fd54-141">Однако в параметре *lParam* поддерживается использование **EC \_ Усефонтинфо** только в Microsoft Rich Edit 3,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1fd54-141">However, only Microsoft Rich Edit 3.0 and later support the use of **EC\_USEFONTINFO** in the *lParam* parameter.</span></span> <span data-ttu-id="1fd54-142">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1fd54-142">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd54-143">Требования</span><span class="sxs-lookup"><span data-stu-id="1fd54-143">Requirements</span></span>



| <span data-ttu-id="1fd54-144">Требование</span><span class="sxs-lookup"><span data-stu-id="1fd54-144">Requirement</span></span> | <span data-ttu-id="1fd54-145">Значение</span><span class="sxs-lookup"><span data-stu-id="1fd54-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd54-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fd54-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd54-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1fd54-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1fd54-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fd54-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd54-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fd54-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1fd54-150">Header</span><span class="sxs-lookup"><span data-stu-id="1fd54-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fd54-151"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fd54-151"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd54-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fd54-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd54-153">**длинные \_ поля EM**</span><span class="sxs-lookup"><span data-stu-id="1fd54-153">**EM\_GETMARGINS**</span></span>](em-getmargins.md)
</dt> </dl>

 

