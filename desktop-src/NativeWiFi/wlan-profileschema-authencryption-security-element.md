---
description: Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Аусенкриптион (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673443"
---
# <a name="authencryption-security-element"></a>Аусенкриптион (Security), элемент

Элемент Аусенкриптион (Security) указывает пару проверки подлинности и шифрования, которая будет использоваться для этого профиля.

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="encryption">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="none"
                         />
                        <xs:enumeration
                            value="WEP"
                         />
                        <xs:enumeration
                            value="TKIP"
                         />
                        <xs:enumeration
                            value="AES"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="useOneX"
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

Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип                                                              | Описание                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**идентификаци**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Указывает метод проверки подлинности, который должен использоваться для подключения к беспроводной локальной сети.<br/> |
| [**ключ**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Задает шифрование данных, используемое для подключения к беспроводной локальной сети.<br/>                       |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Указывает, используется ли 802.1 X.<br/>                                                     |



## <a name="remarks"></a>Комментарии

Элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) может быть вставлен как дочерний элемент элемента **аусенкриптион** .

## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, использующих элемент **аусенкриптион** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md). Пример профиля, в котором используется элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) , см. в разделе [пример профиля FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Образцы профиля беспроводной связи](wireless-profile-samples.md)
</dt> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**бюллетеня**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**безопасность (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
