---
description: Содержит сведения о форматировании горизонтальных линий, используемых для бланков в заметке журнала.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Горизонтальный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810072"
---
# <a name="horizontal-element"></a><span data-ttu-id="4d9c9-103">Горизонтальный элемент</span><span class="sxs-lookup"><span data-stu-id="4d9c9-103">Horizontal Element</span></span>

<span data-ttu-id="4d9c9-104">Содержит сведения о форматировании горизонтальных линий, используемых для бланков в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="4d9c9-105">Определение</span><span class="sxs-lookup"><span data-stu-id="4d9c9-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="4d9c9-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4d9c9-106">Parent Elements</span></span>

[<span data-ttu-id="4d9c9-107">**линелайаут**</span><span class="sxs-lookup"><span data-stu-id="4d9c9-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="4d9c9-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4d9c9-108">Child Elements</span></span>

<span data-ttu-id="4d9c9-109">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="4d9c9-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4d9c9-110">Attributes</span></span>



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
<th><span data-ttu-id="4d9c9-111">attribute</span><span class="sxs-lookup"><span data-stu-id="4d9c9-111">Attribute</span></span></th>
<th><span data-ttu-id="4d9c9-112">Тип</span><span class="sxs-lookup"><span data-stu-id="4d9c9-112">Type</span></span></th>
<th><span data-ttu-id="4d9c9-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4d9c9-113">Required</span></span></th>
<th><span data-ttu-id="4d9c9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4d9c9-114">Description</span></span></th>
<th><span data-ttu-id="4d9c9-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4d9c9-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d9c9-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="4d9c9-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="4d9c9-117"><a href="linelayoutstyletype-simple-type.md"><strong>Линелайаутстилетипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="4d9c9-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="4d9c9-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4d9c9-118">Required</span></span></td>
<td><span data-ttu-id="4d9c9-119">Указывает тип рисуемой линии.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="4d9c9-120">Нет</span><span class="sxs-lookup"><span data-stu-id="4d9c9-120">None</span></span></li>
<li><span data-ttu-id="4d9c9-121">Сплошная</span><span class="sxs-lookup"><span data-stu-id="4d9c9-121">Solid</span></span></li>
<li><span data-ttu-id="4d9c9-122">Штрих</span><span class="sxs-lookup"><span data-stu-id="4d9c9-122">Dash</span></span></li>
<li><span data-ttu-id="4d9c9-123">Точки</span><span class="sxs-lookup"><span data-stu-id="4d9c9-123">Dot</span></span></li>
<li><span data-ttu-id="4d9c9-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="4d9c9-124">DashDot</span></span></li>
<li><span data-ttu-id="4d9c9-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="4d9c9-125">DashDotDot</span></span></li>
<li><span data-ttu-id="4d9c9-126">Double</span><span class="sxs-lookup"><span data-stu-id="4d9c9-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d9c9-127"><strong>Цвет</strong></span><span class="sxs-lookup"><span data-stu-id="4d9c9-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="4d9c9-128"><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="4d9c9-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="4d9c9-129">Необязательно</span><span class="sxs-lookup"><span data-stu-id="4d9c9-129">Optional</span></span></td>
<td><span data-ttu-id="4d9c9-130">Цвет элемента.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-130">Color of the element.</span></span></td>
<td><span data-ttu-id="4d9c9-131">Шестнадцатеричное значение RGB.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="4d9c9-132">Соответствует следующему регулярному выражению: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="4d9c9-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="4d9c9-133">Например, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d9c9-134"><strong>спаЦингбефоре</strong></span><span class="sxs-lookup"><span data-stu-id="4d9c9-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="4d9c9-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="4d9c9-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="4d9c9-136">Необязательно</span><span class="sxs-lookup"><span data-stu-id="4d9c9-136">Optional</span></span></td>
<td><span data-ttu-id="4d9c9-137">Отступ перед элементом.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="4d9c9-138">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d9c9-139"><strong>спаЦингбетвин</strong></span><span class="sxs-lookup"><span data-stu-id="4d9c9-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="4d9c9-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="4d9c9-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="4d9c9-141">Необязательно</span><span class="sxs-lookup"><span data-stu-id="4d9c9-141">Optional</span></span></td>
<td><span data-ttu-id="4d9c9-142">Интервал между этим элементом и окружающими его элементами.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="4d9c9-143">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="4d9c9-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="4d9c9-144">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4d9c9-144">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="4d9c9-145">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="4d9c9-145">Element type</span></span> | [<span data-ttu-id="4d9c9-146">**Хоризонталтипе complexType**</span><span class="sxs-lookup"><span data-stu-id="4d9c9-146">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="4d9c9-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4d9c9-147">Namespace</span></span>    | <span data-ttu-id="4d9c9-148">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="4d9c9-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="4d9c9-149">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="4d9c9-149">Schema name</span></span>  | <span data-ttu-id="4d9c9-150">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="4d9c9-150">Journal Reader</span></span>                                                    |



 

 

 




