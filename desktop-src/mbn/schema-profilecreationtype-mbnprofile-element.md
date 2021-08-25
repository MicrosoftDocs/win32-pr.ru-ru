---
description: Содержит сведения об авторе профиля.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Профилекреатионтипе (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: ddf3e70607cedbaed45da19651ec73736a54bfafab197e95d2cd634d8e3833f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959844"
---
# <a name="profilecreationtype-mbnprofile-element"></a>Профилекреатионтипе (Мбнпрофиле), элемент

Элемент **профилекреатионтипе (мбнпрофиле)** содержит сведения об авторе профиля.

Этот элемент может иметь одно из следующих значений.



| Значение                 | Значение                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "Усерпровисионед"     | Этот профиль создается сведениями, предоставленными пользователем устройства.                                                     |
| "Админпровисионед"    | Этот профиль создается ИТ-администраторами и распространяется на пользователей.                                                     |
| "Операторпровисионед" | Этот профиль создается сетевым оператором и распределяется между пользователями.                                                    |
| "Девицепровисионед"   | Этот профиль создается службой мобильной широкополосной связи с использованием сведений, хранящихся в подготовленном для устройства контексте. |



 

Это необязательный элемент.

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **профилекреатионтипе** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




