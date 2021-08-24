---
title: Структура PROTOCOL_SPECIFIC_DATA (RTM. h)
description: '\_Структура данных, характерная для протокола, \_ содержит память, зарезервированную для данных конкретного протокола маршрутизации.'
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- RAS структуры PROTOCOL_SPECIFIC_DATA
- RAS — указатель структуры PPROTOCOL_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe43e17827a4c6308c7bfd4499de60ec9105a9fa525ab5aad0226887d02ae8e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036464"
---
# <a name="protocol_specific_data-structure"></a>\_Структура данных, характерная для протокола \_

\[этот api был заменен api [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003. Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]

Структура **\_ \_ данных, характерная для протокола** , содержит память, зарезервированную для данных конкретного протокола маршрутизации.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Данные PSD**
</dt> <dd>

Задает массив переменных **типа DWORD** . Эта память резервируется для данных, относящихся к протоколам маршрутизации.

</dd> </dl>

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

[**Окончательная версия \_ IP- \_ маршрута**](rtm-ip-route.md)
</dt> <dt>

[**\_маршрут IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

 





