---
description: Содержит идентификатор SSID для беспроводной локальной сети.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID (Ссидконфиг), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5d58ed866e79269e604fe49ad8afe65d557f27a90d0be03904b8d27da5ac5c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619061"
---
# <a name="ssid-ssidconfig-element"></a>SSID (Ссидконфиг), элемент

Элемент SSID (Ссидконфиг) содержит идентификатор SSID для беспроводной локальной сети.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** В профиле может присутствовать не более одного элемента **SSID** .

``` syntax
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
```

Элемент **SSID** определяется элементом [**ссидконфиг**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                              | Тип | Описание                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)   |      | Содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.<br/> |
| [**name**](wlan-profileschema-name-ssid-element.md) |      | Содержит идентификатор SSID для беспроводной локальной сети.<br/>                      |



## <a name="remarks"></a>Remarks

Несмотря на то, что [**шестнадцатеричные**](wlan-profileschema-hex-ssid-element.md) элементы и [**имена**](wlan-profileschema-name-ssid-element.md) являются необязательными, по крайней мере один **Шестнадцатеричный** элемент или [**имя**](wlan-profileschema-name-ssid-element.md) должны быть дочерними элементами элемента **SSID** .

Когда сведения о профиле преобразуются в идентификатор SSID, [**Шестнадцатеричный**](wlan-profileschema-hex-ssid-element.md) элемент преобразуется в SSID (если есть), а элемент [**Name**](wlan-profileschema-name-ssid-element.md) игнорируется. Если **Шестнадцатеричный** элемент отсутствует, элемент [**Name**](wlan-profileschema-name-ssid-element.md) преобразуется в идентификатор SSID с помощью преобразования Юникод в ASCII.

Если идентификатор SSID хранится в профиле, всегда создается [**Шестнадцатеричный**](wlan-profileschema-hex-ssid-element.md) элемент. Элемент [**Name**](wlan-profileschema-name-ssid-element.md) создается только в случае успешного преобразования ASCII в формат SSID и создания профиля XML. При преобразовании в [**имя**](wlan-profileschema-name-ssid-element.md)некоторые сведения из исходного идентификатора SSID могут быть потеряны.

## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, в которых используется элемент **SSID** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                |
| Распространяемые компоненты<br/>          | API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Ссидконфиг (Вланпрофиле)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




