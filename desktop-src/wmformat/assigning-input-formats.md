---
title: Назначение форматов входных данных
description: Назначение форматов входных данных
ms.assetid: 44c4ed7e-b35e-4ab5-9975-021f343dab6a
keywords:
- Расширенный системный формат (ASF), назначение входных форматов
- ASF (Расширенный системный формат), назначение форматов входных данных
- профили, назначение входных форматов
- кодеки, назначение форматов входных данных
- Формат расширенных систем (ASF), назначения формата ввода
- ASF (Расширенный системный формат), назначения формата ввода
- профили, назначения формата входных данных
- кодеки, назначения формата ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6f87ec74bc5d3750d65ecc91e2df4640a6ed02c9e9a9425b27897e70f825983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840334"
---
# <a name="assigning-input-formats"></a>Назначение форматов входных данных

После определения формата входных данных, который соответствует данным, его можно задать для использования средством записи путем вызова [**ивмвритер:: сетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).

Для видеопотоков необходимо задать размер кадров во входных образцах. В следующем примере кода показано, как настроить и задать входные данные видео. Он использует функцию **финдинпутформат** , определенную в разделе [to Enumerate input formats](to-enumerate-input-formats.md) , для получения формата входных данных для 24-разрядного видео RGB. Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


```C++
HRESULT ConfigureVideoInput(IWMWriter* pWriter,
                            DWORD dwInput,
                            GUID guidSubType,
                            LONG lFrameWidth,
                            LONG lFrameHeight)
{
    DWORD   cbSize = 0;
    LONG    lStride = 0;

    IWMInputMediaProps* pProps  = NULL;
    WM_MEDIA_TYPE*      pType   = NULL;
    WMVIDEOINFOHEADER*  pVidHdr = NULL;
    BITMAPINFOHEADER*   pbmi    = NULL;

    // Get the base input format for the required subtype.
    HRESULT hr = FindInputFormat(pWriter, dwInput, guidSubType, &pProps);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Get the size of the media type structure.
    hr = pProps->GetMediaType(NULL, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Allocate memory for the media type structure.
    pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
    if (pType == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }
    
    // Get the media type structure.
    hr = pProps->GetMediaType(pType, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Adjust the format to match your source images.

    // First set pointers to the video structures.
    pVidHdr = (WMVIDEOINFOHEADER*) pType->pbFormat;
    pbmi  = &(pVidHdr->bmiHeader);
        
    pbmi->biWidth  = lFrameWidth;  
    pbmi->biHeight = lFrameHeight;
    
    // Stride = (width * bytes/pixel), rounded to the next DWORD boundary.
    lStride = (lFrameWidth * (pbmi->biBitCount / 8) + 3) & ~3;


    // Image size = stride * height. 
    pbmi->biSizeImage = lFrameHeight * lStride;

    // Apply the adjusted type to the video input. 
    hr = pProps->SetMediaType(pType);
    if (FAILED(hr))
    {
        goto Exit;
    }

    hr = pWriter->SetInputProps(dwInput, pProps);

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```





## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Работа с входными данными**](working-with-inputs.md)
</dt> </dl>

 

 




