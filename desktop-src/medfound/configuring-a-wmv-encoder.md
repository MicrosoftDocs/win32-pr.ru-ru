---
description: Настройка кодировщика WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Настройка кодировщика WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6324071257dd9d56e33d1dc6ece4886ee73661ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143216"
---
# <a name="configuring-a-wmv-encoder"></a><span data-ttu-id="b215e-103">Настройка кодировщика WMV</span><span class="sxs-lookup"><span data-stu-id="b215e-103">Configuring a WMV Encoder</span></span>

<span data-ttu-id="b215e-104">Чтобы создать допустимый тип выходных данных для кодировщика видео Windows Media (WMV), необходимо иметь следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b215e-104">To create a valid output type for a Windows Media Video (WMV) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="b215e-105">Формат несжатого видео, которое будет кодироваться.</span><span class="sxs-lookup"><span data-stu-id="b215e-105">The format of the uncompressed video that you will encode.</span></span>
-   <span data-ttu-id="b215e-106">Подтип видео, репесентс закодированный формат WMV.</span><span class="sxs-lookup"><span data-stu-id="b215e-106">The video subtype that repesents the encoded WMV format.</span></span> <span data-ttu-id="b215e-107">См. раздел [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b215e-107">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="b215e-108">Целевая скорость потока в закодированном потоке.</span><span class="sxs-lookup"><span data-stu-id="b215e-108">The target bitrate for the encoded stream.</span></span>
-   <span data-ttu-id="b215e-109">Свойства конфигурации, заданные для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b215e-109">The configuration properties to set on the encoder.</span></span>

<span data-ttu-id="b215e-110">Свойства конфигурации описаны в документации по API-интерфейсам аудио-и видеокодеков Windows Media и DSP.</span><span class="sxs-lookup"><span data-stu-id="b215e-110">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="b215e-111">Дополнительные сведения см. в разделе "Свойства потока видео" раздела [Свойства кодировки](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="b215e-111">For more information, see "Video Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

<span data-ttu-id="b215e-112">Чтобы получить допустимый тип выходных данных для кодировщика, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b215e-112">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="b215e-113">Используйте функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) или [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) для создания экземпляра кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b215e-113">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="b215e-114">Запросите кодировщик для интерфейса **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="b215e-114">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="b215e-115">Используйте интерфейс **ипропертисторе** для настройки кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b215e-115">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="b215e-116">Вызовите [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , чтобы задать несжатый тип видео в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="b215e-116">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed video type on the encoder.</span></span>
5.  <span data-ttu-id="b215e-117">Вызовите метод [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить список форматов сжатия из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b215e-117">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of compression formats from the encoder.</span></span> <span data-ttu-id="b215e-118">Кодировщики WMV не возвращают полный тип носителя из этого метода.</span><span class="sxs-lookup"><span data-stu-id="b215e-118">The WMV encoders do not return a complete media type from this method.</span></span> <span data-ttu-id="b215e-119">В типах носителей отсутствуют два фрагмента информации:</span><span class="sxs-lookup"><span data-stu-id="b215e-119">The media types are missing two pieces of information:</span></span>

    -   <span data-ttu-id="b215e-120">Целевая скорость.</span><span class="sxs-lookup"><span data-stu-id="b215e-120">The target bitrate.</span></span>
    -   <span data-ttu-id="b215e-121">Данные частного кодека из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b215e-121">Private codec data from the encoder.</span></span>

    <span data-ttu-id="b215e-122">Перед установкой типа выходных данных кодировщика необходимо добавить оба этих элемента к типу носителя.</span><span class="sxs-lookup"><span data-stu-id="b215e-122">Before setting the output type on the encoder, you must add both of these items to the media type.</span></span>

6.  <span data-ttu-id="b215e-123">Чтобы указать целевую скорость, задайте атрибут [**" \_ \_ Средняя \_ скорость MF MT**](mf-mt-avg-bitrate-attribute.md) " для типа носителя.</span><span class="sxs-lookup"><span data-stu-id="b215e-123">To specify the target bitrate, set the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
7.  <span data-ttu-id="b215e-124">Добавьте данные частного кодека в тип мультимедиа, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="b215e-124">Add the private codec data to the media type, as explained in the next section.</span></span>
8.  <span data-ttu-id="b215e-125">Вызовите [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать тип сжатия мультимедиа для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b215e-125">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="private-codec-data"></a><span data-ttu-id="b215e-126">Данные частного кодека</span><span class="sxs-lookup"><span data-stu-id="b215e-126">Private Codec Data</span></span>

<span data-ttu-id="b215e-127">Данные частного кодека — это непрозрачная структура данных, которую необходимо получить из кодировщика WMV и добавить к типу сжатия, прежде чем задавать тип сжатия кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b215e-127">The private codec data is an opaque data structure that you must get from the WMV encoder and add to the compression type, before setting the compression type on the encoder.</span></span> <span data-ttu-id="b215e-128">Для получения закрытых данных необходимо использовать интерфейс **ивмкодекприватедата** , который описан в пакете SDK для Windows Media Format 11.</span><span class="sxs-lookup"><span data-stu-id="b215e-128">To get the private data, you must use the **IWMCodecPrivateData** interface, which is documented in the Windows Media Format 11 SDK.</span></span>

<span data-ttu-id="b215e-129">Чтобы получить данные частного кодека, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b215e-129">To get the private codec data, perform the following steps:</span></span>

1.  <span data-ttu-id="b215e-130">Вызовите [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить тип мультимедиа из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b215e-130">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a media type from the encoder.</span></span> <span data-ttu-id="b215e-131">(Это шаг 6 из предыдущего раздела.)</span><span class="sxs-lookup"><span data-stu-id="b215e-131">(This is step 6 from the previous section.)</span></span>
2.  <span data-ttu-id="b215e-132">Укажите скорость назначения, задав атрибут " [**\_ \_ Средняя \_ скорость MF MT**](mf-mt-avg-bitrate-attribute.md) " для типа носителя.</span><span class="sxs-lookup"><span data-stu-id="b215e-132">Specify the target bitrate by setting the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
3.  <span data-ttu-id="b215e-133">Преобразуйте тип мультимедиа в структуру [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) , вызвав функцию [**мфинитаммедиатипефроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="b215e-133">Convert the media type into a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure by calling the [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) function.</span></span>
4.  <span data-ttu-id="b215e-134">Запросите кодировщик для интерфейса **ивмкодекприватедата** .</span><span class="sxs-lookup"><span data-stu-id="b215e-134">Query the encoder for the **IWMCodecPrivateData** interface.</span></span>
5.  <span data-ttu-id="b215e-135">Вызовите метод **ивмкодекприватедата:: сетпартиалаутпуттипе** , передав преобразованную структуру [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="b215e-135">Call the **IWMCodecPrivateData::SetPartialOutputType** method, passing in the converted [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span>
6.  <span data-ttu-id="b215e-136">Вызовите метод **ивмкодекприватедата:: жетприватедата** дважды, один раз, чтобы получить размер буфера для закрытых данных, а затем скопируйте данные в буфер.</span><span class="sxs-lookup"><span data-stu-id="b215e-136">Call the **IWMCodecPrivateData::GetPrivateData** method twice, once to get the size of the buffer for the private data, and once to copy the data into the buffer.</span></span>
7.  <span data-ttu-id="b215e-137">Добавьте закрытые данные в тип мультимедиа, задав атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) в типе.</span><span class="sxs-lookup"><span data-stu-id="b215e-137">Add the private data to the media type by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute on the type.</span></span>

<span data-ttu-id="b215e-138">В следующем расширенном примере показано, как создать формат сжатия WMV из несжатого видео типа:</span><span class="sxs-lookup"><span data-stu-id="b215e-138">The following extended example shows how to create a WMV compression format from an uncompressed video type:</span></span>


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



<span data-ttu-id="b215e-139">Функция Креатевидеоенкодер создает кодировщик видео для указанного подтипа видео, например **мфвидеоформат \_ WMV3**:</span><span class="sxs-lookup"><span data-stu-id="b215e-139">The CreateVideoEncoder function creates a video encoder for a specified video subtype, such as **MFVideoFormat\_WMV3**:</span></span>


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



<span data-ttu-id="b215e-140">Функция Аддприватедата добавляет данные частного кодека в тип сжатия:</span><span class="sxs-lookup"><span data-stu-id="b215e-140">The AddPrivateData function adds the private codec data to the compression type:</span></span>


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



<span data-ttu-id="b215e-141">Функция Копипропертисторе — это вспомогательная функция, которая копирует свойства из одного хранилища свойств в другое:</span><span class="sxs-lookup"><span data-stu-id="b215e-141">The CopyPropertyStore function is a helper function that copies properties from one property store to another:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b215e-142">См. также</span><span class="sxs-lookup"><span data-stu-id="b215e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b215e-143">Создание экземпляра MFT для кодировщика</span><span class="sxs-lookup"><span data-stu-id="b215e-143">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="b215e-144">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="b215e-144">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 
