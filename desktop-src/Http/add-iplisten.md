---
title: add iplisten
description: Указывает адрес IPv4 или IPv6, добавляемый в список прослушивания IP-адресов.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Добавить иплистен HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2133a3f590c46c9e27b518d7621c158b86895961acb07670f6603e03513d1cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014982"
---
# <a name="add-iplisten"></a>add iplisten

Указывает адрес IPv4 или IPv6, добавляемый в список прослушивания IP-адресов.

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*
</dt> <dd>

Указывает адрес IPv4 или IPv6, добавляемый в список прослушивания IP-адресов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Добавляет новый IP-адрес в список прослушивания IP-адресов. Это не распространяется на номер порта. Список прослушивания IP-адресов используется для определения области списка адресов, к которым привязывается служба HTTP. "0.0.0.0" означает любой IPv4-адрес, а "::" — любой IPv6-адрес.

## <a name="examples"></a>Примеры

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




