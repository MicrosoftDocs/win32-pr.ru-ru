---
description: Предварительный просмотр Project
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Предварительный просмотр Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d17d5fd0c87d98db2dac0a7ace97a72e2107eeb252561bbc535a5bd8b4a56d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748264"
---
# <a name="previewing-the-project"></a>Предварительный просмотр Project

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

для предварительного просмотра проекта необходим компонент, называемый *подсистемой визуализации*, который создает DirectShowный граф фильтра из временной шкалы. Граф фильтра фактически визуализирует проект. Модуль визуализации можно использовать для предварительного просмотра проекта или для записи окончательного выходного файла.

Эта статья не содержит подробностей о подсистеме визуализации. Для предварительного просмотра требуется только несколько вызовов метода. Более подробное обсуждение, в том числе сведения о записи выходных файлов, можно найти в разделе [подготовка Project](rendering-a-project.md). В следующем примере кода показано, как создать диаграмму предварительного просмотра.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Создайте подсистему отрисовки с помощью функции **CoCreateInstance** . Затем вызывайте следующие методы в интерфейсе [**ирендеренгине**](irenderengine.md) механизма визуализации:

-   [**Сеттимелинеобжект**](irenderengine-settimelineobject.md). Указывает используемую временную шкалу.
-   [**Коннектфронтенд**](irenderengine-connectfrontend.md). Создает диаграмму частичного фильтра с одним выходным закреплением для каждой группы на временной шкале.
-   [**Рендераутпутпинс**](irenderengine-renderoutputpins.md). Завершает диаграмму предварительного просмотра, подключив каждый выходный контакт к обработчику видео или аудио.

после построения графа можно выполнить предварительный просмотр проекта, запустив граф, как и любой график фильтра DirectShow. Сначала получите указатель на граф фильтра, вызвав метод [**ирендеренгине:: жетфилтерграф**](irenderengine-getfiltergraph.md) .


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Запросите граф фильтра для интерфейсов [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) . Используйте эти два интерфейса для запуска графа и ожидания завершения воспроизведения. Описание использования этих интерфейсов см. в разделе [Воспроизведение файла](how-to-play-a-file.md) и [реагирование на события](responding-to-events.md). В следующем коде показан один из способов использования этих интерфейсов.


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



Код в этом примере блокирует выполнение программы до завершения воспроизведения из-за бесконечного параметра в вызове метода [**имедиаевент:: ваитфоркомплетион**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) . Однако если во время воспроизведения возникли проблемы, это может привести к тому, что программа перестанет отвечать на запросы. В реальном приложении используйте цикл обработки сообщений для ожидания завершения воспроизведения. Также рекомендуется предоставить пользователю способ прерывания воспроизведения.

По завершении работы с модулем визуализации всегда вызывайте метод [**ирендеренгине:: скрапит**](irenderengine-scrapit.md) . Этот метод удаляет граф фильтра и освобождает все ресурсы, удерживаемые подсистемой визуализации.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Загрузка и предварительный просмотр Project](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



