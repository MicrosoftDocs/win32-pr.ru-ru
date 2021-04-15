---
description: Указывает стандарт беспроводной локальной сети 802,11, используемый в беспроводной локальной сети.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Элемент Фитипе (Connectivity)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682600"
---
# <a name="phytype-connectivity-element"></a>Элемент Фитипе (Connectivity)

Элемент Фитипе (подключение) указывает стандарт беспроводной локальной сети 802,11, используемый в беспроводной локальной сети.

Можно указать несколько **фитипе** s. Если **фитипе** не указан, профиль можно использовать для подключения к любому **фитипе**. Значение n поддерживается только в Windows Vista с пакетом обновления 1 (SP1) и более поздними версиями операционной системы.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.

``` syntax
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
```

Элемент определяется элементом [**подключения**](wlan-profileschema-connectivity-msm-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**установлен**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**подключение (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




