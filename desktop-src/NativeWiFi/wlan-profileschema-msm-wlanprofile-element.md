---
description: Содержит различные параметры модуля для конкретных носителей (MSM).
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: Элемент MSM (Вланпрофиле)
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
ms.openlocfilehash: 78540c29239df9118732561562985021a512e104b0ddc5e05d43d89f37dd5e33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797944"
---
# <a name="msm-wlanprofile-element"></a>Элемент MSM (Вланпрофиле)

Элемент MSM (Вланпрофиле) содержит различные параметры модуля для конкретных носителей (MSM).

``` syntax
<xs:element name="MSM"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="phyType"
                            minOccurs="0"
                            maxOccurs="4"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="a"
                                     />
                                    <xs:enumeration
                                        value="b"
                                     />
                                    <xs:enumeration
                                        value="g"
                                     />
                                    <xs:enumeration
                                        value="n"
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
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
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
                        <xs:element name="sharedKey"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="keyType">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="networkKey"
                                                 />
                                                <xs:enumeration
                                                    value="passPhrase"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="protected"
                                        type="boolean"
                                     />
                                    <xs:element name="keyMaterial"
                                        type="string"
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
                        <xs:element name="keyIndex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="0"
                                     />
                                    <xs:maxInclusive
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheMode"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="disabled"
                                     />
                                    <xs:enumeration
                                        value="enabled"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheTTL"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="5"
                                     />
                                    <xs:maxInclusive
                                        value="1400"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheSize"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="1"
                                     />
                                    <xs:maxInclusive
                                        value="255"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="preAuthMode"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="disabled"
                                     />
                                    <xs:enumeration
                                        value="enabled"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="preAuthThrottle"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="1"
                                     />
                                    <xs:maxInclusive
                                        value="16"
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

Элемент определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип                                                              | Описание                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**идентификаци**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Подключение**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Содержит различные параметры подключения. Этот элемент является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**ключ**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Задает шифрование данных, используемое для подключения к беспроводной локальной сети.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Указывает, какой индекс ключа должен использоваться для шифрования беспроводного трафика. Используется, только если параметр keyType имеет значение Нетворккэй.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [строка](/dotnet/api/system.string)   | Содержит ключ сети или парольную фразу.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Тип ключа.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**фитипе**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Указывает стандарт беспроводной локальной сети 802,11, используемый в беспроводной локальной сети. значение n поддерживается только в Windows Vista с пакетом обновления 1 (SP1) и более поздними версиями операционной системы.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.<br/>                                                                                                                        |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Указывает, будет ли использоваться кэширование PMK. Этот элемент допустим только для сетей, определенных WPA2.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Указывает количество записей в кэше ОМК на клиенте. Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled. Если включен режим Пмккаче и этот элемент отсутствует, по умолчанию размер кэша составляет 128 записей.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Указывает период времени в минутах, в течение которого будет храниться кэш PMK. Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Определяет, будет ли клиент использовать предварительную проверку подлинности. Предварительная проверка подлинности обеспечивает безопасное быстрое перемещение WPA2. Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled. Если включен режим Пмккаче и этот элемент отсутствует, значение по умолчанию — disabled.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Указывает число попыток при предварительной проверке подлинности на соседних ТД. Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled. Если включен режим Пмккаче и этот элемент отсутствует, число попыток по умолчанию будет равно 3.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.<br/>                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Указывает, зашифрован ли ключ.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент должен иметь значение FALSE.<br/>                                                                                                                                                                                                                                                 |
| [**бюллетеня**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Содержит различные параметры безопасности. Этот элемент является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Содержит сведения об общем ключе. Этот элемент необходим только в том случае, если для пары "Проверка подлинности и шифрование" требуются ключи WEP или PSK.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Указывает, используется ли 802.1 X. Этот флаг является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Remarks

Элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) может быть вставлен как дочерний элемент элемента [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) . Элемент [**OneX**](onexschema-onex-element.md) может быть вставлен как дочерний элемент элемента [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .

## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, в которых используется элемент **MSM** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                |
| Распространяемые компоненты<br/>          | API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Образцы профиля беспроводной связи](wireless-profile-samples.md)
</dt> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
