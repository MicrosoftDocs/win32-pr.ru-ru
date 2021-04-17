---
description: Идентифицирует независимый поставщик оборудования.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Ауихеадер (IHV), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673242"
---
# <a name="ouiheader-ihv-element"></a>Ауихеадер (IHV), элемент

Элемент Ауихеадер (IHV) идентифицирует независимый поставщик оборудования.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="type">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="1"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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

Элемент определяется элементом [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                   | Тип | Описание                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [**КОДОМ**](wlan-profileschema-oui-ouiheader-element.md)   |      | Содержит 3-байтовый hexBinary, определяющий IHV.<br/>                            |
| [**Тип**](wlan-profileschema-type-ouiheader-element.md) |      | Содержит 1-байтовый hexBinary, используемый для различения сетевых карт одним и тем же IHV.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**АППАРАТ**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**IHV (Вланпрофиле)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




