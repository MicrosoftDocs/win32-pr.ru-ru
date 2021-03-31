---
description: В этом разделе показано, как загрузить IWICBitmapFrameDecode из ресурса приложения.
ms.assetid: 2260ad3a-44d4-4fe2-aa8c-608ffc11fbfb
title: Загрузка растрового изображения из ресурса (компонент Windows Imaging Component)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb33ad57b3b9dac1cb5d98719c681adb38c11de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910427"
---
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a><span data-ttu-id="896db-103">Загрузка растрового изображения из ресурса (компонент Windows Imaging Component)</span><span class="sxs-lookup"><span data-stu-id="896db-103">How to Load a Bitmap from a Resource (Windows Imaging Component)</span></span>

<span data-ttu-id="896db-104">В этом разделе показано, как загрузить [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) из ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="896db-104">This topic demonstrates how to load an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) from an application resource.</span></span>

1.  <span data-ttu-id="896db-105">В файле определения ресурса приложения (. RC) определите ресурс.</span><span class="sxs-lookup"><span data-stu-id="896db-105">In the application resource definition (.rc) file , define the resource.</span></span> <span data-ttu-id="896db-106">В следующем примере определяется `Image` ресурс с именем `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="896db-106">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="896db-107">Ресурс будет добавлен в ресурсы приложения при сборке приложения.</span><span class="sxs-lookup"><span data-stu-id="896db-107">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="896db-108">Загрузите ресурс из приложения.</span><span class="sxs-lookup"><span data-stu-id="896db-108">Load the resource from the application.</span></span>

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

    

3.  <span data-ttu-id="896db-109">Блокировка ресурса и получение размера.</span><span class="sxs-lookup"><span data-stu-id="896db-109">Lock the resource and get the size.</span></span>

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

    

4.  <span data-ttu-id="896db-110">Используйте метод [**креатестреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) для создания объекта [**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) и его инициализации с помощью указателя памяти изображения.</span><span class="sxs-lookup"><span data-stu-id="896db-110">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

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

    

5.  <span data-ttu-id="896db-111">Создайте [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из нового объекта потока с помощью метода [**креатедекодерфромстреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="896db-111">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object by using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

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

    

6.  <span data-ttu-id="896db-112">Получение [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) из декодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="896db-112">Retrieve an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) from the decoded image.</span></span>

    ```C++
    // Retrieve the initial frame.
    if (SUCCEEDED(hr)){
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="896db-113">Этот код извлекает только первый кадр ( `0` ) изображения.</span><span class="sxs-lookup"><span data-stu-id="896db-113">This code only retrieves the first (`0`) frame of the image.</span></span> <span data-ttu-id="896db-114">Для изображений с несколькими кадрами используйте [**жетфрамекаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) , чтобы определить количество кадров в изображении.</span><span class="sxs-lookup"><span data-stu-id="896db-114">For multi-framed images, use [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) to determine the number of frames in the image.</span></span>

## <a name="see-also"></a><span data-ttu-id="896db-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="896db-115">See Also</span></span>

[<span data-ttu-id="896db-116">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="896db-116">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="896db-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="896db-117">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="896db-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="896db-118">Samples</span></span>](-wic-samples.md)


 

 



