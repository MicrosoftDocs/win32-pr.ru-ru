---
title: Структура RTM_IP_ROUTE (RTM. h)
description: '\_Структура IP- \_ маршрута RTM содержит сведения, описывающие маршрут, принадлежащий семейству протоколов IP.'
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RAS структуры RTM_IP_ROUTE
- RAS — указатель структуры PRTM_IP_ROUTE
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672909"
---
# <a name="rtm_ip_route-structure"></a>\_Структура IP- \_ маршрута RTM

\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003. Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]

Структура **\_ IP- \_ маршрута RTM** содержит сведения, описывающие маршрут, принадлежащий семейству протоколов IP.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Метка времени RR**
</dt> <dd>

Указывает время создания или последнего обновления записи маршрута. Этот элемент задается диспетчером таблиц маршрутизации. Время выражается в виде структуры FILETIME.

</dd> <dt>

**RR \_ раутингпротокол**
</dt> <dd>

Указывает протокол маршрутизации, который добавил маршрут.

</dd> <dt>

**RR \_ InterfaceID**
</dt> <dd>

Указывает интерфейс, через который был получен маршрут.

</dd> <dt>

**RR \_ протоколспеЦификдата**
</dt> <dd>

Указывает структуру [**\_ \_ данных, характерную для протокола**](protocol-specific-data.md) , которая содержит память, зарезервированную для данных, зависящих от протокола маршрутизации.

</dd> <dt>

**RR, \_ сеть**
</dt> <dd>

Указывает структуру [**IP- \_ сети**](ip-network.md) , которая содержит адрес IP-сети.

</dd> <dt>

**RR \_ некссопаддресс**
</dt> <dd>

Указывает структуру [**IP \_ - \_ \_ адреса следующего прыжка**](ip-next-hop-address.md) , которая содержит адрес маршрутизатора следующего прыжка.

</dd> <dt>

**RR \_ фамилиспеЦификдата**
</dt> <dd>

Указывает структуру [**\_ \_ данных, относящуюся к конкретному IP-адресу**](ip-specific-data.md) , которая содержит данные, относящиеся к семейству IP-протоколов.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Члены структуры **\_ IP- \_ маршрута RTM** имеют все, что выровняйтеся по **DWORD** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                        |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по диспетчеру таблиц маршрутизации версии 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Структуры диспетчера таблиц маршрутизации версии 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**IP- \_ сеть**](ip-network.md)
</dt> <dt>

[**\_адрес следующего \_ ПРЫЖКа IP \_**](ip-next-hop-address.md)
</dt> <dt>

[**\_данные конкретного IP-адреса \_**](ip-specific-data.md)
</dt> </dl>

 

 





