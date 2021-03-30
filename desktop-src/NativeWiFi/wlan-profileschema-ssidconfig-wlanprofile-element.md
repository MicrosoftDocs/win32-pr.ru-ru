---
description: Содержит один или несколько идентификаторов SSID для беспроводных локальных сетей.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Ссидконфиг (Вланпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910356"
---
# <a name="ssidconfig-wlanprofile-element"></a>Ссидконфиг (Вланпрофиле), элемент

Элемент Ссидконфиг (Вланпрофиле) содержит один или несколько идентификаторов SSID для беспроводных локальных сетей.

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="SSID"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="hex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="name"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
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
            <xs:element name="nonBroadcast"
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

Элемент **ссидконфиг** определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                    | Тип                                                              | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | Содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**безымян**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | Содержит имя SSID беспроводной локальной сети (с учетом регистра).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Нешироковещательная рассылка**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [boolean](/dotnet/api/system.boolean) | Указывает, будет ли сеть рассылать свое SSID.<br/> Если для параметра [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) задано значение ESS, это может быть либо **true** , либо **false**. Значение по умолчанию — **true** , если этот элемент отсутствует.<br/> Если параметр [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) имеет значение ибсс, это значение должно быть равно **false**.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.<br/> |
| [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | Содержит идентификатор SSID для беспроводной локальной сети.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** В профиле может присутствовать не более одного элемента [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, использующих элемент **ссидконфиг** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
