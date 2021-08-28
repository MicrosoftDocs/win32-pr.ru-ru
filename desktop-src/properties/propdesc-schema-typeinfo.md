---
description: Указывает сведения о типе свойства.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a70c6eeaee63bcb99ee19217ccff5d3ff7086a2
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632172"
---
# <a name="typeinfo"></a>typeInfo

Указывает сведения о типе свойства. Для каждого [пропертидескриптион](./propdesc-schema-propertydescription.md)должен быть только один элемент [typeInfo]() . этот элемент был изменен для Windows 7.

При наличии нескольких элементов используется последний из них. Если элемент [typeInfo]() не предоставлен, к описанию свойства применяются параметры атрибута по умолчанию.

## <a name="syntax-for-windows-7"></a>синтаксис для Windows 7


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                   | Дочерние элементы |
|------------------------------------------------------------------|----------------|
| [пропертидескриптион](./propdesc-schema-propertydescription.md) | None           |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>type</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; ANY &quot; . Указывает тип свойства. Ниже приведены допустимые типы и связанные с ними типы Variant, полученные с помощью <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>ипропертидескриптион:: жетпропертитипе</strong></a>. 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Любой</td>
<td>По умолчанию. Подсистема свойств не будет применять или приводить значение свойства. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>Ипропертидескриптион:: жетпропертитипе</strong></a> Возвращает VT_NULL. Независимые поставщики программного обеспечения настоятельно рекомендуется предоставлять тип, а не возвращаться к этому по умолчанию.</td>
</tr>
<tr class="even">
<td>NULL</td>
<td>Для этого свойства значение отсутствует. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>Ипропертидескриптион:: жетпропертитипе</strong></a> Возвращает VT_NULL.</td>
</tr>
<tr class="odd">
<td>Строка</td>
<td>Значение должно быть VT_LPWSTR, которое представляет собой строку в Юникоде, заканчивающуюся пустой ссылкой.</td>
</tr>
<tr class="even">
<td>Логический</td>
<td>Значение должно быть значением VT_BOOL, которое является логическим.</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>Значение должно быть VT_UI1, которое представляет собой байт.</td>
</tr>
<tr class="even">
<td>Буфер</td>
<td>Значение должно быть VT_UI1ом | VT_VECTOR буфер байтов.</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>Значение должно быть VT_I2ом, представляющим 16-разрядное целое число.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>Значение должно быть значением VT_UI2, которое представляет собой 16-разрядное целое число без знака.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>Значение должно быть VT_I4, которое представляет собой 32-разрядное целое число.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>Значение должно быть VT_UI4, которое представляет собой 32-разрядное целое число без знака.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>Значение должно быть VT_I8, которое представляет собой 64-разрядное целое число.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>Значение должно быть VT_UI8, которое представляет собой 64-разрядное целое число без знака.</td>
</tr>
<tr class="odd">
<td>Double</td>
<td>Значение должно быть VT_R8, которое является типом Double.</td>
</tr>
<tr class="even">
<td>Дата и время</td>
<td>Значение должно быть VT_FILETIME, которое является значением <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>fileTime</strong></a>.</td>
</tr>
<tr class="odd">
<td>Guid</td>
<td>Значение должно быть VT_CLSID, которое является идентификатором класса (CLSID).</td>
</tr>
<tr class="even">
<td>BLOB-объект</td>
<td>Значение должно быть VT_BLOB, которое имеет длину в байтах с префиксом.</td>
</tr>
<tr class="odd">
<td>STREAM</td>
<td>Значение должно быть VT_STREAM, которое является объектом, реализующим <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</td>
</tr>
<tr class="even">
<td>Буфер обмена</td>
<td>Значение должно быть VT_CF, которое является форматом буфера обмена.</td>
</tr>
<tr class="odd">
<td>Объект</td>
<td>Значение должно быть VT_UNKNOWN, которое является объектом, реализующим <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>граупингранже</td>
<td>Необязательный элемент. Значение по умолчанию — &quot; Дискретный &quot; . Указывает, как свойство отображается, если представление сгруппировано по этому свойству. После установки эти значения извлекаются с помощью <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>ипропертидескриптион:: жетграупингранже</strong></a>. Ниже приведены допустимые типы.

