---
title: Сложный тип Датадефинитионтипе
description: Определяет элемент данных, который необходимо включить в событие. | Сложный тип Датадефинитионтипе
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- Журнал событий сложных типов Датадефинитионтипе
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa492acf00740b0df9b761c40797ec05feb5b2e38b84ec0682296dd845cbe613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589609"
---
# <a name="datadefinitiontype-complex-type"></a>Сложный тип Датадефинитионтипе

Определяет элемент данных, который необходимо включить в событие.

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
             />
            <xs:attribute name="length"
                type="LengthType"
                use="optional"
             />
            <xs:attribute name="count"
                type="CountType"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Имя</th>
<th>Тип</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>count</td>
<td><a href="eventmanifestschema-counttype-simpletype.md"><strong>каунттипе</strong></a></td>
<td>Число элементов в массиве, если элемент данных является массивом. Можно указать фактическое число или имя другого элемента данных, содержащего число. <br/></td>
</tr>
<tr class="even">
<td>Тип</td>
<td><strong>QName</strong></td>
<td>Тип данных для этого элемента данных. Список предопределенных типов входных данных см. в разделе сложный тип <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>length</td>
<td><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>ленгстипе</strong></a></td>
<td>Длина элемента данных переменной длины, например двоичного объекта BLOB. Для двоичных данных укажите длину в байтах, а для строковых данных укажите длину в символах. Можно указать фактическую длину или имя другого элемента данных, который содержит длину.<br/> Если для указания строки фиксированной длины используется атрибут Length, необходимо заполнить строку фиксированной длиной, допуская символ-признак конца строки в конце (например, если длина равна 5, строка &quot; ABC &quot; должна быть дополнена значением &quot; ABC &quot; . Длина строки должна включать символ конца null.<br/></td>
</tr>
<tr class="even">
<td>карта</td>
<td>строка</td>
<td>Имя соответствия "имя-значение", используемое для отображения целочисленных значений в строках. Тип данных элемента данных должен быть одного из следующих типов:<br/>
<ul>
<li>win:UInt8</li>
<li>win:UInt16</li>
<li>win:UInt32</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>
<td>строка</td>
<td>Имя элемента данных. Имя можно использовать для ссылки на этот элемент данных в фрагменте XML, если в шаблоне указан раздел <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> . Вы также можете ссылаться на это имя в атрибуте length или Count другого элемента данных, если этот элемент данных содержит его длину или значение Count.<br/> <strong>Windows Vista:</strong> Этот атрибут является необязательным.<br/></td>
</tr>
<tr class="even">
<td>Тип</td>
<td><strong>QName</strong></td>
<td>Тип данных, используемый при отрисовке этого элемента данных. Список предопределенных типов выходных данных см. в описании сложного типа <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> .<br/> <strong>Windows Vista:</strong> Тип выходных данных игнорируется, и служба определяет тип на основе входного типа.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarks

Для входных типов переменной длины, таких как двоичные BLOB-объекты, необходимо использовать атрибут length для явного указания размера данных. Для строк укажите атрибут Length, только если строки имеют фиксированную длину.

## <a name="examples"></a>Примеры

Ниже приведено несколько примеров определений элементов данных.


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





