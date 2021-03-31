---
title: Инриббонгаллери, элемент
description: Представляет коллекцию In-Ribbon, элемент управления на основе галереи, который предоставляет подмножество элементов по умолчанию непосредственно на ленте. Все оставшиеся элементы отображаются при нажатии кнопки раскрывающегося меню.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Лента Windows для элемента Инриббонгаллери
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24ecf9a34c74d8b66f838e0e49c815f00c80b89c
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/30/2020
ms.locfileid: "104069731"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="7ed63-105">Инриббонгаллери, элемент</span><span class="sxs-lookup"><span data-stu-id="7ed63-105">InRibbonGallery element</span></span>

<span data-ttu-id="7ed63-106">Представляет [коллекцию на ленте](windowsribbon-controls-inribbongallery.md), элемент управления на основе галереи, который предоставляет подмножество элементов по умолчанию непосредственно на ленте.</span><span class="sxs-lookup"><span data-stu-id="7ed63-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="7ed63-107">Все оставшиеся элементы отображаются при нажатии кнопки раскрывающегося меню.</span><span class="sxs-lookup"><span data-stu-id="7ed63-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="7ed63-108">Использование</span><span class="sxs-lookup"><span data-stu-id="7ed63-108">Usage</span></span>

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
```

## <a name="attributes"></a><span data-ttu-id="7ed63-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7ed63-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ed63-110">attribute</span><span class="sxs-lookup"><span data-stu-id="7ed63-110">Attribute</span></span></th>
<th><span data-ttu-id="7ed63-111">Тип</span><span class="sxs-lookup"><span data-stu-id="7ed63-111">Type</span></span></th>
<th><span data-ttu-id="7ed63-112">Обязательно</span><span class="sxs-lookup"><span data-stu-id="7ed63-112">Required</span></span></th>
<th><span data-ttu-id="7ed63-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7ed63-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ed63-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-115">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="7ed63-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="7ed63-116">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-116">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-117">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7ed63-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="7ed63-118">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="7ed63-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="7ed63-119">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="7ed63-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="7ed63-120">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="7ed63-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="7ed63-121">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="7ed63-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ed63-122"><strong>хасларжеитемс</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-123">Логическое</span><span class="sxs-lookup"><span data-stu-id="7ed63-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="7ed63-124">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-124">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-125">Определяет, отображается ли в элементе управления галереи большой или маленький ресурс изображения команды.</span><span class="sxs-lookup"><span data-stu-id="7ed63-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ed63-126">Применяется только к коллекциям, в которых значение атрибута <em>Type</em> равно <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="7ed63-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="7ed63-127">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="7ed63-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="7ed63-128">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="7ed63-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7ed63-129">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ed63-129">Default.</span></span> <br/> </dd> <span data-ttu-id="7ed63-130"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="7ed63-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ed63-131"><strong>итемхеигхт</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ed63-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7ed63-133">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-133">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-134">Вместе с <em>итемвидс</em>определяет размер изображения элемента, отображаемого в элементе управления галереи.</span><span class="sxs-lookup"><span data-stu-id="7ed63-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ed63-135">Применяется только к коллекциям, в которых значение атрибута <em>Type</em> равно</span><span class="sxs-lookup"><span data-stu-id="7ed63-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="7ed63-136">.</span><span class="sxs-lookup"><span data-stu-id="7ed63-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="7ed63-137">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="7ed63-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="7ed63-138">Значение по умолчанию — -1.</span><span class="sxs-lookup"><span data-stu-id="7ed63-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ed63-139"><strong>итемвидс</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ed63-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7ed63-141">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-141">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-142">Вместе с <em>итемхеигхт</em>определяет размер изображения элемента, отображаемого в элементе управления галереи.</span><span class="sxs-lookup"><span data-stu-id="7ed63-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ed63-143">Применяется только к коллекциям, в которых значение атрибута <em>Type</em> равно</span><span class="sxs-lookup"><span data-stu-id="7ed63-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="7ed63-144">.</span><span class="sxs-lookup"><span data-stu-id="7ed63-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="7ed63-145">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="7ed63-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="7ed63-146">Значение по умолчанию — -1.</span><span class="sxs-lookup"><span data-stu-id="7ed63-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ed63-147"><strong>максколумнс</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ed63-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7ed63-149">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-149">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-150">Указывает максимальное число столбцов, которые отображаются в <strong>инриббонгаллери</strong> , например в раскрывающемся списке <em>крупной</em> группы.</span><span class="sxs-lookup"><span data-stu-id="7ed63-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="7ed63-151">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="7ed63-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ed63-152"><strong>максколумнсмедиум</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ed63-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7ed63-154">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-154">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-155">Указывает максимальное число столбцов, которое <strong>инриббонгаллери</strong> отображается в макете группы <em>средних</em> , перед переключением на <em>крупный</em> макет.</span><span class="sxs-lookup"><span data-stu-id="7ed63-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="7ed63-156">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="7ed63-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ed63-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ed63-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7ed63-159">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-159">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-160">Указывает максимальное количество строк для макета элементов <strong>инриббонгаллери</strong> .</span><span class="sxs-lookup"><span data-stu-id="7ed63-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="7ed63-161">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="7ed63-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="7ed63-162">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="7ed63-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ed63-163"><strong>минколумнсларже</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ed63-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7ed63-165">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-165">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-166">Указывает минимальное число столбцов, отображаемых <strong>инриббонгаллери</strong> в макете <em>большой</em> группы перед переключением на <em>средний</em>.</span><span class="sxs-lookup"><span data-stu-id="7ed63-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="7ed63-167">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="7ed63-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ed63-168"><strong>минколумнсмедиум</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ed63-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7ed63-170">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-170">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-171">Указывает минимальное число столбцов, которое <strong>инриббонгаллери</strong> отображается в макете группы <em>средних</em> , перед переключением на <em>малый</em>.</span><span class="sxs-lookup"><span data-stu-id="7ed63-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="7ed63-172">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="7ed63-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ed63-173"><strong>текстпоситион</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-174">текстпоситионтипе</span><span class="sxs-lookup"><span data-stu-id="7ed63-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="7ed63-175">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-175">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-176">Указывает, где отображается метка элемента относительно изображения.</span><span class="sxs-lookup"><span data-stu-id="7ed63-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="7ed63-177">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7ed63-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="7ed63-178">
<dt><span></span><span></span><strong></strong> Нижний</span><span class="sxs-lookup"><span data-stu-id="7ed63-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7ed63-179"><dt><span></span><span></span><strong></strong> Ыть</span><span class="sxs-lookup"><span data-stu-id="7ed63-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7ed63-180"><dt><span></span><span></span><strong></strong> Слева</span><span class="sxs-lookup"><span data-stu-id="7ed63-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7ed63-181"><dt><span></span><span></span><strong></strong> Крывает</span><span class="sxs-lookup"><span data-stu-id="7ed63-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7ed63-182"><dt><span></span><span></span><strong></strong> Справа</span><span class="sxs-lookup"><span data-stu-id="7ed63-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7ed63-183"><dt><span></span><span></span><strong></strong> Лучшая</span><span class="sxs-lookup"><span data-stu-id="7ed63-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ed63-184"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="7ed63-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="7ed63-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="7ed63-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="7ed63-186">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-186">No</span></span><br/></td>
<td><span data-ttu-id="7ed63-187">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7ed63-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="7ed63-188">
<dt><span></span><span></span><strong></strong> Файлов</span><span class="sxs-lookup"><span data-stu-id="7ed63-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7ed63-189"><dt><span></span><span></span><strong></strong> Меню</span><span class="sxs-lookup"><span data-stu-id="7ed63-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="7ed63-190">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7ed63-190">Child elements</span></span>



| <span data-ttu-id="7ed63-191">Элемент</span><span class="sxs-lookup"><span data-stu-id="7ed63-191">Element</span></span>                                                                                           | <span data-ttu-id="7ed63-192">Описание</span><span class="sxs-lookup"><span data-stu-id="7ed63-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7ed63-193">**Установка**</span><span class="sxs-lookup"><span data-stu-id="7ed63-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="7ed63-194">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="7ed63-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="7ed63-195">**Инриббонгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="7ed63-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="7ed63-196">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="7ed63-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="7ed63-197">**Инриббонгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="7ed63-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="7ed63-198">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="7ed63-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="7ed63-199">**Переключатель**</span><span class="sxs-lookup"><span data-stu-id="7ed63-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="7ed63-200">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="7ed63-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="7ed63-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="7ed63-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="7ed63-202">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="7ed63-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="7ed63-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="7ed63-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="7ed63-204">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="7ed63-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7ed63-205">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7ed63-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ed63-206">Элемент</span><span class="sxs-lookup"><span data-stu-id="7ed63-206">Element</span></span></th>
<th><span data-ttu-id="7ed63-207">Описание</span><span class="sxs-lookup"><span data-stu-id="7ed63-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ed63-208"><a href="windowsribbon-element-controlgroup.md"><strong>контролграуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ed63-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7ed63-209"><a href="windowsribbon-element-group.md"><strong>Группа</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ed63-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7ed63-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Куиккакцесстулбар. Аппликатиондефаултс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ed63-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="7ed63-211">Windows 8 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="7ed63-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="7ed63-212">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ed63-212">Remarks</span></span>

<span data-ttu-id="7ed63-213">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7ed63-213">Optional.</span></span>

<span data-ttu-id="7ed63-214">Может встречаться не более одного раза для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md) или [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="7ed63-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="7ed63-215">На следующем снимке экрана показана лента в элементе управления " [Коллекция ленты](windowsribbon-controls-inribbongallery.md) " в Microsoft Paint для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7ed63-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![снимок экрана: элемент управления "Коллекция на ленте" на ленте Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="7ed63-217">Примеры</span><span class="sxs-lookup"><span data-stu-id="7ed63-217">Examples</span></span>

<span data-ttu-id="7ed63-218">В следующем примере показана базовая разметка для [коллекции на ленте](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="7ed63-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="7ed63-219">В этом разделе кода показаны объявления команд **инриббонгаллери** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **инриббонгаллери** .</span><span class="sxs-lookup"><span data-stu-id="7ed63-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



<span data-ttu-id="7ed63-220">В этом разделе кода показаны объявления элементов управления **инриббонгаллери** .</span><span class="sxs-lookup"><span data-stu-id="7ed63-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="7ed63-221">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7ed63-221">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="7ed63-222">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="7ed63-222">Minimum supported system</span></span><br/> | <span data-ttu-id="7ed63-223">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ed63-223">Windows 7</span></span> |
| <span data-ttu-id="7ed63-224">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="7ed63-224">Can be empty</span></span>                        | <span data-ttu-id="7ed63-225">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed63-225">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="7ed63-226">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ed63-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed63-227">Элемент управления "Коллекция ленты"</span><span class="sxs-lookup"><span data-stu-id="7ed63-227">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="7ed63-228">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="7ed63-228">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="7ed63-229">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="7ed63-229">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





