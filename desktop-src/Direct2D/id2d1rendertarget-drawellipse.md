---
title: Методы DrawEllipse ID2D1RenderTarget (D2d1. h)
description: Рисует контур эллипса с заданными размерами и обводкой.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Методы DrawEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685276"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a><span data-ttu-id="be5a9-104">ID2D1RenderTarget: методы:D Равеллипсе</span><span class="sxs-lookup"><span data-stu-id="be5a9-104">ID2D1RenderTarget::DrawEllipse methods</span></span>

<span data-ttu-id="be5a9-105">Рисует контур эллипса с заданными размерами и обводкой.</span><span class="sxs-lookup"><span data-stu-id="be5a9-105">Draws the outline of an ellipse with the specified dimensions and stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="be5a9-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="be5a9-106">Overload list</span></span>



| <span data-ttu-id="be5a9-107">Метод</span><span class="sxs-lookup"><span data-stu-id="be5a9-107">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="be5a9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="be5a9-108">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be5a9-109">[**DrawEllipse (D2D1 \_ ellipse&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="be5a9-109">[**DrawEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="be5a9-110">Рисует контур указанного эллипса с помощью указанного стиля Stroke.</span><span class="sxs-lookup"><span data-stu-id="be5a9-110">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |
| <span data-ttu-id="be5a9-111">[**DrawEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="be5a9-111">[**DrawEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="be5a9-112">Рисует контур указанного эллипса с помощью указанного стиля Stroke.</span><span class="sxs-lookup"><span data-stu-id="be5a9-112">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="be5a9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be5a9-113">Remarks</span></span>

<span data-ttu-id="be5a9-114">Метод **DrawEllipse** не возвращает код ошибки в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="be5a9-114">The **DrawEllipse** method doesn't return an error code if it fails.</span></span> <span data-ttu-id="be5a9-115">Чтобы определить, не завершилась ли операция рисования (например, **DrawEllipse**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="be5a9-115">To determine whether a drawing operation (such as **DrawEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="be5a9-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="be5a9-116">Examples</span></span>

<span data-ttu-id="be5a9-117">Пример см. в разделе [Рисование и заполнение базовой фигуры](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="be5a9-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be5a9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="be5a9-118">Requirements</span></span>



| <span data-ttu-id="be5a9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="be5a9-119">Requirement</span></span> | <span data-ttu-id="be5a9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="be5a9-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="be5a9-121">Header</span><span class="sxs-lookup"><span data-stu-id="be5a9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="be5a9-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="be5a9-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="be5a9-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be5a9-123">Library</span></span><br/> | <dl> <span data-ttu-id="be5a9-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be5a9-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="be5a9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="be5a9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="be5a9-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be5a9-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be5a9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be5a9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5a9-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="be5a9-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

<span data-ttu-id="be5a9-129">[**филлеллипсе**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="be5a9-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span></span>
</dt> </dl>

<span data-ttu-id="be5a9-130">�</span><span class="sxs-lookup"><span data-stu-id="be5a9-130">�</span></span>

<span data-ttu-id="be5a9-131">�</span><span class="sxs-lookup"><span data-stu-id="be5a9-131">�</span></span>
