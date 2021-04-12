---
description: Новые для Windows 7. Определяет свойство, связанное со свойством, определенным в файле описания свойства.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344802"
---
# <a name="relatedproperty"></a>relatedProperty

Новые для Windows 7. Определяет свойство, связанное со свойством, определенным в файле описания свойства. В [релатедпропертинфо](./propdesc-schema-relatedpropertyinfo.md) может быть столько элементов [relatedProperty]() , сколько необходимо.

## <a name="syntax"></a>Синтаксис


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                   | Дочерние элементы |
|------------------------------------------------------------------|----------------|
| [релатедпропертинфо](./propdesc-schema-relatedpropertyinfo.md) | Нет           |



 

## <a name="attributes"></a>Атрибуты



| Атрибут        | Описание                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Общедоступный. Обязательный. Каноническое имя связи свойств. |
| propertyName     | Общедоступный. Обязательный. Каноническое имя связанного свойства.      |



 

## <a name="remarks"></a>Комментарии

Этот элемент позволяет сопоставлять одно свойство с другим. Например, можно сопоставлять текст пользовательского свойства, fabrikam. СторажекапаЦити, с System. Capacity:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
