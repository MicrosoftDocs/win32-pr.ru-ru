---
title: Сложный тип Аттачментстипе
description: Определяет элементы, используемые для указания вложений, отправляемых с сообщением электронной почты.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- планировщик задач сложного типа Аттачментстипе
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d98b266fcb15fbd47fbb2a5bb792b95e4fb765a48b2fbcf6c1185aad9475df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772394"
---
# <a name="attachmentstype-complex-type"></a>Сложный тип Аттачментстипе

Определяет элементы, используемые для указания вложений, отправляемых с сообщением электронной почты.

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                          | Тип                                                                    | Описание                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Файл**](taskschedulerschema-file-attachmentstype-element.md) | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md) | Указывает путь к файлу, который отправляется в виде вложения в сообщение электронной почты.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





