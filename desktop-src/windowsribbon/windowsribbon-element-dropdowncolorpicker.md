---
title: Дропдовнколорпиккер, элемент
description: Представляет Drop-Down цвет, Пиккерконтрол, что при нажатии кнопки отображается палитра цветовых палитр.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Лента Windows для элемента Дропдовнколорпиккер
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00185d14d9066b2cb85da4b23959e84df1827007
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "103786030"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="655c8-104">Дропдовнколорпиккер, элемент</span><span class="sxs-lookup"><span data-stu-id="655c8-104">DropDownColorPicker element</span></span>

<span data-ttu-id="655c8-105">Представляет элемент управления " [Выбор цвета](windowsribbon-controls-dropdowncolorpicker.md)", который при нажатии отображает палитру цветовых палитр.</span><span class="sxs-lookup"><span data-stu-id="655c8-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="655c8-106">Использование</span><span class="sxs-lookup"><span data-stu-id="655c8-106">Usage</span></span>

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="655c8-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="655c8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="655c8-108">attribute</span><span class="sxs-lookup"><span data-stu-id="655c8-108">Attribute</span></span></th>
<th><span data-ttu-id="655c8-109">Тип</span><span class="sxs-lookup"><span data-stu-id="655c8-109">Type</span></span></th>
<th><span data-ttu-id="655c8-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="655c8-110">Required</span></span></th>
<th><span data-ttu-id="655c8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="655c8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="655c8-112"><strong>чипсизе</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="655c8-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="655c8-114">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-114">No</span></span><br/></td>
<td><span data-ttu-id="655c8-115">Размер каждой микросхемы или образца цвета.</span><span class="sxs-lookup"><span data-stu-id="655c8-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="655c8-116">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="655c8-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="655c8-117">
<dt><span></span><span></span><strong></strong> Значительные</span><span class="sxs-lookup"><span data-stu-id="655c8-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-118">Каждая цветовая Микросхема представляет собой 11x11 пиксельный квадрат.</span><span class="sxs-lookup"><span data-stu-id="655c8-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="655c8-119"><dt><span></span><span></span><strong></strong> Высокое</span><span class="sxs-lookup"><span data-stu-id="655c8-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-120">Каждая цветовая Микросхема представляет собой пиксельный квадрат размером 16x16 пикселей.</span><span class="sxs-lookup"><span data-stu-id="655c8-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="655c8-121"><dt><span></span><span></span><strong></strong> Достаточ</span><span class="sxs-lookup"><span data-stu-id="655c8-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-122">Каждая цветовая Микросхема представляет собой 24x24 пиксельный квадрат.</span><span class="sxs-lookup"><span data-stu-id="655c8-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="655c8-123"><strong>колортемплате</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="655c8-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="655c8-125">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-125">No</span></span><br/></td>
<td><span data-ttu-id="655c8-126">Шаблоны макета, указывающие тип выбора раскрывающегося <a href="windowsribbon-controls-dropdowncolorpicker.md">цвета</a>.</span><span class="sxs-lookup"><span data-stu-id="655c8-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="655c8-127">Ограничено одним из следующих значений (если не объявлены дополнительные атрибуты, связанные с <em>колортемплате</em> , отображается представление по умолчанию):</span><span class="sxs-lookup"><span data-stu-id="655c8-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="655c8-128">
<dt><span></span><span></span><strong></strong> (Семеколорс)</span><span class="sxs-lookup"><span data-stu-id="655c8-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-129">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="655c8-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="655c8-130">Установка атрибута <em>колортемплате</em> для <code>ThemeColors</code> включения следующих функций:</span><span class="sxs-lookup"><span data-stu-id="655c8-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="655c8-131">Привязка SplitButton.</span><span class="sxs-lookup"><span data-stu-id="655c8-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="655c8-132">По умолчанию отображается кнопка <strong>автоматического</strong> цвета.</span><span class="sxs-lookup"><span data-stu-id="655c8-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="655c8-133">Сетка образцов <strong>цветов темы</strong> Windows.</span><span class="sxs-lookup"><span data-stu-id="655c8-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="655c8-134">Сетка образцов <strong>стандартных цветов</strong> .</span><span class="sxs-lookup"><span data-stu-id="655c8-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="655c8-135">Сетка образцов <strong>последних цветов</strong> необязательна.</span><span class="sxs-lookup"><span data-stu-id="655c8-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="655c8-136">Диалоговое окно " <strong>другие цвета</strong> " средство запуска.</span><span class="sxs-lookup"><span data-stu-id="655c8-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="655c8-137">По умолчанию не отображается кнопка цвета <strong>цвета</strong> .</span><span class="sxs-lookup"><span data-stu-id="655c8-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="655c8-138"><dt><span></span><span></span><strong></strong> (Стандардколорс)</span><span class="sxs-lookup"><span data-stu-id="655c8-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="655c8-139">Установка атрибута <em>колортемплате</em> для <code>StandardColors</code> включения следующих функций:</span><span class="sxs-lookup"><span data-stu-id="655c8-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="655c8-140">Привязка SplitButton.</span><span class="sxs-lookup"><span data-stu-id="655c8-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="655c8-141">По умолчанию отображается кнопка <strong>автоматического</strong> цвета.</span><span class="sxs-lookup"><span data-stu-id="655c8-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="655c8-142">Сетка образцов <strong>стандартных цветов</strong> .</span><span class="sxs-lookup"><span data-stu-id="655c8-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="655c8-143">Диалоговое окно " <strong>другие цвета</strong> " средство запуска.</span><span class="sxs-lookup"><span data-stu-id="655c8-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="655c8-144">По умолчанию не отображается кнопка цвета <strong>цвета</strong> .</span><span class="sxs-lookup"><span data-stu-id="655c8-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="655c8-145"><dt><span></span><span></span><strong></strong> (Хигхлигхтколорс)</span><span class="sxs-lookup"><span data-stu-id="655c8-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="655c8-146">Установка атрибута <em>колортемплате</em> для <code>HighlightColors</code> включения следующих функций:</span><span class="sxs-lookup"><span data-stu-id="655c8-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="655c8-147">Привязка SplitButton.</span><span class="sxs-lookup"><span data-stu-id="655c8-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="655c8-148">Сетка образцов <strong>стандартных цветов</strong> без заголовка.</span><span class="sxs-lookup"><span data-stu-id="655c8-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="655c8-149">По умолчанию не отображается кнопка цвета <strong>цвета</strong> .</span><span class="sxs-lookup"><span data-stu-id="655c8-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="655c8-150"><strong>Столбцы</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="655c8-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="655c8-152">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-152">No</span></span><br/></td>
<td><span data-ttu-id="655c8-153">Число столбцов цветовой микросхемы (или образцов).</span><span class="sxs-lookup"><span data-stu-id="655c8-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="655c8-154">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)</span><span class="sxs-lookup"><span data-stu-id="655c8-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-155">Любое положительное целочисленное значение от 1 до 256 включительно.</span><span class="sxs-lookup"><span data-stu-id="655c8-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="655c8-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-157">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="655c8-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="655c8-158">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-158">No</span></span><br/></td>
<td><span data-ttu-id="655c8-159">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="655c8-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="655c8-160">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="655c8-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-161">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="655c8-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="655c8-162">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="655c8-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="655c8-163">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="655c8-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="655c8-164"><strong>исаутоматикколорбуттонвисибле</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-165">Логическое</span><span class="sxs-lookup"><span data-stu-id="655c8-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="655c8-166">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-166">No</span></span><br/></td>
<td><span data-ttu-id="655c8-167">Отображает (или скрывает) кнопку <strong>автоматического</strong> цвета.</span><span class="sxs-lookup"><span data-stu-id="655c8-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="655c8-168">Допустим, только <code>StandardColors</code> Если <code>ThemeColors</code> указан параметр или для атрибута <em>колортемплате</em> .</span><span class="sxs-lookup"><span data-stu-id="655c8-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="655c8-169">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="655c8-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="655c8-170">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="655c8-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="655c8-171"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="655c8-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="655c8-172"><strong>исноколорбуттонвисибле</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-173">Логическое</span><span class="sxs-lookup"><span data-stu-id="655c8-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="655c8-174">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-174">No</span></span><br/></td>
<td><span data-ttu-id="655c8-175">Отображает (или скрывает) кнопку <strong>без цвета</strong> .</span><span class="sxs-lookup"><span data-stu-id="655c8-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="655c8-176">Допустимо для всех значений <em>колортемплате</em> .</span><span class="sxs-lookup"><span data-stu-id="655c8-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="655c8-177">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="655c8-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="655c8-178">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="655c8-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="655c8-179"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="655c8-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="655c8-180"><strong>рецентколоргридровс</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="655c8-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="655c8-182">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-182">No</span></span><br/></td>
<td><span data-ttu-id="655c8-183">Число строк цветовой микросхемы (или образца) в области " <strong>Последние цвета</strong> ".</span><span class="sxs-lookup"><span data-stu-id="655c8-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="655c8-184">Допустимо, только если <code>ThemeColors</code> для атрибута <em>колортемплате</em> задано значение.</span><span class="sxs-lookup"><span data-stu-id="655c8-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="655c8-185">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)</span><span class="sxs-lookup"><span data-stu-id="655c8-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-186">Любое положительное целочисленное значение от 1 до 256 включительно.</span><span class="sxs-lookup"><span data-stu-id="655c8-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="655c8-187"><strong>стандардколоргридровс</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="655c8-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="655c8-189">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-189">No</span></span><br/></td>
<td><span data-ttu-id="655c8-190">Число строк цветовой микросхемы (или образца) в области <strong>Стандартные цвета</strong> .</span><span class="sxs-lookup"><span data-stu-id="655c8-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="655c8-191">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)</span><span class="sxs-lookup"><span data-stu-id="655c8-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-192">Любое положительное целочисленное значение от 1 до 256 включительно.</span><span class="sxs-lookup"><span data-stu-id="655c8-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="655c8-193"><strong>семеколоргридровс</strong></span><span class="sxs-lookup"><span data-stu-id="655c8-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="655c8-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="655c8-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="655c8-195">Нет</span><span class="sxs-lookup"><span data-stu-id="655c8-195">No</span></span><br/></td>
<td><span data-ttu-id="655c8-196">Число строк цветовой микросхемы (или образца) в области <strong>цвета темы</strong> .</span><span class="sxs-lookup"><span data-stu-id="655c8-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="655c8-197">Допустимо, только если <code>ThemeColors</code> для атрибута <em>колортемплате</em> задано значение.</span><span class="sxs-lookup"><span data-stu-id="655c8-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="655c8-198">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)</span><span class="sxs-lookup"><span data-stu-id="655c8-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="655c8-199">Любое положительное целочисленное значение от 1 до 256 включительно.</span><span class="sxs-lookup"><span data-stu-id="655c8-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="655c8-200">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="655c8-200">Child elements</span></span>

