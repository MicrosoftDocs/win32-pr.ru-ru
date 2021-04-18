---
description: Указывает количество записей в кэше PMK на клиенте.
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: Пмккачесизе (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673240"
---
# <a name="pmkcachesize-security-element"></a>Пмккачесизе (Security), элемент

Элемент Пмккачесизе (Security) указывает количество записей в кэше PMK на клиенте. Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled". Если **пмккачемоде** включен и этот элемент отсутствует, размер кэша по умолчанию составляет 128 записей.

Кэширование PMK описано в спецификации [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.

``` syntax
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
```

Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



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

 

 




