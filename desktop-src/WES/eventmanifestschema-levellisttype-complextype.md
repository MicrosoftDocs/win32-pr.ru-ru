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
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493089"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





