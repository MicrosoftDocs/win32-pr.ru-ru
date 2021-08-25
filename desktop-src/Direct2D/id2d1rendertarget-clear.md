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
ms.openlocfilehash: 4e4e0c9843752af0799901537c5ee6d682d895a5ada22843ad2c406e9bda32b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928954"
---
# <a name="id2d1rendertargetclear-methods"></a>Методы ID2D1RenderTarget:: Clear

Очищает область рисования до указанного цвета.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                 | Описание                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| [**Очистить (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) | Очищает область рисования до указанного цвета. <br/> |
| [**Очистить (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))  | Очищает область рисования до указанного цвета. <br/> |



## <a name="remarks"></a>Remarks

Direct2D интерпретирует *клеарколор* как прямую альфа-канал (без предварительного умножения). Если альфа-канал целевого объекта прорисовки имеет значение [**D2D1 \_ Alpha \_ \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), то альфа-каналы *клеарколор* пропускается и заменяется на 1,0 f (полностью непрозрачный).

Если целевой объект прорисовки имеет активный клип (заданный параметром [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), команда Clear применяется только к области внутри области обрезки.

## <a name="examples"></a>Примеры

В следующем примере метод **clear** используется для создания белого фона перед отображением другого содержимого.


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

