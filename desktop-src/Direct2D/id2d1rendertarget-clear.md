---
title: Методы очистки ID2D1RenderTarget
description: Очищает область рисования до указанного цвета.
ms.assetid: 3bfec923-17fc-479a-a760-9baab2ff3a56
keywords:
- Методы очистки Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 346e44e3ce0b59e40577d3207f45faafdc33b367
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657632"
---
# <a name="id2d1rendertargetclear-methods"></a><span data-ttu-id="edacb-104">Методы ID2D1RenderTarget:: Clear</span><span class="sxs-lookup"><span data-stu-id="edacb-104">ID2D1RenderTarget::Clear methods</span></span>

<span data-ttu-id="edacb-105">Очищает область рисования до указанного цвета.</span><span class="sxs-lookup"><span data-stu-id="edacb-105">Clears the drawing area to the specified color.</span></span>

### <a name="overload-list"></a><span data-ttu-id="edacb-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="edacb-106">Overload list</span></span>



| <span data-ttu-id="edacb-107">Метод</span><span class="sxs-lookup"><span data-stu-id="edacb-107">Method</span></span>                                                                 | <span data-ttu-id="edacb-108">Описание</span><span class="sxs-lookup"><span data-stu-id="edacb-108">Description</span></span>                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| <span data-ttu-id="edacb-109">[**Очистить (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="edacb-109">[**Clear(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))</span></span> | <span data-ttu-id="edacb-110">Очищает область рисования до указанного цвета.</span><span class="sxs-lookup"><span data-stu-id="edacb-110">Clears the drawing area to the specified color.</span></span> <br/> |
| <span data-ttu-id="edacb-111">[**Очистить (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="edacb-111">[**Clear(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))</span></span>  | <span data-ttu-id="edacb-112">Очищает область рисования до указанного цвета.</span><span class="sxs-lookup"><span data-stu-id="edacb-112">Clears the drawing area to the specified color.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="edacb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edacb-113">Remarks</span></span>

<span data-ttu-id="edacb-114">Direct2D интерпретирует *клеарколор* как прямую альфа-канал (без предварительного умножения).</span><span class="sxs-lookup"><span data-stu-id="edacb-114">Direct2D interprets the *clearColor* as straight alpha (not premultiplied).</span></span> <span data-ttu-id="edacb-115">Если альфа-канал целевого объекта прорисовки имеет значение [**D2D1 \_ Alpha \_ \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), то альфа-каналы *клеарколор* пропускается и заменяется на 1,0 f (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="edacb-115">If the render target's alpha mode is [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), the alpha channel of *clearColor* is ignored and replaced with 1.0f (fully opaque).</span></span>

<span data-ttu-id="edacb-116">Если целевой объект прорисовки имеет активный клип (заданный параметром [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), команда Clear применяется только к области внутри области обрезки.</span><span class="sxs-lookup"><span data-stu-id="edacb-116">If the render target has an active clip (specified by [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), the clear command is only applied to the area within the clip region.</span></span>

## <a name="examples"></a><span data-ttu-id="edacb-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="edacb-117">Examples</span></span>

<span data-ttu-id="edacb-118">В следующем примере метод **clear** используется для создания белого фона перед отображением другого содержимого.</span><span class="sxs-lookup"><span data-stu-id="edacb-118">The following example uses the **Clear** method to create a white background before rendering other content.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="edacb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="edacb-119">Requirements</span></span>



| <span data-ttu-id="edacb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="edacb-120">Requirement</span></span> | <span data-ttu-id="edacb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="edacb-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="edacb-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="edacb-122">Library</span></span><br/> | <dl> <span data-ttu-id="edacb-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edacb-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="edacb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="edacb-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="edacb-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edacb-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edacb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edacb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edacb-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="edacb-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

