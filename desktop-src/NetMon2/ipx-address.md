---
description: Структура IPX- \_ адреса предоставляет адрес на уровне протокола IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Структура IPX_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541183"
---
# <a name="ipx_address-structure"></a>\_Структура адреса IPX

Структура **IPX- \_ адреса** предоставляет адрес на уровне протокола IPX.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Подсеть**
</dt> <dd>

Идентификатор подсети сети.

</dd> <dt>

**Адрес**
</dt> <dd>

Идентификатор подсети NIC.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




