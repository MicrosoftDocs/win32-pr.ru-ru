---
description: диспетчер Graph фильтра
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: диспетчер Graph фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793a261f0d7bd12058aa0dc22a448f567fea6847dca6062494f0943eee03a9b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756724"
---
# <a name="filter-graph-manager"></a>диспетчер Graph фильтра

фильтр Graph Manager создает и управляет графами фильтра. Этот объект является центральным компонентом в DirectShow. Приложения используют его для создания и управления графами фильтра. фильтр Graph Manager также обрабатывает синхронизацию, уведомление о событии и другие аспекты управления графом фильтра. Создайте этот объект, вызвав **CoCreateInstance**.

### <a name="clsid"></a>CLSID

существует два идентификатора clsid для создания фильтра Graph Manager:



| CLSID                      | Описание                                                 |
|----------------------------|-------------------------------------------------------------|
| \_ФИЛТЕРГРАФ CLSID         | создает фильтр Graph Manager в общем рабочем потоке. |
| \_ФИЛТЕРГРАФНОСРЕАД CLSID | создает фильтр Graph Manager в потоке приложения. |



 

Как правило, приложения должны использовать CLSID \_ филтерграф. Оба идентификатора CLSID создают один и тот же объект, но используют различные модели потоков:

-   CLSID \_ филтерграф создает фильтр Graph Manager в рабочем потоке, который совместно используется всеми \_ экземплярами филтерграф CLSID в рамках одного процесса. Поток отправляет сообщения, отправленные фильтрами, и управляет временем существования всех окон, созданных фильтрами.
-   \_филтерграфносреад CLSID создает фильтр Graph Manager в потоке приложения. При использовании этого идентификатора CLSID поток, вызывающий **CoCreateInstance** , должен иметь цикл обработки сообщений, который отправляет сообщения; в противном случае могут возникнуть взаимоблокировки. кроме того, перед выходом из потока приложения он должен освободить фильтр Graph Manager и все объекты графа (например, фильтры, пин-коды, эталонные часы и т. д.).

### <a name="interfaces"></a>Интерфейсы

фильтр Graph Manager предоставляет следующие интерфейсы:

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Объект](directshow-objects.md)
</dt> </dl>

 

 



