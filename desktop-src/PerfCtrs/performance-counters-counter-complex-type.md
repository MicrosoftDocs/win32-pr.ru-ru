---
description: Определяет счетчик.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: Сложный тип счетчика
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d591d4c23b626eaf2e2bfb10b528ff7c054507df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663204"
---
# <a name="counter-complex-type"></a>Сложный тип счетчика

Определяет счетчик.

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент               | Тип                                                                                 | Описание                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **каунтераттрибутес** | [**мужчина: Каунтераттрибутес**](performance-counters-counterattributes-complex-type.md) | Перечисляет уникальные атрибуты, указывающие, как данные счетчика отображаются в приложении-потребителе.<br/> |



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
<td>статистическое выражение</td>

<td>Статистическая функция, применяемая, если атрибут <strong>Instances</strong> набора <a href="performance-counters-counterset-complex-type.md"><strong>счетчиков</strong></a> — Глобалаггрегате, мултиплеаггрегате или глобалаггрегатехистори. Ниже приведены возможные статистические функции, которые можно применять.<br/> <dl> <dt><span id="max"></span><span id="MAX"></span>максимальной</dt> <dd> Возвращается максимальное значение счетчика.<br/> </dd> <dt><span id="min"></span><span id="MIN"></span>минимум</dt> <dd> Возвращается минимальное значение счетчика.<br/> </dd> <dt><span id="avg"></span><span id="AVG"></span>обращения</dt> <dd> Возвращается среднее значение счетчика.<br/> </dd> <dt><span id="sum"></span><span id="SUM"></span>функции</dt> <dd> Возвращается сумма значений счетчика.<br/> </dd> <dt><span id="undefined"></span><span id="UNDEFINED"></span>определено</dt> <dd> Не вычислять этот счетчик.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>басеид</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></td>
<td>Идентификатор другого счетчика в том же наборе счетчиков, значение которого используется для вычисления значения этого счетчика. Базовый счетчик требуется для следующих типов счетчиков:<br/> <dl> <dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> <dd> Требуется базовый счетчик PERF_AVERAGE_BASE.<br/> </dd> <dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> <dd> Требуется базовый счетчик PERF_AVERAGE_BASE.<br/> </dd> <dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> <dd> Требуется базовый счетчик PERF_COUNTER_MULTI_BASE.<br/> </dd> <dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> <dd> Требуется базовый счетчик PERF_LARGE_RAW_BASE.<br/> </dd> <dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> <dd> Требуется базовый счетчик PERF_LARGE_RAW_BASE.<br/> </dd> <dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> <dd> Требуется базовый счетчик PERF_RAW_BASE.<br/> </dd> <dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> <dd> Требуется базовый счетчик PERF_SAMPLE_BASE.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td>дефаултскале</td>

<td>Коэффициент масштабирования, применяемый к значению счетчика (значение счетчика коэффициента *). Значение по умолчанию равно нулю, если масштабирование не применяется. Диапазон допустимых значений — от 10 до 10 (0,0000000001 до 1000000000). Если это значение равно нулю, значение масштаба равно 1; Если это значение равно 1, значение масштаба равно 10; Если это значение равно 1, масштаб имеет значение. 10; и т. д.<br/></td>
</tr>
<tr class="even">
<td>description;</td>
<td><strong>xs:string</strong></td>
<td>Краткое описание счетчика. Не нужно указывать этот атрибут, если счетчик содержит атрибут «не <a href="performance-counters-counterattribute-complex-type.md"><strong>Показывать</strong></a> ».<br/></td>
</tr>
<tr class="odd">
<td>detailLevel</td>

<td>Указывает целевую аудиторию для сведений о счетчике. Допустимы следующие значения:<br/> <dl> <dt><span id="standard"></span><span id="STANDARD"></span>Standard</dt> <dd> Отображение сведений о счетчике, который будет распознать обычный пользователь.<br/> </dd> <dt><span id="advanced"></span><span id="ADVANCED"></span>продвинут</dt> <dd> Отображение сведений о счетчике, который будет понятен только опытному пользователю.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>поле</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>мужчина: Ксимболтипе</strong></a></td>
<td>Имя поля в структуре, которое содержит значение счетчика. Этот атрибут не разрешен для поставщиков пользовательского режима.<br/></td>
</tr>
<tr class="odd">
<td>идентификатор</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></td>
<td>Уникальный номер, определяющий счетчик в наборе счетчиков.<br/></td>
</tr>
<tr class="even">
<td>мултикаунтерид</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></td>
<td>Идентификатор другого счетчика в том же наборе счетчиков, значение множителя которого используется для вычисления значения этого счетчика. Для следующих типов счетчиков требуется значение множителя. Указанный счетчик должен иметь тип PERF_COUNTER_RAWCOUNT.<br/>
<ul>
<li>PERF_COUNTER_MULTI_TIMER</li>
<li>PERF_COUNTER_MULTI_TIMER_INV</li>
<li>PERF_100NSEC_MULTI_TIMER</li>
<li>PERF_100NSEC_MULTI_TIMER_INV</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>

<td>Имя счетчика. Имя должно быть уникальным и содержать менее 1 024 символов. В нем учитывается регистр. Не нужно указывать этот атрибут, если счетчик содержит атрибут «не <a href="performance-counters-counterattribute-complex-type.md"><strong>Показывать</strong></a> ».<br/></td>
</tr>
<tr class="even">
<td>перффрекид</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></td>
<td>Идентификатор другого счетчика в том же наборе счетчиков, значение частоты которого используется для вычисления значения этого счетчика. Для следующих типов счетчиков требуется частота. Тип счетчика PERF_COUNTER_LARGE_RAWCOUNT содержит значение метки времени.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="odd">
<td>перфтимеид</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></td>
<td>Идентификатор другого счетчика в том же наборе счетчиков, значение метки времени которого используется для вычисления значения этого счетчика. Для следующих типов счетчиков требуется метка времени. Тип счетчика PERF_COUNTER_LARGE_RAWCOUNT содержит значение метки времени.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="even">
<td>struct</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>мужчина: Ксимболтипе</strong></a></td>
<td>Имя элемента структуры, который содержит значение этого счетчика. Этот атрибут не разрешен для поставщиков пользовательского режима.<br/></td>
</tr>
<tr class="odd">
<td>символ</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>мужчина: Ксимболтипе</strong></a></td>
<td>Символьное имя, идентифицирующее счетчик. Средство <a href="ctrpp.md">КТРПП</a> создает константу, которую можно использовать при вызове функций, для которых требуется идентификатор счетчика (например, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>перфинкрементулонгкаунтервалуе</strong></a>). Имя константы — это символьное имя.<br/></td>
</tr>
<tr class="even">
<td>тип</td>

<td>Имя типа счетчика. Возможные значения см. в приведенном выше блоке синтаксиса. Дополнительные сведения о каждом типе см. в разделе <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">типы счетчиков</a> в руководству по развертыванию Windows 2003. Имя чувствительно к регистру. Используйте нижний регистр. <br/></td>
</tr>
<tr class="odd">
<td>uri</td>
<td><strong>xs: anyURI</strong></td>
<td>Уникальный универсальный идентификатор ресурса, позволяющий пользователям получать значения счетчиков из любого расположения.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Для обеспечения обратной совместимости каждый счетчик в наборе счетчиков должен указывать одни и те же значения **перффрекид** и **перфтимеид** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