<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Discrete</td>
<td>По умолчанию. Отображает отдельные значения.</td>
</tr>
<tr class="even">
<td>Буквенно-цифровой</td>
<td>Отображает статические буквенно-цифровые диапазоны значений.</td>
</tr>
<tr class="odd">
<td>Размер</td>
<td>Отображает диапазоны статических размеров для значений.</td>
</tr>
<tr class="even">
<td>Дата</td>
<td>Отображает группы "месяц/год". По умолчанию для свойств типа = &quot; DateTime &quot; .</td>
</tr>
<tr class="odd">
<td>тимерелативе</td>
<td>Отображает в группах, относительных по времени.</td>
</tr>
<tr class="even">
<td>Динамический</td>
<td>Отображает динамически созданные диапазоны для значений.</td>
</tr>
<tr class="odd">
<td>Процент</td>
<td>Отображает сегмент процентов.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>исиннате</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;false&quot;. Указывает, считается ли свойство присущей. Свойство присущей, которое либо вычисляется из содержимого файла, либо из других ресурсов или систем. Например, System. Size — это свойство присущей, предоставляемое файловой системой. изменение значения свойства в и само по себе не делает ничего. Другие примеры — System. Image. Dimensions и System.Docумент. PageCount, которые рассчитываются программами на основе содержимого файла, а не на основе изменяемого пользователем параметра. Установка Исиннате = &quot; true &quot; означает, что пользователь не может изменить это свойство непосредственно через элемент управления свойства. Это значение сопоставляется с флагом PDTF_ISINNATE, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</td>
</tr>
<tr class="even">
<td>канбепуржед</td>
<td><strong>Windows Vista с пакетом обновления 1 (SP1) и более поздними версиями</strong>. Общедоступный. Необязательный элемент. Если задано значение &quot; true &quot; , можно удалить свойство присущей. Свойства присущей, вычисляемые из других свойств, доступны только для чтения по определению. Значение по умолчанию для этого атрибута зависит от значения <em>исиннате</em> .

<table>
<thead>
<tr class="header">
<th>исиннате</th>
<th>Канбепуржед значение по умолчанию</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>true</td>
<td>false</td>
</tr>
<tr class="even">
<td>false</td>
<td>true</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Свойство, значение <em>исиннате</em> которого равно &quot; false &quot; (т. е. свойство доступно для чтения и записи), не может также задавать значение false для значения <em>канбепуржед</em> &quot; &quot; . Это ограничение применяется операционной системой.
</blockquote>
</div>
<div>
 
