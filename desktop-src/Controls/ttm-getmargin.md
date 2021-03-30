---
title: Сообщение TTM_GETMARGIN (Коммктрл. h)
description: Извлекает верхнее, левое, нижнее и правое поля, заданные для окна подсказки. Поле — это расстояние (в пикселях) между границей окна подсказки и текстом, содержащимся в окне подсказки.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- Элементы управления Windows для TTM_GETMARGIN сообщений
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988676"
---
# <a name="ttm_getmargin-message"></a><span data-ttu-id="5decf-105">Сообщение ТТМи о \_ прибыли</span><span class="sxs-lookup"><span data-stu-id="5decf-105">TTM\_GETMARGIN message</span></span>

<span data-ttu-id="5decf-106">Извлекает верхнее, левое, нижнее и правое поля, заданные для окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="5decf-106">Retrieves the top, left, bottom, and right margins set for a tooltip window.</span></span> <span data-ttu-id="5decf-107">Поле — это расстояние (в пикселях) между границей окна подсказки и текстом, содержащимся в окне подсказки.</span><span class="sxs-lookup"><span data-stu-id="5decf-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="5decf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5decf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5decf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5decf-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5decf-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5decf-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5decf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5decf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5decf-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать сведения о полях.</span><span class="sxs-lookup"><span data-stu-id="5decf-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the margin information.</span></span> <span data-ttu-id="5decf-113">Элементы структуры **Rect** не определяют ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="5decf-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="5decf-114">Для этого сообщения члены структуры интерпретируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5decf-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="5decf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5decf-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="5decf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5decf-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="5decf-117"><dt>**Вверх**</dt></span><span class="sxs-lookup"><span data-stu-id="5decf-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="5decf-118">Расстояние между верхней границей и верхней частью текста подсказки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5decf-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="5decf-119"><dt>**слева**</dt></span><span class="sxs-lookup"><span data-stu-id="5decf-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="5decf-120">Расстояние между левой границей и левым концом текста подсказки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5decf-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="5decf-121"><dt>**Нижний**</dt></span><span class="sxs-lookup"><span data-stu-id="5decf-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="5decf-122">Расстояние между нижней границей и нижней частью текста подсказки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5decf-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="5decf-123"><dt>**Правильно**</dt></span><span class="sxs-lookup"><span data-stu-id="5decf-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="5decf-124">Расстояние между правой границей и правым концом текста подсказки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5decf-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5decf-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5decf-125">Return value</span></span>

<span data-ttu-id="5decf-126">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="5decf-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5decf-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5decf-127">Remarks</span></span>

<span data-ttu-id="5decf-128">При создании элемента управления ToolTip все четыре поля по умолчанию имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5decf-128">All four margins default to zero when you create the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5decf-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5decf-129">Requirements</span></span>



| <span data-ttu-id="5decf-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5decf-130">Requirement</span></span> | <span data-ttu-id="5decf-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5decf-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5decf-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5decf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5decf-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5decf-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5decf-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5decf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5decf-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5decf-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5decf-136">Header</span><span class="sxs-lookup"><span data-stu-id="5decf-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5decf-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5decf-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5decf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5decf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5decf-139">**ТТМ \_ сетмаргин**</span><span class="sxs-lookup"><span data-stu-id="5decf-139">**TTM\_SETMARGIN**</span></span>](ttm-setmargin.md)
</dt> </dl>

 

