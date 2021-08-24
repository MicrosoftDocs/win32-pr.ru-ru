---
description: указывает, как настроить поисковую подсистему Windows в отношении заданного определения свойства.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: сеарчинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e279f6ffe8ce161c421bc7c3e8918f93a94b90cfa11f65989b0e5531c298374e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885944"
---
# <a name="searchinfo"></a>сеарчинфо

указывает, как настроить поисковую подсистему Windows в отношении заданного определения свойства. если элемент [сеарчинфо]() не предоставлен, свойство не включается в поисковую подсистему Windows. этот элемент был изменен для Windows 7.

## <a name="syntax-for-windows-7"></a>синтаксис для Windows 7


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a>синтаксис для Windows Vista


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
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
<td>ининвертединдекс</td>
<td>Общедоступный. Необязательный элемент. Указывает, должно ли значение свойства храниться в инвертированном индексе. Это позволяет конечным пользователям выполнять полнотекстовые запросы по значениям этого свойства. Значение по умолчанию — &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>Столбец</td>
<td>Общедоступный. Необязательный элемент. указывает, должно ли свойство храниться в базе данных поиска Windows как столбец, чтобы независимые поставщики программного обеспечения могли создавать запросы на основе предикатов (например, &quot; Select *, где &quot; System. Title &quot; = ' ккк ' &quot; ). Если создатель схемы хочет разрешить конечным пользователям (или разработчикам) создавать запросы на основе предикатов для свойств, необходимо задать для этого свойства значение &quot; true &quot; . Значение по умолчанию — &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>исколумнспарсе</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;true&quot;. Если свойство является многозначным, этот атрибут всегда имеет &quot; значение true &quot; .</td>
</tr>
<tr class="even">
<td>колумниндекстипе</td>
<td>Общедоступный. Необязательный элемент. чтобы оптимизировать сортировку и группирование, поисковая система Windows может создать вторичные индексы для свойств, имеющих &quot; значение istrue = true &quot; . этот атрибут полезен только в том случае, если ининвертединдекс имеет &quot; значение true &quot; в Windows Vista или когда &quot; istrue имеет значение true &quot; в Windows 7. Если свойство планируется часто сортировать для пользователей, необходимо указать этот атрибут. значение по умолчанию в Windows Vista — &quot; нотиндексед &quot; . значение по умолчанию в Windows 7 — &quot; ondemand &quot; . Допустимы следующие значения.
<ul>
<li><strong>Нотиндексед</strong>: никогда не создавайте индекс значения.</li>
<li>На <strong>диске</strong>: для этого свойства по умолчанию строится индекс значения.</li>
<li><strong>ондискалл</strong> (только Windows 7 и более поздние версии): создайте индекс значения по умолчанию для этого свойства и, если это свойство vector, а также индекс значения для всех сцепленных векторных значений.</li>
<li><strong>ондисквектор</strong> (только Windows 7 и более поздних версий): для сцепленных векторных значений по умолчанию создается индекс значения.</li>
<li><strong>ondemand</strong> (только Windows 7 и более поздние версии): только индексы значений сборки по запросу, то есть только при первом использовании для запроса.</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>Общедоступный. Необязательный элемент. максимальный размер (в байтах), допустимый для определенного свойства, хранящегося в базе данных поиска Windows. Значение по умолчанию:
<ul>
<li><strong>Windows Vista</strong>: 128 байт</li>
<li><strong>Windows 7 и более поздних версий</strong>: 512 байт</li>
</ul>
Обратите внимание, что этот максимальный размер измеряется в байтах, а не в символах. Максимальное количество символов зависит от их кодировки.<br/></td>
</tr>
<tr class="even">
<td>назначенные клавиши</td>
<td><strong>Windows 7 и более поздней версии.</strong> Общедоступный. Необязательный элемент. Список назначенных значений, которые можно использовать для ссылки на свойство в поисковых запросах. Список отделяется символом "|".</td>
</tr>
</tbody>
</table>



 

 

 
