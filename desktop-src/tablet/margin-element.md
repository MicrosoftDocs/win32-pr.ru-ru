---
description: Определяет линии полей, нарисованные на странице.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Элемент Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272625"
---
# <a name="margin-element"></a><span data-ttu-id="9ae41-103">Элемент Margin</span><span class="sxs-lookup"><span data-stu-id="9ae41-103">Margin Element</span></span>

<span data-ttu-id="9ae41-104">Определяет линии полей, нарисованные на странице.</span><span class="sxs-lookup"><span data-stu-id="9ae41-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="9ae41-105">Определение</span><span class="sxs-lookup"><span data-stu-id="9ae41-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="9ae41-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9ae41-106">Parent Elements</span></span>

<span data-ttu-id="9ae41-107">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9ae41-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9ae41-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9ae41-108">Child Elements</span></span>

<span data-ttu-id="9ae41-109">Нет..</span><span class="sxs-lookup"><span data-stu-id="9ae41-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="9ae41-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9ae41-110">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ae41-111">attribute</span><span class="sxs-lookup"><span data-stu-id="9ae41-111">Attribute</span></span></th>
<th><span data-ttu-id="9ae41-112">Тип</span><span class="sxs-lookup"><span data-stu-id="9ae41-112">Type</span></span></th>
<th><span data-ttu-id="9ae41-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="9ae41-113">Required</span></span></th>
<th><span data-ttu-id="9ae41-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9ae41-114">Description</span></span></th>
<th><span data-ttu-id="9ae41-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="9ae41-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ae41-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="9ae41-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="9ae41-117"><a href="linelayoutstyletype-simple-type.md"><strong>Линелайаутстилетипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="9ae41-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="9ae41-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="9ae41-118">Required</span></span></td>
<td><span data-ttu-id="9ae41-119">Указывает тип рисуемой линии.</span><span class="sxs-lookup"><span data-stu-id="9ae41-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="9ae41-120">Нет</span><span class="sxs-lookup"><span data-stu-id="9ae41-120">None</span></span></li>
<li><span data-ttu-id="9ae41-121">Сплошная</span><span class="sxs-lookup"><span data-stu-id="9ae41-121">Solid</span></span></li>
<li><span data-ttu-id="9ae41-122">Штрих</span><span class="sxs-lookup"><span data-stu-id="9ae41-122">Dash</span></span></li>
<li><span data-ttu-id="9ae41-123">Точки</span><span class="sxs-lookup"><span data-stu-id="9ae41-123">Dot</span></span></li>
<li><span data-ttu-id="9ae41-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="9ae41-124">DashDot</span></span></li>
<li><span data-ttu-id="9ae41-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="9ae41-125">DashDotDot</span></span></li>
<li><span data-ttu-id="9ae41-126">Double</span><span class="sxs-lookup"><span data-stu-id="9ae41-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ae41-127"><strong>Цвет</strong></span><span class="sxs-lookup"><span data-stu-id="9ae41-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="9ae41-128"><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="9ae41-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="9ae41-129">Необязательно</span><span class="sxs-lookup"><span data-stu-id="9ae41-129">Optional</span></span></td>
<td><span data-ttu-id="9ae41-130">Цвет элемента.</span><span class="sxs-lookup"><span data-stu-id="9ae41-130">Color of the element.</span></span></td>
<td><span data-ttu-id="9ae41-131">Шестнадцатеричное значение RGB.</span><span class="sxs-lookup"><span data-stu-id="9ae41-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="9ae41-132">Соответствует следующему регулярному выражению: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="9ae41-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="9ae41-133">Например, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="9ae41-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ae41-134"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="9ae41-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="9ae41-135"><a href="margintypetype-simple-type.md"><strong>Маргинтипетипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="9ae41-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="9ae41-136">Необязательно</span><span class="sxs-lookup"><span data-stu-id="9ae41-136">Optional</span></span></td>
<td><span data-ttu-id="9ae41-137">Показывает левое или правое поле.</span><span class="sxs-lookup"><span data-stu-id="9ae41-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="9ae41-138">Левый</span><span class="sxs-lookup"><span data-stu-id="9ae41-138">Left</span></span></li>
<li><span data-ttu-id="9ae41-139">Правый</span><span class="sxs-lookup"><span data-stu-id="9ae41-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ae41-140"><strong>Интервал</strong></span><span class="sxs-lookup"><span data-stu-id="9ae41-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="9ae41-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="9ae41-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="9ae41-142">Необязательно</span><span class="sxs-lookup"><span data-stu-id="9ae41-142">Optional</span></span></td>
<td><span data-ttu-id="9ae41-143">Интервал между границами страницы и поля.</span><span class="sxs-lookup"><span data-stu-id="9ae41-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="9ae41-144">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="9ae41-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="9ae41-145">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9ae41-145">Element Information</span></span>



|              |                                                           |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="9ae41-146">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="9ae41-146">Element type</span></span> | <span data-ttu-id="9ae41-147">[**Маргинтипе**](margintype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="9ae41-147">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="9ae41-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ae41-148">Namespace</span></span>    | <span data-ttu-id="9ae41-149">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="9ae41-149">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="9ae41-150">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="9ae41-150">Schema name</span></span>  | <span data-ttu-id="9ae41-151">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="9ae41-151">Journal Reader</span></span>                                            |



 

 

 




