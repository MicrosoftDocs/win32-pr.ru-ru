---
description: Содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: шестнадцатеричный элемент (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682823"
---
# <a name="hex-ssid-element"></a>шестнадцатеричный элемент (SSID)

Шестнадцатеричный элемент (SSID) содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.

``` syntax
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
```

Элемент определяется элементом [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

## <a name="remarks"></a>Комментарии

Несмотря на то, что **шестнадцатеричные** элементы и [**имена**](wlan-profileschema-name-ssid-element.md) являются необязательными, по крайней мере один **Шестнадцатеричный** элемент или [**имя**](wlan-profileschema-name-ssid-element.md) должны быть дочерними элементами элемента [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Когда сведения о профиле преобразуются в идентификатор SSID, **Шестнадцатеричный** элемент преобразуется в SSID (если есть), а элемент [**Name**](wlan-profileschema-name-ssid-element.md) игнорируется. Если **Шестнадцатеричный** элемент отсутствует, элемент [**Name**](wlan-profileschema-name-ssid-element.md) преобразуется в идентификатор SSID с помощью преобразования Юникод в ASCII.

Если идентификатор SSID хранится в профиле, всегда создается **Шестнадцатеричный** элемент. Элемент [**Name**](wlan-profileschema-name-ssid-element.md) создается только в случае успешного преобразования ASCII в формат SSID и создания профиля XML. При преобразовании в [**имя**](wlan-profileschema-name-ssid-element.md)некоторые сведения из исходного идентификатора SSID могут быть потеряны.

## <a name="examples"></a>Примеры

Пример профиля, в котором используется элемент **Hex** , см. в разделе [пример профиля FIPS](fips-profile-sample.md).

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

[**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**SSID (Ссидконфиг)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




