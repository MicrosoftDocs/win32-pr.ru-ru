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
ms.openlocfilehash: d7f9af94923f9160d18a9787b61036d5cf4104aede6488e2219b18a84325da46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684024"
---
# <a name="phytype-connectivity-element"></a>Элемент Фитипе (Connectivity)

Элемент Фитипе (подключение) указывает стандарт беспроводной локальной сети 802,11, используемый в беспроводной локальной сети.

Можно указать несколько **фитипе** s. Если **фитипе** не указан, профиль можно использовать для подключения к любому **фитипе**. значение n поддерживается только в Windows Vista с пакетом обновления 1 (SP1) и более поздними версиями операционной системы.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**установлен**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**подключение (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




