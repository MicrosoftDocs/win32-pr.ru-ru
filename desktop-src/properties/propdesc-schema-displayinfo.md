---
description: Задает отображаемые сведения о свойстве.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0bbc3cf0f17d24672e30a110d95341c1cb902d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622090"
---
# <a name="displayinfo"></a>displayInfo

Задает отображаемые сведения о свойстве. Для каждого [пропертидескриптион](./propdesc-schema-propertydescription.md)должен быть только один элемент [displayInfo]() .

При наличии нескольких элементов используется последний из них. Если элемент [displayInfo]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.

## <a name="syntax"></a>Синтаксис


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="FileName"/>
                                <xs:enumeration value="FilePath"/>
                                <xs:enumeration value="Hyperlink"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="YesNo"/>
                                <xs:enumeration value="OnOff"/>
                                <xs:enumeration value="TrueFalse"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="Percentage"/>
                                <xs:enumeration value="ByteSize"/>
                                <xs:enumeration value="KBSize"/>
                                <xs:enumeration value="SampleSize"/>
                                <xs:enumeration value="Bitrate"/>
                                <xs:enumeration value="SampleRate"/>
                                <xs:enumeration value="FrameRate"/>
                                <xs:enumeration value="Pixels"/>
                                <xs:enumeration value="DPI"/>
                                <xs:enumeration value="Duration"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatDurationAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="Month"/>
                                <xs:enumeration value="YearMonth"/>
                                <xs:enumeration value="Year"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatTimeAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="ShortTime"/>
                                <xs:enumeration value="LongTime"/>
                                <xs:enumeration value="HideTime"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatDateAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="ShortDate"/>
                                <xs:enumeration value="LongDate"/>
                                <xs:enumeration value="HideDate"/>
                                <xs:enumeration value="RelativeShortDate"/>
                                <xs:enumeration value="RelativeLongDate"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="value" type="xs:string" use="required"/>
                                <xs:attribute name="text" type="xs:string" use="required"/>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="PercentBar"/>
                                <xs:enumeration value="ProgressBar"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="StaticText"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Boolean"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="NumericText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                   | Дочерние элементы                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [пропертидескриптион](./propdesc-schema-propertydescription.md) | [stringFormat](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [булеанформат](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [numberFormat](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [dateTimeFormat](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [енумератедлист](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [дравконтрол](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [едитконтрол](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [филтерконтрол](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | [куериконтрол](./propdesc-schema-querycontrol.md) (только Windows Vista. не поддерживается в Windows 7 и более поздних версиях.) |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>дефаултколумнвидс</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; 20 &quot; .</td>
</tr>
<tr class="even">
<td>дисплайтипе</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; String &quot; . Указывает тип отображаемой строки. После установки здесь значения связанных <strong>PROPDESC_DISPLAYTYPE</strong> извлекаются с помощью <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>Ипропертидескриптион:: жетдисплайтипе</strong></a>. Ниже приведены допустимые типы. 
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
<td>По умолчанию. Значение отображается в виде строки. Используйте &quot; StringFormat &quot; для форматирования. Метод возвращает PDDT_STRING.</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Значение по умолчанию для числовых свойств. Значение отображается как число. Используйте &quot; NumberFormat &quot; для форматирования. Метод возвращает PDDT_NUMBER.</td>
</tr>
<tr class="odd">
<td>Логический</td>
<td>Значение по умолчанию <typeInfo type=&quot;Boolean&quot;> , если. Значение отображается в виде логического значения. Используйте &quot; булеанформат &quot; для форматирования. Метод возвращает PDDT_BOOLEAN.</td>
</tr>
<tr class="even">
<td>Дата и время</td>
<td>Значение по умолчанию <typeInfo type=&quot;DateTime&quot;> , если. Значение отображается как дата или время. Используйте &quot; DateTimeFormat &quot; для форматирования. Метод возвращает PDDT_DATETIME.</td>
</tr>
<tr class="odd">
<td>Перечисление</td>
<td>Значение отображается как сопоставление отображаемой строки, предоставленное &quot; элементом енумератедлист &quot; . Метод возвращает PDDT_ENUMERATED.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>выравнивание</td>
<td>Необязательный элемент. По умолчанию — &quot; Left &quot; . 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Левый</td>
<td>По умолчанию. По левому краю.</td>
</tr>
<tr class="even">
<td>Center</td>
<td>Выровнять по центру.</td>
</tr>
<tr class="odd">
<td>Правый</td>
<td>По правому краю.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>релативедескриптионтипе</td>
<td>Необязательный элемент. Значение по умолчанию — &quot; General &quot; . Указывает, как должны описываться два значения этого свойства при их сравнении друг с другом. В случае эквивалентности &quot; &quot; всегда используется. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>Ипропертидескриптион:: жетрелативедескриптион</strong></a> и <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>Ипропертидескриптион:: жетрелативедескриптионтипе</strong></a> используют это значение для определения отображаемых имен относительных описаний. 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Общие сведения</td>
<td>По умолчанию. Использует &quot; разные &quot;  /  &quot; &quot;  /  &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Дата</td>
<td>Значение по умолчанию <typeInfo type=&quot;DateTime&quot;> , если. Используется раньше или более ранней версии или более ранних, &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; &quot; чем &quot;  /  &quot; &quot;  /  &quot; &quot; &quot; раньше &quot;  /  &quot; &quot;  /  &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>Размер</td>
<td>Использует &quot; меньшее &quot;  /  &quot; &quot;  /  &quot; увеличение&quot;</td>
</tr>
<tr class="even">
<td>Count</td>
<td>Использует &quot; меньшее &quot;  /  &quot; &quot;  /  &quot; увеличение&quot;</td>
</tr>
<tr class="odd">
<td>Редакция</td>
<td>Используется &quot; ранее &quot;  /  &quot; &quot;  /  &quot;&quot;</td>
</tr>
<tr class="even">
<td>Длина</td>
<td>Использует &quot; более короткий интервал &quot;  /  &quot; &quot;  /  &quot; времени&quot;</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Использует &quot; более короткий интервал &quot;  /  &quot; &quot;  /  &quot; времени&quot;</td>
</tr>
<tr class="even">
<td>Speed</td>
<td>Использует &quot; меньшее быстродействие &quot;  /  &quot; &quot;  /  &quot;&quot;</td>
</tr>
<tr class="odd">
<td>Тариф</td>
<td>Использует &quot; меньшее быстродействие &quot;  /  &quot; &quot;  /  &quot;&quot;</td>
</tr>
<tr class="even">
<td>Рейтинг</td>
<td>Использует &quot; меньшее &quot;  /  &quot; самое &quot;  /  &quot; высокое&quot;</td>
</tr>
<tr class="odd">
<td>Приоритет</td>
<td>Использует &quot; меньшее &quot;  /  &quot; самое &quot;  /  &quot; высокое&quot;</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>дефаултсортдиректион</td>
<td>Задает направление сортировки. По умолчанию используется по &quot; возрастанию &quot; . 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>По возрастанию</td>
<td>Сортирует по возрастанию.</td>
</tr>
<tr class="even">
<td>По убыванию</td>
<td>Сортирует по убыванию.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
