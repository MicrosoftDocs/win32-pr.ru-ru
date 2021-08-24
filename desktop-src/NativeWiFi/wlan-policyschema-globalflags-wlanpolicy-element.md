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
ms.openlocfilehash: 2851ae779bf1693d44642f87d33a71c17000e9dc0b68eeb8daab83972b37457d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800334"
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
| [**шовдениеднетворк**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | Логическое | указывает, отображаются ли запрещенные сети в мастере **Подключение сети** . <br/>                                         |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**вланполици**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**вланполици**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




