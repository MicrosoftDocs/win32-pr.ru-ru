---
title: Методы Креателайер ID2D1RenderTarget (D2d1. h)
description: Создает ресурс слоя, который можно использовать с этим целевым объектом рендеринга и совместимыми целевыми объектами рендеринга.
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
keywords:
- Методы Креателайер Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6e7fe86f041a818db77c28ed9461d8c8fb48ad64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675132"
---
# <a name="id2d1rendertargetcreatelayer-methods"></a>Методы ID2D1RenderTarget:: Креателайер

Создает ресурс слоя, который можно использовать с этим целевым объектом рендеринга и совместимыми целевыми объектами рендеринга.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                 | Описание                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Креателайер (ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))                                | Создает ресурс слоя, который можно использовать с этим целевым объектом рендеринга и совместимыми целевыми объектами рендеринга. <br/>                                               |
| [**Креателайер (D2D1 \_ size \_ F, ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))       | Создает ресурс слоя, который можно использовать с этим целевым объектом рендеринга и совместимыми целевыми объектами рендеринга. Новый слой имеет указанный начальный размер. <br/> |
| [**Креателайер (D2D1 \_ size \_ F \* , ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)) | Создает ресурс слоя, который можно использовать с этим целевым объектом рендеринга и совместимыми целевыми объектами рендеринга. Новый слой имеет указанный начальный размер. <br/> |



## <a name="remarks"></a>Комментарии

При необходимости слой автоматически изменяется.

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
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о слоях](direct2d-layers-overview.md)
</dt> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
