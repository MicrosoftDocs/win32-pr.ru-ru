---
title: Как загрузить точечный рисунок из файла
description: Показывает, как загрузить точечный рисунок Direct2D из файла изображения.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: c9590e799e71e92056157b75573565cf79b9236b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792823"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a>Как загрузить точечный рисунок из файла

Direct2D использует компонент Windows Imaging Component (WIC) для загрузки растровых изображений. Чтобы загрузить точечный рисунок из файла, сначала используйте объекты WIC для загрузки изображения и преобразования его в формат, совместимый с Direct2D, а затем используйте метод [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md) для создания [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

1.  Создайте [**ивикбитмапдекодер**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) с помощью метода [**IWICImagingFactory:: креатедекодерфромфиленаме**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .

    ```C++
    HRESULT DemoApp::LoadBitmapFromFile(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR uri,
        UINT destinationWidth,
        UINT destinationHeight,
        ID2D1Bitmap **ppBitmap
        )
    {
        IWICBitmapDecoder *pDecoder = NULL;
        IWICBitmapFrameDecode *pSource = NULL;
        IWICStream *pStream = NULL;
        IWICFormatConverter *pConverter = NULL;
        IWICBitmapScaler *pScaler = NULL;

        HRESULT hr = pIWICFactory->CreateDecoderFromFilename(
            uri,
            NULL,
            GENERIC_READ,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
            
    ```

    

2.  Извлеките кадр из изображения и сохраните кадр в объекте [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  Точечный рисунок должен быть преобразован в формат, который Direct2D может использовать, поэтому преобразуйте формат пикселей изображения в 32bppPBGRA. (Список поддерживаемых форматов см. в разделе [форматы пикселей и альфа-режимы](supported-pixel-formats-and-alpha-modes.md).) Вызовите метод [**IWICImagingFactory:: креатеформатконвертер**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) , чтобы создать объект [**ивикформатконвертер**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , а затем вызовите метод [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) объекта **ивикформатконвертер** для выполнения преобразования.
    ```C++
        if (SUCCEEDED(hr))
        {

            // Convert the image format to 32bppPBGRA
            // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
            hr = pIWICFactory->CreateFormatConverter(&pConverter);

        }
     
     
        if (SUCCEEDED(hr))
        {
            hr = pConverter->Initialize(
                pSource,
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                NULL,
                0.f,
                WICBitmapPaletteTypeMedianCut
                );
    ```

    

4.  Вызовите метод [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md) , чтобы создать объект [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , который может быть нарисован целевым объектом рендеринга и использоваться с другими объектами Direct2D.
    ```C++
        if (SUCCEEDED(hr))
        {
        
            // Create a Direct2D bitmap from the WIC bitmap.
            hr = pRenderTarget->CreateBitmapFromWicBitmap(
                pConverter,
                NULL,
                ppBitmap
                );
        }

        SafeRelease(&pDecoder);
        SafeRelease(&pSource);
        SafeRelease(&pStream);
        SafeRelease(&pConverter);
        SafeRelease(&pScaler);

        return hr;
    }
    ```

    

В этом примере пропущен некоторый код.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[Как загрузить точечный рисунок из ресурса](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 