---
title: Типы данных службы удаленного доступа (RAS. h)
description: API службы удаленного доступа использует следующие типы данных.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988621"
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
> Поддерживается в Windows Vista и более поздних версиях Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

[**In6 адрес \_ ,**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) который содержит IPv6-адреса.

> [!Note]  
> Поддерживается в Windows Vista и более поздних версиях Windows.

 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



 

