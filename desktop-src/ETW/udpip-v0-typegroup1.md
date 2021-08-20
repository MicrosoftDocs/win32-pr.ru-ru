---
description: UdpIp_V0_TypeGroup1 класс — этот класс является классом типа события для событий UDP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: Класс UdpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8061009fcf419bd7b5ab04eda0b056a8ccee1ad3f3b990a0846058599f34fbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813766"
---
# <a name="udpip_v0_typegroup1-class"></a>\_Класс удпип v0 \_ TypeGroup1

Этот класс является классом типа событий для событий UDP/IP.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a>Члены

Класс **удпип \_ v0 \_ TypeGroup1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **удпип \_ v0 \_ TypeGroup1** имеет следующие свойства.

<dl> <dt>

контекст
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Идентификатор процесса для объекта Address, который сделал или получил запрос.

</dd> <dt>

даддр
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5), Extension ("reduce")
</dt> </dl>

Конечный IP-адрес.

</dd> <dt>

дпорт
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6), Extension ("порт")
</dt> </dl>

Номер порта назначения.

</dd> <dt>

дсизе
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (7)
</dt> </dl>

Размер пакета назначения.

</dd> <dt>

саддр
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Extension ("reduce")
</dt> </dl>

Исходный IP-адрес.

</dd> <dt>

размер;
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Размер исходного пакета.

</dd> <dt>

назван
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), расширение ("порт")
</dt> </dl>

Номер исходного порта.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Удпип \_ v0**](udpip-v0.md)
</dt> </dl>

 

 




