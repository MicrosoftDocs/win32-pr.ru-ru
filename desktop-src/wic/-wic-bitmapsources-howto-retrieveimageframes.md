---
description: В этом разделе показано, как декодировать изображение из нескольких кадров и получить каждый кадр для обработки.
ms.assetid: e4f69608-7bf1-4d54-b586-b749526700c9
title: Получение кадров из изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeeb19e0a0ac69f75673df0736fd0bd4987b3423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144743"
---
# <a name="how-to-retrieve-the-frames-from-an-image"></a><span data-ttu-id="c435d-103">Получение кадров из изображения</span><span class="sxs-lookup"><span data-stu-id="c435d-103">How to Retrieve the Frames from an Image</span></span>

<span data-ttu-id="c435d-104">В этом разделе показано, как декодировать изображение из нескольких кадров и получить каждый кадр для обработки.</span><span class="sxs-lookup"><span data-stu-id="c435d-104">This topic demonstrates how to decode a multi-frame image and retrieve each frame for processing.</span></span>

<span data-ttu-id="c435d-105">Получение кадров изображения</span><span class="sxs-lookup"><span data-stu-id="c435d-105">To retrieve the frames of an image</span></span>

1.  <span data-ttu-id="c435d-106">Создайте [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="c435d-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="c435d-107">Используйте метод [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) для создания [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из файла образа.</span><span class="sxs-lookup"><span data-stu-id="c435d-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    UINT nFrameCount = 0;
    UINT uiWidth, uiHeight;

    // Create decoder for an image.
    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"creek.tiff",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="c435d-108">Получение количества кадров в изображениях.</span><span class="sxs-lookup"><span data-stu-id="c435d-108">Retrieve the number of frames in the images.</span></span>

    ```C++
    // Retrieve the frame count of the image.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrameCount(&nFrameCount);
    }
    ```

    

4.  <span data-ttu-id="c435d-109">Обработайте каждый кадр, получив [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) для каждого кадра в изображении.</span><span class="sxs-lookup"><span data-stu-id="c435d-109">Process each frame by obtaining an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) for each frame in the image.</span></span>

    ```C++
    // Process each frame in the image.
    for (UINT i=0; i < nFrameCount; i++)
    {
       // Retrieve the next bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoder->GetFrame(i, &pIDecoderFrame);
       }

       // Retrieve the size of the bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoderFrame->GetSize(&uiWidth, &uiHeight);
       }

       // Additional frame processing.
       // ...

       SafeRelease(&pIDecoderFrame);
    }
    ```

    

## <a name="see-also"></a><span data-ttu-id="c435d-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="c435d-110">See Also</span></span>

[<span data-ttu-id="c435d-111">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="c435d-111">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="c435d-112">Ссылки</span><span class="sxs-lookup"><span data-stu-id="c435d-112">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="c435d-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="c435d-113">Samples</span></span>](-wic-samples.md)


 

 



