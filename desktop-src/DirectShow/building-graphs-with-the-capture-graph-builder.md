---
description: построение диаграмм с помощью построителя Graph Capture
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: построение диаграмм с помощью построителя Graph Capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3312dfb4ce37c5af981180e669b39f711cdfb5b2b9219f2b2f69f11bd32e7f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119274674"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a>построение диаграмм с помощью построителя Graph Capture

несмотря на свое имя, построитель Graph захвата полезен для создания множества типов графов настраиваемых фильтров, а не только для записи графов. В этой статье содержится краткий обзор использования этого объекта.

построитель Graph для записи предоставляет интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . начните с вызова [**cocreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать построитель Graph для записи и диспетчер Graph фильтра. затем инициализируйте построитель Graph записи, вызывая [**ICaptureGraphBuilder2:: сетфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) с указателем на диспетчер Graph Manager, как показано ниже.


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a>Фильтры подключения

Метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) соединяет два или три фильтра вместе в цепочке. Как правило, метод работает наилучшим образом, если у каждого фильтра есть не более одного входного ПИН-кода или выходного контакта одного типа. Это обсуждение начинается с того, что первые два параметра **RenderStream** и основное внимание уделяется последним трем параметрам. Третий параметр — это указатель [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , который может указывать либо фильтр (как указатель интерфейса [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ), либо выходной ПИН-код (как указатель интерфейса [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ). Четвертый и пятый параметры указывают указатели **ибасефилтер** . Метод **RenderStream** соединяет все три фильтра в цепочке. Например, предположим, что *A*, *B* и *C* являются фильтрами. Предположим, что у каждого фильтра есть только один входной ПИН-код и один выходной ПИН-код. Следующий вызов подключается к B, а затем б к C:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

Все соединения имеют "Интеллектуальные", то есть при необходимости к диаграмме добавляются дополнительные фильтры. дополнительные сведения см. в разделе [интеллектуальные Подключение](intelligent-connect.md). Чтобы подключить только два фильтра, присвойте среднему значению значение **null**. Например, этот вызов подключается к C:

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

Вы можете создать более длинные цепочки, вызвав метод дважды:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

Если последний параметр имеет **значение NULL**, метод автоматически находит модуль визуализации по умолчанию. В нем используется модуль [подготовки видео](video-renderer-filter.md) для видео и модуль [воспроизведения DirectSound](directsound-renderer-filter.md) для аудио. Следовательно

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

эквивалентно

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

где *R* — соответствующий модуль подготовки отчетов. Однако, чтобы подключить фильтр модуля подготовки к просмотру видео вместо модуля подготовки видео, необходимо явно указать его.

Если в третьем параметре указать фильтр, а не ПИН-код, может потребоваться указать, какой из выходных контактов следует использовать для соединения. Это назначение первых двух параметров метода. Первый параметр применяется только к фильтрам записи. Он указывает идентификатор GUID, указывающий категорию ПИН-кода. Полный список категорий см. в разделе [закрепить набор свойств](pin-property-set.md). Две категории допустимы для всех фильтров захвата:

-   **закрепить \_ \_ запись категорий**
-   **\_ \_ Предварительный просмотр категории закрепления**

Если фильтр записи не предоставляет отдельные ПИН-коды для записи и предварительного просмотра, метод [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) вставляет [Интеллектуальный фильтр tee](smart-tee-filter.md) , который разделяет поток на поток записи и предварительный просмотр потока. С точки зрения приложения можно просто обрабатывать все фильтры захвата как имеющие отдельные ПИН-коды и игнорировать базовую топологию графа.

Для записи файла Подключите ПИН-код записи к фильтру мультиплексора. Для интерактивной предварительной версии Подключите предварительный ПИН-код к модулю подготовки отчетов. При переключении двух категорий диаграмма может удалить слишком много кадров во время записи файла; но если граф подключен правильно, он удаляет предварительные кадры по мере необходимости для поддержания пропускной способности потока записи.

В следующем примере показано, как подключить оба потока:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



Некоторые фильтры записи также поддерживают закрытые субтитры, обозначенные **закреплением \_ Category \_ ВБИ**. Чтобы записать скрытые субтитры в файл, выводите эту категорию в фильтр мультиплексора. Чтобы просмотреть скрытые субтитры в окне предварительного просмотра, подключитесь к модулю подготовки отчетов:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



Второй параметр, [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , определяет тип носителя и обычно является одним из следующих:

-   MEDIATYPE \_ Audio
-   \_Видео MEDIATYPE
-   МУЛЬТИМЕДИА с \_ чередованием (DV)

Этот параметр можно использовать каждый раз, когда выходные сигналы фильтра поддерживают перечисление предпочтительных типов мультимедиа. для файловых источников Graph построитель записи автоматически добавляет фильтр синтаксического анализатора при необходимости, а затем запрашивает типы мультимедиа в средстве синтаксического анализа. (Пример см. в разделе о повторном [сжатии AVI-файла](recompressing-an-avi-file.md).) Кроме того, если последний фильтр в цепочке имеет несколько входных ПИН-кодов, метод пытается перечислить типы мультимедиа. Однако не все фильтры поддерживают эту функцию.

## <a name="finding-interfaces-on-filters-and-pins"></a>Поиск интерфейсов в фильтрах и ПИН-кодах

После создания графа, как правило, необходимо разместить различные интерфейсы, предоставляемые фильтрами и ПИН-коды в графе. Например, фильтр захвата может предоставлять интерфейс [**иамдроппедфрамес**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , тогда как в закреплении вывода фильтра может предоставляться интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .

Самый простой способ найти интерфейс — использовать метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) . Этот метод просматривает граф (фильтры и ПИН-коды) до тех пор, пока не найдет нужный интерфейс. Вы можете указать начальную точку для поиска, а также ограничить поиск фильтрами, которые восходящий или нисходящий от начальной точки.

В следующем примере выполняется поиск интерфейса [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) на ПИН-коде предварительной версии видео:


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> В разделе [Поиск интерфейса на фильтре или ПИН-коде](find-an-interface-on-a-filter-or-pin.md) показан альтернативный подход, использующий интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) вместо [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2). Используемый подход зависит от вашего приложения. Если приложение уже использует **ICaptureGraphBuilder2** для построения графа, то [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) является хорошим подходом. В противном случае рассмотрите возможность использования методов **играфбуилдер** .

 

## <a name="finding-pins"></a>Поиск ПИН-кодов

Реже всего может потребоваться указать отдельный ПИН-код для фильтра, хотя в большинстве случаев методы [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) и [**финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) помогут вам устранить неполадки. Если вам нужно найти определенный ПИН-код для фильтра, рекомендуется использовать вспомогательный метод [**ICaptureGraphBuilder2:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) . Укажите категорию, тип мультимедиа (видео или аудио), направление, а также укажите, должен ли ПИН-код быть неподключенным.

Например, следующий код выполняет поиск неподключенного ПИН-кода предварительной версии видео на фильтре записи:


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 
