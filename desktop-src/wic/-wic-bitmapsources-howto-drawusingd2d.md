---
description: В этом разделе показан процесс рисования IWICBitmapSource с помощью Direct2D.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Рисование перерисовки с помощью Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6dfdddb7cd6f7ab7341eb3c13a9fe40b797f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719510"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a>Рисование перерисовки с помощью Direct2D

В этом разделе показан процесс рисования [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) с помощью Direct2D.

Рисование источника точечного рисунка с помощью Direct2D

1.  Декодирование исходного изображения и получение источника точечного рисунка. В этом примере используется [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) для декодирования изображения и извлечения первого кадра изображения.

    ```C++
       // Create a decoder
       IWICBitmapDecoder *pDecoder = NULL;

       hr = m_pIWICFactory->CreateDecoderFromFilename(
           szFileName,                      // Image to be decoded
           NULL,                            // Do not prefer a particular vendor
           GENERIC_READ,                    // Desired read access to the file
           WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
           &pDecoder                        // Pointer to the decoder
           );

       // Retrieve the first frame of the image from the decoder
       IWICBitmapFrameDecode *pFrame = NULL;

       if (SUCCEEDED(hr))
       {
           hr = pDecoder->GetFrame(0, &pFrame);
       }
    ```

    

    Дополнительные типы источников точечных рисунков для рисования см. в разделе [Общие сведения об источниках битовой карты](-wic-bitmapsources.md).

2.  Преобразование исходного растрового изображения в формат пикселей 32bppPBGRA.

    Прежде чем Direct2D сможет использовать изображение, его необходимо преобразовать в формат пикселей 32bppPBGRA. Чтобы преобразовать формат изображения, используйте метод [**креатеформатконвертер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) для создания объекта [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) . После создания используйте метод [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) для выполнения преобразования.

    ```C++
       // Format convert the frame to 32bppPBGRA
       if (SUCCEEDED(hr))
       {
           SafeRelease(&m_pConvertedSourceBitmap);
           hr = m_pIWICFactory->CreateFormatConverter(&m_pConvertedSourceBitmap);
       }

       if (SUCCEEDED(hr))
       {
           hr = m_pConvertedSourceBitmap->Initialize(
               pFrame,                          // Input bitmap to convert
               GUID_WICPixelFormat32bppPBGRA,   // Destination pixel format
               WICBitmapDitherTypeNone,         // Specified dither pattern
               NULL,                            // Specify a particular palette 
               0.f,                             // Alpha threshold
               WICBitmapPaletteTypeCustom       // Palette translation type
               );
       }
    ```

    

3.  Создайте объект [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) для подготовки к просмотру в окне обработчика.

    ```C++
       // Create a D2D render target properties
       D2D1_RENDER_TARGET_PROPERTIES renderTargetProperties = D2D1::RenderTargetProperties();

       // Set the DPI to be the default system DPI to allow direct mapping
       // between image pixels and desktop pixels in different system DPI settings
       renderTargetProperties.dpiX = DEFAULT_DPI;
       renderTargetProperties.dpiY = DEFAULT_DPI;

       // Create a D2D render target
       D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

       hr = m_pD2DFactory->CreateHwndRenderTarget(
           renderTargetProperties,
           D2D1::HwndRenderTargetProperties(hWnd, size),
           &m_pRT
           );
    ```

    

    Дополнительные сведения о целевых объектах отрисовки см. в разделе Direct2D [Render Targets Overview](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).

4.  Создайте объект [ID2D1Bitmap](../direct2d/render-targets-overview.md) с помощью метода [ID2D1RenderTarget:: креатебитмапфромвикбитмап](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) .

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  Нарисуйте [ID2D1Bitmap](../direct2d/render-targets-overview.md) с помощью метода D2D [ID2D1RenderTarget::D равбитмап](../direct2d/id2d1rendertarget-drawbitmap.md) .

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

В этом примере код пропущен. Полный код см. в разделе [средство просмотра изображений WIC с помощью примера Direct2D](-wic-sample-d2d-viewer.md).

## <a name="see-also"></a>См. также:

[Руководство по программированию](-wic-programming-guide.md)


[Ссылки](-wic-codec-reference.md)


[Примеры](-wic-samples.md)


[Direct2D](../direct2d/direct2d-portal.md)


 

 
