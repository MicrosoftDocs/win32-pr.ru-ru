---
description: Содержит сведения, описывающие вертикальный компонент линий в бланке, который используется в заметке журнала. Используется, например, если в заметке есть линии сетки.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Вертикальный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191a9c5cb3190cff9b1e379a68dbfab49ddc25a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343272"
---
# <a name="vertical-element"></a><span data-ttu-id="95860-104">Вертикальный элемент</span><span class="sxs-lookup"><span data-stu-id="95860-104">Vertical Element</span></span>

<span data-ttu-id="95860-105">Содержит сведения, описывающие вертикальный компонент линий в бланке, который используется в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="95860-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="95860-106">Используется, например, если в заметке есть линии сетки.</span><span class="sxs-lookup"><span data-stu-id="95860-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="95860-107">Определение</span><span class="sxs-lookup"><span data-stu-id="95860-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="95860-108">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="95860-108">Parent Elements</span></span>

[<span data-ttu-id="95860-109">**линелайаут**</span><span class="sxs-lookup"><span data-stu-id="95860-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="95860-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="95860-110">Child Elements</span></span>

<span data-ttu-id="95860-111">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="95860-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="95860-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="95860-112">Attributes</span></span>



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
<th><span data-ttu-id="95860-113">attribute</span><span class="sxs-lookup"><span data-stu-id="95860-113">Attribute</span></span></th>
<th><span data-ttu-id="95860-114">Тип</span><span class="sxs-lookup"><span data-stu-id="95860-114">Type</span></span></th>
<th><span data-ttu-id="95860-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="95860-115">Required</span></span></th>
<th><span data-ttu-id="95860-116">Описание</span><span class="sxs-lookup"><span data-stu-id="95860-116">Description</span></span></th>
<th><span data-ttu-id="95860-117">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="95860-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95860-118"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="95860-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="95860-119"><a href="linelayoutstyletype-simple-type.md"><strong>Линелайаутстилетипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="95860-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="95860-120">Обязательно</span><span class="sxs-lookup"><span data-stu-id="95860-120">Required</span></span></td>
<td><span data-ttu-id="95860-121">Указывает тип рисуемой линии.</span><span class="sxs-lookup"><span data-stu-id="95860-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="95860-122">Нет</span><span class="sxs-lookup"><span data-stu-id="95860-122">None</span></span></li>
<li><span data-ttu-id="95860-123">Сплошная</span><span class="sxs-lookup"><span data-stu-id="95860-123">Solid</span></span></li>
<li><span data-ttu-id="95860-124">Штрих</span><span class="sxs-lookup"><span data-stu-id="95860-124">Dash</span></span></li>
<li><span data-ttu-id="95860-125">Точки</span><span class="sxs-lookup"><span data-stu-id="95860-125">Dot</span></span></li>
<li><span data-ttu-id="95860-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="95860-126">DashDot</span></span></li>
<li><span data-ttu-id="95860-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="95860-127">DashDotDot</span></span></li>
<li><span data-ttu-id="95860-128">Double</span><span class="sxs-lookup"><span data-stu-id="95860-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95860-129"><strong>Цвет</strong></span><span class="sxs-lookup"><span data-stu-id="95860-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="95860-130"><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="95860-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="95860-131">Необязательно</span><span class="sxs-lookup"><span data-stu-id="95860-131">Optional</span></span></td>
<td><span data-ttu-id="95860-132">Цвет элемента.</span><span class="sxs-lookup"><span data-stu-id="95860-132">Color of the element.</span></span></td>
<td><span data-ttu-id="95860-133">Шестнадцатеричное значение RGB.</span><span class="sxs-lookup"><span data-stu-id="95860-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="95860-134">Соответствует следующему регулярному выражению: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="95860-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="95860-135">Например, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="95860-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95860-136"><strong>спаЦингбефоре</strong></span><span class="sxs-lookup"><span data-stu-id="95860-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="95860-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="95860-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="95860-138">Необязательно</span><span class="sxs-lookup"><span data-stu-id="95860-138">Optional</span></span></td>
<td><span data-ttu-id="95860-139">Отступ перед элементом.</span><span class="sxs-lookup"><span data-stu-id="95860-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="95860-140">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="95860-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95860-141"><strong>спаЦингбетвин</strong></span><span class="sxs-lookup"><span data-stu-id="95860-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="95860-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="95860-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="95860-143">Необязательно</span><span class="sxs-lookup"><span data-stu-id="95860-143">Optional</span></span></td>
<td><span data-ttu-id="95860-144">Интервал между этим элементом и окружающими его элементами.</span><span class="sxs-lookup"><span data-stu-id="95860-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="95860-145">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="95860-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="95860-146">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="95860-146">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="95860-147">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="95860-147">Element type</span></span> | <span data-ttu-id="95860-148">[**Вертикалтипе**](verticaltype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="95860-148">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="95860-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="95860-149">Namespace</span></span>    | <span data-ttu-id="95860-150">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="95860-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="95860-151">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="95860-151">Schema name</span></span>  | <span data-ttu-id="95860-152">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="95860-152">Journal Reader</span></span>                                                |



 

 

 




