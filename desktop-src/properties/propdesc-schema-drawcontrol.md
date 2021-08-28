---
description: Указывает, какой элемент управления следует использовать при простом отображении свойства.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: дравконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a330854f19005f7f2863c337451b1dcc56cea3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632052"
---
# <a name="drawcontrol"></a>дравконтрол

Указывает, какой элемент управления следует использовать при простом отображении свойства. Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [дравконтрол]() .

При наличии нескольких элементов используется последний из них. Если элемент [дравконтрол]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.

Эта форма элемента управления не позволяет изменять свойства.

## <a name="syntax"></a>Синтаксис


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                   | Дочерние элементы |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | None           |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>управляющие</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; Default &quot; . Допустимы следующие значения. 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>По умолчанию</td>
<td>По умолчанию. Использует элемент управления по умолчанию, основанный на <typeInfo type=&quot;&quot;> атрибуте. Тип по умолчанию — &quot; String &quot; (многозначный), а элемент управления по умолчанию — &quot; мултивалуетекст &quot; . Любой другой тип приводит к использованию &quot; &quot; элемента управления статиктекст.</td>
</tr>
<tr class="even">
<td>мултилинетекст</td>
<td>Использует многострочный элемент управления Text.</td>
</tr>
<tr class="odd">
<td>мултивалуетекст</td>
<td>Использует многозначный элемент управления Text.</td>
</tr>
<tr class="even">
<td>перцентбар</td>
<td>Использует элемент управления "процентная черта".</td>
</tr>
<tr class="odd">
<td>ProgressBar</td>
<td>Использует элемент управления "индикатор выполнения".</td>
</tr>
<tr class="even">
<td>Рейтинг</td>
<td>Использует элемент управления рейтингом «5 звезд».</td>
</tr>
<tr class="odd">
<td>статиктекст</td>
<td>Использует <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>ипропертидескриптион:: форматфордисплай</strong></a> для вывода значения свойства.</td>
</tr>
<tr class="even">
<td>иконлист</td>
<td><strong>Windows 7 и более поздней версии.</strong> Перечисление значков.</td>
</tr>
<tr class="odd">
<td>булеанчеккмарк</td>
<td><strong>Windows 7 и более поздней версии.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
