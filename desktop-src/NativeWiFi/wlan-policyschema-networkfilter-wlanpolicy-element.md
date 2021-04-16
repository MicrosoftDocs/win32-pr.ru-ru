---
description: Определяет список разрешенных и запрещенных сетей для компьютеров.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Нетворкфилтер (Вланполици), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684234"
---
# <a name="networkfilter-wlanpolicy-element"></a>Нетворкфилтер (Вланполици), элемент

Элемент Нетворкфилтер (Вланполици) определяет список разрешенных и запрещенных сетей для компьютеров.

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="network"
                            type="networkItemType"
                            maxOccurs="unbounded"
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
            <xs:element name="blockList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="network"
                            type="networkItemType"
                            maxOccurs="unbounded"
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
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
                type="boolean"
                minOccurs="0"
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

Элемент **нетворкфилтер** определяется элементом [**вланполици**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                    | Тип                                                                     | Описание                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**Разрешенных**](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | Список беспроводных ЛОКАЛЬНЫХ сетей, к которым может подключаться любой компьютер. <br/> |
| [**Списка блокировки**](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | Список беспроводных ЛОКАЛЬНЫХ сетей, к которым компьютер не должен подключаться.<br/>              |
| [**деняллесс**](wlan-policyschema-denyalless-networkfilter-element.md)   | Логическое                                                                  | Указывает, заблокирован ли доступ ко всем сетям инфраструктуры. <br/>                     |
| [**деняллибсс**](wlan-policyschema-denyallibss-networkfilter-element.md) | Логическое                                                                  | Указывает, заблокирован ли доступ ко всем компьютерным сетям. <br/>                             |
| [**сети**](wlan-policyschema-network-allowlist-element.md)             | [**нетворкитемтипе**](wlan-policyschema-networkitemtype-complextype.md) | Разрешенная сеть. <br/>                                                                |
| [**сети**](wlan-policyschema-network-blocklist-element.md)             | [**нетворкитемтипе**](wlan-policyschema-networkitemtype-complextype.md) | Заблокированная сеть. <br/>                                                                 |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**вланполици**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**вланполици**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




