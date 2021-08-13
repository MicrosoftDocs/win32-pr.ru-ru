---
title: Обнаружение формата файла
description: Обнаружение формата файла
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Диспетчер устройств мультимедиа, форматы файлов
- Диспетчер устройств, форматы файлов
- инструкции по программированию, форматы файлов
- Классические приложения, форматы файлов
- создание Windows мультимедиа диспетчер устройств приложений, форматы файлов
- запись файлов на устройства, форматы файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83706a3026968a694d3629551d310db9021b7f8c8118f3d98621751a95af26b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585333"
---
# <a name="discovering-a-files-format"></a>Обнаружение формата файла

Перед отправкой файла на устройство приложение должно определить, поддерживает ли устройство Этот формат файлов.

Обнаружение формата файла может быть сложным. Самый простой способ — создать список расширений файлов, сопоставленных с конкретными \_ значениями ПЕРЕЧИСЛЕНИЯ вмдм форматкоде. Однако в этой системе есть несколько проблем: один формат может иметь несколько расширений (например, .jpg,. jpe и. JPEG для изображений JPEG). Кроме того, одно и то же расширение файла может использоваться различными программами в различных форматах.

Чтобы преодолеть ограничения относительного сопоставления, приложение лучше проверить, соответствует ли формат расширению. пакет SDK для DirectShow предоставляет средства, позволяющие приложению обнаруживать ограниченный набор сведений о большинстве типов файлов мультимедиа. пакет SDK для Windows Media Format предоставляет большое количество сведений, но только файлы ASF. так как для всех типов файлов должен быть проверен код формата, по возможности рекомендуется использовать DirectShow для обнаружения и проверки основного кода формата, а также использовать пакет SDK Windows Media format для поиска дополнительных метаданных, необходимых для файлов ASF. DirectShow также можно использовать для обнаружения базовых метаданных для файлов, отличных от ASF.

Ниже приведен один из способов обнаружения формата файла с помощью сопоставления расширения и DirectShow.

Сначала Сравните расширение имени файла со списком известных расширений. Не забудьте выполнить сравнение без учета регистра. Если расширение не сопоставлено, присвойте формату значение ВМДМ \_ форматкоде \_ undefine.

-   Если код формата не был найден (или вы хотите убедиться, что файл является файлом мультимедиа), можно выполнить следующие действия.
    1.  создание DirectShow объекта детектора мультимедиа с помощью **cocreateinstance**(CLSID \_ медиадет) и получение интерфейса **имедиадет** .
    2.  Откройте файл, вызвав **имедиадет::p UT \_ filename**. Этот вызов завершится ошибкой, если файл защищен.
    3.  Получите тип мультимедиа потока по умолчанию, вызвав метод **имедиадет:: Get \_ стреаммедиатипе**, который возвращает **\_ \_ Тип файла AM**.
    4.  Получите количество потоков, вызвав метод **имедиадет:: Get \_ аутпутстреамс**.
        -   Если имеется только один поток, и он является звуком, то файл имеет тип ВМДМ \_ форматкоде \_ ундефинедаудио
        -   Если имеется только один поток и видео, то файл имеет тип ВМДМ \_ форматкоде \_ ундефинедвидео
        -   Если имеется только один поток, и это видео, а скорость потока равна нулю, то файл имеет тип ВМДМ \_ форматкоде \_ виндовсимажеформат.

Вы также можете попробовать найти соответствующие аудио или видеокодеки из членов **видеоинфохеадер** или **вавеформатекс** , полученных из **Get \_ стреаммедиатипе**.

следующая функция C++ демонстрирует сопоставление расширений файлов и использование DirectShow для анализа неизвестных файлов.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Запись файлов на устройство**](writing-files-to-the-device.md)
</dt> </dl>

 

 




