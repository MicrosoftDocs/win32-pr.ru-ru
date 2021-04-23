---
description: В этом разделе показано, как повернуть IWICBitmapSource с помощью компонента Ивикбитмапфлипротатор.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Отражение и поворот исходного растрового изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f6a805144025f185a4f4793fc4fafb27d7695a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144746"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a><span data-ttu-id="f025a-103">Отражение и поворот исходного растрового изображения</span><span class="sxs-lookup"><span data-stu-id="f025a-103">How to Flip and Rotate a Bitmap Source</span></span>

<span data-ttu-id="f025a-104">В этом разделе показано, как повернуть [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) с помощью компонента [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="f025a-104">This topic demonstrates how to rotate an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using an [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) component.</span></span>

<span data-ttu-id="f025a-105">Отражение и поворот исходного растрового изображения</span><span class="sxs-lookup"><span data-stu-id="f025a-105">To flip and rotate a bitmap source</span></span>

1.  <span data-ttu-id="f025a-106">Создайте объект [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="f025a-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="f025a-107">Используйте метод [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) для создания [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из файла образа.</span><span class="sxs-lookup"><span data-stu-id="f025a-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="f025a-108">Получите первый [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) изображения.</span><span class="sxs-lookup"><span data-stu-id="f025a-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="f025a-109">Формат файла JPEG поддерживает только один кадр.</span><span class="sxs-lookup"><span data-stu-id="f025a-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="f025a-110">Поскольку файл в этом примере является JPEG-файлом, используется первый кадр ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="f025a-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="f025a-111">Сведения о форматах изображений, имеющих несколько кадров, см. [в разделе Получение кадров изображения](-wic-bitmapsources-howto-retrieveimageframes.md) для доступа к каждому кадру изображения.</span><span class="sxs-lookup"><span data-stu-id="f025a-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="f025a-112">Создайте [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) , который будет использоваться для зеркального отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="f025a-112">Create the [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) to use for flipping the image.</span></span>

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  <span data-ttu-id="f025a-113">Инициализируйте объект отражения/вращения, используя данные изображения кадра растрового изображения, перевернутого горизонтально (вдоль вертикальной оси y).</span><span class="sxs-lookup"><span data-stu-id="f025a-113">Initialize the flip/rotator object with the image data of the bitmap frame flipped horizontally (along the vertical y-axis).</span></span>

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    <span data-ttu-id="f025a-114">Дополнительные параметры вращения и зеркального отражения см. в разделе [**викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="f025a-114">See [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) for additional rotations and flipping options.</span></span>

6.  <span data-ttu-id="f025a-115">Рисование или обработка источника отраженного растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="f025a-115">Draw or process the flipped bitmap source.</span></span>

    > [!Note]  
    > <span data-ttu-id="f025a-116">Интерфейс [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) наследуется от интерфейса [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , поэтому можно использовать инициализированный объект перелистывания или поворота в любом месте, где принимается **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="f025a-116">The [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) interface inherits from the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, so you can use the initialized flip/rotator object anywhere that accepts a **IWICBitmapSource**.</span></span>

     

    <span data-ttu-id="f025a-117">На следующем рисунке показано зеркальное отображение изображений горизонтально (вдоль вертикальной оси x).</span><span class="sxs-lookup"><span data-stu-id="f025a-117">The following illustration demonstrates flipping an imaging horizontally (along the vertical x-axis).</span></span>

    ![Иллюстрация, демонстрирующая горизонтальное перелистывание (вдоль оси x веритал) изображения](graphics/fliphorizontal.png)

## <a name="see-also"></a><span data-ttu-id="f025a-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="f025a-119">See Also</span></span>

[<span data-ttu-id="f025a-120">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="f025a-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="f025a-121">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f025a-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="f025a-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="f025a-122">Samples</span></span>](-wic-samples.md)


 

 



