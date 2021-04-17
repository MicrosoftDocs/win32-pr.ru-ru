---
description: Содержит различные параметры безопасности, используемые независимыми поставщиками оборудования.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Элемент безопасности (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673898"
---
# <a name="security-ihv-element"></a>Элемент безопасности (IHV)

Элемент Security (IHV) содержит различные параметры безопасности, используемые независимыми поставщиками оборудования.

Параметры безопасности Microsoft и параметры безопасности IHV являются взаимоисключающими. Если оба набора параметров безопасности находятся в одном профиле, профиль будет недействительным.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент **безопасности** определяется элементом [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**АППАРАТ**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**IHV (Вланпрофиле)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




