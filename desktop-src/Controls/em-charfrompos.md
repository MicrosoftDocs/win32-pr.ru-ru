---
title: Сообщение EM_CHARFROMPOS (Winuser. h)
description: Получает сведения о символе, ближайшее к заданной точке в клиентской области элемента управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- Элементы управления Windows для EM_CHARFROMPOS сообщений
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491499"
---
# <a name="em_charfrompos-message"></a><span data-ttu-id="e27dd-105">\_Сообщение ЧАРФРОМПОС EM</span><span class="sxs-lookup"><span data-stu-id="e27dd-105">EM\_CHARFROMPOS message</span></span>

<span data-ttu-id="e27dd-106">Получает сведения о символе, ближайшее к заданной точке в клиентской области элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e27dd-106">Gets information about the character closest to a specified point in the client area of an edit control.</span></span> <span data-ttu-id="e27dd-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="e27dd-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e27dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e27dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e27dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e27dd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e27dd-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="e27dd-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e27dd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e27dd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e27dd-112">Координаты точки в клиентской области элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e27dd-112">The coordinates of a point in the control's client area.</span></span> <span data-ttu-id="e27dd-113">Координаты находятся в единицах экрана и задаются относительно левого верхнего угла клиентской области элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e27dd-113">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="e27dd-114">**Элементы управления Rich Edit:** Указатель на [**точку**](/previous-versions//dd162807(v=vs.85)) , которая содержит координаты горизонтальной и вертикальной структуры.</span><span class="sxs-lookup"><span data-stu-id="e27dd-114">**Rich edit controls:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that contains the horizontal and vertical coordinates.</span></span>

<span data-ttu-id="e27dd-115">**Изменить элементы управления:** [**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит горизонтальную координату.</span><span class="sxs-lookup"><span data-stu-id="e27dd-115">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate.</span></span> <span data-ttu-id="e27dd-116">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит вертикальную координату.</span><span class="sxs-lookup"><span data-stu-id="e27dd-116">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e27dd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e27dd-117">Return value</span></span>

<span data-ttu-id="e27dd-118">**Элементы управления Rich Edit:** Возвращаемое значение указывает Отсчитываемый от нуля индекс символа, расположенный ближе к указанной точке.</span><span class="sxs-lookup"><span data-stu-id="e27dd-118">**Rich edit controls:** The return value specifies the zero-based character index of the character nearest the specified point.</span></span> <span data-ttu-id="e27dd-119">Возвращаемое значение указывает последний символ в элементе управления "поле ввода", если указанная точка находится за последним символом в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="e27dd-119">The return value indicates the last character in the edit control if the specified point is beyond the last character in the control.</span></span>

<span data-ttu-id="e27dd-120">**Изменить элементы управления:** [**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) Указывает отсчитываемый от нуля индекс символа, ближайшего к указанной точке.</span><span class="sxs-lookup"><span data-stu-id="e27dd-120">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the character nearest the specified point.</span></span> <span data-ttu-id="e27dd-121">Этот индекс задается относительно начала элемента управления, а не от начала строки.</span><span class="sxs-lookup"><span data-stu-id="e27dd-121">This index is relative to the beginning of the control, not the beginning of the line.</span></span> <span data-ttu-id="e27dd-122">Если указанная точка находится за последним символом в элементе управления "поле ввода", возвращаемое значение обозначает последний символ в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="e27dd-122">If the specified point is beyond the last character in the edit control, the return value indicates the last character in the control.</span></span> <span data-ttu-id="e27dd-123">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Указывает отсчитываемый от нуля индекс строки, содержащей символ.</span><span class="sxs-lookup"><span data-stu-id="e27dd-123">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the line that contains the character.</span></span> <span data-ttu-id="e27dd-124">Для однострочных элементов управления редактирования это значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e27dd-124">For single-line edit controls, this value is zero.</span></span> <span data-ttu-id="e27dd-125">Индекс указывает разделитель строк, если указанная точка выходит за пределы последнего видимого символа в строке.</span><span class="sxs-lookup"><span data-stu-id="e27dd-125">The index indicates the line delimiter if the specified point is beyond the last visible character in a line.</span></span>

## <a name="remarks"></a><span data-ttu-id="e27dd-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e27dd-126">Remarks</span></span>

<span data-ttu-id="e27dd-127">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e27dd-127">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e27dd-128">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e27dd-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="e27dd-129">Если точка передается в **EM \_ Чарфромпос** как *lParam* , а точка находится вне границ элемента управления "поле ввода", то *lResult* имеет значение (65535, 65535).</span><span class="sxs-lookup"><span data-stu-id="e27dd-129">If a point is passed to **EM\_CHARFROMPOS** as the *lParam* and the point is outside the bounds of the edit control, then the *lResult* is (65535, 65535).</span></span>

## <a name="requirements"></a><span data-ttu-id="e27dd-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e27dd-130">Requirements</span></span>



| <span data-ttu-id="e27dd-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e27dd-131">Requirement</span></span> | <span data-ttu-id="e27dd-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e27dd-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e27dd-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e27dd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e27dd-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e27dd-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e27dd-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e27dd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e27dd-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e27dd-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e27dd-137">Header</span><span class="sxs-lookup"><span data-stu-id="e27dd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e27dd-138"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e27dd-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e27dd-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e27dd-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="e27dd-140">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e27dd-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e27dd-141">**EM \_ посфромчар**</span><span class="sxs-lookup"><span data-stu-id="e27dd-141">**EM\_POSFROMCHAR**</span></span>](em-posfromchar.md)
</dt> <dt>

<span data-ttu-id="e27dd-142">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e27dd-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e27dd-143">**макелпарам**</span><span class="sxs-lookup"><span data-stu-id="e27dd-143">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

<span data-ttu-id="e27dd-144">[**Точка зрения**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e27dd-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

