---
description: Определяет поставщик и предоставляемые им счетчики.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: Сложный тип поставщика
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909715"
---
# <a name="provider-complex-type"></a>Сложный тип поставщика

Определяет поставщик и предоставляемые им счетчики.

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент        | Тип                                                                   | Описание                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **counterSet** | [**Man: CounterSet**](performance-counters-counterset-complex-type.md) | Определяет набор счетчиков, который содержит один или несколько логически связанных счетчиков.<br/> |



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
<td>аппликатионидентити</td>
<td><strong>xs:string</strong></td>
<td>Имя двоичного файла, содержащего локализованные строки ресурсов: exe или DLL (не включайте в двоичный файл путь к файлу).<br/> Служебная программа Lodctr.exe использует путь из необязательного параметра [<em>path</em>] для поиска двоичного файла. Например, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>путь</em>]]. Если параметр [<em>path</em>] не включен, Lodctr.exe выполняет поиск в папке, содержащей манифест.<br/></td>
</tr>
<tr class="even">
<td>обратный вызов</td>

<td>Этот атрибут указывает, что вы хотите получить уведомление, когда потребитель выполняет определенные действия. <br/> Если включить этот атрибут, средство КТРПП использует альтернативную сигнатуру <a href="counterinitialize.md"><strong>каунтеринитиализе</strong></a> Function, которая используется для передачи имени функции, реализующей функцию обратного вызова <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>контролкаллбакк</strong></a> .<br/> В качестве альтернативы указанию этого атрибута можно использовать аргумент <strong>-нотификатионкаллбакк</strong><a href="ctrpp.md">КТРПП</a> .<br/> <strong>Windows Vista:</strong> Единственным допустимым значением для этого атрибута является &quot; Custom &quot; . Служебная программа <a href="ctrpp.md">КТРПП</a> создает шаблон для функции обратного вызова <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>контролкаллбакк</strong></a> . Шаблон включается в файл c, созданный КТРПП. <br/> <br/></td>
</tr>
<tr class="odd">
<td>провидергуид</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>мужчина: Гуидтипе</strong></a></td>
<td>Строковый идентификатор GUID, однозначно определяющий поставщика в манифесте. Идентификатор GUID должен быть уникальным в пределах манифеста.<br/> Новый GUID необходимо указывать только при изменении версии приложения (если поддерживаются параллельные установки).<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>Имя, используемое для создания имени класса Win32_PerfRawData WMI. Если имя не указано, &quot; счетчики &quot; будут использоваться в качестве имени класса.<br/></td>
</tr>
<tr class="odd">
<td>providerType</td>

<td>Определяет, является ли поставщик поставщиком пользовательского режима, поставщиком режима ядра или поставщиком драйвера. Возможны следующие значения.<br/> 
<table>
<thead>
<tr class="header">
<th>Термин</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>Пользовательском<br/></td>
<td>Укажите этот режим для компонента пользовательского режима, такого как приложение, Библиотека DLL или драйвер пользовательского режима. Типичными расширениями для компонентов пользовательского режима являются exe-или DLL-файлы. Это значение по умолчанию.<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>версиями<br/></td>
<td>Укажите этот режим для компонента режима ядра, такого как драйвер WDM или ВДФ. Стандартным расширением для компонентов режима ядра является. sys.<br/> <strong>Windows Vista и Windows Server 2008:</strong> Это значение не поддерживается до Windows 7 и Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>ресаурцебасе</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></td>
<td><p>Определяет начальное значение индекса ресурса, которое <a href="ctrpp.md">КТРПП</a> использует для создания идентификаторов ресурсов.</p></td>
</tr>
<tr class="odd">
<td>символ</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>мужчина: Ксимболтипе</strong></a></td>
<td><p>Символьное имя, идентифицирующее поставщик. Средство <a href="ctrpp.md">КТРПП</a> создает переменную Handle, которую можно использовать при вызове функций, которым требуется маркер поставщика (например, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>перфсетулонгкаунтервалуе</strong></a>). Символическое имя — это имя переменной.</p>
<p>При включении аргумента <strong>-prefix</strong> при вызове <a href="ctrpp.md">КТРПП</a>Строка префикса добавляется в начало символьного имени.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




