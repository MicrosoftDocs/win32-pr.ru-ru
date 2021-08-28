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
ms.openlocfilehash: a45d811bedfa1d2a228cd29decf2272d85b8ca6de5c1d27656b3e37b8d6b4d4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870544"
---
# <a name="delete-sslcert"></a>delete sslcert

Удаляет привязки сертификатов сервера SSL и соответствующие политики сертификатов клиента для IP-адреса и порта.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ иппорт = \]**_IP-адрес: порт_
</dt> <dd>

Указывает адрес или порт IPv4 или IPv6, для которого будут удалены привязки SSL-сертификатов.

</dd> </dl>

## <a name="examples"></a>Примеры

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**Delete sslcert иппорт = \[ ::: \] 443**

 

 




