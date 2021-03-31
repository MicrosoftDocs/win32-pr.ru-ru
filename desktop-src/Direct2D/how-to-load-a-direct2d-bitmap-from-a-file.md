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
# <a name="how-to-load-a-bitmap-from-a-file"></a><span data-ttu-id="7eb9d-103">Как загрузить точечный рисунок из файла</span><span class="sxs-lookup"><span data-stu-id="7eb9d-103">How to Load a Bitmap from a File</span></span>

<span data-ttu-id="7eb9d-104">Direct2D использует компонент Windows Imaging Component (WIC) для загрузки растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="7eb9d-104">Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="7eb9d-105">Чтобы загрузить точечный рисунок из файла, сначала используйте объекты WIC для загрузки изображения и преобразования его в формат, совместимый с Direct2D, а затем используйте метод [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md) для создания [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="7eb9d-105">To load a bitmap from a file, first use WIC objects to load the image and to convert it to a Direct2D-compatible format, then use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="7eb9d-106">Создайте [**ивикбитмапдекодер**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) с помощью метода [**IWICImagingFactory:: креатедекодерфромфиленаме**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="7eb9d-106">Create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) by using the [**IWICImagingFactory::CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

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

    

2.  <span data-ttu-id="7eb9d-107">Извлеките кадр из изображения и сохраните кадр в объекте [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="7eb9d-107">Retrieve a frame from the image and store the frame in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  <span data-ttu-id="7eb9d-108">Точечный рисунок должен быть преобразован в формат, который Direct2D может использовать, поэтому преобразуйте формат пикселей изображения в 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="7eb9d-108">The bitmap must be converted to a format that Direct2D can use, so convert the image's pixel format to 32bppPBGRA.</span></span> <span data-ttu-id="7eb9d-109">(Список поддерживаемых форматов см. в разделе [форматы пикселей и альфа-режимы](supported-pixel-formats-and-alpha-modes.md).)</span><span class="sxs-lookup"><span data-stu-id="7eb9d-109">(For a list of supported formats, see [Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).).</span></span> <span data-ttu-id="7eb9d-110">Вызовите метод [**IWICImagingFactory:: креатеформатконвертер**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) , чтобы создать объект [**ивикформатконвертер**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , а затем вызовите метод [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) объекта **ивикформатконвертер** для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="7eb9d-110">Call the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then call the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
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

    

4.  <span data-ttu-id="7eb9d-111">Вызовите метод [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md) , чтобы создать объект [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , который может быть нарисован целевым объектом рендеринга и использоваться с другими объектами Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7eb9d-111">Call the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
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

    

<span data-ttu-id="7eb9d-112">В этом примере пропущен некоторый код.</span><span class="sxs-lookup"><span data-stu-id="7eb9d-112">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eb9d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="7eb9d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eb9d-114">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="7eb9d-114">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="7eb9d-115">**креатебитмапфромвикбитмап**</span><span class="sxs-lookup"><span data-stu-id="7eb9d-115">**CreateBitmapFromWicBitmap**</span></span>](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[<span data-ttu-id="7eb9d-116">Как загрузить точечный рисунок из ресурса</span><span class="sxs-lookup"><span data-stu-id="7eb9d-116">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 