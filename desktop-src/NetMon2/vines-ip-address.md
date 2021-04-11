---
description: '\_Структура IP- \_ адресов vines представляет собой IP-адрес в сети Vines.'
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Структура VINES_IP_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346295"
---
# <a name="vines_ip_address-structure"></a>\_Структура IP-адресов vines \_

Структура **\_ IP- \_ адресов vines** представляет собой IP-адрес в сети Vines.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Члены

<dl> <dt>

**нетид**
</dt> <dd>

Идентификатор определенного компьютера в определенной подсети.

</dd> <dt>

**SubnetID**
</dt> <dd>

Идентификатор определенной подсети в целой сети.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




