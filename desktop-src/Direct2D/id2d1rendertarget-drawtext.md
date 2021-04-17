---
title: ID2D1RenderTarget DrawText методы
description: Рисует указанный текст, используя сведения о форматировании, предоставленные объектом Идвритетекстформат.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Методы DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675127"
---
# <a name="id2d1rendertargetdrawtext-methods"></a><span data-ttu-id="33ab8-104">ID2D1RenderTarget: методы:D Равтекст</span><span class="sxs-lookup"><span data-stu-id="33ab8-104">ID2D1RenderTarget::DrawText methods</span></span>

<span data-ttu-id="33ab8-105">Рисует указанный текст, используя сведения о форматировании, предоставленные объектом [**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="33ab8-105">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="33ab8-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="33ab8-106">Overload list</span></span>



| <span data-ttu-id="33ab8-107">Метод</span><span class="sxs-lookup"><span data-stu-id="33ab8-107">Method</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="33ab8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="33ab8-108">Description</span></span>                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ab8-109">[**DrawText (WCHAR \* , идвритетекстформат \* , D2D1 \_ Rect \_ F&, ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ , дврите \_ Text, \_ \_ метод измерения)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="33ab8-109">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F&,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>  | <span data-ttu-id="33ab8-110">Рисует указанный текст, используя сведения о форматировании, предоставленные объектом [**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="33ab8-110">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span><br/>  |
| <span data-ttu-id="33ab8-111">[**DrawText (WCHAR \* , идвритетекстформат \* , D2D1 \_ Rect \_ F \* , ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ , дврите \_ Text, \_ \_ метод измерения)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="33ab8-111">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F\*,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> | <span data-ttu-id="33ab8-112">Рисует указанный текст, используя сведения о форматировании, предоставленные объектом [**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="33ab8-112">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="33ab8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33ab8-113">Remarks</span></span>

<span data-ttu-id="33ab8-114">Чтобы нарисовать текст с помощью Direct2D, используйте метод [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) для текста, имеющего один формат, или метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , если требуется несколько форматов, расширенные функции OpenType или проверка попадания.</span><span class="sxs-lookup"><span data-stu-id="33ab8-114">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format, or the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method when you need multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="33ab8-115">Эти методы используют API DirectWrite для обеспечения высокого качества отображения текста.</span><span class="sxs-lookup"><span data-stu-id="33ab8-115">These methods use the DirectWrite API to provide high-quality text display.</span></span>

<span data-ttu-id="33ab8-116">Этот метод не возвращает код ошибки в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="33ab8-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="33ab8-117">Чтобы определить, не завершилась ли операция рисования (например, **DrawText**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="33ab8-117">To determine whether a drawing operation (such as **DrawText**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="33ab8-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="33ab8-118">Examples</span></span>

<span data-ttu-id="33ab8-119">Пример см. в разделе [Рисование текста](how-to--draw-text.md).</span><span class="sxs-lookup"><span data-stu-id="33ab8-119">For an example, see [How to Draw Text](how-to--draw-text.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33ab8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="33ab8-120">Requirements</span></span>



| <span data-ttu-id="33ab8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="33ab8-121">Requirement</span></span> | <span data-ttu-id="33ab8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="33ab8-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33ab8-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="33ab8-123">Library</span></span><br/> | <dl> <span data-ttu-id="33ab8-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33ab8-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="33ab8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="33ab8-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="33ab8-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33ab8-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ab8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33ab8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ab8-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="33ab8-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="33ab8-129">**идвритетекстформат**</span><span class="sxs-lookup"><span data-stu-id="33ab8-129">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="33ab8-130">Рисование текста</span><span class="sxs-lookup"><span data-stu-id="33ab8-130">How to Draw Text</span></span>](how-to--draw-text.md)
</dt> <dt>

[<span data-ttu-id="33ab8-131">Общие сведения о форматировании и макете текста</span><span class="sxs-lookup"><span data-stu-id="33ab8-131">Text Formatting and Layout Overview</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

