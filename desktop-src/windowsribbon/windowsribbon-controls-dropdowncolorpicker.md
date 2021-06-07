---
title: Средство выбора цвета Drop-Down
description: Платформа Windows Ribbon предоставляет специализированный элемент управления "Выбор цвета" Drop-Down, который предоставляет разнообразные параметры цвета с помощью кнопки разделения и настраиваемого выбора раскрывающегося цвета.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366cc7eadaca23271d5b2afa43ec66235839694a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443665"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="1fbc7-103">Средство выбора цвета Drop-Down</span><span class="sxs-lookup"><span data-stu-id="1fbc7-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="1fbc7-104">Платформа Windows Ribbon предоставляет специализированный элемент управления "Выбор цвета" Drop-Down, который предоставляет разнообразные параметры цвета с помощью кнопки разделения и настраиваемого выбора раскрывающегося цвета.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="1fbc7-105">Введение</span><span class="sxs-lookup"><span data-stu-id="1fbc7-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="1fbc7-106">разметку</span><span class="sxs-lookup"><span data-stu-id="1fbc7-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="1fbc7-107">Код</span><span class="sxs-lookup"><span data-stu-id="1fbc7-107">Code</span></span>](#code)
    -   [<span data-ttu-id="1fbc7-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fbc7-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="1fbc7-109">Обработчики команд</span><span class="sxs-lookup"><span data-stu-id="1fbc7-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="1fbc7-110">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1fbc7-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="1fbc7-111">Введение</span><span class="sxs-lookup"><span data-stu-id="1fbc7-111">Introduction</span></span>

<span data-ttu-id="1fbc7-112">Имитируя внешний вид и функциональность средства выбора цвета Microsoft Office, платформа Ribbon может использовать оба преимущества, а также обеспечивать согласованность и знание широкого спектра приложений.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="1fbc7-113">разметку</span><span class="sxs-lookup"><span data-stu-id="1fbc7-113">Markup</span></span>

<span data-ttu-id="1fbc7-114">Как и все элементы управления Ribbon, палитра Drop-Down цвета легко реализуется и настраивается с помощью разметки.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="1fbc7-115">Платформа предоставляет ряд атрибутов элементов для средства выбора цвета Drop-Down для предоставления различных уровней функциональности.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="1fbc7-116">В следующей таблице перечислены атрибуты палитры цветов Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fbc7-117">attribute</span><span class="sxs-lookup"><span data-stu-id="1fbc7-117">Attribute</span></span></th>
<th><span data-ttu-id="1fbc7-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1fbc7-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fbc7-119">колортемплате</span><span class="sxs-lookup"><span data-stu-id="1fbc7-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="1fbc7-120">Шаблоны макета, указывающие тип Drop-Down палитры.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="1fbc7-121">Существует три шаблона, каждый из которых задает макет элемента управления и значения по умолчанию для связанных атрибутов и ключей свойств.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-122">чипсизе</span><span class="sxs-lookup"><span data-stu-id="1fbc7-122">ChipSize</span></span></td>
<td><span data-ttu-id="1fbc7-123">Размер каждой цветовой микросхемы (или образца).</span><span class="sxs-lookup"><span data-stu-id="1fbc7-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-124">Столбцы</span><span class="sxs-lookup"><span data-stu-id="1fbc7-124">Columns</span></span></td>
<td><span data-ttu-id="1fbc7-125">Число столбцов цветовой микросхемы (или образцов).</span><span class="sxs-lookup"><span data-stu-id="1fbc7-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="1fbc7-126">CommandName</span></span></td>
<td><span data-ttu-id="1fbc7-127">Имя связанного объявления команды.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-128">исаутоматикколорбуттонвисибле</span><span class="sxs-lookup"><span data-stu-id="1fbc7-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="1fbc7-129">Отображает (или скрывает) <strong>автоматическую</strong> кнопку.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="1fbc7-130">Допустим, только если <em>колортемплате</em> имеет значение <code>ThemeColors</code> или <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-131">исноколорбуттонвисибле</span><span class="sxs-lookup"><span data-stu-id="1fbc7-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="1fbc7-132">Отображает (или скрывает) кнопку <strong>без цвета</strong> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="1fbc7-133">Допустимо для всех значений <em>колортемплате</em> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-134">рецентколоргридровс</span><span class="sxs-lookup"><span data-stu-id="1fbc7-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="1fbc7-135">Число строк цветовой микросхемы (или образца) в области " <strong>Последние цвета</strong> ".</span><span class="sxs-lookup"><span data-stu-id="1fbc7-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="1fbc7-136">Допустимо, только если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-137">стандардколоргридровс</span><span class="sxs-lookup"><span data-stu-id="1fbc7-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="1fbc7-138">Число строк цветовой микросхемы (или образца) в области <strong>Стандартные цвета</strong> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-139">семеколоргридровс</span><span class="sxs-lookup"><span data-stu-id="1fbc7-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="1fbc7-140">Число строк цветовой микросхемы (или образца) в области <strong>цвета темы</strong> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="1fbc7-141">Допустимо, только если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1fbc7-142">На следующих снимках экрана показаны макеты палитры Drop-Down по умолчанию для трех цветовых шаблонов.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fbc7-143">`ThemeColors`: \[ снимок экрана новой строки для \] ![ элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение "семеколорс". ](images/markup/colortemplate.themedcolors.1.png) \[ новой строки\]</span><span class="sxs-lookup"><span data-stu-id="1fbc7-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="1fbc7-144">`standardcolors`: \[ снимок экрана новой строки для \] ![ элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение "стандардколорс". ](images/markup/colortemplate.standardcolors.3.png) \[ новой строки\]</span><span class="sxs-lookup"><span data-stu-id="1fbc7-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="1fbc7-145">`highlightcolors`: \[ снимок экрана новой строки для \] ![ элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение "хигхлигхтколорс".](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="1fbc7-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="1fbc7-146">Базовая разметка, необходимая для каждого типа средства выбора цвета Drop-Down, показана в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="1fbc7-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="1fbc7-147">Палитра Drop-Down Color — это допустимый элемент управления ["Кнопка"](windowsribbon-controls-button.md) в шаблоне [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a><span data-ttu-id="1fbc7-148">Код</span><span class="sxs-lookup"><span data-stu-id="1fbc7-148">Code</span></span>

<span data-ttu-id="1fbc7-149">В качестве специализированного элемента управления, поддерживающего настройку, любая реализация средства выбора цвета Drop-Down, которая использует преимущества этих возможностей, требует специального кода приложения для управления свойствами и обработки всех команд, выдаваемых элементом управления.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="1fbc7-150">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fbc7-150">Properties</span></span>

<span data-ttu-id="1fbc7-151">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "Выбор цвета" Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="1fbc7-152">Как правило, свойство выбора цвета для Drop-Down обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="1fbc7-153">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="1fbc7-154">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="1fbc7-155">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="1fbc7-156">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="1fbc7-157">В следующей таблице перечислены ключи свойств, связанные с элементом управления "Выбор цвета" Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fbc7-158">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="1fbc7-158">Property Key</span></span></th>
<th><span data-ttu-id="1fbc7-159">Описание</span><span class="sxs-lookup"><span data-stu-id="1fbc7-159">Description</span></span></th>
<th><span data-ttu-id="1fbc7-160">Примечания</span><span class="sxs-lookup"><span data-stu-id="1fbc7-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fbc7-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="1fbc7-162">Определяет метку для кнопки <strong>автоматического</strong> цвета.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="1fbc7-163">Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> или <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-164">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="1fbc7-166">Определяет выбранное значение цвета как <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="1fbc7-167">Допустимо только в том случае, если <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> имеет значение <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-168">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="1fbc7-170">Определяет выбранный тип цвета.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-171">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="1fbc7-173">Определяет возможность элемента управления реагировать на взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-174">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="1fbc7-176">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="1fbc7-178">Определяет символьную строку для метки элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-179">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="1fbc7-181">Определяет крупное изображение высокой контрастности, отображаемое для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-182">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="1fbc7-183">Дополнительные сведения о форматах изображений см. в разделе <a href="windowsribbon-imageformats.md">указание ресурсов изображения ленты</a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="1fbc7-185">Определяет крупное изображение, отображаемое для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-186">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="1fbc7-187">Дополнительные сведения о форматах изображений см. в разделе <a href="windowsribbon-imageformats.md">указание ресурсов изображения ленты</a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="1fbc7-189">Определяет метку для кнопки " <strong>другие цвета</strong> ".</span><span class="sxs-lookup"><span data-stu-id="1fbc7-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="1fbc7-190">Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> или <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-191">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="1fbc7-193">Определяет метку для кнопки <strong>без цвета</strong> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="1fbc7-194">Допустимо для всех значений <em>колортемплате</em> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-195">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="1fbc7-197">Определяет метку для категории " <strong>Последние цвета</strong> ".</span><span class="sxs-lookup"><span data-stu-id="1fbc7-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="1fbc7-198">Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="1fbc7-199">Это единственный шаблон, содержащий помеченные категории.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-200">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="1fbc7-202">Определяет небольшое изображение с высокой контрастностью, отображаемое для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-203">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="1fbc7-204">Дополнительные сведения о форматах изображений см. в разделе <a href="windowsribbon-imageformats.md">указание ресурсов изображения ленты</a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="1fbc7-206">Определяет небольшое изображение, отображаемое для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-207">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="1fbc7-208">Дополнительные сведения о форматах изображений см. в разделе <a href="windowsribbon-imageformats.md">указание ресурсов изображения ленты</a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="1fbc7-210">Определяет массив значений <a href="/windows/win32/gdi/colorref">COLORREF</a> для образцов палитры цветов Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="1fbc7-211">Каждый Drop-Down палитра цветов <em>колортемплате</em> содержит <code>StandardColors</code> сетку.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1fbc7-212">Отобразятся значения <a href="/windows/win32/gdi/colorref">COLORREF</a> из начальных <em>столбцов</em> <em>стандардколоргридровс</em> x массива.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="1fbc7-213">Если массив определяет меньше цветов, чем число <code>StandardColors</code> образцов, объявленных в разметке, для недостающих микросхем отображаются пустые пробелы.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="1fbc7-214">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="1fbc7-216">Определяет метку для категории " <strong>Стандартные цвета</strong> ".</span><span class="sxs-lookup"><span data-stu-id="1fbc7-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="1fbc7-217">Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="1fbc7-218">Это единственный шаблон, содержащий помеченные категории.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-219">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="1fbc7-221">Определяет строковый массив всплывающих подсказок палитры цветов для <code>StandardColors</code> сетки.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="1fbc7-222">Каждый Drop-Down палитра цветов <em>колортемплате</em> содержит <code>StandardColors</code> сетку.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1fbc7-223">Используются только подсказки, необходимые для метки цветовых палитр, отображаемых в <code>StandardColors</code> сетке.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="1fbc7-224">Если указано меньшее количество меток, чем число образцов в <code>StandardColors</code> сетке, для образцов ремаинининг предоставляется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="1fbc7-225">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="1fbc7-227">Определяет массив значений <a href="/windows/win32/gdi/colorref">COLORREF</a> для образцов палитры цветов Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="1fbc7-228">Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1fbc7-229">Отобразятся значения <a href="/windows/win32/gdi/colorref">COLORREF</a> из начальных <em>столбцов</em> <em>семеколоргридровс</em> x массива.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="1fbc7-230">Если массив определяет меньше цветов, чем число <code>ThemeColors</code> образцов, объявленных в разметке, для недостающих микросхем отображаются пустые пробелы.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="1fbc7-231">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="1fbc7-233">Определяет строковый массив всплывающих подсказок палитры цветов для <code>ThemeColors</code> сетки.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="1fbc7-234">Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1fbc7-235">Используются только подсказки, необходимые для метки цветовых палитр, отображаемых в <code>ThemeColors</code> сетке.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="1fbc7-236">Если указано меньшее количество меток, чем число образцов в <code>ThemeColors</code> сетке, для образцов ремаинининг предоставляется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="1fbc7-237">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="1fbc7-239">Определяет метку для категории <strong>цветов темы</strong> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="1fbc7-240">Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="1fbc7-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="1fbc7-241">Это единственный шаблон, содержащий помеченные категории.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-242">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbc7-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="1fbc7-244">Определяет строку символов для описания подсказки, связанной с <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-245">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbc7-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="1fbc7-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="1fbc7-247">Определяет строку символов для всплывающей подсказки команды.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="1fbc7-248">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="1fbc7-249">Обработчики команд</span><span class="sxs-lookup"><span data-stu-id="1fbc7-249">Command handlers</span></span>

<span data-ttu-id="1fbc7-250">Метод [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) используется для настройки палитры Drop-Down цветом с помощью перечисленных выше ключей свойств.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="1fbc7-251">В следующем примере показано, как задать образцы цветов для палитры Drop-Down цвета на основе предпочтения пользовательского стиля или сетки пользовательских образцов, объявленной в разметке.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



<span data-ttu-id="1fbc7-252">В следующем примере демонстрируется реализация метода [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) , который предоставляет цвет образца палитры Drop-Down цветов для приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1fbc7-253">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1fbc7-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fbc7-254">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="1fbc7-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="1fbc7-255">**Дропдовнколорпиккер, элемент разметки**</span><span class="sxs-lookup"><span data-stu-id="1fbc7-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="1fbc7-256">Свойства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="1fbc7-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="1fbc7-257">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="1fbc7-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="1fbc7-258">Пример Дропдовнколорпиккер</span><span class="sxs-lookup"><span data-stu-id="1fbc7-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

