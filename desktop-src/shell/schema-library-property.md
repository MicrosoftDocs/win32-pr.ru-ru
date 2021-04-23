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
# <a name="property-element-library-schema"></a><span data-ttu-id="10b56-105">Элемент Property (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="10b56-105">property Element (Library Schema)</span></span>

<span data-ttu-id="10b56-106"><property>Элемент указывает свойство, используемое библиотекой.</span><span class="sxs-lookup"><span data-stu-id="10b56-106">The <property> element specifies a property used by the library.</span></span> <span data-ttu-id="10b56-107">Эти свойства относятся к библиотеке, поэтому нет предопределенного набора имен свойств для использования.</span><span class="sxs-lookup"><span data-stu-id="10b56-107">These properties are specific to the library, so there is no predefined set of property names to use.</span></span> <span data-ttu-id="10b56-108">Этот элемент является необязательным и не имеет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="10b56-108">This element is optional and has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b56-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10b56-109">Syntax</span></span>

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

## <a name="element-information"></a><span data-ttu-id="10b56-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="10b56-110">Element Information</span></span>



| <span data-ttu-id="10b56-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="10b56-111">Parent Element</span></span>                                                             | <span data-ttu-id="10b56-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="10b56-112">Child Elements</span></span> |
|----------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="10b56-113">Элемент Пропертисторе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="10b56-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) | <span data-ttu-id="10b56-114">Нет</span><span class="sxs-lookup"><span data-stu-id="10b56-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="10b56-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="10b56-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10b56-116">Атрибут</span><span class="sxs-lookup"><span data-stu-id="10b56-116">Attribute</span></span></th>
<th><span data-ttu-id="10b56-117">Описание</span><span class="sxs-lookup"><span data-stu-id="10b56-117">Description</span></span></th>
<th><span data-ttu-id="10b56-118">Значения</span><span class="sxs-lookup"><span data-stu-id="10b56-118">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10b56-119">name</span><span class="sxs-lookup"><span data-stu-id="10b56-119">name</span></span></td>
<td><span data-ttu-id="10b56-120">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="10b56-120">Public.</span></span> <span data-ttu-id="10b56-121">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="10b56-121">Required.</span></span> <span data-ttu-id="10b56-122">Отображаемое имя свойства.</span><span class="sxs-lookup"><span data-stu-id="10b56-122">The display name of the property.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="10b56-123">type</span><span class="sxs-lookup"><span data-stu-id="10b56-123">type</span></span></td>
<td><span data-ttu-id="10b56-124">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="10b56-124">Public.</span></span> <span data-ttu-id="10b56-125">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="10b56-125">Required.</span></span> <span data-ttu-id="10b56-126">Тип свойства.</span><span class="sxs-lookup"><span data-stu-id="10b56-126">The type of property.</span></span></td>
<td><ul>
<li><span data-ttu-id="10b56-127">Any: по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10b56-127">Any: Default.</span></span> <span data-ttu-id="10b56-128">Значение не будет приведено подсистемой свойств.</span><span class="sxs-lookup"><span data-stu-id="10b56-128">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="10b56-129">VT_NULL будет возвращено функцией Жетпропертитипе.</span><span class="sxs-lookup"><span data-stu-id="10b56-129">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="10b56-130">NULL: значение для этого свойства отсутствует.</span><span class="sxs-lookup"><span data-stu-id="10b56-130">Null: There is no value for this property.</span></span> <span data-ttu-id="10b56-131">VT_NULL будет возвращено функцией Жетпропертитипе.</span><span class="sxs-lookup"><span data-stu-id="10b56-131">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="10b56-132">Строка: значение должно быть VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="10b56-132">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="10b56-133">Boolean: значение должно быть VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="10b56-133">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="10b56-134">Byte: значение должно быть VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="10b56-134">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="10b56-135">Buffer: значение должно быть VT_UI1ом | VT_VECTOR буфер байтов.</span><span class="sxs-lookup"><span data-stu-id="10b56-135">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="10b56-136">Int16: значение должно быть VT_I2.</span><span class="sxs-lookup"><span data-stu-id="10b56-136">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="10b56-137">UInt16: значение должно быть VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="10b56-137">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="10b56-138">Int32: значение должно быть VT_I4.</span><span class="sxs-lookup"><span data-stu-id="10b56-138">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="10b56-139">UInt32: значение должно быть VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="10b56-139">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="10b56-140">Int64: значение должно быть VT_I8.</span><span class="sxs-lookup"><span data-stu-id="10b56-140">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="10b56-141">UInt64: значение должно быть VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="10b56-141">UInt64: The value must be a VT_UI8.</span></span></li>
<li><span data-ttu-id="10b56-142">Double: значение должно быть VT_R8.</span><span class="sxs-lookup"><span data-stu-id="10b56-142">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="10b56-143">DateTime: значение должно быть VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="10b56-143">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="10b56-144">GUID: значение должно быть VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="10b56-144">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="10b56-145">BLOB-объект. значение должно быть VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="10b56-145">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="10b56-146">Объект: значение должно быть VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="10b56-146">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="10b56-147">Stream: значение должно быть VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="10b56-147">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="10b56-148">Буфер обмена. значение должно быть VT_CF.</span><span class="sxs-lookup"><span data-stu-id="10b56-148">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="10b56-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="10b56-149">Remarks</span></span>

<span data-ttu-id="10b56-150">Требования к элементу <канонического имени> соответствуют требованиям для поиска Windows и системы свойств Windows.</span><span class="sxs-lookup"><span data-stu-id="10b56-150">The requirements for the <canonical-name> element match the requirements for Windows Search and the Windows property system.</span></span> <span data-ttu-id="10b56-151">Строка должна иметь тип канонического типа.</span><span class="sxs-lookup"><span data-stu-id="10b56-151">The string must be of type canonical-type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10b56-152">См. также</span><span class="sxs-lookup"><span data-stu-id="10b56-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10b56-153">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="10b56-153">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="10b56-154">Схемы свойств</span><span class="sxs-lookup"><span data-stu-id="10b56-154">Property Schemas</span></span>](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="10b56-155">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="10b56-155">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
