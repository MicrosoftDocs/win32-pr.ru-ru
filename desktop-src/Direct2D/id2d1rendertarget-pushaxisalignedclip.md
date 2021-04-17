---
title: Методы Пушаксисалигнедклип ID2D1RenderTarget (D2d1 \_ 1. h)
description: Задает прямоугольник, на который обрезаются все последующие операции рисования.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Методы Пушаксисалигнедклип Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680020"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a><span data-ttu-id="fd04b-104">ID2D1RenderTarget: методы:P Ушаксисалигнедклип</span><span class="sxs-lookup"><span data-stu-id="fd04b-104">ID2D1RenderTarget::PushAxisAlignedClip methods</span></span>

<span data-ttu-id="fd04b-105">Задает прямоугольник, на который обрезаются все последующие операции рисования.</span><span class="sxs-lookup"><span data-stu-id="fd04b-105">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span>

### <a name="overload-list"></a><span data-ttu-id="fd04b-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="fd04b-106">Overload list</span></span>



| <span data-ttu-id="fd04b-107">Метод</span><span class="sxs-lookup"><span data-stu-id="fd04b-107">Method</span></span>                                                                                                                                         | <span data-ttu-id="fd04b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fd04b-108">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd04b-109">[**Пушаксисалигнедклип (D2D1 \_ \_ F&, \_ режим сглаживания D2D1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="fd04b-109">[**PushAxisAlignedClip(D2D1\_RECT\_F&,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span>  | <span data-ttu-id="fd04b-110">Задает прямоугольник, на который обрезаются все последующие операции рисования.</span><span class="sxs-lookup"><span data-stu-id="fd04b-110">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |
| <span data-ttu-id="fd04b-111">[**Пушаксисалигнедклип (D2D1 \_ Rect \_ F \* , \_ режим сглаживания D2D1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="fd04b-111">[**PushAxisAlignedClip(D2D1\_RECT\_F\*,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span> | <span data-ttu-id="fd04b-112">Задает прямоугольник, на который обрезаются все последующие операции рисования.</span><span class="sxs-lookup"><span data-stu-id="fd04b-112">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="fd04b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd04b-113">Remarks</span></span>

<span data-ttu-id="fd04b-114">Пара [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) и [**попаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) может возникать или внутри [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), но не может перекрываться.</span><span class="sxs-lookup"><span data-stu-id="fd04b-114">A [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pair can occur around or within a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), but cannot overlap.</span></span> <span data-ttu-id="fd04b-115">Например, последовательность **пушаксисалигнедклип**, [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **поплайер**, **Попаксисалигнедклип** является допустимой, но последовательность **пушаксисалигнедклип**, **пушлайер**, **PopAxisAlignedClip**, **PopLayer** недопустима.</span><span class="sxs-lookup"><span data-stu-id="fd04b-115">For example, the sequence of **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** is valid, but the sequence of **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** is invalid.</span></span>

<span data-ttu-id="fd04b-116">Этот метод не возвращает код ошибки в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="fd04b-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="fd04b-117">Чтобы определить, не завершилась ли операция рисования (например, **пушаксисалигнедклип**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="fd04b-117">To determine whether a drawing operation (such as **PushAxisAlignedClip**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="fd04b-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd04b-118">Examples</span></span>

<span data-ttu-id="fd04b-119">Пример см. в разделе [как обрезать с помощью прямоугольника Axis-Aligned Clip](how-to-clip-with-axis-aligned-rects.md).</span><span class="sxs-lookup"><span data-stu-id="fd04b-119">For an example, see the [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd04b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fd04b-120">Requirements</span></span>



| <span data-ttu-id="fd04b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fd04b-121">Requirement</span></span> | <span data-ttu-id="fd04b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fd04b-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd04b-123">Header</span><span class="sxs-lookup"><span data-stu-id="fd04b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fd04b-124"><dt>D2d1 \_ 1. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd04b-124"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="fd04b-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd04b-125">Library</span></span><br/> | <dl> <span data-ttu-id="fd04b-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd04b-126"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fd04b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fd04b-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd04b-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd04b-128"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="fd04b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd04b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd04b-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="fd04b-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="fd04b-131">�</span><span class="sxs-lookup"><span data-stu-id="fd04b-131">�</span></span>

<span data-ttu-id="fd04b-132">�</span><span class="sxs-lookup"><span data-stu-id="fd04b-132">�</span></span>
