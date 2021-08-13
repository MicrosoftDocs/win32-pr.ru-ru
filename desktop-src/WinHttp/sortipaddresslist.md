---
description: Сортирует список IP-адресов.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: Функция Сортипаддресслист
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
ms.openlocfilehash: 3144ecf044f832a49dd6aa4d9fabf76ce8e81c79c195ec101d294c432a8081e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562454"
---
# <a name="sortipaddresslist-function"></a>Функция Сортипаддресслист

Сортирует список IP-адресов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*ипаддресслист* 
</dt> <dd>

Строка, разделенная точкой с запятой, содержащая IP-адреса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Список упорядоченных IP-адресов, разделенных точкой с запятой, или пустая строка, если не удалось отсортировать список IP-адресов.

## <a name="remarks"></a>Remarks

Разработчики Финдпроксифорурлекс должны добавить код, который разбивает строку IP-адресов, разделенных точками с запятой, на отдельные адреса.

## <a name="examples"></a>Примеры

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Определения API вспомогательных функций прокси-сервера с поддержкой IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Расширения IPv6 для формата файла автоматической настройки Navigator](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



