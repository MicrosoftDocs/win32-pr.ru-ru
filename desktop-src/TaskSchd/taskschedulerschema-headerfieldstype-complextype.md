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
ms.openlocfilehash: 1c05b0e739a7aa75fb8e628de45cd929dd8c0b1e696ecef751c0fc8f08d926f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356366"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