<span data-ttu-id="655c8-201">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="655c8-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="655c8-202">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="655c8-202">Parent elements</span></span>



| <span data-ttu-id="655c8-203">Элемент</span><span class="sxs-lookup"><span data-stu-id="655c8-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="655c8-204">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="655c8-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="655c8-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="655c8-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="655c8-206">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="655c8-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="655c8-207">**Группа**</span><span class="sxs-lookup"><span data-stu-id="655c8-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="655c8-208">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="655c8-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="655c8-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="655c8-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="655c8-210">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="655c8-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="655c8-211">Комментарии</span><span class="sxs-lookup"><span data-stu-id="655c8-211">Remarks</span></span>

<span data-ttu-id="655c8-212">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="655c8-212">Optional.</span></span>

<span data-ttu-id="655c8-213">Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="655c8-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="655c8-214">Примеры</span><span class="sxs-lookup"><span data-stu-id="655c8-214">Examples</span></span>

<span data-ttu-id="655c8-215">В следующем примере показана базовая разметка для всех трех типов [средства выбора цвета](windowsribbon-controls-dropdowncolorpicker.md)раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="655c8-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="655c8-216">В этом разделе кода показаны объявления команд для трех элементов **дропдовнколорпиккер** .</span><span class="sxs-lookup"><span data-stu-id="655c8-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



<span data-ttu-id="655c8-217">В этом разделе кода показаны три типа объявлений элементов управления **дропдовнколорпиккер** .</span><span class="sxs-lookup"><span data-stu-id="655c8-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="655c8-218">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="655c8-218">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="655c8-219">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="655c8-219">Minimum supported system</span></span><br/> | <span data-ttu-id="655c8-220">Windows 7</span><span class="sxs-lookup"><span data-stu-id="655c8-220">Windows 7</span></span> |
| <span data-ttu-id="655c8-221">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="655c8-221">Can be empty</span></span>                        | <span data-ttu-id="655c8-222">Да</span><span class="sxs-lookup"><span data-stu-id="655c8-222">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="655c8-223">См. также</span><span class="sxs-lookup"><span data-stu-id="655c8-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="655c8-224">Элемент управления выбора цвета в раскрывающемся списке</span><span class="sxs-lookup"><span data-stu-id="655c8-224">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="655c8-225">Пример Дропдовнколорпиккер</span><span class="sxs-lookup"><span data-stu-id="655c8-225">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





