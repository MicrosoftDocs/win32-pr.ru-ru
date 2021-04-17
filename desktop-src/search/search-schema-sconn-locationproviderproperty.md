---
description: Необязательный <property> элемент указывает свойства, используемые поставщиком расположения.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Элемент Property элемента Локатионпровидер (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105703623"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>Элемент Property элемента Локатионпровидер (схема соединителя поиска)

Необязательный <property> элемент указывает свойства, используемые поставщиком расположения. Эти свойства относятся к этому поставщику расположения, поэтому нет предопределенного набора имен для использования. <property>Элемент имеет два атрибута, как описано в этом разделе.

## <a name="syntax"></a>Синтаксис


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><property> Сведения об элементе



| Родительский элемент                                                                                 | Дочерние элементы                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [Элемент Локатионпровидер (схема соединителя поиска)](search-schema-sconn-locationprovider.md) | , описанного в этом разделе. |



 


## <a name="property-attributes"></a><property> Атрибута



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Описание</th>
<th>Значения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name</td>
<td>Обязательный. Отображаемое имя свойства.</td>
<td> </td>
</tr>
<tr class="even">
<td>тип</td>
<td>Обязательный. Тип свойства.</td>
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
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Для поставщика OpenSearch используются следующие свойства:

-   Опенсеарчшортнаме: короткое имя службы поиска.
-   Опенсеарчкуеритемплате: шаблон, отформатированный согласно соглашению о шаблоне OpenSearch, для службы запросов
-   Максимумресулткаунт: (число) максимальное число результатов, возвращенных службой поиска
-   Линкисфилепас: (Boolean) Если значение true, поставщик пытается интерпретировать возвращенные элементы как файлы, используя их расширения для создания соответствующего Шеллитем в представлении. Если значение равно false, элементы обрабатываются как ярлыки URL-адресов.

 

 



