---
description: Новые возможности вспомогательного приложения IP
ms.assetid: fa9d72d0-2f9c-433d-b05a-8423664b2e3e
title: Новые возможности вспомогательного приложения IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3141797e96442f34a94c2d2afc37585ce6dbc944e7fb35cf9b4602afa042c95a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897624"
---
# <a name="whats-new-in-ip-helper"></a>Новые возможности вспомогательного приложения IP

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 и Windows Server 2012

следующие функции были добавлены в api-интерфейсы вспомогательного компонента IP на Windows 8 и Windows Server 2012.

Функция, которая получает исторические оценки пропускной способности для сетевого подключения. Дополнительные сведения см. в разделе:

-   [**жетипнетворкконнектионбандвидсестиматес**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

Структура, содержащая сведения о доступных оценках пропускной способности и связанной дисперсии, определяемой стеком TCP/IP. Дополнительные сведения см. в разделе:

-   [**\_сведения о пропускной способности NL \_**](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 и Windows Server 2008 R2

следующие функции добавлены в api модуля поддержки IP-адресов в Windows 7 и Windows Server 2008 R2.

Функции, которые преобразуют адрес Ethernet в двоичном формате и строковом формате для MAC-адреса Ethernet. Дополнительные сведения см. в разделе:

-   [**ртлесернетаддресстостринг**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [**ртлесернетстрингтоаддресс**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows сервер 2008 и Windows Vista SP1

следующие функции добавлены в api модуля поддержки IP-адресов в Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).

Функция, которая работает с IPv4 и протоколом ICMP. Дополнительные сведения см. в разделе:

-   [**IcmpSendEcho2Ex**](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a>Windows Vista

следующие группы функций были добавлены в api модуля поддержки IP-адресов в Windows Vista и более поздних версиях.

Функции, работающие с IPv6 и IPv4 для преобразования интерфейса. Дополнительные сведения см. в разделе:

-   [**конвертинтерфацеалиастолуид**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**конвертинтерфацегуидтолуид**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**конвертинтерфацеиндекстолуид**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**конвертинтерфацелуидтогуид**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**конвертинтерфацелуидтоиндекс**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**конвертинтерфацелуидтонамеа**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**конвертинтерфацелуидтонамев**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**конвертинтерфаценаметолуида**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**конвертинтерфаценаметолуидв**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**Если \_ индекстонаме**](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [**Если \_ наметоиндекс**](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

Функции, работающие с протоколами IPv6 и IPv4 для управления интерфейсом. Дополнительные сведения см. в разделе:

-   [**GetIfEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [**жетифстакктабле**](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [**GetIfTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**жетинвертедифстакктабле**](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**жетипинтерфацеентри**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**жетипинтерфацетабле**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**инитиализеипинтерфацеентри**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**сетипинтерфацеентри**](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

Функции, работающие с протоколами IPv6 и IPv4 для управления IP-адресами. Дополнительные сведения см. в разделе:

-   [**креатеаникастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**креатеуникастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**делетеаникастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**делетеуникастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**жетаникастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**жетаникастипаддресстабле**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**жетмултикастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**жетмултикастипаддресстабле**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**жетуникастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**жетуникастипаддресстабле**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**инитиализеуникастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**нотифистаблеуникастипаддресстабле**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**сетуникастипаддрессентри**](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

Функция, которая работает с IPv6 и IPv4 для управления памятью таблицы IP. Дополнительные сведения см. в разделе:

-   [**фримибтабле**](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

Функции, работающие с IPv6 и IPv4 для управления адресами соседей IP. Дополнительные сведения см. в разделе:

-   [**CreateIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**ресолвенеигхбор**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

Функции, работающие с протоколами IPv6 и IPv4 для управления IP-адресами. Дополнительные сведения см. в разделе:

-   [**флушиппастабле**](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [**жетиппасентри**](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [**жетиппастабле**](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

Функции, работающие с протоколами IPv6 и IPv4 для управления маршрутами IP. Дополнительные сведения см. в разделе:

-   [**CreateIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**DeleteIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**GetBestRoute2**](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**GetIpForwardTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**инитиализеипфорвардентри**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**SetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**сетипстатистиксекс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

Функции, работающие с IPv6 и IPv4 для уведомлений. Дополнительные сведения см. в разделе:

-   [**CancelMibChangeNotify2**](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**нотифипинтерфацечанже**](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**NotifyRouteChange2**](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**нотифюникастипаддрессчанже**](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

Служебные функции, работающие с IP-адресами. Дополнительные сведения см. в разделе:

-   [**ConvertIpv4MaskToLength**](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**креатесортедаддресспаирс**](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**парсенетворкстринг**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

Функции, работающие с протоколом TCP и протоколом UDP для получения таблицы TCP-или IPv4 или таблицы прослушивателя UDP. Дополнительные сведения см. в разделе:

-   [**GetTcp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**GetTcpTable2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**GetUdp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

Функции, работающие с протоколом TCP для получения расширенной статистики TCP по соединению. Дополнительные сведения см. в разделе:

-   [**GetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**жетперткпконнектионестатс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**SetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**сетперткпконнектионестатс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

Новые функции, которые работают для управления клиентом Teredo IPv6. Дополнительные сведения см. в разделе:

-   [**жеттередопорт**](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [**нотифитередопортчанже**](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**нотифистаблеуникастипаддресстабле**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

Служебные функции, которые обеспечивают преобразование между IP-адресами и строковыми представлениями IP-адресов. Дополнительные сведения см. в разделе:

-   [**RtlIpv4AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

Функции, обеспечивающие постоянное резервирование для последовательного блока портов TCP или UDP на локальном компьютере. Дополнительные сведения см. в разделе:

-   [**креатеперсистентткппортресерватион**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**креатеперсистентудппортресерватион**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**делетеперсистентткппортресерватион**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**делетеперсистентудппортресерватион**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**лукупперсистентткппортресерватион**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**лукупперсистентудппортресерватион**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a>Windows Server 2003

в api модуля поддержки IP-адресов для Windows Server 2003 и более поздних версий были добавлены следующие функции:

-   [**канцелсекуритихеалсчанженотифи**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**нотифисекуритихеалсчанже**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

## <a name="windows-xp-sp2"></a>Windows XP с пакетом обновления 2 (SP2)

следующие функции были добавлены в api модуля поддержки IP-адресов в Windows XP с пакетом обновления 2 (sp2) и более поздних версий:

-   [**жетовнермодулефромткпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**жетовнермодулефромудпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
