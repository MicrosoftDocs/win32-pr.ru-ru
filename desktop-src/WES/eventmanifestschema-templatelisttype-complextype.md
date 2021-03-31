---
title: Сложный тип Темплателисттипе
description: Определяет список шаблонов, указывающих данные, включаемые в события. | Сложный тип Темплателисттипе
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- Журнал событий сложных типов Темплателисттипе
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820725"
---
# <a name="templatelisttype-complex-type"></a>Сложный тип Темплателисттипе

Определяет список шаблонов, указывающих данные, включаемые в события.

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                   | Тип                                                                         | Описание                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**шаблон**](eventmanifestschema-template-templatelisttype-element.md) | [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md) | Шаблон, определяющий данные, включаемые в событие.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





