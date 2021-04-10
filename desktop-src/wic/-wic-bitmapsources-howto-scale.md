---
description: В этом разделе показано, как масштабировать IWICBitmapSource с помощью компонента Ивикбитмапскалер.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Масштабирование источника точечного рисунка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737f72014929065bc63ec9c6021b05e38799d06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144740"
---
# <a name="how-to-scale-a-bitmap-source"></a><span data-ttu-id="78e96-103">Масштабирование источника точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="78e96-103">How to Scale a Bitmap Source</span></span>

<span data-ttu-id="78e96-104">В этом разделе показано, как масштабировать [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) с помощью компонента [**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="78e96-104">This topic demonstrates how to scale an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) component.</span></span>

<span data-ttu-id="78e96-105">Масштабирование источника точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="78e96-105">To scale a bitmap source</span></span>

1.  <span data-ttu-id="78e96-106">Создайте объект [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="78e96-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="78e96-107">Используйте метод [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) для создания [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из файла образа.</span><span class="sxs-lookup"><span data-stu-id="78e96-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapScaler *pIScaler = NULL;


    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="78e96-108">Получите первый [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) изображения.</span><span class="sxs-lookup"><span data-stu-id="78e96-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="78e96-109">Формат файла JPEG поддерживает только один кадр.</span><span class="sxs-lookup"><span data-stu-id="78e96-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="78e96-110">Поскольку файл в этом примере является JPEG-файлом, используется первый кадр ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="78e96-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="78e96-111">Сведения о форматах изображений, имеющих несколько кадров, см. [в разделе Получение кадров изображения](-wic-bitmapsources-howto-retrieveimageframes.md) для доступа к каждому кадру изображения.</span><span class="sxs-lookup"><span data-stu-id="78e96-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="78e96-112">Создайте [**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) , который будет использоваться для масштабирования изображения.</span><span class="sxs-lookup"><span data-stu-id="78e96-112">Create the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) to use for the image scaling.</span></span>

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  <span data-ttu-id="78e96-113">Инициализируйте объект Scale, используя данные изображения кадра точечного рисунка с половиной размера.</span><span class="sxs-lookup"><span data-stu-id="78e96-113">Initialize the scaler object with the image data of the bitmap frame at half the size.</span></span>

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  <span data-ttu-id="78e96-114">Рисование или обработка источника масштабируемого растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="78e96-114">Draw or process the scaled bitmap source.</span></span>

    <span data-ttu-id="78e96-115">На следующем рисунке демонстрируется масштабирование изображений.</span><span class="sxs-lookup"><span data-stu-id="78e96-115">The following illustration demonstrates imaging scaling.</span></span> <span data-ttu-id="78e96-116">Исходное изображение слева — 200 x 130 пикселей.</span><span class="sxs-lookup"><span data-stu-id="78e96-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="78e96-117">Изображение справа является исходным изображением, масштабированным до половины размера.</span><span class="sxs-lookup"><span data-stu-id="78e96-117">The image on the right is the original image scaled to half the size.</span></span>

    ![Иллюстрация, демонстрирующая масштабирование изображения до меньшего размера](graphics/scaledregion.png)

## <a name="see-also"></a><span data-ttu-id="78e96-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="78e96-119">See Also</span></span>

[<span data-ttu-id="78e96-120">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="78e96-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="78e96-121">Ссылки</span><span class="sxs-lookup"><span data-stu-id="78e96-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="78e96-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="78e96-122">Samples</span></span>](-wic-samples.md)


 

 



