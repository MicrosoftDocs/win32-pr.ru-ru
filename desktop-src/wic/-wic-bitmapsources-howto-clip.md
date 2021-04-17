---
description: В этом разделе показано, как получить прямоугольную часть IWICBitmapSource с помощью компонента Ивикбитмапклиппер.
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: Как обрезать источник точечного рисунка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558188"
---
# <a name="how-to-clip-a-bitmap-source"></a><span data-ttu-id="75937-103">Как обрезать источник точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="75937-103">How to Clip a Bitmap Source</span></span>

<span data-ttu-id="75937-104">В этом разделе показано, как получить прямоугольную часть [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) с помощью компонента [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="75937-104">This topic demonstrates how to obtain a rectangular portion of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using an [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) component.</span></span>

<span data-ttu-id="75937-105">Обрезка источника точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="75937-105">To clip a bitmap source</span></span>

1.  <span data-ttu-id="75937-106">Создайте объект [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="75937-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="75937-107">Используйте метод [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) для создания [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из файла образа.</span><span class="sxs-lookup"><span data-stu-id="75937-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="75937-108">Получите первый [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) изображения.</span><span class="sxs-lookup"><span data-stu-id="75937-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="75937-109">Формат файла JPEG поддерживает только один кадр.</span><span class="sxs-lookup"><span data-stu-id="75937-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="75937-110">Поскольку файл в этом примере является JPEG-файлом, используется первый кадр ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="75937-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="75937-111">Сведения о форматах изображений, имеющих несколько кадров, см. [в разделе Получение кадров изображения](-wic-bitmapsources-howto-retrieveimageframes.md) для доступа к каждому кадру изображения.</span><span class="sxs-lookup"><span data-stu-id="75937-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="75937-112">Создайте [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) , который будет использоваться для вырезания изображения.</span><span class="sxs-lookup"><span data-stu-id="75937-112">Create the [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) to use for the image clipping.</span></span>

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  <span data-ttu-id="75937-113">Инициализируйте объект Clipper данными изображения в заданном прямоугольнике рамки точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="75937-113">Initialize the clipper object with the image data within the given rectangle of the bitmap frame.</span></span>

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  <span data-ttu-id="75937-114">Рисование или обработка обрезанного изображения.</span><span class="sxs-lookup"><span data-stu-id="75937-114">Draw or process the clipped image.</span></span>

    <span data-ttu-id="75937-115">На следующем рисунке показана обрезка изображения.</span><span class="sxs-lookup"><span data-stu-id="75937-115">The following illustration demonstrates imaging clipping.</span></span> <span data-ttu-id="75937-116">Исходное изображение слева — 200 x 130 пикселей.</span><span class="sxs-lookup"><span data-stu-id="75937-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="75937-117">Изображение справа — это исходное изображение, обрезанное до прямоугольника, определенного как `{20,20,100,100}` .</span><span class="sxs-lookup"><span data-stu-id="75937-117">The image on the right is the original image clipped to a rectangle defined as `{20,20,100,100}`.</span></span>

    ![Иллюстрация обрезки изображения](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a><span data-ttu-id="75937-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="75937-119">See Also</span></span>

[<span data-ttu-id="75937-120">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="75937-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="75937-121">Ссылки</span><span class="sxs-lookup"><span data-stu-id="75937-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="75937-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="75937-122">Samples</span></span>](-wic-samples.md)


 

 



