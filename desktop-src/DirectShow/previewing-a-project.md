---
description: Предварительный просмотр Project
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Предварительный просмотр Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159303c175c459b4d5d93ba4c7b4b2622caddac2a35d3474a3059ac703d62645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583563"
---
# <a name="previewing-a-project"></a>Предварительный просмотр Project

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

Для предварительного просмотра проекта сначала вызовите метод **CoCreateInstance** , чтобы создать экземпляр базового механизма визуализации. Идентификатор класса — CLSID \_ рендеренгине. Затем вызовите метод [**ирендеренгине:: сеттимелинеобжект**](irenderengine-settimelineobject.md) , чтобы указать шкалу времени, которую вы готовите к просмотру.

При первом предварительном просмотре временной шкалы выполните следующие вызовы в указанном порядке:

1.  Вызовите [**ирендеренгине:: сетрендерранже**](irenderengine-setrenderrange.md) , чтобы указать, какую часть временной шкалы следует просмотреть. (необязательно)
2.  Вызовите [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) , чтобы создать внешний интерфейс графа.
3.  Вызовите [**ирендеренгине:: рендераутпутпинс**](irenderengine-renderoutputpins.md). Этот метод соединяет каждый выходной закрепление с модулем подготовки видео или модулем подготовки звука, выполняя граф.

В следующем примере кода показаны следующие действия.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



Теперь запустите граф фильтра. во-первых, вызовите метод [**ирендеренгине:: жетфилтерграф**](irenderengine-getfiltergraph.md) , чтобы получить указатель на интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) диспетчера Graph Manager. затем выполните запрос фильтра Graph Manager для интерфейса [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и вызовите [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), как показано в следующем коде:


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



используйте интерфейс [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) диспетчера фильтров Graph, чтобы дождаться завершения предварительной версии. можно также выполнить поиск в графе с помощью интерфейса [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) диспетчера Graph Manager так же, как и графа воспроизведения файлов.

Чтобы снова выполнить предварительный просмотр проекта, вернитесь на граф к нулевому времени и снова вызовите **команду Run** . При изменении содержимого временной шкалы выполните следующие действия.

1.  Вызовите **сетрендерранже**. (необязательно)
2.  Вызовите **коннектфронтенд**.
3.  Если метод **коннектфронтенд** возвращает S \_ warn \_ Аутпутресет, вызовите **рендераутпутпинс**. (Если **коннектфронтенд** возвращает S \_ ОК, этот шаг можно пропустить.)
4.  Поиск графа обратно в нулевое значение времени.
5.  Запустите граф.

В следующем примере показаны следующие действия.


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



Полный пример загрузки и предварительного просмотра файла проекта см. в разделе [Загрузка и предварительный просмотр Project](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление проектами редактирования видео](managing-video-editing-projects.md)
</dt> <dt>

[Подготовка Project](rendering-a-project.md)
</dt> </dl>

 

 



