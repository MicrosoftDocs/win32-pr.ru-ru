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
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682010"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





