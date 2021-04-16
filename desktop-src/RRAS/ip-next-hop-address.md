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
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650387"
---
# <a name="ip_next_hop_address-structure"></a>\_ \_ Структура адреса следующего ПРЫЖКа IP \_

\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003. Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]

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

## <a name="remarks"></a>Комментарии

Структура **IP \_ - \_ \_ адреса следующего прыжка** является определением структуры [**IP- \_ сети**](ip-network.md) . Typedef находится в RTM. h.

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

[**Окончательная версия \_ IP- \_ маршрута**](rtm-ip-route.md)
</dt> </dl>

 

 





