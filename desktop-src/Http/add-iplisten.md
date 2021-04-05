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
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "103987247"
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

## <a name="remarks"></a>Комментарии

Добавляет новый IP-адрес в список прослушивания IP-адресов. Это не распространяется на номер порта. Список прослушивания IP-адресов используется для определения области списка адресов, к которым привязывается служба HTTP. "0.0.0.0" означает любой IPv4-адрес, а "::" — любой IPv6-адрес.

## <a name="examples"></a>Примеры

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




