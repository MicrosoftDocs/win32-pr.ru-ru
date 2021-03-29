---
description: Интерфейсы события (уведомления) позволяют приложению TAPI 3 отвечать на асинхронные события.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Интерфейсы событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7b705c89988ff62d972e594ceb936bb01db78e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541783"
---
# <a name="event-interfaces"></a>Интерфейсы событий

Интерфейсы события (уведомления) позволяют приложению TAPI 3 отвечать на асинхронные события.

Необходимо вызвать метод [**иттапи::p UT \_ EventFilter**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) и задать маску фильтра событий, чтобы включить прием событий запроса. Если не вызвать **иттапи::p UT \_ EventFilter**, приложение не будет принимать никаких событий.

Сведения о том, как приложение обеспечивает получение уведомлений, см. в обзоре [событий](./asynchronous-spontaneous-events.md) . Дополнительные сведения о настройке маски фильтра для отдельных типов событий см. в отдельных интерфейсах, перечисленных в следующей таблице.



| Интерфейс                                                           | Описание                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**итаддрессевент**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Извлекает описание событий адреса.                                                                                                |
| [**итасртерминалевент**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Извлекает описание событий терминала для автоматического распознавания речи.                                                                  |
| [**иткаллхубевент**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Извлекает описание событий Каллхуб.                                                                                                |
| [**иткаллинфочанжеевент**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Извлекает описание событий изменения сведений о вызовах.                                                                                |
| [**иткаллмедиаевент**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Извлекает описание событий мультимедиа вызова.                                                                                             |
| [**иткаллнотификатионевент**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Извлекает описание событий уведомления о вызовах.                                                                                      |
| [**иткаллстативент**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Извлекает описание событий состояния вызова.                                                                                             |
| [**итдигитдетектионевент**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Извлекает сведения о событиях с цифрами DTMF во время вызова.                                                                                |
| [**итдигитженератионевент**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Извлекает сведения о вызовах, требующих создания цифр DTMF.                                                               |
| [**итдигитсгасередевент**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Извлекает данные, связанные с запросом на сбор цифр приложения.                                                                         |
| [**итфилетерминалевент**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Извлекает описание событий файлового терминала.                                                                                          |
| [**итпартиЦипантевент**](./itparticipantevent.md)           | Извлекает описание событий участника конференции.                                                                                 |
| [**итфонивент**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Извлекает описание событий телефона.                                                                                                  |
| [**иткосевент**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Извлекает описание событий качества обслуживания (QOS).                                                                               |
| [**иткуеуивент**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Извлекает описание событий очереди автоматического распределения вызовов (ACD).                                                                |
| [**итрекуестевент**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Получает описание событий запросов [телефонной связи](./assisted-telephony-overview.md) .                                 |
| [**иттапиобжектевент**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Извлекает описание событий объекта TAPI.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Расширяет [**иттапиобжектевент**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); Получает указатель на объект Phone, вызвавший событие объекта TAPI. |
| [**иттонедетектионевент**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Извлекает сведения о событии обнаружения тона.                                                                                         |
| [**иттонетерминалевент**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Извлекает описание событий сигнала терминала.                                                                                          |
| [**итттстерминалевент**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Получает описание событий терминала преобразования текста в речь (TTS).                                                                          |



 



| Интерфейс                                                                                             | Описание                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**итплуггаблетерминалевентсинк**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Уведомляет клиентские приложения об изменениях в подключаемом терминале.                              |
| [**итплуггаблетерминалевентсинкрегистратион**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Регистрирует и отменяет регистрацию клиентского приложения для уведомления о подключаемых событиях терминала. |



 

 

 
