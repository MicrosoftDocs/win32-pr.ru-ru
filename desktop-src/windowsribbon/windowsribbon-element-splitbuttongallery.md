---
title: Сплитбуттонгаллери, элемент
description: Представляет элемент управления коллекции разделенных кнопок с раскрывающимся меню на основе галереи.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Лента Windows для элемента Сплитбуттонгаллери
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68e90137325c16af6942f9f3929f8abfdf795660
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488053"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="833b5-104">Сплитбуттонгаллери, элемент</span><span class="sxs-lookup"><span data-stu-id="833b5-104">SplitButtonGallery element</span></span>

<span data-ttu-id="833b5-105">Представляет элемент управления [коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md) с раскрывающимся меню на основе галереи.</span><span class="sxs-lookup"><span data-stu-id="833b5-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="833b5-106">Использование</span><span class="sxs-lookup"><span data-stu-id="833b5-106">Usage</span></span>

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
```

## <a name="attributes"></a><span data-ttu-id="833b5-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="833b5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="833b5-108">attribute</span><span class="sxs-lookup"><span data-stu-id="833b5-108">Attribute</span></span></th>
<th><span data-ttu-id="833b5-109">Тип</span><span class="sxs-lookup"><span data-stu-id="833b5-109">Type</span></span></th>
<th><span data-ttu-id="833b5-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="833b5-110">Required</span></span></th>
<th><span data-ttu-id="833b5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="833b5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="833b5-112"><strong>аппликатионмодес</strong></span><span class="sxs-lookup"><span data-stu-id="833b5-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="833b5-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="833b5-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="833b5-114">Нет</span><span class="sxs-lookup"><span data-stu-id="833b5-114">No</span></span><br/></td>
<td><span data-ttu-id="833b5-115">Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="833b5-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="833b5-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="833b5-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="833b5-117">Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="833b5-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="833b5-118">Пробелы допустимы и пропускаются.</span><span class="sxs-lookup"><span data-stu-id="833b5-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="833b5-119">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="833b5-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="833b5-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="833b5-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="833b5-121">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="833b5-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="833b5-122">Нет</span><span class="sxs-lookup"><span data-stu-id="833b5-122">No</span></span><br/></td>
<td><span data-ttu-id="833b5-123">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="833b5-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="833b5-124">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="833b5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="833b5-125">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="833b5-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="833b5-126">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="833b5-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="833b5-127">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="833b5-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="833b5-128"><strong>хасларжеитемс</strong></span><span class="sxs-lookup"><span data-stu-id="833b5-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="833b5-129">Логическое</span><span class="sxs-lookup"><span data-stu-id="833b5-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="833b5-130">Нет</span><span class="sxs-lookup"><span data-stu-id="833b5-130">No</span></span><br/></td>
<td><span data-ttu-id="833b5-131">Определяет, отображается ли в элементе управления галереи большой или маленький ресурс изображения команды.</span><span class="sxs-lookup"><span data-stu-id="833b5-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="833b5-132">Применяется только к коллекциям, в которых значение атрибута <em>Type</em> равно <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="833b5-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="833b5-133">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="833b5-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="833b5-134">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="833b5-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="833b5-135">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="833b5-135">Default.</span></span> <br/> </dd> <span data-ttu-id="833b5-136"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="833b5-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="833b5-137"><strong>итемхеигхт</strong></span><span class="sxs-lookup"><span data-stu-id="833b5-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="833b5-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="833b5-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="833b5-139">Нет</span><span class="sxs-lookup"><span data-stu-id="833b5-139">No</span></span><br/></td>
<td><span data-ttu-id="833b5-140"><dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="833b5-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="833b5-141">Значение по умолчанию — -1.</span><span class="sxs-lookup"><span data-stu-id="833b5-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="833b5-142"><strong>итемвидс</strong></span><span class="sxs-lookup"><span data-stu-id="833b5-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="833b5-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="833b5-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="833b5-144">Нет</span><span class="sxs-lookup"><span data-stu-id="833b5-144">No</span></span><br/></td>
<td><span data-ttu-id="833b5-145"><dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="833b5-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="833b5-146">Значение по умолчанию — -1.</span><span class="sxs-lookup"><span data-stu-id="833b5-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="833b5-147"><strong>текстпоситион</strong></span><span class="sxs-lookup"><span data-stu-id="833b5-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="833b5-148">текстпоситионтипе</span><span class="sxs-lookup"><span data-stu-id="833b5-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="833b5-149">Нет</span><span class="sxs-lookup"><span data-stu-id="833b5-149">No</span></span><br/></td>
<td><span data-ttu-id="833b5-150">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="833b5-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="833b5-151">
<dt><span></span><span></span><strong></strong> Нижний</span><span class="sxs-lookup"><span data-stu-id="833b5-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="833b5-152"><dt><span></span><span></span><strong></strong> Ыть</span><span class="sxs-lookup"><span data-stu-id="833b5-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="833b5-153"><dt><span></span><span></span><strong></strong> Слева</span><span class="sxs-lookup"><span data-stu-id="833b5-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="833b5-154"><dt><span></span><span></span><strong></strong> Крывает</span><span class="sxs-lookup"><span data-stu-id="833b5-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="833b5-155"><dt><span></span><span></span><strong></strong> Справа</span><span class="sxs-lookup"><span data-stu-id="833b5-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="833b5-156"><dt><span></span><span></span><strong></strong> Лучшая</span><span class="sxs-lookup"><span data-stu-id="833b5-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="833b5-157"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="833b5-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="833b5-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="833b5-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="833b5-159">Нет</span><span class="sxs-lookup"><span data-stu-id="833b5-159">No</span></span><br/></td>
<td><span data-ttu-id="833b5-160">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="833b5-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="833b5-161">
<dt><span></span><span></span><strong></strong> Файлов</span><span class="sxs-lookup"><span data-stu-id="833b5-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="833b5-162"><dt><span></span><span></span><strong></strong> Меню</span><span class="sxs-lookup"><span data-stu-id="833b5-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="833b5-163">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="833b5-163">Child elements</span></span>



| <span data-ttu-id="833b5-164">Элемент</span><span class="sxs-lookup"><span data-stu-id="833b5-164">Element</span></span>                                                                                                 | <span data-ttu-id="833b5-165">Описание</span><span class="sxs-lookup"><span data-stu-id="833b5-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="833b5-166">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="833b5-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="833b5-167">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="833b5-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="833b5-168">**Установка**</span><span class="sxs-lookup"><span data-stu-id="833b5-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="833b5-169">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="833b5-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="833b5-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="833b5-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="833b5-171">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="833b5-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="833b5-172">**Сплитбуттонгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="833b5-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="833b5-173">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="833b5-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="833b5-174">**Сплитбуттонгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="833b5-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="833b5-175">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="833b5-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="833b5-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="833b5-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="833b5-177">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="833b5-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="833b5-178">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="833b5-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="833b5-179">Элемент</span><span class="sxs-lookup"><span data-stu-id="833b5-179">Element</span></span></th>
<th><span data-ttu-id="833b5-180">Описание</span><span class="sxs-lookup"><span data-stu-id="833b5-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="833b5-181"><a href="windowsribbon-element-controlgroup.md"><strong>контролграуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="833b5-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="833b5-182"><a href="windowsribbon-element-group.md"><strong>Группа</strong></a></span><span class="sxs-lookup"><span data-stu-id="833b5-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="833b5-183"><a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="833b5-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="833b5-184">Если он содержится в <a href="windowsribbon-element-applicationmenu.md"><strong>аппликатионмену</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="833b5-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="833b5-185">Этот элемент поддерживается только на первом уровне и не должен иметь дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="833b5-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="833b5-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Куиккакцесстулбар. Аппликатиондефаултс</strong></a></span><span class="sxs-lookup"><span data-stu-id="833b5-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="833b5-187">Windows 8 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="833b5-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="833b5-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="833b5-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="833b5-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="833b5-189">Remarks</span></span>

<span data-ttu-id="833b5-190">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="833b5-190">Optional.</span></span>

<span data-ttu-id="833b5-191">Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md)или [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="833b5-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="833b5-192">**Сплитбуттонгаллери** поддерживает [режимы приложений](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="833b5-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="833b5-193">[Пользовательский интерфейс \_ PKEY \_ булеанвалуе](windowsribbon-reference-properties-uipkey-booleanvalue.md) используется приложением для запроса состояния переключения для элемента управления "Кнопка" в **сплитбуттонгаллери**.</span><span class="sxs-lookup"><span data-stu-id="833b5-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="833b5-194">На следующем снимке экрана показан элемент управления ["коллекция кнопок с разделением ленты"](windowsribbon-controls-splitbuttongallery.md) в Microsoft Paint для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="833b5-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![снимок экрана: элемент управления "коллекция разделенных кнопок" в Microsoft Paint для Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="833b5-196">Примеры</span><span class="sxs-lookup"><span data-stu-id="833b5-196">Examples</span></span>

<span data-ttu-id="833b5-197">В следующем примере показана базовая разметка для [коллекции разворачивающихся кнопок](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="833b5-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="833b5-198">В этом разделе кода показаны объявления команд **сплитбуттонгаллери** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **сплитбуттонгаллери** .</span><span class="sxs-lookup"><span data-stu-id="833b5-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



<span data-ttu-id="833b5-199">В этом разделе кода показаны объявления элементов управления **сплитбуттонгаллери** .</span><span class="sxs-lookup"><span data-stu-id="833b5-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="833b5-200">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="833b5-200">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="833b5-201">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="833b5-201">Minimum supported system</span></span><br/> | <span data-ttu-id="833b5-202">Windows 7</span><span class="sxs-lookup"><span data-stu-id="833b5-202">Windows 7</span></span> |
| <span data-ttu-id="833b5-203">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="833b5-203">Can be empty</span></span>                        | <span data-ttu-id="833b5-204">Нет</span><span class="sxs-lookup"><span data-stu-id="833b5-204">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="833b5-205">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="833b5-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833b5-206">Элемент управления коллекции разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="833b5-206">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="833b5-207">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="833b5-207">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="833b5-208">**сетмодес**</span><span class="sxs-lookup"><span data-stu-id="833b5-208">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="833b5-209">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="833b5-209">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

