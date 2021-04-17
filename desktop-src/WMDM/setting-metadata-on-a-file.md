---
title: Задание метаданных для файла
description: Задание метаданных для файла
ms.assetid: 478a5412-e8b4-41c8-802f-9c2748dbaeae
keywords:
- Диспетчер устройств Windows Media, метаданные
- Диспетчер устройств, метаданные
- инструкции по программированию, метаданные
- Классические приложения, метаданные
- Создание приложений диспетчер устройств Windows Media, метаданные
- запись файлов на устройства, метаданные
- метаданные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a6fa7002d4fafffe0793ef91b00dd3f1f0e20c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691234"
---
# <a name="setting-metadata-on-a-file"></a>Задание метаданных для файла

Вы можете задать метаданные для файла перед его записью на устройство (при использовании [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) или в существующем хранилище (путем вызова [**IWMDMStorage3:: сетметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)). Атрибуты можно задавать только в существующем хранилище (путем вызова [**ивмдмстораже:: сетаттрибутес**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) или [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).

Задание метаданных выполняется путем создания и заполнения интерфейса [**ивмдмметадата**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) , который передается в [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3). Однако этот метод может очистить все существующие метаданные в файле, кроме жестко запрограммированных метаданных, хранящихся в самой файловой системе, таких как имя файла или размер. Поэтому необходимо скопировать все существующие метаданные, которые вы хотите сохранить в интерфейсе Ивмдмметадата. Так как Windows Media диспетчер устройств нельзя использовать для получения метаданных из локальных файлов, для получения таких метаданных необходимо использовать пакет SDK для формата Windows Media (или другое средство).

Чтобы использовать пакет SDK для Windows Media Format для получения свойств файла ASF, выполните следующие действия.

1.  Создайте объект редактора метаданных, вызвав **вмкреатидитор** и запрашивая интерфейс **ивмметадатаедитор** .
2.  Откройте файл для чтения метаданных, вызвав **ивмметадатаедитор:: Open**.
3.  Если файл является допустимым ASF-файлом и его можно открыть, запросите редактор для интерфейса **ивмхеадеринфо** .
4.  Получите свойства файла путем вызова **ивмхеадеринфо:: жетаттрибутебинаме**, передав требуемую константу свойства пакета SDK Windows Media Format. Список констант формата пакета SDK с эквивалентными константами пакета SDK для Windows Media диспетчер устройств приведен в следующей таблице.



| Константа пакета SDK для формата Windows Media    | Константа Windows Media диспетчер устройств SDK      |
|--------------------------------------|------------------------------------------------|
| g \_ всзвмтитле                        | g \_ всзвмдмтитле                                |
| g \_ всзвмаусор                       | g \_ всзвмдмаусор                               |
| g \_ всзвмалбумтитле                   | g \_ всзвмдмалбумтитле                           |
| g \_ всзвмженре                        | g \_ всзвмдмженре                                |
| g \_ всзвмеар                         | g \_ всзвмдмеар                                 |
| g \_ всзвмтраккнумбер или g \_ всзвмтракк | g \_ всзвмдмтракк                                |
| g \_ всзвмкомпосер                     | g \_ всзвмдмкомпосер                             |
| g \_ всзвмдуратион                     | g \_ всзвмдмдуратион                             |
| g \_ всзвмкопиригхт                    | g \_ всзвмдмпровидеркопиригхт                    |
| g \_ всзвмдескриптион                  | g \_ всзвмдмдескриптион                          |
| g \_ всзвмбитрате                      | g \_ всзвмдмбитрате                              |
| g \_ всзвмратинг                       | g \_ всзвмдмусерратинг                           |
| g \_ всзвмалбумартист                  | g \_ всзвмдмалбумартист                          |
| g \_ всзвмпаренталратинг               | g \_ всзвмдмпаренталратинг                       |
| g \_ всзвмрадиостатионнаме             | g \_ всзвмдммедиастатионнаме                     |
| g \_ всзвмсубтитле                     | g \_ всзвмдмсубтитле                             |
| g \_ всзвмвидеовидс                   | g \_ всзвмдмвидс                                |
| g \_ всзвмвидеохеигхт                  | g \_ всзвмдмхеигхт                               |
| g \_ всзвммуд                         | g \_ всзвмдмтраккмуд                            |
| g \_ всзвмкодек                        | g \_ всзаудиовавекодек или g \_ всзвидеофауркккодек |



 

В следующем примере кода C++ показано получение ряда свойств метаданных из ASF-файла с помощью пакета SDK формата Windows Media и их преобразование в эквивалентные значения диспетчер устройств Windows Media.


```C++
// Structure and array to hold equivalent Windows Media Format SDK 
// and Windows Media Device Manager SDK metadata property names.
struct EquivalentProperty
{
    LPCWSTR FormatSDKConst;
    LPCWSTR WMDMSDKConst;
};
EquivalentProperty EquivalentProperties []= 
{
    {g_wszWMTitle,        g_wszWMDMTitle},
    {g_wszWMAuthor,      g_wszWMDMAuthor},
    {g_wszWMAlbumTitle,  g_wszWMDMAlbumTitle},
    {g_wszWMGenre,       g_wszWMDMGenre},
    {g_wszWMYear,        g_wszWMDMYear},
    {g_wszWMTrackNumber, g_wszWMDMTrack},
    {g_wszWMTrack,       g_wszWMDMTrack},
    {g_wszWMComposer,    g_wszWMDMComposer},
    {g_wszWMBitrate,     g_wszWMDMBitrate},
    {g_wszWMDuration,    g_wszWMDMDuration},
    {g_wszWMCopyright,   g_wszWMDMProviderCopyright},
    {g_wszWMDescription, g_wszWMDMDescription},
    {g_wszWMRating,      g_wszWMDMUserRating},
    {g_wszWMAlbumArtist, g_wszWMDMAlbumArtist},
    {g_wszWMParentalRating,    g_wszWMDMParentalRating},
    {g_wszWMRadioStationName,  g_wszWMDMMediaStationName},
    {g_wszWMSubTitle,    g_wszWMDMSubTitle},
    {g_wszWMVideoWidth,  g_wszWMDMWidth},
    {g_wszWMVideoHeight, g_wszWMDMHeight},
    {g_wszWMMood,        g_wszWMDMTrackMood},
    {g_wszWMCodec,       g_wszAudioWAVECodec},
    {g_wszWMCodec,       g_wszVideoFourCCCodec}
};
// Function that tries to get metadata by using the Format SDK. 
// If it cannot open the file, it returns E_FAIL.
HRESULT GetFileMetadataFromFormatSDK(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    if ((pMetaData == NULL) || (file == NULL)) return E_INVALIDPARAM;
    HRESULT hr = S_OK;
    CComPtr<IWMMetadataEditor> pEditor;

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do {
        hr = WMCreateEditor(&pEditor);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pEditor->Open(file);
        if (FAILED(hr)) 
            break;

        CComPtr<IWMHeaderInfo>pHeaderInfo;
        hr = pEditor->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHeaderInfo);
        if (FAILED(hr))
            break;

        // Copy values from Format SDK to equivalent WMDM SDK metadata values.

        // Loop through all known values
        WORD stream = 0;
        WMT_ATTR_DATATYPE wmfType;
        WORD len = 0;
        BYTE* value = NULL;
        WMDM_TAG_DATATYPE wmdmType;
        for (int i = 0; i < sizeof(EquivalentProperties) / sizeof(EquivalentProperties[0]); i++)
        {
            // Request each value from our equivalency list by name.
            // The function is called twice: once to get the buffer size,
            // and once to get the value in the allocated buffer.
            if (FAILED(pHeaderInfo->GetAttributeByName(
                &stream, EquivalentProperties[i].FormatSDKConst, &wmfType, NULL, &len)))
            {
                continue;
            }

            value = new BYTE[len];
            if (value == NULL) continue;

            if (FAILED(pHeaderInfo->GetAttributeByName(&stream, EquivalentProperties[i].FormatSDKConst, &wmfType, value, &len)))
            {
                delete[] value;
                continue;
            }

            // Send the data to the equivalent WMDM metadata value.
            // First, find the equivalent WMDM type for the WMF type.
            switch(wmfType)
            {
            case WMT_TYPE_BINARY:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            case WMT_TYPE_DWORD:
                wmdmType = WMDM_TYPE_DWORD;
                break;
            case WMT_TYPE_STRING:
                wmdmType = WMDM_TYPE_STRING;
                break;
            case WMT_TYPE_BOOL:
                wmdmType = WMDM_TYPE_BOOL;
                break;
            case WMT_TYPE_QWORD:
                wmdmType = WMDM_TYPE_QWORD;
                break;
            case WMT_TYPE_WORD:
                wmdmType = WMDM_TYPE_WORD;
                break;
            case WMT_TYPE_GUID:
                wmdmType = WMDM_TYPE_GUID;
                break;
            default:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            }

            // Don't worry about trapping errors, because there's nothing 
            // we can do about it.
            pMetadata->AddItem(wmdmType, 
                EquivalentProperties[i].WMDMSDKConst, value, len);
            delete[] value;
        } // Add next value.
    } while (FALSE); // End Do loop error trap.

    // Close the file opened with IWMMetadataEditor.
    pEditor->Close();
    return hr;
}
```



В следующей функции примера C++ показано, как использовать DirectShow для получения сведений о файле и добавления их в метаданные.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
HRESULT GetFileMetadataFromDShow(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    HRESULT hr = S_OK;

    // Add file metadata properties from DirectShow. 
    // This is good for non-ASF files, or to add any information
    // that the Format SDK didn't get.

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do
    {
        // Create the Media Detector object.
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pIMediaDet->put_Filename(BSTR(file));
        if (FAILED(hr))
            break;

        // Get the media type for the default stream.
        AM_MEDIA_TYPE mediaType;
        hr = pIMediaDet->get_StreamMediaType(&mediaType);
        if (FAILED(hr))
            break;

        // We have the file open, so start requesting information from the 
        // Media Detector and adding it to the metadata. When adding 
        // individual metadata values, ignore the HRESULT, because failure 
        // to add these metadata values is not a breaking issue.

        // Get major and minor types.
        WCHAR strMediaType[64];
        ZeroMemory(strMediaType, 64);

        //Change the major type to a string, then add to IWMDMMetaData.
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.majortype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
             g_wszWMDMediaClassPrimaryID, 
            (BYTE*) strMediaType, 
             sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Clear local string, then retrieve subtype the same way.
        ZeroMemory(strMediaType, 64);
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.subtype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
            g_wszWMDMMediaClassSecondaryID, (BYTE*) strMediaType,
            sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Get the duration. Duration is retrieved in seconds, but set 
        // in 100-nanosecond units.
        double duration = 0;
        hr = pIMediaDet->get_StreamLength(&duration);
        if (duration > 0)
        {
            duration *= 10E7;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMDuration, (BYTE*) &duration, sizeof(duration));
        }

        // Get the frame rate.
        double frameRate = 0;
        hr = pIMediaDet->get_FrameRate(&frameRate);
        if (frameRate > 0)
        {
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMFrameRate, 
                (BYTE*) &frameRate,
                sizeof(frameRate));
        }

        // Get the structure for the default stream's major type and 
        // fill in additional information.

        if (IsEqualGUID(mediaType.formattype, FORMAT_VideoInfo))
        {
            VIDEOINFOHEADER* data = (VIDEOINFOHEADER*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMVideoBitrate, 
               (BYTE*) &data->dwBitRate, sizeof(DWORD));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMHeight, 
               (BYTE*) &data->bmiHeader.biHeight, sizeof(LONG));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMWidth, 
               (BYTE*) &data->bmiHeader.biWidth, sizeof(LONG));
        }

        if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
        {
            WAVEFORMATEX* data = (WAVEFORMATEX*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMBlockAlignment, 
                (BYTE*) &data->nBlockAlign, sizeof(WORD));
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMNumChannels, 
               (BYTE*) &data->nChannels, sizeof(WORD));
        }
    } while (FALSE); // End of error loop.
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Запись файлов на устройство**](writing-files-to-the-device.md)
</dt> </dl>

 

 




