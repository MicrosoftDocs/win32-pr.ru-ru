---
description: Задает отображаемые сведения о свойстве.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff0bb441b4535c0b6c6f3183671fbe8ade09183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647377"
---
# <a name="displayinfo"></a><span data-ttu-id="13490-103">displayInfo</span><span class="sxs-lookup"><span data-stu-id="13490-103">displayInfo</span></span>

<span data-ttu-id="13490-104">Задает отображаемые сведения о свойстве.</span><span class="sxs-lookup"><span data-stu-id="13490-104">Specifies a property's display information.</span></span> <span data-ttu-id="13490-105">Для каждого [пропертидескриптион](./propdesc-schema-propertydescription.md)должен быть только один элемент [displayInfo]() .</span><span class="sxs-lookup"><span data-stu-id="13490-105">There should be only one [displayInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span>

<span data-ttu-id="13490-106">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="13490-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="13490-107">Если элемент [displayInfo]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13490-107">If no [displayInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="13490-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13490-108">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="13490-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="13490-109">Element Information</span></span>



| <span data-ttu-id="13490-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="13490-110">Parent Element</span></span>                                                   | <span data-ttu-id="13490-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="13490-111">Child Elements</span></span>                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13490-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="13490-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="13490-113">stringFormat</span><span class="sxs-lookup"><span data-stu-id="13490-113">stringFormat</span></span>](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [<span data-ttu-id="13490-114">булеанформат</span><span class="sxs-lookup"><span data-stu-id="13490-114">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [<span data-ttu-id="13490-115">numberFormat</span><span class="sxs-lookup"><span data-stu-id="13490-115">numberFormat</span></span>](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [<span data-ttu-id="13490-116">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="13490-116">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [<span data-ttu-id="13490-117">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="13490-117">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [<span data-ttu-id="13490-118">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="13490-118">drawControl</span></span>](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="13490-119">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="13490-119">editControl</span></span>](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="13490-120">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="13490-120">filterControl</span></span>](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | <span data-ttu-id="13490-121">[куериконтрол](./propdesc-schema-querycontrol.md) (только для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13490-121">[queryControl](./propdesc-schema-querycontrol.md) (Windows Vista only.</span></span> <span data-ttu-id="13490-122">Не поддерживается в Windows 7 и более поздних версиях.)</span><span class="sxs-lookup"><span data-stu-id="13490-122">Not supported in Windows 7 and later.)</span></span> |



 

