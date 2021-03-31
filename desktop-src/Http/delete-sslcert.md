---
title: delete sslcert
description: Удаляет привязки сертификатов сервера SSL и соответствующие политики сертификатов клиента для IP-адреса и порта.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- Удаление sslcert HTTP
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7672df5eee1634c41ff153435edcbecc58c2595
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "103784539"
---
# <a name="delete-sslcert"></a>delete sslcert

Удаляет привязки сертификатов сервера SSL и соответствующие политики сертификатов клиента для IP-адреса и порта.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[иппорт = \] * * * IP-адрес: порт*
</dt> <dd>

Указывает адрес или порт IPv4 или IPv6, для которого будут удалены привязки SSL-сертификатов.

</dd> </dl>

## <a name="examples"></a>Примеры

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**Delete sslcert иппорт = \[ ::: \] 443**

 

 




