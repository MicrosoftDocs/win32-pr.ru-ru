---
description: Содержит идентификатор SSID беспроводной локальной сети.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: Элемент Name (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911896"
---
# <a name="name-ssid-element"></a>Элемент Name (SSID)

Элемент Name (SSID) содержит идентификатор SSID беспроводной локальной сети.

``` syntax
<xs:element name="name">
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
```

Элемент определяется элементом [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

## <a name="remarks"></a>Remarks

В именах учитывается регистр.

Несмотря на то, что [**шестнадцатеричные**](wlan-profileschema-hex-ssid-element.md) элементы и **имена** являются необязательными, по крайней мере один **Шестнадцатеричный** элемент или **имя** должны быть дочерними элементами элемента [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Когда сведения о профиле преобразуются в идентификатор SSID, [**Шестнадцатеричный**](wlan-profileschema-hex-ssid-element.md) элемент преобразуется в SSID (если есть), а элемент **Name** игнорируется. Если **Шестнадцатеричный** элемент отсутствует, элемент **Name** преобразуется в идентификатор SSID с помощью преобразования Юникод в ASCII.

Если идентификатор SSID хранится в профиле, всегда создается [**Шестнадцатеричный**](wlan-profileschema-hex-ssid-element.md) элемент. Элемент **Name** создается только в случае успешного преобразования ASCII в формат SSID и создания профиля XML. При преобразовании в **имя** некоторые сведения из исходного идентификатора SSID могут быть потеряны.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Escape-символы XML, такие как &, не отображаются. Избегайте использования escape-символов XML в именах SSID для профилей, развернутых в Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2).

## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, в которых используется элемент **Name** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).

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

 

 




