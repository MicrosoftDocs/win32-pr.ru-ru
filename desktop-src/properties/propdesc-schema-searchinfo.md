---
description: указывает, как настроить поисковую подсистему Windows в отношении заданного определения свойства.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: сеарчинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcfc901dfb4610210c4990c962b5251710e5653
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465631"
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
| [пропертидескриптион](./propdesc-schema-propertydescription.md) | None           |



 

## <a name="attributes"></a>Атрибуты




| Атрибут | Описание | 
|-----------|-------------|
| ининвертединдекс | Общедоступный. Необязательный элемент. Указывает, должно ли значение свойства храниться в инвертированном индексе. Это позволяет конечным пользователям выполнять полнотекстовые запросы по значениям этого свойства. Значение по умолчанию — «false». | 
| Столбец | Общедоступный. Необязательный элемент. указывает, должно ли свойство храниться в базе данных поиска Windows как столбец, чтобы независимые поставщики программного обеспечения могли создавать запросы на основе предикатов (например, "Select * Where" System. Title "= ' ккк '"). Если создатель схемы хочет разрешить конечным пользователям (или разработчикам) создавать запросы на основе предикатов для свойств, необходимо задать для этого свойства значение "true". Значение по умолчанию — «false». | 
| исколумнспарсе | Общедоступный. Необязательный элемент. Значение по умолчанию - "true". Если свойство является многозначным, этот атрибут всегда имеет значение true. | 
| колумниндекстипе | Общедоступный. Необязательный элемент. чтобы оптимизировать сортировку и группирование, поисковая система Windows может создать вторичные индексы для свойств, у которых свойство column = "true". этот атрибут полезен только в том случае, если ининвертединдекс имеет значение true в Windows Vista или если в Windows 7 значение datacolumn равно true. Если свойство планируется часто сортировать для пользователей, необходимо указать этот атрибут. значение по умолчанию в Windows Vista — "нотиндексед". значение по умолчанию в Windows 7 — ondemand. Допустимы следующие значения.<ul><li><strong>Нотиндексед</strong>: никогда не создавайте индекс значения.</li><li>На <strong>диске</strong>: для этого свойства по умолчанию строится индекс значения.</li><li><strong>ондискалл</strong> (только Windows 7 и более поздние версии): создайте индекс значения по умолчанию для этого свойства и, если это свойство vector, а также индекс значения для всех сцепленных векторных значений.</li><li><strong>ондисквектор</strong> (только Windows 7 и более поздних версий): для сцепленных векторных значений по умолчанию создается индекс значения.</li><li><strong>ondemand</strong> (только Windows 7 и более поздние версии): только индексы значений сборки по запросу, то есть только при первом использовании для запроса.</li></ul> | 
| maxSize | Общедоступный. Необязательный элемент. максимальный размер (в байтах), допустимый для определенного свойства, хранящегося в базе данных поиска Windows. Значение по умолчанию:<ul><li><strong>Windows Vista</strong>: 128 байт</li><li><strong>Windows 7 и более поздних версий</strong>: 512 байт</li></ul>Обратите внимание, что этот максимальный размер измеряется в байтах, а не в символах. Максимальное количество символов зависит от их кодировки.<br /> | 
| назначенные клавиши | <strong>Windows 7 и более поздней версии.</strong> Общедоступный. Необязательный элемент. Список назначенных значений, которые можно использовать для ссылки на свойство в поисковых запросах. Список отделяется символом "|символов. | 




 

 

 
