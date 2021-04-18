---
description: Указывает период времени в минутах, в течение которого будет храниться кэш PMK.
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: Пмккачеттл (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673239"
---
# <a name="pmkcachettl-security-element"></a>Пмккачеттл (Security), элемент

Элемент Пмккачеттл (Security) указывает продолжительность времени в минутах, в течение которого будет храниться кэш PMK. Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".

Кэширование PMK описано в спецификации [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.

``` syntax
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
                value="1440"
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

 

 




