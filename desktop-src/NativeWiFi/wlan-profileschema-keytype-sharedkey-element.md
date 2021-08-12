---
description: Указывает, будет ли общий ключ представлять собой сетевой ключ или парольную фразу.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: keyType (sharedKey), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 88c9a48d1c70cd156fa3d8f63bd3b70d69a99a1151a18c95ffd556b2503c9575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619287"
---
# <a name="keytype-sharedkey-element"></a>keyType (sharedKey), элемент

Элемент keyType (sharedKey) указывает, будет ли общий ключ представлять собой сетевой ключ или парольную фразу.

``` syntax
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
```

Элемент определяется элементом [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Remarks

Если элемент [**ENCRYPTION**](wlan-profileschema-encryption-authencryption-element.md) имеет значение WEP, для параметра **KeyType** должен быть задан параметр **нетворккэй**.

## <a name="examples"></a>Примеры

Для просмотра образцов профилей, использующих элемент **KeyType** , см. пример [профиля без широковещательной рассылки](non-broadcast-profile-sample.md), [пример профиля WPA-личное](wpa-personal-profile-sample.md)и [профиль WPA2-Personal](wpa2-personal-profile-sample.md).

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

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**sharedKey (безопасность)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




