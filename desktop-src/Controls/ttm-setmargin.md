---
title: Сообщение TTM_SETMARGIN (Коммктрл. h)
description: Задает верхнее, левое, нижнее и правое поля для окна подсказки. Поле — это расстояние (в пикселях) между границей окна подсказки и текстом, содержащимся в окне подсказки.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- Элементы управления Windows для TTM_SETMARGIN сообщений
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654499"
---
# <a name="ttm_setmargin-message"></a><span data-ttu-id="48f80-105">\_Сообщение ТТМ сетмаргин</span><span class="sxs-lookup"><span data-stu-id="48f80-105">TTM\_SETMARGIN message</span></span>

<span data-ttu-id="48f80-106">Задает верхнее, левое, нижнее и правое поля для окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="48f80-106">Sets the top, left, bottom, and right margins for a tooltip window.</span></span> <span data-ttu-id="48f80-107">Поле — это расстояние (в пикселях) между границей окна подсказки и текстом, содержащимся в окне подсказки.</span><span class="sxs-lookup"><span data-stu-id="48f80-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="48f80-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="48f80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f80-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48f80-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="48f80-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="48f80-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="48f80-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48f80-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48f80-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую сведения о полях, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="48f80-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margin information to be set.</span></span> <span data-ttu-id="48f80-113">Элементы структуры **Rect** не определяют ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="48f80-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="48f80-114">Для этого сообщения члены структуры интерпретируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="48f80-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="48f80-115">Значение</span><span class="sxs-lookup"><span data-stu-id="48f80-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="48f80-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48f80-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="48f80-117"><dt>**Вверх**</dt></span><span class="sxs-lookup"><span data-stu-id="48f80-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="48f80-118">Расстояние между верхней границей и верхней частью текста подсказки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="48f80-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="48f80-119"><dt>**слева**</dt></span><span class="sxs-lookup"><span data-stu-id="48f80-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="48f80-120">Расстояние между левой границей и левым концом текста подсказки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="48f80-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="48f80-121"><dt>**Нижний**</dt></span><span class="sxs-lookup"><span data-stu-id="48f80-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="48f80-122">Расстояние между нижней границей и нижней частью текста подсказки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="48f80-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="48f80-123"><dt>**Правильно**</dt></span><span class="sxs-lookup"><span data-stu-id="48f80-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="48f80-124">Расстояние между правой границей и правым концом текста подсказки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="48f80-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48f80-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48f80-125">Return value</span></span>

<span data-ttu-id="48f80-126">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="48f80-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="48f80-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48f80-127">Remarks</span></span>

<span data-ttu-id="48f80-128">Это сообщение не действует, если приложение работает в Windows Vista и для подсказки включены визуальные стили.</span><span class="sxs-lookup"><span data-stu-id="48f80-128">This message has no effect when the application runs on Windows Vista and visual styles are enabled for the tooltip.</span></span> <span data-ttu-id="48f80-129">Вы можете отключить визуальные стили для подсказки с помощью [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span><span class="sxs-lookup"><span data-stu-id="48f80-129">You can disable visual styles for the tooltip by using [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span></span>

## <a name="requirements"></a><span data-ttu-id="48f80-130">Требования</span><span class="sxs-lookup"><span data-stu-id="48f80-130">Requirements</span></span>



| <span data-ttu-id="48f80-131">Требование</span><span class="sxs-lookup"><span data-stu-id="48f80-131">Requirement</span></span> | <span data-ttu-id="48f80-132">Значение</span><span class="sxs-lookup"><span data-stu-id="48f80-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48f80-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48f80-133">Minimum supported client</span></span><br/> | <span data-ttu-id="48f80-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48f80-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48f80-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48f80-135">Minimum supported server</span></span><br/> | <span data-ttu-id="48f80-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48f80-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48f80-137">Header</span><span class="sxs-lookup"><span data-stu-id="48f80-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="48f80-138"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f80-138"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f80-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48f80-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f80-140">**ТТМ \_ прибыль**</span><span class="sxs-lookup"><span data-stu-id="48f80-140">**TTM\_GETMARGIN**</span></span>](ttm-getmargin.md)
</dt> </dl>

 

