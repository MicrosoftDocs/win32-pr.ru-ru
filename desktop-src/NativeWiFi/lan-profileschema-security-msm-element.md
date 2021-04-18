---
description: Содержит параметры безопасности для проводных сетей.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Элемент Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105674763"
---
# <a name="security-msm-element-lan_policy"></a>Элемент Security (MSM) (LAN_policy)

Элемент Security (MSM) содержит параметры безопасности для проводных сетей. Этот элемент является необязательным.

``` syntax
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
```

Элемент **Security** определяется элементом [**MSM**](lan-profileschema-msm-lanprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                 | Тип    | Описание                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**онексенаблед**](lan-profileschema-onexenabled-security-element.md)   | Логическое | Указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 X. <br/>      |
| [**онексенфорцед**](lan-profileschema-onexenforced-security-element.md) | Логическое | Указывает, требует ли служба автоматической настройки для проводных сетей использование 802.1 X для проверки подлинности портов. <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**MSM**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**MSM (Ланпрофиле)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




