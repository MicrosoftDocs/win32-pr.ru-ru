---
title: Структура IP_NEXT_HOP_ADDRESS (RTM. h)
description: Структура IP \_ - \_ адреса следующего прыжка \_ содержит адрес маршрутизатора следующего ПРЫЖКА для IP-маршрута.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- RAS структуры IP_NEXT_HOP_ADDRESS
- RAS структуры PIP_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f79b850c7d5f48e5f409e5380ad7345288187b8939b752b4f282b2274a99cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790968"
---
# <a name="ip_next_hop_address-structure"></a>\_ \_ Структура адреса следующего ПРЫЖКа IP \_

\[этот api был заменен api [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003. Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]

Структура **IP \_ - \_ \_ адреса следующего прыжка** содержит адрес маршрутизатора следующего прыжка для IP-маршрута.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Члены

<dl> <dt>

**N \_ нетнумбер**
</dt> <dd>

Указывает адрес IP-сети, выраженный в виде IP-адреса в порядке байтов на компьютере.

</dd> <dt>

**N \_ Маска сети**
</dt> <dd>

Указывает маску сети. Примените эту маску к IP-адресу, чтобы извлечь сетевой адрес. Маска сети находится в порядке байтов на уровне компьютера.

</dd> </dl>

## <a name="remarks"></a>Remarks

Структура **IP \_ - \_ \_ адреса следующего прыжка** является определением структуры [**IP- \_ сети**](ip-network.md) . Typedef находится в RTM. h.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                        |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по диспетчеру таблиц маршрутизации версии 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Структуры диспетчера таблиц маршрутизации версии 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**IP- \_ сеть**](ip-network.md)
</dt> <dt>

[**Окончательная версия \_ IP- \_ маршрута**](rtm-ip-route.md)
</dt> </dl>

 

 





