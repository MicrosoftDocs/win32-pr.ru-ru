---
description: Использование личных данных видеокодека
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Использование личных данных видеокодека (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e417d4d83cc3ae3174e1bbf3310a6abb2900e2c5f3323192a8d17643e4066f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887094"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a>Использование личных данных видеокодека (Microsoft Media Foundation)

сжатые выходные данные, создаваемые кодеками Windows Media Video 9, не могут быть правильно распакованы без каких бы то ни было данных, предоставленных кодировщиком. Эти данные, называемые частными данными кодека, должны быть добавлены к выходному типу носителя. Можно получить частные данные кодека, вызвав методы интерфейса [ивмкодекприватедата](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) . передайте DMO структуру [**\_ \_ типа носителя**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) в [ивмкодекприватедата:: сетпартиалаутпуттипе](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype). Затем вызовите метод [ивмкодекприватедата:: жетприватедата](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) дважды, один раз, чтобы получить размер данных, а затем скопируйте данные в буфер такого размера. Создайте новый буфер для хранения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) с добавленными закрытыми данными и скопируйте структуру и данные в этот буфер. наконец, задайте для DMO элемента **пбформат** структуры **\_ \_ типа мультимедиа** адрес только что созданного буфера и задайте для элемента **кбформат** общий размер (в байтах) **видеоинфохеадер** и закрытых данных.

при использовании медиафаундатион можно создать [**DMO структуру \_ \_ типа мультимедиа**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) из интерфейса [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , вызвав [**мфкреатеаммедиатипефроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).

Необходимо использовать частные данные кодека, полученные после первой установки свойств кодировщика. При изменении каких бы то ни было свойств необходимо получить новые закрытые данные. Если не использовать закрытые данные, полученные после установки всех свойств для сеанса кодирования, декодер может не суметь распаковать данные.

В следующем примере кода показано, как получить закрытые данные для типа видео:


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
> Частные данные кодека, доставляемые кодировщиком видео, не обязательно должны совпадать с частными данными, доставленными другой реализацией одного и того же кодека для той же конфигурации. Это значение необходимо всегда создавать, выполнив действия, описанные в этом разделе. никогда не копируйте закрытые данные из другого файла.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка кодирования видео](configuringvideoencoding.md)
</dt> <dt>

[Работа с видео](workingwithvideo.md)
</dt> </dl>

 

 
