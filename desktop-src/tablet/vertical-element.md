---
description: Содержит сведения, описывающие вертикальный компонент линий в бланке, который используется в заметке журнала. Используется, например, если в заметке есть линии сетки.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Вертикальный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432126"
---
# <a name="vertical-element"></a><span data-ttu-id="ac5ac-104">Вертикальный элемент</span><span class="sxs-lookup"><span data-stu-id="ac5ac-104">Vertical Element</span></span>

<span data-ttu-id="ac5ac-105">Содержит сведения, описывающие вертикальный компонент линий в бланке, который используется в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="ac5ac-106">Используется, например, если в заметке есть линии сетки.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="ac5ac-107">Определение</span><span class="sxs-lookup"><span data-stu-id="ac5ac-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="ac5ac-108">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ac5ac-108">Parent Elements</span></span>

[<span data-ttu-id="ac5ac-109">**линелайаут**</span><span class="sxs-lookup"><span data-stu-id="ac5ac-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="ac5ac-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ac5ac-110">Child Elements</span></span>

<span data-ttu-id="ac5ac-111">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="ac5ac-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ac5ac-112">Attributes</span></span>



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
<th><span data-ttu-id="ac5ac-113">attribute</span><span class="sxs-lookup"><span data-stu-id="ac5ac-113">Attribute</span></span></th>
<th><span data-ttu-id="ac5ac-114">Тип</span><span class="sxs-lookup"><span data-stu-id="ac5ac-114">Type</span></span></th>
<th><span data-ttu-id="ac5ac-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ac5ac-115">Required</span></span></th>
<th><span data-ttu-id="ac5ac-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ac5ac-116">Description</span></span></th>
<th><span data-ttu-id="ac5ac-117">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ac5ac-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac5ac-118"><strong>Стиль</strong></span><span class="sxs-lookup"><span data-stu-id="ac5ac-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="ac5ac-119"><a href="linelayoutstyletype-simple-type.md"><strong>Линелайаутстилетипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="ac5ac-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="ac5ac-120">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ac5ac-120">Required</span></span></td>
<td><span data-ttu-id="ac5ac-121">Указывает тип рисуемой линии.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="ac5ac-122">Нет</span><span class="sxs-lookup"><span data-stu-id="ac5ac-122">None</span></span></li>
<li><span data-ttu-id="ac5ac-123">Сплошная</span><span class="sxs-lookup"><span data-stu-id="ac5ac-123">Solid</span></span></li>
<li><span data-ttu-id="ac5ac-124">Штрих</span><span class="sxs-lookup"><span data-stu-id="ac5ac-124">Dash</span></span></li>
<li><span data-ttu-id="ac5ac-125">Точки</span><span class="sxs-lookup"><span data-stu-id="ac5ac-125">Dot</span></span></li>
<li><span data-ttu-id="ac5ac-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="ac5ac-126">DashDot</span></span></li>
<li><span data-ttu-id="ac5ac-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="ac5ac-127">DashDotDot</span></span></li>
<li><span data-ttu-id="ac5ac-128">Double</span><span class="sxs-lookup"><span data-stu-id="ac5ac-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac5ac-129"><strong>Цвет</strong></span><span class="sxs-lookup"><span data-stu-id="ac5ac-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="ac5ac-130"><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="ac5ac-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="ac5ac-131">Необязательно</span><span class="sxs-lookup"><span data-stu-id="ac5ac-131">Optional</span></span></td>
<td><span data-ttu-id="ac5ac-132">Цвет элемента.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-132">Color of the element.</span></span></td>
<td><span data-ttu-id="ac5ac-133">Шестнадцатеричное значение RGB.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="ac5ac-134">Соответствует следующему регулярному выражению: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="ac5ac-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="ac5ac-135">Например, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac5ac-136"><strong>спаЦингбефоре</strong></span><span class="sxs-lookup"><span data-stu-id="ac5ac-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="ac5ac-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="ac5ac-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="ac5ac-138">Необязательно</span><span class="sxs-lookup"><span data-stu-id="ac5ac-138">Optional</span></span></td>
<td><span data-ttu-id="ac5ac-139">Отступ перед элементом.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="ac5ac-140">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac5ac-141"><strong>спаЦингбетвин</strong></span><span class="sxs-lookup"><span data-stu-id="ac5ac-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="ac5ac-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="ac5ac-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="ac5ac-143">Необязательно</span><span class="sxs-lookup"><span data-stu-id="ac5ac-143">Optional</span></span></td>
<td><span data-ttu-id="ac5ac-144">Интервал между этим элементом и окружающими его элементами.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="ac5ac-145">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="ac5ac-146">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ac5ac-146">Element Information</span></span>



|  <span data-ttu-id="ac5ac-147">Элемент</span><span class="sxs-lookup"><span data-stu-id="ac5ac-147">Element</span></span>     | <span data-ttu-id="ac5ac-148">Значение</span><span class="sxs-lookup"><span data-stu-id="ac5ac-148">Value</span></span>                                                         |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="ac5ac-149">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ac5ac-149">Element type</span></span> | <span data-ttu-id="ac5ac-150">[**Вертикалтипе**](verticaltype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="ac5ac-150">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ac5ac-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac5ac-151">Namespace</span></span>    | <span data-ttu-id="ac5ac-152">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="ac5ac-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="ac5ac-153">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="ac5ac-153">Schema name</span></span>  | <span data-ttu-id="ac5ac-154">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="ac5ac-154">Journal Reader</span></span>                                                |



 

 

 




