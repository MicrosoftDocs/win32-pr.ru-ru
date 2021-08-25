---
description: — Корневой элемент, определяющий профиль мобильного широкополосного подключения.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Мбнпрофиле, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 049ec22c170afda3a46620e2e94e2a16ae2708b4d6a69fcd0262baa69352a0a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943364"
---
# <a name="mbnprofile-element"></a>Мбнпрофиле, элемент

Элемент **мбнпрофиле** является корневым элементом, идентифицирующим профиль мобильного широкополосного подключения.

На документ может быть только один элемент этого типа.

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
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

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                          | Тип                                                           | Описание                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [**аутоконнектонинтернет**](schema-autoconnectoninternet-mbnprofile-element.md) | Логическое                                                        | Будет ли устройство автоматически подключаться.<br/> |
| [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md)               |                                                                | Параметры автоматического подключения устройства.<br/>           |
| [**Локального**](schema-context-mbnprofile-element.md)                             | [**contextType**](schema-contexttype-complextype.md)          | Параметры настройки подключения к данным.<br/>              |
| [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | Предпочтительные поставщики сети для роуминга.<br/>       |
| [**Описание**](schema-description-mbnprofile-element.md)                     | [**наметипе**](schema-nametype-simpletype.md)                 | Описание профиля.<br/>                    |
| [**HomeProviderName**](schema-homeprovidername-mbnprofile-element.md)           | [**провидернаметипе**](schema-providernametype-simpletype.md) | Имя поставщика услуг домашнего доступа.<br/>                     |
| [**иконфилепас**](schema-iconfilepath-mbnprofile-element.md)                   | [**иконфилетипе**](schema-iconfiletype-simpletype.md)         | Путь к файлу значка.<br/>                         |
| [**IsDefault**](schema-isdefault-mbnprofile-element.md)                         | Логическое                                                        | Является ли профиль стандартным.<br/>            |
| [**Имя**](schema-name-mbnprofile-element.md)                                   | [**наметипе**](schema-nametype-simpletype.md)                 | Имя профиля.<br/>                           |
| [**профилекреатионтипе**](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | Сведения о создателе профиля.<br/>         |
| [**симикЦид**](schema-simiccid-mbnprofile-element.md)                           | [**симикЦидтипе**](schema-simiccidtype-simpletype.md)         | Идентификационный номер SIM-карты для устройств GSM.<br/>     |
| [**субскриберид**](schema-subscriberid-mbnprofile-element.md)                   | [**субскриберидтипе**](schema-subscriberidtype-simpletype.md) | Уникальный идентификатор профиля.<br/>              |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




