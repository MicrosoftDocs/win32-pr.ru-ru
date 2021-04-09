---
description: Запись в несколько файлов
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Запись в несколько файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b40091acff8edffbe84550b03d1ccd4073ddb6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139711"
---
# <a name="capturing-to-multiple-files"></a>Запись в несколько файлов

После записи какого-либо видео в файл можно переключиться на новый файл, заключив граф и указав имя файла в фильтре [записи файлов](file-writer-filter.md) . Вызовите метод [**ифилесинкфилтер:: сетфиленаме**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) для модуля записи файлов. При построении графа можно получить указатель на интерфейс [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) с помощью параметра *псинк* метода сетаутпутфиленаме. В следующем коде показано, как это сделать.


```C++
IBaseFilter *pMux;
IFileSinkFilter *pSink
hr = pBuild->SetOutputFileName(&MEDIASUBTYPE_Avi, L"C:\\YourFileName.avi", 
    &pMux, &pSink);
if (SUCCEEDED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
        pCap, NULL, pMux);

    if (SUCCEEDED(hr))
    {
        pControl->Run();
        /* Wait awhile, then stop the graph. */
        pControl->Stop();
        // Change the file name and run the graph again.
        pSink->SetFileName(L"YourFileName02.avi", 0);
        pControl->Run();
    }
    pMux->Release();
    pSink->Release();
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись видео в файл](capturing-video-to-a-file.md)
</dt> </dl>

 

 



