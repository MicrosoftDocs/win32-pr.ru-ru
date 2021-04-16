---
description: В этом разделе показано, как изменить пикселы источника точечного рисунка с помощью компонентов Ивикбитмап и Ивикбитмаплокк.
ms.assetid: a08af015-bc42-4a31-af03-106714b08d08
title: Изменение пикселов источника точечного рисунка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be623d540fcd313476ea5c7ec5e724231d33aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702404"
---
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a><span data-ttu-id="51616-103">Изменение пикселов источника точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="51616-103">How to Modify the Pixels of a Bitmap Source</span></span>

<span data-ttu-id="51616-104">В этом разделе показано, как изменить пикселы источника точечного рисунка с помощью компонентов [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) и [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="51616-104">This topic demonstrates how to modify the pixels of a bitmap source using the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) and [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) components.</span></span>

<span data-ttu-id="51616-105">Изменение пикселов источника точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="51616-105">To modify the pixels of a bitmap source</span></span>

1.  <span data-ttu-id="51616-106">Создайте объект [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="51616-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="51616-107">Используйте метод [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) для создания [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из файла образа.</span><span class="sxs-lookup"><span data-stu-id="51616-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="51616-108">Получите первый [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) изображения.</span><span class="sxs-lookup"><span data-stu-id="51616-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="51616-109">Формат файла JPEG поддерживает только один кадр.</span><span class="sxs-lookup"><span data-stu-id="51616-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="51616-110">Поскольку файл в этом примере является JPEG-файлом, используется первый кадр ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="51616-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="51616-111">Сведения о форматах изображений, имеющих несколько кадров, см. [в разделе Получение кадров изображения](-wic-bitmapsources-howto-retrieveimageframes.md) для доступа к каждому кадру изображения.</span><span class="sxs-lookup"><span data-stu-id="51616-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="51616-112">Создайте [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) из ранее полученного кадра образа.</span><span class="sxs-lookup"><span data-stu-id="51616-112">Create an [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) from the previously obtained image frame.</span></span>

    ```C++
    IWICBitmap *pIBitmap = NULL;
    IWICBitmapLock *pILock = NULL;

    UINT uiWidth = 10;
    UINT uiHeight = 10;

    WICRect rcLock = { 0, 0, uiWidth, uiHeight };

    // Create the bitmap from the image frame.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFromSource(
          pIDecoderFrame,          // Create a bitmap from the image frame
          WICBitmapCacheOnDemand,  // Cache metadata when needed
          &pIBitmap);              // Pointer to the bitmap
    }
    ```

    

5.  <span data-ttu-id="51616-113">Получение [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) для указанного прямоугольника [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span><span class="sxs-lookup"><span data-stu-id="51616-113">Obtain an [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) for a specified rectangle of the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span></span>

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  <span data-ttu-id="51616-114">Обработка данных пикселей, которые теперь заблокированы объектом [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="51616-114">Process the pixel data that is now locked by the [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

    ```C++
       if (SUCCEEDED(hr))
       {
          UINT cbBufferSize = 0;
          BYTE *pv = NULL;

          // Retrieve a pointer to the pixel data.
          if (SUCCEEDED(hr))
          {
             hr = pILock->GetDataPointer(&cbBufferSize, &pv);
          }
          
          // Pixel manipulation using the image data pointer pv.
          // ...

          // Release the bitmap lock.
          SafeRelease(&pILock);
       }
    }
    ```

    

    <span data-ttu-id="51616-115">Чтобы разблокировать [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), вызовите метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для всех объектов [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) , связанных с **ивикбитмап**.</span><span class="sxs-lookup"><span data-stu-id="51616-115">To unlock the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) objects associated with the **IWICBitmap**.</span></span>

7.  <span data-ttu-id="51616-116">Очистка созданных объектов.</span><span class="sxs-lookup"><span data-stu-id="51616-116">Clean up created objects.</span></span>

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a><span data-ttu-id="51616-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="51616-117">See Also</span></span>

[<span data-ttu-id="51616-118">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="51616-118">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="51616-119">Ссылки</span><span class="sxs-lookup"><span data-stu-id="51616-119">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="51616-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="51616-120">Samples</span></span>](-wic-samples.md)


 

 
