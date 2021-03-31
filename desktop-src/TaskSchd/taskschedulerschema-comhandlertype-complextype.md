---
title: Сложный тип Комхандлертипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Комхандлер.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- планировщик задач сложного типа Комхандлертипе
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071412"
---
# <a name="comhandlertype-complex-type"></a>Сложный тип Комхандлертипе

Определяет дочерние элементы и сведения о последовательности для элемента [**комхандлер**](taskschedulerschema-comhandler-actiongroup-element.md) .

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Тип                                                         | Описание                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [**Класса**](taskschedulerschema-classid-comhandlertype-element.md) | [**гуидтипе**](taskschedulerschema-guidtype-simpletype.md)  | Задает идентификатор класса обработчика.<br/>          |
| [**Data**](taskschedulerschema-data-comhandlertype-element.md)       | [**Заданий**](taskschedulerschema-datatype-complextype.md) | Указывает дополнительные данные, связанные с обработчиком. <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





