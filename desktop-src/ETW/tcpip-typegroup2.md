---
description: Этот класс является классом типа событий для событий IPv4 TCP/IP Connect и Accept. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: Класс TcpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544319"
---
# <a name="tcpip_typegroup2-class"></a>\_Класс TcpIp TypeGroup2

Этот класс является классом типа событий для событий IPv4 TCP/IP Connect и Accept.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Участники

Класс **TcpIp \_ TypeGroup2** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **TcpIp \_ TypeGroup2** имеет следующие свойства.

<dl> <dt>

**коннид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (15)**, **pointer**
</dt> </dl>

Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.

</dd> <dt>

**даддр**
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (3)**, **Extension ("IPAddrV4")**
</dt> </dl>

Конечный IP-адрес.

</dd> <dt>

**дпорт**
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (5)**, **Extension ("порт")**
</dt> </dl>

Номер порта назначения.

</dd> <dt>

**MSS**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (7)**
</dt> </dl>

Максимальный размер сегмента.

</dd> <dt>

**PID**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (1)**
</dt> </dl>

Идентификатор процесса, связанного с запросом.

</dd> <dt>

**ркввин**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (11)**
</dt> </dl>

Размер окна приема TCP.

</dd> <dt>

**ркввинскале**
</dt> <dd> <dl> <dt>

Тип данных: **sint16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (12)**
</dt> </dl>

Коэффициент масштабирования окна приема TCP.

</dd> <dt>

**саккопт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (8)**
</dt> </dl>

Параметр селективного подтверждения (SACK) в заголовке TCP.

</dd> <dt>

**саддр**
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (4)**, **Extension ("IPAddrV4")**
</dt> </dl>

Исходный IP-адрес.

</dd> <dt>

**секнум**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (14)**
</dt> </dl>

Порядковый номер.

</dd> <dt>

**size**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (2)**
</dt> </dl>

Размер пакета.

</dd> <dt>

**сндвинскале**
</dt> <dd> <dl> <dt>

Тип данных: **sint16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (13)**
</dt> </dl>

Коэффициент масштабирования окна отправки TCP.

</dd> <dt>

**назван**
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (6)**, **Extension ("порт")**
</dt> </dl>

Номер исходного порта.

</dd> <dt>

**тсопт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (9)**
</dt> </dl>

Параметр временной метки в заголовке TCP.

</dd> <dt>

**всопт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид (10)**
</dt> </dl>

Параметр масштабирования окна в заголовке TCP.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TcpIp**](tcpip.md)
</dt> </dl>

 

 




