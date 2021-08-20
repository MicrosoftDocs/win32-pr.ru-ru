---
description: Настройка кодировщика WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Настройка кодировщика WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39001edd5901d09bc618fe92d251070d24633fb94812a9c2696b11866f3cb9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880548"
---
# <a name="configuring-a-wmv-encoder"></a>Настройка кодировщика WMV

чтобы создать допустимый тип выходных данных для кодировщика Windows Media Video (WMV), необходимо иметь следующие сведения:

-   Формат несжатого видео, которое будет кодироваться.
-   Подтип видео, репесентс закодированный формат WMV. См. раздел [GUID подтипа видео](video-subtype-guids.md).
-   Целевая скорость потока в закодированном потоке.
-   Свойства конфигурации, заданные для кодировщика.

свойства конфигурации описаны в документации по api-кодекам Windows Media Audio, Video и DSP. Дополнительные сведения см. в разделе "Свойства потока видео" раздела [Свойства кодировки](configuring-the-encoder.md).

Чтобы получить допустимый тип выходных данных для кодировщика, выполните следующие действия.

1.  Используйте функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) или [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) для создания экземпляра кодировщика.
2.  Запросите кодировщик для интерфейса **ипропертисторе** .
3.  Используйте интерфейс **ипропертисторе** для настройки кодировщика.
4.  Вызовите [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , чтобы задать несжатый тип видео в кодировщике.
5.  Вызовите метод [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить список форматов сжатия из кодировщика. Кодировщики WMV не возвращают полный тип носителя из этого метода. В типах носителей отсутствуют два фрагмента информации:

    -   Целевая скорость.
    -   Данные частного кодека из кодировщика.

    Перед установкой типа выходных данных кодировщика необходимо добавить оба этих элемента к типу носителя.

6.  Чтобы указать целевую скорость, задайте атрибут [**" \_ \_ Средняя \_ скорость MF MT**](mf-mt-avg-bitrate-attribute.md) " для типа носителя.
7.  Добавьте данные частного кодека в тип мультимедиа, как описано в следующем разделе.
8.  Вызовите [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать тип сжатия мультимедиа для кодировщика.

### <a name="private-codec-data"></a>Данные частного кодека

Данные частного кодека — это непрозрачная структура данных, которую необходимо получить из кодировщика WMV и добавить к типу сжатия, прежде чем задавать тип сжатия кодировщика. чтобы получить конфиденциальные данные, необходимо использовать интерфейс **ивмкодекприватедата** , описанный в пакете SDK для Windows Media Format 11.

Чтобы получить данные частного кодека, выполните следующие действия.

1.  Вызовите [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить тип мультимедиа из кодировщика. (Это шаг 6 из предыдущего раздела.)
2.  Укажите скорость назначения, задав атрибут " [**\_ \_ Средняя \_ скорость MF MT**](mf-mt-avg-bitrate-attribute.md) " для типа носителя.
3.  преобразуйте тип мультимедиа в [**DMO структуру \_ \_ типа мультимедиа**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) , вызвав функцию [**мфинитаммедиатипефроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .
4.  Запросите кодировщик для интерфейса **ивмкодекприватедата** .
5.  вызовите метод **ивмкодекприватедата:: сетпартиалаутпуттипе** , передав преобразованную структуру [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .
6.  Вызовите метод **ивмкодекприватедата:: жетприватедата** дважды, один раз, чтобы получить размер буфера для закрытых данных, а затем скопируйте данные в буфер.
7.  Добавьте закрытые данные в тип мультимедиа, задав атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) в типе.

В следующем расширенном примере показано, как создать формат сжатия WMV из несжатого видео типа:


```C++
#include <wmcodecdsp.h>
#include <Wmsdk.h>
#include <Dmo.h>
#include <mfapi.h>
#include <uuids.h>

#include <mfidl.h>
#include <mftransform.h>
#include <mferror.h>

#pragma comment(lib, "Msdmo")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "strmiids")
#pragma comment(lib, "propsys")

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn, 
    REFGUID subtype,
    UINT32 TargetBitrate, 
    IPropertyStore *pEncoderProps, 
    IMFMediaType **ppEncodingType,
    DWORD mftEnumFlags = MFT_ENUM_FLAG_SYNCMFT
    );

HRESULT CreateVideoEncoder(REFGUID subtype, DWORD mftEnumFlags, IMFTransform **ppMFT);
HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut);
HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest);

//
// GetEncodedVideoType
// Given an uncompressed video type, finds a suitable WMV type.
//

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn,          // Uncompressed format
    REFGUID subtype,                // Compression format
    UINT32 TargetBitrate,           // Target bit rate
    IPropertyStore *pEncoderProps,  // Encoder properties (can be NULL)
    IMFMediaType **ppEncodingType,  // Receives the WMV type.
    DWORD mftEnumFlags              // MFTEnumEx flags
    )
{
    HRESULT hr = S_OK;

    IMFTransform *pMFT = NULL;
    IPropertyStore *pPropStore = NULL;
    IMFMediaType *pTypeOut = NULL;

    // Instantiate the encoder
    hr = CreateVideoEncoder(subtype, mftEnumFlags, &pMFT);

    // Copy the properties to the encoder.

    if (SUCCEEDED(hr))
    {
        if (pEncoderProps)
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPropStore));

            if (SUCCEEDED(hr))
            {
                hr = CopyPropertyStore(pEncoderProps, pPropStore);
            }
        }
    }

    // Set the uncompressed type.
    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetInputType(0, pTypeIn, 0);
    }

    // Get the partial output type
    if (SUCCEEDED(hr))
    {
        hr = pMFT->GetOutputAvailableType(0, 0, &pTypeOut);
    }

    // Set the bit rate.
    // You must set this before getting the codec private data.

    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetUINT32(MF_MT_AVG_BITRATE, TargetBitrate);   
    }

    if (SUCCEEDED(hr))
    {
        hr = AddPrivateData(pMFT, pTypeOut);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetOutputType(0, pTypeOut, 0);
    }

    if (SUCCEEDED(hr))
    {
        *ppEncodingType = pTypeOut;
        (*ppEncodingType)->AddRef();
    }

    SafeRelease(&pMFT);
    SafeRelease(&pPropStore);
    SafeRelease(&pTypeOut);
    return hr;
}
```



Функция Креатевидеоенкодер создает кодировщик видео для указанного подтипа видео, например **мфвидеоформат \_ WMV3**:


```C++
//
// CreateVideoEncoder
// Creates a video encoder for a specified video subtype.
//

HRESULT CreateVideoEncoder(
    REFGUID subtype,            // Encoding subtype.
    DWORD mftEnumFlags,         // Flags for MFTEnumEx
    IMFTransform **ppMFT        // Receives a pointer to the encoder.
    )
{
    HRESULT hr = S_OK;
    IMFTransform *pMFT = NULL;

    MFT_REGISTER_TYPE_INFO info;
    info.guidMajorType = MFMediaType_Video;
    info.guidSubtype = subtype;

    IMFActivate **ppActivates = NULL;    
    UINT32 count = 0;

    hr = MFTEnumEx(
        MFT_CATEGORY_VIDEO_ENCODER,
        mftEnumFlags | MFT_ENUM_FLAG_SORTANDFILTER,
        NULL,
        &info,
        &ppActivates,
        &count
        );

    if (count == 0)
    {
        hr = E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        hr = ppActivates[0]->ActivateObject(
            __uuidof(IMFTransform),
            (void**)&pMFT
            );
    }

    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    // Clean up

    for (DWORD i = 0; i < count; i++)
    {
        ppActivates[i]->Release();
    }
    CoTaskMemFree(ppActivates);
    SafeRelease(&pMFT);
    return hr;
}
```



Функция Аддприватедата добавляет данные частного кодека в тип сжатия:


```C++
//
// AddPrivateData
// Appends the private codec data to a media type.
//
// pMFT: The video encoder
// pTypeOut: A video type from the encoder's type list.
//
// The function modifies pTypeOut by adding the codec data.
//

HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
{
    HRESULT hr = S_OK;
    ULONG cbData = 0;
    BYTE *pData = NULL;

    IWMCodecPrivateData *pPrivData = NULL;

    DMO_MEDIA_TYPE mtOut = { 0 };

    // Convert the type to a DMO type.
    hr = MFInitAMMediaTypeFromMFMediaType(
        pTypeOut, 
        FORMAT_VideoInfo, 
        (AM_MEDIA_TYPE*)&mtOut
        );
    
    if (SUCCEEDED(hr))
    {
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
    }

    if (SUCCEEDED(hr))
    {
        hr = pPrivData->SetPartialOutputType(&mtOut);
    }

    //
    // Get the private codec data
    //

    // First get the buffer size.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(NULL, &cbData);
    }

    if (SUCCEEDED(hr))
    {
        pData = new BYTE[cbData];

        if (pData == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Now get the data.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(pData, &cbData);
    }

    // Add the data to the media type.
    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
    }

    delete [] pData;
    MoFreeMediaType(&mtOut);
    SafeRelease(&pPrivData);
    return hr;
}
```



Функция Копипропертисторе — это вспомогательная функция, которая копирует свойства из одного хранилища свойств в другое:


```C++
//
// CopyPropertyStore
// Helper function to copy properties from one property
// store to another property store.
//

HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest)
{
    HRESULT hr = S_OK;
    DWORD cProps = 0;

    PROPERTYKEY key;
    PROPVARIANT var;

    PropVariantInit(&var);

    hr = pSrc->GetCount(&cProps);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cProps; i++)
        {
            hr = pSrc->GetAt(i, &key);

            if (FAILED(hr)) { break; }

            hr = pSrc->GetValue(key, &var);

            if (FAILED(hr)) { break; }

            hr = pDest->SetValue(key, var);

            if (FAILED(hr)) { break; }

            PropVariantClear(&var);
        }
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание экземпляра MFT для кодировщика](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Кодировщики мультимедиа](windows-media-encoders.md)
</dt> </dl>

 

 
