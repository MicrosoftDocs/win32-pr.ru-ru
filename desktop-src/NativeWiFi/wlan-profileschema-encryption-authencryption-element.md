---
description: Указывает тип шифрования данных, используемый для подключения к беспроводной локальной сети.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Элемент encryption (Аусенкриптион)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154575"
---
# <a name="encryption-authencryption-element"></a>Элемент encryption (Аусенкриптион)

Элемент encryption (Аусенкриптион) указывает тип шифрования данных, используемый для подключения к беспроводной локальной сети.

``` syntax
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
```

Элемент определяется элементом [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Комментарии

Если элемент **ENCRYPTION** имеет значение WEP, для параметра [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) должен быть задан параметр **нетворккэй**.

Метод шифрования AES указан в спецификациях [802.1 x](https://ieeexplore.ieee.org/document/1438730) и [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, в которых используется элемент **ENCRYPTION** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Аусенкриптион (безопасность)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




