---
description: Создание графа фильтра VMR-9
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Создание графа фильтра VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894918"
---
# <a name="building-a-vmr-9-filter-graph"></a>Создание графа фильтра VMR-9

Так как фильтр визуализации 9 для видео микшера (VMR-9) не является модулем подготовки видео по умолчанию, приложение, использующее VMR-9, должно явно добавить его в граф и подключить. В этом разделе представлены два разных подхода к созданию графов фильтров с помощью фильтра VMR-9.

Использование построителя графа записи

Построитель графов записи — это вспомогательный объект для создания графов настраиваемых фильтров. Его можно использовать для создания графов VMR-9 следующим образом:

1.  Создание и инициализация построителя графа записи, как описано в разделе [Построитель диаграмм записи](about-the-capture-graph-builder.md).
2.  Вызовите CoCreateInstance для создания VMR-9:
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  Вызовите [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) в диспетчере графа фильтров, чтобы добавить VMR-9 в граф фильтра:
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Вызовите [**играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) , чтобы добавить фильтр источника для файла видео:
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Вызовите метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , чтобы отобразить видеопоток в VMR:
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  При необходимости снова вызовите RenderStream для отрисовки аудиопотока:
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

Вы можете смешивать несколько потоков видео, вызывая Аддсаурцефилтер и RenderStream для каждого исходного файла.

Использование диспетчера графа фильтров

Если вы предпочитаете не использовать построитель диаграмм записи, можно создать граф VMR-9, просто используя методы в диспетчере графов фильтров, как показано ниже.

1.  Создайте VMR-9 и добавьте его в граф, как показано в предыдущей процедуре.
2.  Используйте Аддсаурцефилтер, чтобы добавить фильтр источника для файла видео, как показано в предыдущей процедуре.
3.  Если вы хотите подготовить звук, создайте экземпляр фильтра модуля [обработки DirectSound](directsound-renderer-filter.md) и добавьте его в граф фильтра.
4.  Используйте метод Ибасефилтер:: Енумпинс, чтобы найти выходной ПИН-код в фильтре источника. Дополнительные сведения см. в разделе [перечисление ПИН](enumerating-pins.md) -кодов.
5.  Запросите диспетчер графов фильтров для интерфейса IFilterGraph2.
6.  Вызовите [**IFilterGraph2:: рендерекс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) с \_ \_ флагом AM рендерекс рендертоексистингрендерерс. Этот вызов визуализирует выходной ПИН-код, используя только фильтры модуля подготовки отчетов, уже имеющиеся в графе — в данном случае — VMR-9 и модуль подготовки DirectSound. Таким образом, логика интеллектуального соединения не добавляет к диаграмме модуль подготовки видео по умолчанию, что приведет к неподключенному объекту VMR-9.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Построение диаграмм с помощью построителя графа записи](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



