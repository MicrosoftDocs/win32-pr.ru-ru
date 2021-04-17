---
description: Образец фильтра захвата — это фильтр преобразования, который можно использовать для извлечения примеров мультимедиа из потока по мере их прохождения через граф фильтра.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Использование образца захвата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673986"
---
# <a name="using-the-sample-grabber"></a>Использование образца захвата

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

[**Образец фильтра захвата**](sample-grabber-filter.md) — это фильтр преобразования, который можно использовать для извлечения примеров мультимедиа из потока по мере их прохождения через граф фильтра.

Если нужно просто извлечь точечный рисунок из видеофайла, проще использовать объект [детектора мультимедиа (медиадет)](media-detector--mediadet.md) . Дополнительные сведения см. в разделе Получение [кадра афиши](grabbing-a-poster-frame.md) . Тем не менее, образец захвата является более гибким, так как он работает практически с любым типом мультимедиа (см. раздел [**исамплеграббер:: сетмедиатипе**](isamplegrabber-setmediatype.md) для некоторых исключений) и обеспечивает больший контроль над приложением.

-   [Создание диспетчера графа фильтров](#create-the-filter-graph-manager)
-   [Добавление образца захвата к графу фильтра](#add-the-sample-grabber-to-the-filter-graph)
-   [Задание типа носителя](#set-the-media-type)
-   [Создание графа фильтра](#build-the-filter-graph)
-   [Запуск графа](#run-the-graph)
-   [Взять пример](#grab-the-sample)
-   [Пример кода](#example-code)
-   [См. также](#related-topics)

## <a name="create-the-filter-graph-manager"></a>Создание диспетчера графа фильтров

Для начала создайте [Диспетчер графа фильтров](filter-graph-manager.md) и запросите интерфейсы [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) .


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Добавление образца захвата к графу фильтра

Создайте экземпляр фильтра захвата образца и аддит на графе фильтра. Запросите образец фильтра захвата для интерфейса [**исамплеграббер**](isamplegrabber.md) .


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a>Задание типа носителя

При первом создании образца захвата не имеет предпочтительного типа носителя. Это означает, что вы можете подключиться почти к любому фильтру в графе, но вы не сможете контролировать тип полученных данных. Перед построением остальной части графа необходимо задать тип мультимедиа для образца захвата, вызвав метод [**исамплеграббер:: сетмедиатипе**](isamplegrabber-setmediatype.md) .

При подключении образца захвата будет сравнивать этот тип носителя с типом мультимедиа, предлагаемым другим фильтром. Единственные поля, которые он проверяет, — основной тип, подтип и тип формата. Для любого из этих значений GUID значения \_ null означает "принимать любое значение". В большинстве случаев потребуется задать основной тип и подтип. Например, в следующем коде указано несжатое 24-разрядное видео RGB:


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a>Создание графа фильтра

Теперь можно построить оставшуюся часть графа фильтра. Так как образец захвата будет подключаться только с помощью указанного типа носителя, это позволяет использовать преимущества [интеллектуальных механизмов соединения](intelligent-connect.md) диспетчера графа фильтров при построении графа.

Например, если указано несжатое видео, можно подключить фильтр источника к образцу области захвата, а диспетчер графа фильтров автоматически добавит средство синтаксического анализа файлов и декодера. В следующем примере используется вспомогательная функция Коннектфилтерс, которая указана в [подсоединении двух фильтров](connect-two-filters.md):


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





Образец захвата представляет собой фильтр преобразования, поэтому выходной ПИН-код должен быть подключен к другому фильтру. Часто вы можете просто отбросить образцы после завершения их выполнения. В этом случае подключите образец захвата к [**фильтру визуализации NULL**](null-renderer-filter.md), который отклоняет полученные данные.

В следующем примере показана связь образца захвата с фильтром визуализации NULL:


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





Имейте в виду, что размещение образца захвата между видеодекодером и модулем визуализации видео может значительно повредить производительность визуализации. Образец захвата — это фильтр переноса на месте, который означает, что выходной буфер совпадает с входным буфером. Для отрисовки видео выходной буфер, скорее всего, находится на графической карте, где операции чтения выполняются намного медленнее, по сравнению с операциями чтения в основной памяти.

## <a name="run-the-graph"></a>Запуск графа

Образец захвата работает в одном из двух режимов:

-   Режим буферизации создает копию каждого примера, прежде чем доставлять пример нисходящий.
-   Режим обратного вызова вызывает определяемую приложением функцию обратного вызова для каждого примера.

В этой статье описывается режим буферизации. (Перед использованием режима обратного вызова имейте в виду, что функция обратного вызова должна быть достаточно ограниченной. В противном случае это может радикально снизить производительность или даже привести к взаимоблокировкам. Дополнительные сведения см. в разделе [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md). Чтобы активировать режим буферизации, вызовите метод [**исамплеграббер:: сетбуфферсамплес**](isamplegrabber-setbuffersamples.md) со значением **true**.

При необходимости вызовите метод [**исамплеграббер:: сетонешот**](isamplegrabber-setoneshot.md) со значением **true**. Это приводит к остановке образца захвата после получения первого примера носителя, что бывает полезно, если требуется взять один кадр из потока. Выполните поиск в нужное время, запустите граф и дождитесь события [**EC \_ Complete**](ec-complete.md) . Обратите внимание, что уровень точности кадров зависит от источника. Например, поиск файла MPEG часто не является точным.

Чтобы максимально ускорить выполнение графа, включите график часов, как описано в разделе [Настройка часов графа](setting-the-graph-clock.md).

В следующем примере включается Однофакторный режим и режим буферизации, запускается граф фильтра и происходит ожидание завершения.


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a>Взять пример

В режиме буферизации образец захвата сохраняет копию каждого образца. Метод [**исамплеграббер:: жеткуррентбуффер**](isamplegrabber-getcurrentbuffer.md) копирует буфер в выделенный вызывающим объектом массив. Чтобы определить необходимый размер массива, сначала вызовите **жеткуррентбуффер** с **пустым** указателем для адреса массива. Затем выделите массив и вызовите метод еще раз, чтобы скопировать буфер. Следующий пример показывает эти шаги.


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



Необходимо знать точный формат данных в буфере. Чтобы получить эти сведения, вызовите метод [**исамплеграббер:: жетконнектедмедиатипе**](isamplegrabber-getconnectedmediatype.md) . Этот метод заполняет структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) форматом.

Для несжатого видеопотока сведения о форматировании содержатся в структуре [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . В следующем примере показано, как получить сведения о форматировании для несжатого видеопотока.


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> Образец захвата не поддерживает [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

 

## <a name="example-code"></a>Пример кода

Ниже приведен полный код для предыдущих примеров.

> [!Note]  
> В этом примере функция [саферелеасе](../medfound/saferelease.md) используется для высвобождения указателей интерфейса.

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование служб редактирования DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
