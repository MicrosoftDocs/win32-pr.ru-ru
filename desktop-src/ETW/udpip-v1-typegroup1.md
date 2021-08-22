---
description: UdpIp_V1_TypeGroup1 класс — этот класс является классом типа события для событий UDP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: Класс UdpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2c4a16dc8e0d08ab70a15b1d6a887ff8863a1b81c46c4318421df2169fd5d196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069344"
---
# <a name="udpip_v1_typegroup1-class"></a>\_ \_ Класс TypeGroup1 удпип v1

Этот класс является классом типа событий для событий UDP/IP.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a>Члены

Класс **удпип \_ v1 \_ TypeGroup1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **удпип \_ v1 \_ TypeGroup1** имеет следующие свойства.

<dl> <dt>

даддр
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), Extension ("reduce")
</dt> </dl>

Конечный IP-адрес.

</dd> <dt>

дпорт
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5), Extension ("порт")
</dt> </dl>

Номер порта назначения.

</dd> <dt>

ИД процесса
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1)
</dt> </dl>

Идентификатор процесса, связанного с запросом.

</dd> <dt>

саддр
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Extension ("reduce")
</dt> </dl>

Исходный IP-адрес.

</dd> <dt>

размер;
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Размер пакета.

</dd> <dt>

назван
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6), Extension ("порт")
</dt> </dl>

Номер исходного порта.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Удпип \_ v1**](udpip-v1.md)
</dt> <dt>

[**удпип**](udpip.md)
</dt> </dl>

 

 




