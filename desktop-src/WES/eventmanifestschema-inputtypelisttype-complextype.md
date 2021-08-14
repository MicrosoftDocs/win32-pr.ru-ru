---
title: Сложный тип Инпуттипелисттипе
description: Определяет список входных типов.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Журнал событий сложных типов Инпуттипелисттипе
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 156ee19a90cdbb64e742d9876a39741155a3d5172f8da05f38f666cc077fc47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343745"
---
# <a name="inputtypelisttype-complex-type"></a>Сложный тип Инпуттипелисттипе

Определяет список входных типов.

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                | Тип                                                           | Описание                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [**Тип**](eventmanifestschema-intype-inputtypelisttype-element.md) | [**InputType**](eventmanifestschema-inputtype-complextype.md) | Определяет тип входных данных.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





