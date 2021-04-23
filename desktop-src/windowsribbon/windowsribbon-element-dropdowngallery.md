---
title: Дропдовнгаллери, элемент
description: Представляет Drop-Down элемент управления "Коллекция" с меню на основе галереи.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- Лента Windows для элемента Дропдовнгаллери
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dfc2890e33fa7f5d93919e7361465e163dadcb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533227"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="db508-104">Дропдовнгаллери, элемент</span><span class="sxs-lookup"><span data-stu-id="db508-104">DropDownGallery element</span></span>

<span data-ttu-id="db508-105">Представляет [раскрывающийся список](windowsribbon-controls-dropdowngallery.md) элементов управления галереи с меню на основе галереи.</span><span class="sxs-lookup"><span data-stu-id="db508-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="db508-106">Использование</span><span class="sxs-lookup"><span data-stu-id="db508-106">Usage</span></span>

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
```

## <a name="attributes"></a><span data-ttu-id="db508-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="db508-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db508-108">attribute</span><span class="sxs-lookup"><span data-stu-id="db508-108">Attribute</span></span></th>
<th><span data-ttu-id="db508-109">Тип</span><span class="sxs-lookup"><span data-stu-id="db508-109">Type</span></span></th>
<th><span data-ttu-id="db508-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="db508-110">Required</span></span></th>
<th><span data-ttu-id="db508-111">Описание</span><span class="sxs-lookup"><span data-stu-id="db508-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db508-112"><strong>аппликатионмодес</strong></span><span class="sxs-lookup"><span data-stu-id="db508-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="db508-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="db508-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="db508-114">Нет</span><span class="sxs-lookup"><span data-stu-id="db508-114">No</span></span><br/></td>
<td><span data-ttu-id="db508-115">Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="db508-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="db508-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="db508-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="db508-117">Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="db508-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="db508-118">Пробелы допустимы и пропускаются.</span><span class="sxs-lookup"><span data-stu-id="db508-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="db508-119">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="db508-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db508-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="db508-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="db508-121">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="db508-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="db508-122">Нет</span><span class="sxs-lookup"><span data-stu-id="db508-122">No</span></span><br/></td>
<td><span data-ttu-id="db508-123">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db508-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="db508-124">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="db508-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="db508-125">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="db508-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="db508-126">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="db508-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="db508-127">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="db508-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db508-128"><strong>хасларжеитемс</strong></span><span class="sxs-lookup"><span data-stu-id="db508-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="db508-129">Логическое</span><span class="sxs-lookup"><span data-stu-id="db508-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="db508-130">Нет</span><span class="sxs-lookup"><span data-stu-id="db508-130">No</span></span><br/></td>
<td><span data-ttu-id="db508-131">Определяет, отображается ли в элементе управления галереи большой или маленький ресурс изображения команды.</span><span class="sxs-lookup"><span data-stu-id="db508-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="db508-132">Применяется только к коллекциям, в которых значение атрибута <em>Type</em> равно <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="db508-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="db508-133">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="db508-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="db508-134">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="db508-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="db508-135">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db508-135">Default.</span></span> <br/> </dd> <span data-ttu-id="db508-136"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="db508-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db508-137"><strong>итемхеигхт</strong></span><span class="sxs-lookup"><span data-stu-id="db508-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="db508-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="db508-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="db508-139">Нет</span><span class="sxs-lookup"><span data-stu-id="db508-139">No</span></span><br/></td>
<td><span data-ttu-id="db508-140"><dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="db508-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="db508-141">Значение по умолчанию — -1.</span><span class="sxs-lookup"><span data-stu-id="db508-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db508-142"><strong>итемвидс</strong></span><span class="sxs-lookup"><span data-stu-id="db508-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="db508-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="db508-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="db508-144">Нет</span><span class="sxs-lookup"><span data-stu-id="db508-144">No</span></span><br/></td>
<td><span data-ttu-id="db508-145"><dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="db508-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="db508-146">Значение по умолчанию — -1.</span><span class="sxs-lookup"><span data-stu-id="db508-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db508-147"><strong>текстпоситион</strong></span><span class="sxs-lookup"><span data-stu-id="db508-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="db508-148">текстпоситионтипе</span><span class="sxs-lookup"><span data-stu-id="db508-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="db508-149">Нет</span><span class="sxs-lookup"><span data-stu-id="db508-149">No</span></span><br/></td>
<td><span data-ttu-id="db508-150">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="db508-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="db508-151">
<dt><span></span><span></span><strong></strong> Нижний</span><span class="sxs-lookup"><span data-stu-id="db508-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="db508-152"><dt><span></span><span></span><strong></strong> Ыть</span><span class="sxs-lookup"><span data-stu-id="db508-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="db508-153"><dt><span></span><span></span><strong></strong> Слева</span><span class="sxs-lookup"><span data-stu-id="db508-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="db508-154"><dt><span></span><span></span><strong></strong> Крывает</span><span class="sxs-lookup"><span data-stu-id="db508-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="db508-155"><dt><span></span><span></span><strong></strong> Справа</span><span class="sxs-lookup"><span data-stu-id="db508-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="db508-156"><dt><span></span><span></span><strong></strong> Лучшая</span><span class="sxs-lookup"><span data-stu-id="db508-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db508-157"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="db508-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="db508-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="db508-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="db508-159">Нет</span><span class="sxs-lookup"><span data-stu-id="db508-159">No</span></span><br/></td>
<td><span data-ttu-id="db508-160">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="db508-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="db508-161">
<dt><span></span><span></span><strong></strong> Файлов</span><span class="sxs-lookup"><span data-stu-id="db508-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="db508-162"><dt><span></span><span></span><strong></strong> Меню</span><span class="sxs-lookup"><span data-stu-id="db508-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="db508-163">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="db508-163">Child elements</span></span>



| <span data-ttu-id="db508-164">Элемент</span><span class="sxs-lookup"><span data-stu-id="db508-164">Element</span></span>                                                                                           | <span data-ttu-id="db508-165">Описание</span><span class="sxs-lookup"><span data-stu-id="db508-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="db508-166">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="db508-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="db508-167">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="db508-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="db508-168">**Установка**</span><span class="sxs-lookup"><span data-stu-id="db508-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="db508-169">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="db508-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="db508-170">**Дропдовнгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="db508-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="db508-171">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="db508-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="db508-172">**Дропдовнгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="db508-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="db508-173">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="db508-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="db508-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="db508-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="db508-175">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="db508-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="db508-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="db508-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="db508-177">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="db508-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="db508-178">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="db508-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db508-179">Элемент</span><span class="sxs-lookup"><span data-stu-id="db508-179">Element</span></span></th>
<th><span data-ttu-id="db508-180">Описание</span><span class="sxs-lookup"><span data-stu-id="db508-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db508-181"><a href="windowsribbon-element-controlgroup.md"><strong>контролграуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="db508-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="db508-182"><a href="windowsribbon-element-group.md"><strong>Группа</strong></a></span><span class="sxs-lookup"><span data-stu-id="db508-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="db508-183"><a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="db508-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="db508-184">Если он содержится в <a href="windowsribbon-element-applicationmenu.md"><strong>аппликатионмену</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db508-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="db508-185">Этот элемент поддерживается только на первом уровне и не должен иметь дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="db508-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db508-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Куиккакцесстулбар. Аппликатиондефаултс</strong></a></span><span class="sxs-lookup"><span data-stu-id="db508-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="db508-187">Windows 8 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="db508-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db508-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="db508-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="db508-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db508-189">Remarks</span></span>

<span data-ttu-id="db508-190">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="db508-190">Optional.</span></span>

<span data-ttu-id="db508-191">Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md)или [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="db508-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="db508-192">**Дропдовнгаллери** поддерживает [режимы приложений](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="db508-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="db508-193">На следующем снимке экрана показан [раскрывающийся список](windowsribbon-controls-dropdowngallery.md) элементов управления "Коллекция ленты" в Microsoft Paint для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="db508-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![снимок экрана с раскрывающимся элементом управления галереи в Microsoft Paint для Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="db508-195">Примеры</span><span class="sxs-lookup"><span data-stu-id="db508-195">Examples</span></span>

<span data-ttu-id="db508-196">В следующем примере показана базовая разметка для **дропдовнгаллери**.</span><span class="sxs-lookup"><span data-stu-id="db508-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="db508-197">В этом разделе кода показаны объявления команд **дропдовнгаллери** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **дропдовнгаллери** .</span><span class="sxs-lookup"><span data-stu-id="db508-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



<span data-ttu-id="db508-198">В этом разделе кода показаны объявления элементов управления **дропдовнгаллери** .</span><span class="sxs-lookup"><span data-stu-id="db508-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="db508-199">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="db508-199">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="db508-200">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="db508-200">Minimum supported system</span></span><br/> | <span data-ttu-id="db508-201">Windows 7</span><span class="sxs-lookup"><span data-stu-id="db508-201">Windows 7</span></span> |
| <span data-ttu-id="db508-202">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="db508-202">Can be empty</span></span>                        | <span data-ttu-id="db508-203">Нет</span><span class="sxs-lookup"><span data-stu-id="db508-203">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="db508-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db508-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db508-205">**Элемент управления "раскрывающийся список"**</span><span class="sxs-lookup"><span data-stu-id="db508-205">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="db508-206">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="db508-206">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="db508-207">**сетмодес**</span><span class="sxs-lookup"><span data-stu-id="db508-207">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="db508-208">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="db508-208">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

