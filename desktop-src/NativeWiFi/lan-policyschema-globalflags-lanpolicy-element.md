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
ms.openlocfilehash: bfbfecbc1d60e34a913bb523f5af8c2ab25665fd689976c87725d392f6ea26c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801134"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**ланполици**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**ланполици**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




