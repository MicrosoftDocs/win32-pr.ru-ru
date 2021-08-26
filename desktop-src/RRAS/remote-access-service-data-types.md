---
title: Типы данных службы удаленного доступа (RAS. h)
description: API службы удаленного доступа использует следующие типы данных.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26df8b8336b9b96ec338a79ed846519fb8a0ca019e6dd5996b9ac17087faa371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028254"
---
# <a name="remote-access-service-data-types"></a>Типы данных службы удаленного доступа

API службы удаленного доступа использует следующие типы данных.


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

**RASIPV4ADDR**
</dt> <dd>

Значение [**в \_ адресе**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) , содержащее IPv4-адрес.

> [!Note]  
> поддерживается в Windows Vista и более поздних версиях Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

[**In6 адрес \_ ,**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) который содержит IPv6-адреса.

> [!Note]  
> поддерживается в Windows Vista и более поздних версиях Windows.

 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



 