## <a name="attributes"></a><span data-ttu-id="13490-123">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="13490-123">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13490-124">Атрибут</span><span class="sxs-lookup"><span data-stu-id="13490-124">Attribute</span></span></th>
<th><span data-ttu-id="13490-125">Описание</span><span class="sxs-lookup"><span data-stu-id="13490-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13490-126">дефаултколумнвидс</span><span class="sxs-lookup"><span data-stu-id="13490-126">defaultColumnWidth</span></span></td>
<td><span data-ttu-id="13490-127">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="13490-127">Public.</span></span> <span data-ttu-id="13490-128">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="13490-128">Optional.</span></span> <span data-ttu-id="13490-129">Значение по умолчанию — &quot; 20 &quot; .</span><span class="sxs-lookup"><span data-stu-id="13490-129">Default is &quot;20&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-130">дисплайтипе</span><span class="sxs-lookup"><span data-stu-id="13490-130">displayType</span></span></td>
<td><span data-ttu-id="13490-131">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="13490-131">Public.</span></span> <span data-ttu-id="13490-132">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="13490-132">Optional.</span></span> <span data-ttu-id="13490-133">Значение по умолчанию — &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="13490-133">Default is &quot;String&quot;.</span></span> <span data-ttu-id="13490-134">Указывает тип отображаемой строки.</span><span class="sxs-lookup"><span data-stu-id="13490-134">Specifies the type of the display string.</span></span> <span data-ttu-id="13490-135">После установки здесь значения связанных <strong>PROPDESC_DISPLAYTYPE</strong> извлекаются с помощью <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>Ипропертидескриптион:: жетдисплайтипе</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="13490-135">Once set here, the associated <strong>PROPDESC_DISPLAYTYPE</strong> values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>.</span></span> <span data-ttu-id="13490-136">Ниже приведены допустимые типы.</span><span class="sxs-lookup"><span data-stu-id="13490-136">The following are valid types.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="13490-137">Значение</span><span class="sxs-lookup"><span data-stu-id="13490-137">Value</span></span></th>
<th><span data-ttu-id="13490-138">Значение</span><span class="sxs-lookup"><span data-stu-id="13490-138">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13490-139">Строка</span><span class="sxs-lookup"><span data-stu-id="13490-139">String</span></span></td>
<td><span data-ttu-id="13490-140">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13490-140">Default.</span></span> <span data-ttu-id="13490-141">Значение отображается в виде строки.</span><span class="sxs-lookup"><span data-stu-id="13490-141">Value is displayed as a string.</span></span> <span data-ttu-id="13490-142">Используйте &quot; StringFormat &quot; для форматирования.</span><span class="sxs-lookup"><span data-stu-id="13490-142">Use &quot;stringFormat&quot; to format.</span></span> <span data-ttu-id="13490-143">Метод возвращает PDDT_STRING.</span><span class="sxs-lookup"><span data-stu-id="13490-143">Method returns PDDT_STRING.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-144">Число</span><span class="sxs-lookup"><span data-stu-id="13490-144">Number</span></span></td>
<td><span data-ttu-id="13490-145">Значение по умолчанию для числовых свойств.</span><span class="sxs-lookup"><span data-stu-id="13490-145">Default for numeric properties.</span></span> <span data-ttu-id="13490-146">Значение отображается как число.</span><span class="sxs-lookup"><span data-stu-id="13490-146">Value is displayed as a number.</span></span> <span data-ttu-id="13490-147">Используйте &quot; NumberFormat &quot; для форматирования.</span><span class="sxs-lookup"><span data-stu-id="13490-147">Use &quot;numberFormat&quot; to format.</span></span> <span data-ttu-id="13490-148">Метод возвращает PDDT_NUMBER.</span><span class="sxs-lookup"><span data-stu-id="13490-148">Method returns PDDT_NUMBER.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-149">Логическое</span><span class="sxs-lookup"><span data-stu-id="13490-149">Boolean</span></span></td>
<td><span data-ttu-id="13490-150">Значение по умолчанию <typeInfo type=&quot;Boolean&quot;> , если.</span><span class="sxs-lookup"><span data-stu-id="13490-150">Default if <typeInfo type=&quot;Boolean&quot;>.</span></span> <span data-ttu-id="13490-151">Значение отображается в виде логического значения.</span><span class="sxs-lookup"><span data-stu-id="13490-151">Value is displayed as a boolean.</span></span> <span data-ttu-id="13490-152">Используйте &quot; булеанформат &quot; для форматирования.</span><span class="sxs-lookup"><span data-stu-id="13490-152">Use &quot;booleanFormat&quot; to format.</span></span> <span data-ttu-id="13490-153">Метод возвращает PDDT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="13490-153">Method returns PDDT_BOOLEAN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-154">Дата/время</span><span class="sxs-lookup"><span data-stu-id="13490-154">DateTime</span></span></td>
<td><span data-ttu-id="13490-155">Значение по умолчанию <typeInfo type=&quot;DateTime&quot;> , если.</span><span class="sxs-lookup"><span data-stu-id="13490-155">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="13490-156">Значение отображается как дата или время.</span><span class="sxs-lookup"><span data-stu-id="13490-156">Value is displayed as a date or time.</span></span> <span data-ttu-id="13490-157">Используйте &quot; DateTimeFormat &quot; для форматирования.</span><span class="sxs-lookup"><span data-stu-id="13490-157">Use &quot;dateTimeFormat&quot; to format.</span></span> <span data-ttu-id="13490-158">Метод возвращает PDDT_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="13490-158">Method returns PDDT_DATETIME.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-159">Перечисление</span><span class="sxs-lookup"><span data-stu-id="13490-159">Enumeration</span></span></td>
<td><span data-ttu-id="13490-160">Значение отображается как сопоставление отображаемой строки, предоставленное &quot; элементом енумератедлист &quot; .</span><span class="sxs-lookup"><span data-stu-id="13490-160">Value is displayed as a display string mapping provided by the &quot;enumeratedList&quot; element.</span></span> <span data-ttu-id="13490-161">Метод возвращает PDDT_ENUMERATED.</span><span class="sxs-lookup"><span data-stu-id="13490-161">Method returns PDDT_ENUMERATED.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-162">выравнивание</span><span class="sxs-lookup"><span data-stu-id="13490-162">alignment</span></span></td>
<td><span data-ttu-id="13490-163">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="13490-163">Optional.</span></span> <span data-ttu-id="13490-164">По умолчанию — &quot; Left &quot; .</span><span class="sxs-lookup"><span data-stu-id="13490-164">Default is &quot;Left&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="13490-165">Значение</span><span class="sxs-lookup"><span data-stu-id="13490-165">Value</span></span></th>
<th><span data-ttu-id="13490-166">Значение</span><span class="sxs-lookup"><span data-stu-id="13490-166">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13490-167">Левый</span><span class="sxs-lookup"><span data-stu-id="13490-167">Left</span></span></td>
<td><span data-ttu-id="13490-168">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13490-168">Default.</span></span> <span data-ttu-id="13490-169">По левому краю.</span><span class="sxs-lookup"><span data-stu-id="13490-169">Align left.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-170">Center</span><span class="sxs-lookup"><span data-stu-id="13490-170">Center</span></span></td>
<td><span data-ttu-id="13490-171">Выровнять по центру.</span><span class="sxs-lookup"><span data-stu-id="13490-171">Align center.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-172">Правый</span><span class="sxs-lookup"><span data-stu-id="13490-172">Right</span></span></td>
<td><span data-ttu-id="13490-173">По правому краю.</span><span class="sxs-lookup"><span data-stu-id="13490-173">Align right.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-174">релативедескриптионтипе</span><span class="sxs-lookup"><span data-stu-id="13490-174">relativeDescriptionType</span></span></td>
<td><span data-ttu-id="13490-175">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="13490-175">Optional.</span></span> <span data-ttu-id="13490-176">Значение по умолчанию — &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="13490-176">Default is &quot;General&quot;.</span></span> <span data-ttu-id="13490-177">Указывает, как должны описываться два значения этого свойства при их сравнении друг с другом.</span><span class="sxs-lookup"><span data-stu-id="13490-177">Specifies how two values of this property should be described when they are compared with one another.</span></span> <span data-ttu-id="13490-178">В случае эквивалентности &quot; &quot; всегда используется.</span><span class="sxs-lookup"><span data-stu-id="13490-178">In the case of equivalency, &quot;Same&quot; is always used.</span></span> <span data-ttu-id="13490-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>Ипропертидескриптион:: жетрелативедескриптион</strong></a> и <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>Ипропертидескриптион:: жетрелативедескриптионтипе</strong></a> используют это значение для определения отображаемых имен относительных описаний.</span><span class="sxs-lookup"><span data-stu-id="13490-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> and <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> use this value to determine what relative description display names to use.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="13490-180">Значение</span><span class="sxs-lookup"><span data-stu-id="13490-180">Value</span></span></th>
<th><span data-ttu-id="13490-181">Значение</span><span class="sxs-lookup"><span data-stu-id="13490-181">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13490-182">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="13490-182">General</span></span></td>
<td><span data-ttu-id="13490-183">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13490-183">Default.</span></span> <span data-ttu-id="13490-184">Использует &quot; разные &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="13490-184">Uses &quot;Different&quot; / &quot;Same&quot; / &quot;Different&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-185">Дата</span><span class="sxs-lookup"><span data-stu-id="13490-185">Date</span></span></td>
<td><span data-ttu-id="13490-186">Значение по умолчанию <typeInfo type=&quot;DateTime&quot;> , если.</span><span class="sxs-lookup"><span data-stu-id="13490-186">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="13490-187">Используется раньше или более ранней версии или более ранних, &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; &quot; чем &quot;  /  &quot; &quot;  /  &quot; &quot; &quot; раньше &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="13490-187">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;, or uses &quot;Older&quot; / &quot;Same&quot; / &quot;Newer&quot;, or uses &quot;Sooner&quot; / &quot;Same&quot; / &quot;Later&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-188">Размер</span><span class="sxs-lookup"><span data-stu-id="13490-188">Size</span></span></td>
<td><span data-ttu-id="13490-189">Использует &quot; меньшее &quot;  /  &quot; &quot;  /  &quot; увеличение&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-189">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-190">Count</span><span class="sxs-lookup"><span data-stu-id="13490-190">Count</span></span></td>
<td><span data-ttu-id="13490-191">Использует &quot; меньшее &quot;  /  &quot; &quot;  /  &quot; увеличение&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-191">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-192">Редакция</span><span class="sxs-lookup"><span data-stu-id="13490-192">Revision</span></span></td>
<td><span data-ttu-id="13490-193">Используется &quot; ранее &quot;  /  &quot; &quot;  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-193">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-194">Длина</span><span class="sxs-lookup"><span data-stu-id="13490-194">Length</span></span></td>
<td><span data-ttu-id="13490-195">Использует &quot; более короткий интервал &quot;  /  &quot; &quot;  /  &quot; времени&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-195">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-196">Duration</span><span class="sxs-lookup"><span data-stu-id="13490-196">Duration</span></span></td>
<td><span data-ttu-id="13490-197">Использует &quot; более короткий интервал &quot;  /  &quot; &quot;  /  &quot; времени&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-197">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-198">Speed</span><span class="sxs-lookup"><span data-stu-id="13490-198">Speed</span></span></td>
<td><span data-ttu-id="13490-199">Использует &quot; меньшее быстродействие &quot;  /  &quot; &quot;  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-199">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-200">Тариф</span><span class="sxs-lookup"><span data-stu-id="13490-200">Rate</span></span></td>
<td><span data-ttu-id="13490-201">Использует &quot; меньшее быстродействие &quot;  /  &quot; &quot;  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-201">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-202">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="13490-202">Rating</span></span></td>
<td><span data-ttu-id="13490-203">Использует &quot; меньшее &quot;  /  &quot; самое &quot;  /  &quot; высокое&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-203">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-204">Приоритет</span><span class="sxs-lookup"><span data-stu-id="13490-204">Priority</span></span></td>
<td><span data-ttu-id="13490-205">Использует &quot; меньшее &quot;  /  &quot; самое &quot;  /  &quot; высокое&quot;</span><span class="sxs-lookup"><span data-stu-id="13490-205">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13490-206">дефаултсортдиректион</span><span class="sxs-lookup"><span data-stu-id="13490-206">defaultSortDirection</span></span></td>
<td><span data-ttu-id="13490-207">Задает направление сортировки.</span><span class="sxs-lookup"><span data-stu-id="13490-207">Specifies sort direction.</span></span> <span data-ttu-id="13490-208">По умолчанию используется по &quot; возрастанию &quot; .</span><span class="sxs-lookup"><span data-stu-id="13490-208">Default is &quot;Ascending&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="13490-209">Значение</span><span class="sxs-lookup"><span data-stu-id="13490-209">Value</span></span></th>
<th><span data-ttu-id="13490-210">Значение</span><span class="sxs-lookup"><span data-stu-id="13490-210">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13490-211">По возрастанию</span><span class="sxs-lookup"><span data-stu-id="13490-211">Ascending</span></span></td>
<td><span data-ttu-id="13490-212">Сортирует по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="13490-212">Sorts ascending.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13490-213">По убыванию</span><span class="sxs-lookup"><span data-stu-id="13490-213">Descending</span></span></td>
<td><span data-ttu-id="13490-214">Сортирует по убыванию.</span><span class="sxs-lookup"><span data-stu-id="13490-214">Sorts descending.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
