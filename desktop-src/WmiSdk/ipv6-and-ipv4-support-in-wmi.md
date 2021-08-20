---
description: Поставщик IP-маршрута WMI и классы сетевых классов предоставляют данные для адресов IPv4. начиная с Windows Vista, инструментарий WMI также обеспечивает ограниченную поддержку возможностей сети IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Поддержка IPv6 и IPv4 в WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea400d6c896220dcde5c15d40481444a77ffb309eac8bfdc50cb06ab634c384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819302"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>Поддержка IPv6 и IPv4 в WMI

[Поставщик IP-маршрута](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI и классы сетевых классов предоставляют данные для адресов IPv4. начиная с Windows Vista, инструментарий WMI также обеспечивает ограниченную поддержку возможностей сети IPv6.

## <a name="wmi-ip-data"></a>Данные IP-адреса WMI

Следующие классы предоставляют только данные IPv4:

-   [**\_IP4RouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**\_IP4PersistedRouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**\_IP4RouteTableEvent Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**\_Активерауте Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**\_Сетевого адаптера Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

Следующие классы предоставляют данные для IPv4 и IPv6.

-   [**\_NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    Свойство **ипаддесс** содержит IPv6-адрес компьютера в сети IPv6.

-   [**\_Пингстатус Win32**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ Пингстатус**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) может возвращать данные для адресов IPv4 или IPv6.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>Подключения IPv4 и IPv6 к WMI

При подключении к пространству имен WMI на удаленном компьютере на целевом компьютере должно быть работает то же программное обеспечение, что и для подключающегося компьютера. Например, компьютер с протоколом IPv4 не может подключиться к компьютеру с протоколом IPv6, даже если попытка подключения выполняется с помощью имени компьютера в вызове [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md)или с помощью `winmgmts` подключения моникера. Обратная связь также имеет значение true: компьютер, на котором работает только протокол IPv6, не может подключиться к компьютеру, на котором выполняется только протокол IPv4.

Если конечный компьютер работает как с IPv4, так и с IPv6, то подключение можно выполнить с компьютера, на котором работает программное обеспечение с любым IP-адресом. Имя компьютера или IP-адрес в формате IPv4 или IPv6 можно указать в соединении с пространством имен WMI.

Компьютер, на котором запущены протоколы IPv4 и IPv6 и подключается к целевому компьютеру только по протоколу IPv4 или только к IPv6, должен предоставить IP-адрес в соответствующем формате для IP-адреса целевого компьютера.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об инструментарии WMI](about-wmi.md)
</dt> </dl>

 

 
