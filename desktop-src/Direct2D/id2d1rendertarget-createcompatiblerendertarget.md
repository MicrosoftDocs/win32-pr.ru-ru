---
title: Методы Креатекомпатиблерендертаржет ID2D1RenderTarget (D2d1. h)
description: Создает новый целевой объект прорисовки растрового изображения для использования во время промежуточного рисования, совместимого с текущим целевым объектом рендеринга.
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
keywords:
- Методы Креатекомпатиблерендертаржет Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9015586109ff5015743874d18b604de919a9464a655383cf4d47aabb7b7acf35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432784"
---
# <a name="id2d1rendertargetcreatecompatiblerendertarget-methods"></a>Методы ID2D1RenderTarget:: Креатекомпатиблерендертаржет

Создает новый целевой объект прорисовки растрового изображения для использования во время промежуточного рисования, совместимого с текущим целевым объектом рендеринга.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                        | Описание                                                                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Креатекомпатиблерендертаржет (D2D1 \_ size \_ F, D2D1 \_ size \_ U, D2D1 \_ пикселей \_ , D2D1 \_ совместимые \_ \_ параметры целевого объекта прорисовки \_ , ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget))       | Создает целевой объект прорисовки растрового изображения для использования во время промежуточного рисования, совместимого с текущим целевым объектом отрисовки.<br/>                                                                                                             |
| [**Креатекомпатиблерендертаржет (D2D1 \_ size \_ F \* , D2D1 \_ size \_ U \* , D2D1 \_ пикселей \_ \* , D2D1 \_ совместимые \_ \_ параметры целевого объекта прорисовки \_ , ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)) | Создает целевой объект прорисовки растрового изображения для использования во время промежуточного рисования, совместимого с текущим целевым объектом отрисовки. <br/>                                                                                                            |
| [**Креатекомпатиблерендертаржет (ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))                                                                                                 | Создает новый целевой объект прорисовки растрового изображения для использования во время промежуточного рисования, совместимого с текущим целевым объектом рендеринга и имеющий тот же размер, DPI и формат пикселей (но не альфа-режим), что и текущий целевой объект отрисовки. <br/>         |
| [**Креатекомпатиблерендертаржет (D2D1 \_ size \_ F, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_id2d1bitmaprendertarget))                                                                                   | Создает новый целевой объект прорисовки растрового изображения для использования во время промежуточного рисования, совместимого с текущим целевым объектом рендеринга и имеющий тот же формат пикселей (но не альфа-режим), что и текущий целевой объект отрисовки. <br/>                        |
| [**Креатекомпатиблерендертаржет (D2D1 \_ size \_ F, D2D1 \_ размер \_ U, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_id2d1bitmaprendertarget))                                                                     | Создает целевой объект прорисовки растрового изображения для использования во время промежуточного экрана, совместимого с текущим целевым объектом отрисовки. Новый целевой объект прорисовки изображения имеет тот же формат пикселей (но не альфа-режим), что и текущий целевой объект отрисовки. <br/> |
| [**Креатекомпатиблерендертаржет (D2D1 \_ размер \_ F, D2D1 \_ размер \_ U, \_ Формат пикселей D2D1 \_ , ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_id2d1bitmaprendertarget))                                                 | Создает целевой объект прорисовки растрового изображения для использования во время промежуточного рисования, совместимого с текущим целевым объектом отрисовки. <br/>                                                                                                            |



## <a name="examples"></a>Примеры

В следующем примере метод **креатекомпатиблерендертаржет** используется для создания [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) и использует его для рисования шаблона сетки. Шаблон сетки используется в качестве источника [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).


```C++
HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget->CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &amp;pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &amp;pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget->BeginDraw();
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget->EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget->GetBitmap(&amp;pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget->CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap->Release();
            }

            pGridBrush->Release();
        }

        pCompatibleRenderTarget->Release();
    }

    return hr;
}
```



В следующем примере кода кисть используется для рисования шаблона.


```C++
// Paint a grid background.
m_pRenderTarget->FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
```



В этом примере код пропущен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
