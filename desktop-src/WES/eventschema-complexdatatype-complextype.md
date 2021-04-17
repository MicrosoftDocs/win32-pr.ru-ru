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
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691898"
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
| [**Данные**](eventschema-data-complexdatatype-element.md) | [**DataType**](eventschema-datafieldtype-complextype.md) | Список элементов данных в структуре. Список элементов находится в том же порядке, что и определено в шаблоне.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя | Тип   | Описание                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Название | строка | Имя структуры. Это имя, указанное при определении структуры в шаблоне (см. сложный тип [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |



## <a name="remarks"></a>Комментарии

Функция [**евтрендер**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) визуализирует содержимое структуры как двоичный BLOB-объект. функция не отображает отдельные элементы данных структуры.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





