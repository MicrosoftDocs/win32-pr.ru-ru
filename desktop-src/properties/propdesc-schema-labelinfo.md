---
description: Указывает способ отображения меток свойства.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: лабелинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662767"
---
# <a name="labelinfo"></a>лабелинфо

Указывает способ отображения меток свойства. Для каждого элемента [пропертидескриптион](./propdesc-schema-propertydescription.md) должен быть только один элемент [лабелинфо]() .

При наличии нескольких элементов используется последний из них. Если элемент [лабелинфо]() не указан, метка свойства не отображается; Однако это обычно является дефектом.

## <a name="syntax"></a>Синтаксис


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                   | Дочерние элементы |
|------------------------------------------------------------------|----------------|
| [пропертидескриптион](./propdesc-schema-propertydescription.md) | Нет           |



 

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
<td>метка</td>
<td>Общедоступный. Необязательный элемент. Метка, отображаемая в пользовательском интерфейсе (например, метка столбца сведений или панель предварительного просмотра). Синтаксис позволяет получить прямую отображаемую строку или ссылку на непрямо отображаемую строку. Используйте строку с косвенным отображением, так как она может быть локализована. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>Ипропертидескриптион::</strong></a> Возвращает разрешенное отображаемое имя.</td>
</tr>
<tr class="even">
<td>сортдескриптион</td>
<td>Необязательный элемент. Указывает строки, предлагаемые в качестве параметров сортировки. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>Ипропертидескриптион:: жетсортдескриптион</strong></a> возвращает это описание сортировки. Следующие значения предоставляют соответствующие строки пользовательского интерфейса.
<ul>
<li>Общие: Сортировка по мере &quot; &quot;  /  &quot; уменьшения&quot;</li>
<li>Атоз: по &quot; верхнему &quot;  /  &quot; Z-поверх&quot;</li>
<li>Ловессигхест: &quot; самый низкий на &quot; высшем верху  /  &quot;&quot;</li>
<li>Олдестневест: &quot; самые старые самые &quot;  /  &quot; новые в начале&quot;</li>
<li>Смаллестларжест: &quot; самый маленький на самый &quot;  /  &quot; крупный сверху&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>инвитатионтекст</td>
<td>Необязательный элемент. Текст строки справки, отображаемый в качестве инструкции пользователю для элемента управления или подсказки (например, &quot; введите имя автора &quot; ). Синтаксис позволяет получить прямую отображаемую строку или ссылку на непрямо отображаемую строку. Используйте строку с косвенным отображением, так как она может быть локализована. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>Ипропертидескриптион:: жетедитинвитатион</strong></a> возвращает Разрешенный текст приглашения.</td>
</tr>
<tr class="even">
<td>хиделабел</td>
<td>Необязательный элемент. Значение по умолчанию — &quot;false&quot;. Указывает, скрыта ли метка.</td>
</tr>
</tbody>
</table>



 

 

 
