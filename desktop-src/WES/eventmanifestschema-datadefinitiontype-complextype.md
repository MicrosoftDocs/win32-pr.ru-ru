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
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693955"
---
# <a name="datadefinitiontype-complex-type"></a><span data-ttu-id="be9f3-105">Сложный тип Датадефинитионтипе</span><span class="sxs-lookup"><span data-stu-id="be9f3-105">DataDefinitionType Complex Type</span></span>

<span data-ttu-id="be9f3-106">Определяет элемент данных, который необходимо включить в событие.</span><span class="sxs-lookup"><span data-stu-id="be9f3-106">Defines a data item that you want to include with the event.</span></span>

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

## <a name="attributes"></a><span data-ttu-id="be9f3-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="be9f3-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be9f3-108">Имя</span><span class="sxs-lookup"><span data-stu-id="be9f3-108">Name</span></span></th>
<th><span data-ttu-id="be9f3-109">Тип</span><span class="sxs-lookup"><span data-stu-id="be9f3-109">Type</span></span></th>
<th><span data-ttu-id="be9f3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="be9f3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be9f3-111">count</span><span class="sxs-lookup"><span data-stu-id="be9f3-111">count</span></span></td>
<td><span data-ttu-id="be9f3-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>каунттипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="be9f3-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span></span></td>
<td><span data-ttu-id="be9f3-113">Число элементов в массиве, если элемент данных является массивом.</span><span class="sxs-lookup"><span data-stu-id="be9f3-113">The number of elements in the array if the data item is an array.</span></span> <span data-ttu-id="be9f3-114">Можно указать фактическое число или имя другого элемента данных, содержащего число.</span><span class="sxs-lookup"><span data-stu-id="be9f3-114">You can specify the actual count or the name of another data item that contains the count.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be9f3-115">Тип</span><span class="sxs-lookup"><span data-stu-id="be9f3-115">inType</span></span></td>
<td><span data-ttu-id="be9f3-116"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="be9f3-116"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="be9f3-117">Тип данных для этого элемента данных.</span><span class="sxs-lookup"><span data-stu-id="be9f3-117">The data type for this data item.</span></span> <span data-ttu-id="be9f3-118">Список предопределенных типов входных данных см. в разделе сложный тип <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="be9f3-118">For a list of predefined input data types, see the <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be9f3-119">length</span><span class="sxs-lookup"><span data-stu-id="be9f3-119">length</span></span></td>
<td><span data-ttu-id="be9f3-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>ленгстипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="be9f3-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span></span></td>
<td><span data-ttu-id="be9f3-121">Длина элемента данных переменной длины, например двоичного объекта BLOB.</span><span class="sxs-lookup"><span data-stu-id="be9f3-121">The length of a variable length data item, such as a binary blob.</span></span> <span data-ttu-id="be9f3-122">Для двоичных данных укажите длину в байтах, а для строковых данных укажите длину в символах.</span><span class="sxs-lookup"><span data-stu-id="be9f3-122">For binary data, specify the length in bytes and for string data, specify the length in characters.</span></span> <span data-ttu-id="be9f3-123">Можно указать фактическую длину или имя другого элемента данных, который содержит длину.</span><span class="sxs-lookup"><span data-stu-id="be9f3-123">You can specify the actual length or the name of another data item that contains the length.</span></span><br/> <span data-ttu-id="be9f3-124">Если для указания строки фиксированной длины используется атрибут Length, необходимо заполнить строку фиксированной длиной, допуская символ-признак конца строки в конце (например, если длина равна 5, строка &quot; ABC &quot; должна быть дополнена значением &quot; ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="be9f3-124">If you use the length attribute to specify a fixed length string, you must pad the string to its fixed length allowing for the null-terminator character at the end (for example, if the length is 5, the string &quot;abc&quot; must be padded as &quot;abc &quot;.</span></span> <span data-ttu-id="be9f3-125">Длина строки должна включать символ конца null.</span><span class="sxs-lookup"><span data-stu-id="be9f3-125">The string length must include the null-terminator character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be9f3-126">карта</span><span class="sxs-lookup"><span data-stu-id="be9f3-126">map</span></span></td>
<td><span data-ttu-id="be9f3-127">строка</span><span class="sxs-lookup"><span data-stu-id="be9f3-127">string</span></span></td>
<td><span data-ttu-id="be9f3-128">Имя соответствия "имя-значение", используемое для отображения целочисленных значений в строках.</span><span class="sxs-lookup"><span data-stu-id="be9f3-128">The name of the name/value map to use to map integer values to strings.</span></span> <span data-ttu-id="be9f3-129">Тип данных элемента данных должен быть одного из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="be9f3-129">The data type of the data item must be of one of the following types:</span></span><br/>
<ul>
<li><span data-ttu-id="be9f3-130">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="be9f3-130">win:UInt8</span></span></li>
<li><span data-ttu-id="be9f3-131">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="be9f3-131">win:UInt16</span></span></li>
<li><span data-ttu-id="be9f3-132">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="be9f3-132">win:UInt32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be9f3-133">name</span><span class="sxs-lookup"><span data-stu-id="be9f3-133">name</span></span></td>
<td><span data-ttu-id="be9f3-134">строка</span><span class="sxs-lookup"><span data-stu-id="be9f3-134">string</span></span></td>
<td><span data-ttu-id="be9f3-135">Имя элемента данных.</span><span class="sxs-lookup"><span data-stu-id="be9f3-135">The name of the data item.</span></span> <span data-ttu-id="be9f3-136">Имя можно использовать для ссылки на этот элемент данных в фрагменте XML, если в шаблоне указан раздел <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="be9f3-136">You can use the name to reference this data item in your XML fragment if you specify a <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> section in your template.</span></span> <span data-ttu-id="be9f3-137">Вы также можете ссылаться на это имя в атрибуте length или Count другого элемента данных, если этот элемент данных содержит его длину или значение Count.</span><span class="sxs-lookup"><span data-stu-id="be9f3-137">You can also reference this name in a length or count attribute of another data item if this data item contains its length or count value.</span></span><br/> <span data-ttu-id="be9f3-138"><strong>Windows Vista:</strong> Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="be9f3-138"><strong>Windows Vista:</strong> This attribute is optional.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be9f3-139">Тип</span><span class="sxs-lookup"><span data-stu-id="be9f3-139">outType</span></span></td>
<td><span data-ttu-id="be9f3-140"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="be9f3-140"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="be9f3-141">Тип данных, используемый при отрисовке этого элемента данных.</span><span class="sxs-lookup"><span data-stu-id="be9f3-141">The data type to use when rendering this data item.</span></span> <span data-ttu-id="be9f3-142">Список предопределенных типов выходных данных см. в описании сложного типа <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="be9f3-142">For a list of predefined output data types, see the <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> complex type.</span></span><br/> <span data-ttu-id="be9f3-143"><strong>Windows Vista:</strong> Тип выходных данных игнорируется, и служба определяет тип на основе входного типа.</span><span class="sxs-lookup"><span data-stu-id="be9f3-143"><strong>Windows Vista:</strong> The output type is ignored, and the service determines the type based on the input type.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="be9f3-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be9f3-144">Remarks</span></span>

<span data-ttu-id="be9f3-145">Для входных типов переменной длины, таких как двоичные BLOB-объекты, необходимо использовать атрибут length для явного указания размера данных.</span><span class="sxs-lookup"><span data-stu-id="be9f3-145">For variable length input types, such as binary blobs, you must use the length attribute to explicitly specify the size of the data.</span></span> <span data-ttu-id="be9f3-146">Для строк укажите атрибут Length, только если строки имеют фиксированную длину.</span><span class="sxs-lookup"><span data-stu-id="be9f3-146">For strings, specify the length attribute only if the strings are of a fixed length.</span></span>

## <a name="examples"></a><span data-ttu-id="be9f3-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="be9f3-147">Examples</span></span>

<span data-ttu-id="be9f3-148">Ниже приведено несколько примеров определений элементов данных.</span><span class="sxs-lookup"><span data-stu-id="be9f3-148">The following are a few examples of the data item definitions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="be9f3-149">Требования</span><span class="sxs-lookup"><span data-stu-id="be9f3-149">Requirements</span></span>



| <span data-ttu-id="be9f3-150">Требование</span><span class="sxs-lookup"><span data-stu-id="be9f3-150">Requirement</span></span> | <span data-ttu-id="be9f3-151">Значение</span><span class="sxs-lookup"><span data-stu-id="be9f3-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="be9f3-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be9f3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="be9f3-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be9f3-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="be9f3-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be9f3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="be9f3-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be9f3-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





