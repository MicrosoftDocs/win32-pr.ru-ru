---
description: Просмотр стандартного телетекста в мире
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Просмотр стандартного телетекста в мире
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2129538d91a7ac48fea26fd5f1987473896760c164fb3e2b1d4a2b1d142a1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078553"
---
# <a name="viewing-world-standard-teletext"></a>Просмотр стандартного телетекста в мире

> [!Note]  
> эта функция была удалена из Windows Vista и более поздних операционных систем. он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.

 

Международный стандарт телетекста (WST) кодируется в вертикальном интервале (ВБИ) аналогового телевизионного сигнала. Граф фильтра для предварительного просмотра телетекста аналогичен графу, используемому для просмотра скрытых субтитров. Эта диаграмма показана на следующей схеме.

![Диаграмма WST Preview](images/vidcap10.png)

Эта диаграмма использует следующие фильтры для отображения WST:

-   [Преобразователь tee/Sink-to-Sink](tee-sink-to-sink-converter.md). Принимает сведения ВБИ из фильтра записи и разделяет их на отдельные потоки для каждой из служб данных, имеющихся в сигнале.
-   [WST кодек](wst-codec-filter.md). Декодирует данные телетекста из примеров ВБИ.
-   [WST декодер](wst-decoder-filter.md). Преобразует данные телетекста и рисует текст на точечные рисунки. нисходящий фильтр (в данном случае наложение Mixer) накладывает на видео растровые изображения.

метод **RenderStream** в построителе Capture Graph не поддерживает фильтры WST напрямую, поэтому приложение должно выполнить некоторую дополнительную работу.

1.  добавьте наложение Mixer фильтр к графу фильтра. В следующем коде используется функция Аддфилтербиклсид, описанная в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md). (аддфилтербиклсид не является DirectShow API.)
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Подключение контрольный пин-код для фильтра модуля подготовки видео через Mixer наложения. Метод **RenderStream** можно использовать следующим образом:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Добавьте фильтр преобразователя tee/Sink-to-Sink в граф фильтра. В следующем коде используется функция Креатекернелфилтер, описанная в разделе [Создание фильтров Kernel-Mode](creating-kernel-mode-filters.md). (креатекернелфилтер не является DirectShow API.)
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Добавьте фильтр кодека WST в граф фильтра:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Вызовите **RenderStream** , чтобы подключить ПИН-код ВБИ фильтра захвата к преобразовательу tee/Sink-Sink, а также к преобразователю tee/Sink-Sink в фильтре кодека WST:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Вызовите **RenderStream** еще раз, чтобы соединить фильтр кодека WST с наложением Mixer. Фильтр декодера WST автоматически помещается в граф.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  Не забудьте освободить все интерфейсы фильтров.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> В настоящее время фильтр WST декодера не поддерживает подключения к фильтру модуля подготовки видео (VMR). Поэтому для просмотра телетекста необходимо использовать фильтр модуля подготовки видео прежних версий.

 

Если фильтр записи имеет ПИН-код ВБИ (ПИН-код \_ категпори \_ видеопорт \_ ВБИ), подключите его к фильтру [распределителя (ВБИ Surface](vbi-surface-allocator.md) ). В противном случае граф будет работать неправильно. В следующем примере кода используется функция Аддфилтербиклсид, описанная в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md), и функция финдпинбикатегори, описанная в разделе [Работа с категориями ПИН-кода](working-with-pin-categories.md). (ни одна из функций не является DirectShow API.)


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Субтитры и телетекст](closed-captions-and-teletext.md)
</dt> </dl>

 

 



