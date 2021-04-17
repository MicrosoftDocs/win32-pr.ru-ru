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
# <a name="how-to-create-a-decoder-using-an-image-filename"></a>Создание декодера с помощью имени файла образа

В этом разделе описывается создание декодера точечных рисунков с помощью имени файла образа.

Создание декодера точечных рисунков с помощью имени файла образа

1.  Создайте объект [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) для создания объектов компонента Windows Imaging Component (WIC).

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

4.  Обработка кадра изображения. Дополнительные сведения об объектах [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) см. в разделе [Обзор источников битовой карты](-wic-bitmapsources.md).

## <a name="see-also"></a>См. также:

[Руководство по программированию](-wic-programming-guide.md)


[Ссылки](-wic-codec-reference.md)


[Примеры](-wic-samples.md)


 

 



