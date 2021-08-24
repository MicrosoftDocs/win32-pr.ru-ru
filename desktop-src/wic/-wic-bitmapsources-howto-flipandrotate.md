---
description: В этом разделе показано, как повернуть IWICBitmapSource с помощью компонента Ивикбитмапфлипротатор.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Отражение и поворот исходного растрового изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a61a1546f5a0191d2e20cc3079af3e4d772e6d2c3c07a5dd1e1e4aa331dc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331553"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a>Отражение и поворот исходного растрового изображения

В этом разделе показано, как повернуть [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) с помощью компонента [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .

Отражение и поворот исходного растрового изображения

1.  создайте объект [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента обработки изображений Windows (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Используйте метод [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) для создания [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) из файла образа.

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

    

3.  Получите первый [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) изображения.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Формат файла JPEG поддерживает только один кадр. Поскольку файл в этом примере является JPEG-файлом, используется первый кадр ( `0` ). Сведения о форматах изображений, имеющих несколько кадров, см. [в разделе Получение кадров изображения](-wic-bitmapsources-howto-retrieveimageframes.md) для доступа к каждому кадру изображения.

4.  Создайте [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) , который будет использоваться для зеркального отображения изображения.

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  Инициализируйте объект отражения/вращения, используя данные изображения кадра растрового изображения, перевернутого горизонтально (вдоль вертикальной оси y).

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

    

    Дополнительные параметры вращения и зеркального отражения см. в разделе [**викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

6.  Рисование или обработка источника отраженного растрового изображения.

    > [!Note]  
    > Интерфейс [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) наследуется от интерфейса [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , поэтому можно использовать инициализированный объект перелистывания или поворота в любом месте, где принимается **IWICBitmapSource**.

     

    На следующем рисунке показано зеркальное отображение изображений горизонтально (вдоль вертикальной оси x).

    ![Иллюстрация, демонстрирующая горизонтальное перелистывание (вдоль оси x веритал) изображения](graphics/fliphorizontal.png)

## <a name="see-also"></a>См. также

[Руководство по программированию](-wic-programming-guide.md)


[Ссылки](-wic-codec-reference.md)


[Примеры](-wic-samples.md)


 

 



