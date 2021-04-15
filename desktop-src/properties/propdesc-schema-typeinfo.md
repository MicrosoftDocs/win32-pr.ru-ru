---
description: Указывает сведения о типе свойства.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662756"
---
# <a name="typeinfo"></a><span data-ttu-id="5fcd9-103">typeInfo</span><span class="sxs-lookup"><span data-stu-id="5fcd9-103">typeInfo</span></span>

<span data-ttu-id="5fcd9-104">Указывает сведения о типе свойства.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-104">Specifies a property's type information.</span></span> <span data-ttu-id="5fcd9-105">Для каждого [пропертидескриптион](./propdesc-schema-propertydescription.md)должен быть только один элемент [typeInfo]() .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-105">There should be only one [typeInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span> <span data-ttu-id="5fcd9-106">Этот элемент был изменен для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-106">This element has changed for Windows 7.</span></span>

<span data-ttu-id="5fcd9-107">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="5fcd9-108">Если элемент [typeInfo]() не предоставлен, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-108">If no [typeInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="5fcd9-109">Синтаксис для Windows 7</span><span class="sxs-lookup"><span data-stu-id="5fcd9-109">Syntax for Windows 7</span></span>


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



## <a name="element-information"></a><span data-ttu-id="5fcd9-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5fcd9-110">Element Information</span></span>



| <span data-ttu-id="5fcd9-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="5fcd9-111">Parent Element</span></span>                                                   | <span data-ttu-id="5fcd9-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5fcd9-112">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="5fcd9-113">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="5fcd9-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="5fcd9-114">Нет</span><span class="sxs-lookup"><span data-stu-id="5fcd9-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="5fcd9-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5fcd9-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fcd9-116">Атрибут</span><span class="sxs-lookup"><span data-stu-id="5fcd9-116">Attribute</span></span></th>
<th><span data-ttu-id="5fcd9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5fcd9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fcd9-118">type</span><span class="sxs-lookup"><span data-stu-id="5fcd9-118">type</span></span></td>
<td><span data-ttu-id="5fcd9-119">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-119">Public.</span></span> <span data-ttu-id="5fcd9-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-120">Optional.</span></span> <span data-ttu-id="5fcd9-121">Значение по умолчанию — &quot; ANY &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-121">Default is &quot;Any&quot;.</span></span> <span data-ttu-id="5fcd9-122">Указывает тип свойства.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-122">Indicates the type of the property.</span></span> <span data-ttu-id="5fcd9-123">Ниже приведены допустимые типы и связанные с ними типы Variant, полученные с помощью <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>ипропертидескриптион:: жетпропертитипе</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-123">The following are valid types and their associated variant types are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5fcd9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-124">Value</span></span></th>
<th><span data-ttu-id="5fcd9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fcd9-126">Любой</span><span class="sxs-lookup"><span data-stu-id="5fcd9-126">Any</span></span></td>
<td><span data-ttu-id="5fcd9-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-127">Default.</span></span> <span data-ttu-id="5fcd9-128">Подсистема свойств не будет применять или приводить значение свойства.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-128">The property subsystem will not enforce or coerce the property value.</span></span> <span data-ttu-id="5fcd9-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>Ипропертидескриптион:: жетпропертитипе</strong></a> Возвращает VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span> <span data-ttu-id="5fcd9-130">Независимые поставщики программного обеспечения настоятельно рекомендуется предоставлять тип, а не возвращаться к этому по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-130">Independent software vendors (ISVs) are strongly encouraged to provide a type rather than fall back on this default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-131">NULL</span><span class="sxs-lookup"><span data-stu-id="5fcd9-131">Null</span></span></td>
<td><span data-ttu-id="5fcd9-132">Для этого свойства значение отсутствует.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-132">There is no value for this property.</span></span> <span data-ttu-id="5fcd9-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>Ипропертидескриптион:: жетпропертитипе</strong></a> Возвращает VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-134">Строка</span><span class="sxs-lookup"><span data-stu-id="5fcd9-134">String</span></span></td>
<td><span data-ttu-id="5fcd9-135">Значение должно быть VT_LPWSTR, которое представляет собой строку в Юникоде, заканчивающуюся пустой ссылкой.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-135">The value must be a VT_LPWSTR, which is a Unicode string terminated by a null reference.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-136">Логическое</span><span class="sxs-lookup"><span data-stu-id="5fcd9-136">Boolean</span></span></td>
<td><span data-ttu-id="5fcd9-137">Значение должно быть значением VT_BOOL, которое является логическим.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-137">The value must be a VT_BOOL, which is a boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-138">Byte</span><span class="sxs-lookup"><span data-stu-id="5fcd9-138">Byte</span></span></td>
<td><span data-ttu-id="5fcd9-139">Значение должно быть VT_UI1, которое представляет собой байт.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-139">The value must be a VT_UI1, which is a byte.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-140">Буфер</span><span class="sxs-lookup"><span data-stu-id="5fcd9-140">Buffer</span></span></td>
<td><span data-ttu-id="5fcd9-141">Значение должно быть VT_UI1ом | VT_VECTOR буфер байтов.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-141">The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-142">Int16</span><span class="sxs-lookup"><span data-stu-id="5fcd9-142">Int16</span></span></td>
<td><span data-ttu-id="5fcd9-143">Значение должно быть VT_I2ом, представляющим 16-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-143">The value must be a VT_I2, which is a 16-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-144">UInt16</span><span class="sxs-lookup"><span data-stu-id="5fcd9-144">UInt16</span></span></td>
<td><span data-ttu-id="5fcd9-145">Значение должно быть значением VT_UI2, которое представляет собой 16-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-145">The value must be a VT_UI2, which is a 16-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-146">Int32</span><span class="sxs-lookup"><span data-stu-id="5fcd9-146">Int32</span></span></td>
<td><span data-ttu-id="5fcd9-147">Значение должно быть VT_I4, которое представляет собой 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-147">The value must be a VT_I4, which is a 32-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-148">UInt32</span><span class="sxs-lookup"><span data-stu-id="5fcd9-148">UInt32</span></span></td>
<td><span data-ttu-id="5fcd9-149">Значение должно быть VT_UI4, которое представляет собой 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-149">The value must be a VT_UI4, which is a 32-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-150">Int64</span><span class="sxs-lookup"><span data-stu-id="5fcd9-150">Int64</span></span></td>
<td><span data-ttu-id="5fcd9-151">Значение должно быть VT_I8, которое представляет собой 64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-151">The value must be a VT_I8, which is a 64-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-152">UInt64</span><span class="sxs-lookup"><span data-stu-id="5fcd9-152">UInt64</span></span></td>
<td><span data-ttu-id="5fcd9-153">Значение должно быть VT_UI8, которое представляет собой 64-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-153">The value must be a VT_UI8, which is a 64-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-154">Double</span><span class="sxs-lookup"><span data-stu-id="5fcd9-154">Double</span></span></td>
<td><span data-ttu-id="5fcd9-155">Значение должно быть VT_R8, которое является типом Double.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-155">The value must be a VT_R8, which is a double.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-156">Дата/время</span><span class="sxs-lookup"><span data-stu-id="5fcd9-156">DateTime</span></span></td>
<td><span data-ttu-id="5fcd9-157">Значение должно быть VT_FILETIME, которое является значением <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>fileTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-157">The value must be a VT_FILETIME, which is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-158">Guid</span><span class="sxs-lookup"><span data-stu-id="5fcd9-158">Guid</span></span></td>
<td><span data-ttu-id="5fcd9-159">Значение должно быть VT_CLSID, которое является идентификатором класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="5fcd9-159">The value must be a VT_CLSID, which is a class identifier (CLSID).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-160">BLOB-объект</span><span class="sxs-lookup"><span data-stu-id="5fcd9-160">Blob</span></span></td>
<td><span data-ttu-id="5fcd9-161">Значение должно быть VT_BLOB, которое имеет длину в байтах с префиксом.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-161">The value must be a VT_BLOB, which are length-prefixed bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-162">Stream</span><span class="sxs-lookup"><span data-stu-id="5fcd9-162">Stream</span></span></td>
<td><span data-ttu-id="5fcd9-163">Значение должно быть VT_STREAM, которое является объектом, реализующим <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-163">The value must be a VT_STREAM, which is an object that implements <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-164">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="5fcd9-164">Clipboard</span></span></td>
<td><span data-ttu-id="5fcd9-165">Значение должно быть VT_CF, которое является форматом буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-165">The value must be a VT_CF, which is a clipboard format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-166">Объект</span><span class="sxs-lookup"><span data-stu-id="5fcd9-166">Object</span></span></td>
<td><span data-ttu-id="5fcd9-167">Значение должно быть VT_UNKNOWN, которое является объектом, реализующим <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-167">The value must be a VT_UNKNOWN, which is an object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-168">граупингранже</span><span class="sxs-lookup"><span data-stu-id="5fcd9-168">groupingRange</span></span></td>
<td><span data-ttu-id="5fcd9-169">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-169">Optional.</span></span> <span data-ttu-id="5fcd9-170">Значение по умолчанию — &quot; Дискретный &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-170">Default is &quot;Discrete&quot;.</span></span> <span data-ttu-id="5fcd9-171">Указывает, как свойство отображается, если представление сгруппировано по этому свойству.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-171">Specifies how the property is displayed when a view is grouped by this property.</span></span> <span data-ttu-id="5fcd9-172">После установки эти значения извлекаются с помощью <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>ипропертидескриптион:: жетграупингранже</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-172">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>.</span></span> <span data-ttu-id="5fcd9-173">Ниже приведены допустимые типы.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-173">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5fcd9-174">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-174">Value</span></span></th>
<th><span data-ttu-id="5fcd9-175">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-175">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fcd9-176">Discrete</span><span class="sxs-lookup"><span data-stu-id="5fcd9-176">Discrete</span></span></td>
<td><span data-ttu-id="5fcd9-177">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-177">Default.</span></span> <span data-ttu-id="5fcd9-178">Отображает отдельные значения.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-178">Displays individual values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-179">Буквенно-цифровой</span><span class="sxs-lookup"><span data-stu-id="5fcd9-179">Alphanumeric</span></span></td>
<td><span data-ttu-id="5fcd9-180">Отображает статические буквенно-цифровые диапазоны значений.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-180">Displays static alphanumeric ranges for values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-181">Размер</span><span class="sxs-lookup"><span data-stu-id="5fcd9-181">Size</span></span></td>
<td><span data-ttu-id="5fcd9-182">Отображает диапазоны статических размеров для значений.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-182">Displays static size ranges for values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-183">Дата</span><span class="sxs-lookup"><span data-stu-id="5fcd9-183">Date</span></span></td>
<td><span data-ttu-id="5fcd9-184">Отображает группы "месяц/год".</span><span class="sxs-lookup"><span data-stu-id="5fcd9-184">Displays month/year groups.</span></span> <span data-ttu-id="5fcd9-185">По умолчанию для свойств типа = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-185">Default for properties of type=&quot;DateTime&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-186">тимерелативе</span><span class="sxs-lookup"><span data-stu-id="5fcd9-186">TimeRelative</span></span></td>
<td><span data-ttu-id="5fcd9-187">Отображает в группах, относительных по времени.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-187">Displays in time-relative groups.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-188">Динамический</span><span class="sxs-lookup"><span data-stu-id="5fcd9-188">Dynamic</span></span></td>
<td><span data-ttu-id="5fcd9-189">Отображает динамически созданные диапазоны для значений.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-189">Displays dynamically created ranges for the values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-190">Процент</span><span class="sxs-lookup"><span data-stu-id="5fcd9-190">Percent</span></span></td>
<td><span data-ttu-id="5fcd9-191">Отображает сегмент процентов.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-191">Displays percent buckets.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-192">исиннате</span><span class="sxs-lookup"><span data-stu-id="5fcd9-192">isInnate</span></span></td>
<td><span data-ttu-id="5fcd9-193">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-193">Public.</span></span> <span data-ttu-id="5fcd9-194">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-194">Optional.</span></span> <span data-ttu-id="5fcd9-195">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-195">Default is &quot;false&quot;.</span></span> <span data-ttu-id="5fcd9-196">Указывает, считается ли свойство присущей.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-196">Specifies whether the property is considered innate.</span></span> <span data-ttu-id="5fcd9-197">Свойство присущей, которое либо вычисляется из содержимого файла, либо из других ресурсов или систем.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-197">An innate property is one which is either calculated from the content of a file, or from other resources or systems.</span></span> <span data-ttu-id="5fcd9-198">Например, System. Size — это свойство присущей, предоставляемое файловой системой. изменение значения свойства в и само по себе не делает ничего.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-198">For example, System.Size is an innate property provided by the file system; changing the value of the property in and of itself does nothing.</span></span> <span data-ttu-id="5fcd9-199">Другие примеры — System. Image. Dimensions и System.Docумент. PageCount, которые рассчитываются программами на основе содержимого файла, а не на основе изменяемого пользователем параметра.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-199">Other examples are System.Image.Dimensions and System.Document.PageCount, which are calculated by programs based upon the content of the file, not based upon a user-changeable setting.</span></span> <span data-ttu-id="5fcd9-200">Установка Исиннате = &quot; true &quot; означает, что пользователь не может изменить это свойство непосредственно через элемент управления свойства.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-200">Setting isInnate=&quot;true&quot; means the user cannot edit this property directly via a property control.</span></span> <span data-ttu-id="5fcd9-201">Это значение сопоставляется с флагом PDTF_ISINNATE, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-201">This value maps to the PDTF_ISINNATE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-202">канбепуржед</span><span class="sxs-lookup"><span data-stu-id="5fcd9-202">canBePurged</span></span></td>
<td><span data-ttu-id="5fcd9-203"><strong>Windows Vista с пакетом обновления 1 (SP1) и более поздних версий</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-203"><strong>Windows Vista with Service Pack 1 (SP1) and later only</strong>.</span></span> <span data-ttu-id="5fcd9-204">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-204">Public.</span></span> <span data-ttu-id="5fcd9-205">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-205">Optional.</span></span> <span data-ttu-id="5fcd9-206">Если задано значение &quot; true &quot; , можно удалить свойство присущей.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-206">When set to &quot;true&quot;, allows an innate property to be deleted.</span></span> <span data-ttu-id="5fcd9-207">Свойства присущей, вычисляемые из других свойств, доступны только для чтения по определению.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-207">Innate properties, which are calculated from other properties, are read-only by definition.</span></span> <span data-ttu-id="5fcd9-208">Значение по умолчанию для этого атрибута зависит от значения <em>исиннате</em> .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-208">The default value for this attribute depends on the <em>isInnate</em> value.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5fcd9-209">исиннате</span><span class="sxs-lookup"><span data-stu-id="5fcd9-209">isInnate</span></span></th>
<th><span data-ttu-id="5fcd9-210">Канбепуржед значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5fcd9-210">canBePurged Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fcd9-211">true</span><span class="sxs-lookup"><span data-stu-id="5fcd9-211">true</span></span></td>
<td><span data-ttu-id="5fcd9-212">false</span><span class="sxs-lookup"><span data-stu-id="5fcd9-212">false</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-213">false</span><span class="sxs-lookup"><span data-stu-id="5fcd9-213">false</span></span></td>
<td><span data-ttu-id="5fcd9-214">true</span><span class="sxs-lookup"><span data-stu-id="5fcd9-214">true</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="5fcd9-215">Свойство, значение <em>исиннате</em> которого равно &quot; false &quot; (т. е. свойство доступно для чтения и записи), не может также задавать значение false для значения <em>канбепуржед</em> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-215">A property whose <em>isInnate</em> value is &quot;false&quot; (meaning that the property is read/write) cannot also set the <em>canBePurged</em> value to &quot;false&quot;.</span></span> <span data-ttu-id="5fcd9-216">Это ограничение применяется операционной системой.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-216">This restriction is enforced by the operating system.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="5fcd9-217">Хотя этот атрибут появился в Windows Vista с пакетом обновления 1 (SP1), файл. пропдеск, включающий этот атрибут, совместим с Windows Vista до Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5fcd9-217">Although this attribute was introduced in Windows Vista with Service Pack 1 (SP1), a .propdesc file that includes this attribute is compatible with Windows Vista prior to Windows Vista with SP1.</span></span> <span data-ttu-id="5fcd9-218">В этой ситуации атрибут <em>канбепуржед</em> просто игнорируется.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-218">The <em>canBePurged</em> attribute is simply ignored in that situation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-219">мултиплевалуес</span><span class="sxs-lookup"><span data-stu-id="5fcd9-219">multipleValues</span></span></td>
<td><span data-ttu-id="5fcd9-220">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-220">Public.</span></span> <span data-ttu-id="5fcd9-221">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-221">Optional.</span></span> <span data-ttu-id="5fcd9-222">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-222">Default is &quot;false&quot;.</span></span> <span data-ttu-id="5fcd9-223">Указывает, может ли это свойство иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-223">Specifies whether this property can have multiple values.</span></span> <span data-ttu-id="5fcd9-224">Это значение сопоставляется с флагом PDTF_MULTIPLEVALUES, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-224">This value maps to the PDTF_MULTIPLEVALUES flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span> <span data-ttu-id="5fcd9-225">Это также влияет на то, имеет ли VT_VECTOR значение типа VARTYPE значения свойства.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-225">This also influences whether VT_VECTOR is OR'd to the VARTYPE of the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-226">isGroup</span><span class="sxs-lookup"><span data-stu-id="5fcd9-226">isGroup</span></span></td>
<td><span data-ttu-id="5fcd9-227">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-227">Public.</span></span> <span data-ttu-id="5fcd9-228">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-228">Optional.</span></span> <span data-ttu-id="5fcd9-229">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-229">Default is &quot;false&quot;.</span></span> <span data-ttu-id="5fcd9-230">Указывает, является ли свойство заголовком группы.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-230">Specifies whether the property is a group heading.</span></span> <span data-ttu-id="5fcd9-231">Заголовок группы строго используется в проплистс, не имеет значения, никогда не хранится в файле, а также должен иметь <typeInfo type=&quot;Null&quot;> .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-231">A group heading is strictly used in proplists, has no value, is never stored in a file, and should also have <typeInfo type=&quot;Null&quot;>.</span></span> <span data-ttu-id="5fcd9-232">Некоторые элементы пользовательского интерфейса в системе используют проплистс для указания последовательности отображаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-232">Some UI in the system use proplists to indicate the sequence of the properties to display.</span></span> <span data-ttu-id="5fcd9-233">Эти проплистс могут содержать ссылки на заголовки групп (например, System. Пропграуп. Camera), которые сообщают пользовательскому интерфейсу о необходимости запуска нового раздела группы (например, &quot; параметры камеры &quot; ).</span><span class="sxs-lookup"><span data-stu-id="5fcd9-233">These proplists may include references to group headings (eg, System.PropGroup.Camera), which tell the UI to start a new group section (eg, &quot;Camera Settings&quot;).</span></span> <span data-ttu-id="5fcd9-234">В описании свойства с параметром &quot; IsTrue = true &quot; должно быть указано значение <labelInfo label=&quot;Some localized label&quot;> , иначе это не полезное свойство.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-234">A property description with isGroup=&quot;true&quot; should specify a <labelInfo label=&quot;Some localized label&quot;>, otherwise it isn't a useful property.</span></span> <span data-ttu-id="5fcd9-235">Это значение сопоставляется с флагом PDTF_ISGROUP, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-235">This value maps to the PDTF_ISGROUP flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-236">aggregationType</span><span class="sxs-lookup"><span data-stu-id="5fcd9-236">aggregationType</span></span></td>
<td><span data-ttu-id="5fcd9-237">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-237">Public.</span></span> <span data-ttu-id="5fcd9-238">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-238">Optional.</span></span> <span data-ttu-id="5fcd9-239">Значение по умолчанию — &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-239">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="5fcd9-240">Задает способ отображения агрегатных свойств при выборе нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-240">Specifies how aggregate properties are displayed when multiple items are selected.</span></span> <span data-ttu-id="5fcd9-241">После установки эти значения извлекаются с помощью <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>ипропертидескриптион:: жетаггрегатионтипе</strong></a> в качестве <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-241">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> as an <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span></span> <span data-ttu-id="5fcd9-242">Ниже приведены допустимые типы.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-242">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5fcd9-243">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-243">Value</span></span></th>
<th><span data-ttu-id="5fcd9-244">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-244">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fcd9-245">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5fcd9-245">Default</span></span></td>
<td><span data-ttu-id="5fcd9-246">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-246">Default.</span></span> <span data-ttu-id="5fcd9-247">Отображает заполнитель с <strong>несколькими значениями</strong> в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-247">Displays a <strong>Multiple Values</strong> placeholder in the UI.</span></span> <span data-ttu-id="5fcd9-248">Это значение по умолчанию, если <em>тип</em> несовместим с указанным <em>aggregationType</em>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-248">This is the default if the <em>type</em> is incompatible with the specified <em>aggregationType</em>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-249">First</span><span class="sxs-lookup"><span data-stu-id="5fcd9-249">First</span></span></td>
<td><span data-ttu-id="5fcd9-250">Отображает значение свойства первого элемента в выделенном фрагменте или коллекции.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-250">Displays the property value of the first item in the selection or collection.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-251">SUM</span><span class="sxs-lookup"><span data-stu-id="5fcd9-251">Sum</span></span></td>
<td><span data-ttu-id="5fcd9-252">Отображает сумму числовых значений.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-252">Displays the sum of the numerical values.</span></span> <span data-ttu-id="5fcd9-253">Полезно для таких свойств, как System. Media. Duration или System. size.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-253">Useful for properties such as System.Media.Duration or System.Size.</span></span> <span data-ttu-id="5fcd9-254">Это значение несовместимо с нечисловыми типами.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-254">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-255">Среднее значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-255">Average</span></span></td>
<td><span data-ttu-id="5fcd9-256">Отображает среднее арифметическое числовых значений.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-256">Displays the average of the numerical values.</span></span> <span data-ttu-id="5fcd9-257">Полезно для таких свойств, как System. рейтингов.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-257">Useful for properties such as System.Rating.</span></span> <span data-ttu-id="5fcd9-258">Это значение несовместимо с нечисловыми типами.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-258">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-259">Диапазон дат</span><span class="sxs-lookup"><span data-stu-id="5fcd9-259">DateRange</span></span></td>
<td><span data-ttu-id="5fcd9-260">Отображает диапазон дат.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-260">Displays a range of dates.</span></span> <span data-ttu-id="5fcd9-261">Полезен для таких свойств, как System. photo. Датетакен.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-261">Useful for properties like System.Photo.DateTaken.</span></span> <span data-ttu-id="5fcd9-262">Это значение несовместимо с любым исключением, кроме Type = &quot; DateTime &quot; и является значением по умолчанию для свойств этого типа.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-262">This value is not compatible with anything except type=&quot;DateTime&quot; and is the default for properties of that type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-263">Union</span><span class="sxs-lookup"><span data-stu-id="5fcd9-263">Union</span></span></td>
<td><span data-ttu-id="5fcd9-264">Отображает объединение всех значений в выделении или коллекции.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-264">Displays a union of all the values in the selection or collection.</span></span> <span data-ttu-id="5fcd9-265">Порядок отображения значений не определен.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-265">The order in which the values are shown is undefined.</span></span> <span data-ttu-id="5fcd9-266">Это значение используется по умолчанию для свойств типа = &quot; String &quot; и мултиплевалуес = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-266">This value is the default for properties of type=&quot;String&quot; and multipleValues=&quot;true&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-267">Максимум</span><span class="sxs-lookup"><span data-stu-id="5fcd9-267">Maximum</span></span></td>
<td><span data-ttu-id="5fcd9-268">Отображает максимальное значение в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-268">Displays the maximum value in the collection.</span></span> <span data-ttu-id="5fcd9-269">Полезен для таких свойств, как System. DateModified.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-269">Useful for properties like System.DateModified.</span></span> <span data-ttu-id="5fcd9-270">Несовместимо с нечисловыми или типами, не являющимися датами.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-270">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-271">Минимальные</span><span class="sxs-lookup"><span data-stu-id="5fcd9-271">Minimum</span></span></td>
<td><span data-ttu-id="5fcd9-272">Отображает минимальное значение в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-272">Displays the minimum value in the collection.</span></span> <span data-ttu-id="5fcd9-273">Несовместимо с нечисловыми или типами, не являющимися датами.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-273">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-274">истрипроперти</span><span class="sxs-lookup"><span data-stu-id="5fcd9-274">isTreeProperty</span></span></td>
<td><span data-ttu-id="5fcd9-275">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-275">Public.</span></span> <span data-ttu-id="5fcd9-276">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-276">Optional.</span></span> <span data-ttu-id="5fcd9-277">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-277">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-278">для просмотра</span><span class="sxs-lookup"><span data-stu-id="5fcd9-278">isViewable</span></span></td>
<td><span data-ttu-id="5fcd9-279">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-279">Public.</span></span> <span data-ttu-id="5fcd9-280">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-280">Optional.</span></span> <span data-ttu-id="5fcd9-281">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-281">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="5fcd9-282">Указывает, должно ли это свойство быть видимым для пользователя.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-282">Specifies whether this property is intended to be viewable to the user.</span></span> <span data-ttu-id="5fcd9-283">Например, в пользовательском интерфейсе выбора столбцов отображаются только те свойства, которые имеют значение «Viewed» = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-283">For example, the Column Chooser UI only shows the properties that have isViewable=&quot;true&quot;.</span></span> <span data-ttu-id="5fcd9-284">Исключением является Пользовательский интерфейс, управляемый проплист, который всегда будет отображать свойство.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-284">The exception is UI that is driven by a proplist, which will always show the property.</span></span> <span data-ttu-id="5fcd9-285">Если у вас есть свойство, предназначенное только для выбора данных между двумя объектами и не предназначенное для просмотра пользователем, этот атрибут должен иметь значение false.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-285">If you have a property that is only meant to shuttle data between two objects, and never intended to be viewed by the user, this attribute should be false.</span></span> <span data-ttu-id="5fcd9-286">Это значение сопоставляется с флагом PDTF_ISVIEWABLE, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-286">This value maps to the PDTF_ISVIEWABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-287">с подзапросом</span><span class="sxs-lookup"><span data-stu-id="5fcd9-287">isQueryable</span></span></td>
<td><span data-ttu-id="5fcd9-288">Только для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-288">Windows Vista only.</span></span> <span data-ttu-id="5fcd9-289">Не поддерживается в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-289">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="5fcd9-290">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-290">Public.</span></span> <span data-ttu-id="5fcd9-291">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-291">Optional.</span></span> <span data-ttu-id="5fcd9-292">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-292">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="5fcd9-293">Указывает, должно ли это свойство быть доступно в пользовательском интерфейсе конструктор запросов поиска.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-293">Specifies whether this property is intended to be available in the Search Query Builder UI.</span></span> <span data-ttu-id="5fcd9-294">Свойство должно иметь значение "IsTrue" = &quot; true &quot; , прежде чем &quot; параметру IsTrue = true &quot; соблюдается.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-294">A property must have isViewable=&quot;true&quot; before isQueryable=&quot;true&quot; is respected.</span></span> <span data-ttu-id="5fcd9-295">Это значение сопоставляется с флагом PDTF_ISQUERYABLE, определенным в <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> и используется в <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>Ипропертидескриптион:: жеттипефлагс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-295">This value maps to the PDTF_ISQUERYABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-296">сеарчраввалуе</span><span class="sxs-lookup"><span data-stu-id="5fcd9-296">searchRawValue</span></span></td>
<td><span data-ttu-id="5fcd9-297"><strong>Windows 7 и более поздние версии.</strong></span><span class="sxs-lookup"><span data-stu-id="5fcd9-297"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="5fcd9-298">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-298">Public.</span></span> <span data-ttu-id="5fcd9-299">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-299">Optional.</span></span> <span data-ttu-id="5fcd9-300">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-300">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-301">инклудеинфуллтексткуери</span><span class="sxs-lookup"><span data-stu-id="5fcd9-301">includeInFullTextQuery</span></span></td>
<td><span data-ttu-id="5fcd9-302">Только для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-302">Windows Vista only.</span></span> <span data-ttu-id="5fcd9-303">Не поддерживается в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-303">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="5fcd9-304">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-304">Public.</span></span> <span data-ttu-id="5fcd9-305">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-305">Optional.</span></span> <span data-ttu-id="5fcd9-306">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-306">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-307">conditionType</span><span class="sxs-lookup"><span data-stu-id="5fcd9-307">conditionType</span></span></td>
<td><span data-ttu-id="5fcd9-308">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-308">Public.</span></span> <span data-ttu-id="5fcd9-309">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-309">Optional.</span></span> <span data-ttu-id="5fcd9-310">Значение по умолчанию — &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-310">Default is &quot;String&quot;.</span></span> <span data-ttu-id="5fcd9-311">Задает указание для пользовательского интерфейса конструктор запросов поиска, чтобы он мог определить список возможных операторов условия внутри предиката.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-311">Specifies a hint to the Search Query Builder UI so that it can determine the list of possible condition operators inside a predicate.</span></span> <span data-ttu-id="5fcd9-312">Ниже приведены распознаваемые значения.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-312">The following are recognized values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5fcd9-313">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-313">Value</span></span></th>
<th><span data-ttu-id="5fcd9-314">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-314">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fcd9-315">Строка</span><span class="sxs-lookup"><span data-stu-id="5fcd9-315">String</span></span></td>
<td><span data-ttu-id="5fcd9-316">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-316">Default.</span></span> <span data-ttu-id="5fcd9-317">Будут использоваться следующие операторы: имеет значение &quot; &quot; , not,,,, &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; , &quot; начинается с, &quot; &quot; заканчивается на &quot; , &quot; Contains &quot; , &quot; не содержит &quot; , &quot; имеет значение Like &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-317">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;&lt;&quot;, &quot;&gt;&quot;, &quot;<=&quot;, &quot;>=&quot;, &quot;starts with&quot;, &quot;ends with&quot;, &quot;contains&quot;, &quot;doesn't contain&quot;, &quot;is like&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-318">Число</span><span class="sxs-lookup"><span data-stu-id="5fcd9-318">Number</span></span></td>
<td><span data-ttu-id="5fcd9-319">Значение по умолчанию для числовых свойств.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-319">Default for numeric properties.</span></span> <span data-ttu-id="5fcd9-320">Следующие операторы будут использоваться: &quot; Equals, &quot; &quot; не равно &quot; , &quot; меньше &quot; , &quot; больше &quot; , &quot; меньше или равно &quot; , &quot; больше или равно &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-320">The following operators will be used: &quot;equals&quot;, &quot;doesn't equal&quot;, &quot;is less than&quot;, &quot;is greater than&quot;, &quot;is less than or equal to&quot;, &quot;is greater than or equal to&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-321">Дата/время</span><span class="sxs-lookup"><span data-stu-id="5fcd9-321">DateTime</span></span></td>
<td><span data-ttu-id="5fcd9-322">По умолчанию для свойств типа = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-322">Default for properties of type=&quot;DateTime&quot;.</span></span> <span data-ttu-id="5fcd9-323">Будут использоваться следующие операторы: имеет значение &quot; , а — &quot; &quot; нет &quot; , &quot; перед, &quot; &quot; а — до, а — после, &quot; &quot; &quot; &quot; а &quot; включается.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-323">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;is before&quot;, &quot;is after&quot;, &quot;is before but includes&quot;, &quot;is after but includes&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-324">Логическое</span><span class="sxs-lookup"><span data-stu-id="5fcd9-324">Boolean</span></span></td>
<td><span data-ttu-id="5fcd9-325">По умолчанию для свойств типа = &quot; Boolean &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-325">Default for properties of type=&quot;Boolean&quot;.</span></span> <span data-ttu-id="5fcd9-326">То же, что и номер.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-326">Same as Number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-327">Размер</span><span class="sxs-lookup"><span data-stu-id="5fcd9-327">Size</span></span></td>
<td><span data-ttu-id="5fcd9-328">То же, что и номер.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-328">Same as Number.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-329">дефаултоператион</span><span class="sxs-lookup"><span data-stu-id="5fcd9-329">defaultOperation</span></span></td>
<td><span data-ttu-id="5fcd9-330">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-330">Public.</span></span> <span data-ttu-id="5fcd9-331">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-331">Optional.</span></span> <span data-ttu-id="5fcd9-332">Значение по умолчанию &quot; равно &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-332">Default is &quot;Equal&quot;.</span></span> <span data-ttu-id="5fcd9-333">Задает указание для средства поиска конструктор запросов, чтобы оно могла определить оператора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-333">Specifies a hint to the Search Query Builder tool so that it can determine the default operator.</span></span> <span data-ttu-id="5fcd9-334">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5fcd9-334">The possible values are as follows:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5fcd9-335">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-335">Value</span></span></th>
<th><span data-ttu-id="5fcd9-336">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcd9-336">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fcd9-337">Равно</span><span class="sxs-lookup"><span data-stu-id="5fcd9-337">Equal</span></span></td>
<td><span data-ttu-id="5fcd9-338">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-338">Default.</span></span> <span data-ttu-id="5fcd9-339">Обозначает эквивалент.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-339">Indicates equivalent.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-340">NotEqual</span><span class="sxs-lookup"><span data-stu-id="5fcd9-340">NotEqual</span></span></td>
<td><span data-ttu-id="5fcd9-341">Указывает на неэквивалентность.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-341">Indicates not equivalent.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-342">LessThan;</span><span class="sxs-lookup"><span data-stu-id="5fcd9-342">LessThan</span></span></td>
<td><span data-ttu-id="5fcd9-343">Указывает, что меньше.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-343">Indicates less than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fcd9-344">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="5fcd9-344">GreaterThan</span></span></td>
<td><span data-ttu-id="5fcd9-345">По умолчанию для свойств исключением = &quot; size &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-345">Default for properties of conditionType=&quot;Size&quot;.</span></span> <span data-ttu-id="5fcd9-346">Указывает, что больше.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-346">Indicates greater than.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fcd9-347">Содержит</span><span class="sxs-lookup"><span data-stu-id="5fcd9-347">Contains</span></span></td>
<td><span data-ttu-id="5fcd9-348">По умолчанию для свойств исключением = &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="5fcd9-348">Default for properties of conditionType=&quot;String&quot;.</span></span> <span data-ttu-id="5fcd9-349">Указывает на включение.</span><span class="sxs-lookup"><span data-stu-id="5fcd9-349">Indicates inclusion.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
