---
description: Поставщик WDM (WDM) предоставляет доступ к классам, экземплярам, методам и событиям драйверов оборудования, которые соответствуют модели WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Поставщик WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811434"
---
# <a name="wdm-provider"></a>Поставщик WDM

Поставщик WDM (WDM) предоставляет доступ к классам, экземплярам, методам и событиям драйверов оборудования, которые соответствуют модели WDM. Классы для драйверов оборудования находятся в корневом \\ пространстве имен WMI.

Классы WDM определяются преимущественно в WMI. mof.

WDM — это интерфейс операционной системы, с помощью которого аппаратные компоненты предоставляют сведения и уведомления о событиях. Поставщик WDM является классом, экземпляром, событием и поставщиком метода, который позволяет приложениям управления получать доступ к данным и событиям из драйверов устройств с поддержкой интерфейса WMI для WDM. Классы, созданные поставщиком WDM для представления данных драйвера устройства, находятся только в \\ пространстве имен root WMI. Это пространство имен уже должно существовать до того, как поставщик WDM будет обрабатывать установленные драйверы WDM.

Поставщик WDM записывает сведения о операциях WDM в файл Вмипров. log. Дополнительные сведения см. в разделе [файлы журналов WMI](/windows/desktop/WmiSdk/wmi-log-files).

Как класс, экземпляр, метод и поставщик событий, Поставщик WDM реализует стандартный интерфейс [**ивбемпровидеринит**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) , а также следующие методы [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) :

-   [**креатеклассенумасинк**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**креатеинстанцеенумасинк**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**жетобжектасинк**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ексекмесодасинк**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ексеккуерясинк**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**путинстанцеасинк**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

Поставщик WDM поддерживает событие внешних событий [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) , которое УВЕДОМЛЯет Инструментарий WMI о событиях из драйверов на основе WDM. Вы можете зарегистрировать потребителей событий для событий **WMIEvent** , как и любое другое событие. Дополнительные сведения см. [в разделе Получение WMI-события](/windows/desktop/WmiSdk/receiving-a-wmi-event). При запуске драйвера не вызываются события создания класса.

Поставщик WDM поддерживает следующий класс:

-   [**вмибинаримофресаурце**](wmibinarymofresource.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поставщики WMI](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Доступ к данным из драйверов устройств](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
