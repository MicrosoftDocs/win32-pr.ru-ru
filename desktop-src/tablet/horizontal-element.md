---
description: Содержит сведения о форматировании горизонтальных линий, используемых для бланков в заметке журнала.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Горизонтальный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432384"
---
# <a name="horizontal-element"></a><span data-ttu-id="623cb-103">Горизонтальный элемент</span><span class="sxs-lookup"><span data-stu-id="623cb-103">Horizontal Element</span></span>

<span data-ttu-id="623cb-104">Содержит сведения о форматировании горизонтальных линий, используемых для бланков в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="623cb-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="623cb-105">Определение</span><span class="sxs-lookup"><span data-stu-id="623cb-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="623cb-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="623cb-106">Parent Elements</span></span>

[<span data-ttu-id="623cb-107">**линелайаут**</span><span class="sxs-lookup"><span data-stu-id="623cb-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="623cb-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="623cb-108">Child Elements</span></span>

<span data-ttu-id="623cb-109">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="623cb-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="623cb-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="623cb-110">Attributes</span></span>



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
<th><span data-ttu-id="623cb-111">attribute</span><span class="sxs-lookup"><span data-stu-id="623cb-111">Attribute</span></span></th>
<th><span data-ttu-id="623cb-112">Тип</span><span class="sxs-lookup"><span data-stu-id="623cb-112">Type</span></span></th>
<th><span data-ttu-id="623cb-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="623cb-113">Required</span></span></th>
<th><span data-ttu-id="623cb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="623cb-114">Description</span></span></th>
<th><span data-ttu-id="623cb-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="623cb-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="623cb-116"><strong>Стиль</strong></span><span class="sxs-lookup"><span data-stu-id="623cb-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="623cb-117"><a href="linelayoutstyletype-simple-type.md"><strong>Линелайаутстилетипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="623cb-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="623cb-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="623cb-118">Required</span></span></td>
<td><span data-ttu-id="623cb-119">Указывает тип рисуемой линии.</span><span class="sxs-lookup"><span data-stu-id="623cb-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="623cb-120">Нет</span><span class="sxs-lookup"><span data-stu-id="623cb-120">None</span></span></li>
<li><span data-ttu-id="623cb-121">Сплошная</span><span class="sxs-lookup"><span data-stu-id="623cb-121">Solid</span></span></li>
<li><span data-ttu-id="623cb-122">Штрих</span><span class="sxs-lookup"><span data-stu-id="623cb-122">Dash</span></span></li>
<li><span data-ttu-id="623cb-123">Точки</span><span class="sxs-lookup"><span data-stu-id="623cb-123">Dot</span></span></li>
<li><span data-ttu-id="623cb-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="623cb-124">DashDot</span></span></li>
<li><span data-ttu-id="623cb-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="623cb-125">DashDotDot</span></span></li>
<li><span data-ttu-id="623cb-126">Double</span><span class="sxs-lookup"><span data-stu-id="623cb-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623cb-127"><strong>Цвет</strong></span><span class="sxs-lookup"><span data-stu-id="623cb-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="623cb-128"><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="623cb-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="623cb-129">Необязательно</span><span class="sxs-lookup"><span data-stu-id="623cb-129">Optional</span></span></td>
<td><span data-ttu-id="623cb-130">Цвет элемента.</span><span class="sxs-lookup"><span data-stu-id="623cb-130">Color of the element.</span></span></td>
<td><span data-ttu-id="623cb-131">Шестнадцатеричное значение RGB.</span><span class="sxs-lookup"><span data-stu-id="623cb-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="623cb-132">Соответствует следующему регулярному выражению: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="623cb-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="623cb-133">Например, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="623cb-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623cb-134"><strong>спаЦингбефоре</strong></span><span class="sxs-lookup"><span data-stu-id="623cb-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="623cb-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="623cb-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="623cb-136">Необязательно</span><span class="sxs-lookup"><span data-stu-id="623cb-136">Optional</span></span></td>
<td><span data-ttu-id="623cb-137">Отступ перед элементом.</span><span class="sxs-lookup"><span data-stu-id="623cb-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="623cb-138">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="623cb-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623cb-139"><strong>спаЦингбетвин</strong></span><span class="sxs-lookup"><span data-stu-id="623cb-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="623cb-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="623cb-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="623cb-141">Необязательно</span><span class="sxs-lookup"><span data-stu-id="623cb-141">Optional</span></span></td>
<td><span data-ttu-id="623cb-142">Интервал между этим элементом и окружающими его элементами.</span><span class="sxs-lookup"><span data-stu-id="623cb-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="623cb-143">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="623cb-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="623cb-144">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="623cb-144">Element Information</span></span>



|  <span data-ttu-id="623cb-145">Элемент</span><span class="sxs-lookup"><span data-stu-id="623cb-145">Element</span></span>     | <span data-ttu-id="623cb-146">Значение</span><span class="sxs-lookup"><span data-stu-id="623cb-146">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="623cb-147">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="623cb-147">Element type</span></span> | [<span data-ttu-id="623cb-148">**Хоризонталтипе complexType**</span><span class="sxs-lookup"><span data-stu-id="623cb-148">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="623cb-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="623cb-149">Namespace</span></span>    | <span data-ttu-id="623cb-150">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="623cb-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="623cb-151">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="623cb-151">Schema name</span></span>  | <span data-ttu-id="623cb-152">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="623cb-152">Journal Reader</span></span>                                                    |



 

 

 




