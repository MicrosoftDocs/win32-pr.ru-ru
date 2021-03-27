---
description: Этот класс является классом типа событий для событий конфигурации сетевых интерфейсных карт. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: Класс SystemConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991148"
---
# <a name="systemconfig_nic-class"></a>\_Класс сетевого адаптера системконфиг

Этот класс является классом типа событий для событий конфигурации сетевых интерфейсных карт.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a>Участники

Класс **\_ сетевого адаптера системконфиг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ сетевого адаптера системконфиг** имеет следующие свойства.

<dl> <dt>

днссервераддрессес
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

IP-адреса, используемые для запросов DNS-серверов. Список адресов разделяются запятыми.

</dd> <dt>

IpAddresses
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

IP-адреса, связанные с сетевой картой. Список адресов разделяются запятыми.

</dd> <dt>

Ipv4Index
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Индекс адаптера для сетевого адаптера IPv4. Индекс адаптера может измениться, если адаптер отключен, а затем включен или в других обстоятельствах и не должен считаться постоянным.

</dd> <dt>

Ipv6Index
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Индекс адаптера для сетевого адаптера IPv6. Индекс адаптера может измениться, если адаптер отключен, а затем включен или в других обстоятельствах и не должен считаться постоянным.

</dd> <dt>

никдескриптион
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Описание адаптера.

</dd> <dt>

фисикаладдр
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Format ("x")
</dt> </dl>

Аппаратный адрес для адаптера.

</dd> <dt>

фисикаладдрлен
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Длина аппаратного адреса адаптера.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системконфиг**](systemconfig.md)
</dt> </dl>

 

 




