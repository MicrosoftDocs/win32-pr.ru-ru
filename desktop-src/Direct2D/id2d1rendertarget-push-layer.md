---
title: Методы Пушлайер ID2D1RenderTarget (D2d1 \_ 1. h)
description: Добавляет указанный слой в целевой объект отрисовки, чтобы он получал все последующие операции рисования до вызова Поплайер.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Методы Пушлайер Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689466"
---
# <a name="id2d1rendertargetpushlayer-methods"></a><span data-ttu-id="ba022-104">ID2D1RenderTarget: методы:P Ушлайер</span><span class="sxs-lookup"><span data-stu-id="ba022-104">ID2D1RenderTarget::PushLayer methods</span></span>

<span data-ttu-id="ba022-105">Добавляет указанный слой в целевой объект отрисовки, чтобы он получал все последующие операции рисования до вызова [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="ba022-105">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ba022-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="ba022-106">Overload list</span></span>



| <span data-ttu-id="ba022-107">Метод</span><span class="sxs-lookup"><span data-stu-id="ba022-107">Method</span></span>                                                                                                                            | <span data-ttu-id="ba022-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ba022-108">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba022-109">[**Пушлайер ( \_ Параметры слоя D2D1 \_&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="ba022-109">[**PushLayer(D2D1\_LAYER\_PARAMETERS&,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span></span>  | <span data-ttu-id="ba022-110">Добавляет указанный слой в целевой объект отрисовки, чтобы он получал все последующие операции рисования до вызова [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="ba022-110">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |
| <span data-ttu-id="ba022-111">[**Пушлайер ( \_ Параметры слоя \_ D2D1 \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="ba022-111">[**PushLayer(D2D1\_LAYER\_PARAMETERS\*,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span></span> | <span data-ttu-id="ba022-112">Добавляет указанный слой в целевой объект отрисовки, чтобы он получал все последующие операции рисования до вызова [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="ba022-112">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ba022-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba022-113">Remarks</span></span>

<span data-ttu-id="ba022-114">Метод [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) позволяет вызывающему объекту начать перенаправление отрисовки на слой.</span><span class="sxs-lookup"><span data-stu-id="ba022-114">The [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method enables a caller to begin redirecting rendering to a layer.</span></span> <span data-ttu-id="ba022-115">Все операции отрисовки допустимы в слое.</span><span class="sxs-lookup"><span data-stu-id="ba022-115">All rendering operations are valid in a layer.</span></span> <span data-ttu-id="ba022-116">На расположение слоя влияет набор универсальных преобразований для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="ba022-116">The location of the layer is affected by the world transform set on the render target.</span></span>

<span data-ttu-id="ba022-117">Каждый **пушлайер** должен иметь соответствующий вызов [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="ba022-117">Each **PushLayer** must have a matching [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) call.</span></span> <span data-ttu-id="ba022-118">Если количество вызовов **поплайер** превышает число вызовов **пушлайер** , то целевой объект прорисовки помещается в состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="ba022-118">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="ba022-119">Если метод [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) вызывается перед извлечением всех необработанных слоев, то целевой объект прорисовки помещается в состояние ошибки и возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="ba022-119">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned.</span></span> <span data-ttu-id="ba022-120">Состояние ошибки можно очистить с помощью вызова [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="ba022-120">The error state can be cleared by a call to [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

<span data-ttu-id="ba022-121">Определенный ресурс [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) может быть активным только в один момент времени.</span><span class="sxs-lookup"><span data-stu-id="ba022-121">A particular [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) resource can be active only at one time.</span></span> <span data-ttu-id="ba022-122">Иными словами, нельзя вызвать метод [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) , а затем сразу же следовать другому методу **пушлайер** с тем же ресурсом уровня.</span><span class="sxs-lookup"><span data-stu-id="ba022-122">In other words, you cannot call a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method, and then immediately follow with another **PushLayer** method with the same layer resource.</span></span> <span data-ttu-id="ba022-123">Вместо этого необходимо вызвать второй метод **пушлайер** с различными ресурсами слоя.</span><span class="sxs-lookup"><span data-stu-id="ba022-123">Instead, you must call the second **PushLayer** method with different layer resources.</span></span>

<span data-ttu-id="ba022-124">Пример см. в разделе [Обрезка области с помощью слоев](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="ba022-124">For an example, see [How to Clip a Region with Layers](how-to-clip-with-layers.md).</span></span>

<span data-ttu-id="ba022-125">Этот метод не возвращает код ошибки в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="ba022-125">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="ba022-126">Чтобы определить, не завершилась ли операция рисования (например, **пушлайер**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="ba022-126">To determine whether a drawing operation (such as **PushLayer**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="ba022-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="ba022-127">Examples</span></span>

<span data-ttu-id="ba022-128">В следующем примере слой используется для обрезки точечного рисунка до геометрической маски.</span><span class="sxs-lookup"><span data-stu-id="ba022-128">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="ba022-129">Полный пример см. в разделе [как обрезать геометрическую маску](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="ba022-129">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="ba022-130">Требования</span><span class="sxs-lookup"><span data-stu-id="ba022-130">Requirements</span></span>



| <span data-ttu-id="ba022-131">Требование</span><span class="sxs-lookup"><span data-stu-id="ba022-131">Requirement</span></span> | <span data-ttu-id="ba022-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ba022-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba022-133">Header</span><span class="sxs-lookup"><span data-stu-id="ba022-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ba022-134"><dt>D2d1 \_ 1. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba022-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="ba022-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba022-135">Library</span></span><br/> | <dl> <span data-ttu-id="ba022-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba022-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ba022-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ba022-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba022-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba022-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="ba022-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba022-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba022-140">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="ba022-140">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="ba022-141">Общие сведения о слоях</span><span class="sxs-lookup"><span data-stu-id="ba022-141">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

<span data-ttu-id="ba022-142">�</span><span class="sxs-lookup"><span data-stu-id="ba022-142">�</span></span>

<span data-ttu-id="ba022-143">�</span><span class="sxs-lookup"><span data-stu-id="ba022-143">�</span></span>
