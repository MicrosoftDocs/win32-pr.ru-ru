---
description: Содержит параметры модуля для конкретных носителей (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Элемент MSM (Ланпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265403"
---
# <a name="msm-lanprofile-element"></a>Элемент MSM (Ланпрофиле)

Элемент MSM (Ланпрофиле) содержит параметры модуля для конкретного носителя (MSM).

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="security">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OneXEnforced"
                            type="boolean"
                         />
                        <xs:element name="OneXEnabled"
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

Элемент **MSM** определяется элементом [**ланпрофиле**](lan-profileschema-lanprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                 | Тип    | Описание                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**онексенаблед**](lan-profileschema-onexenabled-security-element.md)   | Логическое | Указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 X.<br/>       |
| [**онексенфорцед**](lan-profileschema-onexenforced-security-element.md) | Логическое | Указывает, требует ли служба автоматической настройки для проводных сетей использование 802.1 X для проверки подлинности портов. <br/> |
| [**бюллетеня**](lan-profileschema-security-msm-element.md)              |         | Содержит параметры безопасности. <br/>                                                                                                  |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**ланпрофиле**](lan-profileschema-lanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**ланпрофиле**](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




