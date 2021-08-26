---
description: Определяет тип, определяющий допустимые значения для атрибута Type \[ средства чтения журнала элемента содержимого \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Простой тип Контенттипетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 83b49427e65bb5190554a0c995bec119de1230f0baab869ea4c5ce48dc5616f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008974"
---
# <a name="contenttypetype-simple-type"></a>Простой тип Контенттипетипе

Определяет тип, определяющий допустимые значения для атрибута *Type* [ \[ средства \] чтения журнала элемента содержимого](content-element--journal-reader.md).

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **контенттипетипе** — это строка, которая ограничена следующим шаблоном:

-   `Normal|Inert`

## <a name="remarks"></a>Remarks

Допустимые значения: "нормальный" и "инерт".

Если тип — «инерт», то содержимое, содержащееся в журнале, является страницей журнала, которая является фоном документа доступным только для чтения и не является редактируемым. Это происходит при создании документа с помощью драйвера принтера составителя заметок журнала.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                     |



 

 




