---
description: Определяет, может ли данная строка узла разрешаться в IP-адрес.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: Функция Исресолвабликс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 580f5400b59a1142de90843e2be26790aef25a9311f7aa6f732aebeef606c701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899174"
---
# <a name="isresolvableex-function"></a>Функция Исресолвабликс

Определяет, может ли данная строка узла разрешаться в IP-адрес.

## <a name="parameters"></a>Параметры

<dl> <dt>

*узел* 
</dt> <dd>

Строка, содержащая узел HTTP, который предоставляется в Финдпроксифорурл.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если узел разрешается в IPv4-или IPv6-адрес; в противном случае — значение FALSE.

## <a name="examples"></a>Примеры

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a>См. также

<dl> <dt>

[Определения API вспомогательных функций прокси-сервера с поддержкой IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Расширения IPv6 для формата файла автоматической настройки Navigator](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



