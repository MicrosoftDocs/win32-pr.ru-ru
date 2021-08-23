---
title: Сложный тип Комплексдататипе
description: Определяет структуру, содержащую один или несколько элементов данных.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- Журнал событий сложных типов Комплексдататипе
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f86b15defc32469dd1a4abd0f6366e1a93d4b83441b1e1518ff7ac999f30bd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055812"
---
# <a name="complexdatatype-complex-type"></a>Сложный тип Комплексдататипе

Определяет структуру, содержащую один или несколько элементов данных.

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                  | Тип                                                      | Описание                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Данные**](eventschema-data-complexdatatype-element.md) | [**Заданий**](eventschema-datafieldtype-complextype.md) | Список элементов данных в структуре. Список элементов находится в том же порядке, что и определено в шаблоне.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя | Тип   | Описание                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Название | строка | Имя структуры. Это имя, указанное при определении структуры в шаблоне (см. сложный тип [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |



## <a name="remarks"></a>Remarks

Функция [**евтрендер**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) визуализирует содержимое структуры как двоичный BLOB-объект. функция не отображает отдельные элементы данных структуры.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





