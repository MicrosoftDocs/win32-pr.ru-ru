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
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a><span data-ttu-id="da63e-103">Как загрузить растровое изображение из ресурса (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="da63e-103">How to Load a Bitmap from a Resource (Direct2D)</span></span>

<span data-ttu-id="da63e-104">Как описано в статье [Загрузка точечного рисунка из файла](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D использует компонент Windows Imaging Component (WIC) для загрузки растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="da63e-104">As described in [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="da63e-105">Чтобы загрузить точечный рисунок из ресурса, используйте объекты WIC для загрузки изображения и преобразования его в формат, совместимый с Direct2D. затем используйте метод [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md) для создания [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="da63e-105">To load a bitmap from a resource, use WIC objects to load the image and to convert it to a Direct2D-compatible format; then, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="da63e-106">В [файле определения ресурса приложения](/windows/desktop/menurc/about-resource-files)определите ресурс.</span><span class="sxs-lookup"><span data-stu-id="da63e-106">In the [application resource definition file](/windows/desktop/menurc/about-resource-files), define the resource.</span></span> <span data-ttu-id="da63e-107">В следующем примере определяется ресурс с именем «Самплеимаже».</span><span class="sxs-lookup"><span data-stu-id="da63e-107">The following example defines a resource named "SampleImage".</span></span>

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

<span data-ttu-id="da63e-108">Этот ресурс будет добавлен в файл ресурсов приложения при сборке приложения.</span><span class="sxs-lookup"><span data-stu-id="da63e-108">This resource will be added to the application's resource file when the application is built.</span></span>

2.  <span data-ttu-id="da63e-109">Загрузите образ из файла ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="da63e-109">Load the image from the application resource file.</span></span>

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

    

3.  <span data-ttu-id="da63e-110">Блокировка ресурса и вычисление размера изображения.</span><span class="sxs-lookup"><span data-stu-id="da63e-110">Lock the resource and calculate the image's size.</span></span>
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

    

4.  <span data-ttu-id="da63e-111">Используйте метод [**IWICImagingFactory:: креатестреам**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) для создания объекта [**ивикстреам**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="da63e-111">Use the [**IWICImagingFactory::CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) object.</span></span>
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

    

5.  <span data-ttu-id="da63e-112">Чтобы создать [**ивикбитмапдекодер**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder), используйте метод [**IWICImagingFactory:: креатедекодерфромстреам**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="da63e-112">Use the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method to create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

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

    

6.  <span data-ttu-id="da63e-113">Извлеките кадр из изображения и сохраните его в объекте [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="da63e-113">Retrieve a frame from the image and store it in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  <span data-ttu-id="da63e-114">Прежде чем Direct2D сможет использовать образ, его необходимо преобразовать в формат пикселей 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="da63e-114">Before Direct2D can use the image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="da63e-115">Чтобы преобразовать формат изображения, используйте метод [**IWICImagingFactory:: креатеформатконвертер**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) для создания объекта [**ивикформатконвертер**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , а затем используйте метод [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) объекта **ивикформатконвертер** для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="da63e-115">To convert the image format, use the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then use the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
 
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

    

8.  <span data-ttu-id="da63e-116">Наконец, используйте метод [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md) для создания объекта [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , который может быть нарисован целевым объектом отрисовки и используется с другими объектами Direct2D.</span><span class="sxs-lookup"><span data-stu-id="da63e-116">Finally, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
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

    

<span data-ttu-id="da63e-117">В этом примере пропущен некоторый код.</span><span class="sxs-lookup"><span data-stu-id="da63e-117">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da63e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="da63e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da63e-119">Как загрузить точечный рисунок из файла</span><span class="sxs-lookup"><span data-stu-id="da63e-119">How to Load a Bitmap from a File</span></span>](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 
