---
description: Диспетчер графа фильтров
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Диспетчер графа фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894142"
---
# <a name="filter-graph-manager"></a>Диспетчер графа фильтров

Диспетчер графов фильтров создает и управляет графами фильтра. Этот объект является центральным компонентом DirectShow. Приложения используют его для создания и управления графами фильтра. Диспетчер графов фильтров также обрабатывает синхронизацию, уведомление о событиях и другие аспекты управления графом фильтра. Создайте этот объект, вызвав **CoCreateInstance**.

### <a name="clsid"></a>CLSID

Существует два идентификатора CLSID для создания диспетчера графа фильтров:



| CLSID                      | Описание                                                 |
|----------------------------|-------------------------------------------------------------|
| \_ФИЛТЕРГРАФ CLSID         | Создает диспетчер графа фильтров в общем рабочем потоке. |
| \_ФИЛТЕРГРАФНОСРЕАД CLSID | Создает диспетчер графа фильтров в потоке приложения. |



 

Как правило, приложения должны использовать CLSID \_ филтерграф. Оба идентификатора CLSID создают один и тот же объект, но используют различные модели потоков:

-   CLSID \_ филтерграф создает диспетчер графа фильтров в рабочем потоке, который совместно используется всеми \_ экземплярами филтерграф CLSID в рамках одного процесса. Поток отправляет сообщения, отправленные фильтрами, и управляет временем существования всех окон, созданных фильтрами.
-   \_ФИЛТЕРГРАФНОСРЕАД CLSID создает диспетчер графа фильтров в потоке приложения. При использовании этого идентификатора CLSID поток, вызывающий **CoCreateInstance** , должен иметь цикл обработки сообщений, который отправляет сообщения; в противном случае могут возникнуть взаимоблокировки. Кроме того, перед выходом из потока приложения он должен освободить диспетчер графов фильтров и все объекты графа (например, фильтры, ПИН-коды, эталонные часы и т. д.).

### <a name="interfaces"></a>Интерфейсы

Диспетчер графов фильтров предоставляет следующие интерфейсы:

-   [**иамграфстреамс**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [**иамстатс**](/windows/desktop/api/Control/nn-control-iamstats)
-   [**ибасикаудио**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [**ифилтерчаин**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [**ифилтерграф**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [**IFilterGraph3**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [**играфконфиг**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [**играфверсион**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent)
-   [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [**имедиафилтер**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition)
-   [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [**икуеуекомманд**](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [**ирегистерсервицепровидер**](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [**Метод IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   **IServiceProvider**
-   [**ивидеофраместеп**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Объекты DirectShow](directshow-objects.md)
</dt> </dl>

 

 



