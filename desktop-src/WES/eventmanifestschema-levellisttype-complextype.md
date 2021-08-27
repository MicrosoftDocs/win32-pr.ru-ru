---
title: Сложный тип Левеллисттипе
description: Определяет список уровней серьезности, определяющих уровень детализации события.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- Журнал событий сложных типов Левеллисттипе
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8087913cacac67f0c7487b5eb41f404ebdc205765c693bdfda9f86995a809493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124304"
---
# <a name="levellisttype-complex-type"></a>Сложный тип Левеллисттипе

Определяет список уровней серьезности, определяющих уровень детализации события.

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                          | Тип                                                           | Описание                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**уровню**](eventmanifestschema-level-levellisttype-element.md) | [**LevelType**](eventmanifestschema-leveltype-complextype.md) | Определяет значение серьезности, определяющее уровень детализации событий во время ведения журнала.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





