---
title: Вспомогательные функции IP
description: Следующие функции извлекают и изменяют параметры конфигурации для транспорта TCP/IP на локальном компьютере.
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
ms.openlocfilehash: 050db5574a1c10f01dadd1f53bb8e5a5aee2625a922680fe44f50a76e07ada97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389135"
---
# <a name="ip-helper-functions"></a>Вспомогательные функции IP

Следующие функции извлекают и изменяют параметры конфигурации для транспорта TCP/IP на локальном компьютере. Следующий список категорий поможет определить, какая коллекция функций лучше всего подходит для данной задачи.

-   [**жетнетворкконнективитихинт**](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [**жетнетворкконнективитихинтфоринтерфаце**](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [**нотифинетворкконнективитихинтчанже**](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a>Управление адаптерами

-   [**жетадаптериндекс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [**жетадаптерсаддрессес**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [**жетадаптерсинфо**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [**жетперадаптеринфо**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [**жетунидиректионаладаптеринфо**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a>Управление протоколом разрешения адресов (ARP)

-   [**креатеипнетентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [**креатепроксярпентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [**делетеипнетентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [**делетепроксярпентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [**флушипнеттабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [**жетипнеттабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [**сендарп**](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [**сетипнетентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a>Преобразование интерфейса

-   [**конвертинтерфацеалиастолуид**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**конвертинтерфацегуидтолуид**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**конвертинтерфацеиндекстолуид**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**конвертинтерфацелуидтоалиас**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [**конвертинтерфацелуидтогуид**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**конвертинтерфацелуидтоиндекс**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**конвертинтерфацелуидтонамеа**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**конвертинтерфацелуидтонамев**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**конвертинтерфаценаметолуида**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**конвертинтерфаценаметолуидв**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**Если \_ индекстонаме**](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [**Если \_ наметоиндекс**](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a>Управление интерфейсом

-   [**фриинтерфацеднссеттингс**](/windows/win32/api/netioapi/nf-netioapi-freeinterfacednssettings)
-   [**жетфриендлифиндекс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [**жетифентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [**GetIfEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [**GetIfEntry2Ex**](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [**жетифстакктабле**](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [**жетифтабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [**GetIfTable2**](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**жетинтерфацеднссеттингс**](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings)
-   [**жетинтерфацеинфо**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [**жетинвертедифстакктабле**](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**жетипинтерфацеентри**](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**жетипинтерфацетабле**](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**жетнумберофинтерфацес**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [**инитиализеипинтерфацеентри**](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**сетифентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [**сетинтерфацеднссеттингс**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings)
-   [**сетипинтерфацеентри**](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a>Протокол Интернета (IP) и Протокол управляющих сообщений Интернета (ICMP)

-   [**жетикмпстатистикс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [**жетипстатистикс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [**Icmp6CreateFile**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [**Icmp6ParseReplies**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [**Icmp6SendEcho2**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [**икмпклосехандле**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [**икмпкреатефиле**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [**икмппарсереплиес**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [**икмпсендечо**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [**IcmpSendEcho2**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [**IcmpSendEcho2Ex**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [**сетипттл**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a>Управление IP-адресами

-   [**аддипаддресс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [**креатеаникастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**креатеуникастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**делетеипаддресс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [**делетеаникастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**делетеуникастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**жетаникастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**жетаникастипаддресстабле**](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**жетипаддртабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [**жетмултикастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**жетмултикастипаддресстабле**](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**жетуникастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**жетуникастипаддресстабле**](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**инитиализеуникастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**ипрелеасеаддресс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [**ипреневаддресс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [**нотифистаблеуникастипаддресстабле**](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**сетуникастипаддрессентри**](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a>Преобразование строки IP-адреса

-   [**RtlIpv4AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a>Управление адресами соседей IP

-   [**CreateIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**ресолвенеигхбор**](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a>Управление IP-путями

-   [**флушиппастабле**](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [**жетиппасентри**](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [**жетиппастабле**](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a>Управление IP-маршрутами

-   [**креатеипфорвардентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [**CreateIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**делетеипфорвардентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [**DeleteIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**енаблераутер**](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [**жетбестинтерфаце**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [**жетбестинтерфацеекс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [**жетбестрауте**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [**GetBestRoute2**](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**жетипфорвардтабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [**GetIpForwardTable2**](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**жетрттандхопкаунт**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [**инитиализеипфорвардентри**](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**сетипфорвардентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [**SetIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**сетипстатистикс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [**сетипстатистиксекс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [**уненаблераутер**](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a>Управление памятью таблицы IP

-   [**фримибтабле**](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a>Служебная программа IP

-   [**ConvertIpv4MaskToLength**](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**креатесортедаддресспаирс**](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**парсенетворкстринг**](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a>Сетевая конфигурация

-   [**жетнетворкпарамс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a>Уведомление

-   [**CancelMibChangeNotify2**](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**нотифяддрчанже**](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [**нотифипинтерфацечанже**](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**нотифираутечанже**](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [**NotifyRouteChange2**](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**нотифюникастипаддрессчанже**](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="packet-timestamping"></a>Метки времени пакетов

-   [**каптуреинтерфацехардварекросстиместамп**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)
-   [**жетинтерфацеактиветиместампкапабилитиес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities)
-   [**жетинтерфацесуппортедтиместампкапабилитиес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)
-   [**регистеринтерфацетиместампконфигчанже**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
-   [**унрегистеринтерфацетиместампконфигчанже**](/windows/win32/api/iphlpapi/unregisterinterfacetimestampconfigchange)

## <a name="persistent-port-reservation"></a>Постоянное резервирование портов

-   [**креатеперсистентткппортресерватион**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**креатеперсистентудппортресерватион**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**делетеперсистентткппортресерватион**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**делетеперсистентудппортресерватион**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**лукупперсистентткппортресерватион**](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**лукупперсистентудппортресерватион**](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a>Работоспособность системы безопасности

-   [**канцелсекуритихеалсчанженотифи**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**нотифисекуритихеалсчанже**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

эти функции определяются только на Windows Server 2003.

> [!Note]  
> эти функции недоступны в Windows Vista и на Windows Server 2008.

## <a name="teredo-ipv6-client-management"></a>Управление клиентом Teredo IPv6

-   [**жеттередопорт**](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [**нотифитередопортчанже**](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**нотифистаблеуникастипаддресстабле**](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a>Протокол TCP и протокол UDP.

-   [**жетекстендедткптабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [**жетекстендедудптабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**жетовнермодулефромткпентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [**жетовнермодулефромудпентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetPerTcp6ConnectionEStats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**жетперткпконнектионестатс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**жетткпстатистикс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [**жетткпстатистиксекс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [**GetTcpStatisticsEx2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [**GetTcp6Table**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**жетткптабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [**GetTcpTable2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**SetPerTcp6ConnectionEStats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**сетперткпконнектионестатс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [**сетткпентри**](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [**GetUdp6Table**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [**жетудпстатистикс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [**жетудпстатистиксекс**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [**GetUdpStatisticsEx2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [**жетудптабле**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a>Устаревшие интерфейсы API

> [!Note]  
> Эти функции являются устаревшими и не поддерживаются корпорацией Майкрософт.

-   [**аллокатеанджетткпекстаблефромстакк**](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [**аллокатеанджетудпекстаблефромстакк**](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