</div>
<p>хотя этот атрибут появился в Windows vista с пакетом обновления 1 (SP1), пропдеск-файл, включающий этот атрибут, совместим с Windows Vista до Windows Vista с пакетом обновления 1 (sp1). В этой ситуации атрибут <em>канбепуржед</em> просто игнорируется.</p></td>
</tr>
<tr class="odd">
<td>мултиплевалуес</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;false&quot;. Указывает, может ли это свойство иметь несколько значений. Это значение сопоставляется с флагом PDTF_MULTIPLEVALUES, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>. Это также влияет на то, имеет ли VT_VECTOR значение типа VARTYPE значения свойства.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;false&quot;. Указывает, является ли свойство заголовком группы. Заголовок группы строго используется в проплистс, не имеет значения, никогда не хранится в файле, а также должен иметь <typeInfo type=&quot;Null&quot;> . Некоторые элементы пользовательского интерфейса в системе используют проплистс для указания последовательности отображаемых свойств. эти проплистс могут содержать ссылки на заголовки групп (например, System. пропграуп. Camera), которые сообщают пользовательскому интерфейсу о необходимости запуска нового раздела группы (например, &quot; Camera Параметры &quot; ). В описании свойства с параметром &quot; IsTrue = true &quot; должно быть указано значение <labelInfo label=&quot;Some localized label&quot;> , иначе это не полезное свойство. Это значение сопоставляется с флагом PDTF_ISGROUP, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</td>
</tr>
<tr class="odd">
<td>aggregationType</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; Default &quot; . Задает способ отображения агрегатных свойств при выборе нескольких элементов. После установки эти значения извлекаются с помощью <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>ипропертидескриптион:: жетаггрегатионтипе</strong></a> в качестве <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>. Ниже приведены допустимые типы.

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
<td>По умолчанию. Отображает заполнитель с <strong>несколькими значениями</strong> в пользовательском интерфейсе. Это значение по умолчанию, если <em>тип</em> несовместим с указанным <em>aggregationType</em>.</td>
</tr>
<tr class="even">
<td>Первое</td>
<td>Отображает значение свойства первого элемента в выделенном фрагменте или коллекции.</td>
</tr>
<tr class="odd">
<td>SUM</td>
<td>Отображает сумму числовых значений. Полезно для таких свойств, как System. Media. Duration или System. size. Это значение несовместимо с нечисловыми типами.</td>
</tr>
<tr class="even">
<td>Средний</td>
<td>Отображает среднее арифметическое числовых значений. Полезно для таких свойств, как System. рейтингов. Это значение несовместимо с нечисловыми типами.</td>
</tr>
<tr class="odd">
<td>Диапазон дат</td>
<td>Отображает диапазон дат. Полезен для таких свойств, как System. photo. Датетакен. Это значение несовместимо с любым исключением, кроме Type = &quot; DateTime &quot; и является значением по умолчанию для свойств этого типа.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Отображает объединение всех значений в выделении или коллекции. Порядок отображения значений не определен. Это значение используется по умолчанию для свойств типа = &quot; String &quot; и мултиплевалуес = &quot; true &quot; .</td>
</tr>
<tr class="odd">
<td>Максимум</td>
<td>Отображает максимальное значение в коллекции. Полезен для таких свойств, как System. DateModified. Несовместимо с нечисловыми или типами, не являющимися датами.</td>
</tr>
<tr class="even">
<td>Минимальные</td>
<td>Отображает минимальное значение в коллекции. Несовместимо с нечисловыми или типами, не являющимися датами.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>истрипроперти</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>для просмотра</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;false&quot;. Указывает, должно ли это свойство быть видимым для пользователя. Например, в пользовательском интерфейсе выбора столбцов отображаются только те свойства, которые имеют значение «Viewed» = &quot; true &quot; . Исключением является Пользовательский интерфейс, управляемый проплист, который всегда будет отображать свойство. Если у вас есть свойство, предназначенное только для выбора данных между двумя объектами и не предназначенное для просмотра пользователем, этот атрибут должен иметь значение false. Это значение сопоставляется с флагом PDTF_ISVIEWABLE, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</td>
</tr>
<tr class="even">
<td>с подзапросом</td>
<td>Windows Только Vista. не поддерживается в Windows 7 и более поздних версиях. Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;false&quot;. Указывает, должно ли это свойство быть доступно в пользовательском интерфейсе конструктор запросов поиска. Свойство должно иметь значение "IsTrue" = &quot; true &quot; , прежде чем &quot; параметру IsTrue = true &quot; соблюдается. Это значение сопоставляется с флагом PDTF_ISQUERYABLE, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</td>
</tr>
<tr class="odd">
<td>сеарчраввалуе</td>
<td><strong>Windows 7 и более поздней версии.</strong> Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>инклудеинфуллтексткуери</td>
<td>Windows Только Vista. не поддерживается в Windows 7 и более поздних версиях. Общедоступный. Необязательный элемент. Значение по умолчанию — &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; String &quot; . Задает указание для пользовательского интерфейса конструктор запросов поиска, чтобы он мог определить список возможных операторов условия внутри предиката. Ниже приведены распознаваемые значения. 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Строка</td>
<td>По умолчанию. Будут использоваться следующие операторы: имеет значение &quot; &quot; , not,,,, &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; , &quot; начинается с, &quot; &quot; заканчивается на &quot; , &quot; Contains &quot; , &quot; не содержит &quot; , &quot; имеет значение Like &quot; .</td>
</tr>
<tr class="even">
<td>Число</td>
<td>Значение по умолчанию для числовых свойств. Следующие операторы будут использоваться: &quot; Equals, &quot; &quot; не равно &quot; , &quot; меньше &quot; , &quot; больше &quot; , &quot; меньше или равно &quot; , &quot; больше или равно &quot; .</td>
</tr>
<tr class="odd">
<td>Дата и время</td>
<td>По умолчанию для свойств типа = &quot; DateTime &quot; . Будут использоваться следующие операторы: имеет значение &quot; , а — &quot; &quot; нет &quot; , &quot; перед, &quot; &quot; а — до, а — после, &quot; &quot; &quot; &quot; а &quot; включается.</td>
</tr>
<tr class="even">
<td>Логический</td>
<td>По умолчанию для свойств типа = &quot; Boolean &quot; . То же, что и номер.</td>
</tr>
<tr class="odd">
<td>Размер</td>
<td>То же, что и номер.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>дефаултоператион</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию &quot; равно &quot; . Задает указание для средства поиска конструктор запросов, чтобы оно могла определить оператора по умолчанию. Возможны следующие значения:

<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Равно</td>
<td>По умолчанию. Обозначает эквивалент.</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>Указывает на неэквивалентность.</td>
</tr>
<tr class="odd">
<td>LessThan;</td>
<td>Указывает, что меньше.</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>По умолчанию для свойств исключением = &quot; size &quot; . Указывает, что больше.</td>
</tr>
<tr class="odd">
<td>Содержит</td>
<td>По умолчанию для свойств исключением = &quot; String &quot; . Указывает на включение.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
