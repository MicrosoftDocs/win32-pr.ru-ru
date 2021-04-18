---
description: Необязательный <property> элемент указывает свойство, используемое соединителем поиска. Эти свойства относятся только к этому соединителю поиска, поэтому предопределенный набор имен для использования отсутствует. У этого элемента нет дочерних элементов.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Элемент Property элемента Пропертисторе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540626"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>Элемент Property элемента Пропертисторе (схема соединителя поиска)

Необязательный <property> элемент указывает свойство, используемое соединителем поиска. Эти свойства относятся только к этому соединителю поиска, поэтому предопределенный набор имен для использования отсутствует. У этого элемента нет дочерних элементов.

## <a name="syntax"></a>Синтаксис


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                           | Дочерние элементы |
|------------------------------------------------------------------------------------------|----------------|
| [Элемент Пропертисторе (схема соединителя поиска)](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание</th>
<th>Значения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name</td>
<td>Общедоступный. Обязательный. Отображаемое имя свойства.</td>
<td> </td>
</tr>
<tr class="even">
<td>тип</td>
<td>Общедоступный. Обязательный. Тип свойства.</td>
<td>Any: по умолчанию. Значение не будет приведено подсистемой свойств. VT_NULL будет возвращено функцией Жетпропертитипе.
<ul>
<li>NULL: значение для этого свойства отсутствует. VT_NULL будет возвращено функцией Жетпропертитипе.</li>
<li>Строка: значение должно быть VT_LPWSTR.</li>
<li>Boolean: значение должно быть VT_BOOL.</li>
<li>Byte: значение должно быть VT_UI1.</li>
<li>Buffer: значение должно быть VT_UI1ом | VT_VECTOR буфер байтов.</li>
<li>Int16: значение должно быть VT_I2.</li>
<li>UInt16: значение должно быть VT_UI2.</li>
<li>Int32: значение должно быть VT_I4.</li>
<li>UInt32: значение должно быть VT_UI4.</li>
<li>Int64: значение должно быть VT_I8.</li>
<li>UInt64: значение должно быть VT_UI8</li>
<li>Double: значение должно быть VT_R8.</li>
<li>DateTime: значение должно быть VT_FILETIME.</li>
<li>GUID: значение должно быть VT_CLSID.</li>
<li>BLOB-объект. значение должно быть VT_BLOB.</li>
<li>Объект: значение должно быть VT_UNKNOWN.</li>
<li>Stream: значение должно быть VT_STREAM.</li>
<li>Буфер обмена. значение должно быть VT_CF.</li>
</ul></td>
</tr>
<tr class="odd">
<td>schema</td>
<td>Общедоступный. Необязательный элемент. Схема, в которой определено свойство.</td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Соединители поиска OpenSearch могут использовать свойство Опенсеарчхтмлролловертемплате. Это свойство определяет шаблон, отформатированный согласно соглашению о шаблоне OpenSearch. Шаблон Опенсеарчхтмлролловертемплате используется, когда пользователь нажимает кнопку "Поиск на веб-сайте" на панели команд.

## <a name="example"></a>Пример

В следующем примере показан <propertyStore> элемент с двумя <property> элементами.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



