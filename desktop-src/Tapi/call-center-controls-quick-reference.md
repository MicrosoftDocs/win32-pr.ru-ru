---
description: Интерфейсы центра обработки вызовов предоставляют методы, которые ставят и распространяют вызовы в центре обработки вызовов.
ms.assetid: 0b9a455d-a614-4698-90ab-e81f020fad3e
title: Краткий справочник по элементам управления центра обработки вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8aa058d08edee533da950a1ca02a46c2867fd315ad22dff2aa7ba4cd72e1e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948236"
---
# <a name="call-center-controls-quick-reference"></a>Краткий справочник по элементам управления центра обработки вызовов

Интерфейсы центра обработки вызовов предоставляют методы, которые ставят и распространяют вызовы в центре обработки вызовов. Интерфейс TAPI 3. x определяет пять основных объектов центра обработки звонков: Акдграуп, Agent, Аженсандлер, Ажентсессион и Queue. Все эти объекты могут быть расширены для предоставления методов, зависящих от реализации. Кроме того, интерфейс [**иттапикаллцентер**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter) объекта TAPI предоставляет методы для перечисления объектов аженсандлер.



| Интерфейс центра обработки вызовов                              | Описание:                                                              |
|----------------------------------------------------|--------------------------------------------------------------------------|
| [**итакдграуп**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)                   | Получает сведения о имени и очереди для ACD.                        |
| [**итакдграупевент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Возвращает описание событий ACD Group.                                    |
| [**итажент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)                         | Предоставляет методы для задания и получения сведений об агенте.         |
| [**итажентевент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Интерфейс уведомления для [**итажент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                   |
| [**итаженсандлер**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)           | Предоставляет методы для создания объектов агентов и перечисления ACD.       |
| [**итаженсандлеревент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Возвращает описание событий Аженсандлер.                                 |
| [**итажентсессион**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)           | Предоставляет методы для задания и получения сведений, касающихся сеанса агента. |
| [**итажентсессионевент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Интерфейс уведомления для [**итажентсессион**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession).     |
| [**иткуеуе**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)                         | Возвращает и задает сведения об очереди.                            |
| [**иткуеуивент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)               | Возвращает сведения о событии очереди.                               |
| [**иенумакдграуп**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)             | Перечисляет [**итакдграуп**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup).                             |
| [**иенумажент**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)                   | Перечисляет [**итажент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                                   |
| [**иенумаженсандлер**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler)     | Перечисляет [**итаженсандлер**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler).                     |
| [**иенумажентсессион**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession)     | Перечисляет [**итажентсессион**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession).                     |
| [**иенумкуеуе**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)                   | Перечисляет [**иткуеуе**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue).                                   |



 

Следующие интерфейсы перечисляют элементы TAPI 3. x в соответствии со стандартами COM. Эти интерфейсы представляют собой изолированные объекты, которые также обобщены с помощью связанных с ними объектов.



| Интерфейс перечислителя                           | Описание:                                          |
|------------------------------------------------|------------------------------------------------------|
| [**иенумакдграуп**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)         | Перечисляет [**итакдграуп**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup).         |
| [**иенумажент**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)               | Перечисляет [**итажент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).               |
| [**иенумаженсандлер**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler) | Перечисляет [**итаженсандлер**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler). |
| [**иенумажентсессион**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession) | Перечисляет [**итажентсессион**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession). |
| [**иенумкуеуе**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)               | Перечисляет [**иткуеуе**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue).               |



 

Интерфейсы события (уведомления) позволяют приложению TAPI 3. x реагировать на асинхронные события. Необходимо вызвать метод [**иттапи::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) и задать маску фильтра событий, чтобы включить прием событий запроса. Если не вызвать **иттапи::p UT \_ EventFilter**, приложение не будет принимать никаких событий.



| Интерфейс событий                                    | Описание:                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------|
| [**итакдграупевент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Извлекает описание событий группы автоматического распределения вызовов (ACD). |
| [**итажентевент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Извлекает описание событий агента.                                   |
| [**итаженсандлеревент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Извлекает описание событий обработчика агента.                           |
| [**итажентсессионевент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Извлекает описание событий сеанса агента.                           |



 

 

 
