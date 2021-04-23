---
description: Использование личных данных видеокодека
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Использование личных данных видеокодека (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e86fc31a50d2c4e553b5947717ea930698d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702024"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a><span data-ttu-id="5ae50-103">Использование личных данных видеокодека (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="5ae50-103">Using Video Codec Private Data (Microsoft Media Foundation)</span></span>

<span data-ttu-id="5ae50-104">Сжатые выходные данные, созданные кодеками Windows Media Video 9, не могут быть правильно распакованы без каких бы то ни было данных, предоставленных кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="5ae50-104">The compressed output produced by the Windows Media Video 9 codecs cannot be properly decompressed without some data provided by the encoder.</span></span> <span data-ttu-id="5ae50-105">Эти данные, называемые частными данными кодека, должны быть добавлены к выходному типу носителя.</span><span class="sxs-lookup"><span data-stu-id="5ae50-105">This data, called codec private data, must be appended to the output media type.</span></span> <span data-ttu-id="5ae50-106">Можно получить частные данные кодека, вызвав методы интерфейса [ивмкодекприватедата](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="5ae50-106">You can get the codec private data by calling the methods of the [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) interface.</span></span> <span data-ttu-id="5ae50-107">Передайте для [ивмкодекприватедата:: сетпартиалаутпуттипе](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype)структуру [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="5ae50-107">Pass the otherwise complete [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure to [IWMCodecPrivateData::SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span></span> <span data-ttu-id="5ae50-108">Затем вызовите метод [ивмкодекприватедата:: жетприватедата](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) дважды, один раз, чтобы получить размер данных, а затем скопируйте данные в буфер такого размера.</span><span class="sxs-lookup"><span data-stu-id="5ae50-108">Then call [IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) twice, once to get the size of the data, and then again to copy the data to a buffer of that size.</span></span> <span data-ttu-id="5ae50-109">Создайте новый буфер для хранения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) с добавленными закрытыми данными и скопируйте структуру и данные в этот буфер.</span><span class="sxs-lookup"><span data-stu-id="5ae50-109">Create a new buffer to hold the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure with the private data appended, and copy the structure and the data to that buffer.</span></span> <span data-ttu-id="5ae50-110">Наконец, установите для элемента **пбформат** структуры **\_ \_ типа мультимедиа DMO** адрес только что созданного буфера и задайте для элемента **кбформат** общий размер (в байтах) **видеоинфохеадер** и закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="5ae50-110">Finally, set the **pbFormat** member of the **DMO\_MEDIA\_TYPE** structure to the address of the newly created buffer and set the **cbFormat** member to the combined size, in bytes, of the **VIDEOINFOHEADER** and the private data.</span></span>

<span data-ttu-id="5ae50-111">При использовании Медиафаундатион можно создать структуру [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) из интерфейса [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , вызвав [**мфкреатеаммедиатипефроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span><span class="sxs-lookup"><span data-stu-id="5ae50-111">If you are using MediaFoundation you can construct a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure from an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface by calling [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span></span>

<span data-ttu-id="5ae50-112">Необходимо использовать частные данные кодека, полученные после первой установки свойств кодировщика.</span><span class="sxs-lookup"><span data-stu-id="5ae50-112">You must use the codec private data obtained after first setting the properties on the encoder.</span></span> <span data-ttu-id="5ae50-113">При изменении каких бы то ни было свойств необходимо получить новые закрытые данные.</span><span class="sxs-lookup"><span data-stu-id="5ae50-113">If any properties are changed, you must get new private data.</span></span> <span data-ttu-id="5ae50-114">Если не использовать закрытые данные, полученные после установки всех свойств для сеанса кодирования, декодер может не суметь распаковать данные.</span><span class="sxs-lookup"><span data-stu-id="5ae50-114">If you do not use the private data obtained after all the properties are set for the encoding session, the decoder may not be able to decompress the data.</span></span>

<span data-ttu-id="5ae50-115">В следующем примере кода показано, как получить закрытые данные для типа видео:</span><span class="sxs-lookup"><span data-stu-id="5ae50-115">The following code example demonstrates how to obtain the private data for a video type:</span></span>


```
HRESULT GetFinalOutputType(DMO_MEDIA_TYPE* pMedia, IMediaObject* pDMO)
{
    // WARNING //
    // This function does not deallocate the memory pointed to by 
    // pMedia->pbFormat. If the VIDEOINFOHEADER referenced by pbFormat
    // was dynamically allocated, a reference to it must be kept before
    //  calling this function so that it can be freed.

    // Perform simple parameter checks.
    if(pMedia == NULL || pDMO == NULL)
        return E_POINTER;
    if(pMedia->formattype != MEDIATYPE_VideoInfo)
        return E_INVALIDARG;

    HRESULT hr = S_OK;

    IWMCodecPrivateData* pPrivData = NULL;
    BYTE* pbData = NULL;
    DWORD cbData = 0;

    BYTE* pbNewVidInf  = NULL;
    DWORD cbNewVidInf  = 0;
    BYTE* pbNewPriv    = NULL;

    // Get the private data interface.
    hr = pDMO->QueryInterface(IID_IWMCodecPrivateData,
                              (void**)&pPrivData);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the partial media type.
    hr = pPrivData->SetPartialOutputType(pMedia);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the size of the private data.
    hr = pPrivData->GetPrivateData(NULL, &cbData);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the private data.
    pbData = new BYTE[cbData];
    if(pbData == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit:
    }

    // Get the private data.
    hr = pPrivData->GetPrivateData(pbData, &cbData);

    // Allocate memory for the new VIDEOINFOHEADER.
    cbNewVidInf = pMedia->cbFormat + cbData;
    pbNewVidInf = new BYTE[cbNewVidInf];

    // Copy the VIDEOINFOHEADER to the new buffer.
    memcpy((void*)pbNewVidInf, (void*)pMedia->pbFormat, pMedia->cbFormat);

    // Get the address of the first byte following the VIDEOINFOHEADER.
    pbNewPriv = pbNewVidInf + pMedia->cbFormat;

    // Copy the private data to the new buffer.
    memcpy((void*)pbNewPriv, (void*)pbData, cbData);

    // Set the new VIDEOINFOHEADER in the DMO_MEDIA_TYPE.
    pMedia->pbFormat = pbNewVidInf;
    pMedia->cbFormat = cbNewVidInf;

Exit:
    SAFE_RELEASE(pPrivData);
    SAFE_ARRAY_DELETE(pbData);
    pbNewPriv = NULL;
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="5ae50-116">Частные данные кодека, доставляемые кодировщиком видео, не обязательно должны совпадать с частными данными, доставленными другой реализацией одного и того же кодека для той же конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5ae50-116">The codec private data delivered by a video encoder is not guaranteed to be the same as the private data delivered by a different implementation of the same codec for the same configuration.</span></span> <span data-ttu-id="5ae50-117">Это значение необходимо всегда создавать, выполнив действия, описанные в этом разделе. никогда не копируйте закрытые данные из другого файла.</span><span class="sxs-lookup"><span data-stu-id="5ae50-117">You must always generate this value using the steps in this topic; never copy the private data from another file.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5ae50-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5ae50-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae50-119">Настройка кодирования видео</span><span class="sxs-lookup"><span data-stu-id="5ae50-119">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="5ae50-120">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="5ae50-120">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
