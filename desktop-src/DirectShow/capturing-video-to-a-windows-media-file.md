---
description: Запись видео в файл Windows Media
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Запись видео в файл Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273260"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Запись видео в файл Windows Media

Чтобы записать видео и закодировать его в файл Windows Media Video (WMV), подключите ПИН-код записи к фильтру [модуля записи WM ASF](wm-asf-writer-filter.md) , как показано на следующей схеме.

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



Значение МЕДИАСУБТИПЕ \_ ASF сообщает построителю диаграмм о записи, что в качестве приемника файла используется фильтр модуля записи WM ASF. Построитель диаграмм записи создает фильтр, добавляет его в граф и вызывает метод [**ифилесинкфилтер:: сетфиленаме**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) , чтобы задать имя выходного файла. Он возвращает указатель на фильтр в качестве исходящего параметра (


```
pASFWriter
```



в предыдущем примере).

Чтобы задать профиль Windows Media, используйте интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) в модуле записи WM ASF. Это необходимо сделать перед подключением любых ПИН-кодов в модуле записи WM ASF.


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



Каждый входной ПИН-код в фильтре модуля записи WM ASF соответствует потоку в профиле Windows Media. Необходимо подключить каждый ПИН-код, чтобы содержимое файла совпадало с профилем.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись видео в файл](capturing-video-to-a-file.md)
</dt> </dl>

 

 



