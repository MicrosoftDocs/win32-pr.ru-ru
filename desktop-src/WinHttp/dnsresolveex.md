---
description: Разрешение строки узла в IP-адрес
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: Функция Днсресолвикс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1c63ba3e20653c41864394d9c563c851f2aab5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712552"
---
# <a name="dnsresolveex-function"></a>Функция Днсресолвикс

Разрешение строки узла в IP-адрес

## <a name="parameters"></a>Параметры

<dl> <dt>

*хост* 
</dt> <dd>

Строка, содержащая узел HTTP, который предоставляется в Финдпроксифорурл.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Строка с разделителями-двоеточием, содержащая адреса IPv6 и IPv4, или пустая строка, если узел не разрешается.

## <a name="remarks"></a>Комментарии

Разработчики Финдпроксифорурлекс должны добавить код, который разбивает строку IP-адресов, разделенных точками с запятой, на отдельные адреса.

## <a name="examples"></a>Примеры

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Определения API вспомогательных функций прокси-сервера с поддержкой IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Расширения IPv6 для формата файла автоматической настройки Navigator](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



