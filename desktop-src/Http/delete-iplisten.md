---
title: delete iplisten
description: Указывает адрес IPv4 или IPv6, удаляемый из списка прослушивания IP-адресов.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- Удаление иплистен HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104069229"
---
# <a name="delete-iplisten"></a>delete iplisten

Указывает адрес IPv4 или IPv6, удаляемый из списка прослушивания IP-адресов.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ address = \]** *IPAddress*
</dt> <dd>

Указывает IPv4-или IPv6-адрес, который нужно удалить из списка прослушивания IP.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Удаляет IP-адрес из списка прослушивания IP-адресов. Это не распространяется на номер порта. Список прослушивания IP-адресов используется для определения области списка адресов, к которым привязывается служба HTTP. "0.0.0.0" означает любой IPv4-адрес, а "::" — любой IPv6-адрес.

## <a name="examples"></a>Примеры

**Удаление иплистен Address = FE80:: 1**

**удалить иплистен Address = 1.1.1.1**

**удалить адрес иплистен = 0.0.0.0**

**удалить иплистен Address =::**

 

 




