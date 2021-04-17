---
description: Определяет, находится ли IP-адрес в определенной подсети.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: Функция Исиннетекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702893"
---
# <a name="isinnetex-function"></a>Функция Исиннетекс

Определяет, находится ли IP-адрес в определенной подсети.

## <a name="parameters"></a>Параметры

<dl> <dt>

*IP* 
</dt> <dd>

Строка, содержащая адреса IPv6/IPv4.

</dd> <dt>

*иппрефикс* 
</dt> <dd>

Строка, содержащая префикс IP с разделителями-двоеточием с старшими n битами, указанными в битовом поле (т. е. 3FFE: 8311: FFFF::/48 или 123.112.0.0/16).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если узел находится в той же подсети; в противном случае — значение FALSE.

Также возвращает значение FALSE, если префикс имеет неправильный формат или если в сравнении используются адреса и префиксы различных типов (т. е. префикс IPv4 и IPv6-адрес).

## <a name="examples"></a>Примеры

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Определения API вспомогательных функций прокси-сервера с поддержкой IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Расширения IPv6 для формата файла автоматической настройки Navigator](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



