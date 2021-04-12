---
description: Определяет тип, содержащий допустимые значения для атрибута Type элемента Margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Простой тип Маргинтипетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272308"
---
# <a name="margintypetype-simple-type"></a>Простой тип Маргинтипетипе

Определяет тип, содержащий допустимые значения для атрибута **Type** [элемента Margin](margin-element.md).

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **маргинтипетипе** — это **строка** , которая ограничена следующим шаблоном:

-   `Left|Right`

## <a name="remarks"></a>Комментарии

Допустимые значения для атрибута **Type** [элемента Margin](margin-element.md) : Left и right.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                     |



 

 




