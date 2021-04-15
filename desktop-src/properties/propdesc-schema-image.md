---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Элемент Image (схема описания свойства)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662768"
---
# <a name="image"></a>Изображение

Для каждого родительского элемента должен быть только один элемент [Image]() .

## <a name="syntax"></a>Синтаксис


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительские элементы                                                                  | Дочерние элементы |
|----------------------------------------------------------------------------------|----------------|
| [enum](./propdesc-schema-enum.md), [енумранже](./propdesc-schema-enumrange.md) | Нет           |



 

## <a name="attributes"></a>Атрибуты



| Атрибут | Описание       |
|-----------|-------------------|
| res       | Общедоступный. Обязательный. |



 

 

 
