---
title: Создание подписок на события оборудования
description: На компьютерах с установленным контроллером управления основной платой (BMC) события оборудования вызываются и регистрируются в журнале системных событий (SEL), который представляет собой хранилище событий BMC, которое хранится в энергонезависимой памяти.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ee32d590143ed8a1ffacec6f59ad3b3094c2d2a22d0df66b0cb0d3521f83e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751116"
---
# <a name="creating-hardware-event-subscriptions"></a>Создание подписок на события оборудования

На компьютерах с установленным контроллером управления основной платой (BMC) события оборудования вызываются и регистрируются в журнале системных событий (SEL), который представляет собой хранилище событий BMC, которое хранится в энергонезависимой памяти. для чтения этих событий оборудования на Windows Server 2008 с помощью Просмотр событий необходимо создать подписку на эти события. аппаратные подписки на события будут работать только на Windows Server 2008.

Следующая процедура определяет, как создать подписку на событие SEL для получения событий оборудования:

1.  Сохраните следующий XML-код в файле .xml (в этом примере файл называется Wsmanselrg.xml). Этот XML определяет подписку.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  Создайте подписку на событие, выполнив следующую команду в окне командной строки (Wecutil.exe программа находится в каталоге% SYSTEMROOT% \\ System32):

    **Wecutil CS** *<path> \\wsmanselrg.xml*

3.  Убедитесь, что Подписка активна, выполнив следующую команду в окне командной строки:

    **Wecutil GR** *всманселрг*

Контроллер BMC — это микроконтроллер, подключенный локально к серверу. Контроллеры BMC имеют датчики, отслеживающие физическое состояние сервера и отдельное сетевое подключение, которое может взаимодействовать по сети, даже если сервер находится в автономном режиме. У вас есть доступ к данным BMC через поставщик IPMI WMI. Дополнительные сведения о поставщике IPMI см. в разделе [поставщик IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

Для работы подписки на события на компьютере должен быть установлен контроллер BMC и поставщик IPMI. для компьютеров, работающих на Windows Server 2008, поставщик IPMI устанавливается по умолчанию. Если контроллер BMC недоступен, то драйвер IPMI не может быть установлен, а состояние среды выполнения подписки всегда будет содержать ошибку (0x8004001-WMI, общий сбой).

 

 