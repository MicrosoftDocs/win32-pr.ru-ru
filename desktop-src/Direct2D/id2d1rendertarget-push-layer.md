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
# <a name="id2d1rendertargetpushlayer-methods"></a>ID2D1RenderTarget: методы:P Ушлайер

Добавляет указанный слой в целевой объект отрисовки, чтобы он получал все последующие операции рисования до вызова [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                            | Описание                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Пушлайер ( \_ Параметры слоя D2D1 \_&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))  | Добавляет указанный слой в целевой объект отрисовки, чтобы он получал все последующие операции рисования до вызова [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . <br/> |
| [**Пушлайер ( \_ Параметры слоя \_ D2D1 \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)) | Добавляет указанный слой в целевой объект отрисовки, чтобы он получал все последующие операции рисования до вызова [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . <br/> |



## <a name="remarks"></a>Комментарии

Метод [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) позволяет вызывающему объекту начать перенаправление отрисовки на слой. Все операции отрисовки допустимы в слое. На расположение слоя влияет набор универсальных преобразований для целевого объекта прорисовки.

Каждый **пушлайер** должен иметь соответствующий вызов [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . Если количество вызовов **поплайер** превышает число вызовов **пушлайер** , то целевой объект прорисовки помещается в состояние ошибки. Если метод [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) вызывается перед извлечением всех необработанных слоев, то целевой объект прорисовки помещается в состояние ошибки и возвращается ошибка. Состояние ошибки можно очистить с помощью вызова [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

Определенный ресурс [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) может быть активным только в один момент времени. Иными словами, нельзя вызвать метод [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) , а затем сразу же следовать другому методу **пушлайер** с тем же ресурсом уровня. Вместо этого необходимо вызвать второй метод **пушлайер** с различными ресурсами слоя.

Пример см. в разделе [Обрезка области с помощью слоев](how-to-clip-with-layers.md).

Этот метод не возвращает код ошибки в случае сбоя. Чтобы определить, не завершилась ли операция рисования (например, **пушлайер**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Примеры

В следующем примере слой используется для обрезки точечного рисунка до геометрической маски. Полный пример см. в разделе [как обрезать геометрическую маску](how-to-clip-with-layers.md).


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1. h (включение D2d1. h)</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Общие сведения о слоях](direct2d-layers-overview.md)
</dt> </dl>

�

�
