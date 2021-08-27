---
description: Изображение
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Элемент Image (схема описания свойства)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39145ebf4db2bab4ffffeeec31db15e26a881a5bf63b752096a5732522ff8d9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011504"
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



 

 

 
