---
description: Содержит глобальные параметры для автоматической настройки проводных сетей.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Глобалфлагс (Ланполици), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265406"
---
# <a name="globalflags-lanpolicy-element"></a>Глобалфлагс (Ланполици), элемент

Элемент Глобалфлагс (Ланполици) содержит глобальные параметры для автоматической настройки проводных сетей.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент **глобалфлагс** определяется элементом [**ланполици**](lan-policyschema-lanpolicy-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Тип    | Описание                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**енаблеаутоконфиг**](lan-policyschema-enableautoconfig-globalflags-element.md) | Логическое | Указывает, используют ли компьютеры встроенную службу автоматической настройки для управления подключениями к проводным сетям, для которых требуется проверка подлинности уровня 2 (например, 802.1 X).<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**ланполици**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**ланполици**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




