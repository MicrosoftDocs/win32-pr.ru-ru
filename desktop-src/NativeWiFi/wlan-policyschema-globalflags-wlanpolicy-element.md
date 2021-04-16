---
description: Содержит глобальные параметры для модуля автоматической настройки (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Глобалфлагс (Вланполици), элемент
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
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546815"
---
# <a name="globalflags-wlanpolicy-element"></a>Глобалфлагс (Вланполици), элемент

Элемент Глобалфлагс (Вланполици) содержит глобальные параметры для модуля автоматической настройки (ACM). Этот элемент является обязательным.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:element name="showDeniedNetwork"
                type="boolean"
             />
            <xs:element name="allowEveryoneToCreateAllUserProfiles"
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

Элемент **глобалфлагс** определяется элементом [**вланполици**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                                    | Тип    | Описание                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**алловеверйонетокреатеаллусерпрофилес**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | Логическое | Указывает, может ли любой пользователь создать профиль для всех пользователей. <br/>                                                               |
| [**енаблеаутоконфиг**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | Логическое | Указывает, используют ли компьютеры встроенную службу автоматической настройки (автоконфигурации) для управления беспроводными подключениями. <br/> |
| [**шовдениеднетворк**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | Логическое | Указывает, отображаются ли запрещенные сети в мастере **подключения к сети** . <br/>                                         |



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

 

 




