---
description: Необязательный <property> элемент указывает свойства, используемые поставщиком расположения.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Элемент Property элемента Локатионпровидер (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105703623"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a><span data-ttu-id="496a9-103">Элемент Property элемента Локатионпровидер (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="496a9-103">property Element of locationProvider (Search Connector Schema)</span></span>

<span data-ttu-id="496a9-104">Необязательный <property> элемент указывает свойства, используемые поставщиком расположения.</span><span class="sxs-lookup"><span data-stu-id="496a9-104">The optional <property> element specifies the properties used by the location provider.</span></span> <span data-ttu-id="496a9-105">Эти свойства относятся к этому поставщику расположения, поэтому нет предопределенного набора имен для использования.</span><span class="sxs-lookup"><span data-stu-id="496a9-105">These properties are specific to this location provider, so there is no predefined set of names to use.</span></span> <span data-ttu-id="496a9-106"><property>Элемент имеет два атрибута, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="496a9-106">The <property> element has two attributes, as described in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="496a9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="496a9-107">Syntax</span></span>


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><span data-ttu-id="496a9-108"><property> Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="496a9-108"><property> Element Information</span></span>



| <span data-ttu-id="496a9-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="496a9-109">Parent Element</span></span>                                                                                 | <span data-ttu-id="496a9-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="496a9-110">Child Elements</span></span>                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="496a9-111">Элемент Локатионпровидер (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="496a9-111">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | <span data-ttu-id="496a9-112">, описанного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="496a9-112">property, described in this topic.</span></span> |



 


## <a name="property-attributes"></a><span data-ttu-id="496a9-113"><property> Атрибута</span><span class="sxs-lookup"><span data-stu-id="496a9-113"><property> Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="496a9-114">attribute</span><span class="sxs-lookup"><span data-stu-id="496a9-114">Attribute</span></span></th>
<th><span data-ttu-id="496a9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="496a9-115">Description</span></span></th>
<th><span data-ttu-id="496a9-116">Значения</span><span class="sxs-lookup"><span data-stu-id="496a9-116">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="496a9-117">name</span><span class="sxs-lookup"><span data-stu-id="496a9-117">name</span></span></td>
<td><span data-ttu-id="496a9-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="496a9-118">Required.</span></span> <span data-ttu-id="496a9-119">Отображаемое имя свойства.</span><span class="sxs-lookup"><span data-stu-id="496a9-119">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="496a9-120">тип</span><span class="sxs-lookup"><span data-stu-id="496a9-120">type</span></span></td>
<td><span data-ttu-id="496a9-121">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="496a9-121">Required.</span></span> <span data-ttu-id="496a9-122">Тип свойства.</span><span class="sxs-lookup"><span data-stu-id="496a9-122">The type of property.</span></span></td>
<td><span data-ttu-id="496a9-123">Any: по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="496a9-123">Any: Default.</span></span> <span data-ttu-id="496a9-124">Значение не будет приведено подсистемой свойств.</span><span class="sxs-lookup"><span data-stu-id="496a9-124">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="496a9-125">VT_NULL будет возвращено функцией Жетпропертитипе.</span><span class="sxs-lookup"><span data-stu-id="496a9-125">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="496a9-126">NULL: значение для этого свойства отсутствует.</span><span class="sxs-lookup"><span data-stu-id="496a9-126">Null: There is no value for this property.</span></span> <span data-ttu-id="496a9-127">VT_NULL будет возвращено функцией Жетпропертитипе.</span><span class="sxs-lookup"><span data-stu-id="496a9-127">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="496a9-128">Строка: значение должно быть VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="496a9-128">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="496a9-129">Boolean: значение должно быть VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="496a9-129">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="496a9-130">Byte: значение должно быть VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="496a9-130">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="496a9-131">Buffer: значение должно быть VT_UI1ом | VT_VECTOR буфер байтов.</span><span class="sxs-lookup"><span data-stu-id="496a9-131">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="496a9-132">Int16: значение должно быть VT_I2.</span><span class="sxs-lookup"><span data-stu-id="496a9-132">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="496a9-133">UInt16: значение должно быть VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="496a9-133">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="496a9-134">Int32: значение должно быть VT_I4.</span><span class="sxs-lookup"><span data-stu-id="496a9-134">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="496a9-135">UInt32: значение должно быть VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="496a9-135">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="496a9-136">Int64: значение должно быть VT_I8.</span><span class="sxs-lookup"><span data-stu-id="496a9-136">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="496a9-137">UInt64: значение должно быть VT_UI8</span><span class="sxs-lookup"><span data-stu-id="496a9-137">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="496a9-138">Double: значение должно быть VT_R8.</span><span class="sxs-lookup"><span data-stu-id="496a9-138">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="496a9-139">DateTime: значение должно быть VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="496a9-139">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="496a9-140">GUID: значение должно быть VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="496a9-140">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="496a9-141">BLOB-объект. значение должно быть VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="496a9-141">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="496a9-142">Объект: значение должно быть VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="496a9-142">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="496a9-143">Stream: значение должно быть VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="496a9-143">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="496a9-144">Буфер обмена. значение должно быть VT_CF.</span><span class="sxs-lookup"><span data-stu-id="496a9-144">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="496a9-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="496a9-145">Remarks</span></span>

<span data-ttu-id="496a9-146">Для поставщика OpenSearch используются следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="496a9-146">For the OpenSearch provider, the following properties are used:</span></span>

-   <span data-ttu-id="496a9-147">Опенсеарчшортнаме: короткое имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="496a9-147">OpenSearchShortName: Short name of the search service</span></span>
-   <span data-ttu-id="496a9-148">Опенсеарчкуеритемплате: шаблон, отформатированный согласно соглашению о шаблоне OpenSearch, для службы запросов</span><span class="sxs-lookup"><span data-stu-id="496a9-148">OpenSearchQueryTemplate: Template, formatted following the OpenSearch template convention, for the query service</span></span>
-   <span data-ttu-id="496a9-149">Максимумресулткаунт: (число) максимальное число результатов, возвращенных службой поиска</span><span class="sxs-lookup"><span data-stu-id="496a9-149">MaximumResultCount: (number) Maximum number of results returned by the search service</span></span>
-   <span data-ttu-id="496a9-150">Линкисфилепас: (Boolean) Если значение true, поставщик пытается интерпретировать возвращенные элементы как файлы, используя их расширения для создания соответствующего Шеллитем в представлении.</span><span class="sxs-lookup"><span data-stu-id="496a9-150">LinkIsFilePath: (Boolean) If true, the provider tries to interpret returned items as files, using their extensions to create the proper ShellItem in the view.</span></span> <span data-ttu-id="496a9-151">Если значение равно false, элементы обрабатываются как ярлыки URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="496a9-151">If false, items are treated as URL shortcuts.</span></span>

 

 



