---
title: Сложный тип Хеадерфиелдстипе
description: Определяет элементы, указывающие поля для заголовка электронной почты.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- планировщик задач сложного типа Хеадерфиелдстипе
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489855"
---
# <a name="headerfieldstype-complex-type"></a>Сложный тип Хеадерфиелдстипе

Определяет элементы, указывающие поля для заголовка электронной почты.

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                         | Тип                                                                       | Описание                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [**хеадерфиелд**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**хеадерфиелдтипе**](taskschedulerschema-headerfieldtype-complextype.md) | Задает поле в заголовке сообщения электронной почты. <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





