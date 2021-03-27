---
description: <property>Элемент указывает свойство, используемое библиотекой. Эти свойства относятся к библиотеке, поэтому нет предопределенного набора имен свойств для использования. Этот элемент является необязательным и не имеет дочерних элементов.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Элемент Property (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997250"
---
# <a name="property-element-library-schema"></a>Элемент Property (схема библиотеки)

<property>Элемент указывает свойство, используемое библиотекой. Эти свойства относятся к библиотеке, поэтому нет предопределенного набора имен свойств для использования. Этот элемент является необязательным и не имеет дочерних элементов.

## <a name="syntax"></a>Синтаксис

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                             | Дочерние элементы |
|----------------------------------------------------------------------------|----------------|
| [Элемент Пропертисторе (схема библиотеки)](schema-library-propertystore.md) | Нет           |



 

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

</tr>
<tr class="even">
<td>type</td>
<td>Общедоступный. Обязательный. Тип свойства.</td>
<td><ul>
<li>Any: по умолчанию. Значение не будет приведено подсистемой свойств. VT_NULL будет возвращено функцией Жетпропертитипе.</li>
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
<li>UInt64: значение должно быть VT_UI8.</li>
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



 

## <a name="remarks"></a>Примечания

Требования к элементу <канонического имени> соответствуют требованиям для поиска Windows и системы свойств Windows. Строка должна иметь тип канонического типа.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схемы свойств](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[Схема описания соединителя поиска](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
