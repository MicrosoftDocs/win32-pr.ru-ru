---
description: В этом разделе описывается создание декодера точечных рисунков с помощью имени файла образа.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Создание декодера с помощью имени файла образа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693562"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a><span data-ttu-id="2a66c-103">Создание декодера с помощью имени файла образа</span><span class="sxs-lookup"><span data-stu-id="2a66c-103">How to Create a Decoder Using an Image Filename</span></span>

<span data-ttu-id="2a66c-104">В этом разделе описывается создание декодера точечных рисунков с помощью имени файла образа.</span><span class="sxs-lookup"><span data-stu-id="2a66c-104">This topic describes how to create a bitmap decoder by using an image filename.</span></span>

<span data-ttu-id="2a66c-105">Создание декодера точечных рисунков с помощью имени файла образа</span><span class="sxs-lookup"><span data-stu-id="2a66c-105">To create a bitmap decoder by using an image filename</span></span>

1.  <span data-ttu-id="2a66c-106">Создайте объект [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="2a66c-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="2a66c-107">Используйте метод [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) для создания [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из файла образа.</span><span class="sxs-lookup"><span data-stu-id="2a66c-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="2a66c-108">Получите первый [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) изображения.</span><span class="sxs-lookup"><span data-stu-id="2a66c-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="2a66c-109">Формат файла JPEG поддерживает только один кадр.</span><span class="sxs-lookup"><span data-stu-id="2a66c-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="2a66c-110">Поскольку файл в этом примере является JPEG-файлом, используется первый кадр ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="2a66c-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="2a66c-111">Сведения о форматах изображений, имеющих несколько кадров, см. [в разделе Получение кадров изображения](-wic-bitmapsources-howto-retrieveimageframes.md) для доступа к каждому кадру изображения.</span><span class="sxs-lookup"><span data-stu-id="2a66c-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="2a66c-112">Обработка кадра изображения.</span><span class="sxs-lookup"><span data-stu-id="2a66c-112">Process the image frame.</span></span> <span data-ttu-id="2a66c-113">Дополнительные сведения об объектах [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) см. в разделе [Обзор источников битовой карты](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="2a66c-113">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2a66c-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="2a66c-114">See Also</span></span>

[<span data-ttu-id="2a66c-115">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="2a66c-115">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="2a66c-116">Ссылки</span><span class="sxs-lookup"><span data-stu-id="2a66c-116">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="2a66c-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="2a66c-117">Samples</span></span>](-wic-samples.md)


 

 



