---
title: Как загрузить растровое изображение из ресурса (Direct2D)
description: Показывает, как загрузить точечный рисунок Direct2D, хранящийся в качестве ресурса приложения.
ms.assetid: 7285e6ea-ebc7-4693-8a77-99bff0b5d0d1
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: fe96ba4e0674392333173df7daeb5a354a379343
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105672435"
---
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a>Как загрузить растровое изображение из ресурса (Direct2D)

Как описано в статье [Загрузка точечного рисунка из файла](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D использует компонент Windows Imaging Component (WIC) для загрузки растровых изображений. Чтобы загрузить точечный рисунок из ресурса, используйте объекты WIC для загрузки изображения и преобразования его в формат, совместимый с Direct2D. затем используйте метод [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md) для создания [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

1.  В [файле определения ресурса приложения](/windows/desktop/menurc/about-resource-files)определите ресурс. В следующем примере определяется ресурс с именем «Самплеимаже».

    ```C++
    // THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
    // ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
    // THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
    // PARTICULAR PURPOSE.
    //
    // Copyright (c) Microsoft Corporation. All rights reserved
    #include "windows.h"

    SampleImage Image "sampleImage.jpg"
    ```

Этот ресурс будет добавлен в файл ресурсов приложения при сборке приложения.

2.  Загрузите образ из файла ресурсов приложения.

    ```C++
    HRESULT DemoApp::LoadResourceBitmap(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR resourceName,
        PCWSTR resourceType,
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

        HRSRC imageResHandle = NULL;
        HGLOBAL imageResDataHandle = NULL;
        void *pImageFile = NULL;
        DWORD imageFileSize = 0;

        // Locate the resource.
        imageResHandle = FindResourceW(HINST_THISCOMPONENT, resourceName, resourceType);
        HRESULT hr = imageResHandle ? S_OK : E_FAIL;
        if (SUCCEEDED(hr))
        {
            // Load the resource.
            imageResDataHandle = LoadResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageResDataHandle ? S_OK : E_FAIL;
        }
    ```

    

3.  Блокировка ресурса и вычисление размера изображения.
    ```C++
        if (SUCCEEDED(hr))
        {
            // Lock it to get a system memory pointer.
            pImageFile = LockResource(imageResDataHandle);

            hr = pImageFile ? S_OK : E_FAIL;
        }
        if (SUCCEEDED(hr))
        {
            // Calculate the size.
            imageFileSize = SizeofResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageFileSize ? S_OK : E_FAIL;
            
        }
    ```

    

4.  Используйте метод [**IWICImagingFactory:: креатестреам**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) для создания объекта [**ивикстреам**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) .
    ```C++
        if (SUCCEEDED(hr))
        {
              // Create a WIC stream to map onto the memory.
            hr = pIWICFactory->CreateStream(&pStream);
        }
        if (SUCCEEDED(hr))
        {
            // Initialize the stream with the memory pointer and size.
            hr = pStream->InitializeFromMemory(
                reinterpret_cast<BYTE*>(pImageFile),
                imageFileSize
                );
        }
    ```

    

5.  Чтобы создать [**ивикбитмапдекодер**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder), используйте метод [**IWICImagingFactory:: креатедекодерфромстреам**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create a decoder for the stream.
            hr = pIWICFactory->CreateDecoderFromStream(
                pStream,
                NULL,
                WICDecodeMetadataCacheOnLoad,
                &pDecoder
                );
        }
    ```

    

6.  Извлеките кадр из изображения и сохраните его в объекте [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  Прежде чем Direct2D сможет использовать образ, его необходимо преобразовать в формат пикселей 32bppPBGRA. Чтобы преобразовать формат изображения, используйте метод [**IWICImagingFactory:: креатеформатконвертер**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) для создания объекта [**ивикформатконвертер**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , а затем используйте метод [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) объекта **ивикформатконвертер** для выполнения преобразования.
 
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

    

8.  Наконец, используйте метод [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md) для создания объекта [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , который может быть нарисован целевым объектом отрисовки и используется с другими объектами Direct2D.
    ```C++
        if (SUCCEEDED(hr))
        {
            //create a Direct2D bitmap from the WIC bitmap.
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

[Как загрузить точечный рисунок из файла](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 
