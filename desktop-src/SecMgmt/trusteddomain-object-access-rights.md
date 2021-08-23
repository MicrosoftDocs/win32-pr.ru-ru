---
description: Содержит список и описание прав доступа объекта Трустеддомаин.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Права доступа к объекту Трустеддомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efeaf621cc3727cb936e69806bbcf89dabe5d41eb39b38dce3f9f23a0200dcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893012"
---
# <a name="trusteddomain-object-access-rights"></a>Права доступа к объекту Трустеддомаин

Тип объекта [**трустеддомаин**](trusteddomain-object.md) имеет следующие типы доступа:



| Тип доступа                  | Описание                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| \_ \_ доменное имя доверенного запроса \_ | Этот тип доступа необходим для запроса имени доверенного домена.              |
| ДОВЕРЕНные \_ наборы \_ контроллеров    | Этот тип доступа необходим для задания списка контроллеров доверенного домена. |
| POSIX TRUSTed \_ Query \_        | Этот тип доступа необходим для получения смещения идентификатора POSIX доверенного домена.  |
| ДОВЕРЕНный \_ набор \_ POSIX          | Этот тип доступа необходим для установки смещения идентификатора POSIX доверенного домена.       |



 

## <a name="generic-access-masks"></a>Универсальные маски доступа

Этот тип объекта имеет следующие универсальные сопоставления доступа:

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a>Стандартные типы доступа

Этот объект не поддерживает (необязательно) СИНХРОНИЗАЦИю стандартного типа доступа. Поддерживаются все необходимые типы доступа. Маска всех поддерживаемых типов доступа для этого типа объектов:

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



