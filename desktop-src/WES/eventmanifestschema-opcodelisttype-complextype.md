---
title: Сложный тип Опкоделисттипе
description: Определяет список кодов операций, которые используются для определения операций компонента приложения.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- Журнал событий сложных типов Опкоделисттипе
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c44a2c2fa38957f302dfe3861a89f57dbe51d44ca737268a8988f8c138be8b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767304"
---
# <a name="opcodelisttype-complex-type"></a>Сложный тип Опкоделисттипе

Определяет список кодов операций, которые используются для определения операций компонента приложения.

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                             | Тип                                                             | Описание                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [**транслируют**](eventmanifestschema-opcode-opcodelisttype-element.md) | [**опкодетипе**](eventmanifestschema-opcodetype-complextype.md) | Определяет операцию в компоненте приложения.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





