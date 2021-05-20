---
description: Представляет атрибуты и поведение сетевого адаптера. Этот класс включает дополнительные свойства и методы, которые поддерживают управление протоколом TCP/IP, который не зависит от сетевого адаптера.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Класс Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153577"
---
# <a name="win32_networkadapterconfiguration-class"></a>\_Класс Win32 NetworkAdapterConfiguration

Класс **WMI \_ NetworkAdapterConfiguration** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет атрибуты и поведение сетевого адаптера. Этот класс включает дополнительные свойства и методы, которые поддерживают управление протоколом TCP/IP, который не зависит от сетевого адаптера.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ NetworkAdapterConfiguration** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ NetworkAdapterConfiguration** содержит следующие методы.



| Метод                                                                                                                       | Описание                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**дисаблеипсек**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Отключает протокол IPsec на этом сетевом адаптере с поддержкой TCP/IP.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Включает протокол DHCP для службы с этим сетевым адаптером.<br/>                                              |
| [**енабледнс**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Включает службу доменных имен (DNS) для службы на этом сетевом адаптере, привязанном к TCP/IP.<br/>                                                     |
| [**енаблеипфилтерсек**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Включает протокол IPsec глобально для всех сетевых адаптеров, привязанных к IP-адресу.<br/>                                                                               |
| [**енаблеипсек**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Включает протокол IPsec для этого конкретного сетевого адаптера с поддержкой TCP/IP.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Включает статическую адресацию TCP/IP для целевого сетевого адаптера.<br/>                                                                           |
| [**Свойство enablewins**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Включение параметров WINS, относящихся к TCP/IP, но независимо от сетевого адаптера.<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Освобождает IP-адрес, привязанный к определенному сетевому адаптеру с поддержкой DHCP.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Освобождает IP-адреса, привязанные ко всем сетевым адаптерам с поддержкой DHCP.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Обновляет IP-адрес на конкретных сетевых адаптерах с поддержкой DHCP.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Обновляет IP-адреса на всех сетевых адаптерах с поддержкой DHCP.<br/>                                                                              |
| [**сетарпалвайссаурцерауте**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Задает передачу запросов ARP по протоколу TCP/IP.<br/>                                                                                        |
| [**сетарпусисерснап**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Позволяет использовать пакеты Ethernet для кодирования привязки 802,3.<br/>                                                                                       |
| [**сетдатабасепас**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Задает путь к стандартным файлам базы данных Интернета (узлы, файлы LMHOSTS, сети и ПРОТОКОЛы).<br/>                                           |
| [**сетдеадгвдетект**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Включает обнаружение неработающих шлюзов.<br/>                                                                                                            |
| [**сетдефаулттос**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Является устаревшей. Этот метод задает значение типа службы (TOS) по умолчанию в заголовке исходящих пакетов IP.<br/>                                   |
| [**сетдефаултттл**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Задает значение срока жизни (TTL) по умолчанию в заголовке исходящих пакетов IP.<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Задает домен DNS.<br/>                                                                                                                       |
| [**сетднссерверсеарчордер**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Задает порядок поиска сервера в виде массива элементов.<br/>                                                                                      |
| [**сетднссуффикссеарчордер**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Задает порядок поиска суффиксов в виде массива элементов.<br/>                                                                                      |
| [**сетдинамикднсрегистратион**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Указывает динамическую регистрацию DNS IP-адресов для этого адаптера, привязанного к IP-адресу.<br/>                                                              |
| [**сетфорвардбуффермемори**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Указывает, сколько IP-адресов памяти выделяется для хранения данных пакетов в очереди пакетов маршрутизатора.<br/>                                                    |
| [**сетгатевайс**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Указывает список шлюзов для пакетов маршрутизации, предназначенных для другой подсети, к которой подключен этот адаптер.<br/>                |
| [**сетигмплевел**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Задает степень, с которой система поддерживает многоадресную рассылку IP-адресов и участвует в протоколе управления группами Интернета.<br/>                   |
| [**сетипконнектионметрик**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Задает метрику маршрутизации, связанную с этим адаптером, привязанным к IP-адресу.<br/>                                                                             |
| [**сетипусезероброадкаст**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Задает использование IP-адресов без широковещательной рассылки.<br/>                                                                                                              |
| [**сетипксфраметипенетворкпаирс**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | Задает пары номеров или кадров сетевого протокола IPX для этого сетевого адаптера.<br/>                                            |
| [**сетипксвиртуалнетворкнумбер**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | Задает номер виртуальной сети сетевого обмена пакетами (IPX) на целевом компьютере.<br/>                                       |
| [**сеткипаливеинтервал**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Задает интервал между повторными передачами проверки активности до получения ответа.<br/>                                                      |
| [**сеткипаливетиме**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Задает частоту, с которой TCP пытается проверить, что неактивное подключение по-прежнему доступно, отправив пакет проверки активности.<br/>                           |
| [**сетмту**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Задает для сетевого интерфейса максимальное значение по умолчанию (MTU).<br/> Этот метод не поддерживается.<br/>                         |
| [**сетнумфорвардпаккетс**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Задает число заголовков IP-пакетов, выделенных для очереди пакетов маршрутизатора.<br/>                                                                |
| [**сетпмтубхдетект**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Включает обнаружение маршрутизаторов-черных дыр.<br/>                                                                                                   |
| [**сетпмтудисковери**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Включает обнаружение максимального блока передачи (MTU).<br/>                                                                                         |
| [**сетткпипнетбиос**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Задает используемую по умолчанию операцию NetBIOS через TCP/IP.<br/>                                                                                         |
| [**сетткпмаксконнектретрансмиссионс**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Задает число попыток, по истечении которых TCP будет повторно передавать запрос на подключение, прежде чем прервать выполнение.<br/>                                                         |
| [**сетткпмаксдатаретрансмиссионс**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Задает число повторных попыток передачи отдельного сегмента данных, передаваемых TCP, перед прерыванием соединения.<br/>                                    |
| [**сетткпнумконнектионс**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Задает максимальное число подключений, которые TCP может открыть одновременно.<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Указывает, использует ли TCP спецификацию RFC 1122 для срочных данных или режим, используемый в производных системах проектирования программного обеспечения (BSD).<br/> |
| [**сетткпвиндовсизе**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Задает максимальный размер окна приема TCP, предлагаемый системой.<br/>                                                                            |
| [**сетвинссервер**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | Задает основной и дополнительный серверы Windows Internet Служба именования (WINS) в этом сетевом адаптере, привязанном к TCP/IP.<br/>                        |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ NetworkAdapterConfiguration** имеет следующие свойства.

<dl> <dt>

**арпалвайссаурцерауте**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| арпалвайссаурцерауте")
</dt> </dl>

Если **значение — true**, протокол TCP/IP передает запросы ARP с включенной маршрутизацией источника в сетях Token Ring. По умолчанию (FALSE), ARP сначала выполняет запросы без исходной маршрутизации, а затем попытается включить исходную маршрутизацию, если ответ не получен. Маршрутизация источников позволяет выполнять маршрутизацию сетевых пакетов между различными типами сетей.

</dd> <dt>

**арпусисерснап**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| арпусисерснап")
</dt> </dl>

Если **true**, пакеты Ethernet следуют кодировке протокола IEEE 802,3 Sub-Network Access (привязать). Установка для этого параметра значения 1 заставляет TCP/IP передавать пакеты Ethernet с помощью кодировки привязки 802,3. По умолчанию (FALSE) стек передает пакеты в формате Ethernet DIX.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Краткое текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DatabasePath")
</dt> </dl>

Допустимый путь к файлам Windows для стандартных файлов базы данных Интернета (узлы, файлы LMHOSTS, сети и ПРОТОКОЛы). Путь к файлу используется интерфейсом сокетов Windows.

</dd> <dt>

**деадгвдетектенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енабледеадгвдетект")
</dt> </dl>

Если **значение равно true**, происходит обнаружение недоставленных шлюзов. Если эта функция включена, протокол TCP запрашивает переключение IP-адреса на резервный шлюз, если он несколько раз пересылает сегмент, не получая ответа.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| DefaultGateway")
</dt> </dl>

Массив IP-адресов шлюзов по умолчанию, которые использует компьютерная система.

Пример: "192.168.12.1 192.168.46.1"

</dd> <dt>

**дефаулттос**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| дефаулттос")
</dt> </dl>

Значение типа службы (TOS) по умолчанию, заданное в заголовке исходящих пакетов IP. Для запроса комментариев (RFC) 791 определяются значения. Значение по умолчанию: 0 (ноль), допустимый диапазон: 0-255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DefaultTTL")
</dt> </dl>

Значение срока жизни (TTL) по умолчанию, заданное в заголовке исходящих пакетов IP. TTL указывает число маршрутизаторов, через которые может пройти IP-пакет, чтобы достичь его назначения, прежде чем будет удалено. Каждый маршрутизатор уменьшается на единицу TTL по мере прохождения пакета и отбрасывает пакеты, если TTL равен 0 (нулю). Значение по умолчанию: 32, допустимый диапазон: 1-255.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")
</dt> </dl>

Если **значение — true**, сервер DHCP автоматически назначает IP-адрес компьютерной системе при установлении сетевого подключения.

</dd> <dt>

**дхкплеасикспирес**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| леасетерминатестиме")
</dt> </dl>

Дата и время истечения срока действия IP-адреса, назначенного компьютеру сервером протокола динамической настройки узлов (DHCP).

Пример: 20521201000230,000000000

</dd> <dt>

**дхкплеасеобтаинед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| леасеобтаинедтиме")
</dt> </dl>

Дата и время получения аренды IP-адреса, назначенного компьютеру сервером DHCP.

Пример: 19521201000230,000000000

</dd> <dt>

**DHCPServer**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")
</dt> </dl>

IP-адрес DHCP-сервера.

Пример: "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| domain")
</dt> </dl>

Название организации, за которой следует точка и расширение, указывающее тип организации, например "microsoft.com". Имя может быть любым сочетанием букв от A до Z, цифрами от 0 до 9 и дефисом (-), а также символа точки (.), используемого в качестве разделителя.

Пример: "microsoft.com"

</dd> <dt>

**днсдомаинсуффикссеарчордер**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| сеарчлист")
</dt> </dl>

Массив DNS-суффиксов доменов, добавляемых к концу имен узлов во время разрешения имен. При попытке разрешить полное доменное имя (FQDN) из имени только для узла система сначала добавит имя локального домена. Если это не удалось, система будет использовать список суффиксов домена для создания дополнительных полных доменных имен в указанном порядке и запроса DNS-серверов для каждого из них.

Пример: "samples.microsoft.com example.microsoft.com"

</dd> <dt>

**днсенабледфорвинсресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енабледнс")
</dt> </dl>

Если **значение — true**, служба доменных имен (DNS) включает разрешение имен по разрешению Windows Internet служба ИМЕНОВАНИЯ (WINS). Если имя не удается разрешить с помощью DNS, запрос имени перенаправляется в WINS для разрешения.

</dd> <dt>

**Атрибуты**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Параметры \| HostName")
</dt> </dl>

Имя узла, используемое для идентификации локального компьютера для проверки подлинности некоторыми служебными программами. Другие служебные программы на основе TCP/IP могут использовать это значение для получения имени локального компьютера. Имена узлов хранятся на DNS-серверах в таблице, которая сопоставляет имена с IP-адресами, используемыми службой DNS. Имя может быть любым сочетанием букв от A до Z, цифрами от 0 до 9 и дефисом (-), а также символа точки (.), используемого в качестве разделителя. По умолчанию это имя компьютера сети Microsoft, но администратор сети может назначить другое имя узла, не влияя на имя компьютера.

Пример: "корпднс"

</dd> <dt>

**днссерверсеарчордер**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| nameserver")
</dt> </dl>

Массив IP-адресов сервера, используемых для запросов DNS-серверов.

</dd> <dt>

**домаинднсрегистратионенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если задано **значение true**, IP-адреса для этого подключения регистрируются в DNS под доменным именем этого подключения, а не регистрируются в полном DNS-имени компьютера. Доменное имя этого соединения задается с помощью метода [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() или назначается DSCP. Зарегистрированное имя — это имя узла компьютера с добавленным доменным именем.

</dd> <dt>

**Параметра**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Память, выделенная протоколом IP для хранения данных пакетов в очереди пакетов маршрутизатора. Когда это пространство буфера заполнено, маршрутизатор начинает удалять пакеты в случайном порядке из очереди. Буферы данных очереди пакетов имеют длину 256 байт, поэтому значение этого параметра должно быть кратно 256. Несколько буферов объединяются в цепочку для больших пакетов. Заголовок IP-адреса для пакета хранится отдельно. Этот параметр игнорируется, и никакие буферы не выделяются, если IP-маршрутизатор не включен. Размер буфера может варьироваться от MTU сети до значения меньше 0xFFFFFFFF. Значение по умолчанию: 74240 (50 1480-байтовых пакетов, округленное до кратного 256).

</dd> <dt>

**фуллднсрегистратионенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если задано **значение true**, IP-адреса для этого подключения регистрируются в DNS под полным DNS-именем компьютера. Полное DNS-имя компьютера отображается на вкладке **Сетевая идентификация** в окне Системное приложение панели управления.

</dd> <dt>

**гатевайкостметрик**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив значений метрик целочисленной стоимости (от 1 до 9999), которые будут использоваться для вычисления самых быстрых, наиболее надежных или наименее ресурсоемких маршрутов. Этот аргумент имеет корреспонденцию "один к одному" со свойством **дефаултипгатевай** .

</dd> <dt>

**игмплевел**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| игмплевел")
</dt> </dl>

Область, в которой система поддерживает многоадресную рассылку IP-адресов и участвует в протоколе IGMP. На уровне 0 (нуль) система не обеспечивает поддержку многоадресной рассылки. На уровне 1 система может только передавать пакеты IP-адресов многоадресной рассылки. На уровне 2 система может отправлять пакеты многоадресной рассылки IP-адресов и полностью участвовать в протоколе IGMP для получения пакетов многоадресной рассылки.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Без многоадресной рассылки** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Многоадресная рассылка IP** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP-& многоадресная рассылка IGMP** (2)


</dt> <dd>

Многоадресная рассылка IP и IGMP (по умолчанию)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| класс Win32Registry системы \\ \\ \\ \\ управления CurrentControlSet \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Номер индекса конфигурации сетевого адаптера Windows. Номер индекса используется, если доступно более одной конфигурации.

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение индекса, уникально идентифицирующего локальный сетевой интерфейс. Значение этого свойства совпадает со значением свойства **InterfaceIndex** в экземпляре [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) , представляющем сетевой интерфейс в таблице маршрутов.

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip \| IPAddress")
</dt> </dl>

Массив всех IP-адресов, связанных с текущим сетевым адаптером. Это свойство может содержать адреса IPv6 или IPv4. Дополнительные сведения см. [в разделе Поддержка IPv6 и IPv4 в WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).

Пример IPv6-адреса: "2010:836B: 4179:: 836B: 4179"

</dd> <dt>

**ипконнектионметрик**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Стоимость использования настроенных маршрутов для адаптера с IP-адресом и является взвешенным значением для этих маршрутов в таблице IP-маршрутизации. При наличии нескольких маршрутов к назначению в таблице IP-маршрутизации используется маршрут с наименьшей метрикой. Значение по умолчанию — 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip")
</dt> </dl>

Если задано **значение true**, TCP/IP привязан и включен на этом сетевом адаптере.

</dd> <dt>

**ипфилтерсекуритенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ипфилтерсекуритенаблед")
</dt> </dl>

При **значении true** безопасность IP-портов включается глобально для всех сетевых адаптеров, привязанных к IP-адресу, и действуют значения безопасности, связанные с отдельными сетевыми адаптерами. Это свойство используется в сочетании с **ипсекпермитткппортс**, **ипсекпермитудппортс** и **ипсекпермитиппротоколс**. Если задано **значение false**, безопасность IP-фильтра отключается для всех сетевых адаптеров и обеспечивает нефильтрованный трафик для трафика всех портов и протоколов.

</dd> <dt>

**иппортсекуритенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| ипфилтерсекуритенаблед")
</dt> </dl>

При **значении true** безопасность IP-портов включается глобально для всех сетевых адаптеров, привязанных к IP-адресу. Это свойство устарело. Вместо этого свойства следует использовать **ипфилтерсекуритенаблед**.

</dd> <dt>

**ипсекпермитиппротоколс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| равипалловедпротоколс")
</dt> </dl>

Массив протоколов, разрешенных для запуска по IP-адресу. Список протоколов определяется с помощью метода [**енаблеипсек**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . Список будет либо пустым, либо содержать числовые значения. Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех протоколов. Пустая строка указывает, что не разрешено выполнять никакие протоколы, если **ипфилтерсекуритенаблед** имеет **значение true**.

</dd> <dt>

**ипсекпермитткппортс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ткпалловедпортс")
</dt> </dl>

Массив портов, которым будет предоставлено разрешение на доступ к TCP. Список протоколов определяется с помощью метода [**енаблеипсек**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . Список будет либо пустым, либо содержать числовые значения. Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех портов. Пустая строка указывает, что нет портов, которым предоставляется разрешение на доступ, если **ипфилтерсекуритенаблед** имеет **значение true**.

</dd> <dt>

**ипсекпермитудппортс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| удпалловедпортс")
</dt> </dl>

Массив портов, которым будет предоставлено разрешение на доступ по протоколу UDP. Список протоколов определяется с помощью метода [**енаблеипсек**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . Список будет либо пустым, либо содержать числовые значения. Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех портов. Пустая строка указывает, что нет портов, которым предоставляется разрешение на доступ, если **ипфилтерсекуритенаблед** имеет **значение true**.

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ службы \| Parameters \| Маска подсети")
</dt> </dl>

Массив всех масок подсети, связанных с текущим сетевым адаптером.

Пример: 255.255.0.0

</dd> <dt>

**ипусезероброадкаст**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| усезероброадкаст")
</dt> </dl>

Если задано **значение true**, IP-нули — широковещательные (0.0.0.0), а в системе используются широковещательные рассылки (255.255.255.255). В компьютерных системах обычно используются такие широковещательные рассылки, но на основе реализаций BSD используются нулевые широковещательные рассылки. Системы, которые не используют те же широковещательные пакеты, не будут взаимодействовать в одной сети. Значение по умолчанию — **false**.

</dd> <dt>

**ипксаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets версии 2 \| [**жетсоккопт**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ Address")
</dt> </dl>

Технология IPX не поддерживается, и это свойство не содержит полезных данных.

</dd> <dt>

**ипксенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Технология IPX не поддерживается, и это свойство не содержит полезных данных.

</dd> <dt>

**ипксфраметипе**
</dt> <dd> <dl> <dt>

Тип данных: массив **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ нвлнкипкс \\ \\ Parameters \| пкттипе")
</dt> </dl>

Технология IPX не поддерживается, и это свойство не содержит полезных данных.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802,2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Оснастка Ethernet** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**Авто** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**ипксмедиатипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ нвлнкипкс \\ \\ Parameters \| mediaType")
</dt> </dl>

Технология IPX не поддерживается, и это свойство не содержит полезных данных.

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token Ring** (2)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (3)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**АркНет** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**ипкснетворкнумбер**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ нвлнкипкс \\ \\ Parameters \| нетворкнумбер")
</dt> </dl>

Технология IPX не поддерживается, и это свойство не содержит полезных данных.

</dd> <dt>

**ипксвиртуалнетнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ нвлнкипкс \\ \\ Parameters \| виртуалнетворкнумбер")
</dt> </dl>

Технология IPX не поддерживается, и это свойство не содержит полезных данных.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| keepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("миллисекунды")
</dt> </dl>

Интервал между повторными передачами проверки активности проверяется до получения ответа. После получения ответа задержка до следующей передачи активности продолжает управляться значением **KeepAliveTime**. Соединение будет прервано после того, как число повторных передач, указанных в **TcpMaxDataRetransmissions** , не ответило. Значение по умолчанию: 1000, допустимый диапазон: 1 – 0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| keepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("миллисекунды")
</dt> </dl>

Свойство **KeepAliveTime** показывает, как часто TCP пытается проверить, что неактивное соединение остается неизменным, отправив пакет проверки активности. Доступная удаленная система будет подтверждать передачу проверки активности. Пакеты проверки активности не отправляются по умолчанию. Эта функция может быть включена в подключении приложения. По умолчанию: 7 200 000 (два часа).

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| входные и выходные функции устройства Win32API \| DeviceIoControl")
</dt> </dl>

MAC-адрес сетевого адаптера. Изготовитель назначает MAC-адрес для уникальной идентификации сетевого адаптера.

Пример: "00:80: C7:8F: 6C: 96"

</dd> <dt>

**Максимальный передаваемый блок данных**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Переопределяет максимальное значение по умолчанию (MTU) для сетевого интерфейса. MTU — это максимальный размер пакета (включая транспортный заголовок), который транспорт будет передавать через базовую сеть. Датаграмма IP может охватывать несколько пакетов. Диапазон этого значения охватывает минимальный размер пакета (68) до MTU, поддерживаемый базовой сетью.

</dd> <dt>

**нумфорвардпаккетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| нумфорвардпаккетс")
</dt> </dl>

Число заголовков IP-пакетов, выделенных для очереди пакетов маршрутизатора. Если все заголовки используются, маршрутизатор начнет отбрасывать пакеты из очереди в случайном порядке. Это значение должно быть не меньше значения параметра **ForwardBufferMemory** , деленного на максимальный размер данных IP-адреса сетей, подключенных к маршрутизатору. Оно должно быть не больше значения параметра **ForwardBufferMemory** , деленного на 256, поскольку для каждого пакета используются по крайней мере 256 байт памяти буфера обмена. Оптимальное число пересылаемых пакетов для заданного значения **ForwardBufferMemory** зависит от типа трафика в сети. Эти два значения будут находиться в другом месте. Если маршрутизатор не включен, этот параметр пропускается и заголовки не выделяются. Значение по умолчанию: 50, допустимый диапазон: 1 — 0xFFFFFFFE.

</dd> <dt>

**пмтубхдетектенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енаблепмтубхдетект")
</dt> </dl>

Если **значение — true**, обнаружение маршрутизаторов-черных дыр происходит, когда TCP обнаруживает путь к максимальной единице передачи. Маршрутизатор с черными отверстиями не возвращает сообщения с недостижимыми адресами ICMP, когда требуется фрагментировать IP-датаграмму с установленным битом «не фрагментировать». Протокол TCP зависит от получения этих сообщений для выполнения обнаружения MTU пути. Если эта функция включена, протокол TCP попытается отправить сегменты без установленного бита дефрагментации, если несколько повторных передач сегмента попадают в неподтвержденные. Если сегмент подтвержден как результат, размер MSS будет уменьшен, а в будущих пакетах соединения будет установлен бит не фрагмента. Включение обнаружения "Черная дыра" увеличивает максимальное число повторных передач, выполненных для данного сегмента. Значение этого свойства по умолчанию равно **false**.

</dd> <dt>

**пмтудисковеренаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енаблепмтудисковери")
</dt> </dl>

Если задано **значение true**, то по пути к удаленному узлу обнаруживается максимальный путь передаваемых данных (MTU). При обнаружении пути MTU и ограничении сегментов TCP этим размером TCP может исключить фрагментацию маршрутизаторов по пути, соединяющего сети с разными MTU. Фрагментация негативно влияет на пропускную способность TCP и перегрузку сети. Если задать для этого параметра **значение false** , то для всех подключений, которые не являются компьютерами в локальной подсети, будет использоваться значение MTU в 576 байт. Значение по умолчанию — **true**.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ нетворккардс \| ServiceName")
</dt> </dl>

Имя службы сетевого адаптера. Обычно это имя короче полного названия продукта.

Пример: "Елнкии"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Идентификатор, по которому известен текущий объект.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**ткпипнетбиосоптионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Битовая карта возможных параметров, связанных с NetBIOS через TCP/IP. Значения определяются в следующем списке.

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**Енабленетбиосвиадхкп** (0)


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**EnableNetbios** (1)


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**Дисабленетбиос** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ткпмаксконнектретрансмиссионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ткпмаксконнектретрансмиссионс")
</dt> </dl>

Число попыток TCP повторно передать запрос на подключение перед завершением соединения. Начальное время ожидания повторной передачи — 3 секунды. Время ожидания повторной передачи удваивается для каждой попытки. Значение по умолчанию: 3, допустимый диапазон: 0 – 0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpMaxDataRetransmissions")
</dt> </dl>

Число раз, когда TCP пересылает отдельный сегмент данных (не сегмент соединения) перед завершением соединения. Время ожидания повторной передачи удваивается при каждой последующей повторной передаче соединения. Значение по умолчанию: 5, допустимый диапазон: 0 – 0xFFFFFFFF.

</dd> <dt>

**ткпнумконнектионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ткпнумконнектионс")
</dt> </dl>

Максимальное число подключений, которые TCP может открыть одновременно. Значение по умолчанию: 0xFFFFFE, допустимый диапазон: 0 — 0xFFFFFE.

</dd> <dt>

**TcpUseRFC1122UrgentPointer**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")
</dt> </dl>

Если **значение — true**, TCP использует спецификацию RFC 1122 для срочных данных. Если **значение равно false** (по умолчанию), TCP использует режим, используемый в производных системах проектирования программного обеспечения (BSD). Два механизма по-разному обрабатывают срочный указатель и не взаимодействуют. Значение по умолчанию — **false**.

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Максимальный размер окна приема TCP, предлагаемый системой. В окне приема указывается число байтов, которое отправитель может передать без получения подтверждения. Как правило, больший объем получаемых окон повысит производительность по сравнению с сетями с высокой задержкой и высокой пропускной способностью. Для повышения эффективности принимающее окно должно быть кратно максимальному размеру сегмента (MSS) TCP. По умолчанию: в четыре раза больше, чем максимальный размер данных TCP, или даже кратный объему данных TCP, округленный до ближайшего числа, кратного 8192. Сети Ethernet по умолчанию имеют значение 8760. Допустимый диапазон: 0-65535.

> [!Note]  
> Windows Vista: это свойство обращается к `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` записи реестра, которая не используется в текущей реализации операционной системы.

 

</dd> <dt>

**винсенаблелмхостслукуп**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енаблелмхостс")
</dt> </dl>

Если **значение — true**, используются локальные файлы поиска. Файлы подстановок будут содержать карту IP-адресов для имен узлов. Если они существуют в локальной системе, они будут находиться в драйверах% SystemRoot% \\ system32 \\ \\ и т. д.

</dd> <dt>

**виншостлукупфиле**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| системные сведения о функциях \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ драйверы \\ \\ и т. д. \\ \\ )
</dt> </dl>

Путь к файлу поиска WINS в локальной системе. Этот файл будет содержать карту IP-адресов для имен узлов. Если файл, указанный в этом свойстве, найден, он будет скопирован в папку% SystemRoot% \\ system32 с \\ драйверами \\ и в локальной системе. Действует, только если свойство **винсенаблелмхостслукуп** имеет **значение true**.

</dd> <dt>

**винспримарисервер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| входные и выходные функции устройства Win32API \| DeviceIoControl")
</dt> </dl>

IP-адрес основного WINS-сервера.

</dd> <dt>

**винсскопеид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Параметры \| ScopeId")
</dt> </dl>

Значение, добавляемое к концу NetBIOS-имени, которое изолирует группу компьютерных систем, взаимодействующих друг с другом. Он используется для всех транзакций NetBIOS через TCP/IP-связь с этой компьютерной системой. Компьютеры, настроенные с идентичными идентификаторами областей, могут взаимодействовать с этим компьютером. Клиенты TCP/IP с разными идентификаторами областей пропускают пакеты с компьютеров с этим идентификатором области. Действует, только если метод [**свойство enablewins**](enablewins-method-in-class-win32-networkadapterconfiguration.md) успешно выполняется.

</dd> <dt>

**винссекондарисервер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| входные и выходные функции устройства Win32API \| DeviceIoControl")
</dt> </dl>

IP-адрес дополнительного WINS-сервера.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ NetworkAdapterConfiguration** является производным от [**\_ параметра CIM**](cim-setting.md).

## <a name="examples"></a>Примеры

Пример кода VBScript для надстройки [инструментария WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) в коллекции TechNet использует класс **Win32 \_ NetworkAdapterConfiguration** для получения сведений о конфигурации сети с нескольких удаленных компьютеров.

Пример " [Get-компутеринфо-запрос компьютера с локального/удаленного компьютера" (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell в коллекции TechNet использует несколько вызовов оборудования и программного обеспечения, включая **Win32 \_ NetworkAdapterConfiguration**, для вывода сведений о локальной или удаленной системе.

Следующий код PowerShell извлекает параметры конфигурации для адаптера Microsoft ИСТАП.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



В следующем \# примере C извлекается описание и номер индекса всех экземпляров конфигурации сетевого адаптера. Обратите внимание, что в этом \# образце C используется пространство имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , которое обычно масштабируется более эффективно, чем классы WMI пространства имен [System. Management](/dotnet/api/system.management) .


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



В следующем \# примере C извлекается описание и номер индекса всех экземпляров конфигурации сетевого адаптера. Обратите внимание, что \# в этом примере на языке C используется исходное пространство имен [System. Management](/dotnet/api/system.management) , которое было заменено [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



В следующем примере извлекаются сведения из класса **Win32 \_ NetworkAdapterConfiguration** .


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Параметр CIM**](cim-setting.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> <dt>

[Задачи WMI: Сетевые подключения](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Задачи WMI: учетные записи и домены](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[Поддержка IPv6 и IPv4 в WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
