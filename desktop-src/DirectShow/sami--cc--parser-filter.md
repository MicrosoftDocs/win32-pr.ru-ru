---
description: Фильтр средства синтаксического анализа SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Фильтр средства синтаксического анализа SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77f0aa2d913b7f0295a078c8174ae483bb1cb62
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909682"
---
# <a name="sami-cc-parser-filter"></a>Фильтр средства синтаксического анализа SAMI (CC)

Анализирует заголовки данных из синхронизированных доступных файлов обмена мультимедиа (SAMI).

Саамский является текстовым форматом, похожим на HTML, и используется для кодирования заголовков на основе времени. Этот фильтр преобразует данные SAMIs в текстовый поток. Каждый пример в потоке содержит одну запись заголовка, а также сведения о форматировании. Метки времени для образцов формируются на основе сведений о времени в файле SAMI.

Этот фильтр предназначен для использования с фильтром модуля [подготовки](internal-script-command-renderer-filter.md) отчетов для внутреннего выполнения. Модуль подготовки отчетов команды внутреннего сценария получает текстовые примеры и отправляет их в приложение в виде уведомлений о событиях. Дополнительные сведения см. в разделе "Замечания".



| Метка | Значение |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Иамстреамселект**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Типы носителей входных закрепления                    | \_Поток MEDIATYPE                                                                                        |
| Интерфейсы входных закрепления                     | [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Типы носителей для выходного ПИН-кода                   | MEDIATYPE \_ Text, медиасубтипе \_ null                                                                      |
| Интерфейсы выходного ПИН-кода                    | [**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Фильтровать CLSID                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                         |
| Исполняемый объект                               | quartz.dll                                                                                               |
| [Заслуживают](merit.md)                       | \_маловероятно                                                                                          |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                            |



 

## <a name="remarks"></a>Комментарии

Ниже приведен простой файл SAMI:


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



Тег **Style** определяет два языковых параметра: Английский (. ЕНКК) и французский (. ФРКК). Он также определяет два стиля: \# обычные и \# гринтекст. Каждый тег **синхронизации** определяет время начала для заголовка в миллисекундах. Теги **P** содержат текст заголовка, а атрибут **Class** задает языковой параметр, к которому применяется заголовок.

Для каждого языка и стиля фильтр создает логический поток. В любое время включается ровно один языковой поток и один поток стилей. Когда фильтр формирует образец, он выбирает заголовок для текущего языка и применяет текущий стиль. По умолчанию первый язык и стиль, объявленный в файле, включены. Приложение может использовать метод [**иамстреамселект:: enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) для включения другого потока.

При использовании параметров по умолчанию первый заголовок в файле Example создает следующие выходные данные:


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Если выходные данные попадают во внутренний модуль подготовки команд сценария, этот фильтр отправляет уведомление о событии [**\_ \_ событий EC OLE**](ec-ole-event.md) . Второй параметр события — это BSTR с текстом заголовка. Приложение может получить событие и отобразить заголовок.

В следующем примере показано, как отобразить файл SAMI, получить сведения о потоке, включить потоки и отобразить текст заголовка. В примере предполагается, что предыдущий файл SAMId сохранен как C: \\ Sami \_ Test \_ File. Sami.

Для краткости в этом примере использовались жестко закодированные индексы потоков при вызове метода **иамстреамселект:: enable** . Он также выполняет минимальную проверку на наличие ошибок.


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



Этот фильтр использует интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) для извлечения образцов из фильтра источника. Поэтому он не поддерживает интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) на входном ПИН-коде.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



