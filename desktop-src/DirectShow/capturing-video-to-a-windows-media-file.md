---
description: запись видео в Windowsный файл мультимедиа
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: запись видео в Windowsный файл мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3268d3a3df4a24c5836dba81f7ef4cf0b872907f09367d3212d27c38c0dd4414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158712"
---
# <a name="capturing-video-to-a-windows-media-file"></a>запись видео в Windowsный файл мультимедиа

чтобы записать видео и закодировать его в файл Windows Media video (WMV), подключите пин-код записи к фильтру [модуля записи WM ASF](wm-asf-writer-filter.md) , как показано на следующей схеме.

![Диаграмма записи мультимедиа Windows](images/vidcap03.png)

Самый простой способ создать этот граф — задающего МЕДИАСУБТИПЕ \_ ASF в методе [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



значение медиасубтипе \_ Asf сообщает построителю Graph для записи, что в качестве приемника файла используется фильтр модуля записи WM Asf. построитель Graph записи создает фильтр, добавляет его в граф и вызывает метод [**ифилесинкфилтер:: сетфиленаме**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) , чтобы задать имя выходного файла. Он возвращает указатель на фильтр в качестве исходящего параметра (


```
pASFWriter
```



в предыдущем примере).

используйте интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) в модуле записи WM ASF, чтобы задать профиль носителя Windows. Это необходимо сделать перед подключением любых ПИН-кодов в модуле записи WM ASF.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Дополнительные сведения о настройке профиля см. в разделе [Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md).

Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , чтобы подключить фильтр записи к модулю записи ASF:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



каждый входной пин-код в фильтре модуля записи WM ASF соответствует потоку в профиле носителя Windows. Необходимо подключить каждый ПИН-код, чтобы содержимое файла совпадало с профилем.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запись видео в файл](capturing-video-to-a-file.md)
</dt> </dl>

 

 



