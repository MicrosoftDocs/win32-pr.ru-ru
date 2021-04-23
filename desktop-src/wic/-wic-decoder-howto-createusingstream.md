---
description: В этом разделе описывается, как создать растровый декодер с помощью потока.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Создание декодера с помощью потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693716"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a><span data-ttu-id="45f83-103">Создание декодера с помощью потока</span><span class="sxs-lookup"><span data-stu-id="45f83-103">How to Create a Decoder Using a Stream</span></span>

<span data-ttu-id="45f83-104">В этом разделе описывается, как создать растровый декодер с помощью потока.</span><span class="sxs-lookup"><span data-stu-id="45f83-104">This topic describes how to create a bitmap decoder by using a stream.</span></span>

<span data-ttu-id="45f83-105">Создание декодера точечных рисунков с помощью потока</span><span class="sxs-lookup"><span data-stu-id="45f83-105">To create a bitmap decoder by using a stream</span></span>

1.  <span data-ttu-id="45f83-106">Загрузить файл изображения в поток.</span><span class="sxs-lookup"><span data-stu-id="45f83-106">Load an image file into a stream.</span></span> <span data-ttu-id="45f83-107">В этом примере создается поток для ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="45f83-107">In this example, a stream is created for an application resource.</span></span>

    <span data-ttu-id="45f83-108">В файле определения ресурса приложения (. RC) определите ресурс.</span><span class="sxs-lookup"><span data-stu-id="45f83-108">In the application resource definition (.rc) file, define the resource.</span></span> <span data-ttu-id="45f83-109">В следующем примере определяется `Image` ресурс с именем `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="45f83-109">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="45f83-110">Ресурс будет добавлен в ресурсы приложения при сборке приложения.</span><span class="sxs-lookup"><span data-stu-id="45f83-110">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="45f83-111">Загрузите ресурс из приложения.</span><span class="sxs-lookup"><span data-stu-id="45f83-111">Load the resource from the application.</span></span>

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  <span data-ttu-id="45f83-112">Блокировка ресурса и получение размера.</span><span class="sxs-lookup"><span data-stu-id="45f83-112">Lock the resource and get the size.</span></span>

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  <span data-ttu-id="45f83-113">Создайте [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="45f83-113">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  <span data-ttu-id="45f83-114">Используйте метод [**креатестреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) для создания объекта [**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) и его инициализации с помощью указателя памяти изображения.</span><span class="sxs-lookup"><span data-stu-id="45f83-114">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

6.  <span data-ttu-id="45f83-115">Создайте [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из нового объекта потока с помощью метода [**креатедекодерфромстреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="45f83-115">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

7.  <span data-ttu-id="45f83-116">Получите первый [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) изображения.</span><span class="sxs-lookup"><span data-stu-id="45f83-116">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="45f83-117">Формат файла JPEG поддерживает только один кадр.</span><span class="sxs-lookup"><span data-stu-id="45f83-117">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="45f83-118">Поскольку файл в этом примере является JPEG-файлом, используется первый кадр ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="45f83-118">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="45f83-119">Сведения о форматах изображений, имеющих несколько кадров, см. [в разделе Получение кадров изображения](-wic-bitmapsources-howto-retrieveimageframes.md) для доступа к каждому кадру изображения.</span><span class="sxs-lookup"><span data-stu-id="45f83-119">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

8.  <span data-ttu-id="45f83-120">Обработка кадра изображения.</span><span class="sxs-lookup"><span data-stu-id="45f83-120">Process the image frame.</span></span> <span data-ttu-id="45f83-121">Дополнительные сведения об объектах [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) см. в разделе [Обзор источников битовой карты](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="45f83-121">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="45f83-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="45f83-122">See Also</span></span>

[<span data-ttu-id="45f83-123">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="45f83-123">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="45f83-124">Ссылки</span><span class="sxs-lookup"><span data-stu-id="45f83-124">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="45f83-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="45f83-125">Samples</span></span>](-wic-samples.md)


 

 



