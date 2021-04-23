---
description: Необязательный <property> элемент указывает свойство, используемое соединителем поиска. Эти свойства относятся только к этому соединителю поиска, поэтому предопределенный набор имен для использования отсутствует. У этого элемента нет дочерних элементов.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Элемент Property элемента Пропертисторе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540626"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a><span data-ttu-id="a34ed-105">Элемент Property элемента Пропертисторе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="a34ed-105">property Element of propertyStore (Search Connector Schema)</span></span>

<span data-ttu-id="a34ed-106">Необязательный <property> элемент указывает свойство, используемое соединителем поиска.</span><span class="sxs-lookup"><span data-stu-id="a34ed-106">The optional <property> element specifies a property used by the search connector.</span></span> <span data-ttu-id="a34ed-107">Эти свойства относятся только к этому соединителю поиска, поэтому предопределенный набор имен для использования отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a34ed-107">These properties are specific to this search connector, so there is no predefined set of names to use.</span></span> <span data-ttu-id="a34ed-108">У этого элемента нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="a34ed-108">This element has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a34ed-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a34ed-109">Syntax</span></span>


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="a34ed-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a34ed-110">Element Information</span></span>



| <span data-ttu-id="a34ed-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a34ed-111">Parent Element</span></span>                                                                           | <span data-ttu-id="a34ed-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a34ed-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a34ed-113">Элемент Пропертисторе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="a34ed-113">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a><span data-ttu-id="a34ed-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a34ed-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a34ed-115">Атрибут</span><span class="sxs-lookup"><span data-stu-id="a34ed-115">Attribute</span></span></th>
<th><span data-ttu-id="a34ed-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a34ed-116">Description</span></span></th>
<th><span data-ttu-id="a34ed-117">Значения</span><span class="sxs-lookup"><span data-stu-id="a34ed-117">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a34ed-118">name</span><span class="sxs-lookup"><span data-stu-id="a34ed-118">name</span></span></td>
<td><span data-ttu-id="a34ed-119">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a34ed-119">Public.</span></span> <span data-ttu-id="a34ed-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a34ed-120">Required.</span></span> <span data-ttu-id="a34ed-121">Отображаемое имя свойства.</span><span class="sxs-lookup"><span data-stu-id="a34ed-121">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="a34ed-122">тип</span><span class="sxs-lookup"><span data-stu-id="a34ed-122">type</span></span></td>
<td><span data-ttu-id="a34ed-123">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a34ed-123">Public.</span></span> <span data-ttu-id="a34ed-124">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a34ed-124">Required.</span></span> <span data-ttu-id="a34ed-125">Тип свойства.</span><span class="sxs-lookup"><span data-stu-id="a34ed-125">The type of property.</span></span></td>
<td><span data-ttu-id="a34ed-126">Any: по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a34ed-126">Any: Default.</span></span> <span data-ttu-id="a34ed-127">Значение не будет приведено подсистемой свойств.</span><span class="sxs-lookup"><span data-stu-id="a34ed-127">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="a34ed-128">VT_NULL будет возвращено функцией Жетпропертитипе.</span><span class="sxs-lookup"><span data-stu-id="a34ed-128">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="a34ed-129">NULL: значение для этого свойства отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a34ed-129">Null: There is no value for this property.</span></span> <span data-ttu-id="a34ed-130">VT_NULL будет возвращено функцией Жетпропертитипе.</span><span class="sxs-lookup"><span data-stu-id="a34ed-130">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="a34ed-131">Строка: значение должно быть VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="a34ed-131">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="a34ed-132">Boolean: значение должно быть VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="a34ed-132">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="a34ed-133">Byte: значение должно быть VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="a34ed-133">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="a34ed-134">Buffer: значение должно быть VT_UI1ом | VT_VECTOR буфер байтов.</span><span class="sxs-lookup"><span data-stu-id="a34ed-134">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="a34ed-135">Int16: значение должно быть VT_I2.</span><span class="sxs-lookup"><span data-stu-id="a34ed-135">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="a34ed-136">UInt16: значение должно быть VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="a34ed-136">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="a34ed-137">Int32: значение должно быть VT_I4.</span><span class="sxs-lookup"><span data-stu-id="a34ed-137">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="a34ed-138">UInt32: значение должно быть VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="a34ed-138">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="a34ed-139">Int64: значение должно быть VT_I8.</span><span class="sxs-lookup"><span data-stu-id="a34ed-139">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="a34ed-140">UInt64: значение должно быть VT_UI8</span><span class="sxs-lookup"><span data-stu-id="a34ed-140">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="a34ed-141">Double: значение должно быть VT_R8.</span><span class="sxs-lookup"><span data-stu-id="a34ed-141">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="a34ed-142">DateTime: значение должно быть VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="a34ed-142">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="a34ed-143">GUID: значение должно быть VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="a34ed-143">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="a34ed-144">BLOB-объект. значение должно быть VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="a34ed-144">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="a34ed-145">Объект: значение должно быть VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="a34ed-145">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="a34ed-146">Stream: значение должно быть VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="a34ed-146">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="a34ed-147">Буфер обмена. значение должно быть VT_CF.</span><span class="sxs-lookup"><span data-stu-id="a34ed-147">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a34ed-148">schema</span><span class="sxs-lookup"><span data-stu-id="a34ed-148">schema</span></span></td>
<td><span data-ttu-id="a34ed-149">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a34ed-149">Public.</span></span> <span data-ttu-id="a34ed-150">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a34ed-150">Optional.</span></span> <span data-ttu-id="a34ed-151">Схема, в которой определено свойство.</span><span class="sxs-lookup"><span data-stu-id="a34ed-151">The schema where the property is defined.</span></span></td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a34ed-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a34ed-152">Remarks</span></span>

<span data-ttu-id="a34ed-153">Соединители поиска OpenSearch могут использовать свойство Опенсеарчхтмлролловертемплате.</span><span class="sxs-lookup"><span data-stu-id="a34ed-153">OpenSearch search connectors can use the OpenSearchHTMLRolloverTemplate property.</span></span> <span data-ttu-id="a34ed-154">Это свойство определяет шаблон, отформатированный согласно соглашению о шаблоне OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="a34ed-154">This property identifies a template that is formatted following the OpenSearch template convention.</span></span> <span data-ttu-id="a34ed-155">Шаблон Опенсеарчхтмлролловертемплате используется, когда пользователь нажимает кнопку "Поиск на веб-сайте" на панели команд.</span><span class="sxs-lookup"><span data-stu-id="a34ed-155">The OpenSearchHTMLRolloverTemplate template is used when the user clicks on the "Search on website" button in the command bar.</span></span>

## <a name="example"></a><span data-ttu-id="a34ed-156">Пример</span><span class="sxs-lookup"><span data-stu-id="a34ed-156">Example</span></span>

<span data-ttu-id="a34ed-157">В следующем примере показан <propertyStore> элемент с двумя <property> элементами.</span><span class="sxs-lookup"><span data-stu-id="a34ed-157">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



