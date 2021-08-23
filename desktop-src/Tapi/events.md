---
description: События являются важной частью обработки вызовов в TAPI 3. Обработка событий включает четыре этапа.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: События (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b2cf181f10373505a0fe50d3c9efa7358b3ccb749acb723d8314dee27ff9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660864"
---
# <a name="events-telephony-api"></a>События (API телефонии)

События являются важной частью обработки вызовов в TAPI 3. Обработка событий включает четыре этапа.

**Регистрация и включение приема событий**

1.  Реализуйте метод [**иттапиевентнотификатион:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) . (TAPI вызывает этот метод при возникновении события.) Как правило, эта реализация не превышает **AddRef** указателя интерфейса **IDispatch** , а затем POST в конвейер сообщений приложения.
2.  Зарегистрируйте исходящий интерфейс [**иттапиевентнотификатион**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) , используя интерфейсы COM Standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) и [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) , и передайте метод [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) в указатель на [**иттапиевентнотификатион:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).
3.  Вызовите метод [**иттапи::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) , чтобы сообщить TAPI о том, какие события будут обработаны приложением. Фильтр событий состоит из элементов **или** ED в перечислении [**\_ событий TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .
    > [!Note]  
    > Необходимо вызвать метод **иттапи::p UT \_ EventFilter** , чтобы задать маску фильтра событий и включить прием событий. Если не вызвать **иттапи::p UT \_ EventFilter**, приложение не будет принимать никаких событий.

     

Также необходимо вызвать метод [**иттапи:: регистеркаллнотификатионс**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) для каждого объекта адреса, для которого приложение будет выполнять вызовы.

Список всех интерфейсов событий см. в разделе [интерфейсы событий](./event-interfaces.md) . В разделе [Регистрация событий](register-events.md) приведены примеры кода, иллюстрирующие процесс регистрации и [получающий вызов](receive-a-call.md) примера кода, в котором показано одно использование событий.

 

 
