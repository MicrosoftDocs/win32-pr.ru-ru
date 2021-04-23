---
title: ID2D1RenderTarget ФиллопаЦитимаск методы
description: Применяет маску непрозрачности, описываемую указанным растровым изображением к кисти, и использует эту кисть для рисования области целевого объекта отрисовки.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Методы ФиллопаЦитимаск Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656929"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a><span data-ttu-id="c5491-104">Методы ID2D1RenderTarget:: ФиллопаЦитимаск</span><span class="sxs-lookup"><span data-stu-id="c5491-104">ID2D1RenderTarget::FillOpacityMask methods</span></span>

<span data-ttu-id="c5491-105">Применяет маску непрозрачности, описываемую указанным растровым изображением к кисти, и использует эту кисть для рисования области целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c5491-105">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c5491-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="c5491-106">Overload list</span></span>



| <span data-ttu-id="c5491-107">Метод</span><span class="sxs-lookup"><span data-stu-id="c5491-107">Method</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="c5491-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c5491-108">Description</span></span>                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5491-109">[**ФиллопаЦитимаск (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ непрозрачная \_ маска,&, "f", \_ модуль D2D, f \_ \_ \_ \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="c5491-109">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F&,D2D\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span></span>       | <span data-ttu-id="c5491-110">Применяет маску непрозрачности, описываемую указанным растровым изображением к кисти, и использует эту кисть для рисования области целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c5491-110">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |
| <span data-ttu-id="c5491-111">[**ФиллопаЦитимаск (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ непрозрачность- \_ \_ содержимое, D2D, \_ прямоугольник \_ f \* , D2D \_ \_ -прямоугольник f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="c5491-111">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F\*,D2D\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span></span> | <span data-ttu-id="c5491-112">Применяет маску непрозрачности, описываемую указанным растровым изображением к кисти, и использует эту кисть для рисования области целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c5491-112">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="c5491-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5491-113">Remarks</span></span>

<span data-ttu-id="c5491-114">Для правильной работы этого метода целевой объект прорисовки должен использовать режим сглаживания с [**\_ \_ \_ псевдонимом D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) .</span><span class="sxs-lookup"><span data-stu-id="c5491-114">For this method to work properly, the render target must be using the [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) antialiasing mode.</span></span> <span data-ttu-id="c5491-115">Режим сглаживания можно задать, вызвав метод [**ID2D1RenderTarget:: сетантиалиасмоде**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) .</span><span class="sxs-lookup"><span data-stu-id="c5491-115">You can set the antialiasing mode by calling the [**ID2D1RenderTarget::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) method.</span></span>

<span data-ttu-id="c5491-116">Этот метод не возвращает код ошибки в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="c5491-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="c5491-117">Чтобы определить, не завершилась ли операция рисования (например, **филлопаЦитимаск**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="c5491-117">To determine whether a drawing operation (such as **FillOpacityMask**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5491-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c5491-118">Requirements</span></span>



| <span data-ttu-id="c5491-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c5491-119">Requirement</span></span> | <span data-ttu-id="c5491-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c5491-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c5491-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5491-121">Library</span></span><br/> | <dl> <span data-ttu-id="c5491-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5491-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="c5491-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c5491-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5491-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5491-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5491-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5491-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5491-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="c5491-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

