---
description: Предварительный просмотр проекта
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Предварительный просмотр проекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990206"
---
# <a name="previewing-the-project"></a>Предварительный просмотр проекта

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

Для предварительного просмотра проекта необходим компонент, называемый *модулем подготовки* отчетов, который создает граф фильтра DirectShow из временной шкалы. Граф фильтра фактически визуализирует проект. Модуль визуализации можно использовать для предварительного просмотра проекта или для записи окончательного выходного файла.

Эта статья не содержит подробностей о подсистеме визуализации. Для предварительного просмотра требуется только несколько вызовов метода. Более подробное обсуждение, в том числе запись выходных файлов, можно найти в разделе [Подготовка проекта](rendering-a-project.md). В следующем примере кода показано, как создать диаграмму предварительного просмотра.


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

После построения графика можно просмотреть проект, запустив граф, как и любой граф фильтра DirectShow. Сначала получите указатель на граф фильтра, вызвав метод [**ирендеренгине:: жетфилтерграф**](irenderengine-getfiltergraph.md) .


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Загрузка и предварительный просмотр проекта](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



