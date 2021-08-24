---
description: Логическое представление сетевого порта на сетевом устройстве.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: Класс CIM_NetworkPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aa69b2728f3d0cdb97bcc972ef6b72ab5bd0df3202df60e92f87e161ea9a1702
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694714"
---
# <a name="cim_networkport-class"></a>\_Класс CIM нетворкпорт

Логическое представление сетевого порта на сетевом устройстве.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ нетворкпорт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ нетворкпорт** имеет следующие свойства.

<dl> <dt>

**активемаксимумтрансмиссионунит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")
</dt> </dl>

Активный или согласованный максимальный блок передачи (MTU), поддерживаемый портом.

</dd> <dt>

**Авточувствительность**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**значение true** , если порт может автоматически определять скорость или другие характеристики связи подключенного сетевого носителя; в противном случае — **значение false**.

</dd> <dt>

**фуллдуплекс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**значение true** , если порт работает в режиме полного дуплекса; в противном случае — **значение false**.

</dd> <dt>

**линктечнологи**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ нетворкпорт**.**Осерлинктечнологи**")
</dt> </dl>

Технология компоновки, используемая портом. Если задано значение "1" (другое), свойство **осерлинктечнологи** содержит описание типа ссылки.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (2)


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

**ГЕО(3** )


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

**FC** (4)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (5)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (6)


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token Ring** (7)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (8)


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**Инфракрасная связь** (9)


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

**Bluetooth** (10)


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

**Беспроводная локальная сеть** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -сетевой адаптер 802, порт \| 001,3 ")
</dt> </dl>

Массив, содержащий сетевые адреса порта.

</dd> <dt>

**осерлинктечнологи**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ нетворкпорт**.**Линктечнологи**")
</dt> </dl>

Технология Link, если для **линктечнологи** задано значение "1" (другое).

</dd> <dt>

**осернетворкпорттипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ нетворкпорт**.**Осерпорттипе**"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ логикалпорт**](cim-logicalport.md).**PortType**")
</dt> </dl>

> [!Note]  
> Нерекомендуемое описание: тип модуля для порта, если свойство **portType** содержит значение 1 (другое).

 

Это свойство использовать не рекомендуется. Вместо этого мы советуем использовать свойство **portType** в классе [**CIM \_ логикалпорт**](cim-logicalport.md) .

</dd> <dt>

**перманентаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -сетевой адаптер 802, порт \| 001,2 ")
</dt> </dl>

Сетевой адрес, жестко закодированный в порт. Жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения. При внесении этого изменения это свойство следует обновлять одновременно. Если адрес не существует, **перманентаддресс** должен оставаться пустым.

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Номер порта сетевого порта. Сетевые порты часто нумеруются относительно логического модуля или сетевого элемента.

</dd> <dt>

**Скорость**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("скорость"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. ифспид "," MIF. DMTF \| Network Adapter 802 \| , порт 001,5 "), **Пунит** (" бит/сек ")
</dt> </dl>

Текущая пропускная способность порта в битах в секунду. Для портов, которые зависят от пропускной способности или для тех, для которых не удается выполнить точную оценку, это свойство должно содержать номинальную пропускную способность.

</dd> <dt>

**суппортедмаксимумтрансмиссионунит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")
</dt> </dl>

Максимальный размер блока передачи (MTU), поддерживаемый портом.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ЛОГИКАЛПОРТ CIM**](cim-logicalport.md)
</dt> </dl>

 

