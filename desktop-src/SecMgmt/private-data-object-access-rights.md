---
description: Содержит список и описание прав доступа к закрытому объекту данных.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Права доступа к закрытому объекту данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497187"
---
# <a name="private-data-object-access-rights"></a>Права доступа к закрытому объекту данных

Типы доступа для этого типа объектов:



| Тип доступа          | Описание                                      |
|----------------------|--------------------------------------------------|
| значение СЕКРЕТного \_ запроса \_ | Этот тип доступа необходим для получения секрета. |
| \_значение набора секретов \_   | Этот тип доступа необходим для изменения секрета.   |



 

## <a name="generic-access-masks"></a>Универсальные маски доступа

Этот тип объекта имеет следующие универсальные сопоставления доступа:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Стандартные типы доступа:

Этот объект не поддерживает (необязательно) СИНХРОНИЗАЦИю стандартного типа доступа. Поддерживаются все необходимые типы доступа. Маска всех поддерживаемых типов доступа для этого типа объектов:

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



