---
description: Содержит общие сведения о ключе.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: sharedKey (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673897"
---
# <a name="sharedkey-security-element"></a>sharedKey (Security), элемент

Элемент sharedKey (Security) содержит общие сведения о ключе. Этот элемент необходим только в том случае, если для пары "Проверка подлинности и шифрование" требуются ключи WEP или PSK.

``` syntax
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
```

Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                 | Тип                                                              | Описание                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md) | [string](/dotnet/api/system.string)   | Содержит ключ сети или парольную фразу.<br/>                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | Тип ключа.<br/>                                                                                                                                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)     | [boolean](/dotnet/api/system.boolean) | Указывает, зашифрован ли ключ.<br/> **Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент должен иметь значение FALSE.<br/> |



## <a name="remarks"></a>Комментарии

Для Windows Vista и Windows Server 2008 данные, связанные с элементом **sharedKey** , шифруются перед сохранением в хранилище профилей.

Для Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2) данные не шифруются.

## <a name="examples"></a>Примеры

Для просмотра образцов профилей, использующих элемент **sharedKey** , см. пример [профиля без широковещательной рассылки](non-broadcast-profile-sample.md), [пример профиля WPA-личное](wpa-personal-profile-sample.md)и [профиль WPA2-Personal](wpa2-personal-profile-sample.md).

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

[**бюллетеня**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**безопасность (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
