---
title: Структура RTM_IPX_ROUTE (RTM. h)
description: '\_ \_ Структура маршрута RTM IPX содержит сведения, описывающие маршрут для семейства протоколов IPX.'
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RAS структуры RTM_IPX_ROUTE
- RAS — указатель структуры PRTM_IPX_ROUTE
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988430"
---
# <a name="rtm_ipx_route-structure"></a>\_ \_ Структура маршрута RTM IPX

\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003. Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]

Структура **\_ \_ маршрута RTM IPX** содержит сведения, описывающие маршрут для семейства протоколов IPX.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
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

Указывает [**специфичную для протокола структуру \_ \_ данных**](protocol-specific-data.md) , которая содержит память, зарезервированную для данных, относящихся к протоколам маршрутизации.

</dd> <dt>

**RR, \_ сеть**
</dt> <dd>

Указывает структуру [**\_ сети IPX**](ipx-network.md) , которая содержит IP-адрес.

</dd> <dt>

**RR \_ некссопаддресс**
</dt> <dd>

Указывает структуру [**\_ \_ \_ адресов следующего прыжка IPX**](ipx-next-hop-address.md) , которая содержит адрес маршрутизатора следующего прыжка.

</dd> <dt>

**RR \_ фамилиспеЦификдата**
</dt> <dd>

Указывает структуру [**\_ \_ данных, характерную**](ipx-specific-data.md) для протокола IPX, которая содержит данные, относящиеся к семейству протоколов IPX.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Элементы структуры **маршрута RTM- \_ IPX \_** выводятся полностью по **значению DWORD** .

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

[Структуры диспетчера таблиц маршрутизации версии \_ 1 \_](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_сеть IPX**](ipx-network.md)
</dt> <dt>

[**\_адрес следующего \_ ПРЫЖКа IPX \_**](ipx-next-hop-address.md)
</dt> <dt>

[**\_данные, относящиеся к IPX \_**](ipx-specific-data.md)
</dt> </dl>

 

 





