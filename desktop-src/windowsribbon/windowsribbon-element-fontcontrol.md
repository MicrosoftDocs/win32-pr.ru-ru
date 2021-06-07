---
title: Фонтконтрол, элемент
description: Представляет элемент управления "Шрифт", который является специализированным контейнером для отдельных элементов управления, предназначенных для обработки шрифтов.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Лента Windows для элемента Фонтконтрол
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c9d900c2af4f7f8ba26f5ac8dbbdc0d055668d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443405"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="af1e4-104">Фонтконтрол, элемент</span><span class="sxs-lookup"><span data-stu-id="af1e4-104">FontControl element</span></span>

<span data-ttu-id="af1e4-105">Представляет [элемент управления "шрифт](windowsribbon-controls-fontcontrol.md)", который является специализированным контейнером для отдельных элементов управления, предназначенных для обработки шрифтов.</span><span class="sxs-lookup"><span data-stu-id="af1e4-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="af1e4-106">Использование</span><span class="sxs-lookup"><span data-stu-id="af1e4-106">Usage</span></span>

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
```

## <a name="attributes"></a><span data-ttu-id="af1e4-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="af1e4-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af1e4-108">attribute</span><span class="sxs-lookup"><span data-stu-id="af1e4-108">Attribute</span></span></th>
<th><span data-ttu-id="af1e4-109">Тип</span><span class="sxs-lookup"><span data-stu-id="af1e4-109">Type</span></span></th>
<th><span data-ttu-id="af1e4-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="af1e4-110">Required</span></span></th>
<th><span data-ttu-id="af1e4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="af1e4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af1e4-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="af1e4-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="af1e4-114">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-114">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="af1e4-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="af1e4-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="af1e4-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="af1e4-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="af1e4-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="af1e4-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="af1e4-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="af1e4-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af1e4-120"><strong>фонттипе</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="af1e4-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="af1e4-122">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-122">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-123">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="af1e4-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="af1e4-124">
<dt><span></span><span></span><strong></strong> (Фонтонли)</span><span class="sxs-lookup"><span data-stu-id="af1e4-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-125">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af1e4-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="af1e4-126">Установка атрибута <em>фонттипе</em> для <code>FontOnly</code> включения следующих функций:</span><span class="sxs-lookup"><span data-stu-id="af1e4-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="af1e4-127">Поле со списком <strong>семейства шрифтов</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="af1e4-128">Поле со списком " <strong>Размер шрифта</strong> ".</span><span class="sxs-lookup"><span data-stu-id="af1e4-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="af1e4-129">Переключатели <strong>полужирный</strong>, <strong>курсив</strong>, <strong>Подчеркнутый</strong>и <strong>Зачеркнутый</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-130">Выключатели <strong>зачеркивания</strong> и <strong>подчеркивания</strong> отображаются по умолчанию, но могут быть скрыты путем установки атрибутов <em>исстрикесраугхбуттонвисибле</em> и <em>исундерлинебуттонвисибле</em> в значение <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="af1e4-131"><dt><span></span><span></span><strong></strong> (Фонтвисколор)</span><span class="sxs-lookup"><span data-stu-id="af1e4-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="af1e4-132">Установка атрибута <em>фонттипе</em> для <code>FontWithColor</code> включения следующих функций:</span><span class="sxs-lookup"><span data-stu-id="af1e4-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="af1e4-133">Поле со списком <strong>семейства шрифтов</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="af1e4-134">Поле со списком " <strong>Размер шрифта</strong> ".</span><span class="sxs-lookup"><span data-stu-id="af1e4-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="af1e4-135"><strong>Увеличение</strong> и уменьшение <strong>размера шрифта шрифта и кнопок</strong> увеличения и уменьшения.</span><span class="sxs-lookup"><span data-stu-id="af1e4-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="af1e4-136">Переключатели <strong>полужирный</strong>, <strong>курсив</strong>, <strong>Подчеркнутый</strong>и <strong>Зачеркнутый</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-137">Выключатели <strong>зачеркивания</strong> и <strong>подчеркивания</strong> отображаются по умолчанию, но могут быть скрыты путем установки атрибутов <em>исстрикесраугхбуттонвисибле</em> и <em>исундерлинебуттонвисибле</em> в значение <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="af1e4-138">Палитра цветов <strong>текста</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="af1e4-139">Палитра цветов <strong>выделения текста</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-140">Этот элемент управления скрыт по умолчанию, но его можно отобразить, задав для атрибута <em>ишигхлигхтбуттонвисибле</em> значение <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="af1e4-141"><dt><span></span><span></span><strong></strong> (Ричфонт)</span><span class="sxs-lookup"><span data-stu-id="af1e4-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="af1e4-142">Установка атрибута <em>фонттипе</em> для <code>RichFont</code> включения следующих функций:</span><span class="sxs-lookup"><span data-stu-id="af1e4-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="af1e4-143">Поле со списком <strong>семейства шрифтов</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="af1e4-144">Поле со списком " <strong>Размер шрифта</strong> ".</span><span class="sxs-lookup"><span data-stu-id="af1e4-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="af1e4-145"><strong>Увеличение</strong> и уменьшение <strong>размера шрифта шрифта и кнопок</strong> увеличения и уменьшения.</span><span class="sxs-lookup"><span data-stu-id="af1e4-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="af1e4-146">Переключатели <strong>полужирный</strong>, <strong>курсив</strong>, <strong>Подчеркнутый</strong>и <strong>Зачеркнутый</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-147">Переключатели <strong>зачеркивания</strong> и <strong>подчеркивания</strong> отображаются по умолчанию и не могут быть скрыты путем установки атрибутов <em>исстрикесраугхбуттонвисибле</em> и <em>исундерлинебуттонвисибле</em> в значение <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="af1e4-148">Палитра цветов <strong>текста</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="af1e4-149">Палитра цветов <strong>выделения текста</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-150">Этот элемент управления отображается по умолчанию и не может быть скрыт путем присвоения атрибуту <em>ишигхлигхтбуттонвисибле</em> значения <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="af1e4-151">Выключатели <strong>подстрочных</strong> и <strong>верхних индексов</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af1e4-152"><strong>исгровшринкбуттонграупвисибле</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-153">Логическое</span><span class="sxs-lookup"><span data-stu-id="af1e4-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="af1e4-154">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-154">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-155"><strong>Windows 8 и более поздние версии</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="af1e4-156">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="af1e4-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-157">Кнопки увеличения и сжатия никогда не отображаются в <a href="windowsribbon-element-minitoolbar.md"><strong>минитулбар</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="af1e4-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="af1e4-158">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="af1e4-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-159">По умолчанию, если значение <em>фонттипе</em> равно <code>FontWithColor</code> или <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="af1e4-160"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="af1e4-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-161">По умолчанию, если значение <em>фонттипе</em> равно <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af1e4-162"><strong>ишигхлигхтбуттонвисибле</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-163">Логическое</span><span class="sxs-lookup"><span data-stu-id="af1e4-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="af1e4-164">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-164">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-165">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="af1e4-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-166">Выделение цветом доступно только из <strong>фонтконтрол</strong> , если значение атрибута <em>фонттипе</em> равно <code>FontWithColor</code> или <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="af1e4-167">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="af1e4-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-168">По умолчанию, если значение <em>фонттипе</em> равно <code>FontWithColor</code> или <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="af1e4-169">Действует, только если значение <em>фонттипе</em> равно <code>FontWithColor</code> или <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="af1e4-170"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="af1e4-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-171">По умолчанию, если значение <em>фонттипе</em> равно <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="af1e4-172">Действует, только если значение <em>фонттипе</em> равно <code>FontOnly</code> или <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af1e4-173"><strong>исстрикесраугхбуттонвисибле</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-174">Логическое</span><span class="sxs-lookup"><span data-stu-id="af1e4-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="af1e4-175">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-175">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-176">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="af1e4-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="af1e4-177">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="af1e4-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-178">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af1e4-178">Default.</span></span> <br/> </dd> <span data-ttu-id="af1e4-179"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="af1e4-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-180">Действует, только если значение <em>фонттипе</em> равно <code>FontOnly</code> или <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af1e4-181"><strong>исундерлинебуттонвисибле</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-182">Логическое</span><span class="sxs-lookup"><span data-stu-id="af1e4-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="af1e4-183">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-183">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-184">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="af1e4-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="af1e4-185">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="af1e4-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-186">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af1e4-186">Default.</span></span> <br/> </dd> <span data-ttu-id="af1e4-187"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="af1e4-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-188">Действует, только если значение <em>фонттипе</em> равно <code>FontOnly</code> или <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af1e4-189"><strong>максимумфонтсизе</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="af1e4-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="af1e4-191">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-191">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-192">Максимальный отображаемый размер точки.</span><span class="sxs-lookup"><span data-stu-id="af1e4-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="af1e4-193">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)</span><span class="sxs-lookup"><span data-stu-id="af1e4-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-194">Целочисленное значение в диапазоне от 1 до 9999 включительно.</span><span class="sxs-lookup"><span data-stu-id="af1e4-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="af1e4-195">Значение по умолчанию — <strong>9999</strong>.</span><span class="sxs-lookup"><span data-stu-id="af1e4-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af1e4-196"><strong>минимумфонтсизе</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="af1e4-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="af1e4-198">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-198">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-199">Минимальный размер точки для вывода.</span><span class="sxs-lookup"><span data-stu-id="af1e4-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="af1e4-200">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)</span><span class="sxs-lookup"><span data-stu-id="af1e4-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-201">Целочисленное значение в диапазоне от 1 до 9999 включительно.</span><span class="sxs-lookup"><span data-stu-id="af1e4-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="af1e4-202">Значение по умолчанию — <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="af1e4-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af1e4-203"><strong>шовтруетипеонли</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-204">Логическое</span><span class="sxs-lookup"><span data-stu-id="af1e4-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="af1e4-205">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-205">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-206">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="af1e4-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="af1e4-207">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="af1e4-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-208">Отображаются только шрифты TrueType и OpenType.</span><span class="sxs-lookup"><span data-stu-id="af1e4-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="af1e4-209"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="af1e4-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-210">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af1e4-210">Default.</span></span> <span data-ttu-id="af1e4-211">Для типа отображаемых шрифтов ограничение не размещается.</span><span class="sxs-lookup"><span data-stu-id="af1e4-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af1e4-212"><strong>шоввертикалфонтс</strong></span><span class="sxs-lookup"><span data-stu-id="af1e4-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="af1e4-213">Логическое</span><span class="sxs-lookup"><span data-stu-id="af1e4-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="af1e4-214">Нет</span><span class="sxs-lookup"><span data-stu-id="af1e4-214">No</span></span><br/></td>
<td><span data-ttu-id="af1e4-215">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="af1e4-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-216">Вертикальным шрифтам предшествует символ @ в списке <strong>семейств шрифтов</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="af1e4-217">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="af1e4-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-218">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af1e4-218">Default.</span></span> <span data-ttu-id="af1e4-219">Отображает вертикальные шрифты, которые <strong>отображаются на панели</strong> управления " <strong>шрифты</strong> ".</span><span class="sxs-lookup"><span data-stu-id="af1e4-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="af1e4-220"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="af1e4-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="af1e4-221">Позволяет приложению, не поддерживающему вертикальный текст, скрывать любые вертикальные шрифты, которые отображаются <strong>на панели</strong> управления <strong>шрифтами</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af1e4-222">В Windows Vista панель управления « <strong>шрифты</strong> » не предлагает функции <strong>отображения</strong> или <strong>скрытия</strong> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="af1e4-223">В этом случае атрибут <em>шоввертикалфонтс</em> должен иметь значение <code>False</code> .</span><span class="sxs-lookup"><span data-stu-id="af1e4-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="af1e4-224">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="af1e4-224">Child elements</span></span>

<span data-ttu-id="af1e4-225">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="af1e4-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="af1e4-226">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="af1e4-226">Parent elements</span></span>



| <span data-ttu-id="af1e4-227">Элемент</span><span class="sxs-lookup"><span data-stu-id="af1e4-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="af1e4-228">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="af1e4-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="af1e4-229">**Группа**</span><span class="sxs-lookup"><span data-stu-id="af1e4-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="af1e4-230">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="af1e4-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="af1e4-231">Remarks</span><span class="sxs-lookup"><span data-stu-id="af1e4-231">Remarks</span></span>

<span data-ttu-id="af1e4-232">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="af1e4-232">Optional.</span></span>

<span data-ttu-id="af1e4-233">Может встречаться не более одного раза для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md)или [**менуграуп**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="af1e4-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="af1e4-234">Все атрибуты команды **фонтконтрол** , объявленные в разметке, такие как [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или [**Command. тултиптитле**](windowsribbon-element-command-tooltiptitle.md), переопределяются атрибутами отдельных элементов управления, составляющих **фонтконтрол**.</span><span class="sxs-lookup"><span data-stu-id="af1e4-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="af1e4-235">Любая попытка выбрать цветовую палитру из палитры [элементов управления шрифта](windowsribbon-controls-fontcontrol.md) может привести к нарушению прав доступа, если с элементом управления не связан ни один обработчик команд.</span><span class="sxs-lookup"><span data-stu-id="af1e4-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="af1e4-236">Примеры</span><span class="sxs-lookup"><span data-stu-id="af1e4-236">Examples</span></span>

<span data-ttu-id="af1e4-237">В следующем примере показана базовая разметка для трех типов [элементов управления шрифта](windowsribbon-controls-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="af1e4-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="af1e4-238">В этом разделе кода показаны объявления команд **фонтконтрол** , каждая из которых содержит объявление контейнера [**группы**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="af1e4-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



<span data-ttu-id="af1e4-239">В этом разделе кода показаны объявления элементов управления **фонтконтрол** , где каждая **фонтконтрол** и [**Группа**](windowsribbon-element-group.md) объявляются на одной вкладке.</span><span class="sxs-lookup"><span data-stu-id="af1e4-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a><span data-ttu-id="af1e4-240">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="af1e4-240">Element information</span></span>

* <span data-ttu-id="af1e4-241">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="af1e4-241">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="af1e4-242">**Может быть пустым**: Да</span><span class="sxs-lookup"><span data-stu-id="af1e4-242">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="af1e4-243">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af1e4-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1e4-244">Элемент управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="af1e4-244">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="af1e4-245">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="af1e4-245">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="af1e4-246">Пример Фонтконтрол</span><span class="sxs-lookup"><span data-stu-id="af1e4-246">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





