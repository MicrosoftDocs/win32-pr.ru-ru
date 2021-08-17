---
description: Содержит профиль проводной сети.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Ланпрофиле, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6adaa0f4884ad275137a6c949dbc466416006f33bb6603dc61e87153d9b23361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065104"
---
# <a name="lanprofile-element"></a>Ланпрофиле, элемент

Элемент Ланпрофиле содержит профиль проводной сети. Этот элемент является уникальным корневым элементом для профиля проводной сети.

Целевое пространство имен для элемента Ланпрофиле — `https://www.microsoft.com/networking/LAN/profile/v1` .

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
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

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                 | Тип    | Описание                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSM**](lan-profileschema-msm-lanprofile-element.md)                 |         | Содержит параметры модуля для конкретных носителей (MSM). <br/>                                                                               |
| [**онексенаблед**](lan-profileschema-onexenabled-security-element.md)   | Логическое | Указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 X. <br/>      |
| [**онексенфорцед**](lan-profileschema-onexenforced-security-element.md) | Логическое | Указывает, требует ли служба автоматической настройки для проводных сетей использование 802.1 X для проверки подлинности портов. <br/> |
| [**бюллетеня**](lan-profileschema-security-msm-element.md)              |         | Содержит параметры безопасности. <br/>                                                                                                  |



## <a name="remarks"></a>Remarks

Сведения о просмотре списка дочерних элементов в древовидной структуре см. в разделе [ \_ элементы схемы профиля локальной сети](lan-profileschema-elements.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




