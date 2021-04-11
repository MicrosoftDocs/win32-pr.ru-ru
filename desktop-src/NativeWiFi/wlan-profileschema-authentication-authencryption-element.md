---
description: Указывает метод проверки подлинности, используемый для подключения к беспроводной локальной сети.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Элемент authentication (Аусенкриптион)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263474"
---
# <a name="authentication-authencryption-element"></a>Элемент authentication (Аусенкриптион)

Элемент authentication (Аусенкриптион) определяет метод проверки подлинности, используемый для подключения к беспроводной локальной сети.

``` syntax
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
```

Элемент определяется элементом [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Комментарии

В следующей таблице описаны значения перечисления.



| Значение   | Описание                            |
|---------|----------------------------------------|
| open    | Откройте аутентификацию 802,11.            |
| общие  | Общая проверка подлинности 802,11.          |
| Активация Windows     | Проверка подлинности WPA-Enterprise 802,11.  |
| впапск  | Проверка подлинности WPA-Personal 802,11.    |
| WPA2    | Проверка подлинности WPA2-Enterprise 802,11. |
| WPA2PSK | Проверка подлинности WPA2-Personal 802,11.   |



 

Дополнительные сведения о методах проверки подлинности 802,11 см. в спецификациях [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)и [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, в которых используется элемент **authentication** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).

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

 

 




