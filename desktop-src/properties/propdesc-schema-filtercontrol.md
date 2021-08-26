---
description: Указывает, какой элемент управления следует использовать в меню фильтра заголовка.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: филтерконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f002543b220347ba9aaba3659aa9a66f8aea7760b9d8a9177ef2980a823434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885964"
---
# <a name="filtercontrol"></a>филтерконтрол

Указывает, какой элемент управления следует использовать в меню фильтра заголовка. Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [филтерконтрол]() .

При наличии нескольких элементов используется последний из них. Если элемент [филтерконтрол]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.

## <a name="syntax"></a>Синтаксис


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                   | Дочерние элементы |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Нет           |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание</th>
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
<td>По умолчанию. Использует элемент управления по умолчанию, основанный на <typeInfo type=&quot;&quot;> атрибуте. По умолчанию используется тип &quot; DateTime &quot; , а элементом управления по умолчанию является &quot; Calendar &quot; . Любой другой тип приведет к отсутствию специального элемента управления фильтра.</td>
</tr>
<tr class="even">
<td>Календарь</td>
<td>Использует элемент управления Calendar.</td>
</tr>
<tr class="odd">
<td>Рейтинг</td>
<td>Использует элемент управления рейтингом «5 звезд».</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
