---
title: Методы Филлеллипсе ID2D1RenderTarget (D2d1. h)
description: Закрашивает внутреннюю часть указанного эллипса.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- Методы Филлеллипсе Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685169"
---
# <a name="id2d1rendertargetfillellipse-methods"></a><span data-ttu-id="b5de0-104">Методы ID2D1RenderTarget:: Филлеллипсе</span><span class="sxs-lookup"><span data-stu-id="b5de0-104">ID2D1RenderTarget::FillEllipse methods</span></span>

<span data-ttu-id="b5de0-105">Закрашивает внутреннюю часть указанного эллипса.</span><span class="sxs-lookup"><span data-stu-id="b5de0-105">Paints the interior of the specified ellipse.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b5de0-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="b5de0-106">Overload list</span></span>



| <span data-ttu-id="b5de0-107">Метод</span><span class="sxs-lookup"><span data-stu-id="b5de0-107">Method</span></span>                                                                                                             | <span data-ttu-id="b5de0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b5de0-108">Description</span></span>                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span data-ttu-id="b5de0-109">[**Филлеллипсе (D2D1 \_ ellipse&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="b5de0-109">[**FillEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span>  | <span data-ttu-id="b5de0-110">Закрашивает внутреннюю часть указанного эллипса.</span><span class="sxs-lookup"><span data-stu-id="b5de0-110">Paints the interior of the specified ellipse.</span></span> <br/> |
| <span data-ttu-id="b5de0-111">[**Филлеллипсе (D2D1 \_ Ellipse \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="b5de0-111">[**FillEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span> | <span data-ttu-id="b5de0-112">Закрашивает внутреннюю часть указанного эллипса.</span><span class="sxs-lookup"><span data-stu-id="b5de0-112">Paints the interior of the specified ellipse.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="b5de0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5de0-113">Remarks</span></span>

<span data-ttu-id="b5de0-114">Этот метод не возвращает код ошибки в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="b5de0-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="b5de0-115">Чтобы определить, не завершилась ли операция рисования (например, **филлеллипсе**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="b5de0-115">To determine whether a drawing operation (such as **FillEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="b5de0-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="b5de0-116">Examples</span></span>

<span data-ttu-id="b5de0-117">Пример см. в разделе [Рисование и заполнение базовой фигуры](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="b5de0-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5de0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b5de0-118">Requirements</span></span>



| <span data-ttu-id="b5de0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b5de0-119">Requirement</span></span> | <span data-ttu-id="b5de0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b5de0-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5de0-121">Header</span><span class="sxs-lookup"><span data-stu-id="b5de0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b5de0-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5de0-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5de0-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5de0-123">Library</span></span><br/> | <dl> <span data-ttu-id="b5de0-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5de0-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5de0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b5de0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5de0-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5de0-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5de0-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5de0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5de0-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="b5de0-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="b5de0-129">Рисование и заполнение базовой фигуры</span><span class="sxs-lookup"><span data-stu-id="b5de0-129">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="b5de0-130">�</span><span class="sxs-lookup"><span data-stu-id="b5de0-130">�</span></span>

<span data-ttu-id="b5de0-131">�</span><span class="sxs-lookup"><span data-stu-id="b5de0-131">�</span></span>
