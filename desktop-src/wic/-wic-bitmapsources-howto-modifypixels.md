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
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a>Изменение пикселов источника точечного рисунка

В этом разделе показано, как изменить пикселы источника точечного рисунка с помощью компонентов [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) и [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

Изменение пикселов источника точечного рисунка

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

4.  Создайте [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) из ранее полученного кадра образа.

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

    

5.  Получение [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) для указанного прямоугольника [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  Обработка данных пикселей, которые теперь заблокированы объектом [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

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

    

    Чтобы разблокировать [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), вызовите метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для всех объектов [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) , связанных с **ивикбитмап**.

7.  Очистка созданных объектов.

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a>См. также:

[Руководство по программированию](-wic-programming-guide.md)


[Ссылки](-wic-codec-reference.md)


[Примеры](-wic-samples.md)


 

 
