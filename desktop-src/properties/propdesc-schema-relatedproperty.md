---
description: новое для Windows 7. Определяет свойство, связанное со свойством, определенным в файле описания свойства.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285c0f8b0731ba790cd57105f907cd4df85b6faa41c3f649588aca7ef457418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938684"
---
# <a name="relatedproperty"></a>relatedProperty

новое для Windows 7. Определяет свойство, связанное со свойством, определенным в файле описания свойства. В [релатедпропертинфо](./propdesc-schema-relatedpropertyinfo.md) может быть столько элементов [relatedProperty]() , сколько необходимо.

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



 

## <a name="remarks"></a>Remarks

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



 

 
