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
ms.openlocfilehash: 5c6ad1bcdf161b335d9367d7de4df84b7eb2e6ea
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532957"
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





## <a name="related-topics"></a>См. также

<dl> <dt>

[**Работа с входными данными**](working-with-inputs.md)
</dt> </dl>

 

 




