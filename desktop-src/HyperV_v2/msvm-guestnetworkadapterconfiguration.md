---
description: Представляет конфигурацию сетевого адаптера в гостевой операционной системе.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Класс Msvm_GuestNetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154595"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a>\_Класс мсвм гуестнетворкадаптерконфигуратион

Представляет конфигурацию сетевого адаптера в гостевой операционной системе.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ гуестнетворкадаптерконфигуратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ гуестнетворкадаптерконфигуратион** имеет следующие свойства.

<dl> <dt>

**дефаултгатевайс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив строк, содержащий IP-шлюзы по умолчанию, настроенные на сетевом адаптере в гостевой операционной системе. Максимальное число IP-шлюзов по умолчанию, которые могут быть настроены на одном сетевом адаптере, составляет пять.

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включена ли DHCP на сетевом адаптере в гостевой операционной системе.

</dd> <dt>

**DNSServers**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив строк, содержащий DNS-серверы, настроенные на сетевом адаптере в гостевой операционной системе.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Уникальный идентификатор для этого объекта.

</dd> <dt>

**IPAddresses**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив строк, содержащий IP-адреса, настроенные на сетевом адаптере в гостевой операционной системе.

</dd> <dt>

**ипаддрессоригинс**
</dt> <dd> <dl> <dt>

Тип данных: **UINT16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Источник IP-адресов, настроенных на сетевом адаптере в гостевой операционной системе.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

**Статический** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**протоколифтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет IP-протоколы, к которым применяются параметры, заданные этим экземпляром.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

**IPv4/V6** (4098)


</dt> <dd></dd> </dl>

</dd> <dt>

**Подсети**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив строк, содержащий подсети, настроенные на сетевом адаптере в гостевой операционной системе. Каждый элемент в этом массиве применяется к соответствующему элементу в массиве **ipaddresses** .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

