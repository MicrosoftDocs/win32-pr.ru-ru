---
description: Представляет службу пересылки для сетевого трафика. Служба обрабатывает пакеты, полученные конечными точками протокола, удаляя их или отправляя пакеты другим конечным точкам протокола.
ms.assetid: 366ae2bf-a436-4ad2-b212-39958a7fbc43
title: Класс CIM_ForwardingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardingService
- CIM_ForwardingService.ProtocolType
- CIM_ForwardingService.OtherProtocolType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 63dd03c6e458ee88ef73dea89d006d6d733dd147ed2d4ad7433901c18cbb25d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014662"
---
# <a name="cim_forwardingservice-class"></a>\_Класс CIM форвардингсервице

Представляет службу пересылки для сетевого трафика. Служба обрабатывает пакеты, полученные конечными точками протокола, удаляя их или отправляя пакеты другим конечным точкам протокола.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_ForwardingService : CIM_NetworkService
{
  uint16 ProtocolType;
  string OtherProtocolType;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ форвардингсервице** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ форвардингсервице** имеет следующие свойства.

<dl> <dt>

**осерпротоколтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ форвардингсервице**.**ProtocolType**")
</dt> </dl>

Определяет тип пересылаемого протокола, если значение свойства **ProtocolType** равно 1 (другое).

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ форвардингсервице**.**Осерпротоколтипе**")
</dt> </dl>

Тип протокола для пересылки.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (2)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (3)


</dt> <dd></dd> <dt>

<span id="IPv4_IPv6"></span><span id="ipv4_ipv6"></span><span id="IPV4_IPV6"></span>

**IPv4/IPv6** (4)


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** (5)


</dt> <dd></dd> <dt>

<span id="AppleTalk"></span><span id="appletalk"></span><span id="APPLETALK"></span>

**AppleTalk** (6)


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

Протокол **DECnet** (7)


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** (8)


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

**КОНП** (9)


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

**Клнп** (10)


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

**Vines** (11)


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

**КСНС** (12)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (13)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (14)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (15)


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**Токенринг** (16)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (17)


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**InfiniBand** (18)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

**Fibre Channel** (19)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Сетевая служба CIM**](cim-networkservice.md)
</dt> </dl>

 

