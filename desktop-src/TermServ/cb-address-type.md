---
title: Перечисление CB_ADDRESS_TYPE (Кбклиент. h)
description: Указывает тип адреса.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- Перечисление CB_ADDRESS_TYPE службы удаленных рабочих столов
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50903baa9fe85685ef3390ee3d545dd7defff5288d0960d6a2d7ec6ebe2276ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001702"
---
# <a name="cb_address_type-enumeration"></a>\_ \_ Перечисление типов адресов CB

Указывает тип адреса.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**адрес CB не \_ \_ определен**
</dt> <dd>

Тип адреса не определен.

</dd> <dt>

<span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**Адрес версии-получателя CB \_ \_**
</dt> <dd>

Адрес — это IPv4-адрес.

</dd> <dt>

<span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**\_Адрес \_ версии-получателя CB**
</dt> <dd>

Адрес является адресом IPv6.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>Кбклиент. h</dt> </dl> |



 

 





