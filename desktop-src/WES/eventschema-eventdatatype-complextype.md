---
title: Сложный тип Евентдататипе
description: Определяет элементы данных событий и структуры, содержащие данные события.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- Журнал событий сложных типов Евентдататипе
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 424f7f5f6472859a06605467c427fc7b9f210a960f0920fb8593778bd757fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589027"
---
# <a name="eventdatatype-complex-type"></a>Сложный тип Евентдататипе

Определяет элементы данных событий и структуры, содержащие данные события.

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                              | Тип                                                               | Описание                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Двоичный**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | Двоичный BLOB-объект данных для событий, записываемых с помощью [ведения журнала событий](/windows/desktop/EventLog/event-logging).<br/> |
| [**комплексдата**](eventschema-complexdata-eventdatatype-element.md) | [**комплексдататипе**](eventschema-complexdatatype-complextype.md) | Структура, определенная в шаблоне для события.<br/>                                |
| [**Данные**](eventschema-data-eventdatatype-element.md)               | [**Заданий**](eventschema-datafieldtype-complextype.md)          | Элемент данных верхнего уровня, определенный в шаблоне для события.<br/>                      |



## <a name="attributes"></a>Атрибуты



| Имя | Тип   | Описание                                                       |
|------|--------|-------------------------------------------------------------------|
| Название | строка | Имя шаблона, содержащего элементы данных.<br/> |



## <a name="remarks"></a>Remarks

Функция [**евтрендер**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) отображает массивы и структуры как двоичные BLOB-объекты.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

